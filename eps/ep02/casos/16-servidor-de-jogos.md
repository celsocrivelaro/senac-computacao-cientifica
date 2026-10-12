# EP02 — Caso: Servidor de Jogos

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **jogo on-line** mantém **servidores de jogos** que hospedam as partidas. Os jogadores que se conectam entram em uma fila de pareamento até que haja jogadores suficientes e um servidor livre para iniciar uma partida. Quando os servidores estão lotados, a espera aumenta e os jogadores desistem.

O objetivo do caso é simular a infraestrutura do jogo para analisar o comportamento da fila de jogadores e determinar quantos servidores são necessários para atender os jogadores de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Jogador que se conecta |
| Fila | Jogadores aguardando pareamento ou vaga em um servidor |
| Servidor | Servidor de jogo, que hospeda partidas |
| Tempo de serviço | Duração de uma partida |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de servidor de jogos, e o modelo deve incorporar os que forem relevantes para o problema:

- **Pareamento**: uma partida só começa quando há um número mínimo de jogadores, o que é um atendimento em grupo.
- **Capacidade dos servidores**: cada servidor hospeda um número limitado de partidas ou de jogadores ao mesmo tempo.
- **Escalonamento automático**: novos servidores podem ser iniciados quando a fila cresce, com um tempo de inicialização.
- **Regiões**: jogadores e servidores estão em regiões diferentes, e o pareamento prefere jogadores da mesma região.
- **Variação da chegada ao longo do tempo**: picos à noite, nos fins de semana e no lançamento de atualizações.
- **Desistência e quedas**: jogadores desistem da fila, e servidores podem cair, encerrando as partidas em andamento.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de servidor de jogos faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
