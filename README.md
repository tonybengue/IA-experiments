# Github

## Synthaxe Markdown
https://www.markdownguide.org/basic-syntax/

## Basiques  
https://git-scm.com/book/fr/v2  
https://help.github.com/en/articles/adding-an-existing-project-to-github-using-the-command-line  
https://carlchenet.com/debuter-avec-git-partie-5-fusionner-des-branches/

.git : Mécanique de git
.gitignore : Fichiers à ignorer sur le serveur distant

## Aide
> `git help`
> `git help commande`

## Configuration
Régler email
> `git config --global user.email "votreEmail"`

Régler nom
> `git config --global user.name "votre nom"`

Affichage couleurs
> `git config --global color.ui true` 

(OPTIONNEL) Lier le repot local au repos distant
> `git remote add origin https://github.com/tonybengue/repoToLink.git`

### Démarche standarde
(OPTIONNEL) Dans le dossier courant pour initialiser un dossier .git ou le + dans l'onglet de Contrôle de version
> `git init`

Un U (unstaged) apparait dans le logiciel de contrôle de version pour signalé que le fichié n'est pas traqué.  
Appuyez sur + pour mettre en attente le fichier ou lancer
> `git add nomFichier"`  

Conseillé de commiter / valider avec message a chaque modification même si l'on peut laisser quelques fichier en zone de transit (staging area)
> `git commit -m "Message"`  

Envoyer sur la branche master
> `git push -u origin master`

### Remote
Changer de remote  
https://help.github.com/en/articles/changing-a-remotes-url

> `git remote set-url origin https://github.com/tonybengue/new_repo.git`

Verifier repo distant lié
> `git remote -v`

Effacer repo distant lié
> `git remote rm repoToDelete`

### Working tree / Espace de travail
La où se situent les fichiers untracked

Statut en cours (Working tree et stating area)
> `git status`  
> `git status --long`

### Zone de transit / Staging area
Ajoute le fichier à track
> `git add nomFichier`

Ajoute tous les fichiers à track du working tree
> `git add .`
> `git add --all`

Ajoute tous les fichiers à track du working tree avec l'extension voulue
> `git add ".html"`

Montre la différence entre tous les fichiers modifiés dans la zone d'attente et working tree
> `git diff`

Voir modifications sur un fichier
> `git diff nomFichier`

Voir modifications dans la staging area
> `git diff --staged`

### Commits
C'est ce qui va être envoyé sur Github. Apres un commit la staging area se vide.

Commiter avec editeur Vim
> `git commit`

Commiter le/les éléments de la staging area / zone de transit avec un message
> `git commit -m "message du commit"`

Commiter automatiquement les fichiers à stager
> `git commit -a -m "message du commit"`

Voir informations du repository local
> `git ls-tree --full-tree -r HEAD`

Voir les commit 
> `git log`
Voir les commit de manière condensée
> `git log --oneline`
Voir le commit traqué
> `git log nomCommit`
Voir le commit pour le fichier
> `git log -n 1 -p nomFichier`
    puis la touche q pour quitter

### Branches
Voir les branches
> `git branch`

Créer une nouvelle branche
> `git branch nouvelleBranche`

Se positionner sur la branche souhaitée
> `git checkout nouvelleBranche`

Créer et se positionner sur la nouvelle branche
> `git checkout -b maBranche`

Supprime une branche ( si pas de commit )
> `git branch -d maBranche`

#### Clonage de branche
On se positionne sur la branche mère
> `git checkout brancheMere`

#### Fusion de branches
https://github.com/adrienjoly/cours-git/blob/master/tutos/conflit-de-fusion.md

Puis on se positionne sur la branche fille
> `git merge brancheFille`

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

### Revenir en arrière
Revenir à un commit précédent pour le visionner ( tous fichiers ) 
> `git checkout numCommit`
Revenir en arrière pour le fichier voulu à tel commit en le stagant
> `git checkout numCommit nomFichier`

Défait ce qui avait était commité en créant un nouveau commit (pas de perte d'historique)
> `git revert numCommit`

Annule tous les fichiers en zone d'attente
> `git reset`
Annule le fichier en zone d'attente
> `git reset HEAD nomFichier`
> `git reset -- nomFichier`
Revenir au dernier commit précédent en vidant la staging area et les modifications
> `git reset --hard`
Revenir au commit souhaité mais laisse les modifications ajoutées au staging
> `git reset numCommit`
Revenir au nombre de commit suivant le ^ en laissant les modifications dans la staging area (défaut)
> `git reset HEAD^ --mixed`
Revenir au nombre de commit suivant le ^ en mettant les modifications dans la staging area 
> `git reset HEAD^ --soft`
Revenir au nombre de commit suivant le ^ en supprimant les modifications effectuées depuis
> `git reset HEAD^ --hard`

### Modifier historique
https://www.youtube.com/watch?v=dnJ8Z1bpKCA&list=PLjwdMgw5TTLXuY5i7RW0QqGdW0NZntqiP&index=8