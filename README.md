# 🧠 Caderno Temático: Machine Learning — Estudo com NotebookLM

> Projeto desenvolvido como parte do desafio da DIO: uso da Inteligência Artificial (NotebookLM) como ferramenta de aprendizagem ativa para curadoria, síntese e consolidação de conhecimento sobre Machine Learning.

---

## 🎯 Contexto e Objetivos

**Tema escolhido:** Machine Learning (Aprendizado de Máquina)

**Por que esse tema:**
> _Escreva aqui sua motivação: interesse profissional, curiosidade, necessidade de aplicar em um projeto, transição de carreira etc._

**Objetivos de estudo:**
- [ ] Entender os principais tipos de aprendizado (supervisionado, não supervisionado, por reforço)
- [ ] Compreender o fluxo de um projeto de ML (coleta de dados → treino → avaliação → deploy)
- [ ] Diferenciar os principais algoritmos (regressão, árvores de decisão, redes neurais, etc.)
- [ ] Entender métricas de avaliação de modelos (acurácia, precisão, recall, F1, etc.)
- [ ] _Adicione outros objetivos específicos seus_

---

## 📚 Curadoria de Fontes

Fontes carregadas no NotebookLM (9 fontes — mistura de conceitos gerais, comparações técnicas, aplicação prática e um artigo científico):

1. **Aprendizado de máquina — Wikipédia** — https://pt.wikipedia.org/wiki/Aprendizado_de_máquina — Visão geral enciclopédica do conceito, histórico e principais subáreas. Bom ponto de partida neutro.
2. **Aprendizado supervisionado vs. não supervisionado — AWS** — https://aws.amazon.com/compare/the-difference-between-machine-learning-supervised-and-unsupervised — Explicação técnica e oficial da AWS sobre os dois principais paradigmas de aprendizado.
3. **Characterizing Performance Bugs in Deep Learning Systems (arXiv, Cao et al., 2021)** — https://arxiv.org/abs/2112.01771 — Artigo científico que investiga bugs de performance em sistemas de Deep Learning (TensorFlow/Keras). Traz uma camada mais avançada e "de engenharia" ao caderno.
4. **Introduction to AI — KodeKloud** — https://notes.kodekloud.com/docs/Mastering-Generative-AI-with-OpenAI/What-is-Generative-AI/Introduction-to-AI/page — Introdução a IA, ML e Deep Learning, comparando programação tradicional com técnicas de machine learning.
5. **Machine Learning e Programação Tradicional: as diferenças — Primavera BSS** — https://pt.primaverabss.com/pt/blog/machine-learning-e-programacao-tradicional/ — Artigo em português comparando os dois paradigmas com exemplos práticos (classificação de imagens, reconhecimento de voz).
6. **Machine Learning Tradicional Vs Deep Learning: Qual É O Melhor? — Victor Alves (DIO)** — https://www.dio.me/articles/machine-learning-tradicional-vs-deep-learning-qual-e-o-melhor-9e1676dd5670 — Comparação direta entre ML tradicional e Deep Learning, com prós e contras de cada abordagem.
7. **Modelos Preditivos: O que São, Como Funcionam e Onde São Usados — Cetax** — https://cetax.com.br/modelos-preditivos/ — Explica o conceito de modelos preditivos e sua aplicação prática em empresas.
8. **Programa Bootcamp Machine Learning — turma 1 (.docx)** — material próprio do bootcamp/curso (arquivo local) — Conteúdo estruturado do programa de estudos que estou seguindo, usado como referência de currículo.
9. **Sistema Tutor Inteligente baseado em Aprendizado de Máquina para Ensino-aprendizagem de Manutenção de Software — UFU** — https://repositorio.ufu.br/handle/123456789/41374 — Trabalho acadêmico brasileiro aplicando ML a um sistema tutor inteligente, trazendo um caso de uso real e aprofundado.
10. **Traditional Programming vs Machine Learning: How They Compare — T-Gency** — https://t-gency.com/tech-education/traditional-programming-vs-machine-learning-how-they-compare/ — Mais uma comparação (em inglês) entre os dois paradigmas, útil para triangular definições com as fontes em português.

> 💡 Nota de curadoria: essa combinação mistura fontes introdutórias (Wikipédia, AWS, Primavera BSS), comparativas (DIO, T-Gency, KodeKloud) e uma fonte acadêmica mais avançada (arXiv, UFU) — o que permite perguntar ao NotebookLM tanto conceitos básicos quanto questões mais técnicas de engenharia de ML.

---

## 🧪 Engenharia de Prompts e "Cicatrizes"

Documentação do processo de refinamento das perguntas feitas ao NotebookLM — incluindo tentativas que não deram certo de primeira.

### 🩹 Cicatriz principal: perguntar antes de carregar as fontes

Na minha primeira rodada de testes, fiz todas as 5 perguntas estratégicas **antes de subir qualquer fonte** para o caderno no NotebookLM. Resultado: a ferramenta respondeu tudo com base em "conhecimento geral" (equivalente a um LLM genérico), e não com base nas fontes que eu havia curado — e, em toda resposta, o próprio NotebookLM avisou isso e sugeriu rodar uma pesquisa (*Fast Research*) para popular o caderno.

**Aprendizado:** o valor real do NotebookLM está em ancorar as respostas nas fontes carregadas (com citações rastreáveis). Sem isso, ele vira "só mais um chat de IA" — perde-se justamente a vantagem de curadoria que é o objetivo do desafio. A correção foi: primeiro fazer upload das 5 fontes no painel esquerdo, e só depois repetir as mesmas perguntas para comparar a diferença.

---

### Pergunta 1: O que é Machine Learning e como difere da programação tradicional?
- **Prompt v1 (sem fontes carregadas):** "O que é Machine Learning e como ele se diferencia da programação tradicional?"
- **Resposta obtida (v1):** Explicou por analogia — na programação tradicional o humano escreve as regras; em ML, o sistema aprende as regras a partir de exemplos rotulados (ex: e-mails marcados como spam).
- **Problema encontrado:** Resposta genérica, sem nenhuma citação das fontes curadas (Google MLCC, artigo do Domingos etc.), porque nenhuma fonte estava carregada ainda.
- **Prompt v2 (planejado, após carregar as fontes):** "Com base nas fontes carregadas, principalmente na Wikipédia e no artigo da Primavera BSS, explique o que é Machine Learning e como ele difere da programação tradicional. Cite de qual fonte vem cada parte da explicação."
- **Resultado esperado:** Resposta ancorada nas fontes, com citações que permitem checar a origem de cada afirmação.
- **Aprendizado:** Pedir explicitamente "com base nas fontes carregadas" + solicitar citação da origem é essencial para explorar o diferencial do NotebookLM.

### Pergunta 2: Tipos de aprendizado de máquina
- **Prompt v1 (sem fontes carregadas):** "Quais são os três principais tipos de aprendizado de máquina e qual a diferença entre eles?"
- **Resposta obtida (v1):** Definiu supervisionado, não supervisionado e por reforço com exemplos genéricos (filtro de spam, agrupamento de clientes, jogos/robótica).
- **Problema encontrado:** Mesma limitação — resposta correta tecnicamente, mas não vinculada às fontes específicas do caderno.
- **Prompt v2 (planejado):** "Baseado exclusivamente nas fontes carregadas, explique os três tipos de aprendizado de máquina e aponte em qual fonte cada tipo é discutido com mais profundidade."
- **Aprendizado:** Essa pergunta funciona bem mesmo sem fontes (conceito estável e bem consolidado), mas ganha valor de rastreabilidade quando ancorada.

### Pergunta 3: Comparação entre algoritmos (regressão, árvore de decisão, redes neurais)
- **Prompt v1 (sem fontes carregadas):** "Compare regressão linear, árvore de decisão e redes neurais em uma tabela: quando usar cada uma?"
- **Resposta obtida (v1):** Gerou uma tabela clara com "quando usar" e "principal vantagem" para os três modelos.
- **Problema encontrado:** Boa formatação, mas sem nenhuma citação — o NotebookLM avisou explicitamente que a resposta era baseada em conhecimento geral, não nas fontes.
- **Prompt v2 (planejado):** "Usando as fontes carregadas (especialmente os artigos da DIO e do T-Gency sobre ML tradicional vs. Deep Learning), monte uma tabela comparando regressão linear, árvore de decisão e redes neurais, indicando a fonte de cada informação."
- **Aprendizado:** Pedir formato de tabela funcionou bem de cara — vale manter esse padrão de prompt (formato + comparação) para outras perguntas.

### Pergunta 4: Erros comuns de iniciantes (a pergunta "difícil")
- **Prompt v1 (sem fontes carregadas):** "Baseado exclusivamente nas fontes carregadas, quais erros comuns um iniciante comete ao treinar seu primeiro modelo de Machine Learning?"
- **Resposta obtida (v1):** O NotebookLM **recusou-se a afirmar que a resposta vinha das fontes** (porque não havia nenhuma carregada) e foi transparente sobre isso, respondendo com conhecimento geral: overfitting, dados não tratados, vazamento de dados (data leakage).
- **Problema encontrado:** Esse foi o teste mais revelador — mesmo pedindo explicitamente "baseado exclusivamente nas fontes", o NotebookLM não inventou uma citação falsa; ele avisou a limitação. Isso mostra um comportamento positivo de transparência da ferramenta.
- **Prompt v2 (planejado, após carregar as fontes):** repetir o mesmo prompt e comparar se a resposta passa a citar, por exemplo, o artigo do arXiv sobre bugs de performance em sistemas de Deep Learning, ou o trabalho da UFU.
- **Aprendizado:** Um prompt bem escrito não substitui a fonte. A ordem das operações importa: **carregar fontes → depois perguntar**, nunca o contrário.

### Pergunta 5: Glossário de termos técnicos
- **Prompt v1 (sem fontes carregadas):** "Liste os 10 termos técnicos mais importantes mencionados nas fontes, com definição curta para cada um."
- **Resposta obtida (v1):** Gerou uma lista sólida de 10 termos (overfitting, dataset, algoritmo, features, target, hiperparâmetros, viés, variância, gradiente descendente, época) — mas eram termos gerais de ML, não necessariamente "mencionados nas fontes" (que ainda não existiam no caderno).
- **Problema encontrado:** A resposta é tecnicamente útil, mas contradiz o próprio prompt ("mencionados nas fontes") — sinal de que preciso validar depois se esses termos realmente aparecem nas 5 fontes curadas ou se preciso pedir a lista de novo já com as fontes carregadas.
- **Prompt v2 (planejado):** "Releia as fontes carregadas e liste apenas os termos técnicos que aparecem explicitamente nelas, com a definição usada por cada fonte."
- **Aprendizado:** Bom material bruto para o glossário, mas preciso re-executar com as fontes carregadas para garantir fidelidade ao conteúdo real do caderno (e não a conhecimento genérico do modelo).

---

**Próximo passo no processo:** carregar as 5 fontes da curadoria no painel do NotebookLM e repetir as 5 perguntas acima nas versões v2, registrando aqui as respostas finais com citações.

---

## 📘 Miniguia de Estudo (Entrega Final)

### 🧾 Resumos Estruturados

#### 1. O que é Machine Learning
_Resumo em suas próprias palavras, baseado nas fontes e nas respostas do NotebookLM._

#### 2. Tipos de Aprendizado
- **Supervisionado:** ...
- **Não supervisionado:** ...
- **Por reforço:** ...

#### 3. Fluxo de um Projeto de ML
1. Coleta e preparação dos dados
2. Divisão em treino/teste
3. Escolha e treinamento do modelo
4. Avaliação de métricas
5. Ajuste de hiperparâmetros
6. Deploy e monitoramento

#### 4. Principais Algoritmos
- **Regressão Linear/Logística:** ...
- **Árvores de Decisão / Random Forest:** ...
- **KNN:** ...
- **Redes Neurais:** ...

#### 5. Métricas de Avaliação
- **Acurácia:** ...
- **Precisão e Recall:** ...
- **F1-Score:** ...
- **RMSE / MAE (para regressão):** ...

---

### 📖 Glossário

- **Overfitting:** quando o modelo aprende demais os dados de treino e perde capacidade de generalizar.
- **Underfitting:** quando o modelo é simples demais para capturar os padrões dos dados.
- **Feature:** variável de entrada usada pelo modelo para fazer previsões.
- **Label (rótulo):** variável de saída que o modelo tenta prever (em aprendizado supervisionado).
- **Hiperparâmetro:** configuração definida antes do treinamento (ex: taxa de aprendizado).
- **Dataset:** conjunto de dados usado para treinar/testar o modelo.
- _Adicione outros termos conforme aprender_

---

### 🔁 Prompts Reutilizáveis para Revisão

- "Explique [conceito de ML] como se eu já soubesse programação mas nunca tivesse estudado Machine Learning."
- "Crie 5 perguntas de múltipla escolha sobre [tema] baseadas nas fontes carregadas neste caderno."
- "Compare [algoritmo A] e [algoritmo B] em uma tabela, destacando vantagens, desvantagens e casos de uso."
- "Resuma em 3 bullet points os pontos mais importantes sobre [tema] segundo as fontes."
- "Dê um exemplo prático de aplicação de [conceito] no mundo real."

---

## 🔗 Sobre este projeto

Projeto criado para o desafio **"Caderno Temático no NotebookLM"** da [DIO](https://www.dio.me/).

**Ferramenta utilizada:** [NotebookLM](https://notebooklm.google.com/)
**Autor(a):** _seu nome_
**Data:** _data de conclusão_
