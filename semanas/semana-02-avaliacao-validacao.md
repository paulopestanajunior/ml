# Semana 2 — Avaliação e Validação de Modelos

Nesta semana você se concentra em **avaliar e validar modelos** de machine learning.  Aprenderá a reconhecer problemas de sobreajuste, utilizar métricas de desempenho apropriadas, aplicar validação cruzada, ajustar hiperparâmetros e interpretar resultados levando em conta custos e benefícios.  O objetivo é preparar uma base sólida para decidir quando um modelo está pronto para produção.

## Índice da semana

- [Dia 7 — Generalização, overfitting e underfitting](#dia-7--generalização-overfitting-e-underfitting)
- [Dia 8 — Métricas de avaliação e matriz de confusão](#dia-8--métricas-de-avaliação-e-matriz-de-confusão)
- [Dia 9 — Validação cruzada e ajuste de hiperparâmetros](#dia-9--validação-cruzada-e-ajuste-de-hiperparâmetros)
- [Dia 10 — Métodos de ensemble e curvas ROC](#dia-10--métodos-de-ensemble-e-curvas-roc)
- [Dia 11 — Seleção de modelos e valor esperado](#dia-11--seleção-de-modelos-e-valor-esperado)
- [Dia 12 — Projeto: avaliação comparativa](#dia-12--projeto-avaliação-comparativa)

## Dia 7 — Generalização, overfitting e underfitting

**Referência principal**

* *Data Science para Negócios*, capítulo 5 – discute generalização, sobreajuste e controle de complexidade, incluindo técnicas como cross‑validation e regularização【681657430915828†L114-L135】.

**Referência complementar**

* *Hands‑On Machine Learning*, capítulos sobre regularização e curvas de aprendizado.

**Material on‑line**

* Postagens no blog `mlpills.substack.com` sobre overfitting e underfitting.

**Atividades**

- [ ] Ler o capítulo 5 de *DS para Negócios* para entender a importância de generalização e as causas do overfitting e underfitting【681657430915828†L114-L135】.
- [ ] Plotar curvas de aprendizado (score vs tamanho do conjunto de treinamento) para o modelo desenvolvido na semana 1.  Usar Scikit‑Learn (`learning_curve`) para visualizar se há overfitting.
- [ ] Experimentar reduzir a complexidade do modelo (por exemplo, limitando a profundidade da árvore ou aplicando regularização L2) e observar o impacto.
- [ ] Anotar conclusões sobre trade‑off viés‑variância em seu resumo semanal.

## Dia 8 — Métricas de avaliação e matriz de confusão

**Referência principal**

* *DS para Negócios*, capítulo 7 – apresenta diversas métricas de avaliação, explica problemas de acurácia em classes desbalanceadas, a importância da matriz de confusão, custos e benefícios e o conceito de valor esperado na avaliação de modelos【681657430915828†L174-L190】.

**Referência complementar**

* Artigos da documentação do Scikit‑Learn sobre `accuracy_score`, `precision`, `recall`, `f1_score` e `confusion_matrix`.

**Atividades**

- [ ] Revisar os tipos de erros (falso positivo, falso negativo) e construir uma matriz de confusão para o classificador criado na semana 1, utilizando `confusion_matrix`.
- [ ] Calcular e comparar diferentes métricas: acurácia, precisão, recall, F1 e **AUC** (quando aplicável).  Entender em quais cenários cada métrica é mais indicada【681657430915828†L174-L190】.
- [ ] Criar um relatório em formato de tabela ou gráfico comparando as métricas e interpretar quais trade‑offs estão envolvidos.

## Dia 9 — Validação cruzada e ajuste de hiperparâmetros

**Referência principal**

* *DS para Negócios*, capítulo 5 – descreve métodos de validação cruzada e sua relação com overfitting【681657430915828†L114-L135】.

**Referência complementar**

* *Hands‑On Machine Learning*, seções sobre `GridSearchCV` e `RandomizedSearchCV`.

**Atividades**

- [ ] Implementar validação cruzada **k‑fold** (usando `cross_val_score`) para o modelo usado anteriormente e registrar a média e o desvio padrão das métricas.
- [ ] Utilizar `GridSearchCV` ou `RandomizedSearchCV` para ajustar hiperparâmetros do modelo (por exemplo, profundidade da árvore, número de estimadores em uma Random Forest).
- [ ] Avaliar o melhor conjunto de hiperparâmetros com base na métrica escolhida (ex.: F1 ou AUC).
- [ ] Documentar o processo e resultados em seu notebook.

## Dia 10 — Métodos de ensemble e curvas ROC

**Referência principal**

* *Hands‑On Machine Learning*, capítulo sobre **Random Forest** e **Boosting**, que mostram como combinar modelos para reduzir variância e melhorar performance.

**Referência complementar**

* *DS para Negócios*, capítulo 8 – apresenta visualizações de desempenho, como curvas ROC, área sob a curva (AUC) e curvas de lift【681657430915828†L193-L205】.

**Atividades**

- [ ] Treinar um modelo de ensemble (por exemplo, **Random Forest** ou **Gradient Boosting**) no dataset utilizado.  Comparar seu desempenho com o modelo simples das semanas anteriores.
- [ ] Plotar a curva ROC e calcular a AUC usando `roc_curve` e `auc` do Scikit‑Learn.  Interpretar o trade‑off entre sensibilidade e especificidade.
- [ ] Explorar outro método de ensemble (Bagging ou Voting Classifier) e discutir diferenças em relação ao Random Forest.

## Dia 11 — Seleção de modelos e valor esperado

**Referência principal**

* *DS para Negócios*, capítulo 7 – discute como usar **valor esperado** para avaliar modelos, levando em consideração custos e benefícios e comparando contra baselines【681657430915828†L174-L190】.

**Referência complementar**

* Artigo ou vídeo sobre métricas de custo (cost sensitive learning) e balanceamento de classes.

**Atividades**

- [ ] Definir um cenário fictício (por exemplo, detecção de fraude com custos diferentes para falsos positivos e falsos negativos).  Estabelecer um valor monetário para cada tipo de erro.
- [ ] Calcular o **valor esperado** ou lucro esperado para cada modelo treinado (árvore, Random Forest etc.), conforme a matriz de confusão e os custos/benefícios estabelecidos【681657430915828†L174-L190】.
- [ ] Selecionar o modelo com maior valor esperado e justificar a escolha, mesmo que sua acurácia não seja a mais alta.
- [ ] Documentar no resumo semanal um comparativo entre as métricas tradicionais e a métrica de valor esperado.

## Dia 12 — Projeto: avaliação comparativa

**Referência principal**

* Todos os materiais estudados ao longo da semana.

**Atividades**

- [ ] Escolher um novo conjunto de dados (por exemplo, `wine quality` ou um dataset de classificação binária do Kaggle).  Repetir todas as etapas: pré‑processamento, divisão, treinamento de pelo menos três modelos (árvore, logística, Random Forest, SVM etc.), validação cruzada e ajuste de hiperparâmetros.
- [ ] Comparar os modelos com base em várias métricas (acurácia, F1, AUC, valor esperado) e decidir qual modelo seria implantado em produção e por quê.
- [ ] Registrar as decisões e aprendizados em um relatório em `resumos/semana-02-resumo.md`.
- [ ] Marcar as tarefas concluídas na checklist semanal.