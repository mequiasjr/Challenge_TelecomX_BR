# Challenge_TelecomX_BR

# Telecom X - Análise de Evasão de Clientes

## Propósito da Análise
Esta análise exploratória de dados (EDA) investiga os fatores que contribuem para a evasão de clientes (Churn) na Telecom X, uma empresa de telecomunicações. A evasão impacta diretamente a receita e a reputação, e o objetivo é identificar padrões e insights que orientem estratégias de retenção, com base em dados extraídos de uma API. A análise revelou que contratos de curto prazo, ausência de serviços adicionais e mensalidades altas são os principais drivers de churn, com recomendações para melhorar a retenção.

## Estrutura do Projeto e Organização dos Arquivos
- **TelecomX_BR.ipynb**: Notebook principal com as etapas de extração, transformação, análise e relatório final. Contém o código para carregar dados, tratar inconsistências, criar a coluna `DailyCharges`, realizar análises descritivas e de correlação, e gerar visualizações.
- **TelecomX_dicionario.md**: Dicionário de dados com a descrição das colunas do dataset.
- **TelecomX_Data.json**: Dados brutos carregados diretamente da API.

## Exemplos de Gráficos e Insights Obtidos
- **Distribuição de Evasão**: Gráfico de barras mostrando a taxa de churn (aproximadamente calculada dinamicamente no notebook). Insight: A taxa de evasão indica a proporção de clientes que deixaram a empresa.
- **Evasão por Contrato**: Gráfico de barras indicando que contratos mensais (Month-to-month) têm maior churn em comparação com contratos de um ou dois anos. Insight: Contratos de longo prazo reduzem significativamente a evasão.
- **Distribuição de Tenure por Evasão**: Boxplot mostrando que clientes com menor `Tenure` (tempo de contrato) são mais propensos a churn. Insight: Clientes novos são um grupo de risco para evasão.
- **Matriz de Correlação**: Heatmap revelando forte correlação negativa entre `Tenure` e `Churn`, e correlação positiva entre `MonthlyCharges` e `Churn`. Insight: Clientes antigos churnam menos, enquanto mensalidades altas aumentam a evasão.
- **Evasão por Serviços Adicionais**: Gráficos de barras mostrando que clientes sem `OnlineSecurity` ou `TechSupport` têm maior probabilidade de churn. Insight: Serviços adicionais aumentam a retenção.
- **Evasão por Método de Pagamento**: Gráfico indicando que `Electronic check` está associado a maior evasão. Insight: Métodos de pagamento automáticos podem melhorar a retenção.

## Instruções para Executar o Notebook
1. Faça upload do arquivo `TelecomX_BR.ipynb` no Google Colab.
2. Execute a célula inicial para instalar as dependências, se necessário:
   ```bash
   !pip install pandas numpy matplotlib seaborn requests
   ```
3. Execute todas as células do notebook sequencialmente. O notebook inclui:
   - Extração de dados da API.
   - Tratamento de inconsistências e criação da coluna `DailyCharges`.
   - Análises descritivas, visualizações (gráficos de barras, boxplots, heatmap) e cálculo da taxa de evasão.
   - Relatório final em Python com conclusões e recomendações.
4. Verifique os gráficos gerados e o relatório final exibido na última célula.

**Notas**:
- **Dependências**: Requer Python 3.8+ e as bibliotecas listadas.
- **Possíveis Problemas**: Valores ausentes em `Churn` são tratados no notebook (removidos). Colunas numéricas como `MonthlyCharges` e `TotalCharges` são convertidas de string para float.

