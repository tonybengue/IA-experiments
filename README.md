# Github

## Synthaxe Markdown
https://www.markdownguide.org/basic-syntax/

## Basique  
https://git-scm.com/book/fr/v2
https://help.github.com/en/articles/adding-an-existing-project-to-github-using-the-command-line

### Démarche standarde
(OPTIONNEL) Dans le dossier courant pour initialiser un dossier .git ou le + dans l'onglet de Contrôle de version
> `git init`

Un U (unstaged) apparait dans le logiciel de contrôle de version pour signalé que le fichié n'est pas traqué.  
Appuyez sur + pour mettre en attente le fichier ou lancer
> `git add nomFichier"`  

Conseillé de commiter / valider avec message a chaque modification même si l'on peut laisser quelques fichier en zone de transit (staging area)
> `git commit -m "Message"`  

(OPTIONNEL) Lier le repot local au repos distant
> `git remote add origin https://github.com/tonybengue/repoToLink.git`

Envoyer sur la branche master
> `git push -u origin master`

### Working tree / Espace de travail
La où se situent les fichiers untracked

Statut en cours (Working tree et stating area)
> `git status`

### Zone de transit / Staging area
Ajoute le fichier à track
> `git add nomFichier`

Ajoute tous les fichiers à track du working tree
> `git add .`

### Commits
C'est ce qui va être envoyé sur Github. Apres un commit la staging area se vide.

Voir informations du repository local
> `git ls-tree --full-tree -r HEAD`

Voir tous les fichiers traqués par le repo
> `git log puis la touche q pour quitter`

Commiter le/les éléments de la staging area / zone de transit
> `git commit -m "message du commit"`

### Remote
Changer de remote  
https://help.github.com/en/articles/changing-a-remotes-url

> `git remote set-url origin https://github.com/tonybengue/new_repo.git`

Verifier repo distant lié
> `git remote -v`

Effacer repo distant lié
> `git remote rm repoToDelete`

### Branches
Voir les branches
> `git branch`

Créer une nouvelle branche
> `git branch nouvelle-branche`

Se positionner sur la branche souhaitée
> `git checkout nouvelle-branche`

Créer et se positionner sur la nouvelle branche
> `git checkout -b ma-branche`

#### Clonage de branche
On se positionne sur la branche mère
> `git checkout brancheMere`

Puis on se positionne sur la branche fille
> `git merge bracnheFille`

#### Remisage
https://git-scm.com/book/fr/v1/Utilitaires-Git-Le-remisage

Remise le code en cours (si on veut changer de branche sans commit)
> `git stash`

Liste les stash
> `git stash list`

Applique le dernier stash
> `git stash apply`  

Applique le stash n°
> `git stash apply@x`

