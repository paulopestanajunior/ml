# Plano 2 — Machine Learning Avançado, LLMs e Sistemas Multiagentes

Este plano de estudos aprofunda os fundamentos de **aprendizado de máquina** e **ciência de dados** e avança para o desenvolvimento de **modelos de linguagem (LLMs)** e **sistemas multiagentes**.  O foco é estudar desde a formulação de problemas, avaliação e validação de modelos clássicos até o uso de arquiteturas modernas de agentes colaborativos, com atenção para implantação, observabilidade e verificação de alucinações.

## Visão geral

* **Duração sugerida:** 8 semanas
* **Carga diária:** 3 h/dia (pode ajustar para 2 h/dia estendendo a duração)
* **Foco:** teoria, interpretação de resultados e prática aplicada em Python
* **Pré‑requisitos:** concluir o plano de estatística (Plano 1) ou ter boa base em programação e estatística

O plano está dividido em oito semanas.  As primeiras semanas revisitam conceitos de **Data Science** e modelagem supervisionada/não supervisionada com foco na avaliação de modelos.  Em seguida, estudamos redes neurais e transformadores, partimos para modelos de linguagem e **RAG** (retrieval‑augmented generation) e dedicamos duas semanas para sistemas **multiagentes**, incluindo arquiteturas, estratégias de avaliação, observabilidade e, por fim, práticas de implantação e verificação de viabilidade de produtos baseados em LLMs.

## Bibliografia recomendada

* **Data Science para Negócios** – Foster Provost & Tom Fawcett (1ª edição).  Este livro apresenta tarefas canônicas de mineração de dados e o processo de data science (business understanding, data understanding, preparação, modelagem, avaliação e implantação)【681657430915828†L53-L66】.
* **Mãos à Obra: Aprendizado de Máquina com Scikit‑Learn, Keras e TensorFlow** – Aurélien Géron (2ª edição).  Útil para implementação prática de regressão, classificação, clustering, redes neurais e técnicas modernas de deep learning.
* **Hands‑On Large Language Models** – Jay Alammar & Maarten Grootendorst (O’Reilly).  O livro mostra como utilizar LLMs pré‑treinados para redação, sumarização e classificação, construir sistemas de busca semântica além da correspondência por palavras‑chave, e desenvolver pipelines avançados que combinam **RAG** e ajuste fino de modelos【51140306659036†L25-L49】.
* **Artigos e guias on‑line**:
  * Guia da **Phoenix/Arize** sobre avaliação de sistemas multiagentes – define sistemas multiagentes e apresenta arquiteturas (rede, supervisor, hierárquica etc.) e estratégias de avaliação (handoff, nível de sistema e coordenação)【662432890623241†L140-L159】【662432890623241†L165-L183】.
  * Artigo da **Orq.ai** “A Comprehensive Guide to Evaluating Multi‑Agent LLM Systems” – discute a transição de sistemas de agente único para multiagentes e explica por que a colaboração e escalabilidade requerem novos frameworks de avaliação【173980910064675†L243-L249】.
  * Blog da **LangChain** sobre observabilidade de agentes – ressalta que a observabilidade de LLMs e agentes é diferente da observabilidade de software tradicional e demanda rastreamento detalhado de runs e traces【707464467098071†L24-L33】.
  * Artigo da **Snorkel AI** sobre observabilidade de LLMs – mostra que a observabilidade monitora precisão, completude, relevância e segurança das respostas, descrevendo os pilares e componentes da observabilidade de LLMs【658830042717487†L72-L97】.

## Organização do repositório

* **README.md** – visão geral e links para cada semana.
* **semanas/** – contém um arquivo markdown para cada semana (`semana‑01‑ds‑ml‑fundamentos.md` etc.). Cada arquivo possui um índice de dias, referências e uma checklist de atividades.
* **notebooks/** – pasta para notebooks Jupyter. Inclui um `README.md` com instruções.
* **datasets/** – pasta para conjuntos de dados utilizados nos exercícios, com um `README.md` explicando cada um.
* **resumos/** – resumos e fichamentos de leituras, separados por semana.
* **checklist‑geral.md** – lista global para acompanhar a conclusão de cada semana.

## Navegação por semana

* [Semana 1 — Fundamentos de Data Science e Aprendizado de Máquina](semanas/semana-01-fundamentos-ds-ml.md)
* [Semana 2 — Avaliação e Validação de Modelos](semanas/semana-02-avaliacao-validacao.md)
* [Semana 3 — Aprendizado Não Supervisionado e Redução de Dimensionalidade](semanas/semana-03-nao-supervisionado.md)
* [Semana 4 — Redes Neurais e Deep Learning](semanas/semana-04-redes-neurais.md)
* [Semana 5 — Modelos de Linguagem e RAG](semanas/semana-05-llms-rag.md)
* [Semana 6 — Sistemas Multiagentes: Fundamentos e Arquiteturas](semanas/semana-06-multiagentes-basico.md)
* [Semana 7 — Avaliação, Observabilidade e Métricas de Multiagentes](semanas/semana-07-avaliacao-observabilidade.md)
* [Semana 8 — Implantação e Produção de Sistemas de LLM Multiagentes](semanas/semana-08-producao.md)

## Checklist geral

Use esta lista para marcar a conclusão de cada semana:

* [ ] Semana 1 concluída
* [ ] Semana 2 concluída
* [ ] Semana 3 concluída
* [ ] Semana 4 concluída
* [ ] Semana 5 concluída
* [ ] Semana 6 concluída
* [ ] Semana 7 concluída
* [ ] Semana 8 concluída

Boa jornada de estudos!  Cada semana apresenta leituras, práticas e projetos para consolidar seu conhecimento e prepará‑lo para construir e avaliar sistemas de linguagem de ponta‑a‑ponta.