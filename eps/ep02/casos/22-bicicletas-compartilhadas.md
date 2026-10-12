# EP02 — Caso: Bicicletas compartilhadas

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **sistema de bicicletas compartilhadas** distribui **bicicletas** em estações espalhadas pela cidade. O usuário retira uma bicicleta em uma estação, pedala até o destino e a devolve em outra estação. Como os deslocamentos não são simétricos, algumas estações esvaziam e outras lotam ao longo do dia, e equipes de redistribuição levam bicicletas de umas para outras.

O objetivo do caso é simular o sistema para analisar a disponibilidade de bicicletas e de vagas nas estações e determinar a quantidade de bicicletas e a política de redistribuição que atendem os usuários de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Usuário que quer retirar uma bicicleta |
| Fila | Usuários aguardando bicicleta em uma estação vazia, ou aguardando vaga para devolver em uma estação cheia |
| Servidor | Bicicleta |
| Tempo de serviço | Duração da viagem, da retirada até a devolução |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de bicicletas compartilhadas, e o modelo deve incorporar os que forem relevantes para o problema:

- **Servidor que se desloca**: a bicicleta termina o serviço em outra estação, e a oferta de cada estação muda a cada viagem.
- **Capacidade das estações**: cada estação tem um número limitado de vagas; com a estação cheia, o usuário não consegue devolver a bicicleta.
- **Fluxos assimétricos**: de manhã os deslocamentos vão dos bairros para o centro e, à tarde, o inverso.
- **Redistribuição**: equipes com caminhões levam bicicletas de estações cheias para estações vazias, com capacidade e tempo de deslocamento próprios.
- **Manutenção**: bicicletas com defeito ficam indisponíveis até serem recolhidas e reparadas.
- **Desistência**: o usuário que não encontra bicicleta vai a outra estação ou desiste da viagem.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de bicicletas compartilhadas faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
