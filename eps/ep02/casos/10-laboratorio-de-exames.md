# EP02 — Caso: Laboratório de exames

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **laboratório de exames** recebe amostras de pacientes e as processa em **equipamentos de análise**. As amostras chegam ao longo do dia, aguardam a vez no equipamento adequado e o resultado tem um prazo de entrega. Exames urgentes concorrem com os de rotina pelos mesmos equipamentos.

O objetivo do caso é simular o laboratório para analisar o comportamento das filas de amostras e determinar quantos equipamentos são necessários para cumprir os prazos de entrega de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Amostra de exame de um paciente |
| Fila | Amostras aguardando análise |
| Servidor | Equipamento de análise |
| Tempo de serviço | Tempo de análise da amostra no equipamento |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de laboratório de exames, e o modelo deve incorporar os que forem relevantes para o problema:

- **Tipos de exame**: exames diferentes usam equipamentos diferentes e têm tempos de análise distintos.
- **Prioridade**: exames urgentes têm prioridade sobre os de rotina.
- **Processamento em lote**: alguns equipamentos analisam várias amostras de uma vez, até a sua capacidade.
- **Etapas em série**: recepção, preparo da amostra, análise e liberação do resultado são etapas sucessivas.
- **Calibração e manutenção**: equipamentos param periodicamente para calibração e manutenção.
- **Variação da chegada ao longo do tempo**: concentração das coletas nas primeiras horas da manhã.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de laboratório de exames faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
