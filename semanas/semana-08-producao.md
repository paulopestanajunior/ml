# Semana 8 — Produção, segurança, custo e decisão de produto

## Índice
- [Dia 43 — Serving e arquitetura operacional](#dia-43--serving-e-arquitetura-operacional)
- [Dia 44 — APIs, empacotamento e deployment](#dia-44--apis-empacotamento-e-deployment)
- [Dia 45 — Escalabilidade, roteamento e custo](#dia-45--escalabilidade-roteamento-e-custo)
- [Dia 46 — Guardrails, segurança e governança](#dia-46--guardrails-segurança-e-governança)
- [Dia 47 — Viabilidade de produto](#dia-47--viabilidade-de-produto)
- [Dia 48 — Projeto final ponta a ponta](#dia-48--projeto-final-ponta-a-ponta)

## Links externos da semana
- [Ray Serve LLM](https://docs.ray.io/en/latest/serve/llm)
- [vLLM Production Stack](https://docs.vllm.ai/en/latest/deployment/integrations/production-stack/)
- [OpenTelemetry Signals](https://opentelemetry.io/docs/concepts/signals/)
- [LangSmith docs](https://docs.langchain.com/langsmith)
- [Data Science for Business — Table of Contents](https://data-science-for-biz.com/contents/)

## Dia 43 — Serving e arquitetura operacional

**Referência principal**
- *Building Applications with AI Agents*, design trade-offs / monitoring / protection
- Ray Serve LLM
- vLLM production stack

**Objetivo**
Entender serving de verdade.

**Atividades**
- [ ] Comparar API externa vs serving local
- [ ] Estudar OpenAI-compatible API, autoscaling e routing
- [ ] Entender multi-LoRA, cache e throughput
- [ ] Desenhar arquitetura alvo do seu sistema

## Dia 44 — APIs, empacotamento e deployment

**Referência principal**
- *AI Agents in Action*, plataforma e serviços
- docs da stack escolhida

**Atividades**
- [ ] Empacotar pipeline com FastAPI ou similar
- [ ] Criar contrato de entrada/saída
- [ ] Definir variáveis de ambiente e segredos
- [ ] Planejar deploy com Docker

## Dia 45 — Escalabilidade, roteamento e custo

**Referência principal**
- Ray Serve LLM
- vLLM production stack
- *Data Science para Negócios*, valor esperado como apoio de decisão

**Objetivo**
Trazer custo para a arquitetura.

**Atividades**
- [ ] Estimar custo por requisição
- [ ] Definir fallback de modelo
- [ ] Definir cache e budget
- [ ] Comparar caminho barato vs caminho premium

## Dia 46 — Guardrails, segurança e governança

**Referência principal**
- *Building Applications with AI Agents*, protecting agentic systems
- suas práticas de observabilidade

**Atividades**
- [ ] Definir moderação e filtros
- [ ] Definir política para dados sensíveis
- [ ] Definir quando entra human-in-the-loop
- [ ] Criar checklist de segurança do sistema

## Dia 47 — Viabilidade de produto

**Referência principal**
- *Data Science para Negócios*, decisão baseada em valor
- *Building Applications with AI Agents*, trade-offs e colaboração humano-agente

**Objetivo**
Julgar se o produto faz sentido.

**Atividades**
- [ ] Criar matriz custo / benefício / risco
- [ ] Definir sinais de que multiagente é overengineering
- [ ] Escrever critérios de go / no-go
- [ ] Comparar 2 opções de produto ou arquitetura

## Dia 48 — Projeto final ponta a ponta

**Entregável**
- [ ] Sistema completo com LLM + retrieval + observabilidade + plano de produção
- [ ] Documento de arquitetura
- [ ] Documento de viabilidade
- [ ] Notebook ou demo final
- [ ] Resumo em `resumos/semana-08-resumo.md`
