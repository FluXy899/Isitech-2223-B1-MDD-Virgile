## Commande basique 

Cette commande initialise le dépot Git, Git va traquer toutes les odifications effectuées au sein de ce dossier 
``` sh 
git init 
```
Pour consulter l'etat du dépot Git il suffit de lancer la commande : 
- Si en rouge fichier non suivi 
- Si en vert fichier suivi 
- Si pas de fichier tout les fichiers sont sauvegarder 
``` bash  
git status
```
Permet d'ajouter des fichiers non suivis : 
``` bash  
git add .
```
Pour sauvegarder le travail : 
``` bash  
git commit -m "nom du commit"
```

## Merise 
Merise est une méthode de modélisation de données. Elle permet de representer les données d'un systeme d'information.\
Merise est un acronyme de : Méthode d'etude et de Réalisation Informatique pour les systemes d'entreprise.

Presentation gélérale : 
Trois points clés : 
- Une approche dite systemique :  les processus de l'entreprise -> systeme d'information 
- Une séparaton des données et des traitements 
- Une approche nivelée 

### 1 - L'approche systemique 

Le systeme de pilotage  : 
- Il compose l'ensemble des acteurs qui vont **piloter** le systeme d'information

 Le systeme d'information : 
- Il compose l'ensemble des acteurs qui vont **utiliser** le systeme d'information

Le systeme opérant : 
- Il compose l'ensemble des acteurs qui vont **produire** les données du systeme d*