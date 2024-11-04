# Criando um modelo de identificação de fraudes

**Origem da base de dados:** https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

**<u>Informações obtidas através do Kaggle</u>**

**Contexto**: 
É importante que as empresas de cartão de crédito reconheçam transações fraudulentas para que os clientes não sejam cobrados por itens que não compraram.

**Conteúdo**: 
O conjunto de dados contém transações feitas por cartões de crédito em setembro de 2013 por titulares de cartões europeus. Esse conjunto apresenta transações de dois dias, com 492 fraudes em um total de 284.807 transações. ***O conjunto de dados é altamente desbalanceado***, com a classe positiva (fraudes) representando 0,172% de todas as transações.

Ele contém apenas variáveis numéricas, que são o resultado de uma transformação PCA (Análise de Componentes Principais). Infelizmente, devido a questões de confidencialidade, não podemos fornecer as variáveis originais nem mais informações contextuais sobre os dados. As variáveis V1, V2, … V28 são os componentes principais obtidos com o PCA; as únicas variáveis que não foram transformadas são 'Time' e 'Amount'. A variável 'Time' indica o tempo em segundos decorrido entre cada transação e a primeira do conjunto de dados. A variável 'Amount' é o valor da transação, podendo ser utilizada para aprendizado sensível a custo dependente do exemplo. A variável 'Class' é a variável de resposta, sendo 1 em caso de fraude e 0 caso contrário.

**Objetivos**: 
- Testar diferentes métodos de balanceamento de dados, a fim de definir um método para para treinar os modelos de previsão cuja classe de Fraude e Não-Fraude estará adequadamente balanceada (50%-50%)
- Usar diferentes modelo de Classificação (Decision Tree, Logistic Regression, Support Vector Machine, KNearest Neighbors, Random Forest)
- Definir quais métricas serão mais importante avaliarmos par esse problema (Recall, por exemplo), e analisar gráficamente outras métricas como Curva ROC e Curva Precisão-Recall
- Simualar os custos que podemos ter com os diferentes modelos apresentando diferentes resultados de Precisão e Recall como forma de ajudar a escolher qual é o melhor modelo para a aplicação.

**Ao final do modelo, teremos a seguite Matriz de Confusão, Curva ROC e Curva Precisão-Recall para os 5 modelos testados:**

![Confusion Matrix](Analises_Graficas/Confusion%20Matrix%20-%20Modelos%20Finais.png)
![Curva ROC e Curva Precisão-Recall](Analises_Graficas/Curva%20ROC%20e%20Precisão-Recall%20-%20Modelos%20Finais.png)
