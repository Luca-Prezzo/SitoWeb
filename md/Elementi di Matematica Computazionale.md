# Elementi di Matematica Computazionale

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

|          Atomiche           |        Non Atomiche         |
| :-------------------------: | :-------------------------: |
| Roma è la capitale d'Italia |         Che ora è?          |
|          1 + 1 = 2          | Leggi questo con attenzione |

La differenza è che le proposizioni atomiche possono essere vere oppure false, 1 o 0, quelle non atomiche invece hanno risposte diverse.



-----



## Gli elementi della logica

**I connettivi logici** servono a collegare o unire due proposizioni.

|     Connettivo     | Simbolo | Operazione   |
| :----------------: | :-----: | ------------ |
|        NOT         |    ¬    | Negazione    |
|        AND         |    ∧    | Congiunzione |
|         OR         |    V    | Disgiunzione |
|   Se... allora..   | &rArr;  | Implicazione |
| ...Se e solo se... |    ≡    | Equivalenza  |
|      ...Se...      | &lArr;  | Conseguenza  |

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

   |   P   |   Q   |  P∧Q  |
   | :---: | :---: | :---: |
   | Vero  | Vero  | Vero  |
   | Vero  | Falso | Falso |
   | Falso | Vero  | Falso |
   | Falso | Falso | Falso |

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
- (P → Q ∧ R) → (P → Q), per risolvere la traccia la dividiamo e prendiamo la prima parentesi;
Sappiamo da quanto visto prima che Q ∧ R → Q, possiamo quindi dedurre che (P → Q) → (P → Q), per qui una tautologia.
```

```
- (P v Q → R) → (P → Q), prendiamo la prima parentesi, e sappiamo dalla seconda formula che P → P v Q, quindi P → R, possiamo sostituire P con P v Q
```

