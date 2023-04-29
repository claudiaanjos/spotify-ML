<h2 align="left">
  👩🏻‍💻 Reamostragem dos dados e ajuste do modelo selecionado
</h2>

Hoje o desafio será realizar a reamostragem dos dados.

A reamostragem é uma técnica utilizada em machine learning para lidar com desequilíbrios nos dados. Quando você tem um conjunto de dados em que uma das classes é muito menor do que a outra, isso pode afetar a precisão do modelo. Nesse caso, a reamostragem é uma técnica útil para equilibrar o número de instâncias em cada classe.

Lembra que, lá no dia 02, eu comentei sobre o ponto de corte de popularidade? Bom, é aqui que ele entra de novo. Se você definiu um ponto de corte de 50, talvez seus dados não estejam tão desbalanceados. Mas quando você sobe o ponto de corte para 80, por exemplo, você vai perceber que a proporção de músicas populares é muito menor que músicas não populares.

É importante se atentar a isso, pois a consequência desse desequilíbrio é que o modelo terá uma tendência a dar muitos "alarmes falsos". Ou seja, ele vai responder muito bem às entradas para as classes majoritárias (não popular), mas terá um desempenho inferior para as minoritárias (popular).

Oversampling e Undersampling são duas técnicas utilizadas para lidar com dados desbalanceados. Como você pode ver na imagem abaixo, o undersampling envolve a redução do número de observações da classe majoritária. Já o oversampling consiste em aumentar o número de observações na classe minoritária, criando novas amostras ou duplicando as amostras existentes.

Por este motivo, no desafio de hoje, você precisará realizar o balanceamento das classes de popularidade de músicas.

Utilize no mínimo duas técnicas, para que você possa comparar os resultados de performance (através das métricas) e decidir qual teve um melhor desempenho.

Reamostragem de dados feita? Ok! Então, agora é o momento que você precisa reajustar o seu modelo. Você precisará definir e testar diferentes hiperparâmetros para obter a melhor performance.

Os hiperparâmetros são parâmetros do modelo que não são aprendidos durante o treinamento, mas que precisam ser definidos pelo usuário. Exemplos de hiperparâmetros incluem o número de árvores em um modelo de floresta aleatória, por exemplo.

Encontrando os melhores hiperparâmetros do modelo, você poderá treinar novamente o seu modelo.

Lembre-se que o objetivo final do projeto é criar um modelo de machine learning capaz de prever com precisão a popularidade de músicas no Spotify. Então, não deixe de explorar diferentes técnicas e abordagens para obter o melhor resultado possível.

#

### Extras 

- Crie um dicionário com vários modelos para que você possa aplicar cada técnica sobre cada modelo e obter o melhor.

```
Dicionário dos classificadores
classifiers = {
      "LogisticRegression": LogisticRegression(),
      "KNearest": KNeighborsClassifier(),
      "DecisionTreeClassifier": DecisionTreeClassifier(),
      "Random Forest": RandomForestClassifier()
}
```

- Algumas técnicas que vocês podem utilizar para balanceamento de classes são: Distribuição Random UnderSampling, Distribuição Random OverSampling, Smote (Over-Sampling), Híbrido (OverSampling e UnderSampling).

- Você pode utilizar a RandomizedSearchCV para encontrar os melhores hiperparâmetros para um determinado modelo. É uma técnica interessante, pois permite especificar um conjunto de hiperparâmetros a serem testados e, então, realizar uma busca aleatória para encontrar as melhores configurações.

- Para aprofundar no tema "performance de modelos" recomendo a leitura deste post. Nele, você pode entender a diferença entre usar a RandomizedSearchCV e a GridSearchCV.

