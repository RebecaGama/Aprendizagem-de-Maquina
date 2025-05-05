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

* **Carregamento dos dados:**
  Dataset com visitas diárias a um site, contendo colunas como `Page.Loads`, `Unique.Visits` e `Date`.

* **Renomeação de colunas**:
  O Prophet exige colunas com nomes fixos:
  `Date → ds` (datas), `Unique.Visits → y` (valor a ser previsto)

* **Conversão de data**:
  A coluna `ds` foi convertida para o formato `datetime` e renomeada para `ds`, enquanto a variável alvo (`Page.Loads`) foi renomeada para `y`

* **Limpeza de valores:**
  Valores numéricos com vírgulas foram convertidos corretamente para inteiros.
  
* **Conversão de números**:
  Os valores numéricos foram tratados para remoção de vírgulas e convertidos para o tipo `int`

* **Divisão treino/teste**:
  Os últimos 30 dias foram reservados para teste, o restante para treino
  
##

## ⚙️ Modelo Utilizado

Foi utilizado o Prophet, um modelo desenvolvido pelo Facebook para lidar com séries temporais que apresentam tendência e sazonalidade. Foi escolhido pela sua facilidade de uso e capacidade de gerar boas previsões com dados temporais.

* Modelo treinado com dados históricos de visitas
* Previsão para os **30 dias seguintes**
* Frequência definida como **diária (`'D'`)**

##

## 📊 Resultados

### 🔹 Previsão Gerada

Foi gerada a previsão de visitas únicas para os próximos 30 dias e comparada com os valores reais do período de teste.

![1](https://github.com/user-attachments/assets/009346fd-5482-44b0-a40f-c5e7ed42ac11)

### 🔹 Componentes do Modelo

![2](https://github.com/user-attachments/assets/ff52c083-5d4d-45ba-9239-66fe05c0eec8)

*O modelo capturou:*

* **Tendência crescente** ao longo dos anos.
* **Picos semanais** entre segunda e quarta-feira.
* **Ciclos anuais**, com alta entre março e maio, e novembro.

### 🔹 Comparação Real vs. Previsto

![3](https://github.com/user-attachments/assets/ca241829-de1a-4caa-83d2-00643471dc95)

##

## 📏 Avaliação do Modelo

A comparação entre os valores reais e previstos nos últimos 30 dias foi avaliada com métricas de erro:

| Métrica                                  | Valor |
| ---------------------------------------- | ------- |
| **MAE** (erro absoluto médio)            | 269.996 |
| **MSE** (erro quadrático médio)          | 149.364 |
| **RMSE** (raiz do erro quadrático médio) | 386.477 |

> Valores mais baixos indicam melhor desempenho do modelo.
##

## ✅ Conclusão

* O modelo **capturou bem os padrões sazonais e a tendência geral** de visitas ao site.
* Pequenos desvios ocorrem em pontos de picos muito acentuados, o que é esperado.
* As métricas obtidas indicam **bom desempenho preditivo**, principalmente para uso operacional de curto prazo.

