# Previsão de Saída de Clientes de um Banco

> **Resultado:** **F1 de 0,60** no conjunto de teste, acima da meta de 0,59, com **AUC-ROC de 0,85**, usando Random Forest com upsampling da classe minoritária.

## Problema de negócio

Os clientes do Beta Bank estão saindo aos poucos, todo mês. Como é mais barato manter clientes do que conquistar novos, o banco quer prever quais clientes estão prestes a encerrar o relacionamento.

## Dados

- 10.000 clientes, com pontuação de crédito, país, gênero, idade, tempo de relacionamento, saldo, número de produtos, salário estimado e atividade
- Classes desbalanceadas: cerca de 20% dos clientes saíram do banco

## Abordagem

1. **Pré-processamento:** tratamento de valores ausentes, remoção de identificadores e codificação de país e gênero com one-hot encoding.
2. **Divisão dos dados:** 60% treino, 20% validação e 20% teste, com estratificação.
3. **Escolha do modelo pelo F1 na validação:** árvore de decisão e floresta aleatória com diferentes profundidades e números de árvores.
4. **Correção do desbalanceamento:** comparação entre pesos de classe, upsampling e downsampling, aplicados só no treino e avaliados na validação original.
5. **Ajuste do limiar de decisão** na validação.
6. **Avaliação final no teste**, usado uma única vez.

## Resultados

| Técnica (validação) | F1 | Recall | Precisão | AUC-ROC |
|---|---|---|---|---|
| Sem balanceamento | 0,56 | 0,43 | 0,78 | 0,85 |
| Pesos de classe | 0,60 | 0,54 | 0,67 | 0,85 |
| **Upsampling** | **0,62** | **0,63** | **0,60** | **0,86** |
| Downsampling | 0,59 | 0,75 | 0,48 | 0,86 |

Com o upsampling (o limiar padrão de 0,5 foi o melhor na validação), o modelo final alcançou no **teste**: **F1 de 0,60 (meta de 0,59)**, AUC-ROC de 0,85 e acurácia de 83%.

## Correções desta versão

Na versão anterior, as técnicas de balanceamento eram avaliadas nos próprios dados de treino reamostrados, o que inflava os resultados, o ajuste era feito pela acurácia e o modelo final era treinado no conjunto de validação, com apenas 2 mil clientes. O F1 no teste era de 0,56, abaixo da meta. Agora todas as escolhas são feitas pelo F1 na validação original, o modelo é treinado no conjunto de treino e o teste é usado uma única vez.

## Próximos passos

- Testar modelos de boosting, como LightGBM e CatBoost
- Definir o limiar de decisão com base no custo de cada tipo de erro

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_08
pip install pandas numpy scikit-learn jupyter
jupyter notebook
```

O conjunto de dados (`Churn.csv`) foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, coloque o arquivo na mesma pasta do notebook.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
