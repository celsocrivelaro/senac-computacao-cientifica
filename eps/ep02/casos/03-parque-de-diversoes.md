# EP02 — Caso: Parque de diversões

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **parque de diversões** reúne **brinquedos** com capacidade e duração de ciclo próprias. Os frequentadores entram na fila de um brinquedo, embarcam em grupos a cada ciclo e, ao sair, escolhem o próximo brinquedo. A fila de cada brinquedo depende da sua capacidade, da duração do ciclo e da atratividade em relação aos demais.

O objetivo do caso é simular o parque para analisar o comportamento das filas dos brinquedos e determinar a configuração de brinquedos e de capacidade que mantém as filas em tamanho satisfatório.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Frequentador do parque |
| Fila | Fila de cada brinquedo |
| Servidor | Brinquedo, que atende um grupo de frequentadores por ciclo |
| Tempo de serviço | Duração de um ciclo do brinquedo, incluindo embarque e desembarque |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de parque de diversões, e o modelo deve incorporar os que forem relevantes para o problema:

- **Atendimento em lote**: o brinquedo atende vários frequentadores ao mesmo tempo, até a sua capacidade, e só inicia o ciclo seguinte quando o anterior termina.
- **Escolha do brinquedo**: a forma como o frequentador escolhe o próximo brinquedo, por exemplo pela atratividade ou pelo tamanho da fila.
- **Chegada em grupos**: famílias e grupos de amigos chegam juntos e entram juntos nas filas.
- **Fila prioritária**: ingressos que dão acesso a uma fila rápida, com prioridade sobre a fila comum.
- **Desistência**: o frequentador desiste da fila quando ela está grande demais e vai para outro brinquedo.
- **Paradas**: brinquedos param para manutenção ou por condições do tempo, como chuva.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de parque de diversões faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
