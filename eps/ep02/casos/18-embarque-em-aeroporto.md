# EP02 — Caso: Embarque em aeroporto

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

O **embarque em um aeroporto** é um processo em etapas: o passageiro despacha a bagagem no **balcão de *check-in***, passa pela **inspeção de segurança** (raio-X) e aguarda no **portão de embarque**. Cada etapa tem servidores e tempos de serviço próprios, e o passageiro precisa concluir todas antes do horário de fechamento do voo.

O objetivo do caso é simular o embarque para analisar o comportamento das filas em cada etapa e determinar quantos balcões e canais de inspeção são necessários para que os passageiros embarquem a tempo de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Passageiro |
| Fila | Filas do *check-in*, da inspeção de segurança e do portão de embarque |
| Servidor | Balcão de *check-in*, canal de inspeção de segurança e portão de embarque |
| Tempo de serviço | Duração do atendimento em cada etapa |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de embarque em aeroporto, e o modelo deve incorporar os que forem relevantes para o problema:

- **Etapas em série**: o passageiro passa pelo *check-in*, pela inspeção de segurança e pelo portão, nessa ordem, e cada etapa tem os seus servidores.
- **Prazo do voo**: o passageiro precisa chegar ao portão antes do fechamento do voo; quem não chega perde o embarque.
- **Chegada antecipada**: os passageiros chegam com antecedências diferentes em relação ao horário do voo.
- **Tipos de passageiro**: passageiros sem bagagem despachada ou com *check-in* on-line pulam a primeira etapa.
- **Filas prioritárias**: passageiros prioritários e de classes superiores têm filas próprias em algumas etapas.
- **Recurso compartilhado**: balcões e canais de inspeção atendem passageiros de vários voos, cujos horários se concentram em ondas ao longo do dia.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de embarque em aeroporto faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
