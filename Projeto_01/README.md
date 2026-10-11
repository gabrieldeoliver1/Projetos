# Comportamento de Usuários de Streaming de Música em Duas Cidades

> **Resultado:** a atividade dos usuários varia conforme o dia da semana e a cidade, mas as preferências de gênero musical são praticamente iguais nas duas cidades. Das três hipóteses testadas, uma foi confirmada e duas foram rejeitadas.

## Problema de negócio

Um serviço de streaming de música (dados do Yandex.Music) quer entender se os usuários de duas cidades, Springfield e Shelbyville, escutam música de forma diferente. O objetivo é testar hipóteses sobre o comportamento dos usuários antes de tomar decisões de negócio.

## Dados

- 65.079 registros de músicas tocadas, com usuário, música, artista, gênero, cidade, horário e dia da semana
- Dados de três dias da semana: segunda, quarta e sexta-feira

## Abordagem

1. **Pré-processamento:** padronização dos nomes das colunas, tratamento de valores ausentes, remoção de 3.826 registros duplicados e correção de duplicatas implícitas no gênero (por exemplo, `hip`, `hop` e `hip-hop` unificados em `hiphop`).
2. **Teste das hipóteses:** agrupamento dos dados por cidade, dia da semana e faixa de horário para comparar volume de músicas e gêneros mais ouvidos.

## Resultados

**Hipótese 1 – a atividade varia por dia da semana e cidade: confirmada**

| Cidade | Segunda | Quarta | Sexta |
|---|---|---|---|
| Springfield | 15.740 | 11.056 | 15.945 |
| Shelbyville | 5.614 | 7.003 | 5.895 |

Em Springfield, o pico é na segunda e na sexta, com queda na quarta. Em Shelbyville acontece o contrário: a quarta é o dia de maior atividade.

**Hipótese 2 – os gêneros ouvidos na segunda de manhã e na sexta à noite diferem entre as cidades: rejeitada.** Os gêneros mais ouvidos são praticamente os mesmos nas duas cidades nesses períodos.

**Hipótese 3 – Shelbyville prefere rap e Springfield prefere pop: rejeitada.** Pop é o gênero mais ouvido nas duas cidades, e o rap não aparece entre os cinco primeiros em nenhuma delas.

**Limitação:** a quantidade de registros sem gênero informado é alta o suficiente para aparecer entre os 15 gêneros mais ouvidos em Springfield, o que pede cautela na interpretação da hipótese 2.

## Tecnologias

Python · Pandas · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_01
pip install pandas jupyter
jupyter notebook
```

O conjunto de dados foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, ajuste o caminho do arquivo na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
