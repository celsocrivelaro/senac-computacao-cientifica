# EP02 — Caso: Pronto-Socorro

Este documento descreve o caso atribuído ao grupo. Ele complementa o enunciado geral do EP02, que define os conceitos, os experimentos, a forma de entrega e as políticas. Em caso de dúvida, vale o enunciado geral.

## O problema

Um **pronto-socorro** recebe pacientes sem agendamento, que passam por triagem e são atendidos por **médicos e enfermeiros**. O atendimento não segue apenas a ordem de chegada: pacientes mais graves têm prioridade. Quando a equipe é insuficiente, a espera dos casos menos graves pode se estender por horas.

O objetivo do caso é simular o pronto-socorro para analisar o comportamento das filas de atendimento e determinar a composição da equipe que atende os pacientes de forma satisfatória.

## Elementos do modelo

| Elemento do sistema de filas | No caso |
|------------------------------|---------|
| Usuário | Paciente |
| Fila | Pacientes aguardando triagem ou atendimento |
| Servidor | Médico ou enfermeiro |
| Tempo de serviço | Duração da triagem ou do atendimento |

## Características a investigar na pesquisa

A pesquisa do tema deve levantar como estes aspectos se apresentam em situações reais de pronto-socorro, e o modelo deve incorporar os que forem relevantes para o problema:

- **Triagem e classificação de risco**: os pacientes passam por triagem e recebem uma prioridade, que define a ordem de atendimento.
- **Prioridade**: pacientes graves são atendidos antes, mesmo que tenham chegado depois.
- **Etapas em série**: triagem, atendimento médico, exames e medicação são etapas sucessivas, com servidores diferentes.
- **Recursos compartilhados**: leitos, salas e equipamentos são compartilhados e podem limitar o atendimento.
- **Variação da chegada ao longo do tempo**: horários e dias da semana com mais procura, e surtos sazonais de doenças.
- **Desistência**: pacientes de baixa prioridade deixam o pronto-socorro sem atendimento após longa espera.

A lista acima é um repertório de aspectos a reconhecer no problema real; não é necessário modelar todos.

## Cenários e perguntas da análise

O mapeamento dos três cenários exigidos no enunciado geral (caso base, caso com volume e caso extremo) para situações reais de pronto-socorro faz parte do exercício: cabe ao grupo identificar, a partir da pesquisa, as situações que representam cada cenário.

Da mesma forma, cabe ao grupo formular as perguntas que a análise dos cenários deve responder sobre o caso, e respondê-las com os resultados da simulação.
