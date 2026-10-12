# EP02 — Caso: Postos de distribuição

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **posto de distribuição** (centro de distribuição) recebe caminhões que vêm carregar ou descarregar mercadorias. Cada caminhão ocupa uma **doca** durante a operação. Quando todas as docas estão ocupadas, os caminhões aguardam no pátio, e o tempo parado tem custo para a transportadora e para o posto.

O objetivo do caso é simular o posto de distribuição para analisar o comportamento da fila de caminhões e determinar quantas docas, e com que recursos, são necessárias para atender a demanda de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Caminhão que chega para carga ou descarga |
| Fila | Caminhões aguardando no pátio |
| Servidor | Doca |
| Tempo de serviço | Tempo de carga ou descarga do caminhão na doca |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de posto de distribuição, e o modelo deve incorporar os que forem relevantes para o problema:

- **Agendamento**: parte dos caminhões chega em horários agendados e parte chega sem agendamento.
- **Tipos de operação**: carga e descarga, e tipos de caminhão diferentes, têm tempos de serviço distintos.
- **Recurso compartilhado**: empilhadeiras e equipes de conferência são compartilhadas entre as docas e podem ser o gargalo do sistema.
- **Docas especializadas**: docas destinadas a certos tipos de caminhão ou de carga, como carga refrigerada.
- **Capacidade do pátio**: o pátio comporta um número limitado de caminhões em espera.
- **Turnos e janelas de operação**: horários de funcionamento e mudanças de equipe ao longo do dia.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de posto de distribuição faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
