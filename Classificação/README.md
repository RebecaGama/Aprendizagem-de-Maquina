<h1 align="center"> Classificação </h1>

## 🧠 Sobre o Projeto

<div align="justify">

Este projeto tem como objetivo desenvolver um modelo de **classificação de sentimentos** a partir de **resenhas de filmes**.  
A ideia central é construir um classificador capaz de prever se uma resenha é **positiva** ou **negativa** com base apenas no seu conteúdo textual.

</div>

##

## 📂 Base de Dados

- **Fonte:** IMDb Movie Reviews Dataset  
  - Disponível em: [Kaggle](https://www.kaggle.com/)
- **Idioma:** Inglês
  - Todas as resenhas estão escritas em inglês.
- **Tamanho:**
  - 50.000 registros (resenhas de filmes)
  - Divididos igualmente entre 25.000 resenhas positivas e 25.000 resenhas negativas
  - Arquivo .csv com cerca de 80 MB
- **Descrição:**
  - `review`: Texto da resenha do filme.
  - `sentiment`: Rótulo da resenha:
    - `positive` (1): Resenha positiva.
    - `negative` (0): Resenha negativa.

##

## 🎯 Objetivo

Classificar automaticamente resenhas de filmes como **positivas** ou **negativas** por meio de técnicas de Processamento de Linguagem Natural (PLN) e Aprendizagem de Máquina.

> ✅ Projeto finalizado.

##

## 🧹 Pré-processamento dos Dados

As etapas de tratamento incluíram:

- **Limpeza do texto:**  
  Remoção de pontuações, números e conversão para letras minúsculas.
  
- **Stopwords:**  
  Exclusão de palavras comuns irrelevantes (usando `nltk.stopwords`).
  
- **Tokenização:**  
  Separação do texto em palavras individuais.
  
- **Stemming:**  
  Redução das palavras à sua raiz (com `PorterStemmer`).

- **Conversão de rótulos:**  
  `positive` → 1  
  `negative` → 0

##

## ⚙️ Algoritmos Utilizados

Foram testados cinco algoritmos de classificação:

1. **Naive Bayes**
2. **Árvore de Decisão**
3. **Random Forest**
4. **Support Vector Machine (SVM)**
5. **Rede Neural**

##

## 📊 Resultados

### 🟡 **Naive Bayes**
- Melhor **recall** para classe 0 (negativa).
- Boa **precisão** para classe 1 (positiva).
- **Acurácia:** 85%

![Naive Bayes](https://github.com/user-attachments/assets/dcf06660-cf52-4138-a019-870874a99d16)

###  **Árvore de Decisão**
- Maior sensibilidade para a classe 0 (negativa), e menor desempenho para classe 1 (positiva).
- **F1-Score médio:** 0.69
- **Acurácia:** 69%

![Árvore de Decisão](https://github.com/user-attachments/assets/1fb2dbaa-1f7c-4d96-b1b8-fab281c15fb2)

###  **Random Forest**
- Modelo robusto, com boa capacidade de generalização.
- Resultados equilibrados entre precisão e recall nas duas classes.
- **Acurácia:** 85%

![Random Forest](https://github.com/user-attachments/assets/82cda757-3d26-40d3-a6c4-fd918822736f)

### 🔵 **SVM**
- Melhor equilíbrio entre precisão e recall para ambas as classes.
- **F1-score:** 0.86 (positiva) e 0.85 (negativa).
- **Acurácia:** 84%

 ![Support Vector Machine](https://github.com/user-attachments/assets/cc15073b-8571-46b7-bb07-ecbcc22291c4)

###  **Rede Neural**
- Modelo complexo
- Obteve métricas próximas ao SVM, mostrando bom poder preditivo.
- **Acurácia:** 81%

![Rede Neural](https://github.com/user-attachments/assets/5ea5261a-b527-44d2-a442-c99e70676650)

##

## 🔧 Ajustes de Parâmetros

### 📌 Support Vector Machine
- **Melhor configuração:**  
  - `C=1`, `kernel='linear'`, `class_weight='balanced'`
- **Resultado:**  
  - Acurácia: 85%  
  - F1-score balanceado (0.85 e 0.84)  
  - Boa performance nas duas classes.

![SVM Ajustado](https://github.com/user-attachments/assets/6f9c251c-647c-479a-93e6-0f73d266a1fe)

### 📌 Árvore de Decisão
- **Desempenho inicial:** Acurácia de 73%
- **Ajustes realizados:**
  - **GridSearchCV** para otimizar:
    - `max_depth`
    - `min_samples_split`
    - `min_samples_leaf`
    - `criterion`
  - Uso de `class_weight='balanced'` para lidar com classes desbalanceadas.
- **Resultados após ajuste:**
  - Recall da classe 1 subiu de 0.69 → 0.79
  - Recall da classe 0 caiu de 0.77 → 0.60
  - Acurácia geral caiu levemente para 69%, mas houve maior sensibilidade para resenhas positivas.

![Árvore de Decisão Ajustada](https://github.com/user-attachments/assets/b25d1939-5e12-4f29-97cc-1020576c6693)

##

## ✅ Conclusão

- **Naive Bayes** se destacou em avaliações negativas, mas com viés perceptível.
- **SVM** teve o melhor desempenho global, sendo mais equilibrado e indicado para uso em produção.
- **Árvore de Decisão**, apesar de menos precisa, ofereceu boa interpretabilidade e sensibilidade para a classe positiva.
- 🎯 **Objetivo atingido**: Desenvolver modelos eficientes de classificação de sentimentos com base em texto.
