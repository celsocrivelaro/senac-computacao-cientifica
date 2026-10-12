# EP02 — Caso: Estacionamento de shopping

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

O **estacionamento de um shopping** recebe carros que passam pela **cancela de entrada**, procuram uma **vaga**, permanecem enquanto os ocupantes estão no shopping e saem pela **cancela de saída** após o pagamento. A ocupação acumula ao longo do dia: quando as vagas se esgotam, os carros esperam por uma vaga livre e a fila pode chegar à rua.

O objetivo do caso é simular o estacionamento para analisar o comportamento das filas de entrada e de saída e da ocupação das vagas, e determinar a configuração de cancelas e de vagas que atende os clientes de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Carro |
| Fila | Filas das cancelas de entrada e de saída, e carros aguardando vaga livre |
| Servidor | Cancela de entrada, vaga e cancela de saída |
| Tempo de serviço | Tempo de passagem pela cancela e tempo de permanência na vaga |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de estacionamento de shopping, e o modelo deve incorporar os que forem relevantes para o problema:

- **Etapas em série**: entrada, busca de vaga, permanência e saída são etapas sucessivas com servidores diferentes.
- **Permanência longa**: o tempo de permanência na vaga é muito maior que o das cancelas e varia conforme o motivo da visita, como compras, cinema ou alimentação.
- **Capacidade limitada**: o número de vagas é fixo; quando todas estão ocupadas, os carros esperam ou desistem.
- **Formas de pagamento**: pagamento em caixa ou totem antes da saída, na cancela de saída ou por tag eletrônica, com tempos distintos.
- **Variação da chegada ao longo do tempo**: picos nos fins de semana, nos horários de refeição e em datas comemorativas.
- **Vagas especiais**: vagas reservadas para idosos, pessoas com deficiência e carros elétricos.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de estacionamento de shopping faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
