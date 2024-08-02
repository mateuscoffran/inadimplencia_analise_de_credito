# Controle de Inadimplência em operações de Crédito

****

## 🔍 Sobre o Projeto

O objetivo deste projeto é analisar quais os fatores de risco dos clientes de uma Fintech, de forma a conseguir aprovar mais contratos com a menor inadimplência possível.

O projeto foi desenvolvido em Jupyter Notebook. Todo o trabalho foi elaborado a partir de uma base de dados em Excel com diversas informações de clientes da Fintech.

Esse estudo de caso foi proposto pela escola de Ciência de Dados "Preditiva Analytics". A base de dados também foi disponibilizada pela escola.

## 🗃️ Etapas do Projeto

Para o desenvolvimento do projeto foram importadas e utilizadas várias bibliotecas, como pandas, numpy, scikit-learn, matplotlib, seaborn e optuna.

Foi elaborada a fase de Preparação de Dados, em que foram analisados os Missing Values e valores duplicados.

Em seguida, foi realizada a Análise Exploratória de Dados (EDA). Foi realizada a análise univariada das variáveis numéricas e categóricas. Posteriormente, foi realizada a análise multivariada, sendo calculado o Índice de Correlação entre variáveis quantitativas e o nível de associação entre as variáveis e a variável binária (Inadimplência ou Não Inadimplência),  utilizando o IV (Information Value). Com base nesses cálculos, realizei uma série de análises do comportamento das variáveis e dos relacionamentos entre elas.

Com a EDA finalizada, desenvolvi 7 modelos para avaliar qual teria o melhor poder de classificação dos clientes inadimplentes.
Os 7 modelos desenvolvidos foram: Regressão Logística, Árvore de Decisão, Bagging de Regressão Logística, Random Forest, AdaBoost, Gradient Boosting e XG Boost.

Foram calculadas métricas de desempenho dos modelos. A principal medida utilizada para avaliação dos modelos foi o Recall, uma vez que a Fintech está com a grande preocupação de ter o mínimo de inadimplência possível, de reduzir o seu risco de crédito e dado o potencial de prejuízo que ela pode ter ao emprestar para clientes que se tornarão inadimplentes.

Uma vez analisados todos os modelos, realizei a Tunagem dos Hiperparâmetros de todos os modelos, considerando como referência para a otimização, a métrica Recall.

Após a Tunagem, o modelo que apresentou a melhor performance foi o Gradient Boosting, apresentando um Recall de 57% na base de teste e entregando uma boa capacidade de generalização.
