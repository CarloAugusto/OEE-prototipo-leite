# OEE (Overall Equipment Effectiveness) — Protótipo no Setor Lácteo

Este repositório apresenta um **protótipo de dashboard de OEE** (Eficácia Geral do Equipamento), aplicado a uma **linha fictícia de envase de leite UHT**.  
O objetivo é **demonstrar habilidades em análise de dados, simulação de indicadores industriais e visualização em Power BI**.

---

## Objetivo do Projeto

- Simular dados de produção de uma linha de envase de leite UHT.  
- Calcular os indicadores de **Disponibilidade, Performance e Qualidade**.  
- Desenvolver um **dashboard interativo no Power BI** para análise e tomada de decisão.  
- Demonstrar aplicação prática de **KPIs industriais** e boas práticas de visualização.  

---

## O que é OEE?

OEE é um **KPI (Key Performance Indicator) de excelência operacional** que combina três dimensões em uma única métrica:

- **Disponibilidade (%)** → mede perdas por paradas não planejadas  
- **Performance (%)** → mede perdas por redução de velocidade  
- **Qualidade (%)** → mede perdas por produtos defeituosos  

O cálculo é: 

$OEE = Disponibilidade \times Performance \times Qualidade$
Um OEE de **100%** significa que a linha produz **apenas produtos bons**, **o mais rápido possível**, **sem perdas de tempo**.

---

## Metodologia

### 1. Simulação de dados (Excel/Google Sheets)
Cenário: uma linha de produção de leite UHT (480 minutos por turno).  
Variáveis simuladas incluem:
- Tempo planejado, paradas não planejadas  
- Velocidade teórica da máquina  
- Produção total vs. defeituosa  
- Turno, produto e data  

---

### 2. Cálculo dos KPIs
Indicadores calculados diretamente na planilha:
- `Disponibilidade_% = (Tempo_Real / Tempo_Planejado) * 100`
- `Performance_% = (Produção Real / Produção Teórica) * 100`
- `Qualidade_% = (Caixas Boas / Caixas Produzidas) * 100`
- `OEE_% = Disponibilidade × Performance × Qualidade`

### 🔹 Disponibilidade
- **Mede**: perdas de tempo por paradas não planejadas.  
- **Pergunta-chave**: *"Quanto tempo a máquina realmente operou em comparação com o tempo que deveria ter operado?"*  
- **Cálculo**: `(Tempo em Produção) / (Tempo Total Planejado)`  
- **Exemplos de perdas**: quebras de equipamento, falta de matéria-prima, tempo de setup e ajustes.  

### 🔹 Performance (ou Desempenho)
- **Mede**: perdas de velocidade.  
- **Pergunta-chave**: *"A máquina produziu na velocidade máxima projetada?"*  
- **Cálculo**: `(Produção Real) / (Produção Teórica no Tempo em Produção)`  
- **Exemplos de perdas**: pequenas paradas não registradas, operação em velocidade reduzida, equipamento desgastado.  

### 🔹 Qualidade
- **Mede**: perdas por produtos defeituosos.  
- **Pergunta-chave**: *"Quantos produtos fabricados estão bons e prontos para o cliente?"*  
- **Cálculo**: `(Produtos Bons) / (Produção Real Total)`  
- **Exemplos de perdas**: retrabalho, sucata, produtos descartados.  

---

### 3. Construção do Dashboard (Power BI)
- **Cards de KPIs**: OEE, Disponibilidade, Performance, Qualidade  
- **Gráfico de linha**: evolução do OEE ao longo do tempo  
- **Filtros (slicers)**: seleção por turno, produto e data  

---

### 4. Publicação
- Protótipo documentado no GitHub  

---

## Estrutura do Repositório

```OEE-prototipo-leite/
├── data/
│   ├── README.md
│   ├── oee_prototipo_leite.csv
│   └── oee_prototipo_leite.db
│
├── docs/
│   ├── README.md
│   └── script_simulation.R
│
├── LICENSE
├── README.md   # principal
├── dashboard_oee.pbix
└── .gitattributes

