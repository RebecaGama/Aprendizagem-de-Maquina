<h1 align="center"> Agrupamento </h1>

## 🧠 Sobre o Projeto

<div align="justify">
  Este projeto tem como objetivo aplicar o algoritmo de agrupamento K-means para segmentar clientes com base em seus hábitos de consumo. A partir do Wholesale     
  Customers Dataset, buscamos identificar perfis distintos de compradores analisando seus gastos anuais em diferentes categorias de produtos.
</div>

##

## 📂 Base de Dados

- **Fonte:** Wholesale customers Data Set  
  - Disponível em: [Kaggle](https://www.kaggle.com/datasets/uciml/wholesale-customers)
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

> 🛠 Projeto em desenvolvimento.

##


## 🧹 Pré-processamento dos Dados

- Remoção das colunas `Channel` e `Region`, pois não representam diretamente o padrão de consumo.
- Aplicação de **normalização com `StandardScaler`**, garantindo que todas as variáveis tenham a mesma escala.
- Utilização de **PCA (Análise de Componentes Principais)** para reduzir a dimensionalidade dos dados e permitir uma visualização mais clara dos agrupamentos em 2D e 3D.

##

## ⚙️ Algoritmos Utilizados

- **K-Means Clustering** (do `scikit-learn`) para segmentação de clientes.
- **PCA (Principal Component Analysis)** para visualização dos clusters em 2 e 3 dimensões.
- Visualizações com `matplotlib`.

##

## 📊 Resultados

- Foram identificados 3 grupos principais de consumidores, baseados nos padrões de consumo de produtos alimentícios e de limpeza.
- Cada grupo apresenta características distintas que podem indicar perfis de clientes, como:
  - Clientes que gastam mais em produtos frescos.
  - Clientes com foco em mercearia e detergentes.
  - Clientes com consumo equilibrado entre categorias.
- As visualizações geradas com PCA ajudaram a compreender melhor a separação entre esses grupos.

##

## 🔧 Ajustes de Parâmetros

- O número de clusters foi definido como 3 com base na experimentação visual, mas pode ser ajustado usando o **método do cotovelo**.
- O PCA foi testado com 2 e 3 componentes principais para facilitar a visualização dos agrupamentos.

##

## ✅ Conclusão

O uso de K-means neste projeto permitiu identificar diferentes perfis de clientes a partir dos dados de consumo anual. Essa segmentação é essencial para estratégias de marketing personalizadas, como promoções direcionadas ou otimização de estoques para diferentes tipos de consumidores. Futuramente, o projeto pode ser aprimorado com métodos de validação de cluster, como Silhouette Score, e testes com outros algoritmos de agrupamento.
