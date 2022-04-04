---
title: 🔄 Algoritmo di Euclide
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

# Algoritmo di Euclide

## Calcolo del massimo comun divisore

Dati due interi $a, b$ calcolare il massimo comun divisore di $a, b$.

**INPUT:**

-   $a, b$ – coppia di numeri interi maggiori di $0$

**OUTPUT:**

-   $\text{mcd}$ – numero intero maggiore di $0$

I vincoli che vengono imposti sull'<u>**INPUT**</u> servono per garantire il funzionamento del metodo di soluzione. Nel caso in cui i numeri non siano interi, il funzionamento dell'algoritmo non è garantito. I vincoli imposto sull'<u>**OUTPUT**</u> sono necessari per aggiungere una verifica alla soluzione: se si ottiene un numero non intero e/o minore di zero, l'algoritmo è errato.

---

## Algoritmo di Euclide per il calcolo del minimo comun divisore

L'algoritmo di Euclide si basa sulle seguenti proprietà:

1. **_SE $(a = b)$ ALLORA: $\mathord{\text{mcd}}(a,b) = a = b$;_**
2. **_SE $(a > b)$ ALLORA: $\mathord{\text{mcd}}(a, b) = \mathord{\text{mcd}}(a - b, b)$;_**
3. **_SE $(a < b)$ ALLORA: $\mathord{\text{mcd}}(a, b) = \mathord{\text{mcd}}(a, b - a)$._**

Prendiamo i numeri $a = 5, b = 3$ e troviamo il loro $\mathord{\text{mcd}}$. Notiamo che $5 \neq 3$, quindi la prima regola non si applica, ma la seconda sì dato che $5 > 3$. Dunque si ha:

$$
\mathord{\text{mcd}}(5, 3) \implies
\mathord{\text{mcd}} (5 - 3, 3) = \mathord{\text{mcd}}(2, 3)
$$

Ripetiamo i passaggi precedenti per $a = 2, b = 3$. I due numeri non sono uguali, inoltre $2$ non è maggiore di $3$, però si ha che $2 < 3$, quindi:

$$
\mathord{\text{mcd}}(2, 3) \implies
\mathord{\text{mcd}}(2, 3 - 2) = \mathord{\text{mcd}}(2, 1)
$$

Ripetiamo nuovamente il procedimento. La prima condizione non si verifica ma la seconda sì dato che $2 > 1$, dunque:

$$
\mathord{\text{mcd}}(2, 1) \implies
\mathord{\text{mcd}}(2, 2 - 1) = \mathord{\text{mcd}}(1, 1) = 1
$$

Quindi si procede finché i due numeri $a, b$ sono uguali. Lo svantaggio è che per numeri molto grandi bisogna ripetere più volte questo procedimento. Il caso peggiore che si può incontrare è proprio quello appena analizzato: quando $\mathord{\text{mcd}}(a, b) = 1$.

È importante notare che questo **non** è un algoritmo. Esso è utile a dare un'idea per come risolvere il problema, non è la soluzione. Queste proprietà potrebbero essere tranquillamente usate per trovare il minimo comun divisore di una coppia di numeri, però non è esplicitato che sia necessario ripetere le azioni finché i due numeri sono uguali. È necessario esplicitare questa ripetizione, senza l'utilizzo del comando `GOTO`.

---

## Algoritmo di Euclide - pseudocodifica

La pseudocodifica dell'algoritmo di Euclide risulta essere abbastanza semplice. Denotiamo con ➤ [...] un commento nello pseudocodice, che a sua volta abbreviamo con p-codice.

-   **_MENTRE_** $(a \neq b)$ ➤ **ripetizione** dello p-codice tramite **_MENTRE_** finché $a \neq b$ sarà FALSA.
    -   **_SE_** $(a > b)$ ➤ **controllo** tramite **_SE_**. Diverso procedimento a seconda della condizione
        -   **_ALLORA:_** _assegna_ ad $a$ il valore $a - b$ ➤ _dichiaro_ il procedimento per c = VERA
        -   **_ALTRIMENTI:_** _assegna_ a $b$ il valore $b - a$ ➤ _dichiaro_ il procedimento per c = FALSA
    -   **_FINE_SE_** ➤ **fine** del costrutto **_SE_**
-   **_FINE_MENTRE_** ➤ **fine** del blocco **_MENTRE_**.
-   _assegna_ a $\mathord{\text{mcd}}$ il valore $a$ ➤ _assegno_ a $\mathord{\text{mcd}}$ il valore di $a$ dopo il ciclo **_MENTRE_**

L'utilizzo del comando **_MENTRE_** è il modo più semplice per imporre una ripetizione di un blocco di pseudocodice. Se si commette un errore e non si verifica mai la condizione $a = b$, allora il comando si ripeterà all'infinito e non ci sarà modo d'interromperlo. Se per esempio, i due numeri sono negativi l'algoritmo si ripete all'infinito, ma siccome nelle condizioni iniziali ho imposto di usare numeri maggiori di zero, questo non succederà.

Quando si scrivono algoritmi che fanno uso di ripetizioni è **assolutamente** necessario avere un modo di uscire dal ciclo continuo. In questo caso la possibilità d'interrompere il ciclo è data dall'**_ALTRIMENTI_**. È assolutamente necessario porre una fine a un algoritmo altrimenti non può essere considerato tale.

Spesso è necessaria una singola condizione per interrompere il ciclo, in questo caso se i due valori sono uguali la ripetizione termina.

L'algoritmo visto in [precedenza](https://www.notion.so/Algoritmo-di-Euclide-1612c595ab55438bb252d98e4e2a740d) essenzialmente fa eseguire le stesse azioni di quello appena scritto, però il primo non esplicita la ripetizione e utilizza tre costrutti **_SE_**.

Lo pseudocodice è un modo per _descrivere_ la soluzione, ma **non** è la soluzione. In questo la soluzione verrà unicamente descritta attraverso l'uso dello pseudocodice. È possibile non scrivere a parole le dichiarazioni come “_assegna_”, ma si possono usare dei simboli come $\gets$ e $\coloneqq$ ma **mai** va utilizzato l'uguale $(=)$ perché è già riservato al confronto. Lo pseudocodice precedente dunque diventerebbe:

-   **_MENTRE_** $(a \neq b)$
    -   **_SE_** $(a > b)$
        -   **_ALLORA:_** $a \gets a - b$
        -   **_ALTRIMENTI:_** $b \gets b - a$
    -   **_FINE_SE_**
-   **_FINE_MENTRE_**
-   $\mathord{\text{mcd}} \gets a$

Notiamo che i simboli che vengono usati sono simboli che vengono regolarmente usati in matematica e non sono necessariamente simboli usati da linguaggi di programmazione. Un altro simbolo per indicare il diverso $(\neq)$ è <> e non $!=$ dato che quest'ultimo viene usato in C.

Sarebbe inoltre errato scrivere **_while_** [...] oppure **_if_** [...] poiché la sintassi che dobbiamo usare non è quella del C o di altri linguaggi. Non vanno nemmeno usate parentesi graffe per delimitare dei blocchi d'istruzione come **_MENTRE_**, **_SE_**, etc.

Non è stato utilizzato il comando `GOTO`. Nonostante questo, al rigo dell'istruzione **_FINE_MENTRE_** avviene un'operazione simile: l'esecuzione si ferma e viene controllata la condizione del **_MENTRE_**; se questa è VERA allora il blocco viene ripetuto (andando a simulare una sorta di `GOTO`, però controllato), se questa è FALSA si passa al rigo successivo.

Il significato del costrutto **_SE_** è abbastanza semplice: avviene una verifica della condizione e si hanno due casi in base alla condizione, se è:

1. VERA si eseguono le istruzioni dell'**_ALLORA_**;
2. FALSA si eseguono le istruzioni dell'**_ALTRIMENTI_**.

---

## Algoritmo di Euclide – flow-chart

```mermaid
flowchart LR
%% Declaring nodes names and descriptions
START([Inizio]); END([Fine]);
READ[/Lettura a,b/]; WRITE[/Scrittura a/];
IS_GREATER{a > b?}; IS_LESSER{a < b?};
THEN[a = a - b]; ELSE[b = b - a];
dummy1(( )); dummy2(( ));   %% used to better connect main nodes

%% Declare how to style blocks
classDef Terminator color: black, fill: #6A2C70, stroke: #202020, stroke-width:2px;

classDef Decision color: black, fill: #F08A5D, stroke: #202020, stroke-width: 2px;

classDef Process color: black, fill: #B83B5E, stroke: #202020, stroke-width: 2px;

classDef Data color: black, fill: #F9ED69, stroke: #202020, stroke-width:2px;

class START,END Terminator;
class IS_GREATER,IS_LESSER Decision;
class THEN,ELSE Process;
class READ,WRITE Data;

%% Declare how to style arrows
linkStyle default stroke-width: 3px;

%% Actual flowchart
START --> READ;
READ --> dummy1 --> IS_GREATER;
IS_GREATER -->|no| IS_LESSER;
IS_GREATER --> |sì| THEN;
IS_LESSER -->|no| WRITE;
IS_LESSER -->|sì| ELSE;
THEN & ELSE --> dummy2 --> dummy1;
WRITE --> END;
```

---

## Algoritmo di Euclide - codifica

```C
while (a != b) {
    if (a > b) {
        a = a - b;
    }
    else {
        b = b - a;
    }
}
mcd = a;
```

---

## Algoritmo di Euclide - considerazioni

L'algoritmo di Euclide si può esprimere in modo più naturale mediante la ricorsione, come vedremo in seguito.
