# Classificação de Preços de Motocicletas com Machine Learning

## Sobre o projeto

Este projeto tem como objetivo desenvolver uma esteira de aprendizado de máquina (*Machine Learning Pipeline*) para classificar motocicletas usadas em três categorias de preço: **Econômica, Intermediária e Premium**.

O desenvolvimento contempla desde a análise exploratória e preparação dos dados até o treinamento, avaliação e realização de previsões utilizando algoritmos de classificação.

## Dataset

Foi utilizado o conjunto de dados [Motorcycle Dataset](https://www.kaggle.com/datasets/nehalbirla/motorcycle-dataset), disponibilizado no Kaggle.

A base contém informações sobre motocicletas usadas, incluindo:

- Modelo da motocicleta;
- Ano de fabricação;
- Tipo de vendedor;
- Quantidade de proprietários anteriores;
- Quilometragem;
- Preço de referência (ex-showroom);
- Preço de venda.

Após a remoção de 6 registros duplicados, foram utilizados **1.055 registros**.

## Tecnologias e bibliotecas

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- KaggleHub
- Jupyter Notebook

## Etapas do projeto

1. **Análise exploratória:** inspeção dos dados, estatísticas descritivas, valores ausentes, duplicados e correlações.
2. **Limpeza e transformação:** remoção de registros duplicados, tratamento de valores ausentes e preparação das variáveis.
3. **Criação das categorias:** transformação do preço de venda em três classes, utilizando os tercis calculados sobre os dados de treinamento.
4. **Divisão dos dados:** separação em treinamento (70%), validação (15%) e teste (15%).
5. **Pré-processamento:** utilização de imputação de valores ausentes, codificação de variáveis categóricas e organização das transformações com Pipeline e ColumnTransformer.
6. **Treinamento:** implementação e comparação dos algoritmos Árvore de Decisão e Random Forest.
7. **Avaliação:** análise da acurácia, relatório de classificação e matriz de confusão.
8. **Predição:** realização de uma classificação individual para uma motocicleta.

## Modelos utilizados

Foram implementados dois algoritmos:

- **Decision Tree (Árvore de Decisão):** utilizado como modelo de comparação.
- **Random Forest:** selecionado por apresentar o melhor resultado na validação.

## Resultados

| Modelo | Acurácia na validação |
|---|---:|
| Árvore de Decisão | 73,42% |
| Random Forest | 74,68% |

O Random Forest foi selecionado para a avaliação final.

**Resultado no conjunto de teste:**

- Acurácia: **78,62%**
- Registros avaliados: 159
- Classificações corretas: 125
- Classificações incorretas: 34
- F1-score ponderado: 79%

A categoria Premium apresentou o melhor F1-score (86%), enquanto a categoria Intermediária apresentou maior dificuldade de classificação (74%).

## Como executar

1. Clone ou baixe este repositório.
2. Instale as bibliotecas necessárias.
3. Abra o arquivo `classificacao_precos_motocicletas.ipynb` no Jupyter Notebook ou JupyterLab.
4. Execute as células sequencialmente.

O notebook realiza o download do dataset por meio do KaggleHub. É necessário ter acesso à internet e configurar a autenticação do Kaggle conforme necessário.

## Limitações e melhorias futuras

O modelo apresentou resultados satisfatórios, mas ainda existem oportunidades de melhoria:

- Avaliar outros algoritmos de classificação;
- Realizar ajuste de hiperparâmetros;
- Investigar o impacto de valores extremos;
- Melhorar a representação das variáveis categóricas;
- Avaliar novas técnicas de engenharia de atributos.

## Autor

Desenvolvido como projeto acadêmico na área de Análise e Desenvolvimento de Sistemas, com foco em análise de dados e aprendizado de máquina.
