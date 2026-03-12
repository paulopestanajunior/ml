# Semana 3 — Aprendizado Não Supervisionado e Redução de Dimensionalidade

Esta semana trata de métodos **não supervisionados** — algoritmos que aprendem padrões e estruturas sem rótulos de saída. Você estudará medidas de similaridade, vizinhança e clustering, além de técnicas de redução de dimensionalidade como **PCA**. Também aprenderá a avaliar a qualidade de clusters e a importância do pré‑processamento.

## Índice da semana

- [Dia 13 — Similaridade e vizinhos](#dia-13--similaridade-e-vizinhos)
- [Dia 14 — Algoritmos de clustering](#dia-14--algoritmos-de-clustering)
- [Dia 15 — Redução de dimensionalidade (PCA)](#dia-15--redução-de-dimensionalidade-pca)
- [Dia 16 — Engenharia de atributos e escalonamento](#dia-16--engenharia-de-atributos-e-escalonamento)
- [Dia 17 — Avaliação de clusters](#dia-17--avaliação-de-clusters)
- [Dia 18 — Projeto: segmentação de dados](#dia-18--projeto-segmentação-de-dados)

## Dia 13 — Similaridade e vizinhos

**Referência principal**

* *DS para Negócios*, capítulo 6 – introduz conceitos de similaridade e distância e apresenta métodos de vizinhos mais próximos (k‑NN) e clustering, destacando questões de dimensionalidade, eficiência e influência do número de vizinhos.

**Referência complementar**

* *Hands‑On Machine Learning*, seções sobre k‑NN e medidas de distância.

**Atividades**

- [ ] Revisar as definições de **distância Euclidiana** e outras métricas (por exemplo, Manhattan, Minkowski) e quando utilizá‑las.
- [ ] Implementar um classificador **k‑nearest neighbors** com Scikit‑Learn no dataset da semana 1. Ajustar k e observar como ele afeta a fronteira de decisão e a performance.
- [ ] Visualizar os vizinhos em um gráfico de dispersão 2D (use PCA ou selecione duas features). Interpretar como os pontos próximos influenciam a predição.
- [ ] Escrever no resumo como a escolha da métrica de distância e do número de vizinhos impacta o resultado.

## Dia 14 — Algoritmos de clustering

**Referência principal**

* *DS para Negócios*, capítulo 6 – apresenta métodos de clustering: **k‑means**, clustering hierárquico e outras abordagens, discute preparação de dados e exemplos de aplicação.

**Referência complementar**

* *Mãos à Obra*, capítulo sobre clustering e PCA (caso tenha acesso);
* Documentação do Scikit‑Learn (`KMeans`, `AgglomerativeClustering`, `DBSCAN`).

**Atividades**

- [ ] Utilizar `KMeans` para segmentar um dataset (por exemplo, clientes ou vinhos). Avaliar diferentes valores de *k* com o método do cotovelo (inércia) e a pontuação **silhouette**.
- [ ] Testar um método **hierárquico** (`AgglomerativeClustering`) e visualizar o dendrograma (com `scipy.cluster.hierarchy`). Comparar com o k‑means.
- [ ] Explorar um método baseado em densidade (`DBSCAN`) e observar como ele lida com clusters de forma arbitrária e pontos de ruído.
- [ ] Documentar vantagens e desvantagens de cada algoritmo no resumo.

## Dia 15 — Redução de dimensionalidade (PCA)

**Referência principal**

* *Mingoti – Análise de Dados através de Métodos de Estatística Multivariada*, capítulo 3 – explica componentes principais (PCA), critérios para determinar o número de componentes e interpretação de autovalores (variação explicada).

**Referência complementar**

* Documentação do Scikit‑Learn (`PCA`), que mostra como ajustar e transformar dados com PCA.

**Atividades**

- [ ] Ler o capítulo sobre **PCA** no livro da Mingoti, entendendo como as componentes principais são calculadas, como determinar o número de componentes e como interpretar a variância explicada.
- [ ] Aplicar PCA ao dataset usado para clustering (dia 14), projetando os dados em 2 ou 3 dimensões. Plotar os dados transformados e colorir por cluster para avaliar separabilidade.
- [ ] Experimentar reduzir a dimensionalidade antes de aplicar k‑means ou DBSCAN e observar mudanças na qualidade do agrupamento.
- [ ] Registrar insights sobre benefícios e limitações do PCA (por exemplo, perda de interpretabilidade, necessidade de padronização).

## Dia 16 — Engenharia de atributos e escalonamento

**Referência principal**

* *Hands‑On Machine Learning*, capítulos que tratam de pré‑processamento e transformação de features (normalização, padronização, codificação, discretização).

**Referência complementar**

* Artigos sobre feature engineering (por exemplo, no Kaggle ou Medium).

**Atividades**

- [ ] Explorar diferentes técnicas de escalonamento (`StandardScaler`, `MinMaxScaler`, `RobustScaler`) e transformação (`PowerTransformer`) em seus dados. Analisar como elas impactam algoritmos baseados em distância.
- [ ] Criar novas features a partir de combinações ou transformações (ex.: interação entre variáveis, log de valores skewed). Avaliar se essas novas variáveis melhoram a performance do k‑NN ou do clustering.
- [ ] Registrar no resumo os cuidados com vazamento de informação ao aplicar transformações (treinar escalonadores apenas no conjunto de treino).

## Dia 17 — Avaliação de clusters

**Referência principal**

* *DS para Negócios*, capítulo 6 – discute como interpretar resultados de cluster e a importância de combinar dados exploratórios e conhecimento de domínio para avaliar a utilidade dos clusters.

**Referência complementar**

* Artigos sobre métricas de clustering (silhouette, Davies–Bouldin, Calinski–Harabasz).

**Atividades**

- [ ] Calcular a **silhouette score** para diferentes números de clusters em k‑means e interpretar os valores obtidos (quanto mais próximo de 1, melhor a coesão e separação). Visualizar a silhouette plot.
- [ ] Calcular outras métricas, como **Davies–Bouldin index** e **Calinski–Harabasz score**, e comparar resultados.
- [ ] Avaliar a interpretabilidade dos clusters com base em características reais (por exemplo, quais tipos de clientes cada cluster representa). Discutir se os clusters fazem sentido para o negócio.
- [ ] Escrever um parágrafo no resumo sobre como escolher o número de clusters e como validar clusters sem rótulos.

## Dia 18 — Projeto: segmentação de dados

**Referência principal**

* Todos os materiais estudados na semana.

**Atividades**

- [ ] Selecionar um dataset realista (por exemplo, dados de transações, características de produtos ou métricas de comportamento de usuários). Realizar limpeza, tratamento de valores faltantes e escalonamento.
- [ ] Aplicar PCA (se necessário) para reduzir a dimensionalidade e, em seguida, testar diferentes algoritmos de clustering (k‑means, hierárquico, DBSCAN) e valores de k/eps.
- [ ] Avaliar os resultados com as métricas estudadas e interpretar clusters sob a ótica do negócio: o que cada grupo representa? Quais ações poderiam ser tomadas a partir dessa segmentação?
- [ ] Salvar gráficos e relatórios no notebook e escrever um resumo em `resumos/semana-03-resumo.md`.
- [ ] Marcar as tarefas concluídas na checklist.