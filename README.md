# MK-AI
An AI that can play  Mortal Kombat II - Genesis
<a name="br1"></a> 

**Mortal Kombat 2**

<b>Henrique Andrade Lopes<sup>1</sup>, Saulo Henrique R. Barbosa<sup>1</sup></b>

<sup>1</sup>DPI – Universidade Federal de Viçosa (UFV)

Campus Universitário - 36570-900, Viçosa, MG – Brasil

{henrique.a.lopes,saulo.h.barbosa}@ufv.br

***Abstract.** This report describes the development of an artiﬁcial intelligence*

*(AI) agent to play Mortal Kombat 2, a renowned ﬁghting game. The project's*

*objective was to create an autonomous agent capable of making strategic*

*decisions and adapting to the opponent's skills using reinforcement learning*

*techniques. The agent was trained using the Proximal Policy Optimization*

*(PPO) algorithm and optimized with the assistance of Optuna to ﬁnd the best*

*hyperparameters. The results demonstrated a signiﬁcant evolution of the agent*

*throughout the training, showcasing its ability to learn and improve its*

*performance.*

***Resumo.** Este relatório descreve o desenvolvimento de um agente de*

*inteligência artiﬁcial (IA) para jogar Mortal Kombat 2, um renomado jogo de*

*luta. O objetivo do projeto foi criar um agente autônomo capaz de tomar*

*decisões estratégicas e adaptar-se às habilidades do oponente, utilizando*

*técnicas de aprendizado por reforço. O agente foi treinado utilizando o*

*algoritmo Proximal Policy Optimization (PPO) e otimizado com o auxílio do*

*Optuna para encontrar os melhores hiperparâmetros. Os resultados*

*mostraram uma evolução signiﬁcativa do agente ao longo do treinamento,*

*demonstrando sua capacidade de aprender e melhorar seu desempenho.*

**1. Introdução**

Com o avanço da inteligência artiﬁcial (IA) e o crescente interesse em sua aplicação em

jogos, surgem desaﬁos cada vez mais complexos para o desenvolvimento de agentes

autônomos capazes de competir e vencer adversários virtuais ou humanos. Neste

contexto, o presente trabalho aborda a criação de um agente de IA com o objetivo de

jogar Mortal Kombat 2, um renomado jogo de luta. O desenvolvimento de um agente

que possa tomar decisões estratégicas e adaptar-se às habilidades do oponente

representa um desaﬁo relevante no campo da IA e oferece um ambiente propício para a

aplicação de técnicas de aprendizado por reforço.

**1.1. Motivação**

O interesse em desenvolver uma inteligência artiﬁcial capaz de jogar Mortal Kombat 2 é

impulsionado por várias razões. Primeiramente, o jogo é um desaﬁo complexo que

exige habilidades de tomada de decisão em tempo real, estratégias de combate e reações

rápidas. O desenvolvimento de um agente de IA competente nesse contexto não só

demonstra a capacidade da IA de enfrentar desaﬁos em ambientes dinâmicos, mas

também pode fornecer insights valiosos para o aprimoramento de técnicas de

aprendizado por reforço.



<a name="br2"></a> 

Além do desaﬁo técnico e cientíﬁco, há também um aspecto cultural envolvido

nesse projeto. Mortal Kombat 2 é uma parte importante da história dos videogames e é

uma franquia popular até os dias de hoje. Ao desenvolver uma IA capaz de jogar esse

jogo de forma competente, estamos contribuindo para a divulgação da inteligência

artiﬁcial e fomentando o interesse por parte das futuras gerações mostrando como a

inteligência artiﬁcial pode ser aplicada em áreas de entretenimento.

**2. Metodologia**

Neste trabalho, utilizamos a técnica de Aprendizado por Reforço para treinar um agente

de IA capaz de jogar Mortal Kombat 2. A aprendizagem por reforço é uma abordagem

em que o agente interage com um ambiente e recebe recompensas ou punições com

base em suas ações, com o objetivo de aprender uma política de ação que maximize as

recompensas a longo prazo.

No escopo do jogo proposto, o agente precisa tomar decisões estratégicas em

tempo real, adaptar-se às ações do oponente e aprender a utilizar golpes especiais,

combos e defesas para vencer as partidas. Para alcançar esse objetivo, utilizamos o

algoritmo Proximal Policy Optimization (PPO)[1], um método de otimização de

políticas que busca melhorar gradualmente as estratégias de ação do agente.

Utilizamos a "CnnPolicy"[2], que é uma política baseada em redes neurais

convolucionais (CNNs) que é comumente usada em algoritmos de aprendizado por

reforço, como o PPO, para tomar decisões em ambientes de jogos. As CNNs são um

tipo de arquitetura de rede neural especialmente adequada para processar dados de

entrada com estrutura espacial, como imagens.

**3. Pré-processamento dos dados**

Realizamos um pré-processamento dos dados de entrada para reduzir a

dimensionalidade e tornar o treinamento mais eﬁciente. Nesse pré-processamento, as

informações visuais do jogo foram convertidas para uma representação em preto e

branco, e apenas os pixels que sofreram modiﬁcações entre frames foram utilizados

como entrada para a IA. Isso permitiu que a IA considerasse apenas as informações

relevantes para a tomada de decisão, reduzindo a complexidade do problema.

**3.1. Otimizações**

Para otimizar ainda mais o desempenho do agente, utilizamos o Optuna[3], uma

ferramenta de otimização de hiperparâmetros. O Optuna automatiza a busca pelos

melhores valores de hiperparâmetros para o treinamento do agente, explorando

diferentes combinações e avaliando o desempenho da IA em cada iteração. Dessa

forma, podemos encontrar conﬁgurações ideais que maximizem a taxa de vitórias do

agente em Mortal Kombat 2.

**4. Resultados**

Durante o treinamento do agente de IA em Mortal Kombat 2, realizamos análises e

coletamos evidências para fundamentar o objetivo do nosso trabalho. Uma das

principais métricas utilizadas foi a evolução do reward recebido pelo agente em

confrontos contra os oponentes do jogo. Observamos que, ao longo do treinamento, o



<a name="br3"></a> 

agente apresentou uma progressão signiﬁcativa, aumentando gradualmente seu reward.

Na conﬁguração ﬁnal da recompensa, o agente era recompensado de acordo com

sua própria vida, recebendo um bônus de acordo com sua vida restante, além de uma

penalidade baseada na vida do inimigo. Adicionalmente, também foi aplicada uma

penalidade constante ao agente para incentivá-lo a concluir a luta o mais rápido

possível.

**4.1. Optuna**

Na fase de otimização dos hiperparâmetros utilizando o Optuna, obtivemos diferentes

conﬁgurações para os hiperparâmetros. Realizamos um estudo e selecionamos a

conﬁguracao de hiperparametros que apresentou o melhor desempenho.

**Figura 1. Evolução do reward médio recebido pelo agente em diversas**

**conﬁgurações de hiperparametros pelo optuna.**

**4.2. Treinamento**

Realizamos o treinamento com diversos valores para os hiperparâmetros e analisamos a

taxa média de recompensa ao longo do treinamento. A recompensa representa o valor

recebido pelo agente com o passar do tempo. Inicialmente, a recompensa era baixa, mas

à medida que o agente aprendeu, essa recompensa aumentou progressivamente,

indicando uma melhoria no desempenho do agente. Aqui está a evolução do agente que

conquistou sua primeira vitória sobre o oponente. É importante observar que foram

necessárias quase 6 milhões de partidas para que o agente conseguisse derrotar seu

adversário.



<a name="br4"></a> 

**Figura 2. Evolução do reward médio recebido pelo agente ﬁnal**

Observamos que o agente foi capaz de aprender e utilizar estratégias de

combate, como a execução de combos e a defesa contra ataques do oponente. Além

disso, o agente demonstrou capacidade de adaptação, ajustando suas ações com base nas

habilidades e comportamento do oponente.

**5. Código**

O código implementado para o agente de IA em Mortal Kombat 2 está disponível no

seguinte repositório do GitHub: https://github.com/H3nriqu3L/MK-AI

Adicionalmente, também estão disponíveis algumas versões do agente durante a

fase de treinamento.

**6. Conclusão**

O desenvolvimento de um agente de IA capaz de jogar Mortal Kombat 2 utilizando

aprendizado por reforço foi um desaﬁo complexo, mas obtivemos sucesso em nosso

trabalho. Através do treinamento com o algoritmo PPO e da otimização de

hiperparâmetros com o Optuna, conseguimos aprimorar signiﬁcativamente o

desempenho do agente.

Ao longo do treinamento, observamos uma notável evolução do agente, que

inicialmente tomava ações aleatórias, mas foi se adaptando ao ambiente e aperfeiçoando

suas estratégias de jogo. A taxa de vitórias do agente aumentou progressivamente,

indicando sua capacidade de aprender e melhorar seu desempenho ao longo do tempo.

Este trabalho não só demonstra a aplicação bem-sucedida da inteligência

artiﬁcial em um jogo de luta renomado, como também destaca o potencial e as

possibilidades da IA em enfrentar desaﬁos complexos em ambientes dinâmicos. Através

do aprendizado por reforço, o agente foi capaz de aprender estratégias de combate,

adaptar-se às habilidades do oponente e tomar decisões estratégicas em tempo real.

No entanto, também enfrentamos algumas diﬁculdades durante

o

desenvolvimento do projeto. O treinamento do agente exigiu uma quantidade

signiﬁcativa de recursos computacionais e tempo de execução. Além disso, a otimização

de hiperparâmetros pode ser um processo demorado e exigir várias iterações para

encontrar as melhores conﬁgurações.



<a name="br5"></a> 

Como considerações pessoais, destacamos a importância de explorar diferentes

técnicas de aprendizado por reforço e otimização para obter melhores resultados. Além

disso, ressaltamos a necessidade de um pré-processamento adequado dos dados de

entrada para reduzir a dimensionalidade e focar nas informações relevantes para a

tomada de decisão.

No geral, este projeto nos proporcionou uma experiência valiosa no campo da

inteligência artiﬁcial aplicada a jogos, uma vez que conseguimos aplicar os

conhecimentos aprendidos em sala de aula de maneira prática. Aprendemos sobre os

desaﬁos e oportunidades envolvidos na criação de agentes autônomos capazes de

competir em ambientes complexos. Esperamos que este trabalho contribua para o

avanço do conhecimento e inspire futuras pesquisas na área de IA em jogos.

**Referências**

[1]: Documentação stablebaseline3 PPO:

<https://stable-baselines3.readthedocs.io/en/master/modules/ppo.html>

[2]: Documentação stablebaseline3 Policies:

https://stable-baselines.readthedocs.io/en/master/modules/policies.html

[3]: Documentação Optuna:

<https://optuna.readthedocs.io/en/stable/>

[4]: Documentação Gym-retro (biblioteca para emulaçao de jogos):

<https://retro.readthedocs.io/en/latest/getting_started.html>


