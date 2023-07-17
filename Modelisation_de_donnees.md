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
**Fonctionnement du systeme systemique** 

![alt text](/img/image.png)\
Le systeme de pilotage  : 
- Il compose l'ensemble des acteurs qui vont **piloter** le systeme d'information

 Le systeme d'information : 
- Il compose l'ensemble des acteurs qui vont **utiliser** le systeme d'information

Le systeme opérant : 
- Il compose l'ensemble des acteurs qui vont **produire** les données du systeme d'information


### 2 - La séparation des données et des traitements 

Elle permet de séparer les données du systeme d'info et les traitements effectués sur ces données

Cette demarche se fait en 3 étapes : 
- L'analyse des flux : on analyse les fluxs d'informations entre acteyrs du systeme d'information et systeme opérant 
- L'etude des documents interne -> Factures, Bon de livraison 
- L'etude des documents en externes -> Fournisseurs, Clients

Différents types d'informations : 
- Les infos de base ou élémentaires : Données de base du systeme d'information -> Adresse, Prenom, numéro de téléphone, etc 
- Les informations calculée : Données calculées à partir des données de base -> Prix de base, etc
- Les traitements ou les fonctions : Traitements effectués sur les données de base pour obtenir les données calculées 

 *Resumé des 3 étapes :*\
Vous devrez identifiées les données et les traitements effectués sur ces données 

### 3 - L'approche nivelée 
\
Pour effectuer la conceptiion d'un SI, on va utiliser un approche nivelée, elle se compose de 4 niveaux : 

- Niveau conceptuel
- Niveau organisationnel
- Niveau logique
- Niveau physique 

  ### 3.1 - Niveau conceptuel
  Le niveau conceptuel permet de modéliser les données de l'entreprise. On va utiliser le modèle conceptuel de données -> MCD pour modéliser les données de l'entreprise, et le MCT pour modéliser les traitements effectués sur ces données.

  ### 3.2 - Niveau organisationnel
  Le niveau organisationnel va permettre d'intégrer a l'analyse précedente toutes les notions de temporalité, de chronologie des opérations, de contraintes géographique. On va utiliser le modele organisationnel des traitements -> MOT et le modele organisationnel des données -> MOD pour modéliser les traitements de l'entreprise. 

  *En résumé on se pose les questions suivantes à partir des données receuillies auu niveau conceptuel :*
  - **Quand** les traitements sont ils effectués ?
  - **Ou** les traitements sont ils effectués ?
  - Par **qui** les traitements sont ils effectués ?

   ### 3.3 - Niveau logique

   Le niveau logique va permettre de modéliser les données de l'entreprise en utilisant le modèle logique de données -> MLD et les traitements de l'entreprise en utilisant le modèle logique des traitements -> MLT \
   
   Le MLD est indépendant des langages de programmation et des SGBD -> Système de gestion de base de données \
   \
   On  répond à la question: **Avec Quoi** les traitements sont-ils effectués 

    ### 3.4 - Niveau physique 

    Il s'agit de l'organisation `réelle` des données. On va utiliser le modèle physique de données -> MPD et le modèle physique de traitements -> MPT. 

    Ici, on apporte les solutions téchniques de stockage des données et de traitements des données. 

    On répond a la question : **Comment** les traitements sont-ils effectue ? 

### Résumé: Les niveaux de Merise 
![alt text](/img/image-1.png)

## Des données aux dépdendances fonctionnelles 

Pour etre integrées dans un systeme d'information, les données doivent etre triées et organisées. On va souvent tenter de classer par type de données : 
- Chaines de caractères, format texte
- Type alphanumérique, format texte
- Type numérique (integer, float...)
- Type date (date,datetime, timestamp)0
- Logique ou booleen (true, false)

Création d'un dictionnaire de données
![alt text](/img/image-2.png)

### Fiche adhérent
![alt text](/TD%201/Tableau%20adh%C3%A9rent%20.png)
### Facture
![alt text](/TD%201/facture.png)


### Les dépendances fonctionnelles 
\
Une dépendance fonctionelle est une relation entre deux attributs d'une table. Elle permet de définir une relation de dépendance entre 2 attributs d'une table 
# Sujet TP lundi
![alt text](/img/image-14.png)
![alt text](image-5.png)
![alt text](image-6.png)
![alt text](image-7.png)

## MCD 

Ici on va introduire les notions d'entité, de relation et de propriété.

Les propriétés sont les informations de bases d'un SI

**Les entités sont les objets du SI :**

![alt text](/img/image-8.png)

**Les relations :**


![alt text](/img/image-9.png)

**Les Cardinalités :** Elles permettent de définir le nombre d'occurences d'une entité par rapport à une autre entité dans le cadre d'une relation. 

![alt text](/img/image-10.png)

Petit exemple : 

![alt text](/img/image-11.png)

![alt text](/img/image-12.png)

![alt text](/img/image-13.png)

### *Quelques relges de conception :*
- Toute entité doit avoir un ID 
- Toutes les propiétés dependent fonctionnellement de l'ID 
- Le nom d'une propriété ne doit apparaitre q'une fois dans le MCD : si vous avez une entité `Eleve` et une entité `Professeur`, vous ne pouvez pas avoir une propriété nom dans les deux entité. Il faut donc renommer la propiété nom de l'entité  en nomprofesseur par exemple.


### Installation d'analysis 
*Prérequis java :*
- version 7 **Minimum**