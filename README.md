# 🍷 Tech Challenge - Data Analytics [FASE 02]
> **Classificação e Preditividade da Qualidade de Vinhos com Machine Learning**

---

## 📌 Sobre o Projeto

Este projeto faz parte da **Fase 02 do Tech Challenge** do curso de Data Analytics. O objetivo principal é construir modelos de **Machine Learning** capazes de prever e classificar a qualidade de variantes tintas do vinho português *"Vinho Verde"*.

A base de dados utilizada é originária do **Kaggle** (`WineQT.csv`) e apresenta desafios clássicos de projetos reais de Ciência de Dados:
- **Volume reduzido de dados** (poucas amostras após tratamento);
- **Classes altamente desbalanceadas** (concentração de notas intermediárias 5 e 6);
- **Variáveis em escalas distintas** (exigindo padronização/normalização).

---

## 📊 Estrutura e Atributos do Dataset

O dataset possui **1143 linhas** (antes do tratamento) e **13 colunas**, sendo composto pelas seguintes características físico-químicas:

| Atributo | Descrição |
| :--- | :--- |
| `fixed acidity` | Acidez fixa |
| `volatile acidity` | Acidez volátil |
| `citric acid` | Ácido cítrico |
| `residual sugar` | Açúcar residual |
| `chlorides` | Cloretos |
| `free sulfur dioxide` | Dióxido de enxofre livre |
| `total sulfur dioxide` | Dióxido de enxofre total |
| `density` | Densidade |
| `pH` | pH do vinho |
| `sulphates` | Sulfatos |
| `alcohol` | Teor alcoólico |
| `quality` | **Target:** Nota de qualidade do vinho (3 a 8) |
| `Id` | Identificador único |

---

## 🔍 Etapas da Análise Exploratória (EDA)

Durante a exploração inicial dos dados no notebook, foram identificados e tratados os seguintes pontos:

1. **Tipos de Dados e Nulos:**
   - Todas as variáveis explicativas são numéricas (`float64`).
   - Não foram encontrados valores nulos/ausentes.

2. **Registros Duplicados:**
   - Foram identificados **125 registros duplicados** (desconsiderando a coluna `Id`).
   - A base foi tratada, reduzindo o total de **1143 para 1018 linhas únicas**.

3. **Análise da Variável Target (`quality`):**
   - Apesar da escala teórica ser de 0 a 10, o dataset contém apenas as notas **3, 4, 5, 6, 7 e 8**.
   - As notas **5 e 6** concentram a grande maioria das amostras, evidenciando o alto desbalanceamento da classe de resposta.

4. **Escala e Outliers:**
   - Identificou-se grande variação entre as escalas das variáveis (ex: `chlorides` varia entre 0.01 e 0.61, enquanto `total sulfur dioxide` atinge até 289.00).
   - Constatou-se a necessidade de avaliar a presença de *outliers* para definir a melhor técnica de tratamento (Padronização com `StandardScaler` ou Normalização com `MinMaxScaler`).

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- **Linguagem:** Python 3.x
- **Análise e Manipulação de Dados:** `pandas`, `numpy`
- **Visualização de Dados:** `matplotlib`, `seaborn`
- **Machine Learning & Preprocessamento:** `scikit-learn` *(e/ou outras bibliotecas do seu notebook)*

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
Certifique-se de ter o **Python 3.8+** e o **Jupyter Notebook** (ou VS Code / Google Colab) instalados.

### 1. Clonar o repositório
git clone https://github.com/pamvilar/fiap-tech-challenge-fase2-14dtat.git
cd fiap-tech-challenge-fase2-14dtat

---

## 🎥 Assista ao vídeo de apresentação deste Projeto: 

[![Vídeo de Apresentação](https://img.youtube.com/vi/68PQ212Fk_I/maxresdefault.jpg)](https://www.youtube.com/watch?v=68PQ212Fk_I)

---

## 📂 Estrutura do Repositório

```text
TECH_CHALLENGE_FASE_02
│
├── DataSet/
│   └── WineQT.csv
│
├── Notebook/
│   └── TechChallengeVinhos_Fase02.ipynb
│
├── Relatório/
│   └── relatorio-vinhos-ml-fase2.pdf
│   └── Classificação da Qualidade dos Vinhos com Machine Learning.pptx
│
├── .gitignore
└── README.md
```
