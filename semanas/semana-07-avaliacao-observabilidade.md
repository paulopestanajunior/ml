# Semana 7 — Avaliação, Observabilidade e Métricas em Multiagentes

Com os fundamentos de multiagentes estabelecidos, esta semana aprofunda estratégias de **avaliação de sistemas** e explora a **observabilidade de LLMs e agentes**. Você aprenderá por que a observabilidade de LLMs é diferente da observabilidade tradicional de software, quais são os pilares e componentes necessários, como detectar alucinações e vieses, e como medir o desempenho de um sistema multiagente em produção.

## Índice da semana

- [Dia 37 — Revisão de avaliação de multiagentes](#dia-37--revisão-de-avaliação-de-multiagentes)
- [Dia 38 — Fundamentos de observabilidade de LLMs](#dia-38--fundamentos-de-observabilidade-de-llms)
- [Dia 39 — Pilares e componentes da observabilidade](#dia-39--pilares-e-componentes-da-observabilidade)
- [Dia 40 — Detecção de alucinações e vieses](#dia-40--detecção-de-alucinações-e-vieses)
- [Dia 41 — Observabilidade de agentes e tracing](#dia-41--observabilidade-de-agentes-e-tracing)
- [Dia 42 — Projeto: monitoramento e avaliação em prática](#dia-42--projeto-monitoramento-e-avaliação-em-prática)

## Dia 37 — Revisão de avaliação de multiagentes

**Referência principal**

* Revisão das estratégias de avaliação vistas no dia 34: **Agent Handoff Evaluation**, **System‑Level Evaluation** e **Coordination Evaluation**.

**Atividades**

- [ ] Revisar suas anotações da semana anterior sobre as três estratégias de avaliação e as métricas propostas.
- [ ] Pensar em exemplos concretos de quando cada estratégia seria usada (por exemplo, handoff evaluation em chatbots com múltiplos agentes, system-level evaluation para medir latência total e taxa de sucesso).
- [ ] Atualizar seu resumo com qualquer nova ideia ou métrica que tenha surgido.

## Dia 38 — Fundamentos de observabilidade de LLMs

**Referência principal**

* Artigo da **Snorkel AI** sobre observabilidade de LLMs – explica que monitorar a qualidade de LLMs envolve medir precisão, completude, relevância e segurança das respostas, e que observabilidade de LLMs difere da observabilidade de sistemas tradicionais.

**Referência complementar**

* Trechos do mesmo artigo que discutem os desafios de depurar LLMs, como respostas infinitas, dificuldade de replicação e detecção de drift.

**Atividades**

- [ ] Ler o artigo da Snorkel AI para entender por que os métodos tradicionais de monitoramento de software não são suficientes para LLMs. Anotar os pilares da observabilidade de LLMs: precisão, completude, relevância e segurança.
- [ ] Identificar exemplos de falhas em LLMs (alucinações, respostas incompletas, viés, linguagem imprópria) e discutir como cada pilar da observabilidade pode ajudar a detectá‑las.
- [ ] Registrar no resumo as diferenças entre monitorar LLMs e monitorar pipelines de ML tradicionais (por exemplo, outputs inesgotáveis, dificuldade de explicar decisões etc.).

## Dia 39 — Pilares e componentes da observabilidade

**Referência principal**

* Snorkel AI – seções que descrevem os princípios da observabilidade de LLMs (orientada por dados, métricas em tempo real, transparência, insights preditivos) e os componentes necessários: monitoramento de respostas, latência e throughput, padrões de uso, detecção de drift, detecção de erros e feedback loop.

**Referência complementar**

* Documentação de ferramentas como **LangSmith**, **Langfuse** ou **Phoenix**, que implementam tracing e dashboards.

**Atividades**

- [ ] Estudar os princípios da observabilidade (por exemplo, uso de métricas orientadas a dados e transparência) e como cada componente (monitoramento de latência, drift, feedback) contribui para a detecção de problemas.
- [ ] Criar uma checklist de componentes que você deseja implementar em seu projeto de LLMs (ex.: coletar métricas de latência e throughput, registrar prompts e respostas, implementar anotação de segurança).
- [ ] Explorar uma ferramenta de observabilidade (como **LangSmith** ou **Phoenix**) para visualizar runs e traces. Anotar quais informações são coletadas e como elas ajudam na depuração.

## Dia 40 — Detecção de alucinações e vieses

**Referência principal**

* Snorkel AI – discute que alucinações e vieses são aspectos centrais a monitorar em LLMs e apresenta princípios para detecção e mitigação.

**Referência complementar**

* Artigos da OpenAI ou Anthropic sobre **red teaming** e técnicas de verificação de fatos.

**Atividades**

- [ ] Ler trechos do artigo da Snorkel AI sobre alucinações e vieses. Anotar o que caracteriza uma alucinação e como diferenciar de imprecisão menor.
- [ ] Testar seu modelo ou pipeline RAG com perguntas adversárias ou fora do escopo e observar se ele gera alucinações. Registrar exemplos.
- [ ] Explorar técnicas para mitigar alucinações: RAG, filtragem de respostas por classificadores auxiliares, penalizações no objetivo de geração, prompts mais restritos.
- [ ] Pesquisar como medir viés (ex.: proporção de respostas estereotipadas) e considerar incorporar métricas de fair‑ness no monitoramento.

## Dia 41 — Observabilidade de agentes e tracing

**Referência principal**

* Blog da **LangChain** – afirma que para depurar agentes é necessário entender como eles raciocinam, e que a observabilidade de agentes requer **runs**, **traces** e **threads** para rastrear cada passo de decisão.

**Referência complementar**

* Documentação do **LangSmith** e exemplos de uso de tracing com múltiplos agentes.

**Atividades**

- [ ] Ler o blog da LangChain e anotar por que o comportamento dos agentes não pode ser depurado apenas com logs tradicionais; compreender a necessidade de rastrear prompts, contextos, ferramentas chamadas e respostas.
- [ ] Configurar **LangSmith** ou **Langfuse** em um pipeline multiagente simples (do projeto da semana 6) para coletar runs e traces. Inspecionar o histórico de chamadas, tempo de resposta e prompts gerados.
- [ ] Criar gráficos ou tabelas mostrando a sequência de interações entre agentes e destacar onde ocorreram atrasos ou perdas de contexto.
- [ ] Registrar no resumo como o tracing ajuda a entender e melhorar a coordenação entre agentes.

## Dia 42 — Projeto: monitoramento e avaliação em prática

**Referência principal**

* Todos os materiais estudados nas semanas 6 e 7.

**Atividades**

- [ ] Expandir o pipeline multiagente construído na semana 6 para incluir ferramentas de observabilidade. Instrumentar cada agente para coletar métricas como tempo de execução, número de tokens e resultado da geração.
- [ ] Implementar ou configurar um painel simples (pode ser com pandas ou uma biblioteca de dashboards) para visualizar métricas em tempo real e identificar pontos de falha.
- [ ] Avaliar o sistema em relação às três estratégias (handoff, system‑level, coordination). Registrar métricas quantitativas e qualitativas (por exemplo, satisfação do usuário ou revisão manual das respostas).
- [ ] Escrever um relatório em `resumos/semana-07-resumo.md` explicando o processo de instrumentação, o que foi observado, quais problemas foram encontrados (alucinações, atrasos, erros de coordenação) e possíveis melhorias.
- [ ] Marcar as tarefas concluídas no checklist semanal.