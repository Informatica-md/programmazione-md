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

-   È interpretata in modo univoco dall’esecutore;
-   È direttamente eseguita dall’esecutore.

**Cioè l’esecutore comprende in modo univoco che cosa deve fare e sa come farlo.**

Il concetto di operazione elementare è abbastanza soggettivo. Sarebbe meglio descrivere un’operazione elementare dicendo che l’esecutore deve capire l’istruzione (o operazione). Se l’esecutore non comprende l’operazione, allora essa non è elementare.

---

## Proprietà di un algoritmo

Un algoritmo gode necessariamente delle seguenti proprietà:

1. **Non-ambiguità:** ogni operazione descritta deve essere univocamente interpretabile dall’esecutore;
2. **Eseguibilità:** l’esecutore deve essere in grado di eseguire ogni operazione in un tempo finito;
3. **Finitezza:** per ogni insieme di dati d'ingresso, il numero totale di operazioni deve essere finito;
4. **Generalità:** deve produrre un risultato per ogni valore attribuito ai dati iniziali, cioè deve risolvere tutti i problemi di una stessa classe.

La prima proprietà afferma che leggendo l’algoritmo **non** ci deve essere possibilità d'interpretare cosa vi è scritto, esso deve essere chiaro. Nel caso in cui l’algoritmo venga interpretato in maniera diversa da più esecutori, l’algoritmo non può essere considerato tale.

La seconda proprietà afferma che l’algoritmo deve essere eseguibile in un tempo finito. Se le operazioni il tempo che si andrebbe a impiegare per eseguire le azioni di un algoritmo fosse infinito, esso non potrebbe essere considerato tale.

Il terzo punto afferma che il numero di azioni di un algoritmo deve essere finito.

Il quarto punto è leggermente più complesso. In sostanza afferma che un algoritmo ben scritto permette di risolvere tutti i problemi di una stessa classe. Che significa? Spieghiamolo con un esempio: scrivere l’algoritmo per sommare due numeri oppure scrivere l’algoritmo per sommare varie coppie di numeri, è un modo per risolvere il problema, che sicuramente non è il più efficiente. Un buon algoritmo è in grado di risolvere il problema di sommare una coppia di numeri, per ogni possibile coppia di numeri: qualsiasi coppia di numeri si voglia sommare, un algoritmo generale permette di farlo. Avere un algoritmo che risolva tutti i problemi di una categoria è molto meglio che avere molteplici algoritmi che risolvano gli specifici casi. Questo problema, al momento, non si presenterà dato che gli algoritmi sono banali.

Più un algoritmo è generale e più risulta complesso individuarlo e descriverlo. Se, ad esempio, dovessimo scrivere l’algoritmo per sommare $2$ e $3$, possiamo scrivere un algoritmo velocemente. Scrivere un algoritmo che descriva come sommare _qualsiasi_ coppia di numeri è più complesso, bisogna garantire che l’algoritmo funzioni per **qualsiasi** coppia di numeri. Dunque se l’algoritmo non è generale è, di solito, più semplice.

---

## Esecutore

La nozione di algoritmo è legata a quella di esecutore

Un esecutore è completamente caratterizzato dall’insieme di istruzioni che può eseguire. Non esiste un algoritmo se non c’è un sistema in grado di eseguirlo

---

## In sintesi

In un algoritmo:

-   la rappresentazione di un processo risolutivo deve essere espresso con istruzioni di un certo linguaggio, comprensibile dall’esecutore;
-   ciascuna istruzione deve essere definita rigorosamente senza ambiguità;
-   ciascuna istruzione deve essere eseguibile da parte dell’esecutore dell’algoritmo;
-   il processo descritto deve terminare dopo un numero finito di passi.

L’algoritmo deve essere:

-   applicabile a qualsiasi insieme di dati d'ingresso appartenente al dominio di definizione dell’algoritmo;
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
-   descritto con un linguaggio (sistema formale) comprensibile all’esecutore.

---

## Specifica di un algoritmo

{{ fino ad ora “chiacchiere chiacchiere lasciamo perdere” }}

In un algoritmo il risolutore descrive le operazioni necessarie per risolvere un problema e anche l’ordine con cui le istruzioni devono essere eseguite

In un algoritmo occorre specificare:

-   L’elenco degli oggetti da manipolare (<u>**INPUT**</u>) e l’elenco delle informazioni finali (<u>**OUTPUT**</u>);
-   L’insieme delle azioni da eseguire;
-   L’ordine esatto con cui le azioni devono essere eseguite e le condizioni che devono essere verificate perché a una azione ne segua una piuttosto che un’altra.

Ad esempio, nelle ricette vengono elencati gli ingredienti, vengono descritte le azioni da compiere e in che ordine. A volte bisogna effettuare più operazioni contemporaneamente, ciò nonostante è presente un ordine in cui effettuare le operazioni, che non viene deciso dall’esecutore. Per un algoritmo occorre fare la stessa cosa (le ricette sono in realtà algoritmi).

---

## Dominio dei dati

L’insieme dei dati di ingresso a cui si applica un algoritmo si chiama:

-   **Dominio di definizione dell’algoritmo**

L’insieme di tutti i risultati – dati di uscita – dedotti da un algoritmo si dice:

-   **Dominio immagine dell’algoritmo**

---

## Esempio di procedimento risolutivo

In ambiente culinario per poter risolvere il problema di preparare un dolce (RISULTATO) non è sufficiente avere a disposizione una cucina e una serie di ingredienti (DATI INIZIALI).

Occorre una RICETTA, ossia una descrizione dettagliata di una successione finita di semplici azioni che ogni persona è in grado di compiere:

-   RISOLUTORE: compilatore della ricetta
-   ESECUTORE: una persona in grado di eseguire alcune semplici azioni elementari (pesare, mescolare,…)
-   PROCESSO: l’esecuzione di una serie di azioni elementari
-   PASSO: l’esecuzione di una azione elementare

---

## Specifica di un algoritmo

Un algoritmo si può esprimere mediante:

-   Linguaggio naturale (pseudo-codifica)
-   Diagrammi di flusso (descrizione grafica)
-   Linguaggio di programmazione (codifica)

Questi sono i vari modi per descrivere un algoritmo. Il primo viene chiamato linguaggio naturale nonostante sia dell’italiano che fa ampio uso di determinate parole chiave.

Quando si scrive un algoritmo non è necessario aggiungere proposizioni, congiunzioni, etc. e si può dunque scrivere in maniera meno fluida, non è necessario abbellire il testo. Tutto ciò che non aggiunge informazioni è superfluo ma non è errato.

La sintassi è semplice: verbo per descrivere un’operazione e nome per i dati; non è possibile descrivere un’operazione senza un verbo,

{{ questi sono i vari modi per descrivere un alg. viene chiamato ling naturale però non lo è molto, è italiano che utilizza parole chiave. rispetto all’italiano non è necessario aggiungere proposizioni, congiunzioni, etc. si può scrivere in maniera meno fluida, non serve abbellire il testo. tutto ciò che non aggiunge informazioni è superfluo a ma non errato. verbo per operazione nome per i dati. non è possibile descrivere un’operazione senza un verbo, se si usano simboli il verbo viene omesso ma c’è $\gets$ sta per *assegnare* oppure $<$ *confrontare* il simbolo **sostituisce**. se scrivo bene non servono proposizioni e congiunzioni. le strutture di controllo sono standard, si scrivono in quel modo usando delle parole chiave (per questo non è esattamente linguaggio naturale). se in italiano avrei potuto scrivere in vari modi, nell’alg non si fa, si scrive mentre e la condizione. le strutture di controllo sono solo 3. e le parole chiave sono poche, una decina. lo pseudocodice è comodo perché semplice }}

In un algoritmo è necessario specificare:

-   I dati di ingresso e di uscita
-   Le operazioni elementari (istruzioni)
-   L’ordine con cui le istruzioni devono essere eseguite (istruzioni o strutture di controllo)

---

## Linguaggio naturale

Un algoritmo è descritto da frasi di un linguaggio naturale (italiano, inglese)

Le operazioni elementari sono descritte tramite nomi, verbi ed espressioni

-   Le operazioni sono scelte in relazione al problema da risolvere
-   I nomi denotano i dati

Le strutture di controllo o schemi di composizione delle istruzioni sono definite mediante l’utilizzo di parole chiave

---

## Strutture di controllo

Hanno lo scopo di comporre le istruzioni. Definiscono cioè l’ordine con cui le istruzioni devono essere eseguite
Le strutture di controllo fondamentali sono:

-   Sequenza
-   Selezione
-   Iterazione

---

## Sequenza

Permette di comporre ed eseguire le istruzioni una di seguito all’altra

Le istruzioni sono sempre eseguite nell’ordine in cui sono state poste

{{ esegue dall’alto verso il basso (NON al contrario) le operazioni, se non c’è struttura a modificare l’andamento si segue la sequenza. non c’è nessuna parola chiave perché non devo alterare in nessun modo il flusso. è il modo in cui si eseguono normalmente una lista di azioni. l’ordine di esecuzione è il più naturale. }}

---

## Selezione binaria

{{ vista prima nell’algoritmo di euclide. permette di avere due alternative una sotto l’altra però non vengono eseguite entrambe, o se ne esegue una o l’altra. se a > b allora [...] verifico condizione e se è vera, allora se è falsa altrimenti. }}

Permette la scelta tra due istruzioni sulla base di una espressione booleana o condizione

-   CONDIZIONE: espressione il cui valore è vero o falso

Un costrutto potrebbe essere:

-   **_SE_** condizione
    -   **_ALLORA_** [...]
    -   **_ALTRIMENTI_** [...]
-   **_FINE_SE_**

Parole chiave: **_SE_**, **_ALLORA_**, **_ALTRIMENTI_**, **_FINE_**.

{{ queste parole devono essere presenti nella scrittura dell’alg altirmenti è scritto male. allora e altrimenti possono anche essere più operazioni, vedremo in seguito. in alcuni casi si può non avere l’altrimenti e va bene lo stesso. l’allora c’è sempre per forza. le operazioni da fare sono operazioni reali da fare “non fare niente” non è una condizione, allora non va scritta se non bisogna fare niente, va eliminato allora sriverò l’operazione inversa. o si compie un’operazione altrimenti non stiamo a perdere tempo. si scrive in modo tale che il controllo tenda verso il vero. il non fare niente non si scrive. se c’è un alternativa reale allora la si esplicita. questa selezione è presente in preticamente in ogni selezione binaria, assieme all’iterazione. }}

---

## Iterazione a condizione iniziale

Permette di eseguire ripetutamente una o più istruzioni sotto il controllo di una espressione booleana o condizione

Un costrutto potrebbe essere:

-   **_MENTRE_** condizione
    -   [...]
-   **_FINE_MENTRE_**

Parole chiave: **_MENTRE_**, **_FINE_**.

{{ mentre si verifica una condizione eseguo quello che c’è fino all aparola fine, poi ritorno a verificare la condizione. SE vera ripeto fino a fine, e ripeto. se condizione falsa vado oltre. tra mentre e fine tutto quello che si vuole, viene ripetuto fincheé c=F. è la condizione per ocntinuoare, non per fermare. è facile confondersi molti pensan si ala condizione per uscire dal loop. }}

---

## Iterazione a condizione finale

Permette di eseguire ripetutamente una o più istruzioni sotto il controllo di una espressione booleana o condizione

Un costrutto potrebbe essere:

-   **_ESEGUI:_**
    -   [...]
    -   **_FINCHÉ_** condizione
-   **_FINE_ESEGUI_**

Parole chiave: **_ESEGUI_**, **_FINCHÉ_**, **_FINE_**.

{{ ripeto fino al finché e dopo controllo la condizione da verificare. si verifica dopo la struttura. se c=V allora ripeto tutto, se la c=F vado oltre però eseguo almeno una volta il blocco anche se c=F di partenza perché veiene verificata dopo. NEl mentre non è così perché se c=F non eseguo. in alcune situaizoni è utile eseguire nonstante sia F. il mentre copre il 90% dei loop così, a volte serve l’esegui (poi es.). può esere usato sempre se si ha la certezza che la c rispetti le aspettative. raramente serve il finché perché coglio prima essguire tutto prima. è necessario in alcuni casi, vedremo poi. per ora basta il mentre, dopo ce lo dice lui quando usare il finché. }}

{{ collega chiede se si può usare per convertire da decimale a binario. sì ma anche il mentre. se il risultato = 0 mi fermo, si può usare anche il mentre non è necessario l’esegui. mentre e esegui sono praticamente equivalenti però in alcune situazioni voglioamo verificare prima la condizione e in altri verificarla dopo. ci sono casi in cui si nota la differenza. }}

---

## Algoritmo per effettuare una telefonata

1. Sollevare il ricevitore
2. Attendere il segnale di linea
3. Comporre il numero
4. Attendere la risposta
5. Condurre la conversazione
6. Deporre il ricevitore

L’esecuzione dell’algoritmo termina in un tempo finito? {{ (sì ma no) }}

{{ prendiamo questo alg, è semplice da descrivere e risale da quando esistono i ricevitori. effettuare una telefonata, tutti l’hanno effettuata. è un alg ed è una sequenza di azioni, ntiamo la mancanza di parole chiave come mentre, fine, se, allora, altrimenti. è una lista di azioni. l’alg è corretto sotto un certo punto di vista (ora abbiamo i cell quindi è diverso però stiamo là). sull cell il pulsante verde è sollevare il ricevitore, le azioni sono le stesse. l’alg è corretto solo se non si verificano problemi, se si verifica un ‘eccezione, l’alg è errato. esso presuppone che ci sia la linea, non è detto che ci sia, se non c’è l’alg dice di attendere. è una delle più pericolose nella scrittura dell’algoritmo se non si è sicuri. l’esecutore resterà ad attendere finché non arriverà la linea (che non arriverà). attendere risposta se non risponde nessuno? attendere non va usato così facilmente quando si scrive un algoritmo a meno che non siate sicuri che qualcuno risponda al telefono, che l’attesa sia finita. }}

{{ quando scrivete algoritmi il problema è considerare tutte le situazioni e che l’esecutore non rimanga bloccato ad attendere cose che non avvengono. al posto di attendere sarebbe meglio mentre oppure se, ex. passati 30s si chiude. tutte le altre azioni non risultano problematiche. }}

{{ è difficile che un algoritmo sia una semplice sequenza, perché anche nei più semplici bisogna considerare gli errori, come quello di sopra. bisogna vedere che succede mentre attendo segnali di linea e la risposta. posso scrivere attendere 10s il segnale di linea e però scrivere cosa fare dopo, se non lo scrivo la sequenza procede normalmente. è difficile avere un alg completo che sia una sequenza soltanto. anche l’alg di euclide ha un mentre e un se. calcolare il max di 2 num c’è un se nonostante sia un alg semplicissimo }}

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
    -   **\*ALLORA:** assegno\* a **$\text{max}$ \*\***il valore di $b$
    -   **\*ALTRIMENTI:** assegno\* a $***\text{max}$\*\*\* il valore di $a$
-   **_FINE_SE_**

### Alg – pseudocodice

-   **_SE $(a < b)$_**
    -   **_ALLORA: $\text{max} \gets b$_**
    -   **_ALTRIMENTI: $\text{max} \gets a$_**
-   **_FINE_SE_**

Il simbolo “$<$” denota l’operatore di confronto

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

-   Poni il valore max uguale al primo numero dell’elenco E
-   Mentre vi sono ancora numeri nell’elenco E
    -   Confronta il valore massimo attuale max con il numero successivo e determina il valore massimo
-   Fine

-   _assegna_ il valore $\mathord{\text{max}}$ al primo numero dell’elenco $E$
-   **_MENTRE_** $($vi sono ancora numeri nell’elenco $E)$
    -   \*confronta **\***il valore attuale di $\mathord{\text{max}}$ con il numero successivo e _determina_ il nuovo $\mathord{\text{max}}$
-   **_FINE_MENTRE_**

{{ abbiamo più numeri e trovare il max di più numeri }}

{{ l’alg non è scritto secondo i criteri di operazioni elementari, ci sono due operazioni in un rigo. scritto in maniera approssimativa ma comprensibile. punto critico: unire le due operazioni, è un SE e andrebbe scitto così. }}

[Massimo di una lista di numeri](https://www.notion.so/Massimo-di-una-lista-di-numeri-618830f8dece47da83c4bfbfc21f9b6e)

---

## Selezione binaria - Esempio

Determinare se i numeri interi $x, y, z$ sono in ordine crescente

<u>**INPUT:**</u>

-   $x, y, z$ – insieme delle terne dei numeri interi

<u>**OUTPUT:**</u>

-   risposta – Vero o Falso

### Algoritmo – Linguaggio naturale

-   _assegno_ a $\text{\it risposta}$ il valore **Falso**
-   **_SE $(x < y)$_**
    -   **_SE_** $(y < z)$
        -   **_ALLORA:_** _assegno_ a $\text{\it risposta}$ il valore **Vero**
    -   **_FINE_SE_**
-   **_FINE_SE_**

I tre numeri $x, y, z$ sono ordinati in ordine crescente se risulta vera l’espressione ${x < y < z}$

---

## Strutture di controllo

Le strutture di controllo – sequenza, selezione ed iterazione – si possono annidare l’una dentro l’altra

Esempio:

-   **_SE_** $($...$)$
    -   **_ALLORA:_** [blocco_istruzioni]
    -   **_ALTRIMENTI:_** [blocco_istruzioni]
-   **_FINE_SE_**

Blocco istruzioni può a sua volta essere una sequenza o una selezione o una iterazione

---

## Indentazione

Le istruzioni che devono essere eseguite sotto una condizione vengono scritte spostandosi verso destra – rispetto alla posizione della riga in cui c’e’ il controllo

L’obiettivo è quello di migliorare la leggibilità dell’algoritmo

---

## Considerazioni sull’utilizzo del linguaggio naturale

L’uso del linguaggio naturale è utile nell’analisi del problema e nel progetto dell’algoritmo

La progettazione top-down (dall’alto verso il basso) o per raffinamenti successivi consente di scrivere più versioni della soluzione:

Da una versione generale a versioni sempre più dettagliate rispetto al linguaggio di programmazione scelto

---

## Algoritmi - Storia

Il termine algoritmo deriva dal nome del matematico arabo Al-Khuwarismi del IX secolo d.c. che ha contribuito alla fondazione dell’algebra

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

1. Se è disponibile una presa elettrica inseriamo l’alimentatore nella presa
2. Se non è disponibile una presa controlliamo se il lettore contiene le batterie, in caso contrario inseriamo le batterie
3. Accendiamo il lettore
4. Inseriamo il CD nel lettore
5. Premiamo il pulsante “Start”
6. Se il display indica “Disco OK” premiamo il pulsante “Forward” finchè il display non indica il numero del brano voluto
7. Indossiamo le cuffie

Quali sono le azioni elementari descritte nell’al goritmo? Quali sono le strutture di controllo?

## In sintesi

In un algoritmo:

-   la rappresentazione di un processo risolutivo deve essere espresso con istruzioni di un certo linguaggio, comprensibile dall’esecutore;
-   ciascuna istruzione deve essere definita rigorosamente senza ambiguità;
-   ciascuna istruzione deve essere eseguibile da parte dell’esecutore dell’algoritmo;
-   il processo descritto deve terminare dopo un numero finito di passi.

L’algoritmo deve essere:

-   applicabile a qualsiasi insieme di dati d'ingresso appartenente al dominio di definizione dell’algoritmo;
-   costituito da operazioni appartenenti a un determinato insieme di operazioni fondamentali;
-   costituito da regole che prendano in considerazione tutte le alternative che si possono presentare e non devono essere ambigue, cioè devono essere interpretabili in modo univoco.
