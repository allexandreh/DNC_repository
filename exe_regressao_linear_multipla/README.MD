# Regresão Linear Múltipla

Introdução

A regressão linear múltipla é uma técnica estatística que permite explorar a relação entre uma variável resposta (variável dependente Y) e duas ou mais variáveis explanatórias (variáveis independentes X1, X2 etc). O objetivo é desenvolver um modelo que possa prever os valores da variável resposta com base nos valores das variáveis independentes.

Uma parte importante da análise de regressão linear é a significância estatística dos resultados. Isso indica o quão confiáveis são as relações encontradas no modelo entre as variáveis independentes e dependentes.

Uma medida muito utilizada para avaliar a significância estatística é o p-value. Mas o que é o p-value? O que ele representa? Como interpretá-lo?


O que é o p-value?

O p-value, ou valor-p, é uma medida estatística que indica a compatibilidade entre os dados observados em uma amostra e uma hipótese específica sobre a população.

Em termos mais simples, o p-value avalia o quão bem os dados da amostra apoiam a afirmação de que uma hipótese é verdadeira. Quanto menor o p-value, menos suporte há nos dados para a hipótese.

Na regressão linear, o p-value é calculado para testar a significância dos coeficientes do modelo de regressão ajustado. Ou seja, ele testa se existe de fato uma relação linear entre cada variável independente e a variável dependente.

O que foi usado nos notebooks?

Foi usada da biblioteca statsmodels o modelo MRLS.
Para cada notebook e base está acompanhada e eles estão divididos em exemplo e aplicação do conceito.

# Ordem de desenvolvimento

Regresão Linear Múltipla (rlm):

    Nesse desenvolvimento (rlm_limite_exemplo) com a base "limite_credito.xlsx", o intuíto foi mostrar que mais de uma variável explica o modelo, nele o target era o LimitedoChequeEspecial. O notebook foi desenvolvido, visando a seleção de variáveis, levando em consideração o r² e p_value. Nesse notebook foi dado o exemplo de como a técnica poderia ser utilizada e no notebook "rlm_lucro_aplicao" com a base "exercicio_lucro" foi o exercício aplicando a mesma técnica.

Regresão Linear Múltipla com variáveis categóricas:

    Pra essa situação o desenvolvimento foi bem parecido, o que diferencia ele do desenvolvimento anterior é que foi preciso usar dummy para tratar as colunas com variáveis categóricas, nesse tratamento, por exemplo, se na coluna tem masculino e femino, e para um modelo de regressão isso dificulta a execução do modelo, então eles ficam binários, dessa forma a coluna vira duas, uma para cada vez que aparece masculino a palavra é substituída por 1 e caso contrário vira 0, na outra coluna ocorre o oposto. Após os transformações tanto o exemplo "dummy_escolaridade_exemplo.ipynb" com a base "escolaridade.xlsx", quanto a aplicação "limite_dummy_aplicacao.ipynb" com a base "limite_dummy.xlsx", seguem o mesmo princípio do exercício anterior, foca na seleção das variáveis que explicam o modelo, considerando p-value abaixo de 0,05.