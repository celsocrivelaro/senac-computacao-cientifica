# EP02 — Caso: Fila de impressão de uma universidade

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Uma **universidade** oferece **impressoras** compartilhadas para alunos e funcionários. Os trabalhos de impressão enviados entram em uma fila e são impressos um de cada vez em cada impressora. O tempo de impressão depende do tamanho do trabalho, e falhas como falta de papel ou de toner interrompem a impressora até que alguém a reabasteça.

O objetivo do caso é simular o serviço de impressão para analisar o comportamento das filas de trabalhos e determinar quantas impressoras, e com que política de reabastecimento, são necessárias para atender os usuários de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Trabalho de impressão |
| Fila | Trabalhos aguardando impressão |
| Servidor | Impressora |
| Tempo de serviço | Tempo para imprimir o trabalho, proporcional ao número de páginas |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de fila de impressão de uma universidade, e o modelo deve incorporar os que forem relevantes para o problema:

- **Tamanho dos trabalhos**: os trabalhos variam de uma página a centenas de páginas, com tempos de serviço muito diferentes.
- **Escolha da impressora**: fila única para todas as impressoras ou uma fila por impressora escolhida pelo usuário.
- **Falhas e reabastecimento**: impressoras param por falta de papel, falta de toner ou atolamento, e ficam paradas até que um funcionário as atenda.
- **Recurso compartilhado**: um mesmo funcionário é responsável por reabastecer e reparar várias impressoras.
- **Variação da chegada ao longo do tempo**: picos nos dias que antecedem a entrega de trabalhos e nos intervalos entre aulas.
- **Política de atendimento**: ordem de chegada ou prioridade para trabalhos menores.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de fila de impressão de uma universidade faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
