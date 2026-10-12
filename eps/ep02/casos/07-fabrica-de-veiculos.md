# EP02 — Caso: Fábrica de veículos

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Uma **fábrica de veículos** monta carros em uma linha de produção composta por estações, cada uma com **máquinas** que executam uma etapa da montagem. Um carro passa pelas estações em sequência, e uma estação mais lenta ou parada acumula carros à sua frente e deixa as estações seguintes ociosas.

O objetivo do caso é simular a linha de produção para analisar o acúmulo de carros entre as estações e determinar a configuração de máquinas que garante a produção desejada de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Carro em montagem |
| Fila | Carros aguardando a próxima estação (estoque intermediário) |
| Servidor | Máquina de uma estação de montagem |
| Tempo de serviço | Tempo de execução da etapa de montagem na máquina |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de fábrica de veículos, e o modelo deve incorporar os que forem relevantes para o problema:

- **Etapas em série**: cada carro passa por várias estações em ordem, e a saída de uma é a entrada da seguinte.
- **Estoque intermediário limitado**: o espaço entre estações comporta um número limitado de carros; quando ele enche, a estação anterior para (bloqueio).
- **Falhas e manutenção**: máquinas quebram em intervalos aleatórios e ficam paradas durante o reparo.
- **Modelos diferentes**: modelos ou versões de carro com tempos de montagem distintos em algumas estações.
- **Retrabalho**: carros reprovados na inspeção voltam para uma estação anterior.
- **Máquinas em paralelo**: estações com mais de uma máquina para aumentar a capacidade.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de fábrica de veículos faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
