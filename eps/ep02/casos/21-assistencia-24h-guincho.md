# EP02 — Caso: Assistência 24h / guincho

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **serviço de assistência 24h** atende motoristas com o veículo parado por pane, acidente ou pneu furado. O pedido de socorro é registrado em uma central e despachado para um **mecânico** ou um **guincho**, que se desloca até o local. Parte dos pedidos é resolvida no local pelo mecânico; os demais exigem que o veículo seja rebocado.

O objetivo do caso é simular o serviço de assistência para analisar o comportamento da fila de pedidos de socorro e determinar quantos mecânicos e guinchos são necessários para atender os motoristas de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Pedido de socorro de um motorista |
| Fila | Pedidos aguardando um mecânico ou um guincho |
| Servidor | Mecânico ou guincho |
| Tempo de serviço | Tempo de deslocamento até o veículo somado ao atendimento no local ou ao reboque até a oficina |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de assistência 24h, e o modelo deve incorporar os que forem relevantes para o problema:

- **Tipos de ocorrência**: pane elétrica, pneu furado, pane seca e acidente têm tempos de atendimento distintos e exigem recursos diferentes.
- **Resolução em etapas**: o mecânico tenta resolver no local; quando não consegue, o pedido volta para a fila à espera de um guincho.
- **Regiões**: os pedidos e as equipes estão distribuídos por regiões, e a distância afeta o tempo de serviço.
- **Prioridade**: situações de risco, como veículo parado em rodovia ou com crianças a bordo, têm prioridade.
- **Variação da chegada ao longo do tempo**: mais pedidos em feriados, em viagens de fim de ano e em dias de chuva.
- **Disponibilidade das equipes**: equipes próprias e prestadores terceirizados com disponibilidade que varia ao longo do dia.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de assistência 24h faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
