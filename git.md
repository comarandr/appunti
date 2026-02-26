# BASE DI GIT

## Creare una repository

`git init` : Crea una nuova repository Git nella directory corrente
`git clone <url>` : Clona una repository esistente da un URL

## salvare le modifiche

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

## Unire i branch

`git merge <nome-branch>`: Unisce il branch specificato nel branch attivo

in assenza di conflitti non sarà necessario risolvere manualmente le modifiche

`git rebase <nome-branch>`: Applica le modifiche del branch attivo sopra il branch specificato (riordina la cronologia)
