# Semana 5 — Modelos de Linguagem e RAG

Esta semana marca a transição para o mundo dos **modelos de linguagem de grande porte (LLMs)**.  Você aprenderá o que são embeddings e como realizar busca semântica, praticará **engenharia de prompts**, construirá um pipeline de **RAG** (retrieval‑augmented generation) e explorará técnicas de ajuste fino.  O objetivo é preparar terreno para sistemas multiagentes nas semanas seguintes.

## Índice da semana

- [Dia 25 — Introdução a LLMs e embeddings](#dia-25--introdução-a-llms-e-embeddings)
- [Dia 26 — Busca semântica e bases vetoriais](#dia-26--busca-semântica-e-bases-vetoriais)
- [Dia 27 — Engenharia de prompts e avaliação de saídas](#dia-27--engenharia-de-prompts-e-avaliação-de-saídas)
- [Dia 28 — Retrieval‑Augmented Generation (RAG)](#dia-28--retrieval-augmented-generation-rag)
- [Dia 29 — Ajuste fino de LLMs e LoRA](#dia-29--ajuste-fino-de-llms-e-lora)
- [Dia 30 — Projeto: pipeline generativo completo](#dia-30--projeto-pipeline-generativo-completo)

## Dia 25 — Introdução a LLMs e embeddings

**Referência principal**

* *Hands‑On Large Language Models* – capítulos iniciais que descrevem como usar LLMs pré‑treinados para tarefas de copywriting, sumarização e classificação, e introduzem o conceito de embeddings e semântica de busca【51140306659036†L25-L49】.

**Material on‑line**

* Artigos da Hugging Face sobre embeddings (`sentence-transformers`) e modelos `OpenAI/ada-002`.

**Atividades**

- [ ] Ler a introdução do *Hands‑On LLM* para entender como os LLMs são usados em tarefas de texto, explorando copywriting, sumarização e classificação【51140306659036†L25-L49】.
- [ ] Entender o conceito de **embedding**: representações vetoriais densas que capturam semântica.  Ler tutoriais sobre `SentenceTransformer` e `OpenAI Embeddings`.
- [ ] Usar um modelo de embeddings (`all-MiniLM-L6-v2` ou `text-embedding-ada-002`) para converter um conjunto de frases ou documentos em vetores e visualizar a similaridade por meio de distância coseno.
- [ ] Escrever no resumo como embeddings superam bag‑of‑words na comparação semântica.

## Dia 26 — Busca semântica e bases vetoriais

**Referência principal**

* *Hands‑On LLM* – seções sobre construção de sistemas de busca semântica além de correspondência por palavras‑chave, utilizando embeddings e índices vetoriais【51140306659036†L25-L49】.

**Material on‑line**

* Tutoriais sobre **FAISS**, **Chroma** ou **Weaviate** para armazenamento e recuperação de vetores.

**Atividades**

- [ ] Selecionar um corpus pequeno (ex.: artigos de blog, FAQs) e gerar embeddings para cada documento.
- [ ] Construir um índice vetorial com uma biblioteca como **FAISS** ou **Chroma** e implementar uma função de busca que retorne os documentos mais semelhantes a uma consulta em linguagem natural.
- [ ] Comparar os resultados da busca semântica com uma busca por palavras‑chave (TF‑IDF) e anotar diferenças qualitativas.
- [ ] Registrar no resumo as vantagens de índices vetoriais e como eles serão usados no pipeline RAG.

## Dia 27 — Engenharia de prompts e avaliação de saídas

**Referência principal**

* *Hands‑On LLM* – seções sobre **prompt engineering**, demonstrando como formular instruções claras, ajustar tom e estilo, e melhorar a qualidade das respostas【51140306659036†L25-L49】.

**Material on‑line**

* Blogposts de empresas (OpenAI, Anthropic) sobre melhores práticas de prompts; guias como “Prompt Engineering Guide”.

**Atividades**

- [ ] Escrever diferentes prompts para a mesma tarefa (por exemplo, resumir um artigo) e observar como a formulação altera a saída de um modelo (pode usar `gpt-3.5-turbo` via API ou `OpenAssistant` local).
- [ ] Experimentar técnicas de **few‑shot prompting** (incluir exemplos no prompt) e **chain‑of‑thought** (pedir para mostrar raciocínio passo a passo).  Avaliar impacto na qualidade e completude da resposta.
- [ ] Discutir em seu resumo a importância de prompts claros e específicos e como pequenos ajustes podem reduzir alucinações.
- [ ] Criar um checklist de boas práticas de prompt engineering para futura referência.

## Dia 28 — Retrieval‑Augmented Generation (RAG)

**Referência principal**

* *Hands‑On LLM* – seções que mostram como combinar embeddings, busca semântica e modelos generativos para criar pipelines RAG【51140306659036†L25-L49】.

**Material on‑line**

* Tutoriais do **LangChain** e **LlamaIndex** que implementam RAG usando LLMs e índices vetoriais.

**Atividades**

- [ ] Revisar a arquitetura RAG: 1) gerar embeddings e armazenar em base vetorial; 2) recuperar documentos relevantes; 3) passar a consulta e os documentos recuperados como contexto para o modelo gerador; 4) gerar a resposta.
- [ ] Implementar um pipeline RAG simples com **LangChain** ou **LlamaIndex**: criar a base vetorial (FAISS/Chroma), executar a consulta, recuperar trechos relevantes e gerar uma resposta com `GPT‑3.5` ou `Llama 2`.
- [ ] Avaliar a qualidade das respostas com e sem RAG para perguntas factuais; analisar se a busca reduz alucinações.
- [ ] Registrar no resumo benefícios e desafios do RAG, como atualização dinâmica de conhecimento e necessidade de curar o corpus.

## Dia 29 — Ajuste fino de LLMs e LoRA

**Referência principal**

* *Hands‑On LLM* – seções sobre **fine‑tuning** e **LoRA**, explicando como adaptar modelos para tarefas específicas e usar treinamento de baixa rank para reduzir custo e requisitos de armazenamento【51140306659036†L25-L49】.

**Material on‑line**

* Tutoriais do Hugging Face “Parameter‑Efficient Fine‑Tuning” (PEFT).

**Atividades**

- [ ] Ler sobre diferenças entre fine‑tuning completo e **LoRA**.  Entender por que LoRA permite treinar poucas matrizes e congelar o restante do modelo.
- [ ] Usar a biblioteca `peft` do Hugging Face para treinar um modelo (`flan‑t5` ou `mistral‑7b`) em uma tarefa curta (por exemplo, classificar sentimentos).  Registrar tempo de treino e tamanho do checkpoint LoRA.
- [ ] Avaliar se o ajuste fino melhora substancialmente em relação a prompt engineering e RAG.  Discutir trade‑offs entre custo computacional, necessidade de dados rotulados e performance.
- [ ] Escrever no resumo uma reflexão sobre quando vale a pena ajustar um modelo e quando RAG ou prompts são suficientes.

## Dia 30 — Projeto: pipeline generativo completo

**Referência principal**

* Todo o material estudado na semana.

**Atividades**

- [ ] Escolher um tema de interesse (por exemplo, perguntas frequentes de um produto, respostas a consultas jurídicas básicas ou tutoriais de software).  Compilar um corpus de documentos relevantes e construir uma base vetorial.
- [ ] Criar um pipeline RAG completo: ingestar documentos, criar embeddings, indexar, recuperar e gerar respostas.  Testar a pipeline com múltiplas perguntas.
- [ ] Implementar pelo menos uma técnica de avaliação de saídas (por exemplo, classificação por outro modelo ou verificação humana) para medir relevância e factualidade.
- [ ] Opcionalmente: aplicar LoRA para ajustar um modelo no corpus específico e comparar com a pipeline RAG.
- [ ] Escrever um relatório final em `resumos/semana-05-resumo.md` detalhando a arquitetura usada, ferramentas, resultados e desafios.
- [ ] Marcar as tarefas como concluídas no checklist semanal.