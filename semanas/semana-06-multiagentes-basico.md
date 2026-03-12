# Semana 6 — Sistemas Multiagentes: Fundamentos e Arquiteturas

Nas próximas duas semanas você irá mergulhar em **sistemas multiagentes**, que organizam múltiplos modelos de linguagem para cooperar na realização de tarefas complexas.  Começaremos com os conceitos básicos e arquiteturas, entenderemos papéis e responsabilidades de cada agente e experimentaremos construir uma pipeline simples de múltiplos agentes.

## Índice da semana

- [Dia 31 — Conceitos de sistemas multiagentes](#dia-31--conceitos-de-sistemas-multiagentes)
- [Dia 32 — Arquiteturas de sistemas multiagentes](#dia-32--arquiteturas-de-sistemas-multiagentes)
- [Dia 33 — Papéis e especialização de agentes](#dia-33--papéis-e-especialização-de-agentes)
- [Dia 34 — Estratégias de avaliação](#dia-34--estratégias-de-avaliação)
- [Dia 35 — Frameworks e métricas](#dia-35--frameworks-e-métricas)
- [Dia 36 — Projeto: pipeline multiagente simples](#dia-36--projeto-pipeline-multiagente-simples)

## Dia 31 — Conceitos de sistemas multiagentes

**Referência principal**

* Guia da **Phoenix/Arize** – define um sistema multiagente como um conjunto de agentes, cada um controlando um fluxo de aplicação com seu próprio LLM, enfatizando que a divisão de responsabilidades permite modularidade, especialização e controle【662432890623241†L121-L129】.

**Referência complementar**

* Artigo da **Orq.ai** – comenta a transição de sistemas de agente único para multiagentes e destaca a colaboração entre agentes especializados em recuperação, raciocínio ou decisão【173980910064675†L243-L249】.

**Atividades**

- [ ] Ler o guia da Phoenix para entender a definição de sistemas multiagentes, os benefícios de modularidade e especialização e os desafios de coordenação【662432890623241†L121-L129】.
- [ ] Ler a introdução do artigo da Orq.ai e anotar como a pesquisa em LLM evoluiu de arquiteturas de agente único para sistemas multiagentes, distribuindo responsabilidades entre agentes【173980910064675†L243-L249】.
- [ ] Desenhar um diagrama simplificado de um sistema multiagente com dois agentes (ex.: agente de busca e agente de sumarização).  Anotar o fluxo de informações e como cada agente adiciona valor.
- [ ] Registrar suas reflexões no resumo semanal.

## Dia 32 — Arquiteturas de sistemas multiagentes

**Referência principal**

* Phoenix/Arize – seção “Multi‑Agent Architectures”, que descreve diversas arquiteturas: **rede**, **supervisor**, **supervisor chamando ferramentas**, **hierárquica** e **workflow customizado**【662432890623241†L140-L159】.

**Referência complementar**

* Documentação do **LangChain** sobre routers e agentes hierárquicos.

**Atividades**

- [ ] Estudar as cinco arquiteturas descritas pelo guia da Phoenix (rede, supervisor, supervisor com ferramentas, hierárquica e workflow customizado).  Para cada uma, anotar vantagens e limitações【662432890623241†L140-L159】.
- [ ] Pesquisar implementações de cada arquitetura em frameworks como LangChain ou LlamaIndex.  Anotar como a comunicação ocorre em cada configuração.
- [ ] Construir uma tabela comparando arquiteturas (colunas: arquitetura, número de agentes, centralização, flexibilidade, complexidade de coordenação) e salvar em seu resumo ou notebook.
- [ ] Propor um caso de uso (por exemplo, assistente de pesquisa acadêmica) e escolher uma arquitetura apropriada.  Justificar a escolha.

## Dia 33 — Papéis e especialização de agentes

**Referência principal**

* Artigo da **Orq.ai** – enfatiza que agentes em sistemas multiagentes têm especializações específicas (recuperação de informações, raciocínio, decisão) e que essa divisão aumenta a eficiência e capacidade de resolver tarefas complexas【173980910064675†L243-L249】.

**Referência complementar**

* Guia da Phoenix sobre agentes como ferramentas (tool‑calling) e supervisores【662432890623241†L151-L153】.

**Atividades**

- [ ] Listar possíveis tipos de agentes (agente de busca, agente de análise, agente redator, agente crítico) e definir suas responsabilidades.
- [ ] Analisar como os agentes se comunicam: que dados são transmitidos (prompts, contextos), como a informação é transformada e qual agente toma a decisão final.
- [ ] Pensar em critérios para medir a eficácia de cada agente individualmente (tempo de resposta, relevância da resposta, consumo de tokens) e como isso impacta o sistema como um todo.
- [ ] Escrever no resumo a importância de ter papéis claros para evitar redundância e conflitos.

## Dia 34 — Estratégias de avaliação

**Referência principal**

* Phoenix/Arize – seção “Core Evaluation Strategies Explained”, que detalha três níveis de avaliação: **Agent Handoff Evaluation**, **System‑Level Evaluation** e **Coordination Evaluation**【662432890623241†L165-L183】.

**Referência complementar**

* Guia da Phoenix sobre “Hierarchical Evaluation” e posts da LangChain sobre avaliação de agentes.

**Atividades**

- [ ] Estudar cada estratégia de avaliação:  
  1. **Agent Handoff Evaluation** – analisar se a transferência de tarefa ocorre no momento certo, com o contexto adequado e de forma lógica【662432890623241†L165-L170】.  
  2. **System‑Level Evaluation** – medir a taxa de conclusão de tarefas, número de interações e experiência do usuário【662432890623241†L172-L177】.  
  3. **Coordination Evaluation** – avaliar qualidade da comunicação, resolução de conflitos e gerenciamento de recursos【662432890623241†L178-L183】.
- [ ] Listar possíveis métricas para cada estratégia (por exemplo, latência de resposta, número de mensagens trocadas, qualidade da resposta, satisfação do usuário).
- [ ] Pensar em formas de coletar dados de avaliação em um ambiente de produção (logs de agentes, feedback do usuário, contadores de tokens) e anotar em seu resumo.

## Dia 35 — Frameworks e métricas

**Referência principal**

* Artigo da **Orq.ai** – explica que novas métricas e frameworks são necessários para avaliar multiagentes, incluindo colaboração, escalabilidade e qualidade de saída, pois métodos tradicionais não capturam essas dimensões【173980910064675†L243-L256】.

**Referência complementar**

* Postagens sobre ferramentas de avaliação como **ChatEval**, **DeepEval** e o SDK da Phoenix.

**Atividades**

- [ ] Ler o artigo da Orq.ai e anotar por que os métodos tradicionais de avaliação (ex.: acurácia) não são suficientes para medir coordenação e comunicação em sistemas multiagentes【173980910064675†L243-L256】.
- [ ] Pesquisar e comparar frameworks de avaliação:  
  – **ChatEval**: usa LLMs como juízes para pontuar respostas de agentes;  
  – **DeepEval**: biblioteca open source para avaliação de agentes e fluxos;  
  – **Phoenix**: SDK para instrumentar agentes e medir desempenho.  
  Anotar pontos fortes e fracos de cada um.
- [ ] Se possível, instalar uma dessas ferramentas (por exemplo, DeepEval) e rodar uma avaliação simples em um pipeline de dois agentes.  Registrar os resultados.
- [ ] Definir um conjunto de métricas importantes para o seu contexto de uso (ex.: tempo total da pipeline, número de chamadas à API, custo de tokens, satisfação do usuário) e documentar no resumo.

## Dia 36 — Projeto: pipeline multiagente simples

**Referência principal**

* Todos os materiais da semana.

**Atividades**

- [ ] Escolher um problema que necessite vários passos (ex.: responder a uma pergunta extensa pesquisando a web, traduzindo informações e sumarizando em português).  Definir pelo menos dois agentes: um de busca/recuperação e outro de processamento (tradução ou sumarização).
- [ ] Selecionar uma arquitetura (por exemplo, supervisor chamando ferramentas).  Implementar o pipeline usando **LangChain** ou **LlamaIndex**, definindo prompts específicos para cada agente.
- [ ] Registrar logs completos de cada agente (prompt enviado, resposta recebida, tempo de execução).  Se possível, usar uma ferramenta de tracing (LangSmith ou Phoenix) para coletar runs/traces.
- [ ] Avaliar o pipeline em termos de **handoff**, **qualidade da resposta** e **coordenação**.  Anotar problemas (por exemplo, falha na tradução ou perda de contexto) e propor melhorias.
- [ ] Escrever um relatório em `resumos/semana-06-resumo.md` descrevendo a implementação, resultados de avaliação e reflexões sobre modularidade e comunicação.
- [ ] Marcar as atividades concluídas no checklist semanal.