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


## 9 - Modèle Physique des données (MPD)

Voici le schema relationnel/MPD correspondant au MLD precedent :

Diplômes (Diplomes)

Possède (#NumEmployé, #Diplôme, Date d’obtention)

Employés (NumEmployé, Nom, Prénom, Adresse, Code Postal, Ville, Téléphone)

Tables (NumTable, Capacité)

Date (Date)

Service (TypeService, Désignation)

Boissons Diverses (NumBoissons, Désignation, Prix de vente)

Contenir (#NumCommande, #NumBoissons, Quantité)

Commande (NumCommande, #Numemployé, #Date, #TypeService, #NumTable)

Comprend (#NumMenu, #NumCommande, Quantité)

Menus (NumMenu, Libellé, Prix de vente)

Constitué (#NumMenu, #NumPlat)

Constituer (#NumCommande, #NumPlat, Quantité)

Sélectionner (#NumCommande, #NumVin, Quantité)

Carte des vins (NumVin, Nom du vin, Millesime, Prix de vente)

Carte des plats (NumPlat, LibelléPlat, Prix de vente, #NumType)

Type des plats (NumType, Désignation)

Bouteilles (NumBouteille, Date Achat, Prix d’achat, # NumVin, #NumViticulteur)

Viticulteur (NumViticulteur, Nom viticulteur, Prénom viticulteur, Adresse viticulteur, Code postal, Ville, Téléphone)

A partir d'ici il est facile de generer le script SQL correspondant.

```SQL
CREATE TABLE CARTE_DES_VINS
   (
   NUMVIN INTEGER(2) NOT NULL ,
   NOM_DU_VIN CHAR(40)   ,
   MILLESIME INTEGER(2)  ,
   PRIX_DE_VENTE REAL(5,2)
,
    PRIMARY KEY (NUMVIN) CONSTRAINT PK_CARTE_DES_VINS
   );

CREATE TABLE BOUTEILLES
   (
   NUMVITICULTEUR INTEGER(2) NOT NULL ,
   NUMVIN INTEGER(2) NOT NULL ,
   NUMBOUTEILLE INTEGER(2) NOT NULL ,
   DATE_ACHAT DATE(8) ,
   PRIX_D_ACHAT REAL(5,2)
,
    PRIMARY KEY (NUMVITICULTEUR, NUMVIN, NUMBOUTEILLE) CONSTRAINT
PK_BOUTEILLES
   );

$
CREATE TABLE VITICULTEUR
   (
   NUMVITICULTEUR INTEGER(2) NOT NULL ,
   NOM_VITICULTEUR CHAR(20) ,
   PRÉNOM_VITICULTEUR CHAR(20) ,
   ADRESSE_VITICULTEUR CHAR(40) ,
   CODE_POSTAL CHAR(5) ,
   VILLE CHAR(40) ,
   TÉLÉPHONE CHAR(15)
,
    PRIMARY KEY (NUMVITICULTEUR) CONSTRAINT PK_VITICULTEUR
   );
```

## 10 - Les formes normales (FN)

Ensemble de regles qui a pour but d'éviter les anomalies au sein des BDDR(Base de données relationel).
Pour appliquer les concepts des formes normales il est nécessaire de connaitre les trois premieres fromes normales 

### 10.1 - Forme normale 1 (1FN)

Une relation est en premiere forme normale si -> 

- Tous les attributs sont atomiques 
- Les attribus ne contiennent pas de valeurs répétitives 

*Exemple :*

Clients (numCli, Nom, Prénom, Adresse, Telephone)

![Alt text](/img/image-29.png)

![Alt text](/img/image-30.png)

### 10.2 - Forme normale 2 (2FN)

Une relation est en deuxieme forme normale si -> 

- Elle est 1FN 
- Si tous les attributs qui ne sont pas des clés ne dépendent pas d'une partie de la clé primaire 

*Exemple :*

Commande(numCli, CodeArticle, Date, QteCommande, Designation)

![Alt text](/img/image-31.png)

![Alt text](/img/image-32.png)

### 10.3 - Forme normale 3 (3FN)

Une relation est en troisieme forme normale si ->

- Elle est en deuxieme forme normale
- Si toutes les dépendances fonctionnelles(DF) sont directes

"Les attributs non clé primaire ne dépendent pas d'un autre attribut non clé primaire"

*Exemple :*

Commande(numCommande, #CodeClient, #RefArticle)

![Alt text](/img/image-33.png)

![Alt text](/img/image-34.png)

## 11 - Les diagrammes des flux 

Les diagrammes des flux permettent de modéliser les fluxs d'informations entre les acteurs du systeme d''information et les a cteurs du systeme opérant.

**Définition ->**

- `Domaine d'étude :` Le périmetre d'une activite au sein d'une entreprise, d'une activite spécifique
- `L'acteur :` Une personne, un service, une entreprise, un systeme informatique qui intervient dans le domaine d'étude au moyen d'un flux d'information
- `Les fluxs :` Les informations qui circulent entre les acteurs, represente par une fleche et porte un nom et peut etre numérote (par soucis de chronologie)

*Représentation graphique :*

Quelques regles a respecter :

- Un flux ne peut pas etre bidirectionnel
- Un flux ne doit pas etre reflexif
- On ne présente pas les fluxs entre les acteurs externes

![Alt text](/img/image-35.png)

## 12 - UML 

`UML :` Unified Modeling Language(Langage de Modélisation Unifié) est un langage de modélisation de données. UML a été normalisé en 1997 par l'OMG (Object Management Group). Son but est de mettre en forme les concepts orientés objets au travers de diagramme. 

UML porpose 13 diagrammes dependants de facon hiérarchique et se complétant.

1. Les diagrammes statiques : ils permettent de modéliser la structure d'un systeme
    - Diagramme de classe
    - Diagramme d'objets
    - Diagramme de composants
    - Diagramme de déploiement

2. Les diagrammes comportemmentaux : 
    - Diagramme de cas d'usage
    - Diagramme d'activité
    - Diagramme d'état-transition

3. Les diagrammes dyamiques : 
    - Diagramme de séquence
    - Diagramme de communication
    - Diagramme de global d'interaction
    - Diagramme de temps

### 12.1 - Analogie Merise / UML

1. Cas du MCD et du diagramme de classe :  



![Alt text](/img/image-36.png)

# Sujet TP 1 
![Alt text](/img/image-14.png)


# Sujet Cas Pratique 
A partir du MCD suivant il faut construire le MLD. 

![alt text](/img/image-27.png)

Le MLD est le suivant Correction : 

![alt text](/img/image-28.png)


Résultat MLD Perso : 

![alt text](/img/TD1.png)

# Exercice 1 

`Les tests des scripts SQL sont effectués avec le logiciel XAMPP en local.`

**MCD :** 

![alt text](/img/MCDEXO1.png)

**MLD :**

![alt text](/img/MLDEXO1.png)

**MPD :**

Info_Vente (Id_Vente_Info_Vente, Date_Info_Vente, Poids_Info_Vente, Total_Achat_Info_Vente)  

Agriculteur (Id_Agriculteur_Agriculteur, Nom_Agriculteur, Prenom_Agriculteur)  

Legume (Id_Legume_Legume, Nom_Legume_Legume)  

Animal_ (Id_Animal_Animal_, Type_Animal_Animal_)  

Fruits (Id_Fruit_Fruits, Nom_Fruit_Fruits)  

Vendu (Id_Vente_Info_Vente, Id_Agriculteur_Agriculteur)  

En_vente (Id_Agriculteur_Agriculteur, Id_Legume_Legume, Id_Animal_Animal_, Id_Fruit_Fruits) 

**Script MySQL**
``` sql
DROP TABLE IF EXISTS Info_Vente ;
CREATE TABLE Info_Vente (Id_Vente_Info_Vente INT(10) AUTO_INCREMENT NOT NULL,
Date_Info_Vente DATE,
Poids_Info_Vente FLOAT(20),
Total_Achat_Info_Vente FLOAT(10),
PRIMARY KEY (Id_Vente_Info_Vente)) ENGINE=InnoDB;ù$

DROP TABLE IF EXISTS Agriculteur ;
CREATE TABLE Agriculteur (Id_Agriculteur_Agriculteur INT(10) AUTO_INCREMENT NOT NULL,
Nom_Agriculteur VARCHAR(250),
Prenom_Agriculteur VARCHAR(250),
PRIMARY KEY (Id_Agriculteur_Agriculteur)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Legume ;
CREATE TABLE Legume (Id_Legume_Legume INT(10) AUTO_INCREMENT NOT NULL,
Nom_Legume_Legume VARCHAR(250),
PRIMARY KEY (Id_Legume_Legume)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Animal_ ;
CREATE TABLE Animal_ (Id_Animal_Animal  INT(10) AUTO_INCREMENT NOT NULL,
Type_Animal_Animal  VARCHAR(250),
PRIMARY KEY (Id_Animal_Animal_)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Fruits ;
CREATE TABLE Fruits (Id_Fruit_Fruits INT(10) AUTO_INCREMENT NOT NULL,
Nom_Fruit_Fruits VARCHAR(250),
PRIMARY KEY (Id_Fruit_Fruits)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Vendu ;
CREATE TABLE Vendu (Id_Vente_Info_Vente **NOT FOUND**(10) AUTO_INCREMENT NOT NULL,
Id_Agriculteur_Agriculteur **NOT FOUND**(10) NOT NULL,
PRIMARY KEY (Id_Vente_Info_Vente,
 Id_Agriculteur_Agriculteur)) ENGINE=InnoDB;

DROP TABLE IF EXISTS En_vente ;
CREATE TABLE En_vente (Id_Agriculteur_Agriculteur **NOT FOUND**(10) AUTO_INCREMENT NOT NULL,
Id_Legume_Legume **NOT FOUND**(10) NOT NULL,
Id_Animal_Animal  **NOT FOUND**(10) NOT NULL,
Id_Fruit_Fruits **NOT FOUND**(10) NOT NULL,
PRIMARY KEY (Id_Agriculteur_Agriculteur,
 Id_Legume_Legume,
 Id_Animal_Animal_,
 Id_Fruit_Fruits)) ENGINE=InnoDB;

ALTER TABLE Vendu ADD CONSTRAINT FK_Vendu_Id_Vente_Info_Vente FOREIGN KEY (Id_Vente_Info_Vente) REFERENCES Info_Vente (Id_Vente_Info_Vente);

ALTER TABLE Vendu ADD CONSTRAINT FK_Vendu_Id_Agriculteur_Agriculteur FOREIGN KEY (Id_Agriculteur_Agriculteur) REFERENCES Agriculteur (Id_Agriculteur_Agriculteur);
ALTER TABLE En_vente ADD CONSTRAINT FK_En_vente_Id_Agriculteur_Agriculteur FOREIGN KEY (Id_Agriculteur_Agriculteur) REFERENCES Agriculteur (Id_Agriculteur_Agriculteur);
ALTER TABLE En_vente ADD CONSTRAINT FK_En_vente_Id_Legume_Legume FOREIGN KEY (Id_Legume_Legume) REFERENCES Legume (Id_Legume_Legume);
ALTER TABLE En_vente ADD CONSTRAINT FK_En_vente_Id_Animal_Animal_ FOREIGN KEY (Id_Animal_Animal_) REFERENCES Animal_ (Id_Animal_Animal_);
ALTER TABLE En_vente ADD CONSTRAINT FK_En_vente_Id_Fruit_Fruits FOREIGN KEY (Id_Fruit_Fruits) REFERENCES Fruits (Id_Fruit_Fruits);
```

# Exercice 2 

`Les tests des scripts SQL sont effectués avec le logiciel XAMPP en local.`

**MPD :**

*Shèma relationnel :*

Ensembles(CodeEnsemble, Désignation) 

Sous-Ensembles(CodeSousEnsemble, Désignation, Longueur, Largeur, Hauteur, Prix_Unitaire) 

Composants(CodeComposant, Désignation, Prix_Unitaire) 

LienEnsSE(#CodeEnsemble, #CodeSousEnsemble, Qté) 

LienEnsComposant(#CodeEnsemble, #CodeComposant, Qté) 

LienSEComposant(#CodeSousEnsemble, #CodeComposant, Qté) 

*Script SQL :*

```SQL
DROP TABLE IF EXISTS Ensembles ;
CREATE TABLE Ensembles (CodeEnsemble INT(10) AUTO_INCREMENT NOT NULL,
Désignation VARCHAR(250),
PRIMARY KEY (CodeEnsemble)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Sous_Ensembles ;
CREATE TABLE Sous_Ensembles (CodeSousEnsemble INT(10) AUTO_INCREMENT NOT NULL,
Désignation VARCHAR(250),
Longueur FLOAT(20),
Largeur FLOAT(20),
Hauteur FLOAT(20),
Prix_Unitaire FLOAT(10),
PRIMARY KEY (CodeSousEnsemble)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Composants ;
CREATE TABLE Composants (CodeComposant INT(10) AUTO_INCREMENT NOT NULL,
Désignation VARCHAR(250),
Prix_Unitaire FLOAT(10),
PRIMARY KEY (CodeComposant)) ENGINE=InnoDB;

DROP TABLE IF EXISTS LienEnsSE ;
CREATE TABLE LienEnsSE (CodeEnsemble INT(10) NOT NULL,
CodeSousEnsemble INT(10) NOT NULL,
Qté INT(10),
PRIMARY KEY (CodeEnsemble,
 CodeSousEnsemble)) ENGINE=InnoDB;

DROP TABLE IF EXISTS LienEnsComposant ;
CREATE TABLE LienEnsComposant (CodeEnsemble INT(10) NOT NULL,
CodeComposant INT(10) NOT NULL,
Qté INT(10),
PRIMARY KEY (CodeEnsemble,
 CodeComposant)) ENGINE=InnoDB;

DROP TABLE IF EXISTS LienSEComposant ;
CREATE TABLE LienSEComposant (CodeSousEnsemble INT(10) NOT NULL,
CodeComposant INT(10) NOT NULL,
Qté INT(10),
PRIMARY KEY (CodeSousEnsemble,
 CodeComposant)) ENGINE=InnoDB;
```
*Resultat script SQL :* 

![alt text](/img/ResultSQLEXO2.png)

**MLD :**

![alt text](/img/MLDEXO2.png)

**MCD :**

![alt text](/img/MCDEXO2.png)

# Exercice 3 

`Les tests des scripts SQL sont effectués avec le logiciel XAMPP en local.`

**Dictionnaire :**

![alt text](/img/DICEXO3.png)

**MCD :**

![alt text](/img/MCDEXO3.png)

**MLD :**

![alt text](/img/MLDEXO3.png)


**MPD :** 

*Shèma Relationel :*

Client (Id_Client_Client, Nom_Intervention, Prenom_Intervention, Telephone_Intervention, Adresse_Intervention)  
Intervention (Id_Intervention_Intervention, Type_Intervention_Intervention, Date_Intervention, Type_Materiel_Intervention, Type_Manipulations_Intervention)  
tarifs (Temps_tarifs, Intervention_complexe_Prix, Intervention_simple_Prix)  
Composant (Id_Composant__Composant, Etat_Composant, Prix_Composant)  
Entreprise (Id_entrerprise_Entreprise, Nom_Entreprise)  
Intervien (Id_entrerprise_Entreprise, Id_Intervention_Intervention, Id_Client_Client)  
En_vente (Id_entrerprise_Entreprise, Id_Composant__Composant, Quantite_En_vente)  
Couts (Temps_tarifs, Id_Intervention_Intervention)

*Script SQL :*

```SQL
DROP TABLE IF EXISTS Client ;
CREATE TABLE Client (Id_Client_Client INT(10) AUTO_INCREMENT NOT NULL,
Nom_Intervention VARCHAR(250),
Prenom_Intervention VARCHAR(250),
Telephone_Intervention VARCHAR(250),
Adresse_Intervention VARCHAR(250),
PRIMARY KEY (Id_Client_Client)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Intervention ;
CREATE TABLE Intervention (Id_Intervention_Intervention INT(10) AUTO_INCREMENT NOT NULL,
Type_Intervention_Intervention VARCHAR(250),
Date_Intervention DATE,
Type_Materiel_Intervention VARCHAR(250),
Type_Manipulations_Intervention VARCHAR(250),
PRIMARY KEY (Id_Intervention_Intervention)) ENGINE=InnoDB;

DROP TABLE IF EXISTS tarifs ;
CREATE TABLE tarifs (Temps_tarifs INT(10) AUTO_INCREMENT NOT NULL,
Intervention_complexe_Prix FLOAT(10),
Intervention_simple_Prix FLOAT(10),
PRIMARY KEY (Temps_tarifs)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Composant ;
CREATE TABLE Composant (Id_Composant__Composant INT(10) AUTO_INCREMENT NOT NULL,
Etat_Composant VARCHAR(250),
Prix_Composant FLOAT(10),
PRIMARY KEY (Id_Composant__Composant)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Entreprise ;
CREATE TABLE Entreprise (Id_entrerprise_Entreprise INT(10) AUTO_INCREMENT NOT NULL,
Nom_Entreprise VARCHAR(250),
PRIMARY KEY (Id_entrerprise_Entreprise)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Intervien ;
CREATE TABLE Intervien (Id_entrerprise_Entreprise INT(10) NOT NULL,

Id_Intervention_Intervention INT(10) NOT NULL,
Id_Client_Client INT(10) NOT NULL,
PRIMARY KEY (Id_entrerprise_Entreprise,
 Id_Intervention_Intervention,
 Id_Client_Client)) ENGINE=InnoDB;

DROP TABLE IF EXISTS En_vente ;
CREATE TABLE En_vente (Id_entrerprise_Entreprise INT(10) NOT NULL,
Id_Composant__Composant INT(10) NOT NULL,
Quantite_En_vente INT(10),
PRIMARY KEY (Id_entrerprise_Entreprise,
 Id_Composant__Composant)) ENGINE=InnoDB;

DROP TABLE IF EXISTS Couts ;
CREATE TABLE Couts (Temps_tarifs INT(10) NOT NULL,
Id_Intervention_Intervention INT(10) NOT NULL,
PRIMARY KEY (Temps_tarifs,
 Id_Intervention_Intervention)) ENGINE=InnoDB;
```
*Resultat script SQL :* 

![alt text](/img/ResultSQLEXO3.png)


# Exercice 4

`Les tests des scripts SQL sont effectués avec le logiciel XAMPP en local.`

**MCD :**

![alt text](/img/)

**MLD :**

![alt text](/img/)


**MPD :** 

*Shèma Relationel :*


*Script SQL :*

```SQL

```
*Resultat script SQL :* 

![alt text](/img/)

