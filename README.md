# 📊 Lucro Detalhado Power BI

Este projeto apresenta um dashboard interativo desenvolvido no Power BI para análise detalhada de **lucros empresariais**. A visualização permite explorar o desempenho financeiro por **produto**, **segmento**, **país** e **trimestre**, com filtros dinâmicos e gráficos intuitivos.

---

## 🎯 Objetivo

O objetivo principal é fornecer uma ferramenta visual e analítica que ajude empresas a:

- Identificar os produtos mais lucrativos
- Comparar segmentos de mercado
- Avaliar a performance por país e período
- Tomar decisões estratégicas com base em dados reais

---

## 🧰 Tecnologias Utilizadas

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Excel (.xlsx)** como fonte de dados
- Visualizações: Radar, Cascata, Barras Empilhadas, Cartão, Matriz Hierárquica

---

## 📁 Estrutura do Dashboard

### 🔹 Filtros Interativos
- **Ano** (2013, 2014)
- **País**
- **Segmento**
- **Produto**

### 🔹 Gráficos Utilizados

| Tipo de Gráfico       | Título no Dashboard                     | Métrica Principal |
|-----------------------|------------------------------------------|-------------------|
| Radar                 | Soma de Lucro por Produto                | `LucroTotal`      |
| Barras Empilhadas     | Soma de Lucro por Segmento               | `LucroTotal`      |
| Cascata               | Soma de Lucro por Trimestre              | `LucroTotal`      |
| Cartão                | Lucro Total                              | `LucroTotal`      |
| Matriz Hierárquica    | Lucro por Ano → País → Segmento → Produto| `LucroTotal`      |

---

## 📐 Medidas DAX Utilizadas

```DAX
LucroTotal = SUM('Financeiro'[Profit])

Trimestre = "Q" & FORMAT(QUARTER('Financeiro'[Date]), "0")# dashboard-lucro-detalhado
