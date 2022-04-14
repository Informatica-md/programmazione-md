---
title: 📚 Massimo di una lista di numeri
author: Simone Fidanza
type: exercise
lecture date: 13/10/2021
meta:
    tags:
        - Anno I
        - Semestre I
        - INF/01
    docente: Fabio Abbattista
    contatto: fabio.abbattista@uniba.it, fabbattista@gmail.com
---

# Massimo di una lista di numeri

L'obiettivo dell'algoritmo è trovare il massimo in una lista di \(n\) numeri interi. Analizziamo i dati.

<u>**INPUT:**</u>

-   $E$ – elenco di numeri interi;
-   $n$ – numero di elementi di $E$, dev'essere maggiore di $0$

<u>**OUTPUT:**</u>

-   ${\rm max}$ – elemento massimo di $E$, dev'essere un numero intero.

Iniziamo a descrivere l'algoritmo:

-   _assegnare_ a ${\rm max}$ il primo valore di $E$

La frase è ovviamente corretta, però può essere ridotta usando $\coloneqq$ oppure $\gets$. Facciamolo usando il secondo simbolo:

-   ${\rm max} \gets$ primo valore di $E$

Per rendere più semplice l'algoritmo, possiamo utilizzare un numero che vada a indicare le posizioni all'interno dell'elenco. Quindi, al posto di scrivere: “primo”, “secondo” oppure “successivo”, indicheremo le posizioni che vanno da $1$ a $n$. Il termine “successivo” ha significato in correlazione a qualcos'altro: se manca un riferimento iniziale, diventa complicato capire cosa sia il successivo.

Necessitiamo dunque di un altro dato, chiamiamolo $p$, che deve essere $p > 0$ e $p \leq n$. Questo dato non è né un dato di <u>**INPUT**</u> perché non viene ricevuto in <u>**INPUT**</u> e né un dato di <u>**OUTPUT**</u>. È un **dato di lavoro locale** che serve per risolvere il problema. Dunque, sapendo che $0 < p \leq n$, scriviamo l'algoritmo:

-   $p \gets 1$
-   ${\rm max} \gets p$-esimo elemento di $E$
-   **_MENTRE_** $(p \leq n)$
    -   **_SE_** $({\rm max} < p$-esimo elemento di $E)$
        -   **_ALLORA:_** ${\rm max} \gets p$-esimo elemento di $E$
    -   **_FINE_SE_**
    -   $p \gets p + 1$
-   **_FINE_MENTRE_**

Usando questa sintassi non si crea la confusione che si andrebbe a creare se si usasse “successivo”. Questo appena descritto è un algoritmo di ricerca, non è il migliore, però funziona in qualsiasi situazione che rispetti i vincoli di <u>**INPUT**</u>. Vedremo in seguito algoritmi che sono più efficienti ma non sono sempre applicabili.

Il nostro algoritmo può anche essere riscritto meglio:

-   $p \gets 1$
-   ${\rm max} \gets p$-esimo elemento di $E$
-   **_MENTRE_** $(p < n)$
    -   $p \gets p + 1$
    -   **_SE_** $({\rm max} < p$-esimo elemento di $E)$
        -   **_ALLORA:_** ${\rm max} \gets p$-esimo elemento di $E$
    -   **_FINE_SE_**
-   **_FINE_MENTRE_**

Questo è più efficiente perché l'esecutore non deve effettuare un controllo inutile tra il primo elemento e se stesso.
