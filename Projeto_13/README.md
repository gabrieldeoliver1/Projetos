# Previsão da Quantidade de Pedidos de Táxi para a Próxima Hora

> **Resultado:** RMSE de **44,58** no conjunto de teste com Random Forest, bem dentro da meta do projeto (RMSE ≤ 48), usando validação cruzada temporal e a hora do dia como variável.

## Problema de negócio

A Sweet Lift Taxi coletou o histórico de pedidos de táxi nos aeroportos e precisa prever quantos pedidos chegarão na próxima hora. Com essa previsão, a empresa consegue atrair mais motoristas para os horários de pico e reduzir o tempo de espera dos passageiros.

## Dados

- 26.496 registros de pedidos em intervalos de 10 minutos, de março a agosto de 2018
- Uma única variável: a quantidade de pedidos (`num_orders`), indexada por data e hora
- Série reamostrada para intervalos de 1 hora, totalizando 4.416 observações

## Abordagem

1. **Análise exploratória:** visualização da série, média móvel e decomposição sazonal, que mostraram uma tendência de crescimento ao longo dos meses e uma sazonalidade diária bem definida.
2. **Engenharia de features:** variáveis de calendário (mês, dia, dia da semana e **hora do dia**), defasagens dos últimos 6 períodos (lags) e média móvel das 10 horas anteriores.
3. **Divisão temporal:** 80% para treino e 20% para teste, sem embaralhar os dados, preservando a ordem cronológica.
4. **Modelagem:** comparação entre Regressão Linear e Random Forest, com ajuste de hiperparâmetros via `GridSearchCV` e **validação cruzada temporal** (`TimeSeriesSplit`). O conjunto de teste não participou do ajuste.

## Resultados

| Modelo | RMSE treino | RMSE teste |
|---|---|---|
| **Random Forest** | 9,26 | **44,58** |
| Regressão Linear | 29,02 | 47,16 |

O Random Forest foi o modelo escolhido. Ele aproveita bem a hora do dia, cujo efeito não é linear ao longo das 24 horas, mas mostra sinais de overfitting (erro bem menor no treino).

## Correções desta versão

A versão anterior usava validação cruzada comum, que em séries temporais pode usar dados do futuro no ajuste, e não tinha a hora do dia como variável. Com as duas correções, o RMSE no teste caiu de 47,99 (Regressão Linear) para 44,58 (Random Forest).

## Próximos passos

- Limitar a profundidade do Random Forest para reduzir o overfitting
- Testar modelos de boosting, como LightGBM

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · Statsmodels · Matplotlib · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_13
pip install pandas numpy scikit-learn statsmodels matplotlib jupyter
jupyter notebook
```

O conjunto de dados (`taxi.csv`) foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, coloque o arquivo na mesma pasta do notebook.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
