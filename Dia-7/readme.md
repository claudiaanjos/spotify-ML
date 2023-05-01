<h2 align="left">
  👩🏻‍💻 Aplicando o resultado nos dados de teste e salvando os resultados
</h2>

Você avançou muito no seu projeto e, para fechar com chave de ouro, você irá aplicar o modelo de classificação escolhido aos dados de teste e salvar seus resultados.

Lembra que você separou uma parte dos dados para usar como teste? Pois bem, é hora de testar o seu modelo neles e ver como ele se comporta em dados que ele nunca viu antes.

E ah! Não se esqueça de serializar o seu modelo no final desse processo. Ou seja, gerar um arquivo com seu modelo salvo para que possa ser carregado depois em outros projetos ou compartilhado com outras pessoas.

Para salvar o seu modelo, existem duas bibliotecas muito famosas no Python que podem ajudar, Joblib e a Pickle. Para salvar seu modelo usando a Joblib, é só adicionar a linha de código joblib.dump(modelo, nome_arquivo.sav). Se for em Pickle, é só adicionar pickle.dump(modelo, nome_arquivo.pkl).

#

### Extras

Você pode me perguntar: qual seria o próximo passo depois de criar um modelo? Bom, de fato, a criação do modelo é apenas uma parte do processo. Com o modelo pronto, você vai precisar implementar em produção (deploy), para que possa ser usado em aplicações em um projeto real. É importante decidir como as pessoas usarão o modelo para realizar predições ou identificar padrões.

Esse [post](https://blog.somostera.com/data-science/deploy-o-que-e?utm_term=&utm_campaign=ad-cpa-tofu-insti_aniver-6a&utm_source=adwords&utm_medium=ppc&hsa_acc=9763069323&hsa_cam=17892248829&hsa_grp=&hsa_ad=&hsa_src=x&hsa_tgt=&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gad=1&gclid=CjwKCAjwxr2iBhBJEiwAdXECwwutY8s9TfI2vmcnICo30ZX1macXqW-W9oEQgNwFUBLPzTKZpcZFVRoCzdQQAvD_BwE) dá uma boa introdução sobre deploy de modelos. E esse [artigo](https://medium.com/data-hackers/como-eu-fiz-o-deploy-do-meu-primeiro-modelo-de-machine-learning-9b416d9abc51) mostra uma aplicação na prática.

Outro ponto importante após a criação de um modelo é o modelo de retreinamento. Pergunte-se: o modelo ainda é válido para novas cargas de trabalho? Lembre-se de que aprendizado de máquina é muito experimental, então é aqui que você deverá rastrear seus dados e experimentos, verificando o desempenho do modelo com base em métricas, quantas vezes for necessário.

Além disso, você verá que as suas previsões podem começar a envelhecer ou que os dados podem ficar desatualizados, ou, até mesmo, novos padrões podem surgir, tornando o modelo original incapaz de capturar essas mudanças.

Isto e muitas outras diretrizes são mencionadas no artigo "Rules of Machine Learning", escrito por Martin Zinkevich, engenheiro de software no Google. [Recomendo demais essa leitura](https://developers.google.com/machine-learning/guides/rules-of-ml?hl=pt-br&utm_source=ActiveCampaign&utm_medium=email&utm_content=%237DaysOfCode%20-%20Machine%20Learning%207%2F7%3A%20Aplicando%20o%20modelo%20nos%20dados%20de%20teste%20e%20salvando%20os%20resultados&utm_campaign=%5BAlura%20%237Days%20Of%20Code%5D(Js%20e%20DOM%20-%203%C2%AA%20Ed%20)%207%2F7#ml_phase_ii_feature_engineering)!

Uma das coisas mais interessantes que ele menciona é: "[...] é importante se concentrar em algo que não é ensinado em nenhuma classe de machine learning: como analisar e melhorar um modelo atual. Isso é mais uma arte do que uma ciência, mas existem vários antipadrões que podem ajudar a evitar isso." E no decorrer desse tópico, ele mostra algumas boas práticas, como por exemplo, medir o delta entre os modelos, ou seja, calcular a diferença entre os novos resultados e a produção. Fica a dica!😉
