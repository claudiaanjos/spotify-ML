<h2 align="left">
  👩🏻‍💻 Divisão dos dados e validação cruzada
</h2>

No desafio de hoje, você vai trabalhar na divisão dos seus dados em treino, validação e teste. Essa é uma etapa essencial antes de criar os seus modelos de machine learning.

Mas você deve estar se perguntando, por que eu vou precisar dividir, não é mesmo?! A resposta é simples: para avaliar o desempenho do seu modelo de forma justa. Se você usar todos os dados para treinar o modelo, não terá como saber se ele é bom o suficiente para generalizar para dados novos. Além disso, essa técnica é usada para garantir que o modelo não esteja superajustado (overfitting) aos dados de treinamento e que possa funcionar bem em novos dados.

Em resumo, os dados de treinamento são usados para treinar o modelo, enquanto que os dados de teste são usados para avaliar o desempenho do modelo em dados que ele nunca viu antes. E os dados de validação, são usados para ajustar os hiperparâmetros do modelo (parâmetros que melhoram o desempenho do modelo).

Mas como você pode dividir os dados? Bom, existem várias formas de fazer isso.

Uma delas é a divisão aleatória, que simplesmente separa os dados em três conjuntos de forma aleatória. Geralmente, 70-80% dos dados são usados para treino, 10-20% para teste e 10-20% para validação. Essa técnica é simples e rápida, mas pode não ser uma boa escolha quando há desequilíbrio de dados.

Outra forma é a validação cruzada, que é usada para avaliar a capacidade de generalização do modelo em diferentes conjuntos de dados. Ela ajuda muito a evitar o overfitting, que é quando um modelo se ajusta demais aos dados de treinamento, mas não generaliza bem para novos dados.

Uma forma comum de validação cruzada é a StratifiedKFold, que é especialmente útil para conjuntos de dados desbalanceados (e aqui já vai um spoiler do desafio do dia 6 👀).

Além disso, após a divisão dos dados, é necessário dividir o conjunto em X e Y. No seu caso, você terá o conjunto de variáveis explicativas (X), como gênero musical, duração da música, instrumentação, etc, e a variável de saída (Y), que indicará a popularidade da música, e que você quer prever.

Então, minha proposta pra hoje é que você realize a divisão dos dados utilizando a validação cruzada. E como desafio extra, utilize a StratifiedKFold e compare com outras técnicas de divisão de dados.

Lembre-se que a divisão de dados é uma etapa muito importante no processo de machine learning e pode afetar significativamente os resultados do seu modelo.

#

### Extras

- Com dúvidas sobre a validação cruzada? Veja esse [artigo de introdução](https://medium.com/tentando-ser-um-unic%C3%B3rnio/valida%C3%A7%C3%A3o-cruzada-uma-abordagem-intuitiva-697bb001a0ec) e esse [artigo de validação de modelos](https://www.alura.com.br/conteudo/machine-learning-validando-modelos);

- Você pode começar separando seu dataframe em df_train e df_test aplicando o método train_test_split() da [biblioteca Sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html);

- Em seguida, a partir do dataframe de treino (df_train), utilize a validação cruzada para separação dos dados em treino e validação. Tente utilizar a classe StratifiedKFold e aplicar um looping para separar os dados.

- Para entender mais sobre o efeito de Overfitting e Underfitting que eu mencionei anteriormente, recomendo a leitura desse [artigo](https://didatica.tech/underfitting-e-overfitting/).
