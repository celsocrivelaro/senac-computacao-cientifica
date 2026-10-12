# EP02 — Caso: Fábrica de alimento

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Uma **fábrica de alimento** transforma ingredientes em produtos por meio de **processadores e fornos**. Os ingredientes passam por etapas como preparo, mistura e cozimento, e cada etapa tem capacidade e duração próprias. Os fornos costumam processar lotes, e o tempo que um ingrediente pode esperar entre etapas é limitado.

O objetivo do caso é simular a linha de produção para analisar o acúmulo de lotes entre as etapas e determinar a configuração de processadores e fornos que garante a produção desejada de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Lote de ingredientes |
| Fila | Lotes aguardando a próxima etapa de processamento |
| Servidor | Processador ou forno |
| Tempo de serviço | Duração do processamento ou do cozimento do lote |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de fábrica de alimento, e o modelo deve incorporar os que forem relevantes para o problema:

- **Etapas em série**: os lotes passam por várias etapas em ordem, com equipamentos diferentes em cada uma.
- **Processamento em lote**: fornos processam vários itens ao mesmo tempo, até a sua capacidade.
- **Tempo máximo de espera**: ingredientes perecíveis ou massas em fermentação não podem esperar além de um limite e são descartados.
- **Limpeza e troca de produto**: equipamentos param para limpeza ao trocar o produto fabricado.
- **Falhas**: equipamentos quebram e ficam parados durante o reparo.
- **Produtos diferentes**: produtos com receitas e tempos de processamento distintos compartilham os mesmos equipamentos.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de fábrica de alimento faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
