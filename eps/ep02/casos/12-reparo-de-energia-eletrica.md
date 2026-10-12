# EP02 — Caso: Reparo de energia elétrica

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Uma **distribuidora de energia elétrica** recebe solicitações de reparo quando há falta de energia ou falhas na rede, e as atende com **equipes de reparo** que se deslocam até o local. Enquanto a solicitação não é atendida, os clientes da região ficam sem energia.

O objetivo do caso é simular o serviço de reparo para analisar o comportamento da fila de solicitações e determinar quantas equipes são necessárias para restabelecer a energia de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Solicitação de reparo |
| Fila | Solicitações aguardando uma equipe |
| Servidor | Equipe de reparo |
| Tempo de serviço | Tempo de deslocamento da equipe até o local somado à duração do reparo |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de reparo de energia elétrica, e o modelo deve incorporar os que forem relevantes para o problema:

- **Prioridade**: solicitações que afetam hospitais, serviços essenciais ou muitos clientes têm prioridade.
- **Tipos de ocorrência**: ocorrências diferentes, como troca de fusível ou queda de poste, têm tempos de reparo distintos.
- **Regiões**: as solicitações e as equipes estão distribuídas por regiões, e a distância afeta o tempo de serviço.
- **Eventos climáticos**: tempestades geram muitas solicitações em um curto intervalo de tempo.
- **Turnos**: a quantidade de equipes disponíveis muda ao longo do dia.
- **Solicitações duplicadas**: vários clientes da mesma região abrem solicitações para a mesma ocorrência.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de reparo de energia elétrica faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
