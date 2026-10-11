# Estimativa de Idade por Imagem para Evitar a Venda de Álcool a Menores

> **Resultado:** erro absoluto médio (MAE) de **5,79 anos** no conjunto de validação, com transfer learning sobre a ResNet50.

## Problema de negócio

Estabelecimentos comerciais precisam verificar a idade dos clientes na venda de bebidas alcoólicas. A proposta é um modelo de visão computacional que estime a idade de uma pessoa a partir de uma foto do rosto, apoiando essa verificação no momento da compra.

## Dados

- 7.591 fotos de rostos, cada uma rotulada com a idade real da pessoa
- Idades de 1 a 100 anos, com média de 31 e mediana de 29 anos
- Divisão de 75% para treino e 25% para validação

## Abordagem

1. **Análise exploratória:** distribuição das idades e inspeção visual de amostras das imagens.
2. **Preparação das imagens:** normalização dos pixels e aumento de dados com espelhamento horizontal no treino, usando `ImageDataGenerator`.
3. **Modelagem:** transfer learning com a ResNet50 pré-treinada no ImageNet, seguida de `GlobalAveragePooling2D` e camada densa para a regressão da idade.
4. **Treinamento:** otimizador Adam (taxa de aprendizado de 0,0001), função de perda MAE e 30 épocas em GPU.

## Resultados

| Conjunto | MAE |
|---|---|
| Treino | 2,09 anos |
| **Validação** | **5,79 anos** |

Na prática, um erro médio de cerca de 6 anos não permite que o modelo decida sozinho se uma pessoa é maior de idade. Ele funciona melhor como ferramenta de apoio: quando a idade estimada estiver abaixo de uma margem de segurança (por exemplo, 25 anos), o sistema sinaliza ao caixa que peça um documento.

## Próximos passos

- Ajustar a camada de saída para `Dense(1)`, a forma mais adequada para prever um único valor, e validar o resultado em nova execução
- Reduzir a diferença entre o erro de treino e o de validação com mais aumento de dados, regularização e dropout
- Avaliar o erro especificamente na faixa de 15 a 25 anos, a mais importante para este problema

## Tecnologias

Python · TensorFlow · Keras · ResNet50 · Pandas · Matplotlib · Jupyter Notebook

## Como executar

```bash
git clone https://github.com/gabrieldeoliver1/Projetos.git
cd Projetos/Projeto_15
pip install tensorflow pandas matplotlib jupyter
jupyter notebook
```

O conjunto de imagens foi fornecido pela TripleTen durante o bootcamp e não está incluído no repositório. O treinamento foi executado em GPU, e o registro completo das épocas está no notebook.

## 🔗 Contato

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabrieldeoliver1/)

Email: gabrieldeoliver1@gmail.com
