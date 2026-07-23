# Checklist — Seção 5 (Notebook) do Projeto Final

## Pessoa 1
### 5.1 Identificação e descrição do problema
- [X] Título do projeto
- [X] Integrantes do grupo
- [X] Fonte dos dados
- [X] Objetivo da aplicação
- [X] Atributo-alvo definido
- [X] Atributos preditivos listados
- [X] Tipo da tarefa definido (classificação ou regressão)

### 5.2 Compreensão dos dados
- [X] Quantidade de registros e atributos apresentada
- [X] Tipos das variáveis descritos
- [X] Valores ausentes identificados
- [X] Duplicações verificadas
- [X] Inconsistências identificadas
- [X] Distribuição do atributo-alvo apresentada
- [X] Desbalanceamento avaliado (quando houver)
- [ ] Todas as informações **interpretadas** (não só `head()`, `info()`, `describe()`)

### 5.3 Análise exploratória
- [ ] Histogramas (quando pertinente)
- [ ] Boxplots (quando pertinente)
- [ ] Gráficos de dispersão (quando pertinente)
- [ ] Tabelas de frequência (quando pertinente)
- [ ] Medidas de localidade e dispersão
- [X] Correlações entre atributos
- [ ] Relações entre atributos e o alvo
- [ ] Cada figura/tabela acompanhada de explicação/interpretação

## Pessoa 2
### 5.4 Pré-processamento
- [X] Tratamento de valores ausentes (justificado)
- [X] Tratamento de variáveis categóricas (justificado)
- [X] Escalonamento (justificado)
- [X] Tratamento de valores extremos (justificado)
- [X] Remoção de atributos irrelevantes (justificado)
- [X] Remoção de duplicações (justificado)
- [X] Correção de inconsistências (justificado)
- [X] Tratamento de classes desbalanceadas (justificado, se aplicável)
- [X] Para cada tratamento: problema encontrado → tratamento aplicado → por que foi escolhido
- [X] Verificar que não há vazamento de informação entre treino e teste

### 5.5 Separação dos dados
- [X] Separação treino/teste realizada
- [X] Proporção utilizada justificada
- [X] Estratificação aplicada (quando necessária)
- [X] Conjunto de teste reservado apenas para avaliação final

## Filipe
### 5.6 Modelagem
- [X] Baseline definido
- [X] Modelos mínimos exigidos utilizados:
  - [X] **Classificação:** DummyClassifier, SGDClassifier, RandomForestClassifier
- [X] Parâmetros principais de cada modelo apresentados
- [X] Comparação entre os resultados dos modelos
- [X] Validação adequada usada na comparação dos modelos (ex.: validação cruzada)
- [X] Justificativa para escolha do modelo final
- [X] Explicar o que é o average precision e pq usamos

### 5.7 Avaliação e discussão
- [X] Métricas adequadas calculadas:
  - [X] **Classificação:** matriz de confusão, acurácia, precisão, revocação, F1-score
- [X] Discussão: qual modelo teve melhor resultado
- [X] Discussão: por que esse modelo foi escolhido
- [X] Discussão: quais erros foram observados
- [X] Discussão: quais limitações existem
- [X] Discussão: o que poderia ser melhorado