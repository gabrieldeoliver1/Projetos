# Detecção Automática de Resenhas Negativas de Filmes

> **Resultado:** **F1 de 0,88**, acima da meta de 0,85, com **88% de acurácia** e **ROC AUC de 0,95** no conjunto de teste, usando NLTK + TF-IDF + Regressão Logística.

## Problema de negócio

A Film Junky Union, uma comunidade de entusiastas de filmes clássicos, está desenvolvendo um sistema para filtrar e categorizar resenhas. O objetivo é treinar um modelo que identifique automaticamente as resenhas negativas.

## Dados

- 47.331 resenhas de filmes do IMDB, já rotuladas como positivas ou negativas
- Classes balanceadas: 23.715 negativas e 23.616 positivas
- Divisão original do conjunto: 23.796 resenhas para treino e 23.535 para teste

## Abordagem

1. **Análise exploratória:** distribuição de filmes e resenhas ao longo dos anos, número de resenhas por filme e equilíbrio entre as classes.
2. **Pré-processamento do texto:** conversão para minúsculas e remoção de números e pontuação.
3. **Vetorização:** TF-IDF com remoção de stopwords, com duas variações de tratamento do texto (NLTK e lematização com spaCy).
4. **Modelagem:** comparação de quatro modelos, de um baseline constante até LightGBM.
5. **Teste com resenhas próprias:** aplicação dos modelos em resenhas novas, escritas fora do conjunto de dados, para verificar o comportamento em textos reais.

## Resultados (conjunto de teste)

| Modelo | Acurácia | F1 | ROC AUC | APS |
|---|---|---|---|---|
| Baseline (constante) | 50% | – | – | – |
| **NLTK + TF-IDF + Regressão Logística** | **88%** | **0,88** | **0,95** | **0,95** |
| spaCy + TF-IDF + Regressão Logística | 88% | 0,88 | 0,95 | 0,95 |
| spaCy + TF-IDF + LightGBM | 86% | 0,86 | 0,94 | 0,93 |

Os três modelos superam a meta de F1 de 0,85.

O modelo com NLTK e Regressão Logística foi o escolhido: obteve o melhor desempenho com o pré-processamento mais simples e rápido.

**Correção desta versão:** a versão anterior registrava o F1 no limiar 0, o que dava 0,67 para todos os modelos. O cálculo foi corrigido e o notebook foi executado novamente. Também corrigi a seção de resenhas próprias, que usava uma Regressão Logística no lugar do modelo LightGBM.

## Próximos passos

- Testar embeddings de modelos de linguagem pré-treinados (como BERT) em GPU e comparar com o TF-IDF

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · NLTK · spaCy · LightGBM · Matplotlib · Seaborn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_14
pip install pandas numpy scikit-learn nltk spacy lightgbm matplotlib seaborn jupyter
python -m spacy download en_core_web_sm
jupyter notebook
```

O conjunto de dados (`imdb_reviews.tsv`) foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, coloque o arquivo na mesma pasta do notebook. O processamento com spaCy leva cerca de 15 minutos.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
