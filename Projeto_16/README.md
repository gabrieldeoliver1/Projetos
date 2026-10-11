# Previsão de Churn de Clientes – Interconnect

> **Resultado:** **AUC-ROC de 0,82** no conjunto de teste (0,83 na validação cruzada), com um pipeline completo de pré-processamento e Regressão Logística.

## Problema de negócio

A operadora de telecomunicações Interconnect quer prever quais clientes estão propensos a cancelar o contrato. Com essa previsão, a equipe de marketing pode oferecer códigos promocionais e planos especiais aos clientes certos, antes que eles saiam.

## Dados

- 7.043 clientes
- Quatro tabelas unidas pelo `customerID`: contratos, serviços de internet, dados pessoais e serviços de telefonia
- Variável-alvo derivada da data de encerramento do contrato: no notebook, o valor 1 indica clientes que permaneceram, e a probabilidade de churn é obtida como `1 - p` (o AUC-ROC não muda com essa convenção)

## Abordagem

1. **Integração e análise exploratória:** união das quatro tabelas, verificação de qualidade, tratamento de valores ausentes e de inconsistências.
2. **Prevenção de vazamento de dados:** separação entre treino (90%) e teste (10%) antes de qualquer transformação, com estratificação pela variável-alvo, e remoção das colunas de data que revelariam o resultado.
3. **Pipeline de pré-processamento:** imputação de valores ausentes, `OneHotEncoder` nas variáveis categóricas e `StandardScaler` nas numéricas, tudo encapsulado com `ColumnTransformer` e `Pipeline`.
4. **Modelagem e validação:** Regressão Logística avaliada com validação cruzada de 5 folds e, depois, no conjunto de teste.

## Resultados

| Avaliação | AUC-ROC |
|---|---|
| Validação cruzada (5 folds) | 0,83 |
| **Conjunto de teste** | **0,82** |

Os resultados próximos entre validação cruzada e teste indicam que o modelo generaliza bem para clientes novos. Como a solução está encapsulada em um único pipeline, ela pode ser aplicada diretamente a novos dados.

## Próximos passos

- Redefinir o alvo como 1 para clientes que cancelaram, seguindo a convenção usual de problemas de churn
- Testar modelos de boosting (LightGBM, CatBoost) e comparar com a Regressão Logística
- Criar uma feature de tempo de contrato a partir da data de início e de uma data de referência, sem usar informação do encerramento
- Definir um limiar de decisão com base no custo das ações de retenção

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · Matplotlib · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_16
pip install pandas numpy scikit-learn matplotlib jupyter
jupyter notebook
```

Os conjuntos de dados foram fornecidos pela TripleTen durante o bootcamp e não estão incluídos no repositório. O relatório da solução está no notebook `modelo_para_predizer_a_rotatividade_relatorio_solucao.ipynb`.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
