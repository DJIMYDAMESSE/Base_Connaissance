# Projet base de connaissance

Le projet de base de connaissance entre dans le cadre de la formation Web in Pulse de l’école centrale de Nantes.

Durant cette formation, nous avions comme projet la création d’un système de base de connaissance collaborative pour l’entreprise UmanIT encadré par Mr Vincent Graillot.


## Initialiser le projet

1 - Effectuer la commande  pour récupérer l'intégralité du projet depuis Github vers votre poste.
```
git clone git@github.com:nicolas-le-stunff/BaseConnaissance.git 
``` 

2 -  Sur le terminal et dans le dossier racine du projet, exécuter les commandes pour installer les dépendances du projet
```
composer install
symfony console ckeditor:install
symfony console assets:install public
```
 
3 -  Copier le fichier `.env` vers la racine du projet et le renommer en `.env.local`. Le fichier en question servira de configuration entre le projet et votre base de donnée.

4 -  Modifier la ligne 
```
DATABASE_URL=postgresql://{nom}:{motdepasse@{adresse de la bdd}/{nomdelabasededonnée}?serverVersion={versionDuServeur}&charset=utf8
``` 

5 - Effectuer l'application des migrations sur le terminal ain d'appliquer les changements sur votre base de donnée

``
Symfony console do:mi:mi
``
 
6 - Le projet est prêt à être utilisé sur symfony
## Base de donnée DEMO 


Une base de donnée démo est disponible dans le projet.
Celle-ci est au format SQL .

`` 
BDD-Demo.sql
``
La base de donnée est fournis avec deux comptes.

Compte Administrateur 

Identifiant  : 
`Administrateur`

Mot de passe : `root`

-----

Compte Utilisateur 

Identifiant  : 
`Utilisateur`

Mot de passe : `user`


## Règle de développement
### Les branches

`Master` = Branche source du projet  **(Ne pas push dessus)**.

`Dev` = Branche final de developpement (uniquement dédié au merge)

`Dev-{fonctionnalité}-{Prénom}` = Branche de développement personnel.


#### Branche Master
La branche `Master` du projet initial. Le but sera d'avoir des versions (?tags?) du projet à un instant X et stable.

#### Branche Dev
La branche `Dev` est dédiée aux merges de nos différentes branches personnelles. Le but de la branche est de tester le projet et de le rendre stable avant de le pousser vers le master.


#### Branche personnelle
`Dev-{fonctionnalité}-{Prénom}`
Branche perso du projet. Vous êtes libres de faire ce que vous voulez dessus. C'est cette branche qui sera merge vers `dev`

### Les pushs

Nos pushs doivent être effectués uniquement sur la branche `Dev-{fonctionnalité}-{Prénom}`.
Aucun push (hormis sur le README.MD) ne sera accepté sur les branches : Master / Dev


### Merge

Les merges de `Dev` vers `Master` seront à faire lors de réunions pour figer le projet dans une version stable.
Les merges de `Dev-{Fonctionnalité}-{Prénom}` vers `Dev` auront une pull request avec 2 reviews nécessaires pour être acceptée.

### Conflits 

Dans le cadre du projet, nous aurons probablement des conflicts. Les conflicts sur vos branches perso `Dev-{Fonctionnalité}-{Prénom}` seront à votre charge.
Les conflits sur le master et sur le dev seront à regler en groupe.



## Ne pas oublier 
### Mettre à jour son projet
```
git pull
```

### Changement de branche
```
git checkout {nom-de-la-branche}
```
ou pour changer de branche et créer celle-ci :
```
git checkout -b {nom-de-la-branche}
```

### Comment effectuer un push
A effectuer dans l'ordre et sur la **bonne branche**

```
git add {nom-du-fichier}
git commit -m "  /* Commit le fichier et rajoute un commentaire */ 
git push 
```
### Vérifier l'état de nos fichiers 
```
git status
```




## Source

* [Tester le projet](https://base-de-connaissance.nicolas-le-stunff.fr/) - Lien vers le projet live
* [Symfony](https://symfony.com/doc/current/index.html#gsc.tab=0) - Documentation  de symfony
* [Ck editor](https://symfony.com/doc/current/bundles/FOSCKEditorBundle/index.html)
* [Adobe XD](https://creativecloud.adobe.com/apps/download/xd?promoid=B8NR3RT1&mv=other)
* [Comment déployer une application Symfony](https://symfony.com/doc/current/deployment.html)
* [Mailer](https://symfony.com/doc/current/mailer.html)


