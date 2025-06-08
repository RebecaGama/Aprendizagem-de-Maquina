<h1 align="center"> Agrupamento </h1>

## 🧠 Sobre o Projeto

<div align="justify">
  Este projeto tem como objetivo aplicar o algoritmo de agrupamento K-means para segmentar clientes com base em seus hábitos de consumo. A partir do Wholesale     
  Customers Dataset, buscamos identificar perfis distintos de compradores analisando seus gastos anuais em diferentes categorias de produtos.
</div>

##

## 📂 Base de Dados

- **Fonte:** Wholesale customers Data Set  
  - Disponível em: [Kaggle](https://www.kaggle.com/datasets/binovi/wholesale-customers-data-set)
- **Idioma:** Inglês
- **Tamanho:**
  - 440 registros
  - Arquivo `.csv` com cerca de **25 KB**
- **Descrição das colunas:**
  - `Channel`: Canal de compra (1 = Horeca, 2 = Varejo)
  - `Region`: Região do cliente (1 = Lisboa, 2 = Porto, 3 = Outras)
  - `Fresh`: Gasto anual com produtos frescos
  - `Milk`: Gasto anual com leite e laticínios
  - `Grocery`: Gasto anual com mercearia
  - `Frozen`: Gasto anual com alimentos congelados
  - `Detergents_Paper`: Gasto anual com detergentes e papel
  - `Delicassen`: Gasto anual com produtos de delicatessen

##

## 🎯 Objetivo

Aplicar o algoritmo K-means para identificar agrupamentos naturais entre os clientes, com base em suas características de consumo. O objetivo é descobrir padrões de comportamento que possam ser utilizados em estratégias comerciais e de marketing.

> ✅ Projeto finalizado.

##

## 🧹 Pré-processamento dos Dados

As etapas de tratamento incluíram:

- **Importação de bibliotecas**
Importação das bibliotecas necessárias: `pandas`, `matplotlib`, `seaborn`, `sklearn`.

- **Carregamento do dataset**
Leitura do arquivo CSV e visualização inicial para inspecionar dados e identificar possíveis problemas.

- **Remoção de colunas irrelevantes**
As colunas `Channel` e `Region` foram removidas, pois são categóricas e não foram utilizadas na clusterização.

- **Escalonamento dos dados**
Aplicado `StandardScaler` para padronizar as variáveis, garantindo que todas tenham média 0 e desvio padrão 1. Isso evita que variáveis com valores maiores dominem a análise.

##

## ⚙️ Algoritmos Utilizados

* **K-Means:**
  Aplicado para agrupar os clientes em 5 clusters. Cada cliente foi atribuído a um cluster com base na similaridade de padrões de consumo.

* **PCA (Análise de Componentes Principais):**
  Redução de dimensionalidade:

  * **PCA 2D:** para visualização em 2 dimensões.
  * **PCA 3D:** para visualização em 3 dimensões.

##

## 🔧 Ajustes de Parâmetros

- **Número de clusters:**
Testado com 5 clusters com base em experimentação inicial e testes de Elbow Method.

- **Escalonamento:**
PCA e K-means foram aplicados aos dados escalados para resultados mais robustos.

##

## 📊 Resultados

**Clusters formados**
O método Elbow Method identificou 5 grupos de clientes com padrões de consumo distintos.

### 📌 **Método do Cotovelo (Elbow Method) com KneeLocator:**

![KneeLocator](https://github.com/user-attachments/assets/c69d6908-6f78-4c8d-8839-8c206bbc03dd)

### 📌 **PCA 2D:**
  Gráfico de dispersão com cores distintas para cada cluster.
  Permitiu visualizar a separação entre grupos e a distribuição dos dados.

![Gráfico 2D](https://github.com/user-attachments/assets/ae18168c-e463-437f-aff3-51113e52e508)

### 📌 **PCA 3D:**
  Gráfico de dispersão 3D, possibilitando uma análise mais rica da distribuição dos clusters.
  Clientes agrupados de acordo com similaridade de consumo.
  Pontos isolados indicam perfis de clientes mais atípicos.
  
![Gráfico 3D](https://github.com/user-attachments/assets/328bd061-2266-4b11-8f59-66b1749e36e7)

##


## ✅ Conclusão

- O algoritmo K-means foi eficiente para segmentar os clientes com base em seus hábitos de consumo.
- A visualização com PCA permitiu interpretar visualmente os clusters formados e identificar padrões de comportamento, servindo de base para estratégias comerciais e ações de marketing.
