# Previsão do Valor de Mercado de Carros Usados

> **Resultado:** **XGBoost** com RMSE de **1.543 euros** no teste, apenas 1% acima do LightGBM, mas com previsões **cerca de 26 vezes mais rápidas**, o melhor equilíbrio entre qualidade e velocidade para o aplicativo. O erro é cerca de 45% menor que o da Regressão Linear.

## Problema de negócio

O serviço de venda de carros usados Rusty Bargain está desenvolvendo um aplicativo em que o cliente descobre rapidamente o valor de mercado do seu carro. O modelo precisa equilibrar três critérios: qualidade da previsão, velocidade da previsão e tempo de treinamento.

## Dados

- 354.369 anúncios de carros, com especificações técnicas, quilometragem e preço
- 326.965 anúncios após remover preços abaixo de 100 euros e anos de registro impossíveis

## Abordagem

1. **Pré-processamento:** remoção de preços e anos impossíveis, correção de potências impossíveis com a mediana do mesmo modelo e categoria "unknown" para valores ausentes.
2. **Divisão dos dados:** 60% treino, 20% validação e 20% teste, com semente fixa.
3. **Modelagem:** Regressão Linear (linha de base, com one-hot encoding), Árvore de Decisão, Random Forest, XGBoost e LightGBM (com early stopping).
4. **Avaliação:** RMSE e tempos de **treino** e de **previsão** medidos separadamente na validação; os dois melhores modelos avaliados no teste.

## Resultados

| Modelo | RMSE (validação) | Treino | Previsão |
|---|---|---|---|
| LightGBM | 1.524 | 23 s | 17,4 s |
| **XGBoost** | **1.535** | **7 s** | **0,6 s** |
| Random Forest (100 árvores) | 1.590 | 48 s | 1,7 s |
| Árvore de Decisão (profundidade 15) | 1.927 | 0,6 s | 0,01 s |
| Regressão Linear (linha de base) | 2.817 | 0,4 s | 0,1 s |

No **teste**: LightGBM com RMSE de 1.527 euros e XGBoost com 1.543. O preço médio dos anúncios é de 4.652 euros.

## Conclusão para o negócio

O **XGBoost** é o modelo recomendado: o erro é só 1% maior que o do LightGBM, mas as previsões são cerca de 26 vezes mais rápidas, o que importa em um aplicativo em que o cliente espera a resposta na hora.

## Correção desta versão

A versão anterior substituía preços e potências baixos por valores sem sentido (o próprio preço era usado como posição em uma tabela de médias, e a potência recebia médias de preço), não tratava anos de registro impossíveis, não fixava a divisão dos dados e avaliava os modelos só na validação. Com os dados corrigidos, todos os erros mudaram: o melhor RMSE passou de 2.701 (com dados corrompidos) para cerca de 1.530 euros.

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · XGBoost · LightGBM · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_12
pip install pandas numpy scikit-learn xgboost lightgbm jupyter
jupyter notebook
```

O conjunto de dados (`car_data.csv`) foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, coloque o arquivo na mesma pasta do notebook.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
