# Breve guida a Python

## gestione script python

- modulo: file che contiene definizioni e istruzioni python (.py)
- nome modulo: variabile globale `__name__`
- importare un modulo: `import nome_modulo`
- usare funzione modulo: `nome_modulo.nome_funzione()`
- importare una funzione specifica: `from modulo import funzione`, * importa tutte funzioni

## base

- commenti: `# commento`
- assegnamento di variabili: `a = 5`
- assegnamento multiplo: `a,b = 5, 6` oppure `a = b = 5`
- gestione booleani: 0 falso, altro vero
- stampa: `print('ciao')`

## aritmentica

- operazioni matematiche: + - * /
- numeri complessi: `1 + 2j` oppure `complex(1, 2)`
- conversione di tipi: `int(3.14)` oppure `float(3)`
- ultima espressione assegnata `_`

## stringhe

- dichiarazione `'stringa uno'` oppure `"stringa due"`
- quoting `\"`
- stringhe su più riche: uso del carattere `\n\` quando salto di riga
- posso usare `r` per evitare l'escape dei caratteri speciali, es. `ciao = r"ciao\n\come\n\stai?"`
- escape caratteri speciali anche con `'''` o circondate da ulteriori `"`
- concatenazione di stringhe: `a + b`
- concatenazione di ripetizine di stringa: `stringa* 3`
- stringhe dichiarate consecutivamente vengono concatenate: `'str' 'in' 'ga'` &rarr; `'stringa'`
- indicizzazione: `stringa[posizione]`
- indicizzazione a fette: `stringa[inizio:fine:step]`
- se indice posizione omesso all'inizio, parte da 0 `stringa[:2]` &rarr; `'ci'`
- se indice posizione omesso alla fine, arriva fino alla fine `stringa[2:]` &rarr; `'ao'`
- proprietà utile: `s[:i] + s[i:]` &rarr; `s`
- indicizzazione negativa: parte dal fondo `stringa[-1]` &rarr; `'a'`
- NOTA: intervalli di indicizzazioni vengono troncati se fuori intervallo
- stringhe NON possono essere modificate
- lunghezza della stringa: `len(stringa)`
- stringa unicode: `u'ciao'`

```python
stringa = 'ciao'
stringa[0] 
>> c
stringa[1:3]
>> ia
```

## liste

- dichiarazione: `lista = [1, 'stringa'', 3]`
- indicizzazione: `lista[posizione]` come nelle stringhe
- indicizzazione a fette: `lista[inizio:fine:step]` come nelle stringhe
- sono mutabili, anche attraverso indicizzazione a fette: `lista[0:2] = ['nuovi', 'elementi']`
- lunghezza della lista: `len(lista)`

## istruzione if

```python
if condizione:
    print('condizione vera')
elif altra_condizione:
    print('altra condizione vera')
else:
    print('nessuna condizione vera')
```

- `elif` e `else` sono opzionali, `elif` a cascata sostituiscono switch-case

## istruzione for

```python
for elemento in lista:
    print(elemento)
```

## funzione range

- `range(n)` genera una sequenza di numeri da 0 a n-1
- `range(n, m)` genera una sequenza di numeri da n a m-1
- `range(n, m, s)` genera una sequenza di numeri da n a m-1 con passo s
- `for i in range(len(a)): print(a[i])` &rarr; stampa tutti gli elementi di a

```python
>>> range(5)
[0, 1, 2, 3, 4]
>>> range(2, 5)
[2, 3, 4]
>>> range(2, 10, 2)
[2, 4, 6, 8]
>>> a = ['Mari', 'had', 'a', 'dog']
>>> for i in range(len(a)):
...     print i,(a[i])
0 Mari
1 had
2 a
3 dog
```

## istruzioni break, continue, else

- `break` interrompe il ciclo
- `continue` prosegue con l'iterazione seguente del ciclo
- `else` esegue un blocco di codice se il ciclo termina senza `break`

## istruzione pass

- `pass` è un'istruzione nulla, utile per evitare errori di sintassi

## funzioni e metodi

- definizione di una funzione: `def funzione(parametro):`
- funzione con più parametri: `def funzione(parametro1, parametro2):`
- ciclo si basa su indentazione
- ritornare valori, `return`
- metodi: `oggetto.metodo()`

## input

- si usa il comando `input()` per leggere da tastiera
- `input()` restituisce una stringa
- per convertire in intero si usa `int(input())`
- per ammettere input multipli si usa `input().split()`
