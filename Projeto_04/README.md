# Qual Plano de Telefonia Gera Mais Receita

> **Resultado:** os clientes do plano Ultimate geram receita média de US$ 70 por mês, contra US$ 50 do plano Surf. A diferença é estatisticamente significativa (valor-p ≈ 1e-93).

## Problema de negócio

A operadora de telecomunicações Megaline oferece dois planos pré-pagos, Surf e Ultimate. O departamento comercial quer saber qual plano gera mais receita para ajustar o orçamento de publicidade.

## Dados

- Amostra de 500 clientes, com registros de chamadas, mensagens e uso de internet ao longo de 2018
- Cinco tabelas: usuários, chamadas, mensagens, sessões de internet e planos

## Abordagem

1. **Pré-processamento:** correção de tipos de dados, tratamento de duplicatas e valores ausentes.
2. **Agregação mensal:** cálculo, para cada cliente e mês, do total de minutos, mensagens e dados usados, e da receita considerando as cobranças acima do limite do plano.
3. **Análise estatística:** média, variância e desvio padrão do consumo e da receita em cada plano.
4. **Testes de hipóteses:** comparação da receita média entre os planos e entre a região de NY-NJ e as demais regiões.

## Resultados

| Plano | Receita média mensal por cliente | Desvio padrão |
|---|---|---|
| Ultimate | US$ 70,34 | US$ 2,62 |
| Surf | US$ 50,13 | US$ 33,91 |

| Hipótese | Valor-p | Conclusão |
|---|---|---|
| A receita média dos planos Surf e Ultimate é igual | ≈ 1e-93 | Rejeitada: as receitas são diferentes |
| A receita média de NY-NJ é igual à das demais regiões | 0,056 | Não rejeitada ao nível de 5% |

## Conclusão para o negócio

Por cliente, o Ultimate é o plano mais rentável e tem receita estável. O Surf tem receita média menor e muito mais variável, porque muitos clientes ultrapassam os limites do pacote e pagam cobranças extras, o que pode afetar a satisfação. A receita por cliente favorece concentrar o orçamento de publicidade no Ultimate.

## Tecnologias

Python · Pandas · NumPy · SciPy · Matplotlib · Seaborn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_04
pip install pandas numpy scipy matplotlib seaborn jupyter
jupyter notebook
```

Os conjuntos de dados foram fornecidos pela TripleTen durante o bootcamp e não estão incluídos no repositório. Para reproduzir o projeto, ajuste os caminhos dos arquivos na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
