# 🚀 Plano de Preparação para Entrevistas — Senior Java Backend Engineer

> **Para quem é isso:** Engenheiro sênior com sólida experiência real, que conhece o trabalho mas não performa bem sob pressão de entrevistas.  
> **Objetivo:** Máximo ROI em 6–8 semanas com ~10–12h/semana.  
> **Filosofia:** Você não está aprendendo — está *traduzindo* o que já sabe para o formato de entrevista.

---

## ⚡ Rotina Diária Template

> Use isso todos os dias, ajustando o bloco de estudo conforme a semana.

| Horário | Atividade |
|---|---|
| **Dia de semana (1h30)** | |
| 20 min | Revisão do dia anterior (flashcards / anotações) |
| 50 min | Bloco principal de estudo da semana |
| 20 min | "Explicar em voz alta" — escolha 1 conceito e grave/explique sem olhar |
| **Fim de semana (3h–4h)** | |
| 1h | Coding practice (LeetCode / HackerRank) |
| 1h30 | System design ou backend profundo |
| 30 min | Mock interview ou simulação de resposta |

> 💡 **Regra de ouro:** Toda sessão de estudo termina com você *falando* sobre o que aprendeu. Ler sem verbalizar não te prepara para entrevistas.

---

## 📅 Plano Completo — 8 Semanas

---

### 🗓️ SEMANA 1 — Fundação e Diagnóstico

**Meta:** Entender onde você está, estruturar o cérebro para "modo entrevista", eliminar o medo do desconhecido.

#### Tarefas da Semana

**Dias úteis (5 × 1h30):**

- [ ] **Dia 1:** Leia o capítulo 1 do *System Design Interview* (Alex Xu). Depois, tente desenhar do zero a arquitetura do Instagram. Não pesquise — use o que você já sabe.
  > ✅ *Resultado esperado:* Você consegue esboçar um diagrama com pelo menos 5 componentes (load balancer, API, DB, cache, storage) e identificar onde seu raciocínio teve lacunas — sem consultar nada.

- [ ] **Dia 2:** Revise JVM internals em alto nível: heap vs stack, GC generations, ClassLoader. Escreva uma "cheat sheet" de 1 página com suas palavras.
  > ✅ *Resultado esperado:* Você consegue explicar em 60 segundos o que acontece na memória quando um objeto é criado, usado e coletado pelo GC — sem travar, sem recorrer à cheat sheet.

- [ ] **Dia 3:** Resolva 3 problemas LeetCode nível Easy (Arrays/Strings). Foque em *verbalizar* cada passo em voz alta enquanto resolve.
  > ✅ *Resultado esperado:* Você completa os 3 problemas verbalizando sem silêncio prolongado. Mesmo errando a solução ótima, o raciocínio em voz alta fluiu sem pausas constrangedoras.

- [ ] **Dia 4:** Revise seu próprio CV. Para cada projeto, prepare uma resposta no formato STAR (Situação, Tarefa, Ação, Resultado) de 90 segundos. Grave e ouça.
  > ✅ *Resultado esperado:* Você tem ao menos 3 histórias STAR prontas, cada uma com menos de 2 minutos, que soam naturais e não genéricas. Ao ouvir a gravação, você não se sente travado nem vago.

- [ ] **Dia 5:** Revise HashMap internals em Java (hashing, colisões, load factor, resize). Explique em voz alta como se estivesse em entrevista.
  > ✅ *Resultado esperado:* Você consegue responder "Como o HashMap funciona internamente?" de forma fluida, cobrindo hash function, bucket array, linked list/tree em colisão e o que dispara o resize — sem consultar nada.

**Fim de semana (3h):**

- [ ] **1h:** Leia sobre o framework de system design (seção abaixo). Anote o checklist.
  > ✅ *Resultado esperado:* O framework de 5 etapas está anotado com suas palavras e você consegue recitá-lo de memória na ordem correta.

- [ ] **1h:** Mock interview pessoal: abra um timer, pegue uma pergunta de system design (ex: "Design a URL shortener") e resolva em 45 min falando em voz alta.
  > ✅ *Resultado esperado:* Você passou por todas as 5 etapas do framework (mesmo que superficialmente) dentro do tempo. Você sabe quais etapas foram fracas e o que precisa melhorar.

- [ ] **1h:** Liste suas 10 maiores lacunas de conhecimento — seja honesto.
  > ✅ *Resultado esperado:* Você tem uma lista real e priorizada de gaps — não genérica. Essa lista vai guiar o foco das próximas semanas.

#### Materiais
- 📖 *System Design Interview Vol. 1* — Alex Xu (capítulo 1–3)
- 📖 *Java Concurrency in Practice* — Brian Goetz (tenha em mãos, não precisa ler tudo agora)
- 🌐 [Java Memory Model — Baeldung](https://www.baeldung.com/java-stack-heap)
- 🎥 [TechDummies no YouTube — System Design Playlist](https://www.youtube.com/@TechDummiesNarendraL)

---

### 🗓️ SEMANA 2 — Java Core Profundo (Concorrência + Collections)

**Meta:** Consolidar os tópicos Java mais cobrados em entrevistas sênior. Não decorar — *entender e saber explicar*.

#### Tarefas da Semana

**Dias úteis (5 × 1h30):**

- [ ] **Dia 1:** **Concorrência Parte 1** — `synchronized`, `volatile`, `happens-before`. Escreva 2 exemplos de race conditions e corrija-os.
  > ✅ *Resultado esperado:* Você consegue escrever um exemplo de race condition real (sem copiar), explicar por que o problema ocorre e mostrar a correção com `synchronized` ou `volatile` — sabendo qual usar em cada caso.

- [ ] **Dia 2:** **Concorrência Parte 2** — `ExecutorService`, `Future`, `CompletableFuture`. Implemente um exemplo real: chamar 3 APIs em paralelo e agregar resultado.
  > ✅ *Resultado esperado:* Você tem um código funcional de chamadas paralelas com `CompletableFuture.allOf()` e consegue explicar cada linha — incluindo o que acontece se uma das chamadas falhar.

- [ ] **Dia 3:** **Concorrência Parte 3** — `ReentrantLock`, `Semaphore`, `CountDownLatch`, `CyclicBarrier`. Quando usar cada um? Prepare respostas de 60s para cada.
  > ✅ *Resultado esperado:* Para cada uma das 4 primitivas, você consegue dar um caso de uso real de produção em 60 segundos — sem hesitar nem confundir uma com a outra.

- [ ] **Dia 4:** **Collections** — ArrayList vs LinkedList, HashMap vs ConcurrentHashMap vs TreeMap. Por que ConcurrentHashMap não usa `synchronized` no objeto inteiro?
  > ✅ *Resultado esperado:* Você consegue responder "Qual Collection usar para X?" de forma justificada, incluindo a explicação de segment locking (Java 7) e CAS + bin locking (Java 8+) no ConcurrentHashMap.

- [ ] **Dia 5:** **Generics + Streams** — `Comparable` vs `Comparator`, uso de `Stream`, `Optional`. Resolva 3 exercícios de transformação de dados com Streams.
  > ✅ *Resultado esperado:* Você resolve os 3 exercícios de Streams sem consultar documentação e consegue explicar a diferença entre operações intermediárias e terminais — e por que Streams são lazy.

**Fim de semana (4h):**

- [ ] **1h30:** LeetCode — 2 problemas Medium (Two Pointers ou Sliding Window). Verbalize cada etapa.
  > ✅ *Resultado esperado:* Você resolve ao menos 1 dos 2 problemas sem consultar solução, verbalizando continuamente. Se travou, sabe nomear exatamente onde e por quê.

- [ ] **1h:** System design — "Design a Rate Limiter". Resolva seguindo o framework (seção abaixo).
  > ✅ *Resultado esperado:* Você passou pelas 5 etapas do framework, escolheu um algoritmo (Token Bucket ou Sliding Window Counter) e consegue justificar a escolha com trade-offs.

- [ ] **1h30:** Crie flashcards para todos os conceitos desta semana (Anki ou papel).
  > ✅ *Resultado esperado:* Você tem ao menos 15 flashcards criados com suas próprias palavras — e já testou a si mesmo neles antes de terminar a sessão.

#### Materiais
- 📖 *Java Concurrency in Practice* — Brian Goetz (Caps. 1–6)
- 🌐 [Guide to java.util.concurrent — Baeldung](https://www.baeldung.com/java-util-concurrent)
- 🌐 [Java Collections Overview — Baeldung](https://www.baeldung.com/java-collections)
- 📖 *Effective Java* — Joshua Bloch (itens sobre Generics e Concorrência)

#### Perguntas Comuns desta Semana
- "Como o ConcurrentHashMap funciona internamente?"
- "Qual a diferença entre `wait()`/`notify()` e `Lock`/`Condition`?"
- "Explique `volatile` e quando usá-lo."
- "O que é deadlock? Como prevenir?"

---

### 🗓️ SEMANA 3 — JVM + Spring + REST APIs

**Meta:** Ter um entendimento sólido e articulável da JVM e do ecosistema Spring usado no dia a dia.

#### Tarefas da Semana

**Dias úteis (5 × 1h30):**

- [ ] **Dia 1:** **JVM Deep Dive** — GC (G1, ZGC, Shenandoah), heap tuning, GC logs. Saiba explicar o que acontece quando há um GC pause em produção.
  > ✅ *Resultado esperado:* Você consegue descrever o ciclo de vida de um objeto no G1GC (Eden → Survivor → Old Gen) e explicar o que é um Stop-the-World pause — e quais flags JVM você usaria para investigar um problema de GC em produção.

- [ ] **Dia 2:** **JVM Continuação** — JIT compilation, class loading, PermGen vs Metaspace. Saiba explicar `OutOfMemoryError` e seus tipos.
  > ✅ *Resultado esperado:* Você consegue diferenciar os tipos de OOM (`Java heap space`, `GC overhead limit exceeded`, `Metaspace`) e dizer o que causa cada um — e como você investigaria em produção.

- [ ] **Dia 3:** **Spring Core** — IoC, DI, Bean lifecycle, `@Transactional` internals (proxy-based AOP). Saiba responder: "O que acontece se eu chamar um método `@Transactional` de dentro da mesma classe?"
  > ✅ *Resultado esperado:* Você explica de forma clara por que a chamada interna ao `@Transactional` não funciona (self-invocation bypasses the proxy) e sabe dizer pelo menos 2 formas de contornar o problema.

- [ ] **Dia 4:** **Spring Boot + REST** — autoconfiguration, filtros, interceptors, exception handling global (`@ControllerAdvice`). Saiba desenhar o ciclo de vida de uma request HTTP no Spring.
  > ✅ *Resultado esperado:* Você consegue desenhar (no papel ou whiteboard) o fluxo completo de uma request HTTP desde o Tomcat até o Controller e de volta — incluindo onde Filters, Interceptors e ExceptionHandlers atuam.

- [ ] **Dia 5:** **Segurança REST** — JWT, OAuth2 conceitos, Spring Security básico. Explique o fluxo de autenticação de uma API com JWT.
  > ✅ *Resultado esperado:* Você explica o fluxo JWT completo (login → geração do token → envio no header → validação no servidor) sem hesitar, incluindo o que está dentro do payload e por que o token não precisa de sessão no servidor.

**Fim de semana (3h):**

- [ ] **1h:** LeetCode — 1 problema Medium (BFS/DFS ou Binary Search).
  > ✅ *Resultado esperado:* Você resolve o problema verbalizando e consegue explicar a complexidade de tempo e espaço da sua solução sem ser perguntado — isso deve ser automático.

- [ ] **1h:** System design — "Design a Notification System".
  > ✅ *Resultado esperado:* Você cobre os canais (push, email, SMS), o papel de uma message queue (Kafka/SQS), fanout, e sabe explicar como garantir entrega e evitar duplicatas.

- [ ] **1h:** Simulação de entrevista técnica: peça para alguém te fazer perguntas aleatórias desta semana ou use o ChatGPT como entrevistador.
  > ✅ *Resultado esperado:* Você responde pelo menos 5 perguntas técnicas sem silêncio paralisante. Identifica quais respostas soaram vagas ou inseguras para trabalhar na semana seguinte.

#### Materiais
- 🌐 [Spring Framework Reference Documentation](https://docs.spring.io/spring-framework/reference/)
- 🌐 [Baeldung — Spring Guides](https://www.baeldung.com/spring-tutorial)
- 🎥 [Amigoscode — Spring Boot Tutorial](https://www.youtube.com/c/amigoscode)
- 🌐 [GC Tuning Guide — Oracle](https://docs.oracle.com/en/java/javase/17/gctuning/)

#### Perguntas Comuns desta Semana
- "Explique como o Spring resolve dependências circulares."
- "Como o `@Transactional` funciona? Quais são suas propagações?"
- "Qual a diferença entre `@Bean` e `@Component`?"
- "O que acontece quando uma exceção não é tratada dentro de um método `@Transactional`?"

---

### 🗓️ SEMANA 4 — Bancos de Dados + Performance

**Meta:** Dominar os tópicos de banco de dados que aparecem em todo tipo de entrevista sênior.

#### Tarefas da Semana

**Dias úteis (5 × 1h30):**

- [ ] **Dia 1:** **Indexes** — B-Tree vs Hash index, índices compostos, quando NÃO usar índice. Saiba explicar o plano de execução de uma query.
  > ✅ *Resultado esperado:* Você consegue explicar por que uma query com `LIKE '%texto'` não usa índice, o que é um index scan vs seq scan, e quando um índice composto ajuda ou atrapalha — com exemplos concretos.

- [ ] **Dia 2:** **Transactions** — ACID, níveis de isolamento (Read Uncommitted → Serializable), problemas: dirty read, phantom read, non-repeatable read.
  > ✅ *Resultado esperado:* Você consegue dar um exemplo concreto de cada problema (dirty read, phantom read, non-repeatable read) e dizer qual nível de isolamento o resolve — sem decorar tabela, entendendo o porquê.

- [ ] **Dia 3:** **Performance** — N+1 problem, query optimization, EXPLAIN/EXPLAIN ANALYZE (PostgreSQL). Analise uma query lenta e explique como você resolveria.
  > ✅ *Resultado esperado:* Você consegue identificar um N+1 num trecho de código Hibernate e propor a correção (JOIN FETCH, batch loading ou DTO projection) — justificando a escolha.

- [ ] **Dia 4:** **NoSQL vs SQL** — Quando usar cada um? CAP theorem aplicado. MongoDB vs Redis vs Cassandra — trade-offs.
  > ✅ *Resultado esperado:* Dado um cenário (ex: "sistema de sessões de usuário", "feed de atividades", "catálogo de produtos"), você escolhe a tecnologia certa e justifica usando CAP e características de acesso.

- [ ] **Dia 5:** **Connection Pooling + ORM** — HikariCP internals, JPA/Hibernate lazy vs eager loading, session management.
  > ✅ *Resultado esperado:* Você explica o que acontece quando o connection pool esgota em produção, como diagnosticar (métricas, logs, thread dump), e sabe a diferença entre `LazyInitializationException` e como preveni-la.

**Fim de semana (4h):**

- [ ] **1h:** LeetCode — 2 problemas Medium (Strings ou DP simples).
  > ✅ *Resultado esperado:* Ao menos 1 resolvido sem consultar solução. Para o que não conseguiu, você consegue explicar onde travou e qual padrão faltou reconhecer.

- [ ] **1h30:** System design — "Design Twitter's Timeline Feed".
  > ✅ *Resultado esperado:* Você cobre o modelo fan-out (push vs pull vs híbrido), o papel do cache na timeline, e sabe explicar por que a abordagem muda para usuários com milhões de seguidores.

- [ ] **1h30:** Revise semanas 1–4. Identifique os 3 tópicos em que ainda está inseguro. Foque o estudo de domingo neles.
  > ✅ *Resultado esperado:* Você tem 3 tópicos específicos identificados (não genéricos como "concorrência" — mas algo como "não me sinto seguro explicando segment locking do ConcurrentHashMap") e um micro-plano de como vai revisá-los.

#### Materiais
- 📖 *Designing Data-Intensive Applications* — Martin Kleppmann (caps. 3, 7)
- 🌐 [Use The Index, Luke — SQL Indexes Guide](https://use-the-index-luke.com/)
- 🌐 [Baeldung — JPA/Hibernate](https://www.baeldung.com/hibernate-5-spring)
- 🎥 [Hussein Nasser — Database Engineering no YouTube](https://www.youtube.com/@hnasr)

#### Perguntas Comuns desta Semana
- "O que é um índice e como o banco de dados o usa internamente?"
- "Explique os 4 níveis de isolamento de transação."
- "O que é o problema N+1 e como resolver?"
- "Quando você usaria Redis ao invés de um banco relacional?"

---

### 🗓️ SEMANA 5 — System Design Intensivo

**Meta:** Ter um framework confiante e repetível para qualquer pergunta de system design.

#### Framework de System Design (USE SEMPRE NESTA ORDEM)

```
1. CLARIFY (5 min)
   - Quantos usuários? Reads vs Writes? Latência aceitável?
   - Funcionalidades obrigatórias vs opcionais?
   - Escala: 1k req/s? 100k?

2. ESTIMATE (2–3 min)
   - DAU (Daily Active Users)
   - QPS (Queries per Second)
   - Storage necessário
   - Bandwidth

3. HIGH-LEVEL DESIGN (10 min)
   - Desenhe os componentes principais
   - Mostre fluxo de dados
   - Identifique pontos de falha

4. DEEP DIVE (15 min)
   - Banco de dados: schema, índices
   - Cache: onde, TTL, invalidação
   - Escalabilidade: horizontal scaling, sharding
   - Reliability: replication, failover

5. TRADE-OFFS (5 min)
   - O que você sacrificou? Por quê?
   - O que você faria diferente com mais tempo?
```

#### Tarefas da Semana

**Dias úteis (5 × 1h30):**

- [ ] **Dia 1:** "Design a URL Shortener" — resolva aplicando o framework acima. Grave em vídeo ou áudio.
  > ✅ *Resultado esperado:* Ao rever a gravação, você passou pelas 5 etapas na ordem certa, estimou QPS de forma razoável, escolheu o banco de dados com justificativa e discutiu pelo menos 1 trade-off real.

- [ ] **Dia 2:** "Design Instagram" — foque no feed e upload de imagens. Identifique CDN, object storage, database.
  > ✅ *Resultado esperado:* Você consegue explicar por que object storage (S3-like) é usado para imagens e não o banco relacional, como o CDN reduz latência e onde o cache de feed se encaixa na arquitetura.

- [ ] **Dia 3:** "Design a Chat System (WhatsApp)" — foque em WebSockets, message delivery, online presence.
  > ✅ *Resultado esperado:* Você explica a diferença entre polling, long-polling e WebSockets, por que WebSocket é a escolha certa aqui, e como garantir entrega de mensagem quando o destinatário está offline.

- [ ] **Dia 4:** "Design YouTube" — foque em upload, processamento de vídeo (encoding), streaming, CDN.
  > ✅ *Resultado esperado:* Você descreve o fluxo de upload → processamento assíncrono → múltiplas resoluções → CDN, e explica por que o processamento de vídeo é separado do fluxo de request do usuário (async job queue).

- [ ] **Dia 5:** Revise os 4 designs. Quais componentes aparecem sempre? (Load balancer, CDN, Cache, Message Queue, DB replication). Domine esses.
  > ✅ *Resultado esperado:* Você monta uma lista pessoal de "componentes universais" com a função de cada um e consegue encaixá-los em qualquer design novo em menos de 2 minutos — sem precisar pensar do zero.

**Fim de semana (4h):**

- [ ] **2h:** Mock interview de system design com parceiro ou usando Pramp.com.
  > ✅ *Resultado esperado:* Você recebe feedback externo sobre pelo menos 1 ponto fraco concreto (ex: "você pulou os requisitos", "não falou sobre falhas"). Isso vale mais do que qualquer leitura.

- [ ] **2h:** LeetCode — 2 problemas Medium + revisão de estruturas de dados essenciais.
  > ✅ *Resultado esperado:* Você resolve verbalizando e, ao final, consegue categorizar o padrão de cada problema (Two Pointers? BFS? HashMap?) — reconhecer o padrão é mais valioso do que resolver na força bruta.

#### Materiais
- 📖 *System Design Interview Vol. 1 e 2* — Alex Xu (leitura completa agora)
- 🌐 [Grokking the System Design Interview — Educative.io](https://www.educative.io/courses/grokking-the-system-design-interview)
- 🌐 [ByteByteGo Newsletter + YouTube](https://www.youtube.com/@ByteByteGo)
- 🌐 [High Scalability Blog](http://highscalability.com/)

#### Perguntas para Praticar
1. Design a URL Shortener
2. Design Twitter
3. Design WhatsApp
4. Design YouTube
5. Design Uber
6. Design a Rate Limiter
7. Design a Search Autocomplete System
8. Design a Notification System
9. Design a Distributed Cache
10. Design a News Feed

---

### 🗓️ SEMANA 6 — Messaging, Cache e Microsserviços

**Meta:** Consolidar os tópicos que diferenciam candidatos mid de senior.

#### Tarefas da Semana

**Dias úteis (5 × 1h30):**

- [ ] **Dia 1:** **Kafka** — topics, partitions, consumer groups, offsets, at-least-once vs exactly-once. Saiba explicar: "Por que Kafka é tão rápido?"
  > ✅ *Resultado esperado:* Você explica por que Kafka usa append-only log em disco (sequencial é rápido), o papel das partitions para paralelismo e a diferença prática entre at-least-once e exactly-once — com quando usar cada um.

- [ ] **Dia 2:** **Cache** — cache-aside vs write-through vs write-behind. Cache invalidation. Redis data structures e quando usar cada uma.
  > ✅ *Resultado esperado:* Dado um cenário (ex: "contador de likes", "sessão de usuário", "ranking em tempo real"), você escolhe a estrutura Redis certa (String, Hash, Sorted Set, etc.) e a estratégia de cache com justificativa — sem hesitar.

- [ ] **Dia 3:** **Microsserviços** — patterns: Circuit Breaker, Saga, API Gateway, Service Mesh. Saiba explicar distributed transactions sem 2PC.
  > ✅ *Resultado esperado:* Você explica o padrão Saga (coreografia vs orquestração), por que 2PC é problemático em sistemas distribuídos, e como o Circuit Breaker previne cascading failures — com um exemplo real de produção.

- [ ] **Dia 4:** **Observabilidade** — logs, metrics, traces (OpenTelemetry). Como você debugaria um problema de latência em produção?
  > ✅ *Resultado esperado:* Você consegue descrever uma metodologia de investigação de latência (métricas de p99, distributed tracing para encontrar o gargalo, logs correlacionados por trace ID) — como se estivesse explicando para o entrevistador um incidente real que resolveu.

- [ ] **Dia 5:** **Resiliência** — idempotência, retry com exponential backoff, bulkhead pattern. Implemente um exemplo simples de retry em Java.
  > ✅ *Resultado esperado:* Você tem um código de retry com exponential backoff + jitter funcionando, e consegue explicar por que o jitter é importante — e o que é idempotência e por que ela é pré-requisito para retry seguro.

**Fim de semana (3h):**

- [ ] **1h:** System design — "Design a Distributed Cache (Redis-like)".
  > ✅ *Resultado esperado:* Você cobre consistent hashing para distribuição de chaves, o que acontece quando um nó cai (rehashing, replication), e discute eviction policies (LRU, LFU) com trade-offs.

- [ ] **1h:** LeetCode — 2 problemas (qualquer dificuldade, foco em verbalization).
  > ✅ *Resultado esperado:* Você não ficou em silêncio por mais de 15 segundos em nenhum momento. O foco aqui é o hábito de verbalizar — não a correção da solução.

- [ ] **1h:** Simulação de entrevista completa (45 min) — grave e assista.
  > ✅ *Resultado esperado:* Ao assistir a gravação, você identifica pelo menos 2 momentos onde soou inseguro ou vago — e já sabe o que diria diferente. Isso é crescimento concreto.

#### Materiais
- 📖 *Designing Data-Intensive Applications* — Martin Kleppmann (cap. 11 — Streams)
- 🌐 [Confluent — Kafka Architecture](https://developer.confluent.io/learn-kafka/)
- 🌐 [Redis Documentation — Data Types](https://redis.io/docs/data-types/)
- 🌐 [microservices.io — Patterns](https://microservices.io/patterns/)
- 🎥 [Confluent no YouTube](https://www.youtube.com/@Confluent)

---

### 🗓️ SEMANA 7 — Coding + Comunicação sob Pressão

**Meta:** Estabilizar o desempenho em live coding. Não ser excelente — ser *consistente*.

#### A Verdade sobre Live Coding para Sêniors

Você não precisa resolver o problema mais rápido. Você precisa **não travar**. O entrevistador quer ver:
1. Como você pensa em voz alta
2. Se você faz perguntas antes de codar
3. Se você conhece trade-offs
4. Se você sabe analisar complexidade

#### Protocolo Anti-Freeze para Live Coding

```
1. Antes de escrever qualquer código:
   "Deixa eu garantir que entendi o problema..."
   → Repita o problema com suas palavras
   → Confirme o output esperado com exemplos

2. Pense em voz alta:
   "Minha primeira abordagem seria... mas isso seria O(n²)..."
   "Posso melhorar usando..."

3. Se travar:
   "Deixa eu pensar por um segundo..."
   → Comece pela força bruta. Sempre.
   → Depois otimize.

4. Se não souber:
   "Não estou 100% certo da solução ótima, mas posso começar com..."
```

#### Tarefas da Semana

**Dias úteis (5 × 1h30):**

- [ ] **Dia 1:** Two Pointers — 3 problemas. Verbalize cada um.
  > ✅ *Resultado esperado:* Você reconhece o padrão Two Pointers antes de começar a codar — não depois de tentar força bruta. O sinal: "dois índices que se movem para encontrar uma condição" dispara automaticamente.

- [ ] **Dia 2:** Sliding Window — 3 problemas. Verbalize cada um.
  > ✅ *Resultado esperado:* Você identifica quando um problema de substring/subarray é Sliding Window (janela contígua, tamanho variável ou fixo) e consegue estruturar o código com o padrão correto sem consultar exemplos.

- [ ] **Dia 3:** HashMaps / Sets — 3 problemas (frequência, anagramas, etc.)
  > ✅ *Resultado esperado:* Sua primeira reação a problemas de frequência, lookup O(1) ou "já vi esse valor antes?" é instintivamente "HashMap/Set". Você não chega mais nessa solução pela força bruta.

- [ ] **Dia 4:** Trees (BFS/DFS) — 2 problemas. Foque em entender o padrão, não decorar.
  > ✅ *Resultado esperado:* Você distingue quando usar BFS (largura, nível a nível, menor caminho) vs DFS (profundidade, exploração completa) e consegue implementar os dois sem consultar template.

- [ ] **Dia 5:** Simulação completa de live coding com timer: 45 min, 1 problema Medium, verbalizando tudo.
  > ✅ *Resultado esperado:* Você aplicou o Protocolo Anti-Freeze do início ao fim — fez perguntas antes, verbalizou o raciocínio, começou pela força bruta e tentou otimizar. O critério não é resolver: é não travar.

**Fim de semana (4h):**

- [ ] **2h:** Mock interview completo (Pramp, Interviewing.io, ou com colega).
  > ✅ *Resultado esperado:* Você recebe pelo menos 1 feedback específico de um humano — não de você mesmo. Feedback externo vale 10x mais do que auto-avaliação nesta fase.

- [ ] **1h:** Revisão geral — releia suas cheat sheets de todas as semanas.
  > ✅ *Resultado esperado:* Você identifica os 3 tópicos que ainda geram insegurança e já tem um plano de 30 minutos cada para reforçá-los na Semana 8.

- [ ] **1h:** System design — "Design Uber Surge Pricing System".
  > ✅ *Resultado esperado:* Você cobre coleta de dados em tempo real (geolocalização, demanda), processamento de stream (Kafka + Flink/Spark), e o mecanismo de atualização dinâmica de preço — com as latências envolvidas.

#### Materiais
- 🌐 [LeetCode — Top Interview Questions](https://leetcode.com/problemset/top-interview-questions/)
- 🌐 [NeetCode — Roadmap e Soluções](https://neetcode.io/roadmap)
- 📖 *Cracking the Coding Interview* — Gayle McDowell (apenas caps. de estratégia, não todos os problemas)
- 🌐 [Pramp — Mock Interviews Gratuitos](https://www.pramp.com/)

---

### 🗓️ SEMANA 8 — Simulação Intensiva e Refinamento Final

**Meta:** Consolidar tudo. Praticar em condições reais de entrevista.

#### Tarefas da Semana

**Dias úteis (5 × 1h30):**

- [ ] **Dia 1:** Mock interview completa — sistema de design (45 min) + 1 pergunta de Java (15 min).
  > ✅ *Resultado esperado:* Você não pulou nenhuma etapa do framework de system design. A pergunta Java foi respondida com estrutura clara (conceito → por que existe → quando usar → trade-off). Nenhuma resposta ficou em aberto sem você fechar.

- [ ] **Dia 2:** Mock interview completa — live coding (45 min) + behavioral (15 min).
  > ✅ *Resultado esperado:* No coding, você verbalizou do início ao fim sem silêncio longo. No behavioral, suas respostas STAR tiveram resultado mensurável e não foram vagas. Você não disse "eu acho" ou "não tenho certeza" sem complementar com raciocínio.

- [ ] **Dia 3:** Revisão das perguntas que mais te geraram dúvida nas semanas anteriores.
  > ✅ *Resultado esperado:* Os tópicos que antes geravam insegurança agora têm uma resposta de 60–90 segundos fluida — não perfeita, mas sólida o suficiente para não travar numa entrevista real.

- [ ] **Dia 4:** Mock interview completa — simulação de painel (3 perguntas técnicas diferentes em sequência).
  > ✅ *Resultado esperado:* Você mantém energia e clareza do início ao fim das 3 perguntas. O cansaço mental não degradou a qualidade das respostas — esse é o músculo que você está treinando aqui.

- [ ] **Dia 5:** Revisão leve + preparação mental. Sem estudo pesado.
  > ✅ *Resultado esperado:* Você relê suas cheat sheets com leveza — para lembrar, não para aprender. Você termina o dia confiante, não ansioso. Sua preparação está feita.

**Fim de semana (2h):**

- [ ] Revise suas cheat sheets e anotações.
  > ✅ *Resultado esperado:* Você fecha o caderno sentindo que o conteúdo já está internalizado — não que precisa estudar mais.

- [ ] Descanse. Você está pronto.
  > ✅ *Resultado esperado:* Você descansou de verdade. Descanso antes de uma entrevista é parte da performance — não negligência.

---

## ⚡ Plano Mínimo Efetivo — 4 Semanas

> Se você tem apenas 1 mês, faça EXATAMENTE isso:

| Semana | Foco |
|---|---|
| **Semana 1** | Diagnóstico + JVM básico + Collections + 5 problemas LeetCode Easy |
| **Semana 2** | Concorrência Java + Banco de dados (indexes + transactions) + 1 system design |
| **Semana 3** | System Design intensivo (3 designs completos com framework) + Spring core |
| **Semana 4** | Mocks, mocks, mocks. 1 mock interview por dia. Nenhum tópico novo. |

---

## 🎯 Tópicos de Alto Retorno (Maior ROI)

Estes tópicos aparecem em quase toda entrevista sênior Java e custam relativamente pouco tempo para dominar:

### Java Core
1. `ConcurrentHashMap` internals e comparação com `HashMap`
2. `@Transactional` — propagação, rollback, proxy interno
3. `CompletableFuture` — encadeamento, exception handling
4. GC — tipos, tuning básico, o que fazer quando há leak de memória
5. `volatile` vs `AtomicInteger` vs `synchronized`

### Backend / System Design
6. Cache invalidation strategies (the hardest problem in CS)
7. Database indexing — quando ajuda e quando atrapalha
8. Níveis de isolamento de transação + problemas associados
9. Kafka — partitions, consumer groups, ordering guarantees
10. Rate limiting — Token Bucket vs Leaky Bucket vs Sliding Window

### Coding (mínimo suficiente)
11. Two Pointers
12. Sliding Window
13. HashMap para frequência e lookup
14. BFS para grafos/árvores
15. Binary Search aplicado

---

## ❌ Por Que Engenheiros Experientes Falham em Entrevistas

### Erro 1: Confundir "saber fazer" com "saber explicar"
Você resolve problemas complexos no trabalho todo dia — mas nunca precisou articular seu raciocínio em tempo real. Entrevistas são performances, não exames de competência.

**Solução:** Toda sessão de estudo termina com você explicando o conceito em voz alta, sem olhar as anotações.

### Erro 2: Querer mostrar que sabe tudo
Sêniors às vezes over-engineer respostas, divagam, ou tentam impressionar com complexidade desnecessária. Entrevistadores querem clareza e estrutura.

**Solução:** Responda primeiro com o básico sólido, depois expanda se perguntado.

### Erro 3: Silêncio em live coding
O maior erro. Ficar em silêncio enquanto pensa parece incompetência. Mesmo que não saiba a resposta, pensar em voz alta demonstra raciocínio.

**Solução:** Treine o protocolo anti-freeze até virar hábito.

### Erro 4: Subestimar system design
Muitos sêniors acham que vão "improvisar" system design. Sem um framework repetível, você perde pontos mesmo conhecendo os componentes.

**Solução:** Use o framework das 5 etapas religiosamente nas últimas 3 semanas.

### Erro 5: Conhecimento fragmentado sem fio condutor
Você conhece Kafka, Redis, microserviços — mas não consegue conectar esses pontos numa narrativa coerente.

**Solução:** Ao estudar cada tópico, sempre pergunte: "Quando eu usaria isso? Quais são os trade-offs?"

### Erro 6: Não praticar em condições reais
Ler artigos e resolver LeetCode em casa é muito diferente de performar ao vivo com um entrevistador te observando.

**Solução:** A partir da semana 5, toda prática deve ser em formato mock interview com timer.

---

## 💬 Comunicação e Confiança sob Pressão

### Como Soar como Sênior

| ❌ Junior diz... | ✅ Sênior diz... |
|---|---|
| "Eu acho que funciona assim..." | "A minha entendimento é que... e posso explicar o porquê." |
| "Não sei." | "Não tenho certeza agora, mas minha intuição seria... O que eu faria é..." |
| "Tem várias formas de fazer." | "Dependendo dos requisitos, as opções principais são X e Y. Minha recomendação seria X porque..." |
| Resolve sem perguntar | "Antes de começar, deixa eu confirmar alguns requisitos..." |
| Entra em detalhe sem contexto | "Em alto nível, a solução é X. Posso entrar em detalhe em qualquer parte." |

### Como Responder Quando Não Sabe

```
Opção 1 — Admita e raciocine:
"Não tenho essa resposta na ponta da língua, mas posso raciocinar sobre isso...
[pense em voz alta]
...então minha melhor estimativa seria X."

Opção 2 — Reframe para o que você sabe:
"Não trabalhei diretamente com isso, mas sei que [conceito relacionado].
Por analogia, diria que..."

Opção 3 — Seja honesto com contexto:
"Isso é algo que eu resolveria consultando a documentação em produção,
mas os princípios que eu aplicaria seriam..."
```

### Técnicas Anti-Ansiedade

1. **Pausa intencional:** Ao receber uma pergunta difícil, diga "deixa eu pensar por um segundo" antes de responder. Isso não é fraqueza — é deliberação.
2. **Âncoras físicas:** Antes da entrevista, 2 minutos de respiração profunda (4-7-8: inspira 4s, segura 7s, expira 8s).
3. **Power pose:** 2 minutos em posição de poder antes da entrevista (comprovado por Amy Cuddy — reduz cortisol).
4. **Reframe:** Você não está sendo julgado. Você está *avaliando* se a empresa é boa pra você. Isso muda o equilíbrio de poder mentalmente.
5. **Anchoring no que você sabe:** Se travar numa pergunta, pivote: "Deixa eu dar um exemplo de como lidei com algo similar em produção..."

---

## 📚 Biblioteca de Recursos Essenciais

### Livros (Ordem de Prioridade)
1. 📖 **System Design Interview Vol. 1 e 2** — Alex Xu *(obrigatório)*
2. 📖 **Designing Data-Intensive Applications** — Martin Kleppmann *(o melhor livro de backend existente)*
3. 📖 **Java Concurrency in Practice** — Brian Goetz *(referência definitiva)*
4. 📖 **Effective Java** — Joshua Bloch *(para soar como especialista Java)*
5. 📖 **Clean Code** — Robert Martin *(útil para code review e discussões)*

### Sites e Plataformas
- 🌐 [NeetCode.io](https://neetcode.io) — melhor curadoria de LeetCode por padrão
- 🌐 [ByteByteGo.com](https://bytebytego.com) — sistema design visual e direto
- 🌐 [Baeldung.com](https://baeldung.com) — Java/Spring de qualidade
- 🌐 [Pramp.com](https://pramp.com) — mock interviews gratuitos
- 🌐 [Interviewing.io](https://interviewing.io) — mock interviews com engenheiros reais
- 🌐 [High Scalability](http://highscalability.com) — casos reais de empresas

### YouTube
- 🎥 **ByteByteGo** — system design visual
- 🎥 **TechDummies Narendra L** — system design explicado
- 🎥 **NeetCode** — LeetCode com explicação de padrões
- 🎥 **Hussein Nasser** — backend e banco de dados profundo
- 🎥 **Amigoscode** — Spring Boot hands-on

---

## 📋 Perguntas Mais Comuns — Senior Java Backend

### JVM / Core Java
- Como o Garbage Collector funciona? Qual a diferença entre G1 e ZGC?
- O que é o Java Memory Model? O que é happens-before?
- Explique `volatile`. Quando usar em vez de `synchronized`?
- Como o `ClassLoader` funciona? O que é delegation model?
- O que são soft references, weak references e phantom references?

### Concorrência
- Qual a diferença entre `Callable` e `Runnable`?
- Como o `CompletableFuture` funciona? Como encadear operações?
- O que é deadlock? Como detectar e prevenir?
- Explique `ReentrantLock` vs `synchronized`.
- O que é thread starvation?

### Spring
- Como o Spring resolve injeção de dependências?
- Explique os escopos de Bean: singleton, prototype, request, session.
- Como o `@Transactional` funciona internamente (AOP proxy)?
- O que acontece se eu chamar um método `@Transactional` internamente?
- Como configurar segurança em uma API REST com Spring Security?

### Banco de Dados
- Explique os 4 níveis de isolamento de transação.
- O que é um índice B-Tree? Quando ele ajuda? Quando atrapalha?
- O que é o problema N+1? Como resolver?
- Qual a diferença entre sharding e replication?
- Quando usar NoSQL ao invés de SQL?

### System Design
- Design a URL shortener.
- Design a rate limiter.
- Design the Twitter/Instagram feed.
- Design a notification system.
- Design a distributed cache.

---

## ✅ Checklist Semanal de Progresso

Use isso toda sexta-feira para avaliar a semana:

- [ ] Estudei todos os dias planejados?
- [ ] Verbalizei em voz alta pelo menos 1 conceito por dia?
- [ ] Fiz pelo menos 1 simulação de entrevista esta semana?
- [ ] Criei flashcards dos conceitos novos?
- [ ] Identifiquei os 2–3 pontos mais fracos que preciso revisar?

---

> **Lembre-se:** Você já tem o conhecimento. O plano é transformar esse conhecimento em performance confiante sob pressão. Entrevistas são uma habilidade separada — e habilidades se treinam.

---

*Plano gerado para: Senior Java Backend Engineer | 6–8 semanas | ~10–12h/semana*
