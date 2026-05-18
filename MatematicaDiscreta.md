# Matematica discreta

## Indice

1. [Parte 1 - Matematica discreta](#parte-1---matematica-discreta)
    1. [Contare](#contare)
    2. [Insiemi](#insiemi)
    3. [Relazioni](#relazioni)
    4. [Funzioni](#funzioni)
    5. [Induzione](#induzione)
    6. [Sommatorie](#sommatorie)
    7. [Probabilità](#probabilità)
    8. [Matematica degli interi](#matematica-degli-interi)
    9. [Parità e disparità](#parità-e-disparità)
    10. [Principio della piccionaia](#principio-della-piccionaia)
    11. [Principio di somma e del prodotto](#principio-di-somma-e-del-prodotto)
    12. [Principio di inclusione-esclusione](#principio-di-inclusione-esclusione)
    13. [Teoria dei Grafi](#teoria-dei-grafi)
2. [Parte 2 - Algebra lineare](#parte-2---algebra-lineare)
    1. [Spazio $\mathbb{R}^n$](#spazio-mathbbrn)
        1. [Definizioni base](#definizioni-base)
        2. [Operazioni e confronti tra n-ple](#operazioni-e-confronti-tra-n-ple)

## Parte 1 - Matematica discreta

### Contare

### Insiemi

**Insieme**: concetto porimitivo, collezione di oggetti detti elementi
**Cardinalità $|A|$**: numero di elementi di un insieme $A$
**Insieme vuoto $\emptyset$**: insieme senza elementi, $|\emptyset| = 0$
**A sottoinsieme di B**: $A \subseteq B$ se ogni elemento di A è anche in B
**prodotto cartesiano $A \times B$**: insieme di tutte le coppie $(a, b)$ con $a \in A$ e $b \in B$

### Relazioni

**riflessiva**: $x \smile x\ \forall x$
**antiriflessiva**: $\neg (x \smile x)\ \forall x$

**simmetrica**: $x \smile y \implies y \smile x$
**antisimmetrica**: $x \smile y\ \implies \neg (y \smile x)$

**transitiva**: $(x \smile y) \land (y \smile z) \implies (x \smile z)$

**D'ORDINE**: irriflessiva, antisimmetrica e transitiva
**D'EQUIVALENZA**: riflessiva, simmetrica e transitiva

Le relazioni d'equivalenza implicano una partizione dell'insieme in classi di equivalenza

#### Congruenza modulo $n$ $x \equiv_n y$

Resto della divisione intera tra due numeri

$12 \mod 3 = 0$ | $-12 \mod 3 = 0$
$13 \mod 3 = 1$ | $-13 \mod 3 = 2$
$14 \mod 3 = 2$ | $-14 \mod 3 = 1$

dato $x \equiv_n y$ allora:

- $x-y \equiv_n 0$
- $x + z \equiv_n y + z$
- $x \cdot z \equiv_n y \cdot z$

considerando anche $z_1 \equiv_n z_2$:

- $x+z_1 \equiv_n y+z_2$
- $x \cdot z_1 \equiv_n y \cdot z_2$

### Funzioni

**iniettiva**: $x \neq x' \implies f(x) \neq f(x')$
**suriettiva**: $f: A \to B\ f(A) = B $
**biiettiva**: iniettiva e suriettiva, invertibile

**ceiling**: $\lceil x \rceil = \min \{v \in \mathbb{Z} : v \geq x\}$ più piccolo intero maggiore o uguale a $x$
**floor**: $\lfloor x \rfloor = \max \{v \in \mathbb{Z} : v \leq x\}$ più grande intero minore o uguale a $x$

**composta**: $f \circ g(x) = f(g(x))$

### Induzione

- Base: $P(0)$ è vera
- Passo induttivo: $ \forall n \geq 0,\ P(n+1)\ vera \implies P(n)\ vera$

### Sommatorie

$$ \sum_{k=1}^n a_k\ = a_1 + a_2 + \ldots + a_n $$

#### Regole

$ \sum_{k \in K}\ \textbf{c} \cdot a_k = \textbf{c} \cdot \sum_{k \in K}\ a_k $

$ \sum_{k \in K}\ (a_k + b_k) = \sum_{k \in K}\ a_k + \sum_{k \in K}\ b_k $

$ \sum_{k \in K}\ a_k = \sum_{\Pi (k) \in K}\ a_{\Pi(k)} $

$ \sum_{k=1}^\textbf{m}\ a_k + \sum_{k = \textbf{m}}^n\ a_k = a_{\textbf{m}} + \sum_{k=1}^n\ a_k $

$\sum_{k \in K}\ a_k = \sum_{(k + c) \in K}\ a_{(k + c)} $

$\sum_{k = 1}^n\ a_k = \sum_{k = 1}^{\textbf{m}}\ a_k + \sum_{k = \textbf{m+1}}^n\ a_k $

#### Somme multiple

$$\begin{matrix} a_1 b_1 & a_1 b_2 & a_1 b_3 \\ a_2 b_1 & a_2 b_2 & a_2 b_3 \\ a_3 b_1 & a_3 b_2 & a_3 b_3 \end{matrix}$$

| tipologia | formula | estesione |
| --- | --- | --- |
| per righe | $$\sum_{i=1}^3\ \sum_{j=1}^3\ a_i b_j$$ | $$a_1 \sum_{j=1}^3 b_j + a_2 \sum_{j=1}^3 b_j + a_3 \sum_{j=1}^3 b_j$$ |
| per colonne | $$\sum_{j=1}^3\ \sum_{i=1}^3\ a_i b_j$$ | $$ \sum_{i = 1}^3 (a_i)\ b_1 + \sum_{i = 1}^3 (a_i)\ b_2 + \sum_{i = 1}^3 (a_i)\ b_3 $$ |

#### Scambio di indici

$$ \sum_{i \in I} \sum_{j \in J(i)} a_{ij} = \sum_{j \in J} \sum_{i \in I(j)} a_{ij} $$

| $$\sum_{i=0}^n \sum_{j=i}^n s_ij$$ | $$\sum_{j=0}^n \sum_{i=0}^j s_ij$$ |
| --- | --- |

$J(i) = \{0, \ldots, n\}$
$I(j) = \{0, \ldots, j\}$

#### Somme notevoli

- somma numeri consecutivi: $$\sum_{i=1}^n i = \frac{n(n+1)}{2}$$

- somma quadrati numeri consecutivi: $$\sum_{k=1}^n k^2 = \frac{n(n+1)(2n+1)}{6}$$

- somma potenze consecutive: $$\sum_{k=1}^n k^m = \frac{1}{m+1} \sum_{j=0}^m \binom{m+1}{j} B_j n^{m+1-j}$$

#### Metodo di perturbazione

$$ s_n + a_{n+1} = \sum_{k=0}^{n+1} a_k = \sum_{k=0}^n a_{k+1} $$

$$ s_n + a_{n+1} = a_0 + \sum_{k=0}^n a_{k+1} $$

$s(n)$ sia a sinistra che a destra ma con coefficienti diversi per non elidersi

### Probabilità

**universo $S$**: $Pr(S) = P|S| = 1$

**distribuita uniforme**: $Pr(A) = p|A|= \frac{|A|}{|S|}$

**probabilità condizionata**: $Pr(A|B) = \frac{Pr(A \cap B)}{Pr(B)}$

**probabilità eventi indipendenti**: $Pr(A \cap B) = Pr(A) \cdot Pr(B)$

**teorema di Bayes**: $Pr(B|A) = \frac{Pr(A|B) \cdot Pr(B)}{Pr(A)}$

### Matematica degli interi

**divisibilità:** $a|b$ se $\exists m \in \mathbb{Z} : \textbf{b =}\ \textbf{a} \cdot \textbf{m}$

**MCD (a,b)**: $ \max \text{\{divisori a,b\}} $
**mcm (a,b)**: $ \min \text{\{multipli a,b\}} $

**Algoritmo di Euclide**:

Calcolo di $MCD(a,b)$

1. $a : b = r$
2. $r = 0 \implies MCD(a,b) = b $
3. $r \neq 0 \implies b : r = ... $ (ricomincio)

**Teorema di Bezout**: $MCD(a,b) = ax + by$
 $1 = ax + by$ allora $a$ e $b$ sono coprimi

### Parità e disparità

#### Segno permutazioni

### Principio della piccionaia

### Principio di somma e del prodotto

#### Principio di somma

#### Principio di prodotto

#### Combinazioni

#### Coefficiente binomiale

#### Triangolo di Pascal

#### Processi Bernoulliani

#### Disposizioni (insiemi ordinati)

#### Multinsiemi (insiemi con elementi ripetuti)

#### Combinazioni con ripetizioni

### Principio di inclusione-esclusione

#### Principio base

#### Spiazzamenti

### Teoria dei Grafi



## Parte 2 - Algebra lineare

### Spazio $\mathbb{R}^n$

#### Definizioni base

**SPAZIO N-DIMENSIONALE**: insieme $\mathbb{R}^n = \{(x_1, x_2, \ldots, x_n) : x_i \in \mathbb{R}\}$ con $n \geq 1$

**n-pla**: punto dello spazio n-dimensionale, composta da $n$ componenti $x_i$

**origine $O$**: n-pla di 0, $O = (0, 0, \ldots, 0)$, punto di riferimento da cui partono le coordinate

#### Operazioni e confronti tra n-ple

**UGUAGLIANZA**: tutte le componenti devono essere uguali.
Dati due n-ple $A = (a_1, a_2, \ldots, a_n)$ e $B = (b_1, b_2, \ldots, b_n)$
$A = B \iff (a_1 = b_1) \land (a_2 = b_2) \land \ldots \land (a_n = b_n)$.

**SOMMA**: n-pla somma ha come componenti la somma delle rispettive componenti

**proprietà somma**:

- commutativa: $(a+b)=(b+a)\ \forall a,b  \in \mathbb{R}^n$
- associativa: $(a+b)+c = a+(b+c) \forall a,b,c \in \mathbb{R}^n$
- elemento neutro $O$: $a+O = a \forall a \in \mathbb{R}^n$
- elemento opposto $-A$: $a+(-a) = O \forall a \in \mathbb{R}^n$

**PRODOTTO N-PLA $\cdot$ SCALARE**: n-pla risultante ha come componenti le componenti della n-pla originaria moltiplicate per lo scalare

$$ z = \lambda \cdot a \iff z_i = \lambda \cdot a_i\ \forall i = 1, \ldots, n $$

**proprietà prodotto n-pla $\cdot$ scalare**:

- distributivo: $$\lambda \cdot (a+b) = \lambda \cdot a + \lambda \cdot b \forall \lambda \in \mathbb{R}, a,b \in \mathbb{R}^n$$
- elemento neutro: $$1 \cdot a = a \forall a \in \mathbb{R}^n$$

**PRODOTTO SCALARE**:
