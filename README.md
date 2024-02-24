# Google-Stock-Price-Prediction

## Introdução
Este projeto visa prever os preços das ações da Google utilizando uma Rede Neural Recorrente (RNN) implementada com a biblioteca Keras sobre o TensorFlow. O conjunto de dados de treinamento abrange o período de 2012 a 2016, enquanto o conjunto de teste contém resultados de janeiro de 2017.

## Descrição do Projeto

O objetivo principal é criar um modelo capaz de aprender padrões nos dados históricos das ações da Google e fazer previsões sobre os preços futuros. Utilizou-se uma abordagem de Aprendizado de Máquina Supervisionado, especificamente uma RNN com camadas LSTM (Long Short-Term Memory).

## Preparação do Conjunto de Dados

Antes do treinamento, foram realizadas etapas de pré-processamento nos dados. O conjunto de treinamento é carregado a partir de um arquivo CSV contendo informações históricas de preços das ações. Os dados são escalonados para uma faixa entre 0 e 1 usando o MinMaxScaler do scikit-learn. Em seguida, criamos sequências temporais de 60 dias como entrada para a rede neural, com o objetivo de capturar padrões de curto prazo.

## Construção da Rede Neural Recorrente

A arquitetura da RNN é construída com a biblioteca Keras. Optamos por uma estrutura de várias camadas LSTM empilhadas para aprender padrões temporais complexos nos dados. Cada camada LSTM é seguida por uma camada de Dropout para evitar overfitting. A última camada é uma camada densa que gera a saída da previsão.

## Treinamento e Avaliação

O modelo é compilado com o otimizador Adam e a função de perda mean squared error (erro quadrático médio). É então treinado com o conjunto de dados de treinamento, utilizando 100 épocas e um tamanho de lote de 32. A eficácia do modelo é avaliada com o conjunto de dados de teste.

## Fazendo Previsões e Visualizando Resultados

Após o treinamento, o modelo é utilizado para fazer previsões sobre os preços das ações em 2017. Os resultados previstos são invertidos para a escala original e comparados com os preços reais. A visualização gráfica utilizando Matplotlib permite uma análise fácil e intuitiva do desempenho do modelo.

![Resultados de Previsão de Ações da Google](https://cdn.discordapp.com/attachments/1184622679685333042/1210763590311870464/download.png?ex=65ebbe76&is=65d94976&hm=94edecbe2d8e58648a584db9207bac242d9ab3a75e8f4a2f1940aa8109ac676c&)
## Dependências

Certifique-se de ter as seguintes bibliotecas instaladas:

- Numpy: `pip install numpy`
- Matplotlib: `pip install matplotlib`
- Pandas: `pip install pandas`
- Scikit-learn: `pip install scikit-learn`
- TensorFlow: `pip install tensorflow`

## Contribuindo

Contribuições são bem-vindas! Se você encontrar problemas ou tiver sugestões, sinta-se à vontade para abrir uma issue ou enviar um pull request.

Agradeço pelo seu interesse e contribuição!
