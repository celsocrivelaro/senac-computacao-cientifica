# EP02 — Caso: Compra de ingresso para cinema

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **cinema** vende ingressos para as sessões por meio de bilheterias, totens de autoatendimento e venda pela internet, todos dependentes do **processamento** da venda. A procura se concentra nos minutos que antecedem as sessões, e o comprador que não consegue o ingresso a tempo perde o início do filme ou desiste.

O objetivo do caso é simular a venda de ingressos para analisar o comportamento das filas de compradores e determinar a capacidade de atendimento necessária para vender os ingressos de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Comprador de ingresso |
| Fila | Compradores aguardando atendimento |
| Servidor | Ponto de venda: bilheteria, totem ou processamento da venda pela internet |
| Tempo de serviço | Tempo para escolher a sessão e o assento e pagar |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de compra de ingresso para cinema, e o modelo deve incorporar os que forem relevantes para o problema:

- **Canais de venda**: bilheteria, totem e internet têm tempos de serviço distintos e podem ter filas próprias.
- **Horário das sessões**: as chegadas se concentram nos minutos que antecedem cada sessão.
- **Lotação das salas**: cada sessão tem um número limitado de assentos, e o comprador desiste quando ela esgota.
- **Compra em grupo**: compradores que compram vários ingressos de uma vez.
- **Estreias**: chegada concentrada de compradores na abertura das vendas de uma estreia.
- **Desistência**: o comprador desiste quando a fila não permite chegar a tempo para a sessão.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de compra de ingresso para cinema faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
