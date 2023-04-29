<h2 align="left">
  👩🏻‍💻 Validando o modelo
</h2>

Hoje vamos falar sobre a validação do modelo de classificação que você criou para prever a popularidade de músicas no Spotify.

Utilizar métricas adequadas de validação de modelos de Machine Learning é crucial em um projeto. O valor delas reflete a qualidade de um modelo, portanto, se forem mal escolhidas, pode ser impossível avaliar se o modelo atende aos requisitos necessários.

A avaliação de um modelo de classificação é feita a partir da comparação entre as classes preditas pelo modelo e as classes verdadeiras de cada exemplo. Todas as métricas tem o objetivo de medir quão distante o modelo está de uma classificação perfeita, porém, fazem isto de formas diferentes.
Uma forma simples de visualizar a performance de um modelo é através da matriz de confusão, como mostra figura abaixo:

Trazendo para a situação do desafio:

TP: verdadeiro positivo (a música é popular e modelo acertou)
TN: verdadeiro negativo (a música não é popular e o modelo acertou)
FN: falso negativo (o modelo diz que é popular, mas o valor real é não popular)
FP: falso positivo (o modelo diz que não é popular, mas o valor real é popular)

Além dessa métrica, você pode utilizar outras como a Acurácia, que vai mostrar, dentre todas as classificações, quantas o modelo classificou corretamente; a Precisão, que indica, dentre todas as classificações de classe Popular que o modelo fez, quantas estão corretas; o Recall, que mostra, dentre todas as situações de classe Popular como valor esperado, quais estão corretas; e o F1-score, que é a média harmônica entre precisão e recall.

A escolha da métrica dependerá do objetivo do projeto e das características do conjunto de dados. Se o objetivo for minimizar os falsos positivos, a precisão será a métrica mais importante. Se o objetivo for minimizar os falsos negativos, o recall será a métrica mais importante.

Desafio lançado! Que tal validar o modelo que você criou?! 

#

### Extras


- Para gerar o gráfico de matriz de confusão, você pode usar o confusion_matrix() disponível na biblioteca do Scikit-learn. Além disso, utilize também o Seaborn e Matplotlib para ajustar e melhorar seu gráfico.

- Na própria biblioteca do Scikit-learn você também vai encontrar funções prontas para extrair métricas, como: .accuracy_score(), .precision_score(), .recall_score(), .f1_score().
