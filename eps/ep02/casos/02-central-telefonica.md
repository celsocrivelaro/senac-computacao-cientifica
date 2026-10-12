# EP02 — Caso: Central Telefônica

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Uma **central telefônica de atendimento** (*call center*) recebe ligações de clientes e as distribui entre **atendentes**. Cada atendente conversa com um cliente por vez. Quando não há atendente livre, a ligação é colocada em espera, e o cliente pode desligar se a espera for longa.

O objetivo do caso é simular a central de atendimento para analisar o comportamento da fila de espera e determinar quantos atendentes são necessários para atender as ligações de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Ligação de um cliente |
| Fila | Ligações em espera na central |
| Servidor | Atendente |
| Tempo de serviço | Duração da conversa entre o atendente e o cliente |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de central telefônica, e o modelo deve incorporar os que forem relevantes para o problema:

- **Menu de opções (URA)**: a unidade de resposta audível direciona a ligação para filas de assuntos diferentes, como vendas, suporte e cancelamento, cada uma com seus atendentes.
- **Abandono**: o cliente desliga após um tempo de espera que varia de cliente para cliente; a ligação abandonada sai do sistema sem ser atendida.
- **Rechamada**: parte dos clientes que abandonam a ligação liga novamente algum tempo depois.
- **Turnos**: a quantidade de atendentes muda ao longo do dia conforme a escala de trabalho, incluindo pausas e intervalos.
- **Variação da chegada ao longo do tempo**: horários de pico diários e dias de maior volume, como o vencimento de faturas.
- **Transferência**: parte das ligações é transferida para outra fila ou para um atendente especializado, voltando a esperar.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de central telefônica faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
