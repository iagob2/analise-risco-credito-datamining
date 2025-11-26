# 💳 Análise de Risco de Crédito - MinerAI

Este repositório contém o projeto final da disciplina de **Data Mining**, focado na criação de um modelo de concessão de cartões de crédito para a empresa fictícia **MinerAI**.

## 🎯 Objetivo
Desenvolver um algoritmo de Machine Learning capaz de classificar solicitantes de cartão de crédito em **Bons Pagadores (0)** e **Maus Pagadores (1)**, visando mitigar prejuízos financeiros decorrentes da inadimplência.

## 👥 Integrantes do Grupo
* **Ana Paula Velozo:** Introdução, contexto e objetivos.
* **Gabriel Dutra:** Coleta, carregamento e descrição dos dados.
* **Iago Correa de Lima:** Análise univariada e bivariada (variáveis categóricas).
* **Leonardo Renner:** Visualizações avançadas e análise de renda/patrimônio.
* **Persio de Souza Lima:** Detecção de outliers e modelagem (Machine Learning).

## 📊 Sobre os Dados
O dataset utilizado contém **50.000 registros** e **54 variáveis**, abrangendo:
* Dados cadastrais (Idade, Sexo, Estado Civil).
* Dados financeiros (Renda, Patrimônio).
* Dados profissionais e de moradia.
* **Target:** `ALVO MAU=1 ROTULO` (Binário).

> **Nota:** O dataset apresenta desbalanceamento de classes (~74% bons pagadores vs ~26% maus pagadores), o que exigiu técnicas específicas de tratamento.

## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python 3
* **Bibliotecas Principais:**
    * `pandas` & `numpy`: Manipulação de dados.
    * `matplotlib` & `seaborn` & `plotly`: Visualização de dados.
    * `scikit-learn`: Pré-processamento e modelos (Logistic Regression, Random Forest, KNN, Naive Bayes).
    * `xgboost`: Algoritmo de Gradient Boosting.

## 🚀 Metodologia e Modelagem
O projeto seguiu as seguintes etapas:
1.  **EDA (Análise Exploratória):** Identificação de padrões, correlações e outliers (rendas extremas).
2.  **Pré-processamento:**
    * Limpeza de dados (tratamento de nulos em profissão e residência).
    * Conversão de variáveis categóricas.
    * Divisão em Treino/Teste (80/20).
3.  **Machine Learning:**
    Foram treinados e comparados 5 modelos diferentes.
    * *Logistic Regression*
    * *K-Nearest Neighbors (KNN)*
    * *Random Forest*
    * *Naive Bayes*
    * *XGBoost*

## 📈 Resultados
O modelo **XGBoost** (ou o que vocês definiram como melhor no final) apresentou o melhor equilíbrio entre Precisão e Recall (F1-Score), sendo o escolhido para a solução final.

| Modelo | Acurácia | F1-Score |
| :--- | :---: | :---: |
| XGBoost | 61% | 0.42 |
| Random Forest | 74% | 0.06 |
| Logistic Regression | 56% | 0.41 |
*(Valores aproximados obtidos durante a execução)*

## 📂 Estrutura do Projeto
```bash
├── data/                # Arquivos de dados (credit.csv)
├── notebooks/           # Jupyter Notebooks com a análise completa
├── images/              # Gráficos e imagens gerados
├── requirements.txt     # Dependências do projeto
└── README.md            # Documentação do projeto
