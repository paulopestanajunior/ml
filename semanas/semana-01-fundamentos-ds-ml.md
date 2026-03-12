# Semana 1 — Fundamentos de Data Science e Aprendizado de Máquina

Nesta primeira semana você revisitará o processo de **Data Science**, os tipos de tarefas de mineração de dados e as categorias de aprendizado de máquina. O objetivo é entender como transformar um problema de negócio em um problema de modelagem, conhecer as etapas essenciais (entendimento do negócio, preparação de dados, modelagem, avaliação e implantação) e experimentar algoritmos de classificação e regressão com Scikit‑Learn.

## Índice da semana

- [Dia 1 — Processo de data science e tarefas de mineração](#dia-1--processo-de-data-science-e-tarefas-de-mineração)
- [Dia 2 — Tipos de aprendizado de máquina](#dia-2--tipos-de-aprendizado-de-máquina)
- [Dia 3 — Preparação de dados e pipeline](#dia-3--preparação-de-dados-e-pipeline)
- [Dia 4 — Primeiras implementações com Scikit‑Learn](#dia-4--primeiras-implementações-com-scikit-learn)
- [Dia 5 — Pensamento analítico de dados](#dia-5--pensamento-analítico-de-dados)
- [Dia 6 — Revisão e projeto simples](#dia-6--revisão-e-projeto-simples)

## Dia 1 — Processo de data science e tarefas de mineração

**Referência principal**

* *Data Science para Negócios*, capítulo 2: descreve as tarefas canônicas de mineração de dados, diferencia métodos supervisionados e não supervisionados e apresenta o processo de data science — Business Understanding, Data Understanding, Data Preparation, Modeling, Evaluation e Deployment.

**Referência complementar**

* *Data Science para Negócios*, capítulos 3 e 4, que discutem seleção de atributos, segmentação supervisionada e modelos lineares.

**Material on‑line**

* Blog posts ou vídeos da UNIVESP sobre ciência de dados e machine learning.

**Atividades**

- [ ] Ler o capítulo 2 de *Data Science para Negócios* com foco no processo de data science. Faça um resumo das seis etapas (entendimento do negócio, entendimento dos dados, preparação, modelagem, avaliação e implantação).
- [ ] Identificar em um problema real (por exemplo, previsão de churn ou recomendação de produto) como cada etapa do processo se aplica.
- [ ] Criar um mapa mental com as principais tarefas canônicas (classificação, regressão, agrupamento, detecção de anomalias) e diferenciar problemas supervisionados e não supervisionados.
- [ ] Registrar suas anotações em `resumos/semana-01-resumo.md`.

## Dia 2 — Tipos de aprendizado de máquina

**Referência principal**

* *Hands‑On Machine Learning* (cap. 1) e resumo do blog de Jack McKew: o capítulo define Machine Learning, apresenta situações onde o ML é útil e explica as categorias de algoritmos — supervisionado, não supervisionado, semissupervisionado e por reforço, bem como as distinções entre aprendizado em batch vs online e aprendizado baseado em instância vs baseado em modelos.

**Referência complementar**

* *Data Science para Negócios*, capítulo 2 (seção “Supervised vs Unsupervised Methods”).

**Material on‑line**

* Curso introdutório da **Coursera** ou **Kaggle Learn** sobre tipos de machine learning.

**Atividades**

- [ ] Ler o resumo de Jack McKew e o capítulo 1 de *Hands‑On Machine Learning*. Resumir os quatro tipos principais de aprendizado (supervisionado, não supervisionado, semissupervisionado e reforço) e os conceitos de aprendizado online/batch e instância/modelo.
- [ ] Listar ao menos dois exemplos de problemas para cada tipo (ex.: classificação de imagens para supervisionado, clustering de clientes para não supervisionado).
- [ ] Fazer um quiz rápido (no Kaggle Learn ou outro site) sobre classificação de problemas em tipos de ML.
- [ ] Registrar as respostas e reflexões em seu resumo semanal.

## Dia 3 — Preparação de dados e pipeline

**Referência principal**

* *Data Science para Negócios*, seções sobre data preparation (cap. 2).

**Referência complementar**

* *Hands‑On Machine Learning*, capítulos iniciais sobre preparação de dados (pré‑processamento, normalização, codificação de categorias).

**Material on‑line**

* Tutoriais do Scikit‑Learn sobre `Pipeline` e `ColumnTransformer`.

**Atividades**

- [ ] Escolher um dataset simples (`iris`, `wine` ou `titanic` via `scikit‑learn` ou `seaborn`), carregar com pandas e analisar suas características (variáveis qualitativas/quantitativas, variáveis de entrada e alvo).
- [ ] Criar um pipeline de pré‑processamento no Scikit‑Learn que trate valores nulos, realize codificação one‑hot das variáveis categóricas e padronize as variáveis numéricas.
- [ ] Dividir o conjunto em treino/validação/teste (70/15/15) e salvar os subconjuntos em `datasets/` para reutilização nas próximas semanas.
- [ ] Descrever as etapas do pipeline no seu resumo e marcar a tarefa quando finalizada.

## Dia 4 — Primeiras implementações com Scikit‑Learn

**Referência principal**

* *Hands‑On Machine Learning*, capítulos 2 e 3, que apresentam implementação de regressão linear e classificação (regressão logística e árvores de decisão) em Scikit‑Learn.

**Referência complementar**

* *Data Science para Negócios*, capítulos 3 e 4 — seleção de atributos e ajuste de modelos lineares.

**Material on‑line**

* Exemplos de classificadores (KNN, SVM) na documentação do Scikit‑Learn.

**Atividades**

- [ ] Utilizar o dataset preparado no dia 3 para treinar um modelo de **regressão** (se a variável de saída for contínua) ou **classificação** (se for categórica). Comece com **regressão linear** ou **classificador de árvore de decisão**.
- [ ] Ajustar hiperparâmetros básicos (profundidade da árvore, critério de divisão) e avaliar o modelo com validação simples (hold‑out) e `score()` do Scikit‑Learn.
- [ ] Registrar métricas de desempenho iniciais (RMSE para regressão ou acurácia para classificação).
- [ ] Explorar a importância das features (por exemplo, `feature_importances_` em árvores) e relacionar com as discussões de seleção de atributos.

## Dia 5 — Pensamento analítico de dados

**Referência principal**

* *Data Science para Negócios*, capítulo 1 — discute a ubiquidade das oportunidades de dados, a importância do pensamento analítico e como dados e capacidade analítica podem ser ativos estratégicos.

**Referência complementar**

* Artigos ou podcasts sobre carreira em ciência de dados e formulação de problemas.

**Material on‑line**

* Curso introdutório de pensamento analítico (por exemplo, Data Camp ou edX).

**Atividades**

- [ ] Ler o capítulo 1 de *Data Science para Negócios* e destacar as razões pelas quais dados são considerados ativos estratégicos e como o pensamento analítico de dados difere de uma abordagem apenas técnica.
- [ ] Escolher uma notícia ou case de empresa e explicar como a ciência de dados foi aplicada para gerar valor (ex.: recomendação de filmes, detecção de fraudes, previsão de demanda).
- [ ] Escrever um parágrafo no resumo semanal refletindo sobre o valor da ciência de dados e sua relação com os objetivos de negócio.

## Dia 6 — Revisão e projeto simples

**Referência principal**

* Todas as leituras da semana.

**Atividades**

- [ ] Revisar notas e resumos dos dias 1 a 5.
- [ ] Desenvolver um mini‑projeto no notebook: escolher uma tarefa (por exemplo, prever a sobrevivência no Titanic ou prever preços de casas) e aplicar o pipeline completo: pré‑processamento, divisão em conjuntos, treinamento de um modelo simples, avaliação e interpretação dos resultados.
- [ ] Refletir sobre desafios encontrados (por exemplo, dados desbalanceados, falta de dados, interpretação do modelo) e escrever um breve relatório em `resumos/semana-01-resumo.md`.
- [ ] Marcar as atividades concluídas no checklist semanal.