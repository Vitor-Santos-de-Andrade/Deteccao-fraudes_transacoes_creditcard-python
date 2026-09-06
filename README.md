# Detecção de fraudes em transações no cartão de crédito

![Jupyter Notebook](https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white)

Desafio de projeto do Bootcamp Bradesco da DIO, sobre treinar um modelo de Machine Learning em python para detectar anomalias em transações, em que utilizei o jupyter notebook para compor todo o projeto. Foi utilizado o dataset `creditcard.csv` para ser carregado no arquivo `deteccao.ipynb`. Além disso, utilizei o modelo Logistic Regression para verificar as métricas antes do balanceamento e o LGBMClassifier com smote para definir os resultados. 
## Objetivo
Desenvolver um programa para treinar um modelo de Machine Learning, a fim de detectar o máximo de fraudes em transações em cartões de crédito, porém mantendo o equilíbrio entre recall e precision.
## Bibliotecas
Bibliotecas importadas para o projeto:
- pandas
- logging
- numpy
- matplotlib.pyplot
- sklearn.preprocessing
    - StandardScaler
- sklearn.model_selection
    - train_test_split
- sklearn.linear_model
    - LogisticRegression
- sklearn.metrics
    - classification_report
    - roc_curve 
    - precision_recall_curve 
    - roc_auc_score
    - average_precision_score
    - confusion_matrix
- imblearn.over_sampling
    - SMOTE
- lightgbm
    - LGBMClassifier
- seaborn
- shap
## Estrutura do Notebook
1. **Carregar dataset**
2. **Classificação desbalanceada**
3. **Features engineering e temporais**
4. **Validação de dados**
5. **Divisão entre treino e teste**
6. **Regressão Logística**
7. **Balanceamento de dados (smote)**
8. **LGBMClassifier**
9. **Matriz de confusão e impactos financeiros**
10. **Importância das variáveis**
11. **Explicabilidade (SHAP)**
## Resultados Obtidos
**Principais métricas:**
- Precision: 0.78  
- Recall: 0.84  
- F1-score: 0.81  
- Roc_auc: 0.973  
- Average_precision: 0.841

**Valores da matriz de confusão:**
- Fraudes detectadas (TP): 124
- Transações legítimas marcadas como fraude (FP): 36
- Fraudes perdidas (FN): 24
- Transações legítimas corretas (TN): 85259

**Impactos financeiros:**
1. **Foram definidos custos hipotéticos de negócio:**
    - Benefício por cada fraude detectada: R$ 500,00
    - Perda por cada fraude não detectada: R$ 500,00
    - Custo por cada falso positivo: R$ 10,00

2. **Com isso, foi calculado o impacto financeiro total:**
    - Dinheiro recuperado por fraudes detectadas: R$ 62.000,00  
    - Prejuízo total por fraudes não detectadas: R$ 12.000,00  
    - Gasto total com falsos positivos: R$ 360,00  
    - Impacto final: R$ 49.640,00
