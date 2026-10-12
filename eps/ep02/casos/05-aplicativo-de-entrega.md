# EP02 — Caso: Aplicativo de entrega

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **aplicativo de entrega** recebe pedidos de clientes e os atribui a **entregadores**, que retiram a mercadoria no estabelecimento e a levam até o cliente. Quando não há entregador disponível, o pedido aguarda atribuição. O tempo total até a entrega depende da espera pela atribuição, do preparo do pedido e do deslocamento.

O objetivo do caso é simular o serviço de entregas para analisar o comportamento da fila de pedidos e determinar quantos entregadores são necessários para atender a demanda de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Pedido (mercadoria a ser entregue) |
| Fila | Pedidos aguardando atribuição a um entregador |
| Servidor | Entregador |
| Tempo de serviço | Tempo entre a atribuição do pedido e a entrega ao cliente, incluindo retirada e deslocamento |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de aplicativo de entrega, e o modelo deve incorporar os que forem relevantes para o problema:

- **Tempo de preparo**: o pedido só pode ser retirado depois de preparado pelo estabelecimento, o que é um estágio anterior à entrega.
- **Regiões**: os pedidos e os entregadores estão distribuídos em regiões, e a distância afeta o tempo de serviço.
- **Entregas agrupadas**: um entregador pode levar mais de um pedido na mesma viagem.
- **Disponibilidade dos entregadores**: entregadores entram e saem do aplicativo ao longo do dia, e a quantidade disponível varia.
- **Variação da chegada ao longo do tempo**: picos no horário das refeições e em dias de chuva ou de jogos.
- **Cancelamento**: o cliente cancela o pedido quando a espera ultrapassa o tempo que está disposto a aguardar.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de aplicativo de entrega faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
