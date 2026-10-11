# Portfólio de Ciência de Dados e Machine Learning

Projetos de **Gabriel de Oliveira**, Cientista de Dados e Analista de Dados Sênior. São 22 projetos que cobrem análise exploratória, estatística, testes de hipóteses, Machine Learning, séries temporais, NLP e visão computacional, sempre partindo de um problema de negócio, com dados da formação em Ciência de Dados na TripleTen e dados públicos, como os do IBGE e o texto da LGPD.

Cada projeto tem um README próprio com o problema, os dados, a abordagem e os resultados.

## ⭐ Projetos em destaque

| Projeto | Problema de negócio | Técnicas | Resultado |
|---|---|---|---|
| [Previsão de Vendas de Material de Construção](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_17) | Prever as vendas do varejo de material de construção para planejar compras e estoque | Séries temporais, SARIMA, validação por origem móvel | MAPE de 3,37%, 25% melhor que a linha de base |
| [Modelo de Risco de Crédito](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_18) | Estimar a probabilidade de inadimplência de clientes de cartão e definir a política de crédito | WoE/IV, scorecard, LightGBM, SHAP | AUC de 0,78, Gini de 0,56 e KS de 0,43 |
| [Teste A/B no Jogo Cookie Cats](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_19) | Decidir se mover o portão de progresso do nível 30 para o 40 melhora a retenção | Teste Z, bootstrap, bayesiano, poder estatístico, testes A/A | Retenção de 7 dias 0,82 p.p. menor no nível 40 (p = 0,0016) |
| [Análise de E-commerce com SQL](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_20) | Entender vendas, logística, retenção e clientes de um e-commerce com 100 mil pedidos | SQL: JOINs, CTEs, funções de janela, coorte e RFM | 97% dos clientes compram uma vez; atrasos derrubam a nota para menos de 2 |
| [Segmentação de Clientes com Clustering](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_21) | Descobrir perfis de compra para direcionar ações de marketing | K-means, teste de estabilidade, PCA, árvore de decisão | 5 personas; 15% dos clientes geram 40% da receita |
| [Assistente da LGPD com RAG](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_22) | Responder dúvidas sobre a LGPD citando o artigo correto, sem inventar | RAG, BM25, LSA, LLM (Claude), avaliação de busca | Artigo certo entre os 4 primeiros em 80% das perguntas novas |
| [Previsão de Churn de Clientes](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_16) | Identificar clientes de telecom com risco de cancelar | Pipeline, Regressão Logística, validação cruzada | AUC-ROC de 0,83 |
| [Previsão de Demanda de Táxis](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_13) | Prever pedidos da próxima hora para alocar motoristas | Séries temporais, validação temporal, Random Forest | RMSE de 44,58 (meta ≤ 48) |
| [Detecção de Resenhas Negativas](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_14) | Filtrar automaticamente resenhas negativas | NLP, TF-IDF, Regressão Logística | F1 de 0,88 (meta 0,85) e ROC AUC de 0,95 |
| [Estimativa de Idade por Imagem](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_15) | Apoiar a verificação de idade na venda de álcool | Visão computacional, ResNet50, transfer learning | MAE de 5,96 anos no teste; política identifica 89% dos menores |

## 🤖 Machine Learning

| Projeto | Problema de negócio | Técnicas | Resultado |
|---|---|---|---|
| [Recomendação de Plano de Telefonia](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_07) | Recomendar o plano certo para cada cliente | Classificação, GridSearchCV | 82% de acurácia (meta 75%) |
| [Saída de Clientes de um Banco](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_08) | Prever quais clientes vão deixar o banco | Classificação, balanceamento de classes | F1 de 0,60 (meta 0,59) e AUC-ROC de 0,85 |
| [Melhor Região para Poços de Petróleo](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_09) | Escolher a região com maior lucro e menor risco | Regressão, bootstrapping, análise de risco | Região recomendada com risco de 1,4% |
| [Recuperação de Ouro na Indústria](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_10) | Prever a recuperação de ouro no processo | Regressão, sMAPE | sMAPE de 7,84% |
| [ML e Proteção de Dados para Seguradora](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_11) | Proteger dados pessoais usados em modelos | kNN, álgebra linear, ofuscação de dados | kNN com F1 de 0,96; ofuscação sem perda de qualidade |
| [Valor de Mercado de Carros Usados](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_12) | Estimar o preço de carros em um aplicativo | XGBoost, LightGBM, comparação de modelos | RMSE de 2.701 com LightGBM |

## 📊 Análise de Dados e Estatística

| Projeto | Problema de negócio | Técnicas | Resultado |
|---|---|---|---|
| [Comportamento em Streaming de Música](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_01) | Comparar o comportamento de usuários de duas cidades | Pré-processamento, teste de hipóteses | 1 de 3 hipóteses confirmada |
| [Risco de Inadimplência](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_02) | Avaliar fatores de risco para o score de crédito | Análise exploratória, categorização | Taxas de 6,6% a 9,8% por perfil |
| [Preço de Carros Usados](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_03) | Entender o que determina o preço de um veículo | Análise exploratória, tratamento de outliers | Idade, quilometragem e condição |
| [Receita de Planos de Telefonia](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_04) | Definir qual plano gera mais receita | Estatística, testes de hipóteses | Ultimate: US$ 70 contra US$ 50 do Surf |
| [Padrões de Sucesso de Videogames](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_05) | Planejar a campanha de jogos de 2017 | Análise exploratória, correlação, testes | Correlação de 0,41 entre crítica e vendas |
| [Corridas de Táxi e Clima em Chicago](https://github.com/gabrieldeoliver1/Projetos/tree/main/Projeto_06) | Entender a demanda e o impacto do clima | Análise exploratória, teste de hipóteses | Clima altera a duração das corridas |

## 🛠️ Tecnologias

**Linguagens:** Python, SQL (SQLite)  
**Análise e visualização:** Pandas, NumPy, SciPy, Statsmodels, Matplotlib, Seaborn  
**Machine Learning:** Scikit-learn, XGBoost, LightGBM, NLTK, spaCy, TensorFlow, Keras

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_XX
jupyter notebook
```

Cada README traz as bibliotecas necessárias. Os conjuntos de dados dos projetos 1 a 16 foram fornecidos pela TripleTen e não estão incluídos no repositório; os dados dos projetos 17 em diante são públicos e estão na pasta de cada projeto.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
