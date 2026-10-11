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
| **Random Forest** | **0,81** |
| Árvore de Decisão | 0,79 |
| Regressão Logística | 0,74 |

O Random Forest foi o modelo escolhido e alcançou **0,82 de acurácia no teste**. Como referência, um modelo que sempre recomendasse o plano Smart acertaria cerca de 69%.

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

O conjunto de dados foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, ajuste o caminho do arquivo na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
