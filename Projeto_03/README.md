# O Que Determina o Preço de um Carro Usado

> **Resultado:** idade do veículo, quilometragem e condição são os fatores que mais influenciam o preço dos anúncios. As diferenças de preço entre cores acompanham, na verdade, a idade dos carros.

## Problema de negócio

Um site de classificados de veículos publica centenas de anúncios gratuitos por dia. A empresa quer entender quais fatores influenciam o preço de um veículo, a partir dos anúncios publicados nos últimos anos.

## Dados

- 51.525 anúncios de veículos, com preço, ano do modelo, quilometragem, condição, número de cilindros, tipo, transmissão, tração e cor

## Abordagem

1. **Pré-processamento:** padronização de colunas, tratamento de valores ausentes com base em outras características do veículo (por exemplo, ano do modelo e cilindros) e remoção de duplicatas.
2. **Enriquecimento dos dados:** criação de variáveis como idade do veículo no momento do anúncio e quilometragem média por ano.
3. **Valores atípicos:** análise por histogramas, definição de limites e remoção de outliers que distorciam as distribuições.
4. **Análise exploratória:** relação entre preço e cada fator, com foco nos tipos de veículo mais anunciados.

## Resultados

- **Idade do veículo:** carros mais novos têm preços mais altos.
- **Quilometragem:** quanto menor a quilometragem, maior o preço.
- **Condição:** veículos mais conservados são anunciados por valores maiores.
- **Tipo e transmissão:** sedans e SUVs são os tipos mais anunciados. Nos SUVs, a transmissão manual apresentou preço médio maior; nos sedans, a automática.
- **Cor:** carros pretos e brancos têm preços maiores, e verdes e marrons, menores, mas os verdes e marrons são, em mediana, os mais velhos (12 e 10 anos, contra 7). A diferença vem da idade, e não da cor em si.

## Correção desta versão

Na versão anterior, os preços abaixo de 200 dólares eram substituídos por valores tirados da tabela de medianas usando o próprio preço como posição, e não o modelo, o ano e a condição do carro. A quilometragem que continuava ausente era preenchida com 0, e alguns preenchimentos podiam não ter efeito em versões novas do pandas. Tudo foi corrigido e o notebook, executado novamente. As conclusões se mantiveram, com uma leitura mais precisa sobre a cor.

## Tecnologias

Python · Pandas · Matplotlib · Seaborn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_03
pip install pandas matplotlib seaborn jupyter
jupyter notebook
```

O conjunto de dados (`vehicles_us.csv`) foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, coloque o arquivo na mesma pasta do notebook.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
