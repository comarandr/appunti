# Matematica discreta

## Indice

1. [Parte 1 - Matematica discreta](#parte-1---matematica-discreta)
    1. [Insiemi](#insiemi)
2. [Parte 2 - Algebra lineare](#parte-2---algebra-lineare)
    1. [Spazio $\mathbb{R}^n$](#spazio-mathbbrn)
        1. [Definizioni base](#definizioni-base)
        2. [Operazioni e confronti tra n-ple](#operazioni-e-confronti-tra-n-ple)

## Parte 1 - Matematica discreta

### Insiemi

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

**PRODOTTO SCALARE**