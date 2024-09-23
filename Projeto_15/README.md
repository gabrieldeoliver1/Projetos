
# Garantindo que não Vendam Álcool para Menores de Idade

## Descrição do Projeto
Este projeto desenvolve um modelo de aprendizado de máquina utilizando processamento de imagens para garantir que estabelecimentos comerciais não vendam álcool para menores de idade. O modelo é treinado para estimar a idade de uma pessoa com base em uma imagem facial, utilizando técnicas avançadas de deep learning.

## Tecnologias Utilizadas
- **Python**: Linguagem principal para desenvolvimento do projeto.
- **TensorFlow**: Biblioteca usada para construir e treinar o modelo de deep learning.
- **Keras**: API de alto nível usada para construir redes neurais.
- **Pandas**: Manipulação e análise de dados.
- **Matplotlib**: Visualização de dados e gráficos.

### Bibliotecas Utilizadas:
- **ResNet50**: Modelo de rede neural convolucional pré-treinado usado para extração de características das imagens.
- **ImageDataGenerator**: Utilizado para a geração e pré-processamento de imagens.
- **Adam**: Otimizador utilizado para ajustar os pesos da rede neural.
- **GlobalAveragePooling2D**: Operação de pooling para reduzir a dimensionalidade da saída da rede convolucional.

## Funcionalidades Implementadas

1. **Carregamento e Preparação dos Dados**:
   - Os dados consistem em um conjunto de imagens faciais armazenadas no diretório `/datasets/faces/`, com rótulos de idades armazenados no arquivo `labels.csv`.

2. **Exploração de Dados (EDA)**:
   - Análise da distribuição etária e visualização de dados, com gráficos de barras mostrando as idades mais comuns no conjunto de dados.
   - Verificações para garantir que os dados estão prontos para a modelagem.

3. **Divisão dos Dados**:
   - O conjunto de dados foi dividido em treinamento e validação usando o `ImageDataGenerator`, que também realiza augmentação de dados, como flips horizontais e normalização das imagens.

4. **Modelagem**:
   - Implementação do modelo usando a rede **ResNet50** pré-treinada, com camadas adicionais de pooling e densas para prever a idade.
   - O modelo foi compilado com a função de perda **mean_absolute_error** para medir a precisão das previsões.
   
5. **Treinamento do Modelo**:
   - O modelo foi treinado por 30 épocas com um conjunto de treinamento e validação, utilizando a GPU para acelerar o processo.

6. **Resultados**:
   - O modelo alcançou um erro absoluto médio (**MAE**) de 5.7889 ao prever as idades das imagens de teste.

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
