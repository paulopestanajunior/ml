# Semana 5 — LLMs, embeddings e RAG de verdade

## Índice
- [Dia 25 — LLMs, tokens e embeddings](#dia-25--llms-tokens-e-embeddings)
- [Dia 26 — Retrieval: chunking, indexing e busca](#dia-26--retrieval-chunking-indexing-e-busca)
- [Dia 27 — Hybrid retrieval, reranking e query transformation](#dia-27--hybrid-retrieval-reranking-e-query-transformation)
- [Dia 28 — Arquitetura RAG ponta a ponta](#dia-28--arquitetura-rag-ponta-a-ponta)
- [Dia 29 — Avaliação de RAG](#dia-29--avaliação-de-rag)
- [Dia 30 — Projeto RAG robusto](#dia-30--projeto-rag-robusto)

## Links externos da semana
- [Hugging Face Course](https://huggingface.co/course)
- [DeepLearning.AI — Retrieval Augmented Generation (RAG)](https://www.deeplearning.ai/courses/retrieval-augmented-generation-rag/)
- [LangSmith — Trace a RAG app](https://docs.langchain.com/langsmith/observability)
- [RAG paper](https://doi.org/10.48550/arXiv.2005.11401)

## Dia 25 — LLMs, tokens e embeddings

**Referência principal**
- *Hands-On Large Language Models*

**Referência complementar**
- Hugging Face Course

**Objetivo**
Entender base conceitual antes de montar RAG.

**Atividades**
- [ ] Revisar tokens, contexto, embeddings e similaridade
- [ ] Gerar embeddings de documentos
- [ ] Comparar coseno entre consultas e documentos
- [ ] Anotar diferença entre embedding de sentença e geração autoregressiva

## Dia 26 — Retrieval: chunking, indexing e busca

**Referência principal**
- *Hands-On Large Language Models*
- *AI Agents in Action*, cap. de memória e conhecimento

**Objetivo**
Montar o lado de recuperação corretamente.

**Atividades**
- [ ] Comparar chunking por caracteres, sentenças e tokens
- [ ] Definir estratégia de metadata
- [ ] Indexar documentos em base vetorial
- [ ] Medir qualitativamente se o chunk ficou grande demais ou pequeno demais

## Dia 27 — Hybrid retrieval, reranking e query transformation

**Referência principal**
- *Hands-On Large Language Models*
- docs de retrieval / vector DB do stack escolhido

**Objetivo**
Ir além do RAG “tutorial”.

**Atividades**
- [ ] Estudar dense retrieval vs sparse retrieval
- [ ] Montar teste simples de busca híbrida
- [ ] Adicionar reranking
- [ ] Testar query rewrite ou decomposition
- [ ] Escrever quando vale o custo extra

## Dia 28 — Arquitetura RAG ponta a ponta

**Referência principal**
- *Hands-On Large Language Models*
- *AI Agents in Action*, cap. de RAG e memória

**Objetivo**
Entender todos os blocos do sistema.

**Atividades**
- [ ] Desenhar arquitetura de ingestão, indexação, retrieval, reranking e geração
- [ ] Definir fallback quando retrieval falhar
- [ ] Definir cache
- [ ] Definir logging básico por etapa

## Dia 29 — Avaliação de RAG

**Referência principal**
- paper RAG
- docs LangSmith / avaliação de apps de LLM

**Objetivo**
Separar avaliação de retrieval e de geração.

**Atividades**
- [ ] Medir Recall@k ou métrica simples de recuperação
- [ ] Avaliar faithfulness / groundedness manualmente em um conjunto pequeno
- [ ] Separar falha de retrieval de falha de geração
- [ ] Montar um mini dataset de regressão para o sistema

## Dia 30 — Projeto RAG robusto

**Entregável**
- [ ] Notebook `semana05_rag.ipynb`
- [ ] Pipeline com indexação + retrieval + geração
- [ ] Resumo em `resumos/semana-05-resumo.md`
- [ ] Documento com decisões: chunking, embedding, retriever, reranker, avaliação
