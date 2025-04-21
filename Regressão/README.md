<h1 align="center"> Regressão - Séries Temporais </h1>

## 🧠 Sobre o Projeto

<div align="justify">

Este projeto tem como objetivo desenvolver um modelo de **regressão** utilizando técnicas de **séries temporais** para prever o número diário de visitantes de um site.  
A proposta é identificar padrões históricos no tráfego do site e estimar com precisão a quantidade de visitas futuras com base em dados anteriores.

</div>

##

## 📂 Base de Dados

- **Fonte:** Daily Website Visitors  
  - Disponível em: [Kaggle](https://www.kaggle.com/datasets/bobnau/daily-website-visitors)
- **Idioma:** Inglês
  - Todas as resenhas estão escritas em inglês.
- **Tamanho:**
  - 2.167 registros diários (de 14/09/2014 a 19/08/2020)
  - Aproximadamente 5 anos de dados diários
- **Descrição:**
  - `date`: Data da observação.
  - `visitors`: Número de visitantes no site.
  - `pageviews`: Número de visualizações de páginas.
  - `bounce_rate`: Taxa de rejeição (porcentagem de visitantes que saíram sem interagir com a página).
##

## 🎯 Objetivo

Prever o número de **visitantes diários** com base em variáveis históricas como visualizações de página e taxa de rejeição, utilizando algoritmos de regressão e análise de séries temporais.

> 🛠 Projeto em desenvolvimento.

##

## 🧹 Pré-processamento dos Dados

As etapas de tratamento incluíram:

- **Carregamento da Base de Dados**  
   A base foi importada diretamente de um arquivo `.csv` disponível no Kaggle, utilizando a biblioteca `pandas`.

- **Padronização do Nome da Coluna de Data**  
   A coluna original `'Date'` foi renomeada para `'date'` por questões de padronização.

- **Conversão de Datas**  
   A coluna `'date'` foi convertida de string para o tipo `datetime`, permitindo operações de ordenação, frequência e indexação temporal.

- **Definição do Índice Temporal**  
   A coluna `'date'` foi definida como índice do DataFrame, garantindo que o pandas reconheça a estrutura de série temporal.

- **Ordenação Cronológica**  
   Os dados foram ordenados pela data para evitar inconsistências durante a análise temporal.

- **Conversão de Dados Numéricos**  
   Algumas colunas como `'Unique.Visits'`, `'Page.Loads'`, `'Returning.Visits'` etc. estavam em formato de texto com vírgulas (ex: `"1,234"`).  
   Foi necessário remover as vírgulas e converter essas colunas para o tipo `int`.

- **Visualização Exploratória**  
   Após o tratamento, um gráfico foi gerado para visualizar a evolução dos visitantes únicos ao longo do tempo, permitindo observar tendências e padrões visuais.

</br>

##

## ⚙️ Algoritmos Utilizados



##

## 📊 Resultados



##

## 🔧 Ajustes de Parâmetros



##

## ✅ Conclusão
