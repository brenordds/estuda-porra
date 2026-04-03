## Hashmap

Definições
- O(1): tempo constante para busca (por ex: acessar item de array pelo indice). Significa que n muda mesmo que o tamanho cresça.
- O(n): tempo degrada quanto mais itens dentro (por ex: percorrer array em busca de item)

O que é?
- Array de buckets. Cada posição da array pode guardar n itens (caso ocorra colisão).
- Ao inserir algo num hashmap, ele chama hashCode() e usa função de espalhamento para melhorar distribuição dos itens. Assim calcula o indice dentro da array (usando bitwise, por isso tamanho da array sempre é potência de 2)
- É O(1) pq n percorre a array inteira (pode ser O(n) dentro dos buckets em caso de colisão, mas bem menos q array normal obviamente, nesse caso vira uma lista encadeada, mas a **a partir do java 8 se cresce demais (geralmente 8) vira árvore balanceada**).
- Loadsize padrão é 0.75. (o quão cheio o hashmap precisa estar cheio antes de um resize). É custoso pq recria array, recalcula posição de todo mundo, O(n).

## Synchronized, volatile e happens-before

Problemas que isso resolve: visibilidade (thread muda, outra n enxerga), race condition

- Synchronized: mete o lock no negócio e só 1 thread pode mexer, mudanças visiveis para as outras
	- Quando usar: várias threads mexendo num estado e consistência ncessária.
	- Não usar: operações frequentes ou só precisa de leitura simples
- Volatile: assegura leitura e escrita atômica e visibilidade imediata
	- Quando usar: comunicação entre threads, flags e estados simples de leitura
	- Não usar: contadores, lógica complexa

## ExecutorService, Future, CompletableFuture

```java
- ExecutorService = cozinha (onde os pratos são preparados)
- Threads = cozinheiros
- CompletableFuture = pedido que você fez
- allOf = esperar todos os pratos ficarem prontos
- join = pegar o prato pronto


🧵 EXECUTORSERVICE

👉 “A cozinha com número limitado de cozinheiros”

ExecutorService executor = Executors.newFixedThreadPool(3);

✔ controla quantas tarefas rodam ao mesmo tempo
✔ reutiliza threads (não cria toda hora)


📦 FUTURE (antigo)

👉 “Você faz o pedido e fica parado esperando”

Future<String> future = executor.submit(() -> getUser());

String user = future.get(); // BLOQUEIA


🚀 COMPLETABLEFUTURE (moderno)

👉 “Você faz o pedido e continua vivendo — quando ficar pronto, você usa”

CompletableFuture<String> future =
    CompletableFuture.supplyAsync(() -> getUser(), executor);

future.thenApply(user -> user.toUpperCase());

✔ não bloqueia (por padrão)
✔ permite encadear ações
✔ ideal para paralelismo


⚡ CHAMADAS EM PARALELO

👉 “Pedir vários pratos ao mesmo tempo”

CompletableFuture<String> user =
    CompletableFuture.supplyAsync(() -> getUser(), executor);

CompletableFuture<String> orders =
    CompletableFuture.supplyAsync(() -> getOrders(), executor);

CompletableFuture<String> recs =
    CompletableFuture.supplyAsync(() -> getRecs(), executor);


🔗 ALLOF (esperar tudo)

👉 “Esperar todos os pratos ficarem prontos”

CompletableFuture<Void> all =
    CompletableFuture.allOf(user, orders, recs);


🍽️ AGREGANDO RESULTADO

👉 “Juntar todos os pratos na mesa”

CompletableFuture<String> result =
    all.thenApply(v -> {
        return user.join() + " | " +
               orders.join() + " | " +
               recs.join();
    });


⏳ JOIN

👉 “Pegar o prato pronto (ou dar erro)”

String finalResult = result.join();


💥 ERRO (IMPORTANTE)

👉 “Se um prato der ruim, a refeição inteira pode falhar”

Se alguma future falhar:
- allOf falha
- join lança CompletionException

✔ tratar com fallback:

CompletableFuture<String> orders =
    CompletableFuture.supplyAsync(() -> getOrders(), executor)
        .exceptionally(ex -> "fallback-orders");
```

## ReentrantLock, Semaphore, CountDownLatch, CyclicBarrier

- ReentrantLock: faz lock() e unlock() de trechos de código para serem executados apenas por uma thread por vez. (diferença pra synchronized: tenta sem travar (tryLock), tem timeout e mais flexibilidade).
- Semaphore: controla a quantidade de threads que podem estar ali (acquire() e release())
- CountDownLatch: espera o numero de threads terminarem
- CyclicBarrier: espera todas threads chegarem em determinado ponto

## Arrays avançadas

- ArrayList: a array dinâmica (int[])
	- elementos ficam contíguos na memoria. acesso por indice é direto (get(index) O(1)).
	- inserir/remover no meio é lento. add no final geralmente é rápido.
- LinkedList: cada elemento linka pra o próximo (e pra o anterior)
	- precisa percorrer pra achar posicao (O(n))
	- inserir/remover no meio rapido (se ja tiver no)
	- maior overhead de memoria
- TreeMap: mantem a ordem das chaves
	- operacoes O(log n)
- ConcurrentHashMap: um hashmap thread safe performatico.
	- quebra mapa em segmentos, cada um com seu proprio lock

## Generic + Streams (bom dominar)

- Comparable: interface que classe implementa (em seguida faz override do metodo compareTo que explica como comparar instancia da classe com outra).
```java
class Pessoa implements Comparable<Pessoa> {
    String nome;
    int idade;

    @Override
    public int compareTo(Pessoa outra) {
        return Integer.compare(this.idade, outra.idade);
    }
}
```
- Comparator: mais flexivel, chamado direto no objeto, pode ter varios criterios de ordenacao.
```java
Comparator<Pessoa> porNome = Comparator.comparing(p -> p.nome);
```
### Streams

- Processar coleções declarativamente: você descreve o que quer, não como fazer.
```java
lista.stream()  
.filter(x -> x > 10) // intermediária  
.map(x -> x * 2) // intermediária  
.forEach(System.out::println); // terminal
```
- Operações
	- Intermediárias: **filter, map, sorted**
		- Não executam nada
		- Retornam outro stream
	- Terminais: **foreach, collect, count**
		- disparam execução
- Streams são lazy (só executa tudo quando chega numa operação terminal, exemplo: colocar instruções dentro de um filter e não chamar uma operação terminal n vai executar, só vai executar quando chamar naquele stream uma operação terminal)