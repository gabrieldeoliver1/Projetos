# Escolha da Melhor Região para Novos Poços de Petróleo

> **Resultado:** a **Região 1** foi recomendada por ser a única com risco de prejuízo abaixo do limite de 2,5% (risco de 0,7%), com lucro médio estimado de **US$ 5,07 milhões**.

## Problema de negócio

A mineradora OilyGiant precisa decidir onde desenvolver 200 novos poços de petróleo, com orçamento de US$ 100 milhões. O objetivo é escolher, entre três regiões, a que oferece o maior lucro com risco de prejuízo inferior a 2,5%.

## Dados

- Três regiões, com 100.000 poços cada
- Três características geológicas por poço e o volume de reservas (em milhares de barris)

## Abordagem

1. **Modelagem:** um modelo de Regressão Linear por região para prever o volume de reservas de cada poço.
2. **Cálculo de lucro:** seleção dos 200 poços com maior volume previsto e cálculo do lucro esperado, considerando receita de US$ 4.500 por mil barris.
3. **Análise de risco com bootstrapping:** 1.000 simulações de estudos com 500 pontos por região, para estimar o lucro médio, o intervalo de confiança de 95% e o risco de prejuízo.

## Resultados

| Região | RMSE do modelo | Lucro médio | Intervalo de confiança de 95% | Risco de prejuízo |
|---|---|---|---|---|
| 0 | 37,80 | US$ 5,15 mi | US$ 0,11 mi a US$ 10,55 mi | 2,5% |
| **1** | **0,89** | **US$ 5,07 mi** | **US$ 0,79 mi a US$ 9,32 mi** | **0,7%** |
| 2 | 39,98 | US$ 3,87 mi | –US$ 1,36 mi a US$ 9,03 mi | 6,7% |

## Conclusão para o negócio

A Região 0 tem lucro médio um pouco maior, mas atinge o limite de risco de 2,5%. A Região 1 combina lucro médio próximo, menor risco de prejuízo e o modelo mais preciso, sendo a recomendação para o desenvolvimento dos novos poços.

## Tecnologias

Python · Pandas · NumPy · SciPy · Scikit-learn · Matplotlib · Seaborn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_09
pip install pandas numpy scipy scikit-learn matplotlib seaborn jupyter
jupyter notebook
```

Os conjuntos de dados foram fornecidos pela TripleTen durante o bootcamp e não estão incluídos no repositório. Para reproduzir o projeto, ajuste os caminhos dos arquivos na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
