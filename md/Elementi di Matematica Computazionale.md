# **Elementi** di Matematica Computazionalezzzz

## Logica

La logica è la disciplina che studia la condizioni di correttezza di un ragionamento.

Per far ciò possiamo pensare ai sillogismi, ad esempio:

```
Tutti gli uomini sono mortali ⇒ Socrate è un uomo ⇒ Socrate è mortale
```

Attraverso una serie di deduzioni logiche possiamo arrivare alle seguenti conclusioni:

```
Antonio, Bruno e Carlo sono indecisi se andare al cinema. Sappiamo che:
1. Se Corrado va al cinema allora anche Antonio ci andrà
2. Condizione necessaria affinchè Antonio vada al Cinema è che ci vada Bruno
```
Possiamo quindi affermare che:
```
1. Se Corrado è andato al cinema allora anche Bruno;
2. Nessuno è andato al cinema;
3. Se Bruno è andato al cinema allora anche Corrado;
4. Se Corrado non è andato al cinema allora Bruno non è andato nemmeno. 
```



-----



## Calcolo Proposizionale

Una proposizione è un enunciato dichiarativo che "afferma qualcosa" e che deve sottostare ad alcune proprietà inderogabili:

- **Principio del terzo escluso**
​	Che è vero oppure falso, non può esserci una via di mezzo, niente terza opzione.
- **Principio di non contraddittorietà**
​	Che non può essere sia vero che falso al tempo stesso.

Le proposizioni sono essenzialmente divisibili in due categorie:

| <span style="color:#163055">Atomiche</span> | <span style="color:#163055">Non Atomiche</span> |
| :-----------------------------------------: | :---------------------------------------------: |
|         Roma è la capitale d'Italia         |                   Che ora è?                    |
|                  1 + 1 = 2                  |           Leggi questo con attenzione           |

La differenza è che le proposizioni atomiche possono essere vere oppure false, 1 o 0, quelle non atomiche invece hanno risposte diverse.



-----



## Gli elementi della logica

**I connettivi logici** servono a collegare o unire due proposizioni.

| <span style="color:#163055">Connettivo</span> | <span style="color:#163055">Simbolo</span> | <span style="color:#163055">Operazione</span> |
| :-------------------------------------------: | :----------------------------------------: | --------------------------------------------- |
|                      NOT                      |                     ¬                      | Negazione                                     |
|                      AND                      |                     ∧                      | Congiunzione                                  |
|                      OR                       |                     V                      | Disgiunzione                                  |
|                Se... allora..                 |                   &rArr;                   | Implicazione                                  |
|              ...Se e solo se...               |                     ≡                      | Equivalenza                                   |
|                   ...Se...                    |                   &lArr;                   | Conseguenza                                   |

Ad esempio:

```
- Se P è vera, ¬P allora sarà falsa.
- P ∧ Q = T
```

**Gli identificatori** invece identificano una proposizione in modo più semplice, ad esempio:

```
"Antonio va al cinema" diventerà A
"Bruno va al cinema" diventerà B
```

[^ndr]: Nelle proposizioni chiameremo gli identificatori come atomi

**I simboli** sono esattamente ciò che dicono di essere, ovvero, simboli. Essi ci aiutano a capire la veridicità di una proposizione con T pre indicare Vero ed F per indicare Falso.

----



## Tautologie e Contraddizioni

Lo scopo dei problemi del calcolo proposizionale si riduce alla dimostrazione della traccia come tautologia, ma cos'è una tautologia?

Una **tautologia** è una formula del calcolo proposizionale che per ogni valore assegnato sarà sempre Vera.

Ad esempio:

```
P ∧ ¬P = T
```

Al contrario, una **contraddizione** sarà sempre False per ogni valore assegnato.

Ad esempio:

```
P V ¬P = F 
```

Le tautologie fanno parte di implicazioni ed equivalenze.

Ad esempio:

```
P implica tatuologicamente Q se P ⇒ Q è vera;
P è tautologicamente equivalente a Q se P ≡ Q.
```



#### Come si dimostra una tautologia

Per dimostrare che P è una tautologia possiamo ricorrere a più metodi:

1. Utilizzare una tabella di verità in cui controllare uno per uno tutte le possibilità (metodo più semplice ma non utilizzabile in sede d'esame);

   Ad esempio:

   | <span style="color:#163055">P</span> | <span style="color:#163055">Q</span> | <span style="color:#163055">P∧Q</span> |
   | :----------------------------------: | :----------------------------------: | :------------------------------------: |
   |                 Vero                 |                 Vero                 |                  Vero                  |
   |                 Vero                 |                Falso                 |                 Falso                  |
   |                Falso                 |                 Vero                 |                 Falso                  |
   |                Falso                 |                Falso                 |                 Falso                  |

   Abbiamo analizzato tutte le possibilità e possiamo notare come P∧Q non è una tautologia.

2. Cercando di costruire una dimostrazione facendo riferimento alle leggi già dimostrate, alle leggi di inferenza e impostando i tipi di dimostrazione;
3. Dimostrando che non è una tautologia individuando i valori che rendono la nostra proposizione falsa.

-----

## Le formule

Ora che abbiamo delle conoscenze di base, possiamo usare questo starter kit per iniziare a capire il meccanismo che c'è dietro alla formulazione delle proposizioni.

Un esempio di formula può essere:

```
(A and B) or C implica D or F, o in simboli: ( A ∧ B ) v C ⇒ D v F 
```

## I principi di sostituzione

I principi di sostituzione ci aiutano a semplificare le nostre formule per capire se esse possano essere dell tautologie o meno, e sono:

1. Principio di sostituzione per quivalenza
   $$
   \frac{A ≡ B}{C ≡ C[a/b]}
   $$

2. Principi di sostituzione per implicazione
   $$
   \frac{A ⇒ B∧A \quad occorre \quad positivamente \quad in \quad C }{C ⇒ C[a/b]}
   $$
   ​	Se A implica B ed A occorre positivamente in C, allora posso sostituire A con B.
   
   $$
   \frac{A ⇒ B∧A \quad occorre \quad negativamente \quad in \quad C }{C ⇐ C[a/b]}
   $$
   ​	Se A implica B ed A occorre negativamente in C, allora posso sostituire A con B.

Possiamo poi facilmente dedurre le seguenti affermazioni:

```
- A ⇒ A v B, perchè se A è vera allora A or B è vera;
- A ∧ B ⇒ A, perchè se A and B è vera allora A deve essere per forza vera.
```

Facciamo un esempio:

```
- (P ⇒ Q ∧ R) ⇒ (P ⇒ Q), per risolvere la traccia la dividiamo e prendiamo la prima parentesi;
Sappiamo da quanto visto prima che Q ∧ R ⇒ Q, possiamo quindi dedurre che (P ⇒ Q) ⇒ (P ⇒ Q), per qui una tautologia.
```

```
- (P v Q ⇒ R) ⇒ (P ⇒ Q), prendiamo la prima parentesi, e sappiamo dalla seconda formula che P ⇒ P v Q, quindi P ⇒ R, potremmo sostituire P con P v Q;
(P v Q ⇒ R) ⇒ (P ⇒ R)
```

Principio di risoluzione per la disgiunzione:

```
((P v Q) ∧ (P ⇒ R) ∧ (Q ⇒ S)) ⇒ (R v S)
```

```
- (P v Q) ∧ (¬P v R) ⇒ Q v R, riscrivo (¬P v R) come implicazione e quindi P ⇒ R;
(¬Q ⇒ P ) ∧ (P ⇒ R), per la transitività dell'implicazione possiamo dire che ¬Q ⇒ P ⇒ R e quindi Q ⇒ R;
Quindi abbiamo dimostrato che (Q v P) ∧ (¬P v R) ⇒ (Q v R)
```

---

## Forme Normali

Esiste un insieme **minimo** di operatori che sono in grado di formare una proposizione possono essere OR e NOT, NOT ed AND oppure NOT ed IMPLICAZIONE.

Si può minimizzare ulteriormente utilizzando soltanto il NAND.

```
A ⇒ B ≡ ¬A v B, quindi l'implicazione può essere sostituita con or e not;
A ≡ B ≡ A ⇒ B ∧ B ⇒ A, se A e B sono equivalenti allora uno implica l'altro;
A ∧ B ≡ ¬¬(A ∧ B) ≡ ¬(¬A v ¬B) o in caso contrario ↓↓↓
A v B ≡ ¬¬(A v B) ≡ ¬(¬A ∧ ¬B)
```

Diremo che la nostra formula sarà scritta in **forma standard:**

- **Congiuntiva**, (congiunzione di disgiunzione), quando è formata da (P1vP2v...)∧(Q1vQ2v...)∧...

- **Disgiuntiva**, (disgiunzione di congiunzioni), quando è formata da (P1∧P2∧...)v(Q1∧Q2∧...)v...

  P, Q o R rappresentano degli atomi o la loro negazione.

 ```
Esistono altri operatori che però non utilizzeremo, come:
- OR ESCLUSIVO, ⊕, "A ⊕ B" = (A ∧ ¬B) v (¬A ∧ B).
  L'or esclusivo restituisce vero solo se uno soltanto dei due operatori è vero.
- NAND, ⊙, "A ⊙ B" = ¬(A ∧ B) = ¬A v ¬B.
  Il nand, o not and, restituisce vero se l'and è falso e viceversa
 ```

-----

## Esercizio

Proviamo a dimostrare che (A ⇒ B) è una tautologia.

```
A ⇒ B possiamo riscriverla come (T ∧ A) ⇒ (B v F) perchè mettendo in and True non cambia il valore, e mettendo False in un or non cambia, abbiamo riscritto la stessa formula in un altro modo.
Ora, sapendo che il corpo è una congiunzione e la testa una disgiunzione possiamo spostare i singoli elementi da una parte all'altra facendo le opportune modifiche.
Possiamo riscrivere (A1 ∧ A2) ⇒ (B1 v B2 ) come (A1 ∧ ¬B2) ⇒ (B1 v ¬A2), quindi A ⇒ B può essere riscritta come T ⇒ B v ¬A oppure come A ∧ ¬B ⇒ F
```

E' facile intuire che se P ⇒ Q è una tautologia, allora P ∧ ¬Q ⇒ F sarà una contraddizione.

---

## Dimostrazione per assurdo

Supponiamo di avere una formula, P ⇒ Q, e volessimo dimostrare che sia una tautologia, potremmo ricorrere alla dimostrazione per assurdo asserendo la formula come falsa.

P ⇒ Q ≡ P ∧ ¬Q ⇒ F, diciamo che per assurdo che la formula implichi il falso.
Se lo scopo è dimostrare che la formula P → Q è una tautologia, possiamo farlo seguendo la strada opposta, ovvero dimostrando che la sua negazione, in questo cas P ∧ ¬Q → F è una contraddizione.

