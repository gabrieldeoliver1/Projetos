# Previsão da Quantidade de Pedidos de Táxi para a Próxima Hora

> **Resultado:** RMSE de **47,99** no conjunto de teste com Regressão Linear, dentro da meta do projeto (RMSE ≤ 48).

## Problema de negócio

A Sweet Lift Taxi coletou o histórico de pedidos de táxi nos aeroportos e precisa prever quantos pedidos chegarão na próxima hora. Com essa previsão, a empresa consegue atrair mais motoristas para os horários de pico e reduzir o tempo de espera dos passageiros.

## Dados

- 26.496 registros de pedidos em intervalos de 10 minutos, de março a agosto de 2018
- Uma única variável: a quantidade de pedidos (`num_orders`), indexada por data e hora
- Série reamostrada para intervalos de 1 hora, totalizando 4.416 observações

## Abordagem

1. **Análise exploratória:** visualização da série, média móvel e decomposição sazonal, que mostraram uma tendência de crescimento ao longo dos meses e uma sazonalidade diária bem definida.
2. **Engenharia de features:** variáveis de calendário (ano, mês, dia e dia da semana), defasagens dos últimos 6 períodos (lags) e média móvel das 10 horas anteriores.
3. **Divisão temporal:** 80% para treino e 20% para teste, sem embaralhar os dados, preservando a ordem cronológica.
4. **Modelagem:** comparação entre Regressão Linear e Random Forest, com ajuste de hiperparâmetros via `GridSearchCV`.

## Resultados

| Modelo | RMSE treino | RMSE teste |
|---|---|---|
| **Regressão Linear** | 29,05 | **47,99** |
| Random Forest | 19,38 | 54,05 |

A Regressão Linear foi o modelo escolhido. O Random Forest teve erro menor no treino, mas pior no teste, um sinal de overfitting.

## Próximos passos

- Usar `TimeSeriesSplit` na validação cruzada, para respeitar a ordem temporal também durante o ajuste de hiperparâmetros
- Incluir a hora do dia como feature, aproveitando a sazonalidade diária identificada na análise exploratória
- Testar modelos de boosting (LightGBM, CatBoost) e modelos próprios de séries temporais

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · Statsmodels · Matplotlib · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_13
pip install pandas numpy scikit-learn statsmodels matplotlib jupyter
jupyter notebook
```

O conjunto de dados (`taxi.csv`) foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, ajuste o caminho do arquivo na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
