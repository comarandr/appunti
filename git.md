# BASE DI GIT

## Creare una repository

`git init` : Crea una nuova repository Git nella directory corrente
`git clone <url>` : Clona una repository esistente da un URL

## Salvare le modifiche

**area di staging** : è una zona temporanea dove si preparano i file prima di eseguire un commit

`git add <file>` : Aggiunge un file specifico all'area di staging

`git add .` : Aggiunge tutti i file modificati all'area di staging

`git commit -m "messaggio"` : Crea un commit con i file presenti nell'area di staging e un messaggio descrittivo

`git commit` : Apre l'editor predefinito per inserire un messaggio di commit dettagliato (riassunto + descrizione)

`git status` : Mostra lo stato dei file nella directory di lavoro (branch attivo, file modificati, file in staging, file non tracciati)

## Creare nuovi branch

`git branch` : Elenca i branch locali

`git branch <nome-branch>` : Crea un nuovo branch con il nome specificato

- `git branch -d <nome-branch>` : Elimina un branch (deve essere già unito o non avere modifiche non salvate)
- `git branch -D <nome-branch>` : Forza l'eliminazione di un branch anche se non è stato unito

`git switch [options] <nome-branch>` : Passa al branch specificato

- `git switch -c <nome-branch>` : Crea un nuovo branch e passa ad esso
  - `git switch -c name <base-branch>` : Crea un nuovo branch basato su altro branch e passa ad esso
- `git switch -` : Passa al branch precedente
- `git switch --detach <commit>` : Passa a un commit specifico in modalità detached HEAD (non associato a un branch)

`git checkout <nome-branch>` : Passa al branch specificato (spesso sostituito da switch)

- `git checkout -b <nome-branch>` : Crea un nuovo branch e passa ad esso
- `git checkout -d <nome-branch>` : Elimina un branch

## Spostarsi tra i commit

### visualizzare la cronologia dei commit

`git log` : Mostra la cronologia dei commit

`git log --oneline` : Mostra la cronologia dei commit in formato compatto (una riga per commit)

`git log --graph` : Mostra la cronologia dei commit con una rappresentazione grafica dei branch e dei merge

`git log --all` : Mostra la cronologia dei commit di tutti i branch

`git log --remote` : Mostra la cronologia dei commit dei branch remoti

### spostarsi in un commit specifico

`git checkout <commit>` : Passa a un commit specifico (modalità detached HEAD)

`git switch --detach <commit>` : Passa a un commit specifico in modalità detached HEAD (alternativa a checkout)

`git checkout <nome-branch>^` : Passa al commit genitore del branch specificato

`git checkout <nome-branch>~n` : Passa al commit n livelli sopra il branch specificato

### forzatura di un branch

`git branch -f <nome-branch> <commit>` : Forza il branch a puntare a un commit specifico (può causare perdita di dati se non usato con cautela)

- nota: \<commit> può anche essere un riferimento relativo `nome-branch~n` o `nome-branch^`

## Unire i branch

`git merge <nome-branch>`: Unisce il branch specificato nel branch attivo

in assenza di conflitti non sarà necessario risolvere manualmente le modifiche

`git rebase <nome-branch>`: Applica le modifiche del branch attivo sopra il branch specificato (riordina la cronologia)

1. creo il ramo secondario con la feature da sviluppare
2. mi sposto sul ramo secondario e faccio i commit
3. mentre sono sul ramo secondario, faccio un rebase del ramo principale per portare le modifiche più recenti
4. risolvo eventuali conflitti

## Sincronizzare con un repository remoto

`git remote add <nome-remoto> <url>` : Aggiunge un repository remoto con un nome specificato

`git push <nome-remoto> <nome-branch>` : Invia i commit del branch locale al repository remoto

`git pull <nome-remoto> <nome-branch>` : Recupera e unisce i cambiamenti dal repository remoto al branch locale

`git fetch <nome-remoto>` : Recupera i cambiamenti dal repository remoto senza unirli al branch locale

## Annullare le modifiche

`git reset <commit>` : Resetta il branch attivo a un commit specifico, annullando tutte le modifiche successive (perdita di dati)

`git revert <commit>` : Crea un nuovo commit che annulla le modifiche introdotte da un commit specifico (non altera la cronologia)

**nota**: \<commit> è il commit a cui si vuole tornare

## git cherry-pick

`git cherry-pick <commit>` : Applica le modifiche introdotte da un commit specifico al branch attivo (utile per portare modifiche specifiche da un branch all'altro senza unire tutto il branch)

`git rebase -i <nome-branch/commit>` : Interattivo, permette di modificare la cronologia dei commit (riordinare, unire, modificare messaggi)