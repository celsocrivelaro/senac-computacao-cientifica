# EP02 — Caso: Pedágio

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Uma **praça de pedágio** é um ponto de uma rodovia em que os veículos param, ou reduzem a velocidade, para pagar a tarifa de uso da via. A praça é composta por um conjunto de **cabines**, cada uma atendendo um veículo por vez. Quando a taxa de chegada de veículos supera a capacidade de atendimento das cabines abertas, formam-se filas que podem se estender por quilômetros na rodovia.

O objetivo do caso é simular a praça de pedágio para analisar o comportamento das filas e determinar quantas cabines, e de que tipo, são necessárias para atender o fluxo de veículos de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No pedágio |
|------------------------------|------------|
| Usuário | Veículo (carro, moto, caminhão, ônibus) |
| Fila | Fila de veículos diante de cada cabine, ou fila única antes da praça |
| Servidor | Cabine de cobrança |
| Tempo de serviço | Tempo entre a parada do veículo na cabine e a liberação da cancela |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em praças de pedágio reais, e o modelo deve incorporar os que forem relevantes para o problema:

- **Tipos de cabine**: cabines manuais (pagamento em dinheiro, cartão ou PIX) e cabines automáticas (tag eletrônica), com tempos de serviço distintos.
- **Categorias de veículos**: veículos de categorias diferentes podem ter tempos de serviço diferentes, e veículos sem tag não podem usar as cabines automáticas.
- **Escolha da fila**: a forma como o motorista escolhe a cabine, por exemplo a fila mais curta entre as compatíveis com o seu meio de pagamento.
- **Variação da chegada ao longo do tempo**: horários de pico diários, fins de semana e feriados.
- **Abertura e fechamento de cabines**: a operadora pode abrir cabines adicionais quando a fila cresce e fechá-las quando o fluxo diminui.
- **Falhas**: problemas na leitura da tag, falta de troco ou cancela travada, que aumentam o tempo de serviço de um veículo ou interrompem uma cabine.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais do pedágio faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre a praça de pedágio, e respondê-las com os resultados da simulação.
