# EP02 — Caso: Atendimento por chat de um banco

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **banco** atende clientes por **chat** no aplicativo. A conversa começa com um robô, que resolve as solicitações simples; as demais são transferidas para um **atendente**. Diferente de uma ligação, um atendente de chat conduz várias conversas ao mesmo tempo, alternando entre elas enquanto os clientes respondem.

O objetivo do caso é simular o atendimento por chat para analisar o comportamento da fila de conversas e determinar quantos atendentes, e com quantas conversas simultâneas cada um, são necessários para atender os clientes de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Conversa iniciada por um cliente |
| Fila | Conversas aguardando um atendente |
| Servidor | Atendente, que conduz várias conversas ao mesmo tempo |
| Tempo de serviço | Duração da conversa, da transferência pelo robô até o encerramento |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de atendimento por chat de um banco, e o modelo deve incorporar os que forem relevantes para o problema:

- **Atendimento simultâneo**: cada atendente atende até um número máximo de conversas ao mesmo tempo, e o tempo de cada conversa aumenta com o número de conversas em paralelo.
- **Triagem pelo robô**: o robô resolve uma parte das conversas e transfere as demais, o que é uma etapa anterior ao atendimento humano.
- **Assuntos**: assuntos diferentes, como cartão, contestação de compra e empréstimo, têm tempos de serviço distintos e podem ter filas próprias.
- **Abandono**: o cliente fecha o aplicativo quando a espera é longa ou deixa de responder durante a conversa.
- **Variação da chegada ao longo do tempo**: picos em horário comercial, no início do mês e em instabilidades do aplicativo.
- **Turnos**: a quantidade de atendentes muda ao longo do dia.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de atendimento por chat de um banco faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
