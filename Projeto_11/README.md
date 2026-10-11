# Machine Learning e Proteção de Dados para uma Seguradora

> **Resultado:** classificador kNN com **F1 de até 0,96** para prever se um cliente receberá pagamento do seguro (contra 0,20 de um modelo aleatório) e ofuscação de dados pessoais com matriz invertível que **mantém exatamente a qualidade do modelo**.

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

| Tarefa | Resultado |
|---|---|
| Classificação com kNN (dados escalados) | **F1 de até 0,96** (k = 1) |
| Classificação com kNN (dados originais) | F1 de 0,58 ou menos |
| Melhor linha de base aleatória | F1 de 0,20 |
| Regressão Linear própria (número de pagamentos) | REQM de 0,34 e R² de 0,43 |
| Regressão Linear com dados ofuscados | **REQM de 0,34 e R² de 0,43**, com as mesmas previsões |

- **O escalonamento é decisivo para o kNN:** sem ele, a renda, com valores na casa das dezenas de milhares, domina a distância entre os clientes.
- **A ofuscação protege sem custo:** idade, renda e família ficam ilegíveis, e o modelo treinado com os dados ofuscados faz exatamente as mesmas previsões. É uma aplicação direta de princípios de proteção de dados, como os da LGPD.

## Correções desta versão

Uma revisão do notebook encontrou e corrigiu cinco problemas: o alvo da classificação passou a ser binário sem alterar o número de pagamentos usado na regressão; o classificador kNN, que faltava, foi treinado; o R² passou a ser exibido corretamente (antes aparecia a raiz quadrada); o modelo deixou de ser ajustado novamente no conjunto de teste; e o teste de ofuscação passou a usar de fato os dados ofuscados.

## Tecnologias

Python · Pandas · NumPy · Scikit-learn · Álgebra Linear · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_11
pip install pandas numpy scikit-learn seaborn jupyter
jupyter notebook
```

O conjunto de dados (`insurance_us.csv`) foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. Para reproduzir o projeto, coloque o arquivo na mesma pasta do notebook.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
