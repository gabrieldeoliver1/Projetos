# Qual Plano de Telefonia Gera Mais Receita

> **Resultado:** os clientes do plano Ultimate geram receita média de **US$ 72** por mês, contra **US$ 61** do Surf, e a diferença é estatisticamente significativa (valor-p ≈ 3e-15). No Surf, 73% dos meses têm cobranças extras.

## Problema de negócio

A operadora de telecomunicações Megaline oferece dois planos pré-pagos, Surf e Ultimate. O departamento comercial quer saber qual plano gera mais receita para ajustar o orçamento de publicidade.

## Dados

- Amostra de 500 clientes, com registros de chamadas, mensagens e uso de internet ao longo de 2018
- Cinco tabelas: usuários, chamadas, mensagens, sessões de internet e planos

## Abordagem

1. **Pré-processamento:** correção de tipos de dados, tratamento de duplicatas e valores ausentes.
2. **Agregação mensal:** cálculo, para cada cliente e mês, do total de minutos, mensagens e dados usados, e da receita considerando as cobranças acima do limite do plano, com as regras da operadora: cada ligação arredondada para o minuto seguinte e a internet do mês arredondada para o gigabyte seguinte.
3. **Análise estatística:** média, variância e desvio padrão do consumo e da receita em cada plano.
4. **Testes de hipóteses:** comparação da receita média entre os planos e entre a região de NY-NJ e as demais regiões.

## Resultados

| Plano | Receita média mensal por cliente | Desvio padrão | Receita total |
|---|---|---|---|
| Ultimate | US$ 72,31 | US$ 11,40 | US$ 52.066 |
| Surf | US$ 60,71 | US$ 55,39 | US$ 95.491 |

| Hipótese | Valor-p | Conclusão |
|---|---|---|
| A receita média dos planos Surf e Ultimate é igual | ≈ 3e-15 | Rejeitada: as receitas são diferentes |
| A receita média de NY-NJ é igual à das demais regiões | 0,034 | Rejeitada: NY-NJ tem receita menor (US$ 59,92 contra US$ 65,22) |

## Conclusão para o negócio

Por cliente, o Ultimate é o plano mais rentável e tem receita previsível, o que favorece concentrar nele o orçamento de publicidade. O Surf gera mais receita total, por ter mais clientes, mas depende de cobranças extras em 73% dos meses, o que pode afetar a satisfação. Na região de NY-NJ, vale investigar por que a receita por cliente é menor.

## Correção desta versão

Na versão anterior, a duração das ligações e o consumo de internet não eram arredondados para cima, como a operadora cobra, e os testes eram feitos depois de remover os valores atípicos de receita, o que excluía justamente os clientes que pagam cobranças extras. Com o cálculo correto e todos os clientes, a receita média do Surf passou de US$ 50 para US$ 61 e a diferença entre NY-NJ e as demais regiões passou a ser significativa.

## Tecnologias

Python · Pandas · NumPy · SciPy · Matplotlib · Seaborn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_04
pip install pandas numpy scipy matplotlib seaborn jupyter
jupyter notebook
```

Os conjuntos de dados (`megaline_*.csv`) foram fornecidos pela TripleTen durante o bootcamp e não estão incluídos no repositório. Para reproduzir o projeto, coloque os arquivos na mesma pasta do notebook.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
