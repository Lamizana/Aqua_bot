# Aqua-bot

-------------------------------------------------------------------------------

Développer et implémenter un système de mission dans un drone de surface (USV) virtuel au sein d’un environnement de développement et de simulation mis à disposition par les organisateurs.

L’édition 2024 de la compétition Aqua.Bot propose de vous affronter par équipe autour d’une mission simulée de maintenance d’un champ éolien. Les équipes participantes seront amenées à ***développer et implémenter un système de mission dans un drone de surface (USV)* virtuel au sein d’un environnement de développement et de simulation mis à disposition par les organisateurs***.

L’environnement de simulation proposé permet de s’affranchir des étapes de fabrication de l’USV, pour se concentrer sur la réalisation de l’automatisation du système durant les missions.

L’environnement proposé permet d’assurer la répétabilité de vos essais et ainsi d’évaluer les compétiteurs avec un échantillon de simulation suffisamment représentatif.

Les compétences minimums requises pour cette mission sont : **C++, Python, ROS2, Gazebo**

-------------------------------------------------------------------------------

## Introduction

### Design Thinking

Comprendre les bases de la méthodologie du **Design Thinking** : d'où vient-il, à quoi sert-il ?

Petit récapitulatif des 3 pilliers du Design Thinking :

- ***Désirabilité*** : Quel est de problème de mon utilisateur et est-ce que ma solution y répond ?

- ***Viabilité*** : Est-il prêt à payer pour cette solution ?

- ***Faisabilité*** : Mon équipe a-t-elle les moyens techniques de la développer ?

Et enfin, les *5 grandes étapes* de cette méthodologie :

- ***Observation*** : Prendre une posture empathique.

- ***Définition*** : Priorisation des problèmes de notre utilisateur.

- ***Idéation*** : Générer des idées de solutions.

- ***Prototypage*** : Concrétiser sa solution avec peu de moyens.

- ***Lancement*** : Définir une roadmap pour lancer son projet.

Le Design Thinking est une ***méthode Itérative*** ! 

> Revenir en arrière pour ajuster le projet n'est pas un problème, c'est même bien souvent nécessaire.

### Importance de la phase d'observation

Une étape primordiale dans le lancement ou l'accélération d'un projet pour connaître son marché et ses utilisateurs.

Dans cette phases, vous vous mettrez dans la peau d'un détective. Vous partirez à la rencontre de votre cible et de vos parties prenantes.

Le vocabulaire important :

- ***Empathie*** : Capacité à ressentir les émotions d'autrui, se mettre à sa place.

- ***Insight*** : Enseignements clés que vous récolterez auprès de vos utilisateurs.

- ***Benchmark*** : Travail d'exploration destiné à analyser, mesurer et comprendre les fonctionnements et forces d'un marché et de vos concurrents.

- ***Parties prenantes***: Personnes ou organisation, directes ou indirectes, qui entourent l'utilisateur.


### Identifier les parties prenantes 

Le ***Stakeholder map***

À qui s'adresse votre idée et quels sont les acteurs qui gravitent autour de lui et influent son parcours ?

Le but de cette étape est de **comprendre l'environnement de votre utilisateur**, les liens qui existent entre les différents acteurs qui le composent ainsi que leurs enjeux.

Les 3 catégories de ce canva (canva Stakeholder map) :

- **Utilisateurs** : Votre cible finale.

- **Parties prenantes directes** : les acteurs qui auront une influence directe sur l'utilisateur.

- **Parties prenantes indirectes**: les acteurs qui auront une influence indirecte sur lui.


### Analyser la problématique

Les objectifs de cette capsule sont d'acquérir les connaissances nécessaires au *décorticage d'une problématique*, savoir identifier à qui elle s'adresse et son but.

Petit rappel, votre solution ne vaut rien sans un réel problème et son marché. C’est pour cela qu’il est ***important de définir une problématique claire et de quantifier le nombre de personnes touchées par cette problématique***.

Cependant, les problématiques confiées à des équipes d’innovations, ou les premières problématiques identifiées par des startups ne sont pas toujours pertinentes : le problème est vaguement identifié, l’utilisateur n’est pas toujours mentionné, la solution imaginée fait partie intégrante de la problématique, etc… 

> [!NOTE]
> Une phase de compréhension et de cadrage de la problématique est donc nécessaire.

**Albert Einstein** disait: 
- “Si j’ai une heure pour résoudre un problème, je prends 55 minutes pour bien le poser et 5 minutes pour le résoudre”.

En effet, durant toute notre scolarité, on nous a appris à répondre à des énoncés qui nous sont donnés, mais pas à réécrire ces énoncés. 

L’objectif de cette première capsule est donc de bien ***cadrer la problématique qui nous a été confiée pour préparer notre stratégie d’observation***.

Voici la liste des première questions à se poser sur notre problématique : 

- Est-ce que je comprends la problématique à la première lecture ?

- Est-ce que j’arrive à définir le problème explicité par cette problématique ? 

- Est-ce que j’ai déjà été confronté à ce problème ? 

- Est-ce que je connais des personnes qui ont été confrontées à ce problème ? 

- Est-ce que le problème me paraît pertinent ? 

- Est-ce que le problème s’inscrit dans un problème plus large ? 

- Pourquoi choisir ce problème et pas le problème plus large ?

- Est-ce que j’arrive à identifier à qui s’adresse la problématique ?

- Est-ce que la problématique s’adresse bien à un seul type d’usager ? 

- Quel est cet usager ? 

- Est-ce que cet usager est le plus pertinent ? 

- Quel est le but de la résolution de la problématique ? 

- La problématique est-elle suffisamment ouverte pour me permettre de l’explorer ? 

- Est-ce que cette problématique s’inscrit dans une démarche plus globale ? 

- Est-ce que cette problématique est issue de recherches précédentes ?

- Si oui, quelles sont ces recherches ? 

- Est-ce que je comprends l’objectif derrière cette problématique ?

> [!IMPORTANT]
L’objectif de ces premières questions est d’ouvrir la problématique, et de commencer sa stratégie d'observation.

-------------------------------------------------------------------------------
