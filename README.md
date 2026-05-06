# Desafios de Programação

Este repositório contém as soluções para três desafios técnicos propostos.


---

## 📁 Estrutura do Projeto

```
.
├── SQL/
│   ├── loja.sqlite
│   └── queries.ipynb
│
├── data_modeling/
│   ├── breast_cancer.csv
│   ├── analise_modelo.Rmd
│   └── analysis.ipynb
│
├── reconcile_accounts/
│   ├── functions.ipynb
│   ├── transactions1.csv
│   └── transactions2.csv
│
└── README.md
```

---

## 🔁 1. Reconcile_Accounts

### Objetivo

Implementar uma função que compara duas listas de transações financeiras e identifica correspondências entre elas.

### Regras de Conciliação

* As transações são consideradas iguais se:

  * Departamento
  * Valor
  * Beneficiário
    são idênticos

* A **data pode variar em até ±1 dia**

* Cada transação só pode ser usada **uma única vez**

* Em caso de múltiplas correspondências possíveis:

  * Prioriza-se a transação com **data mais antiga**

### Saída

A função retorna duas listas com uma coluna adicional:

* `FOUND`: quando há correspondência
* `MISSING`: quando não há

Arquivo principal:

```
reconcile_accounts/functions.ipynb
```

---

## 📊 2. Modelagem de Dados (`data_modeling`)

### Dataset

Breast Cancer Wisconsin (Diagnostic)

### Variáveis analisadas

* mean concave points
* mean perimeter
* mean fractal dimension
* worst perimeter
* worst texture
* worst area
* target (0 = maligno, 1 = benigno)

### Etapas

#### 1. Análise Exploratória

* Boxplots por classe
* Correlação entre variáveis
* Pairplot
* VIF

**Objetivo:** entender separabilidade entre tumores benignos e malignos

#### 2. Regressão Linear (OLS)

* Modelo com `statsmodels`
* Avaliação de significância estatística


#### 3. Regressão Logística (GLM Binomial)

* Modelo mais adequado para classificação
* Identificação de variáveis relevantes

### Extra

* Uso do stepwise em R

Arquivos:

```
data_modeling/analysis.ipynb
data_modeling/analise_modelo.Rmd
```

---

## 🗄️ 3. Consultas SQL (`SQL`)

Banco de dados de uma loja virtual com três tabelas:

* Clientes
* Pedidos
* Pagamentos

### Queries implementadas

* Clientes e seus pedidos (incluindo sem pedidos)
* Total de pedidos e valor por cliente
* Pedidos sem pagamento

Arquivo:

```
SQL/queries.ipynb
```

---

## ⚙️ Pacotes Utilizados

* Pandas, NumPy
* Statsmodels
* Matplotlib / Seaborn
* SQLite3

---

## 📬 Contato

Caso tenha dúvidas sobre a implementação, fique à vontade para entrar em contato.
