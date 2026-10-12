# EP 2 - Simulação Discreta

## Objetivo

O objetivo deste EP é fazer simulações computacionais discretas. Na computação científica, computadores são excelentes para fazer simulações de casos em que a modelagem matemática não é suficiente para analisar um problema. 

Uma simulação discreta reproduz no computador a evolução de um sistema como uma sequência de eventos, como chegadas, atendimentos e saídas, que ocorrem em instantes distintos, o que permite testar diferentes configurações e cenários do sistema sem precisar alterá-lo na realidade.

A partir dos conceitos de sistemas de filas, recursos e consumidores, cada grupo deve construir um ambiente simulado de um problema real. A chegada dos usuários e o tempo de consumo de cada serviço devem ser aleatórios, segundo funções de probabilidade definidas pelo grupo para o problema do seu tema. Sobre o ambiente simulado, o grupo deve produzir gráficos de análise, ajustar os parâmetros do sistema e analisar as variações resultantes de cada ajuste.

O tema de cada grupo é proposto pelo professor.

A simulação deve ser implementada em Python com a biblioteca [SimPy](https://simpy.readthedocs.io/), de uso obrigatório.

## Conceitos

- **Simulação de eventos discretos** (*discrete-event simulation*): técnica em que o estado do sistema muda apenas em instantes discretos, nos quais ocorrem eventos; entre dois eventos consecutivos, o estado permanece constante.
- **Relógio de simulação**: variável que registra o tempo simulado; avança de um evento para o próximo, e não em passos fixos de tempo real.
- **Evento**: ocorrência instantânea que altera o estado do sistema, como a chegada de um usuário, o início ou o fim de um atendimento, uma desistência ou uma falha de servidor.
- **Usuário** (ou entidade, consumidor): elemento que chega ao sistema, aguarda e consome um serviço. Ex.: carros em um pedágio, pacientes em um pronto-socorro.
- **Fila**: conjunto ordenado de usuários que aguardam atendimento.
- **Servidor** (ou recurso): elemento que presta o serviço a um usuário por vez, durante um tempo de serviço. Ex.: cabines de pedágio, médicos.
- **Disciplina de atendimento**: regra que define o próximo usuário a ser atendido; a mais comum é FIFO (*First-In, First-Out*).
- **Taxa de chegada**: número médio de usuários que chegam ao sistema por unidade de tempo.
- **Tempo de serviço**: duração do atendimento de um usuário por um servidor.
- **Desistência**: saída de um usuário do sistema antes de ser atendido.

Premissas:

- Geralmente as filas são FIFO (*First-In, First-Out*), mas pode haver situações com outras disciplinas de atendimento
- Usuários podem chegar em grupos
- Podemos ter configurações distintas aos problemas: 1 fila para vários servidores ou várias filas para vários servidores
- Pode ou não haver um recurso compartilhado entre os servidores
- Os usuários podem desistir da fila a depender do problema

Tente pensar situações comuns para cada problema. Os valores devem mudar de problema a problema:

- O tempo de serviço pode variar.  No problema de pesagem de caminhões, a balança pode demorar para pesar mais uns caminhões do que outros por alguma distribuição de probabilidade
- A chegada de usuário pode mudar pelo tempo. Por exemplo, um serviço bancário pode ter picos em alguns horários
- Desistência de usuários se a fila está muito grande. No caso de fila de compra de ingressos, alguém pode desistir quando o tamanho da fila está grande
- Falhas no servidor como quebras, paradas ou mesmo desligamento de um servidor

O que deverá ser medido:

- Tempos que os usuários demoram no sistema e nas filas
- Tamanho das filas e variações pelo tempo
- Desistências ou Tempos críticos na fila
- Quantos servidores são necessários para atender as filas de forma satisfatória.

## **🧠 Variação obrigatória**

Cada grupo deve implementar ao menos **um dos seguintes aspectos**. A lista é um repertório de opções; não é necessário implementar todos:

1. **Política de atendimento**: FIFO, prioridade, round-robin, etc.
2. **Capacidade limitada**: filas com tamanho máximo.
3. **Eventos aleatórios**: falhas, atrasos, desistências.
4. **Múltiplas etapas**: serviço em série (ex: triagem → atendimento → saída).
5. **Recursos compartilhados**: servidores que atendem diferentes filas ou precisam compartilhar um recurso entre eles

## 📦 A Entrega

### Explicação do tema

Faça uma pesquisa detalhada sobre o tema, que deve conter:

- A descrição do processo real: como os usuários chegam, como são atendidos e quais problemas de fila ocorrem na prática
- Ao menos 3 fontes citadas com referência completa (artigos, estudos, reportagens, relatórios técnicos ou dados públicos)
- Os valores usados como parâmetros do modelo (taxa de chegada, tempo de serviço, número de servidores), indicando a origem de cada um: fonte citada, observação própria ou estimativa justificada

### Modelagem

Explique quem é quem usando o modelo: Usuários, Filas, Consumidores, Pausas, etc.

### Experimentos

São esperados 3 cenários, pensados a partir do problema base do tema. Exemplo, para um supermercado:

- **Caso base**: o mercado em um dia normal de uso. Serve para explicar as configurações e o modelo do problema: usuários, filas, servidores, etc.
- **Caso com volume** (a depender do estudo de caso): o mercado em horário de pico. Mostrar como o problema se modifica quando há um volume considerável, mas os servidores ainda conseguem dar conta do atendimento, e quanto de fila é aceitável.
- **Caso extremo**: o mercado antes do Natal. Mostrar o problema em congestionamento, as filas crescendo nos momentos de maior movimento e como o sistema se recupera.

Para cada cenário, explicar as configurações:

1) A função de probabilidade da chegada dos usuários: a distribuição, os valores dos parâmetros e por que ela representa as chegadas do tema
2) A função de probabilidade do tempo de serviço de cada usuário: a distribuição, os valores dos parâmetros e por que ela representa o atendimento do tema
3) Desistências ou marcações críticas de acordo com o tamanho da fila, se aplicável
4) O tempo simulado
5) A quantidade de servidores ao mesmo tempo, ou a variação dessa quantidade ao longo do tempo

Para cada cenário, plotar:

- Tamanho das filas ao longo do tempo
- Quantidade de usuários no sistema ao longo do tempo
- Tempo que cada usuário fica na fila e no sistema (da entrada à saída)
- Tempo de trabalho de cada servidor ao longo do tempo
- Desistências ao longo do tempo, se houver

Ao final, apresentar as conclusões tiradas dos cenários: como seria a configuração ideal de filas e de recursos para o problema.

### Código-fonte

- Utilizar Google Colab, Python e SimPy.
- Entregar apenas o arquivo `.ipynb` do notebook.
- O notebook deve conter as explicações sobre o problema em formato texto e os gráficos que mostram as variações entre os cenários.

Dica: diagramas podem ser feitos em ASCII art. Ferramentas de IA são ótimas para isso.

### Apresentação

A apresentação do trabalho deve ser feita em um vídeo no YouTube, no modo "Não listado" (não usar o modo "Privado"), com duração de 5 a 15 minutos. Não marcar o vídeo como "conteúdo para crianças", pois isso restringe o acesso.

Utilize imagens e slides para auxiliar na explicação.

Utilize o código e gráficos nas explicações.

## Políticas

Este trabalho está sujeito às seguintes políticas:

- [O que é e não é avaliado em vídeos](https://github.com/celsocrivelaro/senac-computacao-cientifica/blob/main/politicas/videos.md)
- [Política de uso de ferramentas generativas de IA](https://github.com/celsocrivelaro/senac-computacao-cientifica/blob/main/politicas/ia-generativa.md)
- [Política antiplágio](https://github.com/celsocrivelaro/senac-computacao-cientifica/blob/main/politicas/antiplagio.md)