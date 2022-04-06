---
title: 〰️ Notazione Lineare
author: Simone Fidanza
type: notes
meta:
    tags:
        - Anno I
        - Semestre I
        - INF/01
    docente: Fabio Abbattista
    contatto: fabio.abbattista@uniba.it, fabbattista@gmail.com
---

# Notazione Lineare

## Algoritmo

Chiamiamo algoritmo un metodo risolutivo per un problema, descritto da un insieme di operazioni elementari o istruzioni.

In altre parole un algoritmo è una sequenza finita di passi elementari che definiscono un procedimento mediante il quale è possibile risolvere un problema.

Un passo elementare è chiamato anche operazione elementare, oppure azione elementare, oppure istruzione.

---

## Operazione elementare

Una operazione è elementare se:

-   È interpretata in modo univoco dall'esecutore;
-   È direttamente eseguita dall'esecutore.

**Cioè l'esecutore comprende in modo univoco che cosa deve fare e sa come farlo.**

Il concetto di operazione elementare è abbastanza soggettivo. Sarebbe meglio descrivere un'operazione elementare dicendo che l'esecutore deve capire l'istruzione (o operazione). Se l'esecutore non comprende l'operazione, allora essa non è elementare.

---

## Proprietà di un algoritmo

Un algoritmo gode necessariamente delle seguenti proprietà:

1. **Non-ambiguità:** ogni operazione descritta deve essere univocamente interpretabile dall'esecutore;
2. **Eseguibilità:** l'esecutore deve essere in grado di eseguire ogni operazione in un tempo finito;
3. **Finitezza:** per ogni insieme di dati d'ingresso, il numero totale di operazioni deve essere finito;
4. **Generalità:** deve produrre un risultato per ogni valore attribuito ai dati iniziali, cioè deve risolvere tutti i problemi di una stessa classe.

La prima proprietà afferma che leggendo l'algoritmo **non** ci deve essere possibilità d'interpretare cosa vi è scritto, esso deve essere chiaro. Nel caso in cui l'algoritmo venga interpretato in maniera diversa da più esecutori, l'algoritmo non può essere considerato tale.

La seconda proprietà afferma che l'algoritmo deve essere eseguibile in un tempo finito. Se le operazioni il tempo che si andrebbe a impiegare per eseguire le azioni di un algoritmo fosse infinito, esso non potrebbe essere considerato tale.

Il terzo punto afferma che il numero di azioni di un algoritmo deve essere finito.

Il quarto punto è leggermente più complesso. In sostanza afferma che un algoritmo ben scritto permette di risolvere tutti i problemi di una stessa classe. Che significa? Spieghiamolo con un esempio: scrivere l'algoritmo per sommare due numeri oppure scrivere l'algoritmo per sommare varie coppie di numeri, è un modo per risolvere il problema, che sicuramente non è il più efficiente. Un buon algoritmo è in grado di risolvere il problema di sommare una coppia di numeri, per ogni possibile coppia di numeri: qualsiasi coppia di numeri si voglia sommare, un algoritmo generale permette di farlo. Avere un algoritmo che risolva tutti i problemi di una categoria è molto meglio che avere molteplici algoritmi che risolvano gli specifici casi. Questo problema, al momento, non si presenterà dato che gli algoritmi sono banali.

Più un algoritmo è generale e più risulta complesso individuarlo e descriverlo. Se, ad esempio, dovessimo scrivere l'algoritmo per sommare $2$ e $3$, possiamo scrivere un algoritmo velocemente. Scrivere un algoritmo che descriva come sommare _qualsiasi_ coppia di numeri è più complesso, bisogna garantire che l'algoritmo funzioni per **qualsiasi** coppia di numeri. Dunque se l'algoritmo non è generale è, di solito, più semplice.

---

## Esecutore

La nozione di algoritmo è legata a quella di esecutore

Un esecutore è completamente caratterizzato dall'insieme di istruzioni che può eseguire. Non esiste un algoritmo se non c'è un sistema in grado di eseguirlo

---

## In sintesi

In un algoritmo:

-   la rappresentazione di un processo risolutivo deve essere espresso con istruzioni di un certo linguaggio, comprensibile dall'esecutore;
-   ciascuna istruzione deve essere definita rigorosamente senza ambiguità;
-   ciascuna istruzione deve essere eseguibile da parte dell'esecutore dell'algoritmo;
-   il processo descritto deve terminare dopo un numero finito di passi.

L'algoritmo deve essere:

-   applicabile a qualsiasi insieme di dati d'ingresso appartenente al dominio di definizione dell'algoritmo;
-   costituito da operazioni appartenenti a un determinato insieme di operazioni fondamentali;
-   costituito da regole che prendano in considerazione tutte le alternative che si possono presentare e non devono essere ambigue, cioè devono essere interpretabili in modo univoco.

---

## Attività di ricerca e attività esecutiva

**ATTIVITÀ DI RICERCA:**

-   formulazione di istruzioni da parte del risolutore.

**ATTIVITÀ DI ESECUZIONE:**

-   esecuzione di istruzioni da parte di un esecutore.

Risolutore ed Esecutore devono comunicare mediante un linguaggio.

---

## In sintesi

Risoluzione di un problema:

-   processo che trasforma i dati iniziali in risultati finali.

Il processo deve poter essere:

-   definito come sequenza di azioni elementari per un esecutore;
-   descritto con un linguaggio (sistema formale) comprensibile all'esecutore.

---

## Specifica di un algoritmo

<!-- {{ fino ad ora “chiacchiere chiacchiere lasciamo perdere” }} -->

In un algoritmo il risolutore descrive le operazioni necessarie per risolvere un problema e anche l'ordine con cui le istruzioni devono essere eseguite

In un algoritmo occorre specificare:

-   L'elenco degli oggetti da manipolare (<u>**INPUT**</u>) e l'elenco delle informazioni finali (<u>**OUTPUT**</u>);
-   L'insieme delle azioni da eseguire;
-   L'ordine esatto con cui le azioni devono essere eseguite e le condizioni che devono essere verificate perché a una azione ne segua una piuttosto che un'altra.

Ad esempio, nelle ricette vengono elencati gli ingredienti, vengono descritte le azioni da compiere e in che ordine. A volte bisogna effettuare più operazioni contemporaneamente, ciò nonostante è presente un ordine in cui effettuare le operazioni, che non viene deciso dall'esecutore. Per un algoritmo occorre fare la stessa cosa (le ricette sono in realtà algoritmi).

---

## Dominio dei dati

L'insieme dei dati di ingresso a cui si applica un algoritmo si chiama:

-   **Dominio di definizione dell'algoritmo**

L'insieme di tutti i risultati – dati di uscita – dedotti da un algoritmo si dice:

-   **Dominio immagine dell'algoritmo**

---

## Esempio di procedimento risolutivo

In ambiente culinario per poter risolvere il problema di preparare un dolce (RISULTATO) non è sufficiente avere a disposizione una cucina e una serie di ingredienti (DATI INIZIALI).

Occorre una RICETTA, ossia una descrizione dettagliata di una successione finita di semplici azioni che ogni persona è in grado di compiere:

-   RISOLUTORE: compilatore della ricetta
-   ESECUTORE: una persona in grado di eseguire alcune semplici azioni elementari (pesare, mescolare,…)
-   PROCESSO: l'esecuzione di una serie di azioni elementari
-   PASSO: l'esecuzione di una azione elementare

---

## Specifica di un algoritmo

Un algoritmo si può esprimere mediante:

-   Linguaggio naturale (pseudo-codifica)
-   Diagrammi di flusso (descrizione grafica)
-   Linguaggio di programmazione (codifica)

Questi sono i vari modi per descrivere un algoritmo. Il primo viene chiamato linguaggio naturale nonostante sia dell'italiano che fa ampio uso di determinate parole chiave.

Quando si scrive un algoritmo non è necessario aggiungere proposizioni, congiunzioni, etc. e si può dunque scrivere in maniera meno fluida, non è necessario abbellire il testo. Tutto ciò che non aggiunge informazioni è superfluo ma non è errato.

La sintassi è semplice: verbo per descrivere un'operazione e nome per i dati; non è possibile descrivere un'operazione senza l'utilizzo di un verbo. È possibile usare dei simboli che _sostituiscono_ il verbo, alcuni di essi sono $\gets$ che sta per _assegnare_, $<$ che sta per _confrontare_, $!=$ che è un altro operatore di confronto.

Le strutture di controllo seguono una sintassi **standard**, è necessario scriverle in determinati modi facendo uso di parole chiave. In italiano è possibile scrivere una struttura di controlli in vari modi, nella descrizione di un algoritmo questo non è possibile poiché si creerebbe troppa ambiguità. Le strutture di controllo sono $3$ e utilizzano poche parole chiave, circa una decina.

In un algoritmo è necessario specificare:

-   I dati di ingresso e di uscita
-   Le operazioni elementari (istruzioni)
-   L'ordine con cui le istruzioni devono essere eseguite (istruzioni o strutture di controllo)

---

## Linguaggio naturale

Un algoritmo è descritto da frasi di un linguaggio naturale (italiano, inglese)

Le operazioni elementari sono descritte tramite nomi, verbi ed espressioni

-   Le operazioni sono scelte in relazione al problema da risolvere
-   I nomi denotano i dati

Le strutture di controllo o schemi di composizione delle istruzioni sono definite mediante l'utilizzo di parole chiave

---

## Strutture di controllo

Hanno lo scopo di comporre le istruzioni. Definiscono cioè l'ordine con cui le istruzioni devono essere eseguite
Le strutture di controllo fondamentali sono:

-   Sequenza
-   Selezione
-   Iterazione

---

## Sequenza

Permette di comporre ed eseguire le istruzioni una di seguito all'altra

Le istruzioni sono sempre eseguite nell'ordine in cui sono state poste

Nella sequenza si procede in maniera **Top-Down**, ovvero dal basso verso l'alto e <u>**non**</u> al contrario. Nella sequenza non sono presenti parole chiave poiché non è necessario alterare il flusso. La sequenza segue l'ordine più naturale per eseguire una lista di azioni

---

## Selezione binaria

La selezione binaria è stata vista precedentemente nell'algoritmo di Euclide. Questa permette di avere due alternative, una al di sotto dell'altra. L'esecutore non esegue entrambe le istruzioni, ma solo una delle due. Per decidere quale azione eseguire si fa uso del controllo di una _CONDIZIONE_.

-   _CONDIZIONE_: espressione il cui valore è vero o falso

Il costrutto generale della selezione binaria è il seguente:

-   **_SE_** (condizione)
    -   **_ALLORA:_** [...]
    -   **_ALTRIMENTI:_** [...]
-   **_FINE_SE_**

Parole chiave: **_SE_**, **_ALLORA_**, **_ALTRIMENTI_**, **_FINE_SE_**.

È assolutamente necessario includere queste parole durante la scrittura dell'algoritmo (se si sta facendo uso della selezione binaria), altrimenti l'algoritmo non è scritto correttamente. I blocchi `[...]` che seguono sia **_ALLORA:_** che **_ALTRIMENTI:_** possono contenere numerose operazioni che vedremo in seguito. In vari casi è possibile non fare uso dell'**_ALTRIMENTI:_** al contrario, è obbligatorio inserire l'**_ALLORA:_**.
Le operazioni da eseguire sono operazioni reali, sarebbe errato scrivere di non fare nulla. La condizione della selezione binaria va scelta in modo tale che il controllo tenda verso il vero, ovvero verso l'eseguire un'azione.

---

## Iterazione a condizione iniziale

Permette di eseguire ripetutamente una o più istruzioni sotto il controllo di una espressione booleana o condizione

Un costrutto potrebbe essere:

-   **_MENTRE_** (condizione)
    -   [...]
-   **_FINE_MENTRE_**

Parole chiave: **_MENTRE_**, **_FINE_MENTRE_**.

Nell'iterazione a condizione iniziale, l'esecutore deve innanzitutto verificare che la condizione iniziale sia <u>VERA</u>. Nel caso in cui essa sia <u>VERA</u> allora bisogna eseguire le istruzioni comprese tra **_MENTRE_** e **_FINE_MENTRE_**, Quando l'esecutore giunge a **_FINE_MENTRE_** deve effettuare nuovamente il controllo della condizione e se questa risulta <u>VERA</u> ripetere nuovamente le azioni contenute nel blocco. Se la condizione risulta essere <u>FALSA</u> allora semplicemente l'esecutore procederà oltre.

È importante ricordare che la condizione viene usata per restare all'interno dell'iterazione, infatti se è <u>VERA</u> si procede normalmente.

---

## Iterazione a condizione finale

Permette di eseguire ripetutamente una o più istruzioni sotto il controllo di una espressione booleana o condizione

Un costrutto potrebbe essere:

-   **_ESEGUI_**
    -   [...]
    -   **_FINCHÉ_** condizione
-   **_FINE_ESEGUI_**

Parole chiave: **_ESEGUI_**, **_FINCHÉ_**, **_FINE_**.

Nell'iterazione a condizione iniziale l'esecutore ripete le istruzioni contenute tra **_ESEGUI_** e **_FINE_ESEGUI_**, solo dopo controlla che la condizione sia <u>VERA</u>. Poiché il controllo avviene dopo, le azioni all'interno del blocco vengono eseguite _almeno_ una volta. I due tipi di iterazione sono perlopiù identici, l'unica differenza è il momento il cui avviene il controllo della condizione. Nella maggior parte dei casi sarà sufficiente utilizzare un'iterazione a condizione iniziale ma il altri sarà necessario eseguire le istruzioni nonostante la condizione sia <u>FALSA</u>.

> Un collega chiede se sia possibile utilizzare l'iterazione a condizione finale per convertire da decimale a binario.

È possibile ma è sufficiente utilizzare l'iterazione a condizione finale imponendo che se il risultato sia $0$, si interrompe il ciclo.

---

## Algoritmo per effettuare una telefonata

1. Sollevare il ricevitore
2. Attendere il segnale di linea
3. Comporre il numero
4. Attendere la risposta
5. Condurre la conversazione
6. Deporre il ricevitore

L'esecuzione dell'algoritmo termina in un tempo finito?

> Sì se tutto procede perfettamente, No se ci sono degli imprevisti. Analizziamo.

Analizziamo l'algoritmo precedente, è un algoritmo semplice da descrivere. Questo algoritmo è una semplice sequenza di azioni algoritmo, notiamo dunque l'assenza di parole chiave come **_MENTRE_**, **_FINE_MENTRE_**, **_SE_**, **_FINE_SE_**, **_ALLORA:_**, **_ALTRIMENTI:_**. L'algoritmo andrebbe aggiornato per i tempi moderni, ma è comunque funzionante e le azione da eseguire sono identiche.

Il problema di questo algoritmo è che è corretto solo se non si verificano problemi, nel caso in cui ci sia un'eccezione, l'algoritmo è errato. L'algoritmo presuppone che ci sia la linea e questo non è sempre assicurato. Al punto 2. l'esecutore deve attendere che chiunque abbia chiamato risponda, nemmeno questo è assicurato. L'utilizzo di _attendere_ è molto pericoloso, in questo caso l'esecutore dovrebbe restare in attesa finché non c'è linea, potrebbe restare in attesa per sempre. Accade la stessa cosa al punto 4. Sarebbe dunque più corretto aggiungere un tempo massimo di attesa, oppure evitare completamente l'utilizzo di _attendere_.

Scrivere algoritmi non è semplice perché è necessario considerare tutte le situazioni che l'esecutore può incontrare. È necessario che tutte le azioni non siano problematiche.

È difficile che un algoritmo sia una semplice sequenza, poiché anche negli algoritmo più semplici è necessario considerare gli errori o le eccezioni. Nell'esempio precedente è necessario considerare cosa potrebbe accadere attendendo il segnale di linea e la risposta; bisognerebbe scrivere, ad esempio, _attendere_ $10 {\rm\small \,s}$ il segnale di linea e scrivere anche cosa fare passati i $10 {\rm\small \,s}$. Ad esempio l'algoritmo di Euclide, nonostante sia un algoritmo molto semplice, fa uso del **_MENTRE_** e del **_SE_**.

---

## Selezione binaria - Esempio

Dati due numeri interi determinare il valore massimo

Denotiamo con

-   $a, b$ i due numeri interi
-   $\text{\text{max}}$ il valore massimo

<u>**INPUT:**</u>

-   $a, b$ – coppia di numeri interi

<u>**OUTPUT:**</u>

-   $\text{max}$ – numero intero

Qual è il DOMINIO dei dati di input e di output?

### Algoritmo – Linguaggio naturale

-   **_SE $(a$_** è minore di $b)$
    -   **_ALLORA:_** _assegno_ a $\text{max}$ il valore di $b$
    -   **_ALTRIMENTI:_** _assegno_ a $\text{max}$ il valore di $a$
-   **_FINE_SE_**

### Alg – pseudocodice

-   **_SE $(a < b)$_**
    -   **_ALLORA: $\text{max} \gets b$_**
    -   **_ALTRIMENTI: $\text{max} \gets a$_**
-   **_FINE_SE_**

Il simbolo “$<$” denota l'operatore di confronto

Il simbolo “$\gets$” denota il simbolo di assegnazione

---

## Ricerca del valore massimo

Siano dati $n$ un intero positivo maggiore di $0$ ed un elenco $E$ di $n$ numeri interi. Calcolare il valore massimo tra i valori di $E$.

<u>**INPUT:**</u>

-   $n$ – numero intero maggiore di $0$;
-   $E$ – elenco di $n$ numeri interi

<u>**OUTPUT:**</u>

-   $\mathord{\text{max}}$ – numero intero

### Algoritmo – Linguaggio naturale

È necessario trovare il massimo di una lista di numeri, descriviamo un algoritmo sommario:

-   _assegna_ il valore $\mathord{\text{max}}$ al primo numero dell'elenco $E$
-   **_MENTRE_** $($vi sono ancora numeri nell'elenco $E)$
    -   _confronta_ il valore attuale di $\mathord{\text{max}}$ con il numero successivo e _determina_ il nuovo $\mathord{\text{max}}$
-   **_FINE_MENTRE_**

L'algoritmo non rispetta uno dei criteri degli algoritmo: l'utilizzo di operazioni elementari. Sono presenti due operazioni combinate in una. L'algoritmo è scritto in maniera approssimativa però risulta comunque comprensibile. È, in ogni caso, necessario non unire le due operazioni, sarebbe meglio utilizzare sia un **_MENTRE_** che un **_SE_**.

[Massimo di una lista di numeri](./ex/massimo_lista_numeri.md)

---

## Selezione binaria - Esempio

Determinare se i numeri interi $x, y, z$ sono in ordine crescente

<u>**INPUT:**</u>

-   $x, y, z$ – insieme delle terne dei numeri interi

<u>**OUTPUT:**</u>

-   ${\it risposta}$ – <u>VERO</u> o <u>FALSO</u>

### Algoritmo – Linguaggio naturale

-   _assegno_ a ${\it risposta}$ il valore <u>FALSO</u>
-   **_SE $(x < y)$_**
    -   **_SE_** $(y < z)$
        -   **_ALLORA:_** _assegno_ a ${\it risposta}$ il valore <u>VERO</u>
    -   **_FINE_SE_**
-   **_FINE_SE_**

I tre numeri $x, y, z$ sono ordinati in ordine crescente se risulta <u>VERA</u> l'espressione ${x < y < z}$

---

## Strutture di controllo

Le strutture di controllo – sequenza, selezione ed iterazione – si possono annidare l'una dentro l'altra

Esempio:

-   **_SE_** $($...$)$
    -   **_ALLORA:_** [...]
    -   **_ALTRIMENTI:_** [...]
-   **_FINE_SE_**

Dove `[...]` può a sua volta essere una sequenza o una selezione o una iterazione

---

## Indentazione

Le istruzioni che devono essere eseguite sotto una condizione vengono scritte spostandosi verso destra – rispetto alla posizione della riga in cui c'è il controllo

L'obiettivo è quello di migliorare la leggibilità dell'algoritmo

---

## Considerazioni sull'utilizzo del linguaggio naturale

L'uso del linguaggio naturale è utile nell'analisi del problema e nel progetto dell'algoritmo

La progettazione top-down (dall'alto verso il basso) o per raffinamenti successivi consente di scrivere più versioni della soluzione:

Da una versione generale a versioni sempre più dettagliate rispetto al linguaggio di programmazione scelto

---

## Algoritmi - Storia

Il termine algoritmo deriva dal nome del matematico arabo Al-Khuwarismi del IX secolo d.c. che ha contribuito alla fondazione dell'algebra

Dal termine algoritmo ha origine il nome algebra

---

## Equivalenza

Due algoritmi si dicono equivalenti quando

1. Hanno lo stesso dominio di definizione
2. Hanno lo stesso dominio immagine
3. In corrispondenza degli stessi valori nel dominio di definizione producono gli stessi valori nel dominio immagine

Due algoritmi equivalenti

-   Forniscono lo stesso risultato
-   Possono essere profondamente diversi
-   Possono avere diversa efficienza

---

## Quesiti

Utilizzo di un lettore portatile di CD musicali – avente dei pulsanti di controllo ed un display che indica se nel lettore vi è un CD e qual è il brano selezionato

1. Se è disponibile una presa elettrica inseriamo l'alimentatore nella presa
2. Se non è disponibile una presa controlliamo se il lettore contiene le batterie, in caso contrario inseriamo le batterie
3. Accendiamo il lettore
4. Inseriamo il CD nel lettore
5. Premiamo il pulsante "Start"
6. Se il display indica "Disco OK" premiamo il pulsante "Forward" finché il display non indica il numero del brano voluto
7. Indossiamo le cuffie

Quali sono le azioni elementari descritte nell'algoritmo? Quali sono le strutture di controllo?

## In sintesi

In un algoritmo:

-   la rappresentazione di un processo risolutivo deve essere espresso con istruzioni di un certo linguaggio, comprensibile dall'esecutore;
-   ciascuna istruzione deve essere definita rigorosamente senza ambiguità;
-   ciascuna istruzione deve essere eseguibile da parte dell'esecutore dell'algoritmo;
-   il processo descritto deve terminare dopo un numero finito di passi.

L'algoritmo deve essere:

-   applicabile a qualsiasi insieme di dati d'ingresso appartenente al dominio di definizione dell'algoritmo;
-   costituito da operazioni appartenenti a un determinato insieme di operazioni fondamentali;
-   costituito da regole che prendano in considerazione tutte le alternative che si possono presentare e non devono essere ambigue, cioè devono essere interpretabili in modo univoco.
