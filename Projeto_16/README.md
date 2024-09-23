# Desenvolvendo um Modelo para Predizer a Rotatividade

## Descrição do Projeto
Este projeto visa desenvolver um modelo preditivo de aprendizado de máquina para a operadora de comunicações Interconnect, com o objetivo de prever a rotatividade de clientes. O modelo utiliza dados pessoais e de contratos coletados pela equipe de marketing para identificar usuários que estão propensos a trocar de operadora. Quando um cliente é identificado como potencialmente propenso à rotatividade, a empresa pode intervir com ofertas especiais, como códigos promocionais e opções de planos personalizados.

## Tecnologias Utilizadas
- **Python**: Linguagem principal para desenvolvimento do projeto.
- **Pandas**: Manipulação e análise de dados.
- **NumPy**: Operações numéricas e manipulação de arrays.
- **Matplotlib**: Visualização de dados e gráficos.
- **Scikit-learn**: Biblioteca para modelagem e validação de modelos de aprendizado de máquina.

## Bibliotecas Utilizadas
- **LogisticRegression**: Modelo de regressão logística utilizado para classificação.
- **Pipeline**: Ferramenta para encadear transformações e o modelo em um único objeto.
- **ColumnTransformer**: Utilizado para aplicar diferentes pré-processamentos a colunas específicas.
- **OneHotEncoder**: Codificação de variáveis categóricas em formato binário.
- **SimpleImputer**: Preenchimento de valores ausentes.

## Funcionalidades Implementadas

### Carregamento e Preparação dos Dados
- Os dados foram carregados a partir de quatro arquivos CSV, contendo informações sobre contratos, serviços de internet, dados pessoais e informações de telefone dos clientes.
- Os DataFrames foram unidos com base no `customerID` para criar um conjunto de dados consolidado que inclui todas as variáveis relevantes para a análise.

### Exploração de Dados (EDA)
- Realizada uma análise descritiva inicial para entender a distribuição dos dados.
- Gráficos foram gerados para visualizar a distribuição da variável alvo (`target`), representando a rotatividade (0 = não rotativo, 1 = rotativo).
- Identificação e tratamento de valores ausentes e outliers, com uma abordagem para garantir que todos os dados estivessem prontos para modelagem.

### Pré-processamento dos Dados
- Colunas não relevantes foram excluídas para otimizar o modelo.
- As colunas categóricas foram convertidas em variáveis dummy usando `OneHotEncoder`.
- Valores ausentes foram preenchidos, garantindo que não houvesse dados faltantes durante o treinamento.

### Divisão dos Dados
- O conjunto de dados foi dividido em conjuntos de treinamento (90%) e teste (10%), utilizando `train_test_split` para garantir uma amostragem estratificada da variável alvo.

### Modelagem
- Um pipeline foi criado para integrar pré-processamento e modelagem, utilizando regressão logística.
- O modelo foi avaliado utilizando validação cruzada para garantir que fosse capaz de generalizar bem para novos dados.
- As métricas de desempenho foram avaliadas com foco na pontuação AUROC (Area Under the Receiver Operating Characteristic Curve), que fornece uma medida robusta de desempenho para problemas de classificação desbalanceada.

### Resultados
- O modelo alcançou uma média de 0.82 na pontuação AUROC no conjunto de teste, indicando uma boa capacidade de discriminação entre clientes rotativos e não rotativos.
- A solução final foi encapsulada em um pipeline que pode ser facilmente aplicado a novos dados para prever a rotatividade dos clientes.

## Relatório da Solução
No final do Jupyter Notebook, foi elaborado um relatório com a solução, que será revisado pelo líder da equipe. As etapas foram executadas rigorosamente, sem qualquer omissão. O plano incluiu:

1. **Exclusão e preenchimento de colunas**: Melhorando a avaliação do modelo.
2. **Garantia contra vazamento de dados**: Separação de conjuntos de teste e treinamento.
3. **Validação cruzada**: Para estimar a generalização do modelo.
4. **Treinamento e teste do modelo**: Avaliação em dados reais.

## Dificuldades Encontradas
A maior dificuldade foi a implementação da validação cruzada, uma técnica que, apesar de complexa, é crucial para obter uma estimativa confiável do desempenho do modelo.

## Conclusão
O modelo final, representado pelo pipeline com regressão logística, é uma solução robusta para prever a rotatividade de clientes. A pontuação AUROC de 0.82 indica que o modelo é eficaz e pode ser utilizado para guiar intervenções da equipe de marketing, melhorando a retenção de clientes na Interconnect.

## Clone

Como Executar o Projeto Clone o repositório:

```bash
  Copiar git clone https://github.com/gabrieldeoliver1/Projetos.git Navegue até o diretório do projeto:
```

```bash
  Copiar cd Projeto_15 Abra o notebook:
```




## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com

