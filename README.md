# TP1DevopsHadir (Hadir Manai 2MPSWM)

## Introduction

Dans le cadre de ces Travaux Pratiques, j'ai eu l'occasion d'explorer les bases de Git. Cela m'a permis de découvrir comment gérer des projets, de collaborer efficacement avec d'autres développeurs, et d'acquérir des compétences avancées en Git. Ces Travaux Pratiques ont été une expérience enrichissante et m'ont aidé à approfondir mes connaissances.

# Partie 1: Préparation de l'environnement Git

## 1.1 Création de clé SSH

Pour commencer, j'ai généré ma propre clé SSH afin de sécuriser mes connexions aux dépôts distants. Voici comment j'ai fait :

- J'ai utilisé la commande suivante pour générer ma clé SSH personnalisée :
  ---> ssh-keygen -t rsa -b 4096 -C monadresse@email.com
  Cette commande a créé une paire de clés SSH, une clé privée que je garde en sécurité sur mon ordinateur, et une clé publique que je vais utiliser pour m'authentifier sur les services de dépôt distant.

## 1.2 Copie de la clé publique

Une fois que ma clé SSH a été générée, j'ai copié la clé publique pour pouvoir l'ajouter à mon compte sur le GitHub. Voici comment j'ai fait :

- J'ai utilisé la commande suivante pour afficher le contenu de ma clé publique :
  ---> cat ~/.ssh/id_rsa.pub

# Partie 2: Création d'un nouveau projet

## 2.1 Création d'un référentiel

Pour commencer, je me suis connecté à mon compte GitHub et j'ai suivi ces étapes pour créer un nouveau projet :

- J'ai cliqué sur le bouton "Nouveau" pour créer un nouveau projet.
- J'ai donné un nom significatif au projet et j'ai choisi les options appropriées (public, avec README).
- Ensuite, j'ai cliqué sur "Create Repository".

- J'ai noté l'URL de mon projet, qui ressemble à ceci : `git@github.com:hadirmanai/TP1DevopsHadir.git`.

## 2.2 Clonage du projet

Pour cloner le projet que je viens de créer, j'ai utilisé l'URL SSH que j'ai notée à la partie 2.1, j'ai exécuté la commande suivante :
---> git clone `git@github.com:hadirmanai/TP1DevopsHadir.git`

# Partie 3: Concepts de base de Git

Dans cette partie, je vais vous montrer comment travailler avec les concepts de base de Git.

## 3.1. Travailler avec les fichiers

La première étape consiste à créer un fichier appelé `index.html` dans votre répertoire de projet et à y ajouter du contenu. Voici comment j'ai procédé :

- J'ai créé le fichier `index.html` en utilisant les commandes suivantes :
  ---> touch index.html (Pour créé le fichier index.html)
  ---> echo "Contenu de votre fichier" > index.html (Pour créé dans le fichier)

- Ensuite, j'ai ajouté le fichier à l'index en utilisant la commande suivante :
  ---> git add index.html (ou on peut ajouter avec git add ).

- J'ai validé mon premier commit en utilisant la commande suivante :
  ---> git commit -m "Premier commit : ajout de index.html"

# Partie 4: Collaborer sur Git

Dans cette section, je vais partager mon expérience sur la manière dont j'ai collaboré avec Git pour travailler sur un projet en équipe.

## 4.1. Créez une nouvelle branche

Lorsque j'ai commencé à travailler sur un projet, la première étape était de créer une nouvelle branche pour la fonctionnalité que je devais développer. Voici comment je l'ai fait :

- J'ai décidé d'appeler ma nouvelle branche `ma-fonctionnalite`.

- Pour la créer, j'ai utilisé les commandes suivantes :
  --->git branch ma-fonctionnalite (pour créé une nouvelle branche)
  ---> git checkout ma-fonctionnalite (pour basculer a cette branche)

## 4.2. Effectuez des modifications

Une fois que j'étais sur ma nouvelle branche, j'ai pu commencer à apporter des modifications à mon dépôt local. Voici comment j'ai géré ce processus :

- J'ai effectué les modifications nécessaires à mon projet.
  ---> git add .
- Ensuite, j'ai réalisé un commit en fournissant un message descriptif pour expliquer les modifications que j'avais apportées :
  ---> git commit -m "Modification de ma-fonctionnalite"
- Enfin, pour partager mes modifications, j'ai poussé ma branche vers le GitHub en utilisant la commande suivante :
  --->git push origin ma-fonctionnalite
  Cela a permis à mes collègues de voir mes changements et de collaborer plus efficacement.

## 4.3. Gestion des conflits

Pendant notre travail , il est inévitable que des conflits surviennent lorsque plusieurs personnes modifient le même fichier. Voici comment j'ai abordé la gestion de conflits :

- J'ai commencé par basculer sur la branche sur laquelle je voulais fusionner ma fonctionnalité, souvent la branche master, avec la commande : ---> git checkout master

# Partie 5: Utilisation de GitFlow

Dans cette section, je vais partager le travaille avec GitFlow.

## 5.1. Initialisation de GitFlow

Lorsque j'ai décidé d'explorer GitFlow, la première étape a été de l'initialiser sur mon dépôt. Voici comment je m'y suis pris :

- J'ai lancé la commande suivante pour initialiser GitFlow :
  ---> git flow init

## 5.2. Création d'une nouvelle fonctionnalité

GitFlow simplifie la création de nouvelles fonctionnalités. Voici comment j'ai procédé :

- J'ai lancé la commande suivante pour commencer une nouvelle fonctionnalité :
  ---> git flow feature start ma-fonctionnalite
  Cela a créé une branche de fonctionnalité dédiée à ma tâche.

## 5.3 Création d'une nouvelle version

Lorsqu'est venu le moment de créer une nouvelle version de mon projet, GitFlow m'a rendu la tâche facile. Voici comment cela s'est passé :

- J'ai initié une nouvelle version en utilisant la commande suivante :
  ---->git flow release start ma-version
  Cela a créé une branche de version pour la prochaine itération de mon projet.

## 5.4. Fusion de la fonctionnalité

Une fois que j'ai terminé de travailler sur ma fonctionnalité, GitFlow m'a aidé à la fusionner en douceur dans la branche de développement. Voici comment j'ai géré cette étape :

- J'ai achevé ma fonctionnalité en utilisant la commande suivante :
  ---> git flow feature finish ma-fonctionnalite

## 5.5 Création d'un correctif

Enfin, si un correctif était nécessaire, GitFlow m'a permis de le gérer efficacement. Voici comment j'ai créé un correctif :

- J'ai commencé un correctif en utilisant la commande suivante :
  -----> git flow hotfix start mon-correctif
