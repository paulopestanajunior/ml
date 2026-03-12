# Semana 7 — Avaliação e observabilidade de LLMs e agentes

## Índice
- [Dia 37 — Avaliação de agentes por camada](#dia-37--avaliação-de-agentes-por-camada)
- [Dia 38 — Observabilidade de LLMs](#dia-38--observabilidade-de-llms)
- [Dia 39 — Traces, metrics e logs com OpenTelemetry](#dia-39--traces-metrics-e-logs-com-opentelemetry)
- [Dia 40 — Tracing e avaliação com LangSmith / Phoenix](#dia-40--tracing-e-avaliação-com-langsmith--phoenix)
- [Dia 41 — Alucinação, groundedness, segurança e anonimização](#dia-41--alucinação-groundedness-segurança-e-anonimização)
- [Dia 42 — Projeto de avaliação e observabilidade](#dia-42--projeto-de-avaliação-e-observabilidade)

## Links externos da semana
- [LangSmith Observability](https://docs.langchain.com/langsmith/observability)
- [LangSmith Observability Quickstart](https://docs.langchain.com/langsmith/observability-quickstart)
- [OpenTelemetry Signals](https://opentelemetry.io/docs/concepts/signals/)
- [Phoenix — Evaluating Multi-Agent Systems](https://arize.com/docs/phoenix/learn/evaluating-multi-agent-systems)
- [Phoenix — Evaluate CrewAI agents](https://arize.com/docs/phoenix/integrations/llm-providers/google-gen-ai/google-gen-ai-evals-1)

## Dia 37 — Avaliação de agentes por camada

**Referência principal**
- *Building Applications with AI Agents*, validation and measurement
- Phoenix docs

**Objetivo**
Separar avaliação por handoff, agente e sistema.

**Atividades**
- [ ] Definir avaliação de handoff
- [ ] Definir avaliação sistêmica
- [ ] Definir avaliação de coordenação
- [ ] Criar tabela de métricas por camada

## Dia 38 — Observabilidade de LLMs

**Referência principal**
- *Building Applications with AI Agents*, monitoring in production
- docs do LangSmith observability

**Objetivo**
Entender por que LLM apps exigem observabilidade diferente.

**Atividades**
- [ ] Definir run, trace e thread
- [ ] Explicar por que debugging de LLM é diferente de software tradicional
- [ ] Listar 10 campos que devem ir para telemetria
- [ ] Definir métricas de latência, custo e qualidade

## Dia 39 — Traces, metrics e logs com OpenTelemetry

**Referência principal**
- OpenTelemetry docs

**Objetivo**
Criar base padrão de instrumentação.

**Atividades**
- [ ] Ler sobre traces, metrics e logs
- [ ] Desenhar mapa de telemetria do seu sistema
- [ ] Definir atributos obrigatórios
- [ ] Planejar correlação entre métricas e traces

## Dia 40 — Tracing e avaliação com LangSmith / Phoenix

**Referência principal**
- LangSmith docs
- Phoenix docs

**Objetivo**
Ligar avaliação e observabilidade.

**Atividades**
- [ ] Instrumentar um app com tracing
- [ ] Capturar execução de RAG ou agente
- [ ] Ver passos, tools, latência e falhas
- [ ] Comparar LangSmith e Phoenix no seu contexto

## Dia 41 — Alucinação, groundedness, segurança e anonimização

**Referência principal**
- docs LangSmith sobre anonymizers
- sua stack de avaliação

**Objetivo**
Entrar em qualidade e segurança operacional.

**Atividades**
- [ ] Definir hallucination, groundedness e faithfulness
- [ ] Criar checklist manual de inspeção
- [ ] Planejar anonimização de dados sensíveis nos traces
- [ ] Definir flags de segurança e review humana

## Dia 42 — Projeto de avaliação e observabilidade

**Entregável**
- [ ] Instrumentar o projeto RAG ou multiagente
- [ ] Criar dashboard mínimo de métricas
- [ ] Criar dataset de regressão com casos bons e ruins
- [ ] Resumo em `resumos/semana-07-resumo.md`
