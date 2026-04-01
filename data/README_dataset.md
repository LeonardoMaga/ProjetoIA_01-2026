# Dataset — Consumo de Energia Elétrica (Edifício A)

## Origem

- **Estudo:** Mariano-Hernández et al. (2021)  
- **Título:** A Data-Driven Forecasting Strategy to Predict Continuous Hourly Energy Demand in Smart Buildings  
- **Repositório:** Mendeley Data  
- **DOI:** [10.17632/mzkyh37mtr.2](https://doi.org/10.17632/mzkyh37mtr.2)  
- **Acesso:** Público, sem restrições de uso para fins acadêmicos  

## Descrição

Leituras **horárias** de consumo de energia elétrica (kWh) e variáveis climáticas de um edifício universitário do campus de Valladolid, Espanha, cobrindo o período de **janeiro de 2016 a dezembro de 2020**.

- **Arquivo utilizado:** `db_building_A.csv`  
- **Total de registros:** 43.848 linhas horárias  
- **Período:** 2016-01-01 00:00 → 2020-12-31 23:00  

## Dicionário de Variáveis

| Coluna | Descrição | Unidade |
|---|---|---|
| DATE | Timestamp horário | — |
| **ENERGY** | Consumo de energia elétrica **(variável alvo)** | kWh |
| HDD18_3 | Graus-dia de aquecimento (base 18,3°C) | °C·dia |
| CDD0 | Graus-dia de resfriamento (base 0°C) | °C·dia |
| CDD10 | Graus-dia de resfriamento (base 10°C) | °C·dia |
| PRECTOT | Precipitação total diária | mm/dia |
| RH2M | Umidade relativa a 2m | % |
| T2M | Temperatura média a 2m | °C |
| T2M_MIN | Temperatura mínima a 2m | °C |
| T2M_MAX | Temperatura máxima a 2m | °C |
| ALLSKY | Irradiância solar de céu aberto | MJ/m²/dia |
| HOLIDAY | Indicador de feriado ou recesso acadêmico | 0 ou 1 |

> As variáveis climáticas são valores diários repetidos para cada hora do dia. As variáveis de temperatura e irradiância são provenientes da base **NASA POWER** (https://power.larc.nasa.gov/).

## Problemas Identificados e Tratamentos Aplicados

| Problema | Qtd. | Tratamento |
|---|---|---|
| Valores ausentes em ENERGY | 102 | Interpolação temporal |
| Valores ausentes em ALLSKY | 144 | Interpolação temporal |
| Timestamps duplicados (horário de verão) | 4 | Média dos registros duplicados |
| Gaps de 2h (transição horário de verão) | 4 | Reindexação + interpolação |
| Erros de medição (ENERGY < 50 kWh) | 5 | Substituição por NaN + interpolação |

Após o tratamento: **43.848 registros sem valores ausentes**.

## Estatísticas Descritivas (Após Limpeza)

| Métrica | ENERGY (kWh) | T2M (°C) | RH2M (%) |
|---|---|---|---|
| Mínimo | 51,33 | — | — |
| Máximo | 469,76 | — | — |
| Média | 165,45 | — | — |
| Desvio Padrão | ~72 | — | — |

## Divisão Treino/Teste

| Conjunto | Período | Registros |
|---|---|---|
| Treino | 2016–2019 | 35.064 |
| Teste | 2020 | 8.784 |
