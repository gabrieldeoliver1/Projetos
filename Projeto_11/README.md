# Machine Learning e Proteção de Dados para uma Seguradora

> **Resultado:** ofuscação de dados pessoais de clientes com uma matriz invertível: os dados ficam ilegíveis após a transformação e são recuperados integralmente com a matriz inversa.

## Problema de negócio

A seguradora Proteja Seu Amanhã quer avaliar como o aprendizado de máquina pode ajudar em quatro tarefas: encontrar clientes semelhantes para ações de marketing, prever se um cliente vai receber um pagamento de seguro, prever quantos pagamentos ele vai receber e proteger os dados pessoais dos clientes sem prejudicar os modelos.

## Dados

- 5.000 clientes, com gênero, idade, salário, número de membros da família e número de pagamentos de seguro recebidos

## Abordagem

1. **Clientes semelhantes (kNN):** busca de vizinhos mais próximos com distâncias euclidiana e de Manhattan, comparando dados com e sem escalonamento.
2. **Classificação:** construção de linhas de base com modelos aleatórios para a previsão de recebimento de pagamento.
3. **Regressão:** implementação própria de Regressão Linear a partir da formulação em álgebra linear (equação normal), para prever o número de pagamentos.
4. **Ofuscação de dados:** multiplicação das características pessoais por uma matriz aleatória invertível, verificação da inversibilidade e recuperação dos dados originais com a matriz inversa.

## Resultados

- **Ofuscação:** após a transformação, idade, gênero, salário e tamanho da família deixam de ser legíveis; com a matriz inversa, os valores originais são recuperados, com diferenças apenas na ordem de 10⁻¹² (arredondamento numérico).
- **Regressão Linear própria:** RMSE de 0,23 na previsão do número de pagamentos.
- **Classificação:** a melhor linha de base aleatória obteve F1 de 0,20.

A ofuscação com matriz invertível é uma aplicação direta de princípios de proteção de dados, como os da LGPD: os dados podem ser compartilhados para modelagem sem expor as informações pessoais dos clientes.

## Observações técnicas

Na revisão do notebook, identifiquei pontos na tarefa de regressão que estão documentados no próprio notebook:

- A função de avaliação reporta a raiz quadrada do R² (o valor exibido de 0,66 corresponde a um R² de cerca de 0,44).
- O modelo foi ajustado novamente no conjunto de teste antes da avaliação.
- O teste da regressão com dados ofuscados usou os dados originais, então a comparação empírica entre dados originais e ofuscados ainda precisa ser executada. Pela teoria, as previsões da Regressão Linear não mudam quando as características são multiplicadas por uma matriz invertível, e é esse o resultado esperado na nova execução.

## Próximos passos

- Executar a regressão com os dados ofuscados e comparar as previsões e as métricas com as dos dados originais
- Ajustar o modelo apenas no conjunto de treino e reportar o R² sem a raiz quadrada
- Treinar o classificador kNN e compará-lo com as linhas de base aleatórias

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · Álgebra Linear · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_11
pip install pandas numpy scikit-learn seaborn jupyter
jupyter notebook
```

O conjunto de dados foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, ajuste o caminho do arquivo na célula de leitura dos dados.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
