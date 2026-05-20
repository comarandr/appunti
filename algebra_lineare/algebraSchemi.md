# ALgebra lineare

- n-pla: $(a_1, \ldots, a_n)$

## operazioni

- somma: $$(a_1 a_2 a_3) + (b_1 b_2 b_3) = (a_1 + b_1, a_2 + b_2, a_3 + b_3)$$
- prodotto con scalare: $$\lambda \cdot (a_1 a_2 a_3) = (\lambda \cdot a_1, \lambda \cdot a_2, \lambda \cdot a_3)$$
- prodotto scalare: $$<v \cdot w> = v_1 \cdot w_1 + v_2 \cdot w_2 + v_3 \cdot w_3$$
- norma (radice del prodotto scalare di sè stesso): $$||v|| = \sqrt{v_1^2 + v_2^2 + v_3^2} = \sqrt{<v \cdot v>}$$
- distanza (radice della norma della differenza): $$d(v, w) = \sqrt{(v_1 - w_1)^2 + (v_2 - w_2)^2 + (v_3 - w_3)^2} = \sqrt{||v - w||}$$
- disuguaglianza triangolare: $$||a + b|| \leq ||a|| + ||b||$$
- disuguaglianza di Cauchy-Schwarz:
$$|\sum_{i=1}^n a_i \cdot b_i| \leq ||a|| \cdot ||b||$$
$$|<a \cdot b>| \leq ||a|| \cdot ||b||$$

## formulette geometriche

**rette passanti per $O$**: $\mathcal{L}(v) = \{\lambda v : \lambda \in \mathbb{R}\}$ $\lambda$ parametro
**ortogonalità**: $<a \cdot b> = 0$ prodotto scalare nullo
**angolo tra due n-ple**: $$\alpha = arcos( \frac{<a \cdot b>}{||a|| \cdot ||b||})$$
**rete affini**: $\mathcal{L}(v) + w = \lambda v + w \quad \forall \lambda \in \mathbb{R}$
**retta per 2 punti**: $ (1 -\lambda)P = \lambda Q : (\lambda (P-Q) + P) $
**combinazione affine**: $\alpha P + \beta Q \mid \alpha + \beta = 1 $
**combinazione connessa**: $\alpha P + \beta Q \quad \alpha , \beta \in [0,1] \; \land \; \alpha + \beta = 1 $

## Risoluzioni geometria dello spazio

**equazione retta**: $\begin{cases} x = v_1 \cdot t + p_1 \\ y = v_2 \cdot t + p_2 \\ z = v_3 \cdot t + p_3 \end{cases}$

$t(v_1 v_2 v_3) + (p_1 p_2 p_3)$

**retta per $2$ punti**: $ t(B-A) + A $

$\begin{cases} x = (b_1 - a_1) \cdot t + a_1 \\ y = (b_2 - a_2) \cdot t + a_2 \\ z = (b_3 - a_3) \cdot t + a_3 \end{cases}$

**spazio perpendicolare a $v (v_1 v_2 v_3)$**: $<v, x> = 0$
NB: in $\mathbb{R}^2$ è una retta

**spazio perpendicolare a $v (v_1 v_2 v_3)$ e passante per $P$**: $<v, x> = <v, P>$

**equazione del piano**: $\pi : ax + by + cz = d$

**retta perpendicolare al piano $\pi$**: $v = (a,b,c)$ perpendicolare al piano $\pi : ax + by +cz =d$
NB componenti vettori uguali a coefficienti piano

**retta passante per un punto $P(p_x, p_y, p_z)$ ovvero traslazione**: $d = a \cdot p_x + b \cdot p_y + c \cdot p_z$
$ax + by + cz = a \cdot p_x + b \cdot p_y + c \cdot p_z$

**piano contenente $2$ rette**: $\begin{cases} x = v_1 \cdot t + w_1 \cdot s \\ y = v_2 \cdot t + w_2 \cdot s \\ z = v_3 \cdot t + w_3 \cdot s \end{cases}$
forma parametrica da risolvere per ottenere forma cartesiana

**retta in $\mathbb{R}^2$ dati $2$ piani**: $r: \begin{cases} a_1 x + b_1 y + c_1 z = d_1 \\ a_2 x + b_2 y + c_2 z = d_2 \end{cases}$
parametrica (porre una variabile pari a t)

**rette parallele** $t(v_1 v_2 v_3) + Q; \quad s(v_1 v_2 v_3) + P $
stesso vettore direttore

**piano date due rette parallele**: serve un'altra direzione

**piano data una retta $r$ e un punto $A$**:

1. calcolo 2 punti della retta $r$
2. dati $P', P'' \in r$ e punto $A$ calcolo piano da rette $\vec{A P'}$ e $\vec{AP''}$

## Matrici

**matrice m x n** $A = \begin{bmatrix} a_{11} & a_{12} & \ldots & a_{1n} \\ a_{21} & a_{22} & \ldots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m1} & a_{m2} & \ldots & a_{mn} \end{bmatrix}$

m righe, n colonne

**matrice quadrata**: matrice con stesso numero di righe e colonne, appartenente a $\mathbb{R}^n$

**traccia**: $tr(A) = \begin{bmatrix} a_{11} & \ldots & \ldots & \ldots \\ \ldots & a_{22} & \ldots & \ldots \\ \vdots & \vdots & \ddots & \vdots \\ \ldots & \ldots & \ldots & a_{nn} \end{bmatrix}$

$$ tr(A) = \sum_{i=1}^n a_{ii} $$

**matrice diagonale**: matrice quadrata con tutti gli elementi nulli tranne quelli sulla diagonale principale

$$ D = \begin{bmatrix} \lambda_1 & 0 & \ldots & 0 \\ 0 & \lambda_2 & \ldots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \ldots & \lambda_n \end{bmatrix} $$

**matrice triangolare superiore**: matrice quadrata con tutti gli elementi nulli al di sotto della diagonale principale

$$ U = \begin{bmatrix} \lambda_{11} & x & \ldots & y \\ 0 & \lambda_{22} & \ldots & z \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \ldots & \lambda_{nn} \end{bmatrix} $$

**matrice triangolare inferiore**: matrice quadrata con tutti gli elementi nulli al di sopra della diagonale principale

$$ L = \begin{bmatrix} \lambda_{11} & 0 & \ldots & 0 \\ x & \lambda_{22} & \ldots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ y & z & \ldots & \lambda_{nn} \end{bmatrix} $$

**matrice trasposta**: matrice ottenuta scambiando righe e colonne di una matrice data

$$ A = \begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \\ \vdots & \vdots\\ a_{n1} & a_{n2} \end{bmatrix} \rarr A^T = \begin{bmatrix} a_{11} & a_{21} & \ldots & a_{n1} \\ a_{12} & a_{22} & \ldots & a_{n2} \end{bmatrix} $$

$$a_{ij} = (A^T)_{ji}$$

**matrice simmetrica**: matrice quadrata che è uguale alla sua trasposta, $A = A^T \implies a_{ij} = a_{ji}$

**matrice antisimmetrica**: matrice quadrata che è uguale alla trasposta con segno opposto, $A = -A^T \implies a_{ij} = -a_{ji}$

## operazioni tra matrici

- somma/differenza: $$(A + B)_{ij} = A_{ij} + B_{ij}$$

**prodotto matriciale $ A \in \mathbb{R}^{m \times n}, B \in \mathbb{R}^{n \times p} $**: $$ \begin{matrix} A_1 \\ A_2 \end{matrix} \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \end{bmatrix} \cdot \begin{bmatrix} b_{11} & b_{12} \\ b_{21} & b_{22} \\ b_{31} & b_{32} \end{bmatrix} = \begin{bmatrix} <A_1, B^1> & <A_1 , B^2> \\ <A_2, B^1> & <A_2, B^2> \end{bmatrix} $$

Nota bene: $AB \neq BA$ 

- $\exists AB \implies A \cdot (B+C) = AB + AC$
- $\exists BA \implies (B+C) \cdot A = BA + CA$

**matrice inversa**:

- **sinistra**: $A^{-1} A = I_n$
- **destra**: $A A^{-1} = I_n$
- **inversa matrice quadrata**: $A^{-1} A = A A^{-1} = I_n$

**calcolo matrice inversa**:

1. calcolo la matrice dei complementi algebrici 
2. trasposta della matrice dei complementi algebrici
3. divido per il determinante della matrice originale

**matrice ortogonale (quadrata)**: matrice $A$ tale che $A^T A = I_n$

**matrice simile (quadrata)**: matrice $C$ simile a matrice $A$ se esiste matrice invertibile $B$ tale che $C = B^{-1} A B$

stesso **endomorfismo** rappresentato in basi diverse

## Spazi vettoriali

**spazio vettoriale $V$**: $V \neq \emptyset$ con

- **somma**: $V \times V \quad v + w$
- **prodotto**: $\mathbb{R} \times V \rarr V \quad \lambda v$

**condizioni per essere spazio vettoriale**:

1. commutativa: $(u + v) + w = u + (v + w)$
2. elemento neutro somma: $v + 0 = v$
3. elemento opposto: $v + (-v) = 0$
4. $(\lambda + \delta) \cdot v = \lambda \cdot v + \delta \cdot v$
5. elemento neutro prodotto: $1 \cdot v = v$
6. $(\lambda \cdot \delta) \cdot v = \lambda \cdot (\delta \cdot v)$

**proprietà spazio vettoriale**:

**condizione sottospazio vettoriale**: $\lambda v + \mu w \in W \quad W \subseteq V$
NOTA: se $0 \not\in W$ allora $W$ non è sottospazio vettoriale
intersezione $W \cap U$ è sottospazio vettoriale

**combinazione lineare**: $ \lambda_1 v_1 + \lambda_2 v_2 + \ldots + \lambda_n v_n $ con $v_i$ vettori e $\lambda_i$ valori in $\mathbb{R}$

$$ w = \sum_{i=1}^n \lambda_i v_i $$
$w$ generato da $v_1, v_2, \ldots, v_n$

**inviluppo lineare**: insieme di tutte le combinazioni lineari di un insieme di vettori $S = \{v_1, v_2, \ldots, v_n\}$
$$ \mathcal{L}<W> = \mathcal{L}< v_1, v_2, \ldots, v_n > $$

**dipendeza lineare**: $ \lambda v_1 + \lambda_2 v_2 + \ldots + \lambda_n v_n = 0 $ con almeno un $\lambda_i \neq 0$

**indipendenza lineare**: $ \lambda v_1 + \lambda_2 v_2 + \ldots + \lambda_n v_n = 0 \iff \lambda_1 = \lambda_2 = \ldots = \lambda_n = 0$

**