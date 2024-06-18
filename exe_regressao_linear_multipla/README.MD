# Aprendendo Regresão Linear Múltipla

Nesta etapa do meu aprendizado usei da biblioteca statsmodels o modelo MRLS.
Para cada notebook e base está acompanhada e eles estão divididos em exemplo e aplicação do conceito.

# Ordem de desenvolvimento
## rml: Regresão Linear Múltipla
    Nesse desenvolvimento (rlm_limite_exemplo) com a base "limite_credito.xlsx", o intuíto foi mostrar que mais de uma variável explica o modelo, nele o target era o LimitedoChequeEspecial. O notebook foi desenvolvido, visando a seleção de variáveis, levando em consideração o r² e p_value. Nesse notebook foi dado o exemplo de como a técnica poderia ser utilizada e no notebook "rlm_lucro_aplicao" com a base "exercicio_lucro" foi o exercício aplicando a mesma técnica.

## rml: Regresão Linear Múltipla com variáveis categóricas
    Pra essa situação o desenvolvimento foi bem parecido, o que diferencia ele do desenvolvimento anterior é que foi preciso usar dummy para tratar as colunas com variáveis categóricas, nesse tratamento, por exemplo, se na coluna tem masculino e femino, e para um modelo de regressão isso dificulta a execução do modelo, então eles ficam binários, dessa forma a coluna vira duas, uma para cada vez que aparece masculino a palavra é substituída por 1 e caso contrário vira 0, na outra coluna ocorre o oposto. Após os transformações tanto o exemplo "dummy_escolaridade_exemplo.ipynb" com a base "escolaridade.xlsx", quanto a aplicação "limite_dummy_aplicacao.ipynb" com a base "limite_dummy.xlsx", seguem o mesmo princípio do exercício anterior, foca na seleção das variáveis que explicam o modelo, considerando p-value abaixo de 0,05.