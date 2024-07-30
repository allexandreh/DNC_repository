# Regresão Não Linear

## Notebooks:

nliear_temps

Esse notebook é uma situação exemplo, explorando uma base de temperatura, nele está sendo predita a variável 'actual', por: RandomForestRegressor; AdaBoostRegressor; GradientBoostingRegressor.

nliear_preco_casa

Nesse notebook foi feita uma aplicação dos conceitos do notebook de exemplo, explorando uma base com caracteristicas de casas, nele a intenção foi prever o preço da casa por: RandomForestRegressor; AdaBoostRegressor; GradientBoostingRegressor.

## Conceitos:

Os modelos lineares pressupõem que é possível traçar uma reta entre os pontos dos dados, de forma que essa reta represente adequadamente a relação entre as variáveis.

No entanto, em muitos casos, os dados simplesmente não se comportam de forma linear. Onde mesmo traçando uma reta de regressão, ela não se ajusta bem à distribuição dos pontos.

Isso ocorre porque a relação entre as variáveis não é constante. À medida que a variável independente (eixo X) aumenta, o impacto que ela causa na variável dependente (eixo Y) também varia.

Portanto, esses casos requerem o uso de modelos não lineares, que são capazes de capturar essas variações e representar adequadamente os dados.

As árvores de decisão são uma ótima alternativa para lidar com esses problemas.

- O que são árvores de decisão

As árvores de decisão são modelos bastante utilizados tanto para problemas de classificação quanto de regressão. Elas funcionam traçando diversos caminhos de decisão com base em condições estabelecidas.

De acordo com o vídeo, as principais características das árvores de decisão são:

Conjunto de regras fáceis de entender e implementar: as decisões tomadas pela árvore são transparentes e de fácil interpretação.

Objetivo é criar um modelo com regras de decisão simples: a árvore sempre parte de uma condição (um "se") que deriva para outras condições ou para uma decisão final.

Estrutura representa possíveis caminhos de decisão: esses caminhos são definidos no processo de construção da árvore e culminam em uma previsão ou decisão final.

Alguns conceitos importantes relacionados às árvores de decisão:

Nós: representam pontos de decisão entre duas ou mais alternativas.

Folhas: nós terminais que contêm a decisão final ou previsão.

Valores contínuos: para problemas de regressão, as folhas devem conter valores contínuos.

- Vantagens das árvores de decisão

De acordo com o vídeo, as principais vantagens das árvores de decisão são:

Fácil interpretação: consegue-se entender facilmente as regras e condições utilizadas para chegar a uma decisão.

Menor necessidade de limpeza de dados: é pouco sensível a outliers e dados faltantes.

Lida bem com diferentes tipos de dados: numéricos, categóricos, ordinais etc.

Evita overfitting: com poda e controle de profundidade da árvore.

- Algumas desvantagens mencionadas:

Risco de overfitting, caso a árvore fique muito profunda.
Não tão adequada para problemas com variável alvo contínua.

Alguns pontos importantes na hora de treinar e avaliar o desempenho da árvore de decisão:

Dividir a base de dados em treino e teste para evitar overfitting.
Definir critérios de parada da construção da árvore (profundidade máxima, número mínimo de amostras por nó).
Podar a árvore para evitar overfitting e melhorar performance.
Avaliar desempenho no conjunto de teste com métricas como acurácia, precisão e recall.

Dessa forma, será possível treinar e otimizar uma árvore de decisão para realizar previsões confiáveis a partir das regras aprendidas com os dados.

- Métodos de Ensemble

Existem dois métodos principais para realizar o Ensemble: Bagging e Boosting.

- Bagging

O Bagging (Bootstrap Aggregating) funciona treinando cada modelo base de maneira independente usando um subconjunto aleatório dos dados de treinamento. Cada modelo é treinado em paralelo.

Por exemplo, podemos treinar um modelo de regressão linear usando 60% aleatórios dos dados. Em seguida, treinamos um modelo de floresta aleatória com outros 60% aleatórios e assim por diante. Ao fazer isso, cada modelo é treinado de maneira ligeiramente diferente.

No final, as previsões de cada modelo são agregadas (por exemplo calculando a média) para produzir a previsão final do Ensemble. Como cada modelo captura diferentes padrões nos dados, espera-se que os erros se compensem, reduzindo a variância.

O Bagging é um método de Ensemble paralelo, ou seja, os modelos base são treinados independentemente sem troca de informações.

-Boosting

O Boosting funciona de maneira sequencial, onde os modelos são treinados iterativamente, com cada modelo aprendendo com os erros do modelo anterior.

Por exemplo, podemos treinar um modelo base e identificar quais instâncias ele errou nas previsões. Em seguida, focamos um segundo modelo nessas instâncias difíceis para tentar acertá-las.

O Boosting dá mais peso e atenção às instâncias que os modelos anteriores erraram nas previsões. Isso permite que o Ensemble se concentre nas partes mais difíceis do problema, melhorando a acurácia.

Diferente do Bagging que é um método paralelo, o Boosting é sequencial, com cada modelo aprendendo e tentando melhorar em relação ao anterior.

- Modelos de Ensemble para Regressão

Veremos agora três modelos específicos de Ensemble que podem ser aplicados em problemas de regressão:

Random Forest Regressor

O Random Forest Regressor é um modelo de Ensemble muito popular que utiliza a técnica de Bagging com árvores de decisão.

Ele funciona construindo um grande número de árvores de decisão, onde cada árvore é treinada usando uma amostra aleatória dos dados. As previsões de todas as árvores são então agregadas calculando a média para produzir a previsão final.

Como cada árvore é treinada de maneira ligeiramente diferente, espera-se capturar mais aspectos e complexidades nos dados, reduzindo a variância e overfitting. O Random Forest Regressor costuma ter excelente desempenho para a maioria dos problemas de regressão.

Random Forest Regressor

AdaBoost

O AdaBoost (Adaptive Boosting) é um algoritmo de Boosting que também utiliza árvores de decisão como base. Ele funciona treinando as árvores sequencialmente, com cada árvore dando mais peso e focando nas instâncias que a árvore anterior errou.

O AdaBoost ajusta os pesos aplicados a cada instância a cada iteração. Instâncias que foram difíceis de prever corretamente recebem um peso maior, focando o treinamento nelas.

Assim o Ensemble vai se adaptando e enfocando onde precisa melhorar. O AdaBoost é um dos melhores algoritmos de Boosting, frequentemente superando outros métodos mais simples.

AdaBoost

Gradient Boosting

O Gradient Boosting também utiliza árvores de decisão de maneira sequencial, treinando cada árvore nos resíduos da anterior. Porém, diferente do AdaBoost que ajusta os pesos das instâncias, o Gradient Boosting tenta minimizar a perda residual a cada iteração.

A ideia é converter o problema de regressão em um problema de otimização, minimizando a função perda gradualmente em cada etapa.

O Gradient Boosting Regressor tem se mostrado extremamente eficaz para resolver problemas complexos de regressão, frequentemente superando outros métodos. Seu desempenho pode ser comparado e às vezes superar redes neurais profundas.

Gradient Boosting Regressor

Vantagens e Desvantagens do Ensemble

Algumas vantagens do Ensemble:


Melhora o desempenho da previsão em relação a modelos individuais
Reduz a variância e overfitting aos dados de treinamento
Mais robustez e estabilidade nas previsões
Pode lidar melhor com dados não lineares e complexos

Algumas desvantagens:

Requer mais recursos computacionais para treinar vários modelos
Pode haver overfitting se os modelos base forem muito similares
Difícil interpretar e depurar quando há erros

De maneira geral, o aumento na acurácia das previsões costuma superar as desvantagens para a maioria dos casos práticos.

É importante escolher uma diversidade de modelos base para o Ensemble, para que eles capturem diferentes aspectos do problema e se complementem.