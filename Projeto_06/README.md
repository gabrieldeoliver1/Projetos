# Preferências de Passageiros e Impacto do Clima em Corridas de Táxi

> **Resultado:** a Flash Cab lidera o mercado de táxis de Chicago, o Loop é o principal destino, e a duração das corridas do Loop ao Aeroporto O'Hare muda em sábados chuvosos (valor-p ≈ 3,4e-7).

## Problema de negócio

Uma empresa de corridas quer analisar os dados dos concorrentes no mercado de táxis de Chicago para entender as preferências dos passageiros e o impacto de fatores externos, como o clima, nas corridas.

## Dados

- Dados de corridas de 64 empresas de táxi em Chicago, com número de corridas por empresa
- Média de corridas por bairro de destino
- 864 corridas do Loop ao Aeroporto Internacional O'Hare, com horário, condição do clima e duração
- Os dados são resultados de consultas SQL a um banco de dados de corridas e de condições meteorológicas

## Abordagem

1. **Pré-processamento:** correção de tipos de dados e remoção de corridas com duração implausível.
2. **Análise exploratória:** ranking de empresas e bairros de destino.
3. **Teste de hipóteses:** comparação da duração média das corridas do Loop ao O'Hare em sábados chuvosos e em sábados com tempo bom.

## Resultados

- **Empresas:** a Flash Cab lidera com 19.558 corridas, seguida pela Taxi Affiliation Services (11.422) e pela Medallion Leasing (10.367).
- **Destinos:** Loop (média de 10.727 corridas), River North (9.524) e Streeterville (6.665) são os bairros mais procurados.
- **Clima:** a duração média das corridas do Loop ao O'Hare é diferente em sábados chuvosos (valor-p ≈ 3,4e-7, abaixo do nível de significância de 5%).

## Conclusão para o negócio

A demanda está concentrada em poucos bairros centrais e em uma empresa líder, o que orienta onde concentrar motoristas. O clima afeta a duração das corridas para o aeroporto e deve ser considerado na estimativa de tempo e no preço das viagens.

## Tecnologias

Python · Pandas · SciPy · Matplotlib · Seaborn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_06
pip install pandas scipy matplotlib seaborn jupyter
jupyter notebook
```

Os conjuntos de dados (resultados das consultas SQL) foram fornecidos pela TripleTen durante o bootcamp e não estão incluídos no repositório. Para reproduzir o projeto, ajuste os caminhos dos arquivos na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
