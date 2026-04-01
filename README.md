# Predição de Consumo de Energia Elétrica em Smart Campus com LSTM

**Universidade Presbiteriana Mackenzie — Faculdade de Computação e Informática**  
**Disciplina:** Inteligência Artificial — 7ºN CC Noite  
**Professor:** Dr. Ivan Carlos Alcântara de Oliveira  

---

## 👥 Integrantes

| Nome | RA |
|---|---|
| Mateus Alonso Varjao | 10417888 |
| Lucas Monteiro Soares | 10417881 |
| Leonardo Magalhães | 10417121 |
| Matheus Chediac Rodrigues | 10417490 |

---

## 📋 Sobre o Projeto

Este projeto aplica redes neurais **LSTM (Long Short-Term Memory)** para a **predição de curto prazo do consumo horário de energia elétrica** em um edifício de campus universitário, com horizonte de 24 horas (estratégia *day-ahead*).

O erro de predição é explorado como mecanismo de **detecção de anomalias de consumo**, sinalizando desvios significativos do comportamento esperado.

O projeto está relacionado ao **Trabalho de Conclusão de Curso (TCC)** dos integrantes e é desenvolvido também no contexto da disciplina de Inteligência Artificial.

---

## 🗂️ Estrutura do Repositório

```
📦 repositorio
 ┣ 📂 data/
 ┃ ┗ 📄 README_dataset.md       # Descrição detalhada do dataset
 ┣ 📂 notebooks/
 ┃ ┗ 📓 eda_baseline.ipynb      # Pré-processamento, EDA e modelo baseline
 ┣ 📂 relatorio/
 ┃ ┗ 📄 artigo_n1.docx          # Artigo parcial — entrega N1
 ┗ 📄 README.md
```

---

## 📊 Dataset

- **Fonte:** Mariano-Hernández et al. (2021) — Mendeley Data  
- **DOI:** [10.17632/mzkyh37mtr.2](https://doi.org/10.17632/mzkyh37mtr.2)  
- **Conteúdo:** Leituras horárias de consumo de energia elétrica (kWh) e variáveis climáticas de um edifício universitário em Valladolid, Espanha  
- **Período:** Janeiro de 2016 a Dezembro de 2020  
- **Total:** 43.848 registros horários  

---

## 🔬 Notebooks

| Notebook | Descrição |
|---|---|
| `eda_baseline.ipynb` | Pré-processamento, análise exploratória (EDA) e modelo baseline Naive Sazonal |

---

## 📈 Resultados Parciais (N1)

| Modelo | RMSE (kWh) | MAE (kWh) | MAPE (%) | R² |
|---|---|---|---|---|
| Naive Sazonal 24h (baseline) | 54,38 | 25,28 | 15,62 | 0,4981 |
| LSTM (a implementar) | — | — | — | — |

---

## 🛠️ Tecnologias Utilizadas

- Python 3.10+
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- TensorFlow / Keras *(N2)*

---

## 📅 Entregas

| Etapa | Prazo | Status |
|---|---|---|
| Parte 1 — Proposta | 01/03/2026 | ✅ Entregue |
| Parte 2 — N1 (EDA + Artigo Parcial) | 01/04/2026 | ✅ Entregue |
| Parte 3 — N2 (Modelo completo + Vídeo) | 28/05/2026 | 🔄 Em andamento |

---

## 📚 Referência Principal

Mariano-Hernández, D. et al. (2021). *A Data-Driven Forecasting Strategy to Predict Continuous Hourly Energy Demand in Smart Buildings*. Applied Sciences, v. 11, n. 17, p. 7886. https://doi.org/10.3390/app11177886
