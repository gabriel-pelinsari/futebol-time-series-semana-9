## Objetivo do Projeto

Este notebook realiza análise e predição de séries temporais usando dados de partidas internacionais de futebol, implementando três modelos diferentes:

1. **Prophet** (Facebook)
2. **Sktime** (AutoARIMA)
3. **LSTM** (Long Short-Term Memory)

## Dataset

**International Football Results from 1872 to 2025**

🔗 Link do Kaggle: https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017

Este dataset contém mais de 47.000 resultados de partidas internacionais de futebol.

## Como Usar

### Passo 1: Download do Dataset

1. Acesse o link do Kaggle acima
2. Faça login (ou crie uma conta)
3. Clique em "Download" para baixar o arquivo `results.csv`
4. Coloque o arquivo na mesma pasta do notebook

### Passo 2: Instalação das Dependências

O notebook instalará automaticamente todas as bibliotecas necessárias:

```bash
pip install prophet sktime pmdarima tensorflow scikit-learn pandas numpy matplotlib seaborn opendatasets
```

### Passo 3: Executar o Notebook

Abra o notebook `football_time_series_analysis.ipynb` e execute todas as células sequencialmente.

## Estrutura do Notebook

1. **Instalação e Importação de Bibliotecas**
2. **Download e Carregamento dos Dados**
3. **Análise Exploratória e Preparação**
4. **Divisão Train/Test (80/20)**
5. **Modelo 1: Prophet**
6. **Modelo 2: Sktime (AutoARIMA)**
7. **Modelo 3: LSTM**
8. **Comparação de Modelos e Métricas**
9. **Visualização Comparativa**
10. **Conclusões**

## Métricas de Avaliação

O notebook utiliza três métricas principais:

- **MAE** (Mean Absolute Error): Erro médio absoluto
- **RMSE** (Root Mean Squared Error): Raiz do erro quadrático médio
- **MAPE** (Mean Absolute Percentage Error): Erro percentual absoluto médio

### Justificativa das Métricas

Segundo **Hyndman & Athanasopoulos (2018)** em "Forecasting: Principles and Practice":

- **MAE** é robusto a outliers e fácil de interpretar
- **RMSE** penaliza mais erros grandes
- **MAPE** permite comparação entre diferentes escalas

**Referência:** Hyndman, R.J., & Athanasopoulos, G. (2018) *Forecasting: principles and practice*, 2nd edition, OTexts: Melbourne, Australia. OTexts.com/fpp2

## Requisitos

- Python 3.8+
- Jupyter Notebook ou Google Colab
- 4GB+ de RAM recomendado
- Conexão com internet (para instalação de pacotes)

## Resultados Esperados

O notebook gera:

- Análise exploratória dos dados
- Gráficos de séries temporais
- Predições de três modelos diferentes
- Comparação quantitativa com métricas de erro
- Visualizações comparativas

## 🐛 Troubleshooting

### Erro ao carregar dados

Se você receber um erro `FileNotFoundError`:
- Certifique-se de que o arquivo `results.csv` está na mesma pasta do notebook
- Verifique se o nome do arquivo está correto

### Erro de memória

Se o notebook travar por falta de memória:
- Reduza o tamanho do dataset filtrando por anos mais recentes
- Use Google Colab que oferece mais RAM gratuitamente

### Problemas com Prophet

Prophet pode dar warnings sobre sazonalidade. Isso é normal e não afeta os resultados.

## 📚 Referências Bibliográficas

1. Hyndman, R.J., & Athanasopoulos, G. (2018) *Forecasting: principles and practice*, 2nd edition
2. Taylor, S.J., & Letham, B. (2018). Forecasting at scale. *The American Statistician*
3. Löning, M., et al. (2019). sktime: A Unified Interface for Machine Learning with Time Series
4. Hochreiter, S., & Schmidhuber, J. (1997). Long short-term memory. *Neural computation*
