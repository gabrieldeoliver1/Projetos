# Análise do Risco de Inadimplência de Clientes Bancários

> **Resultado:** filhos, estado civil, faixa de renda e finalidade do empréstimo estão associados à inadimplência. A taxa varia de 6,6% (viúvos) a 9,8% (solteiros) e de 7,2% (empréstimos para imóveis) a 9,4% (empréstimos para carros).

## Problema de negócio

A divisão de empréstimos de um banco quer saber se o estado civil e o número de filhos de um cliente influenciam o pagamento em dia. As conclusões serão usadas na construção do modelo de pontuação de crédito do banco.

## Dados

- 21.525 clientes, com informações sobre família, renda, emprego, finalidade do empréstimo e histórico de inadimplência

## Abordagem

1. **Pré-processamento:** padronização de valores, correção de dados inconsistentes, preenchimento de valores ausentes com base em outras características do cliente e remoção de duplicatas.
2. **Categorização:** criação de faixas de renda (A a E) e agrupamento das finalidades de empréstimo em categorias (carro, educação, casamento e imóveis).
3. **Análise:** cálculo da taxa de inadimplência para cada fator.

## Resultados

| Fator | Menor taxa | Maior taxa |
|---|---|---|
| Filhos | Sem filhos: 7,5% | 1 ou 2 filhos: 9,2% a 9,5% |
| Estado civil | Viúvos: 6,6% | Solteiros: 9,8% |
| Faixa de renda | Faixa B: 6,8% | Faixa D: 8,6% |
| Finalidade | Imóveis: 7,2% | Carro: 9,4% |

Grupos com poucos clientes, como famílias com 4 ou 5 filhos, foram interpretados com cautela por causa do tamanho reduzido da amostra.

## Conclusão para o negócio

Clientes sem filhos, casados, viúvos ou divorciados, de faixas de renda mais altas e que pedem crédito para imóveis apresentam menor risco. Esses fatores podem entrar como variáveis no modelo de pontuação de crédito do banco.

## Tecnologias

Python · Pandas · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_02
pip install pandas jupyter
jupyter notebook
```

O conjunto de dados foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, ajuste o caminho do arquivo na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
