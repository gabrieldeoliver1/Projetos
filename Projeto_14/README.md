# Detecção Automática de Resenhas Negativas de Filmes

## Descrição do Projeto
Este projeto visa desenvolver um protótipo de modelo de aprendizado de máquina que detecta automaticamente resenhas negativas de filmes. Utilizando um conjunto de dados de avaliações de filmes do IMDB, o objetivo é classificar as resenhas como positivas ou negativas, alcançando uma pontuação F1 de, no mínimo, 0,85.

## Tecnologias Utilizadas
- **Python**: Linguagem principal para análise e desenvolvimento do modelo.
- **Jupyter Notebook**: Ambiente interativo para execução do código e visualização dos resultados.

### Bibliotecas:
- **Pandas**: Manipulação e análise de dados tabulares.
- **NumPy**: Operações numéricas e manipulação de arrays.
- **Matplotlib**: Visualização de dados por meio de gráficos.
- **Seaborn**: Gráficos estatísticos avançados.
- **Scikit-learn**: Implementação de algoritmos de aprendizado de máquina.
- **NLTK**: Processamento de linguagem natural e remoção de stopwords.
- **SpaCy**: Tokenização e lematização de texto.
- **LightGBM**: Modelo de boosting eficiente para classificação.
- **BERT**: Modelo de linguagem pré-treinado para extração de embeddings.

## Funcionalidades Implementadas

1. **Coleta e Carregamento dos Dados**:
   - Dados de resenhas de filmes coletados do IMDB e armazenados em um arquivo `.tsv`.

2. **Limpeza e Pré-processamento dos Dados**:
   - Normalização de textos, remoção de números e pontuações.
   - Aplicação de técnicas de tokenização e lematização para processar o texto.

3. **Análise Exploratória de Dados (EDA)**:
   - Visualização de distribuições e padrões dos dados, incluindo gráficos de barras, dispersão e histogramas para análise de variáveis como ano de lançamento, gêneros e polaridade.

4. **Divisão dos Dados**:
   - Separação dos dados em conjuntos de treinamento e teste para garantir uma avaliação imparcial dos modelos.

5. **Modelagem Preditiva**:
   - Teste de diferentes modelos de aprendizado de máquina, incluindo:
     - **Dummy Classifier**: Modelo de base para comparação.
     - **Regressão Logística**: Com vetorização TF-IDF para capturar a importância dos termos.
     - **LightGBM**: Para um modelo de boosting rápido e eficiente.
     - **BERT**: Modelo avançado para extração de embeddings semânticos dos textos.

6. **Avaliação dos Modelos**:
   - Cada modelo foi avaliado com métricas como:
     - **Acurácia**
     - **F1 Score**
     - **ROC AUC**
     - **Average Precision Score (APS)**

7. **Validação do Modelo**:
   - Validação cruzada para garantir a robustez e generalização dos modelos.

8. **Geração de Relatórios**:
   - Relatórios de avaliação dos modelos com visualizações das curvas ROC, precisão e recall, além de gráficos de importância das features.


## Clone

Como Executar o Projeto Clone o repositório:

```bash
  Copiar git clone https://github.com/gabrieldeoliver1/Projetos.git Navegue até o diretório do projeto:
```

```bash
  Copiar cd Projeto_14 Abra o notebook:
```





## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com


