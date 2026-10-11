# Padrões de Sucesso de Videogames

> **Resultado:** a nota da crítica tem correlação moderada com as vendas (0,39 no PS4), enquanto a nota dos usuários praticamente não tem relação (0,002). PS4 e Xbox One eram as plataformas mais promissoras para a campanha de 2017.

## Problema de negócio

A loja online Ice vende videogames no mundo todo. O objetivo é identificar padrões que determinam o sucesso de um jogo, para apostar nos títulos com mais potencial e planejar as campanhas publicitárias de 2017.

## Dados

- 16.715 jogos, com plataforma, ano de lançamento, gênero, vendas por região (América do Norte, Europa, Japão e outras), notas da crítica e dos usuários e classificação etária (ESRB)

## Abordagem

1. **Pré-processamento:** padronização de colunas, tratamento de valores ausentes (incluindo o valor "tbd" nas notas dos usuários) e criação da coluna de vendas totais.
2. **Análise exploratória:** ciclo de vida das plataformas, vendas por plataforma e gênero, e correlação entre notas e vendas.
3. **Perfil por região:** plataformas, gêneros e classificações etárias mais vendidos em cada região.
4. **Testes de hipóteses:** comparação das notas médias dos usuários entre plataformas e entre gêneros.

## Resultados

- **Ciclo de vida:** as plataformas duram em média cerca de 7 anos.
- **Plataformas promissoras:** PS4, Xbox One, WiiU e PC. O PS4 tem a maior venda média por jogo (0,80 milhão), seguido do Xbox One (0,65 milhão).
- **Notas e vendas (PS4):** correlação de 0,39 com a nota da crítica e de 0,002 com a nota dos usuários.
- **Gêneros:** tiro, ação e esportes vendem mais; luta, aventura e quebra-cabeça vendem menos.
- **Classificação etária:** jogos "M" (17+) lideram na América do Norte e na Europa; no Japão, lideram os jogos "E" (livre).

| Hipótese | Valor-p | Conclusão |
|---|---|---|
| As notas médias dos usuários de Xbox One e PC são iguais | 0,66 | Não rejeitada |
| As notas médias dos usuários de Ação e Esportes são diferentes | ≈ 3,6e-9 | Confirmada |

## Conclusão para o negócio

Para 2017, a recomendação é concentrar a campanha em jogos de PS4 e Xbox One, nos gêneros de tiro, ação e esportes, usando a nota da crítica como sinal de potencial de vendas e adaptando o portfólio ao perfil de cada região.

## Tecnologias

Python · Pandas · NumPy · SciPy · Matplotlib · Seaborn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_05
pip install pandas numpy scipy matplotlib seaborn jupyter
jupyter notebook
```

O conjunto de dados foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, ajuste o caminho do arquivo na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
