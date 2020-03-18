## Github

### Fonctionnement de Git
Git est un gestionnaire de version développé par Linus Torvalds (qui a également développé Linux).

#### Pourquoi utiliser git?
Supposons que vous travaillez à plusieurs sur un projet, git vous permettra de créer une copie du projet, de faire des modifications, les sauvegarder et les fusionner avec celles de vos collègues en évitant toutes pertes et en conservant un historique de votre projet.

#### Et Github?
Github facilite l'utilisation de Git, son logiciel Github Desktop permet de gérer vos dépôts avec une interface graphique.
De plus il permet d'accéder à ses projets de n'importe où, de partager vos projets facilement avec d'autres personnes ou de parcourir les projets des autres utilisateurs ( on peut voir github comme un réseau social de développeur).
Vous pouvez télécharger, faire des copies ou forker n'importe quel projet public qui se trouve sur le site.

#### Un lexique pour commencer
  - **Contrôle de version :** Fonctionnalité de Git qui permet de sauvegarder des étapes du développement de votre projet
  - **Dépôt (ou repo pour repository):** répertoire dans lequel vous allez développer votre projet
  - **Commit :** la commande qui permet de créer un point de contrôle dans le développement de votre projet, vous pourrez ainsi restaurer votre projet à cette étape en cas de besoin.
  - **Branche :** afin de ne pas écraser le travail de vos collègues, Git permet de travailler sur des branches, il existe la branche principale du projet (Master) puis les branches que chaque utilisateur va créer (qui sera une copie de Master à un instant t) afin d'apporter ces modifications sans gêner le travail des autres pour ensuite les apporter à la branche principale 


### Créer un projet sur github pas à pas (avec linux)
#### Créer un nouveau dépôt
  - créez un nouveau dossier **mkdir /path/to/directory**
  - placez-vous dans le dossier **cd /path/to/directory**
  - exécutez la commande **git init** pour créer le dépôt


#### Cloner un dépôt existant sur votre machine
  - exécutez **git clone "https://github.com/depot.git"**


#### Ajouter et valider des fichiers
  - Vous pouvez proposer un changement en exécutant les commandes :
    - **git add _file-name_** (pour ajouter un fichier spécifique)
    - **git add \*** (pour ajouter tout les fichiers présents dans le dépôt) (A NE PAS FAIRE)
  - Afin de vérifier le statut du dépôt, connaître les modifications à commiter et les fichiers à ajouter
    - exécutez **git status**
  - Il faut ensuite commit vos changements :
    - exécutez **git commit -m "Message de commit"**
    - Le fichier est alors commit au niveau du dépôt local, mais pas encore dans le dépôt distant, pour les envoyer au dépôt distant
    - exécutez **git push origin _branch-name_** (avec branche étant le nom de la branche sur laquelle vous pushez)
 
 
#### Mettre à jour le dépôt local depuis le dépôt distant **(à faire avant d'envoyer n'importe quelle modification sur le dépôt distant)**
  - Exécutez **git pull**
  - Vous aurez alors récupérez et fusionner les changements du dépôt distant avec votre dépôt local


#### Pour créer une nouvelle branche
  - Exécutez **git checkout -b _new-branch_** (à noter que cette commande vous fera directement passer sur la nouvelle branche)
  - Pour retourner sur la branche principale exécutez **git checkout master**
  - Pour que les autres membres du groupe puissent accéder à la branche, vous devez l'envoyer vers le dépôt distant
    - exécutez **git push origin _new-branch_**


#### Fusionner une branche avec la branche active
  - exécutez **git merge _branch_** 
  - si le merge échoue 
    - vous devez régler les conflits manuellement en éditant les fichiers indiqués par github
    - puis marquer les fichiers comme étant fusionnés avec **git add _file-name_**
   
   
#### Annuler des changements locaux
  - exécutez **git checkout -- _file-name_** pour remplacer le contenu actuel avec la version précédente du fichier
  - pour annuler tous les changements locaux
    - exécutez **git fetch origin**
    - puis **git reset --hard origin/master**

#### Sauvegarder des modifications avec git stash
  - Lorsque vous travaillez sur une feature qui n'est pas encore terminée et que vous ne voulez pas encore la commit, vous pouvez la sauvegarder localement avec la commande **git stash** pour la mettre de côté et la finir plus tard
    - exécutez **git stash** 
    - toutes les modifications que vous avez faites depuis le dernier commit disparaitront et seront sauvegardées
  - Pour restaurer ces modifications vous pourrez utiliser la commande **git stash apply**
 
    
#### Aller plus loin avec git stash
  - Vous pouvez avoir plusieurs stash en cours
    - pour les lister exécutez **git stash list**
    - pour appliquer un stash spécifique exécutez **git stash apply stash@{0}**
    - pour visualiser ce qu'il y a dans un stash exécutez **git stash show stash@{0}**
    - Pour supprimer un stash, exécutez **git stash drop stash@{0}**
  - Si un stash devient trop important il est possible de le transformer en branche à part entière 
    - exécutez **git stash branch stash@{0}**
    


Il est intéressant de créer un projet test de cette manière afin de découvrir le fonctionnement de github avant de se tourner vers github desktop qui vous permettra d'exécuter toutes ces commandes via une interface graphique (pour ceux qui ne sont pas à l'aise avec les lignes de commandes)

### Conseils d'utilisation

1.  Synchroniser le code régulièrement (git pull)
1.  Eviter d'utiliser **git add \*** et sélectionnez les fichiers que vous ajoutez
1.  Commiter dès les premières lignes de code
1.  Commiter régulièrement
1.  Commenter votre commit
1.  Lors de projets de groupe il est intéressant de commencer par établir une norme des commits avec les autres membres
1.  **TRAVAILLER SUR VOTRE PROPRE BRANCHE** lorsque vous travailler à plusieurs sur un projet ...
1.  ... et également lorsque vous travaillez seul. Afin de ne pas casser votre projet, créer une nouvelle branche quand vous commencez à travailler sur une nouvelle feature
1.  Ecrire un readme contenant les informations de votre projet, comment l'installer, les libs utilisés...etc de manière à ce qu'ils puissent être réutilisés de la façon la plus simple possible
1.  Merger avec précaution, assurez-vous de ne pas avoir de modification non commitée, assurez-vous qu'il n'y ait pas de conflits localement avant d'appliquer les changements...
1.  ... et en cas de conflit utiliser **git merge -abort** afin de rollback votre merge
1.  **GIT STASH N'EST PAS UNE COMMANDE DE BACK-UP MAIS DE PROCRASTINATION**


## Ressources

[Understand Github conceptually](https://www.sbf5.com/~cduan/technical/git/)

[Quickstart github](https://help.github.com/en/github/getting-started-with-github/quickstart)

[Desktop github](https://desktop.github.com/)

