# Projeto de Previsão de Churn - Case Inteli Academy

Este projeto desenvolve um modelo de Machine Learning supervisionado para prever a rotatividade (churn) de clientes de uma empresa fictícia de telecomunicações, a TelecomPlus.

## Contexto do Desafio

A TelecomPlus está enfrentando alta taxa de cancelamento de serviços. Como cientista de dados, fui designado para desenvolver um modelo preditivo que identifique clientes com maior probabilidade de cancelar seus serviços nos próximos 3 meses, permitindo que a empresa tome medidas proativas de retenção.

## Objetivos

- Desenvolver um processo completo de modelagem supervisionada
- Aplicar técnicas de pré-processamento e engenharia de features
- Implementar e comparar diferentes algoritmos de classificação
- Interpretar resultados para apoiar decisões de negócio

## Exploração de Dados

A fase exploratória incluiu:

- **Análise estatística descritiva** utilizando `.info()` e `.describe()`
- **Análise de frequência** para variáveis categóricas
- **Visualizações** com matrizes de correlação
- **Identificação de insights** sobre padrões de churn

### Principais Hipóteses Testadas

1. **Gastos mensais x Churn**: A média de gastos é similar entre quem cancela e quem permanece
2. **Reclamações x Churn**: Clientes que cancelam têm ligeiramente mais reclamações
3. **Tempo como cliente x Churn**: Clientes mais antigos tendem a cancelar menos

## Pré-processamento

- **Conversão de variáveis categóricas** usando Label Encoding e One-Hot Encoding
- **Categorização de idade** em faixas etárias
- **Normalização** de variáveis numéricas
- **Tratamento** de valores ausentes e outliers
- **Remoção** de colunas não-informativas (ex: id_cliente)

## Modelagem

### Abordagem

- Divisão dos dados com `train_test_split`
- Engenharia de features criando novas variáveis derivadas

### Algoritmos Testados

1. **Random Forest**: 72% de acurácia (melhor desempenho)
2. **XGBoost**: ~70% de acurácia
3. **Regressão Logística**: menor desempenho (baseline)

### Otimização

- Uso de GridSearch para otimização de hiperparâmetros
- Comparação de modelos por acurácia, ROC-AUC e interpretabilidade

## Resultados

O modelo final escolhido foi o **Random Forest**, que apresentou o melhor equilíbrio entre performance (72% de acurácia) e capacidade de generalização. A análise das features mais importantes também forneceu informações sobre os principais fatores que influenciam o churn.



