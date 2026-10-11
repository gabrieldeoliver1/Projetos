# Previsão do Valor de Mercado de Carros Usados

> **Resultado:** **RMSE de 2.701** com LightGBM, o melhor equilíbrio entre qualidade e velocidade entre os cinco modelos testados.

## Problema de negócio

O serviço de venda de carros usados Rusty Bargain está desenvolvendo um aplicativo em que o cliente descobre rapidamente o valor de mercado do seu carro. O modelo precisa equilibrar três critérios: qualidade da previsão, velocidade da previsão e tempo de treinamento.

## Dados

- 354.369 anúncios de carros, com especificações técnicas, versão, quilometragem e preço
- 251.133 registros após a limpeza

## Abordagem

1. **Pré-processamento:** tratamento de valores ausentes e anômalos, remoção de duplicatas e de colunas sem relevância para o preço, e codificação de variáveis categóricas.
2. **Modelagem:** comparação entre Regressão Linear (linha de base), Árvore de Decisão, Random Forest, XGBoost e LightGBM.
3. **Avaliação:** RMSE e tempo de execução de cada modelo.

## Resultados

| Modelo | RMSE | Tempo de execução |
|---|---|---|
| **LightGBM** | **2.701** | **3,5 s** |
| XGBoost | 2.709 | 7,9 s |
| Árvore de Decisão (profundidade 12) | 2.831 | 19,9 s |
| Random Forest | 2.993 | 0,9 s |
| Regressão Linear (linha de base) | 3.463 | 0,1 s |

## Conclusão para o negócio

O LightGBM teve o menor erro e um tempo de execução baixo, sendo o modelo recomendado para o aplicativo. A Regressão Linear, embora mais rápida, tem erro cerca de 28% maior.

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · XGBoost · LightGBM · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_12
pip install pandas numpy scikit-learn xgboost lightgbm jupyter
jupyter notebook
```

O conjunto de dados foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, ajuste o caminho do arquivo na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
