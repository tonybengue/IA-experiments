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

On se positionne sur la branche mère
> `git checkout mere`

Puis on se positionne sur la branche fille
> `git merge fille`

