# Lundi 
## Commande basique sur Git/Github 

Cette commande initialise le dépot Git, Git va traquer toutes les odifications effectuées au sein de ce dossier 
``` bash 
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
Pour envoyer le travail sur un projet github 
![alt text](/img/github.png)

Commande pour lié le répertoire au porjet sur github 
``` bash 
git remote add origin git@github.com:FluXy899/Isitech-2223-B1-MDD-Virgile.git
```
Pour qu'il passe sur la branche main et oublier le master 
``` bash 
git branch -M main
``` 
Pour voir qu'elle est notre origine 
``` bash 
git remote -v
``` 
Puis faire  ce qui permet de synchroniser la premiere fois 
``` bash 
git push -u origin main
``` 
Maintenant votre projet remonte vers github 
Pour syncrhoniser tout le long du porjet il faudra juste faire 
``` bash 
git push 
``` 
Pour importer un depot git se trouvant sur github il faut créer un dossier et mettre la commande 
``` bash 
git clone lienssh ou https 
``` 
Pour syncrhoniser le dépot importer il suffit de faire 
``` bash 
git pull
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

## 4-  Des données aux dépdendances fonctionnelles 

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


###   4.1- Les dépendances fonctionnelles 
\
Une dépendance fonctionelle est une relation entre deux attributs d'une table. Elle permet de définir une relation de dépendance entre 2 attributs d'une table 

Le role d'une dependance fonctionnelle est de permettre définir une relation de dependance entre 2 attributs d'une table : une donnee A depend fonctionnellement d'une donnée B lorsque la valeur de B détermine la valeur de A 

Pour formaliser une dependance fonctionnelle on utilise la notion suivante : 
Numéro d'adhérent `(Nom, Prénom, CP, Ville, Téléphone, Date d'adhésion, mail)`

La partie de gauche (numéro adhérent) est la `source` de la dépendance fonctionnelle. \

La partie de droite designe le `but` de la dépendance.
![alt text](/img/image-5.png)
![alt text](/img/image-6.png)
![alt text](/img/image-7.png)


###   4.2 - Les dépendances fonctionnelles composees 

Si une dependance fonctionnelle qui fait intervenir plus de deux attributs on parle de dépendances fonctionnelles composee. 

*Exemple :* pour connaitre le temps d'un coureur sur une etape donnee il nous fait son numero ou son nom ainsi que le nom ou le numero de l'etape. 

Formalisation : 
`(numéro courreur, numéro etape)` -> `(Temps)`

###   4.3 - Les dépendances fonctionnelles élémentaires 

**Définition->** \
Une dépendance fonctionnelle A->B est élémentaire s'il n'existe pas une donnee C, sous-ensemble de A, Décrivant une dépendance fonctionnelle type C-> B 

*Exemple ->*
- RefProduit -> LibeleProduit
- NumCommande RefProduit -> QuantiteCommandee -> élémentaire
- <strike> NumCommande Refproduit -> DesignationProduit</strike> -> non élémentaire

###   4.4  - Les dépendances fonctionnelles élémentaires directe 
"On dit que la dépendance fonctionnelle A -> B est directe s'il n'existe aucun attribut C tel que l'on puisse avoir A -> C et C -> B. 
En d'autres termes, cela signifie que la dépendance fonctionnelle entre A et B ne peut pas etre obtenue par transivité"

*Exemple ->*
- RefPromo -> NumApprenant
- NumApprenant -> NomApprenant
- RefPromo-> NomApprenant : RefPromo -> NumApprenant -> NomApprenant

## 5 - MCD 

Ici on va introduire les notions d'entité, de relation et de propriété.

Les propriétés sont les informations de bases d'un SI

**Les entités sont les objets du SI :**

Quelques définitions : 
  - *entité forte :* une entité qui ne dépend pas d'une autre entité pour exister 
  - *Entité faible :* une entité qui dépend d'une autre entité pour exister
  
![alt text](/img/image-8.png)


## 6 - Les relations :


![alt text](/img/image-9.png)

### 6.1 - Les relations "porteuses"

Une relation est dite porteuse si elle possede des propiétés. 

![alt text](/img/image-15.png)
\
![alt text](/img/image-16.png)

### 6.2 - Les relations reflexives 

Une relation est reflexives si elle relie  une entité a elle meme \
![alt text](/img/image-17.png)


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


## 7 - Installation d'analysis 
*Prérequis java :*
- version 7 **Minimum**

# Mardi 

### Les contraintes d'integritefonctionnelles (CIF)

**Définition->**  
Une CIF est définie par le fait qu'une des entités de l'association est complétement déterminée par la connaissance d'une ou de plusieur entités participant à l'association.

*Exemple ->*

![Alt text](/img/image-18.png)

Une salle peut contenir 0 ou plusieurs Ordinateurs. Un ordinateur existe dans une et une seule salle.\
Dans ce type de relation une CIF existe si on a une cardinalite 1,1

# Mercredi 

## 8 - Modèle Logique des données (MLD)

Le MLD  est la suite du processus Merise, on se rapproche un peu plus de de la BDD. 
#### *Cas Simple  ->*
*Partons du MCD suivant :* 

![alt text](/img/image-19.png)

*Nous arrivons au MLD suivant :*

![alt text](/img/image-20.png)
*Nous arrivons au MLD suivant :*
L'entité qui possède la cardianlité `1.1` ou `0.1`  absorbe l'identifiant de l'entité plus forte (0.n ou 1.n ). Cet identitfiant devient alors une **clé etrangère**

#### *Cas (0.n), (0.n) ou (1.n), (1.n)  ->*

*Partons du MCD suivant :* 

![alt text](/img/image-21.png)

Dns le cas ou la `cardinalité maximun` est n des 2 cotés, on crée une entité intermédiaire qui va contenir les deux clés étrangères des deux entittés. 

![alt text](/img/image-22.png)

*Continuons avec le MCD suivant :*

![alt text](/img/image-23.png)

*En suivant la meme logique on obtient le MLD suivant :*

![alt text](/img/image-24.png)

#### *Cas d'une relation reflexive ->*

*Partons du MCD suivant :* 

![alt text](/img/image-25.png)

*Nous arrivons au MLD suivant :*

![alt text](/img/image-26.png)

### 8.1 - Regles de passage du MCD au MLD 

Règles simples de passage du MCD au MLD
L’entité qui possède la cardinalité maximale égale à 1 recevra l’identifiant ou les identifiants des entités ayant les cardinalités maximales les plus fortes.

Les relations ayant toutes leurs entités reliées avec des cardinalités maximales supérieures à 1 se transformeront en entité en absorbant les identifiants des entités jointes.

Toute relation porteuse de propriétés se transformera en entité et absorbera comme clé étrangère les identifiants des entités qui lui sont liées.

Toute relation réflexive se transformera en entité et absorbera comme clé étrangère l’identifiant de l’entité qui lui est liée.


# Sujet TP 1 
![Alt text](/img/image-14.png)

# Sujet Cas Pratique 
A partir du MCD suivant il faut construire le MLD. 

![alt text](/img/image-27.png)

Résultat MLD : 

![alt text](/img/CP1.png)
