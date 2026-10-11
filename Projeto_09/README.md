# Escolha da Melhor Região para Novos Poços de Petróleo

> **Resultado:** a **Região 1** foi recomendada por ser a única com risco de prejuízo abaixo do limite de 2,5% (risco de 1,4%), com lucro médio estimado de **US$ 4,49 milhões**.

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
| 0 | 37,80 | US$ 4,85 mi | –US$ 0,05 mi a US$ 9,84 mi | 2,7% |
| **1** | **0,89** | **US$ 4,49 mi** | **US$ 0,30 mi a US$ 8,47 mi** | **1,4%** |
| 2 | 39,98 | US$ 3,64 mi | –US$ 1,23 mi a US$ 8,58 mi | 7,2% |

## Correção desta versão

Na versão anterior, a amostragem com reposição do bootstrapping podia sortear o mesmo poço mais de uma vez, e a seleção dos melhores poços contava cópias extras desses poços, inflando o lucro. Com a correção, os lucros médios diminuíram e os riscos aumentaram um pouco, mas a recomendação se manteve.

## Conclusão para o negócio

A Região 0 tem lucro médio um pouco maior, mas ultrapassa o limite de risco de 2,5%. A Região 1 é a única dentro do limite, a única com intervalo de confiança inteiro acima de zero e a que tem o modelo mais preciso, sendo a recomendação para o desenvolvimento dos novos poços.

## Tecnologias

Python · Pandas · NumPy · SciPy · Scikit-learn · Matplotlib · Seaborn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_09
pip install pandas numpy scipy scikit-learn matplotlib seaborn jupyter
jupyter notebook
```

Os conjuntos de dados (`geo_data_0.csv` a `geo_data_2.csv`) foram fornecidos pela TripleTen durante o bootcamp e não estão incluídos no repositório. Para reproduzir o projeto, coloque os arquivos na mesma pasta do notebook.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
