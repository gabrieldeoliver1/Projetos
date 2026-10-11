# Previsão da Recuperação de Ouro em um Processo Industrial

> **Resultado:** sMAPE final de **7,84%** na previsão da recuperação de ouro, com Regressão Linear.

## Problema de negócio

A Zyfra desenvolve soluções de eficiência para a indústria pesada. O objetivo é criar um protótipo de modelo que preveja a quantidade de ouro recuperada do minério durante a extração e a purificação, ajudando a otimizar a produção e a eliminar parâmetros não rentáveis.

## Dados

- Dados do processo de extração e purificação de ouro, divididos em conjunto de treino (16.860 registros e 87 variáveis), conjunto de teste (5.856 registros) e conjunto completo
- Duas variáveis-alvo: a recuperação de ouro na etapa de flotação (concentrado bruto) e no concentrado final

## Abordagem

1. **Validação dos dados:** conferência do cálculo da recuperação de ouro a partir das concentrações em cada etapa.
2. **Pré-processamento:** preenchimento de valores ausentes e verificação de duplicatas.
3. **Análise exploratória:** variação das concentrações de ouro, prata e chumbo em cada etapa da purificação e comparação das distribuições de tamanho de partícula entre treino e teste.
4. **Tratamento de anomalias:** remoção de registros com concentração total anormal das substâncias.
5. **Modelagem:** Regressão Linear para prever as duas etapas, avaliada com sMAPE (erro percentual absoluto médio simétrico).

## Resultados

| Etapa | sMAPE |
|---|---|
| Flotação (concentrado bruto) | 6,14% |
| Concentrado final | 8,41% |
| **sMAPE final ponderado (25% flotação, 75% final)** | **7,84%** |

## Próximos passos

- Comparar a Regressão Linear com modelos baseados em árvores, como Random Forest e LightGBM, usando validação cruzada
- Avaliar o modelo contra uma linha de base que preveja a média, para medir o ganho real

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · Matplotlib · Seaborn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_10
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook
```

Os conjuntos de dados foram fornecidos pela TripleTen durante o bootcamp e não estão incluídos no repositório. Para reproduzir o projeto, ajuste os caminhos dos arquivos na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
