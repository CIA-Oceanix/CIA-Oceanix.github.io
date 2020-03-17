## Github

### Créer un projet sur github pas à pas (avec linux)
- Créer un nouveau dépôt
  - créez un nouveau dossier **mkdir /path/to/directory**
  - placer vous dans le dossier **cd /path/to/directory**
  - exécutez la command **git init** pour créer le dépôt


- Cloner un dépôt existant sur votre machine
  - exécutez **git clone "https://github.com/depot.git"**


- Ajouter et valider des fichiers
  - Vous pouvez proposer un changement (l'ajouter à l'Index) en exécutant les commandes :
   - **git add file** (pour ajouter un fichier spécifique)
   - **git add \*** (pour ajouter tout les fichiers présent dans le dépôt) (A NE PAS FAIRE)
  - Il faut ensuite commit vos changements :
   - exécutez **git commit -m "Message de commit"**
  - Le fichier est alors ajouté au HEAD du dépôt local, mais pas encore dans le dépôt distant, pour les envoyer au dépôt distant
   - exécutez **git push origin branche** (avec branche étant le nom de la branche sur laquelle vous pushez)
 
 
- Mettre à jour le dépôt local depuis le dépôt distant **(à faire avant d'envoyer n'importe quelle modification sur le dépôt distant)**
  - exécutez **git pull**
  - Vous aurez alors récupérez et fusionner les changements du dépôt distant avec votre dépôt local


- Pour créer une nouvelle branche
  - exéctuez **git checkout -b nouvelle_branche** (à noter que cette commande vous fera directement passer sur la nouvelle branche)
  - pour retourner sur la branche principale exécutez **git checkout master**
  - pour que les autres membres du groupe puissent accéder à la branche, vous devez l'envoyer vers le dépôt distant
   - exécutez **git push origin nouvelle_branche**


- Fusionner une branche avec la branche active
  - exécutez **git merge branche** 
  - si le merge échoue 
   - vous devez régler les conflits manuellement en éditant les fichiers indiqués par github
   - puis marquer les fichiers comme étant fusionnés avec **git add file**
   
   
- Annuler des changements locaux
  - exécutez **git checkout -- file** pour remplacer le contenu de HEAD avec la version précédente du fichier
  - pour annulez tout les changements locaux
   - exécutez **git fetch origin**
   - puis **git reset --hard origin/master**




Il est intéressant de créer un projet test de cette manière afin de découvrir le fonctionnement de github avant de se tourner vers github desktop

### Conseils d'utilisation

1.  Synchroniser le code régulièrement (git pull) 
1.  Commiter dès les 1eres lignes de code
1.  Commiter régulièrement
1.  Commenter votre commit
1.  Eviter d'utiliser **git add \*** et sélectionnez les fichiers que vous ajoutez
1.  Lors de projet de groupe il est intéressant de commencer par établir une norme des commits avec les autres membres
1.  **TRAVAILLER SUR VOTRE PROPRE BRANCHE** lorsque vous travailler à plusieurs sur un projet ...
1.  ... et également lorsque vous travailler seul. Afin de ne pas casser votre projet, créer une nouvelle branche quand vous commencez à travailler sur une nouvelle feature
1.  Ecrire un readme contenant les informations de votre projet, comment l'installer, les libs utilisés...etc de manière à ce qu'ils puissent être réutiliser de la façon la plus simple possible
1.  Merger avec précaution, assurez vous de ne pas avoir de modification non commitée, assurez vous qu'il n'y ait pas de conflits localement avant d'appliquer les changements...
1.  ... et en cas de conflit utiliser **git merge -abort** afin de rollback votre merge


## Ressources

[Understand Github conceptually](https://www.sbf5.com/~cduan/technical/git/)

[Quickstart github](https://help.github.com/en/github/getting-started-with-github/quickstart)

[Desktop github](https://desktop.github.com/)

