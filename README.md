# Projeto de Classificação de Diabetes com Keras

Este projeto visa a criação de uma rede neural simples para classificar se uma pessoa tem diabetes ou não, utilizando o conjunto de dados **Pima Indians Diabetes Dataset**. A tarefa é uma classificação binária (0 ou 1), onde 1 indica que a pessoa tem diabetes e 0 indica que a pessoa não tem.

## Objetivo

O objetivo é treinar um modelo de rede neural usando o Keras para prever se uma pessoa tem ou não diabetes com base em 8 variáveis de entrada. Essas variáveis são:

1. Número de vezes grávida.
2. Concentração de glicose plasmática após 2 horas em um teste oral de tolerância à glicose.
3. Pressão arterial diastólica (mm Hg).
4. Espessura da prega cutânea do tríceps (mm).
5. Insulina sérica em 2 horas (mu U/ml).
6. Índice de massa corporal (peso em kg / altura em m²).
7. Função pedigree para diabetes.
8. Idade (anos).

O modelo de rede neural será treinado com esses dados e, em seguida, será utilizado para prever se uma nova pessoa tem diabetes.

## Estrutura do Projeto

1. **Importação e Processamento dos Dados**  
   O conjunto de dados é carregado diretamente de uma URL e, em seguida, é dividido em variáveis de entrada (X) e saída (Y). Os dados são então normalizados usando a técnica de `StandardScaler` para melhorar a performance do modelo.

2. **Criação do Modelo de Rede Neural**  
   O modelo é criado usando a API sequencial do Keras. O modelo consiste em várias camadas densamente conectadas, com uma camada de saída que usa a função de ativação `sigmoid` para a classificação binária.

3. **Compilação e Treinamento do Modelo**  
   O modelo é compilado utilizando a função de perda `binary_crossentropy` e o otimizador `Adam` com uma taxa de aprendizado de 0.005. O modelo é treinado por 200 épocas com um tamanho de lote de 16.

4. **Avaliação do Modelo**  
   Após o treinamento, o modelo é avaliado no conjunto de dados de teste, e a precisão (`accuracy`) e a perda (`loss`) são exibidas.

5. **Predição de Novos Dados**  
   O modelo é utilizado para prever se uma nova pessoa tem diabetes, com base em um vetor de entrada simulado.

## Requisitos

- Python 3.x
- Keras
- TensorFlow
- scikit-learn
- NumPy
- Pandas

## Como Rodar o Projeto

1. Clone o repositório ou faça o download do arquivo `.ipynb`.
   
2. Execute o código no seu ambiente local ou no Google Colab.

3. O conjunto de dados será carregado automaticamente a partir da URL fornecida.

4. O modelo será treinado e as métricas de performance serão exibidas.

## Resultados
Após o treinamento do modelo, a acurácia e a perda do modelo são exibidas no terminal. O modelo também faz uma previsão sobre se uma nova pessoa tem diabetes com base nas variáveis fornecidas.

## Possíveis Melhorias
Ajustar a arquitetura da rede neural (ex.: adicionar mais camadas ou neurônios).

Experimentar diferentes funções de ativação e técnicas de regularização (como dropout).

Usar técnicas de validação cruzada para avaliar melhor o modelo.

Ajustar os hiperparâmetros do modelo, como a taxa de aprendizado e o número de épocas.

## Conclusão
Este projeto demonstrou como construir uma rede neural simples usando Keras para classificar a presença de diabetes com base em variáveis médicas. Existem várias maneiras de melhorar a performance do modelo, como ajustar sua arquitetura e otimizar os parâmetros de treinamento.
