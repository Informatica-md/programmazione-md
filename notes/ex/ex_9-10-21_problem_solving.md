---
title: 📚 Esercizi del 9.10.21 – Problem solving
author: Simone Fidanza
type: exercise
meta:
    tags:
        - Anno I
        - Semestre I
        - INF/01
    docente: Fabio Abbattista
    contatto: fabio.abbattista@uniba.it, fabbattista@gmail.com
---

# Esercizi del 9.10.21 – Problem solving

## Somma di due numeri

Siano $a, b$ due numeri. Determinare l'algoritmo che definisce la somma $s = a + b$ dei due numeri.

Ancor prima di scrivere l'algoritmo di somma è necessario capire cosa il simbolo $+$ indichi; ovviamente, indica la somma tra due numeri, ma in che modo si procede? Per sommare due numeri, ad esempio $5, 7$, si prende il primo numero e lo si incrementa di $1$ tante volte quante indicate dal secondo numero: $5 + 7 = 5 + 1 + 1 + 1 + 1 + 1 + 1 + 1 = 12$.

Scriviamo ora l'algoritmo della somma di due qualsiasi numeri $a,b > 0$:

1. Prendere il valore di $a$;
2. Prendere il valore di $b$:
3. Incrementare di $1$ il valore di $a$;
4. Ridurre di $1$ il valore di $b$;
5. **Se $b > 0$ vai** a 3.

Il punto 5. utilizza un'espressione che non è ben vista in informatica: l'espressione `GOTO` (o `GO TO`). Il comando consente di effettuare salti incondizionati da un punto all'altro del codice. L'utilizzo rende illeggibile o di difficile comprensione un algoritmo o una procedura.

Se $a, b \geq 0$ cosa succede? L'algoritmo non risulta più valido per $b = 0$. È necessario aggiungere un controllo prima di 3.

1. Prendere il valore di $a$;
2. Prendere il valore di $b$;
3. **Se $b = 0$ vai** a 7.;
4. Incrementare di $1$ il valore di $a$;
5. Ridurre di $1$ il valore di $b$;
6. **Se $b > 0$ vai** a 3.
7. Risultato: $a$

L'algoritmo è adesso funzionante e senza errori, però non è scritto correttamente. Vedremo in seguito come devono essere scritti.

---

## Conversione da Binario a Decimale

Dati due numeri $a_2,\; a_{10}$, scritti rispettivamente in sistema binario e in sistema decimale, convertire il numero da binario a decimale.

Dato, ad esemio, $a_2 = 0110$, si ha:

1. Prendere l'ultima cifra di $a_2$;
2. Moltiplicare la cifra per $2$ elevato alla posizione in cui si trova la cifra;

Immediatamente notiamo un problema: non è possibile tornare a 1., si riprenderebbe l'ultima cifra del numero. Cambiamo l'algoritmo introducendo un contatore. Assumiamo che la posizione $0$ corrisponda con l'ultima cifra del numero e che il contatore aumenti di $1$ spostandosi di cifra in cifra da destra verso sinistra. Dunque:

1. Definire il contatore $p = 0$;
2. Prendere la cifra in posizione $p$;
3. Moltiplicare la cifra per $2^p$;
4. Incrementare di $1$ il valore di $p$;
5. **Se** il valore di $p$ è minore della lunghezza della cifra, allora **vai** a 2.

L'algoritmo è ancora incompleto e non corretto ma fornisce un'idea di come si debba procedere. Manca un passaggio che andrebbe posto tra 3. e 4.: sommare man mano i valori che si ottengono per formare $a_{10}$. Allora l'algoritmo diventa:

1. Definire il contatore $p = 0$;
2. Prendere la cifra in posizione $p$;
3. Moltiplicare la cifra per $2^p$;
4. Sommare al risultato il valore della moltiplicazione precedente;
5. Incrementare di $1$ il valore di $p$;
6. **Se** il valore di $p$ è minore della lunghezza della cifra, allora **vai** a 2.

---

---

## Esercizi slide

1. Modificare l'algoritmo per la conversione da miglia a kilometri in modo che converta le distanze da chilometri a miglia;
2. Elencare i dati, i risultati, i vincoli e l'algoritmo per un programma che converta il volume da quarti a litri.

## Esercizi assegnati a lezione

analisi e progettazione della ricetta della pasta al forno

-   NO melanzane
-   tante polpette
-   mortadella
-   mozzarella
-   uovo sodo
-   pasta
-   sugo (ragù)
