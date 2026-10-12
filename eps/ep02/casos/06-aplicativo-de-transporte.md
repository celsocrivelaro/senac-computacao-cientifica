# EP02 — Caso: Aplicativo de transporte

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **aplicativo de transporte** recebe solicitações de corrida de passageiros e as atribui a **motoristas** disponíveis. Cada motorista atende um passageiro, ou um grupo, por vez. Quando não há motorista livre próximo, o passageiro aguarda ou desiste da corrida.

O objetivo do caso é simular o serviço de transporte para analisar o comportamento da fila de solicitações e determinar quantos motoristas são necessários para atender a demanda de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Passageiro que solicita uma corrida |
| Fila | Solicitações aguardando um motorista |
| Servidor | Motorista |
| Tempo de serviço | Tempo do deslocamento até o passageiro somado à duração da corrida |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de aplicativo de transporte, e o modelo deve incorporar os que forem relevantes para o problema:

- **Regiões**: passageiros e motoristas estão distribuídos em regiões, e o motorista termina a corrida em outra região, mudando a oferta local.
- **Disponibilidade dos motoristas**: motoristas entram e saem do aplicativo ao longo do dia.
- **Recusa de corridas**: o motorista pode recusar uma solicitação, que volta para a fila.
- **Preço dinâmico**: o aumento do preço em momentos de alta demanda reduz a chegada de solicitações e atrai motoristas.
- **Variação da chegada ao longo do tempo**: picos nos horários de ida e volta do trabalho, à noite nos fins de semana e em eventos.
- **Desistência**: o passageiro cancela a solicitação quando a espera é longa.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de aplicativo de transporte faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
