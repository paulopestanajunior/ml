# Semana 4 — Redes Neurais e Deep Learning

Após dominar fundamentos e técnicas clássicas, esta semana introduz **redes neurais** e conceitos de **deep learning**.  Você aprenderá sobre perceptrons e funções de ativação, montará modelos `Keras`/`TensorFlow` simples, explorará arquiteturas de rede (MLPs, CNNs) e terá um primeiro contato com **transformers**, ponte para os modelos de linguagem da próxima semana.

## Índice da semana

- [Dia 19 — Noções básicas de redes neurais](#dia-19--noções-básicas-de-redes-neurais)
- [Dia 20 — Treinando redes profundas](#dia-20--treinando-redes-profundas)
- [Dia 21 — Convoluções e sequências (opcional)](#dia-21--convoluções-e-sequências-opcional)
- [Dia 22 — Introdução a transformadores](#dia-22--introdução-a-transformadores)
- [Dia 23 — Ajuste fino e transferência de aprendizado](#dia-23--ajuste-fino-e-transferência-de-aprendizado)
- [Dia 24 — Projeto: redes neurais na prática](#dia-24--projeto-redes-neurais-na-prática)

## Dia 19 — Noções básicas de redes neurais

**Referência principal**

* *Mãos à Obra: Aprendizado de Máquina com Scikit‑Learn, Keras e TensorFlow* – capítulo sobre redes neurais artificiais; apresenta perceptron, funções de ativação e backpropagation, e mostra como implementar MLPs no Keras.

**Material on‑line**

* Documentação do TensorFlow/Keras sobre `Sequential` e `Dense` layers.

**Atividades**

- [ ] Revisar os conceitos de neurônio artificial, pesos e bias, funções de ativação (sigmoide, ReLU, tanh) e como o **backpropagation** ajusta pesos em redes.
- [ ] Criar um notebook `semana04_neural_basics.ipynb` e implementar uma rede de perceptron simples no Keras para classificar o dataset de flores Iris.  Comparar o desempenho com o classificador tradicional da semana 1.
- [ ] Explorar a mudança de função de ativação (ReLU vs sigmoide) e número de neurônios em cada camada.
- [ ] Registrar no resumo como a escolha da arquitetura influencia a capacidade de aprender relações não lineares.

## Dia 20 — Treinando redes profundas

**Referência principal**

* *Mãos à Obra*, seções sobre treinamento de redes profundas (otimizadores, funções de perda, regularização e dropout).

**Material on‑line**

* Curso “Deep Learning Specialization” (Andrew Ng) – vídeos sobre redes profundas.

**Atividades**

- [ ] Estender o modelo do dia 19 para uma **rede neural profunda** (Múltiplas camadas).  Utilizar otimizadores diferentes (SGD, Adam) e comparar a convergência e performance.
- [ ] Aplicar **dropout** e **regularização L2** para reduzir overfitting.  Avaliar a influência nas curvas de treinamento e validação.
- [ ] Experimentar em um dataset mais complexo (por exemplo, `Fashion-MNIST` via Keras).  Preprocessar as imagens e treinar uma rede simples.
- [ ] Escrever no resumo as lições aprendidas sobre escolha de otimizadores e regularização.

## Dia 21 — Convoluções e sequências (opcional)

Esta sessão é opcional e introdutória para quem deseja explorar **redes neurais convolucionais (CNNs)** para imagens ou **redes recorrentes (RNNs)** para sequências.

**Referência principal**

* *Mãos à Obra*, capítulos sobre CNNs e RNNs.

**Atividades**

- [ ] Implementar uma **CNN** simples para classificação de dígitos (`MNIST`).  Usar `Conv2D`, `MaxPooling2D` e `Flatten`.  Comparar com a rede densa do dia 20.
- [ ] (Opcional) Explorar uma **rede recorrente simples** (LSTM ou GRU) em uma tarefa de previsão de texto ou séries temporais.
- [ ] Registrar no resumo se a convolução trouxe ganhos de performance e como ela difere de redes densas na captura de padrões locais.

## Dia 22 — Introdução a transformadores

**Referência principal**

* *Hands‑On Large Language Models* – capítulos iniciais que explicam a arquitetura dos **transformers**, mecanismos de atenção e como modelos de linguagem são pré‑treinados e adaptados para diferentes tarefas【51140306659036†L25-L49】.

**Material on‑line**

* Artigos “Attention is All You Need” (Vaswani et al.), blogs de Jay Alammar e tutoriais do Hugging Face sobre `transformers`.

**Atividades**

- [ ] Ler sobre a arquitetura de **transformers**: self‑attention, multi‑head attention, positional encoding e camadas feed‑forward.  Entender por que transformers substituíram RNNs em muitas tarefas de NLP【51140306659036†L25-L49】.
- [ ] Usar `transformers` da Hugging Face para carregar um modelo pré‑treinado (por exemplo, `bert-base-uncased`).  Examinar o tokenizador e gerar embeddings de sentenças.
- [ ] Treinar (ou ajustar levemente) um modelo `DistilBERT` para classificar sentimento de frases pequenas (pode usar um dataset como `IMDB` ou `SST2` via `datasets` da Hugging Face).
- [ ] Documentar no resumo como a atenção permite que o modelo relacione palavras em diferentes posições e como as embeddings podem ser usadas em tarefas de machine learning.

## Dia 23 — Ajuste fino e transferência de aprendizado

**Referência principal**

* *Hands‑On Large Language Models* – seções sobre ajuste fino e aprendizado por instrução, cobrindo técnicas como **LoRA** (Low‑Rank Adaptation) e **in‑context learning**【51140306659036†L25-L49】.

**Material on‑line**

* Tutoriais do Hugging Face sobre fine‑tuning de modelos `BERT` e `GPT` para classificação ou geração.

**Atividades**

- [ ] Estudar a diferença entre **fine‑tuning** completo e métodos leves como **LoRA**.  Ler exemplos de uso em *Hands‑On LLM*【51140306659036†L25-L49】.
- [ ] Escolher um modelo pré‑treinado (por exemplo, `gpt2-small`) e realizar fine‑tuning em um conjunto simples (ex.: notícias esportivas).  Registrar tempo de treino e tamanho dos arquivos adaptados.
- [ ] Experimentar **in‑context learning** com modelos disponíveis via API (por exemplo, ChatGPT ou Llama 2) para realizar tarefas de tradução ou sumarização sem treinamento adicional.
- [ ] Analisar quando faz sentido ajustar um modelo e quando usar in‑context learning e escrever suas conclusões no resumo.

## Dia 24 — Projeto: redes neurais na prática

**Referência principal**

* Todos os materiais da semana.

**Atividades**

- [ ] Escolher um problema do mundo real que pode ser resolvido com redes neurais (por exemplo, classificação de sentimentos, detecção de fraudes, previsão de vendas).  Obter um dataset adequado e aplicar as etapas completas de pré‑processamento.
- [ ] Construir pelo menos dois modelos: um **MLP** e um **transformer** (ou CNN se for imagem).  Treinar, ajustar e comparar as performances em métricas relevantes.
- [ ] Utilizar técnicas de regularização e avaliar com validação cruzada para evitar overfitting.
- [ ] Documentar os resultados em um relatório no resumo (`resumos/semana-04-resumo.md`) e refletir sobre qual modelo seria implantado e por quê.
- [ ] Marcar as tarefas concluídas no checklist semanal.