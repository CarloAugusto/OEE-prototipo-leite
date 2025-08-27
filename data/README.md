#  Pasta `data/`

Este diretório contém os **dados simulados** utilizados no projeto OEE — protótipo para o setor lácteo.

---

##  Arquivo Principal

### `dados_leite.csv`

- **Origem:** Gerado pelo script [`simulacao_oee.R`](../docs/simulacao_oee.R).
- **Objetivo:** Alimentar análises, visualizações e dashboards com dados simulados que refletem práticas de eficiência (OEE) na produção de leite.
- **Escala:** Dados representam várias fazendas/sistemas ao longo de um período definido (ex.: anos ou ciclos de produção).

---

##  Estrutura dos Dados

Cada registro no CSV corresponde a uma **fazenda/ciclo de produção**. As colunas típicas incluem:

| Coluna                   | Descrição                                                |
|--------------------------|-----------------------------------------------------------|
| `farm_id`                | Identificador único da fazenda                           |
| `periodo`                | Período ou ciclo de produção (ex.: ano, mês, semana)     |
| `OEE`                    | Eficácia Geral do Equipamento (%)                        |
| `Disponibilidade`        | Proporção de tempo disponível (Availability) (%)         |
| `Desempenho`             | Eficiência de produção (Performance) (%)                 |
| `Qualidade`              | Proporção de produtos conformes (Quality) (%)            |
| `Paradas_planejadas`     | Tempo planejado de parada (minutos ou horas)             |
| `Paradas_nao_planejadas` | Tempo não planejado de parada (minutos ou horas)         |
| `Produzidas`             | Total de unidades produzidas                             |
| `Defeituosas`            | Unidades descartadas ou retrabalhadas                    |

---

##  Como Utilizar

Este dataset é utilizado em:

- O script `simulacao_oee.R`, para gerar simulações.
- O dashboard (`app.R` ou similar) para visualização interativa dos KPI OEE.

### Exemplo simples de uso em R:

```r
library(readr)
dados <- read_csv("data/dados_leite.csv")
str(dados)
summary(dados$OEE)
