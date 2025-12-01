# ML-Previsao-Turistas
O turismo é um dos setores principais da economia portuguesa, impactando diretamente os níveis de emprego, receita e investimento. Esta análise permite identificar padrões sazonais e tendências, bem como construir previsões fundamentadas para apoio ao planeamento económico e logístico do setor.

### Objetivo

Analisar a série temporal do número de hóspedes estrangeiros em alojamentos turísticos em Portugal (2013–2025) e desenvolver um modelo preditivo que permita estimar o número de turistas no futuro (até 2026), tendo em conta efeitos de sazonalidade e tendência.

### Processo / metodologia
1. Importação & limpeza de dados
2. Análise exploratória
3. Análise de dependências temporais
4. Estacionarização da série
5. Modelação
6. Validação e análise de resíduos
7. Previsão dentro-amostra & fora da amostra

### Ferramentas utilizadas
- R
    - Biblioteca **fpp3** (tsibble, fable, feasts)
    - ggplot2 para gráficos
    - Modelo SARIMA
 
### Resultados
- O modelo SARIMA(1,1,1)(2,1,0)₁₂ foi o mais eficaz segundo AIC, AICc e BIC.
- Erro de previsão no período de teste:
    - **RMSE:** ~142.000 turistas
    - **MAPE:** ~7.73%
- O modelo capturou corretamente tendência e sazonalidade da série.
- Previsões mostram crescimento gradual com forte sazonalidade, especialmente entre Junho–Setembro.
- Estimativa de aumento homólogo previsto:
    - **2025-S1 vs 2024-S1:** +2.68%
    - **2026-S1 vs 2025-S1:** +7.87%
- **Conclusão**: modelo estatisticamente robusto, resíduos comportam-se como ruído branco.
- **Limitação**: não há variáveis externas (PIB, clima, eventos especiais, preços de hotel, etc.)
