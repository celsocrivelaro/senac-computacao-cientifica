# EP02 — Caso: Suporte de TI

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Uma **equipe de suporte de TI** recebe tíquetes com problemas e solicitações dos usuários de uma organização e os resolve por meio de **analistas de suporte**. Cada tíquete tem um prazo de atendimento conforme a sua prioridade, e tíquetes sem solução podem ser escalados para analistas mais especializados.

O objetivo do caso é simular o serviço de suporte para analisar o comportamento da fila de tíquetes e determinar quantos analistas, e em quais níveis, são necessários para cumprir os prazos de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Tíquete aberto por um usuário |
| Fila | Tíquetes aguardando um analista |
| Servidor | Analista de suporte |
| Tempo de serviço | Tempo de trabalho do analista até resolver ou escalar o tíquete |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de suporte de TI, e o modelo deve incorporar os que forem relevantes para o problema:

- **Níveis de suporte**: tíquetes não resolvidos no primeiro nível são escalados para o segundo ou o terceiro, com outros analistas.
- **Prioridade e prazo**: cada tíquete tem uma prioridade e um prazo de atendimento (*SLA*).
- **Categorias de tíquete**: solicitações simples e incidentes complexos têm tempos de serviço distintos.
- **Reabertura**: parte dos tíquetes resolvidos é reaberta e volta para a fila.
- **Incidentes em massa**: uma falha geral gera muitos tíquetes em pouco tempo.
- **Turnos**: a quantidade de analistas disponíveis muda ao longo do dia e da semana.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de suporte de TI faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
