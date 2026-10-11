# Recomendação de Plano de Telefonia com Classificação

> **Resultado:** **82% de acurácia** no conjunto de teste com Random Forest, acima da meta de 75%.

## Problema de negócio

A operadora Megaline quer um modelo que analise o comportamento dos clientes e recomende um dos seus planos mais recentes: Smart ou Ultra.

## Dados

- 3.214 clientes, com número de chamadas, minutos, mensagens e uso de internet por mês
- Variável-alvo: plano do cliente (69% Smart e 31% Ultra)

## Abordagem

1. **Divisão dos dados:** 60% treino, 20% validação e 20% teste.
2. **Modelagem:** comparação entre Árvore de Decisão, Random Forest e Regressão Logística.
3. **Ajuste de hiperparâmetros:** `GridSearchCV` com validação cruzada de 5 folds para cada modelo.
4. **Avaliação final:** aplicação do melhor modelo no conjunto de teste.

## Resultados

| Modelo | Acurácia (validação cruzada) |
|---|---|
| **Random Forest** | **0,80** |
| Árvore de Decisão | 0,79 |
| Regressão Logística | 0,75 |

No conjunto de validação, o Random Forest também foi o melhor (0,82), contra 0,69 de um modelo que sempre recomendasse o plano Smart. No **teste**, alcançou **0,82 de acurácia**.

## Correções desta versão

A divisão dos dados passou a ter semente fixa e estratificação, as células que exibiam os parâmetros de outro modelo foram corrigidas, combinações de hiperparâmetros inválidas foram removidas e o modelo final passou a ser escolhido no conjunto de validação, com um teste de sanidade contra o modelo ingênuo.

## Próximos passos

- Avaliar também precisão e recall da classe Ultra, já que as classes são desbalanceadas
- Analisar a importância das variáveis para explicar as recomendações ao time comercial

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_07
pip install pandas numpy scikit-learn jupyter
jupyter notebook
```

O conjunto de dados (`users_behavior.csv`) foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, coloque o arquivo na mesma pasta do notebook.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
