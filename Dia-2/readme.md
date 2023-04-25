<h2 align="left">
  👩🏻‍💻 Pré processamento dos dados
</h2>

No primeiro dia você fez a coleta de dados e fez uma análise exploratória. Hoje, você irá começar o mergulho em Machine Learning.

Existem três tipos principais de machine learning (aprendizado de máquina): supervisionado, não supervisionado e por reforço. Neste desafio, você vai se concentrar no aprendizado supervisionado, que envolve a previsão de uma variável de saída com base em um conjunto de variáveis de entrada.

Indo mais a fundo, existem dois tipos de aprendizado supervisionado: classificação e regressão. Neste desafio, o foco será desenvolver um modelo de classificação para prever se uma música será popular ou não.

Mas para que você vai fazer isso? Entender se uma música será popular ou não pode ajudar a tomar melhores decisões de marketing e promover o sucesso de uma música, por exemplo.

Antes de começar a criar o seu modelos, você precisará passar pela etapa de pré-processamento de dados. O pré-processamento de dados é uma das etapas mais importantes no processo de Machine Learning. Essa é a fase em que você vai limpar, organizar e transformar os dados brutos em dados que possam ser usados para treinar os seus modelos.

Existem várias técnicas de pré-processamento de dados que você pode aplicar, como: remoção de dados duplicados, preenchimento de dados ausentes, normalização dos dados, engenharia de recursos e outros. Portanto, você pode começar aplicando algumas dessas técnicas aos dados disponíveis.

Outro ponto importante: você deve ter percebido na etapa anterior, de análise dos dados, que a coluna de popularidade apresenta números que variam de 0 a 100. E de acordo com a documentação da API do Spotify, 100 representa a mais popular. Esse número é baseado no número total de reproduções que a faixa teve e quão recentes são as reproduções.

Como você quer saber se uma música será popular ou não, você precisará estabelecer um corte de popularidade. Por exemplo, você pode definir que todas as músicas com popularidade acima de 70 são consideradas populares e aquelas abaixo de 70 são consideradas não populares. Esse corte não é padrão e pode ser ajustado para testar diferentes cenários.

Portanto, para prosseguir com o modelo de classificação, você precisa converter a coluna de popularidade em uma classe binária (1 para popular, 0 para não popular).

#

### Extras

- Para realizar o processo de corte de popularidade, você pode criar uma nova coluna de classe utilizando o método select() da bibllioteca Numpy. Essa função permite criar uma nova coluna a partir de condicionais. É útil quando você quer aplicar diferentes regras a diferentes valores de uma coluna existente e criar uma nova coluna com os resultados.
- Para entender mais sobre pré-processamento de dados e técnicas, deixo este [artigo do Medium](https://medium.com/data-hackers/pr%C3%A9-processamento-de-dados-com-python-53b95bcf5ff4).
- Se você quiser entender mais sobre modelos de classificação, leia esse [artigo](https://medium.com/leti-pires/predi%C3%A7%C3%A3o-da-necessidade-de-leitos-de-uti-no-hospital-s%C3%ADrio-liban%C3%AAs-811c88062f15) sobre um projeto envolvendo leitos de UTI e Covid-19.
- O livro “Machine Learning” é ótimo para aprofundar conceitos de Machine Learning, entender um fluxo de projeto e ainda colocar em prática. Ele é um guia que vai sempre contigo! 
