# Semana 2 — Avaliação, validação e seleção de modelos

## Índice
- [Dia 7 — Overfitting, underfitting e generalização](#dia-7--overfitting-underfitting-e-generalização)
- [Dia 8 — Métricas de classificação e regressão](#dia-8--métricas-de-classificação-e-regressão)
- [Dia 9 — Validação cruzada](#dia-9--validação-cruzada)
- [Dia 10 — Busca de hiperparâmetros](#dia-10--busca-de-hiperparâmetros)
- [Dia 11 — Custo, benefício e valor esperado](#dia-11--custo-benefício-e-valor-esperado)
- [Dia 12 — Revisão e projeto comparativo](#dia-12--revisão-e-projeto-comparativo)

## Links externos da semana
- [Scikit-learn — Model selection and evaluation](https://scikit-learn.org/stable/model_selection.html)
- [Scikit-learn — Cross-validation](https://scikit-learn.org/stable/modules/cross_validation.html)
- [Scikit-learn — Hyper-parameter tuning](https://scikit-learn.org/stable/modules/grid_search.html)
- [Scikit-learn — Classification metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#classification-metrics)
- [Scikit-learn — ROC metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#roc-metrics)

## Dia 7 — Overfitting, underfitting e generalização

**Referência principal**
- *Data Science para Negócios*, cap. 5

**Referência complementar**
- *Mãos à Obra*, partes de curvas de aprendizado e regularização

**Atividades**
- [ ] Definir overfitting e underfitting com exemplos
- [ ] Gerar curva de aprendizado
- [ ] Comparar erro de treino vs validação
- [ ] Escrever um parágrafo sobre viés vs variância

## Dia 8 — Métricas de classificação e regressão

**Referência principal**
- *Data Science para Negócios*, cap. 7

**Referência complementar**
- docs do Scikit-learn

**Atividades**
- [ ] Calcular accuracy, precision, recall, F1 e ROC-AUC
- [ ] Calcular RMSE e MAE em regressão
- [ ] Explicar quando acurácia engana
- [ ] Interpretar uma matriz de confusão

## Dia 9 — Validação cruzada

**Referência principal**
- *Data Science para Negócios*, cap. 5

**Referência complementar**
- *Mãos à Obra*, validação cruzada

**Atividades**
- [ ] Rodar k-fold cross-validation
- [ ] Comparar split único vs CV
- [ ] Salvar distribuição de scores
- [ ] Escrever por que CV é importante

## Dia 10 — Busca de hiperparâmetros

**Referência principal**
- *Mãos à Obra*, tuning de hiperparâmetros

**Referência complementar**
- docs `GridSearchCV` e `RandomizedSearchCV`

**Atividades**
- [ ] Rodar `GridSearchCV`
- [ ] Rodar `RandomizedSearchCV`
- [ ] Comparar custo e benefício
- [ ] Registrar melhor configuração encontrada

## Dia 11 — Custo, benefício e valor esperado

**Referência principal**
- *Data Science para Negócios*, cap. 7

**Objetivo**
Sair da métrica pura e entrar em decisão.

**Atividades**
- [ ] Criar um cenário com custo de falso positivo e falso negativo
- [ ] Calcular valor esperado simples
- [ ] Escolher modelo com base em custo e não só em métrica
- [ ] Escrever a decisão final

## Dia 12 — Revisão e projeto comparativo

**Entregável**
- [ ] Comparar ao menos 3 modelos
- [ ] Criar notebook `semana02_avaliacao.ipynb`
- [ ] Resumo em `resumos/semana-02-resumo.md`
