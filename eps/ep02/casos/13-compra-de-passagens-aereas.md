# EP02 — Caso: Compra de passagens aéreas

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **sistema de venda de passagens aéreas** recebe compradores que pesquisam voos, reservam assentos e pagam. Cada compra ocupa uma unidade de **processamento** do sistema durante a operação. Em promoções, muitos compradores chegam ao mesmo tempo, e o sistema pode colocá-los em uma fila de espera virtual.

O objetivo do caso é simular o sistema de vendas para analisar o comportamento da fila de compradores e determinar a capacidade de processamento necessária para atender a demanda de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Comprador |
| Fila | Compradores aguardando na fila de espera virtual |
| Servidor | Unidade de processamento do sistema de vendas |
| Tempo de serviço | Tempo para concluir a compra: pesquisa, reserva e pagamento |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de compra de passagens aéreas, e o modelo deve incorporar os que forem relevantes para o problema:

- **Fila de espera virtual**: o sistema limita o número de compradores atendidos ao mesmo tempo e coloca os demais em espera.
- **Etapas em série**: pesquisa, reserva e pagamento usam recursos diferentes do sistema.
- **Estoque limitado**: os assentos de cada tarifa são limitados, e o comprador desiste quando a tarifa desejada se esgota.
- **Tempo de reserva**: o assento fica reservado por um tempo limitado durante a compra e volta ao estoque se o pagamento não for concluído.
- **Falha no pagamento**: parte dos pagamentos é recusada, e o comprador tenta novamente ou desiste.
- **Promoções**: chegada concentrada de compradores no início de uma promoção.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de compra de passagens aéreas faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
