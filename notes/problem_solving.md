---
title: 💭 Problem Solving
author: Simone Fidanza
type: notes
lecture date: 9/10/2021
tags:
    - Anno I
    - Semestre I
    - INF/01
docente: Fabio Abbattista
contatto: fabio.abbattista@uniba.it, fabbattista@gmail.com
---

# Problem Solving

## Il metodo di sviluppo del software

Le operazioni da effettuare per sviluppare un software sono le seguenti:

1. Specificare i requisiti del problema;
2. Analizzare il problema;
3. Progettare la sequenza di azioni per risolvere il problema;
4. Realizzare la sequenza di azioni;
5. Fare il test e la verifica del programma;
6. Fare la manutenzione e l'aggiornamento del programma.

Ci sono varie metodologie per lo sviluppo del software che cambiano l'ordine di questi passaggi. Vediamo i vari punti.

---

## Specificare requisiti del problema

Come prima cosa è necessario capire il problema posto e evidenziare questi tre importanti punti:

1. Specificare il problema in maniera non ambigua;
2. Eliminare gli aspetti non importanti;
3. Individuare gli aspetti che servono per arrivare alla soluzione.

---

## Analizzare il problema

Successivamente si procede all'analisi del problema, chiarendo eventuali dubbi che sorgono durante la specifica dei requisiti del problema.

1. Identificare i dati da elaborare (<u>**INPUT**</u>)
2. Identificare i risultati desiderati (<u>**OUTPUT**</u>)
3. Identificare gli eventuali vincoli tra i dati
4. Individuare il formato di presentazione dei risultati.

Nel caso in cui il problema non fornisca o descriva chiaramente tutti i dati, essi vanno individuati. A volte potrebbe non essere chiaro il risultato richiesto, per questa ragione (e altre) si procede all'analisi del problema. Il punto 4. fa riferimento sia a problemi che richiedono un singolo risultato, sia a problemi che ne richiedono molteplici; inoltre specifica se deve essere, ad esempio, a colori, in che punto dello schermo. Nel caso in cui siano richieste più soluzioni, sarà necessario aggiungere delle informazioni per ogni soluzione.

---

## Progettare la sequenza di azioni per risolvere il problema

Dopo aver analizzato il problema, si inizia a scrivere l'algoritmo:

1. Individuare la sequenza di passi da compiere per risolvere il problema (algoritmo)
2. Verificare manualmente che l'algoritmo sia corretto
3. Nella scrittura dell'algoritmo conviene procedere in maniera top-down, individuare prima i passi principali e poi risolvere ognuno di essi separatamente.

---

## Realizzare la sequenza di azioni

Dopo la progettazione, si passa a scrivere l'effettivo programma:

1. Scrivere il programma traducendo ogni passo dell'algoritmo in una o più istruzioni del linguaggio di programmazione.

La conoscenza di un linguaggio è fondamentale, ma se non si è in grado di scrivere un algoritmo questa è inutile. Non ci deve essere mai un'istruzione di un linguaggio di programmazione nell'algoritmo.

---

## Fare il test e la verifica del programma

Successivamente si effettuano dei test del programma. È una fase fondamentale per far in modo che il programma non abbia eventuali problemi:

1. Eseguire diversi casi di test per verificare che il programma funzioni correttamente in ogni situazione possibile

È l'operazione più costosa in termini di tempo, infatti testare ogni possibile operazione che l'utente può effettuare diventa poderoso.

---

## Fare la manutenzione e l'aggiornamento del programma

L'ultimo passaggio è praticamente inutile durante questo corso, ma è fondamentale quando si andranno a progettare software per la vendita. Fare manutenzione vuol dire:

1. Correggere eventuali errori riscontrati successivamente;
2. Aggiornare il programma a fronte di modifiche delle specifiche del problema.

Degli errori possono sorgere più avanti nel tempo. Questa fase si protrae nel tempo per tutta la durata di vita del programma.

Ad esempio, i programmi di contabilità sono soggetti a molti cambiamenti perché l'IVA cambia valore nel tempo.

---

## Esempio: Conversione da miglia a chilometri

Problema: Supponiamo di avere delle cartine stradali, alcune con le indicazioni delle distanze in miglia e altre in chilometri. Vogliamo convertire tutte le distanze in chilometri.

Analisi:

-   Capire cosa fare: dobbiamo convertire dei valori da un sistema di misura ad un altro. In particolare dalle miglia ai chilometri. Il dato da elaborare è quindi una distanza in miglia. Il risultato desiderato è la distanza in chilometri
-   Per risolvere il problema ci serve sapere la relazione esistente tra miglia e chilometri. Un miglio equivale a $1\,609$ chilometri.

<u>**INPUT:**</u>

-   $\text{\small mi}$, la distanza espressa in miglia

<u>**OUTPUT:**</u>

-   $\text{\small km}$, la distanza espressa in chilometri

<u>**VINCOLI:**</u>

-   $1 \text{ \small mi} = 1\,609 \text{ \small km}$

---

## Progettazione

Algoritmo iniziale:

1. Acquisire la distanza in miglia;
2. Convertire la distanza in chilometri:
3. Visualizzare la distanza in chilometri;

---

## Raffinamenti

I passi 1. e 3. non necessitano di ulteriori raffinamenti. Il passo 2., anch'esso abbastanza elementare, può essere comunque ulteriormente dettagliato:

-   la distanza in chilometri è uguale a $1\,609$ volte la distanza in miglia

---

## Algoritmo con raffinamenti

1. Acquisire la distanza in miglia
2. Convertire la distanza in chilometri
    1. la distanza in chilometri è uguale a $1\,609$ volte la distanza in miglia
3. Visualizzare la distanza in chilometri

---

## Verifichiamo manualmente

Supponiamo di acquisire la distanza $10.0 \text{ \small mi}$ al passo 1. Al passo 2. il valore viene moltiplicato per il fattore di conversione $(1\,609 / 10.0)$ dando come risultato $16.09 \text{ \small km}$. Al passo 3. questo valore viene visualizzato come risultato desiderato.

---

## Realizzazione

```C
/***** La faremo in seguito *****/
```

---

## Verifica e test

Conviene provare a eseguire il programma realizzato con vari valori di input. Vedremo in seguito un metodo per scegliere i valori più adatti

---

---

# Esercizi

<!-- [Esercizi del 9.10.21 – Problem solving](https://www.notion.so/Esercizi-del-9-10-21-Problem-solving-806555123eb649388cf2a465c9e972dd) -->

[Esercizi del 9.10.21 – Problem solving](./ex/ex_9-10-21_problem_solving.md)
