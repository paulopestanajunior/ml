# Semana 6 — Sistemas multiagentes: design, orquestração e memória

## Índice
- [Dia 31 — O que é agente e o que não é](#dia-31--o-que-é-agente-e-o-que-não-é)
- [Dia 32 — Tool use e action calling](#dia-32--tool-use-e-action-calling)
- [Dia 33 — Orquestração e patterns multiagentes](#dia-33--orquestração-e-patterns-multiagentes)
- [Dia 34 — Memória, conhecimento e estado](#dia-34--memória-conhecimento-e-estado)
- [Dia 35 — Planning, reasoning e feedback loops](#dia-35--planning-reasoning-e-feedback-loops)
- [Dia 36 — Projeto multiagente](#dia-36--projeto-multiagente)

## Links externos da semana
- [Hugging Face Agents Course](https://huggingface.co/agents-course)
- [Phoenix — Evaluating Multi-Agent Systems](https://arize.com/docs/phoenix/learn/evaluating-multi-agent-systems)
- [DeepLearning.AI — Multi AI Agent Systems with crewAI](https://www.deeplearning.ai/short-courses/multi-ai-agent-systems-with-crewai/)
- [Phoenix — Evaluate CrewAI agents](https://arize.com/docs/phoenix/integrations/llm-providers/google-gen-ai/google-gen-ai-evals-1)

## Dia 31 — O que é agente e o que não é

**Referência principal**
- *Building Applications with AI Agents*, caps. 1 e 2
- *AI Agents in Action*, cap. 1

**Objetivo**
Entender definição séria de agente, componentes e fronteiras do conceito.

**Atividades**
- [ ] Definir agente, ferramenta, workflow e assistente
- [ ] Comparar single-agent vs workflow determinístico
- [ ] Escrever quando um “agente” é só marketing
- [ ] Criar tabela: problema, por que usar agente, por que não usar

## Dia 32 — Tool use e action calling

**Referência principal**
- *Building Applications with AI Agents*, tool use
- *AI Agents in Action*, actions / functions / Semantic Kernel

**Objetivo**
Entender o uso de ferramentas como núcleo do comportamento agentic.

**Atividades**
- [ ] Implementar um agente simples com tools
- [ ] Testar function calling
- [ ] Comparar tool selection correta vs incorreta
- [ ] Documentar falhas de ferramenta e argumentos inválidos

## Dia 33 — Orquestração e patterns multiagentes

**Referência principal**
- *Building Applications with AI Agents*, orchestration e from one agent to many
- *AI Agents in Action*, multi-agent systems com AutoGen / CrewAI

**Objetivo**
Entender padrões de coordenação.

**Atividades**
- [ ] Estudar padrões: supervisor, network, hierarchical, tool-calling, workflow customizado
- [ ] Relacionar com a tabela da Phoenix
- [ ] Escolher um caso de uso e desenhar 2 arquiteturas possíveis
- [ ] Comparar custo e complexidade de coordenação

## Dia 34 — Memória, conhecimento e estado

**Referência principal**
- *Building Applications with AI Agents*, knowledge and memory
- *AI Agents in Action*, capítulo de memory and knowledge

**Objetivo**
Separar memória curta, longa, episódica e conhecimento recuperado.

**Atividades**
- [ ] Definir memória de conversa, memória episódica e memória semântica
- [ ] Relacionar memória com RAG
- [ ] Definir estratégia de estado para um agente
- [ ] Escrever riscos de memória mal gerida

## Dia 35 — Planning, reasoning e feedback loops

**Referência principal**
- *AI Agents in Action*, reasoning, evaluation, planning and feedback
- *Building Applications with AI Agents*, learning / improvement loops

**Objetivo**
Entender agentes para além de “chat com tools”.

**Atividades**
- [ ] Estudar sequential planning, decomposition e feedback
- [ ] Comparar chain-of-thought, prompt chaining e planner explícito
- [ ] Definir um loop de melhoria para agente
- [ ] Escrever quando o planejamento melhora e quando só aumenta latência

## Dia 36 — Projeto multiagente

**Entregável**
- [ ] Notebook `semana06_multiagentes.ipynb`
- [ ] Sistema com pelo menos 2 agentes e 1 ferramenta real
- [ ] Documento de arquitetura
- [ ] Resumo em `resumos/semana-06-resumo.md`
