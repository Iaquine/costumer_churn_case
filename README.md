# Análise de Rotatividade de Clientes (Customer Churn)
Este projeto tem como objetivo estudar o problema de Customer Churn (rotatividade de clientes), um desafio crucial para empresas que buscam manter seus clientes e garantir a sustentabilidade do negócio. O churn ocorre quando um cliente decide encerrar seu relacionamento com uma empresa, migrando para a concorrência ou simplesmente deixando de utilizar seus serviços.

- Importação de bibliotecas: O projeto inicia importando as bibliotecas necessárias para a análise, incluindo pandas para manipulação de dados, numpy para cálculos numéricos, matplotlib e seaborn para visualização, além de bibliotecas específicas para aprendizado de máquina, como scikit-learn, imblearn e XGBoost.

- Carregamento dos dados: Os dados são carregados a partir de um arquivo CSV localizado no Google Drive. A função pd.read_csv é utilizada para ler o arquivo e armazená-lo em um DataFrame chamado df.

# Pré-processamento dos dados:

- Seleção de colunas: As colunas relevantes para a análise são selecionadas e armazenadas em uma lista chamada lista_colunas. O DataFrame df é então filtrado para incluir apenas essas colunas.
Verificação de tipos de dados e valores ausentes: A função df.info() é utilizada para verificar os tipos de dados de cada coluna e identificar se há valores ausentes.
- Estatísticas descritivas: A função df.describe() é utilizada para calcular estatísticas descritivas das colunas numéricas, como média, desvio padrão, valores mínimo e máximo, entre outros.
- Análise exploratória de dados (EDA): A função create_report da biblioteca dataprep é utilizada para gerar um relatório interativo com informações sobre as variáveis, como distribuição, valores ausentes, correlações, etc.
- Verificação de outliers: Boxplots são gerados para visualizar a distribuição de algumas variáveis numéricas e identificar possíveis outliers.
- Transformação de variáveis categóricas: As variáveis categóricas são convertidas em numéricas utilizando a técnica Label Encoding, que atribui um número inteiro a cada categoria.

# Modelagem e Avaliação:

- Divisão dos dados em treino e teste: Os dados são divididos em conjuntos de treino e teste utilizando a função train_test_split do scikit-learn.
- Escalonamento dos dados: Um objeto StandardScaler é criado para padronizar as variáveis numéricas, garantindo que todas tenham média zero e desvio padrão um.
- Definição dos modelos: Vários modelos de classificação são instanciados, incluindo Regressão Logística, Árvore de Decisão, Random Forest, KNN, Gradient Boosting e XGBoost.
- Definição das técnicas de balanceamento: Diferentes técnicas de balanceamento de classes são definidas, incluindo Random Undersampling, NearMiss, Tomek Links, Edited Nearest Neighbours, Condensed Nearest Neighbour, One-Sided Selection, Neighbourhood Cleaning Rule, Random Oversampling, SMOTE, ADASYN, Borderline-SMOTE, SVM SMOTE, SMOTE + Tomek Links, SMOTE + ENN e Undersampling + Oversampling.
- Criação de pipelines: Pipelines são criados para combinar o escalonamento dos dados, a técnica de balanceamento e o modelo de classificação em um único objeto.
- Treinamento e avaliação dos modelos: Os modelos são treinados nos dados de treino e avaliados nos dados de teste utilizando métricas como acurácia, precisão, recall, F1-score e AUC-ROC.
- Comparação dos resultados: Os resultados dos diferentes modelos e técnicas de balanceamento são comparados para identificar a melhor combinação.
- Visualização dos resultados: Gráficos são gerados para visualizar a matriz de confusão e a curva ROC dos modelos.
# Modelos Avaliados

- Regressão Logística
- Árvore de Decisão
- Random Forest
- K-Nearest Neighbors (KNN)
- Gradient Boosting
- XGBoost
# Técnicas de Balanceamento Avaliadas
1. Sem técnica de balanceamento
2. Undersampling:
- Random Undersampling
- NearMiss
- Tomek Links
- Edited Nearest Neighbours
- Condensed Nearest Neighbour
- One-Sided Selection
- Neighbourhood Cleaning Rule
3. Oversampling:
- Random Oversampling
- SMOTE
- ADASYN
4. Combinações:
- SMOTE + Tomek Links
- SMOTE + ENN
- Undersampling + Oversampling
# Conclusão

Este projeto demonstra uma abordagem completa para analisar o problema de churn de clientes, desde a exploração dos dados até a modelagem e avaliação de diferentes técnicas. A utilização de pipelines facilita a comparação de diferentes combinações de modelos e técnicas de balanceamento, permitindo identificar a melhor solução para o problema em questão.
