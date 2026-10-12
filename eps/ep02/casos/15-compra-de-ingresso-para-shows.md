# EP02 — Caso: Compra de ingresso para shows

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **sistema de venda de ingressos para shows** recebe compradores que escolhem setor e quantidade e pagam. Cada compra ocupa uma unidade de **processamento** do sistema. Na abertura das vendas de um show concorrido, a procura supera em muito a capacidade, e o sistema coloca os compradores em uma fila de espera virtual.

O objetivo do caso é simular o sistema de vendas para analisar o comportamento da fila de compradores e determinar a capacidade de processamento necessária para atender a demanda de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Comprador |
| Fila | Compradores aguardando na fila de espera virtual |
| Servidor | Unidade de processamento do sistema de vendas |
| Tempo de serviço | Tempo para concluir a compra: escolha do setor, reserva e pagamento |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de compra de ingresso para shows, e o modelo deve incorporar os que forem relevantes para o problema:

- **Fila de espera virtual**: o sistema limita o número de compradores atendidos ao mesmo tempo e coloca os demais em espera.
- **Abertura das vendas**: grande volume de compradores chega no instante em que as vendas abrem.
- **Estoque por setor**: cada setor tem um número limitado de ingressos, e o comprador desiste ou muda de setor quando o desejado esgota.
- **Pré-venda**: grupos de compradores com acesso antecipado às vendas.
- **Limite por comprador**: limite de ingressos por compra.
- **Abandono e tempo de reserva**: compradores abandonam a fila virtual, e ingressos reservados voltam ao estoque se o pagamento não for concluído a tempo.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de compra de ingresso para shows faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
