# Detecção de Fraude em Cartão de Crédito

## Título e Objetivo
**Título:** Detecção de Fraude em Cartão de Crédito
**Objetivo:** Desenvolver um modelo de Inteligência Artificial capaz de detectar se uma transação de cartão de crédito é legítima ou fraudulenta.

## Integrantes
- Osanyo Victor Bevitori Nascimento - @osanyovictor
- Raíssa Cavalcante de Albuquerque Bitencurte - @raissabac
- Filipe Ciríaco Marcelino do Nascimento - @VilefilipeDCOMP

## Fonte dos Dados
Os dados utilizados neste projeto são provenientes do Kaggle, especificamente do dataset "Credit Card Fraud Detection" (mlg-ulb/creditcardfraud). Este dataset contém transações realizadas por cartões de crédito em setembro de 2013 por portadores europeus, caracterizado por ser um conjunto de dados altamente desbalanceado.

## Tipo da Tarefa
Trata-se de uma tarefa de Classificação Binária, onde o objetivo é classificar cada transação em uma de duas classes:
- 0: Transação legítima (Normal)
- 1: Transação fraudulenta (Fraude)

## Organização dos Arquivos
O repositório está organizado da seguinte forma:
- `main.ipynb`: Notebook Jupyter contendo todo o código do projeto, incluindo pré-processamento, análise exploratória, treinamento, otimização e avaliação dos modelos.
- `README.md`: Este arquivo com a descrição e detalhes gerais do projeto.

## Instruções para abrir o notebook no Colab
1. Acesse o [Google Colaboratory](https://colab.research.google.com/).
2. Na tela inicial, selecione a aba "Upload" (ou acesse Arquivo > Fazer upload de notebook).
3. Faça o upload do arquivo `main.ipynb` do seu computador, ou selecione a aba "GitHub" e cole a URL do repositório.
4. Uma vez aberto, você poderá executar as células sequencialmente. O próprio notebook faz a instalação das dependências (kagglehub, etc) e o download do dataset na primeira célula.

## Modelos Utilizados
Os seguintes modelos de Machine Learning foram treinados e avaliados:
- **DummyClassifier**: Modelo base (baseline) configurado com a estratégia "most_frequent" (prevê sempre a classe majoritária), utilizado para referenciar o efeito do desbalanceamento das classes.
- **SGDClassifier**: Classificador linear otimizado via Gradiente Descendente Estocástico (Stochastic Gradient Descent).
- **RandomForestClassifier**: Modelo de aprendizado em conjunto (ensemble) baseado na construção de múltiplas árvores de decisão.

Para a sintonia fina, utilizou-se a técnica GridSearchCV avaliando hiperparâmetros por meio de validação cruzada estratificada e focando na métrica de Average Precision.

## Principais Resultados
O modelo com melhor performance foi o **RandomForestClassifier** após otimização de hiperparâmetros (n_estimators=150, max_features='log2', max_depth=None, class_weight='balanced').

Ele atingiu uma Média de Precisão (Average Precision) de aproximadamente 0.80 no conjunto de teste, o que supera de forma significativa os demais classificadores avaliados (0.51 para o SGDClassifier e 0.0017 para o DummyClassifier). O modelo obteve Revocação (Recall) próxima de 0.79. Na validação do conjunto de testes os resultados absolutos foram:
- Verdadeiros Positivos (Fraudes detectadas corretamente): 75
- Verdadeiros Negativos (Transações legítimas corretas): 56.648
- Falsos Positivos (Legítimas marcadas como fraude): 3
- Falsos Negativos (Fraudes que passaram despercebidas): 20

## Link do Vídeo
[Link]

## Divisão das Contribuições
- **Osanyo Victor Bevitori Nascimento**: Identificação e descrição do problema, compreensão dos dados e análise exploratória.
- **Raíssa Cavalcante de Albuquerque Bitencurte**: Pré-processamento e separação dos dados (treino e teste).
- **Filipe Ciríaco Marcelino do Nascimento**: Modelagem (Baseline e Classificadores), avaliação com métricas de desempenho e discussão de resultados.

## Declaração de Uso de Ferramentas de Inteligência Artificial
Declaramos que ferramentas de Inteligência Artificial (como Claude e Gemini) foram utilizadas exclusivamente para auxílio na revisão de estilo e formatação da documentação deste repositório (`README.md`), além do refinamento de alguns textos explicativos no notebook (`main.ipynb`).

A concepção, a lógica e a implementação de todos os scripts e códigos que compõem este projeto são de autoria própria e integral dos membros do grupo.