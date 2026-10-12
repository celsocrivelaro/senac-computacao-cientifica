# EP02 — Caso: Colheita em fazenda

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Na **colheita em uma fazenda**, os lotes de plantação ficam prontos para colher ao longo da safra e são colhidos por **colheitadeiras**. Um lote pronto que demora a ser colhido perde qualidade e produtividade, e a colheita depende do clima e do transporte da produção.

O objetivo do caso é simular a colheita para analisar o acúmulo de lotes prontos à espera de colheita e determinar quantas colheitadeiras são necessárias para colher a safra de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Lote de plantação pronto para colher |
| Fila | Lotes prontos aguardando colheita |
| Servidor | Colheitadeira |
| Tempo de serviço | Tempo de colheita do lote, incluindo o deslocamento da máquina até ele |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de colheita em fazenda, e o modelo deve incorporar os que forem relevantes para o problema:

- **Janela de colheita**: cada lote tem um período ideal de colheita; após esse período, há perda de produção.
- **Clima**: chuvas interrompem a colheita de todas as máquinas por um período.
- **Recurso compartilhado**: caminhões ou transbordos que levam a produção colhida são compartilhados entre as colheitadeiras.
- **Tamanho dos lotes**: lotes de áreas diferentes têm tempos de colheita distintos.
- **Falhas**: colheitadeiras quebram e ficam paradas durante o reparo.
- **Jornada de trabalho**: as máquinas operam apenas em certos horários do dia.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de colheita em fazenda faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
