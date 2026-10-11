# Previsão de Saída de Clientes de um Banco

> **Resultado:** F1 de **0,56** para a classe de clientes que saem e **AUC-ROC de 0,86** na validação, com Random Forest e técnicas de balanceamento de classes. A meta do projeto era F1 de 0,59.

## Problema de negócio

Os clientes do Beta Bank estão saindo aos poucos, todo mês. Como é mais barato manter clientes do que conquistar novos, o banco quer prever quais clientes estão prestes a encerrar o relacionamento.

## Dados

- 10.000 clientes, com pontuação de crédito, país, gênero, idade, tempo de relacionamento, saldo, número de produtos, salário estimado e atividade
- Classes desbalanceadas: cerca de 20% dos clientes saíram do banco

## Abordagem

1. **Pré-processamento:** tratamento de valores ausentes, remoção de identificadores e codificação de variáveis categóricas (país e gênero) com one-hot encoding.
2. **Divisão dos dados:** 60% treino, 20% validação e 20% teste, com estratificação.
3. **Modelo sem balanceamento:** ajuste da profundidade da árvore e do número de árvores do Random Forest.
4. **Correção do desbalanceamento:** comparação entre upsampling e downsampling da classe minoritária, combinados com pesos de classe.
5. **Avaliação final:** F1, acurácia e AUC-ROC.

## Resultados

| Avaliação | Resultado |
|---|---|
| F1 sem balanceamento (validação) | 0,53 |
| AUC-ROC (validação) | 0,86 |
| **F1 no teste (classe de clientes que saem)** | **0,56** |
| Acurácia no teste | 81,5% |

Com o balanceamento de classes, o recall da classe de clientes que saem passou de 0,39 (validação, sem balanceamento) para 0,57 (teste), ao custo de uma pequena queda na acurácia. O F1 final ficou próximo, mas abaixo, da meta de 0,59.

## Próximos passos

- Ajustar os hiperparâmetros com base no F1, em vez da acurácia, e aumentar o número de árvores do modelo (hoje são 10)
- Otimizar o limiar de decisão para maximizar o F1
- Testar modelos de boosting, como LightGBM e CatBoost

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_08
pip install pandas numpy scikit-learn jupyter
jupyter notebook
```

O conjunto de dados foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, ajuste o caminho do arquivo na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
