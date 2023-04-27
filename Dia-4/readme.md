<h2 align="left">
  👩🏻‍💻 Baseline do primeiro modelo
</h2>

No desafio de hoje, você irá criar o seu primeiro modelo de Machine Learning. Esse será o modelo inicial, uma linha de base ou baseline.

A baseline é o resultado de um modelo/solução muito básico. Você geralmente cria uma linha de base e, depois, tenta fazer soluções mais complexas para obter um resultado melhor. Se você conseguir uma pontuação melhor do que a linha de base, isso é bom.

Além disso, o modelo de baseline pode te ajudar a identificar se o problema é um problema de viés ou variância. Se o modelo de baseline tem uma precisão muito baixa, isso pode indicar que o problema é difícil e que você precisa de um modelo mais sofisticado para resolvê-lo.

A Regressão Logística é frequentemente usada como um modelo de baseline em problemas de classificação, por ser um modelo simples e fácil de interpretar. Ela estima probabilidades usando uma função logística (tome cuidado: apesar de ter regressão no nome, ela é usada para classificação).

Mas modelos de classificação não se restringem somente à Regressão Logística. Você pode explorar outros modelos de classificação como: Naive Bayes, Floresta Aleatória, Árvore de Decisão, XGBoost, e outros.

Portanto, comece criando seu modelo de baseline inicial. Defina um modelo para começar, instancie ele, treine nos dados de treino e faça a previsão nos dados de treino e dados de validação.

#

### Extras

- Utilize a Biblioteca de Machine Learning, [Scikit-Learn](https://scikit-learn.org/stable/), que é uma das mais conhecidas e utilizadas do Python. Ela suporta e possibilita o treino de diversas técnicas de estatística e Machine Learning.

- Para treinar o modelo, você pode utilizar o método .fit() do modelo a ser utilizado. E em seguida, você pode usar o .predict() para fazer a previsão. As previsões são feitas nos dados de validação/teste, que são diferentes dos dados de treinamento. Isso nos permite avaliar a capacidade do modelo de generalizar para novos dados que nunca foram vistos antes.

- Dependendo do modelo que você escolher, eles terão características distintas entre si. Se você escolheu o modelo de Regressão Logística (que prevê a probabilidade de um evento ocorrer), por exemplo, você vai encontrar um coeficiente .coef_, que te dará uma ideia de como cada variável (acústico, duração, danceabilidade, etc.) afeta a probabilidade.

- Se o coeficiente for positivo, isso significa que a variável aumenta a probabilidade do evento ocorrer; se for negativo, significa que diminui. Recomendo que você consulte a documentação [aqui](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html).

- A biblioteca [Yellowbrick](https://www.scikit-yb.org/en/latest/api/model_selection/importances.html) também permite visualizar os coeficientes e, então, entender a importância dos atributos (FeatureImportances) para o modelo.
