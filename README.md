# ⚡ Análise Preditiva ESG & MCDA Espacial para Data Centers (São Paulo)

[![GitHub Pages](https://img.shields.io/badge/Live_Demo-GitHub_Pages-10b981?style=for-the-badge&logo=github)](https://raquelguerreiro21.github.io/esg-datacenters-sp/)
[![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Databricks](https://img.shields.io/badge/Environment-Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)](https://databricks.com/)

---

## 📌 Visão Geral do Projeto

O avanço acelerado da Inteligência Artificial Generativa e da computação em nuvem elevou drasticamente a demanda por novas infraestruturas de **Data Centers**. Contudo, a seleção de áreas para esses empreendimentos enfrenta um dilema crítico: como conciliar a **alta disponibilidade energética** com a **sustentabilidade ambiental (ESG)** e a **resiliência ao aquecimento global**?

Este projeto apresenta um pipeline de **Ciência de Dados Espaciais e Aprendizado de Máquina** desenvolvido no ambiente **Databricks**. O modelo realiza uma **Análise de Decisão Multicritério Espacial (MCDA)** cruzada com **modelagem preditiva de séries temporais** para identificar os melhores polos para instalação de Data Centers na Região Metropolitana de Campinas/SP.

🌐 **Acesse o Mapa Interativo Online:** [https://raquelguerreiro21.github.io/esg-datacenters-sp/](https://raquelguerreiro21.github.io/esg-datacenters-sp/)

---

## 💡 Principais Conclusões e Insights de Negócio

1. **Polos Prioritários Identificados**: O algoritmo de clusterização espacial (DBSCAN) identificou **2 clusters principais contínuos (Clusters 0 e 1)** de alta viabilidade, localizados com fácil acesso à infraestrutura energética e excelente potencial térmico.
2. **Potencial de Resfriamento Natural (Free Cooling)**: A região avaliada apresentou **82,6% de horas favoráveis ao ano** para operação via *Free Cooling* (Temperatura de Bulbo Úmido $T_w < 21^\circ\text{C}$), reduzindo significativamente o consumo de água e energia (PUE/WUE).
3. **Resiliência Preditiva (2024–2030)**: A projeção via algoritmo **Prophet** validou que, apesar da tendência de elevação térmica global, os clusters selecionados mantêm estabilidade operacional superior à média estadual nos próximos anos.
4. **Estabilidade de Seleção (Análise de Sensibilidade)**: Os hexágonos prioritários mantiveram-se no **Top 30%** em 4 cenários estratégicos distintos (correlação de Spearman $r > 0.85$), comprovando a baixa vulnerabilidade a variações nas prioridades dos investidores (CAPEX vs. Operação ESG).

---

## 🛠️ Arquitetura do Pipeline (5 Etapas)

```text
[1. Coleta & Clima] ──► [2. Malha H3 & UTM 23S] ──► [3. Prophet 2024-2030] ──► [4. MCDA + DBSCAN] ──► [5. Folium & Deploy]
