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

### Les termes importants

Après avoir répondu aux premières questions sur la problématique, certains éléments vous paraissent clairs et d’autres totalement inconnus. Il est temps d’identifier les pistes de recherches qui permettront de : 

- Valider les éléments qui vous paraissent clairs.

- Chercher les réponses à ceux qui vous sont inconnus.

Mais, avant de commencer,il est nécessaire de connaître certains termes qui vous seront utiles : 

1. ***Analogie*** : C'est une ressemblance établie par l'esprit (association d'idées) entre deux ou plusieurs objets de pensée essentiellement différents.

    - Si le raisonnement par analogie peut être riche en tant que processus de représentation, de mise en perspective ou de créativité, il n’a cependant pas valeur de vérité. Si vous raisonnez par analogie, sachez que votre raisonnement, lorsqu’il s’applique à une étude des pratiques humaines, aboutit à une hypothèse (on fait la supposition que X et Y peuvent avoir tel et tel caractères communs, on s’interroge alors sur la valeur générale de ces ressemblances).
     
2. ***Signal faible*** : C'est une information perçue par un récepteur. Ce signal peut être blanc (neutre, invisible, non consciemment perçu), faible ou fort, selon son degré de perception et d’interpellation du récepteur.
    - Un signal dit faible est une information, mineure, qui nous fait buter, une aspérité. C’est quelque chose qui nous alerte et cela extrêmement rapidement, mais qu’il faut savoir repérer. Le « signe faible » plus que « signal » n’est que subjectivité, au sens où il répond à une intentionnalité, une volonté de le voir là où d’autres n’y prêteraient par attention. C’est en cela que l’on rapproche parfois le signal faible de l’intuition. Ainsi, les signaux faibles ne peuvent avoir, en eux-mêmes, de valeur représentative d’une situation. Cependant, dans la démarche d’observation et de construction d’une interprétation, il est utile de les présenter pour les éprouver ou éprouver une autre perception. L’objectif est de favoriser le débat et le doute utile, plus que la perception unique (qui conduirait à la décision ou la solution unique).
     
3. ***Jugement*** : Dans le cadre de votre démarche, le jugement est à proscrire. Vous vous intéressez ici à faire états de pratiques constatées, de faits reconnus, votre capacité d’analyse permettant de les mettre en perspective dans une interprétation. Cette interprétation est une vision construite, éclairée et vérifiée. Elle fait la valeur de votre travail d’inspiration et constituera, plus globalement, la valeur de votre démarche.
     
4. ***Problématique*** : L’ensemble construit autour d’une question principale, des hypothèses de recherche et des lignes d’analyse qui permettent de traiter le sujet. Durant la phase « inspiration », la problématique évolue au fur à mesure de l’avancée de votre enquête.
     
5. ***Hypothèses*** : Supposition que l’on fait d’une chose possible ou non et dont on tire des conséquences à vérifier. L’hypothèse est préparée par un travail de réflexion, elle dérive des analogies qu’aucune règle ne permet d’apercevoir et dirige le travail de recherche. Elle est soumise à un contrôle direct via l’enquête.
     
6. ***Présupposé*** : Supposition implicite — mais qu’il s’agit d’expliciter et de vérifier — qui sert de base au travail de l’observateur.
     
7. ***Postulat*** : Supposition explicite et assumée comme vraie/juste — c’est-à-dire factuelle (reconnue) ou constatée par les membres du groupe de travail. Axiome, hypothèse proposée à l’assentiment du destinataire du travail, comme fondements d’une proposition.
     
8. ***Public / usager*** : La démarche de recherche de terrain implique une ouverture d’esprit, vis-à-vis de son sujet et de ce que l’on observe. Considérer les humains observés sous l’angle du public, avant celle d’usager ou de potentiel usager, permet de ne pas restreindre trop vite l’observation à la dimension pratique d’usage.
    - On peut définir les publics d’un lieu, d’une offre, d’un service, d’une organisation comme tous les humains qui entrent en interaction avec cet objet. Avant l’usage, il s’agit donc de considérer les relations (représentations symboliques et relations constatées à travers les comportements) des publics avec l’objet questionné. Dresser une typologie des publics et celle de leurs relations, avant celle des usagers, participe efficacement de la vision prospective de la démarche de design. Par ailleurs, on préférera parler d’usager plutôt que d’utilisateur, à ce stade de la démarche. L’usager que l’on observe n’est pas forcément l’utilisateur final, celui que l’on vise dans la solution que l’on propose. On gardera donc à l’esprit le cheminement suivant : comprendre ses publics, identifier leurs pratiques, avant de déterminer des profils d’usagers, puis des profils d’utilisateurs.
     
9. ***Pratique espérée***: Dans notre contexte, c’est conception initiale, c’est-à-dire la manière dont on projette l’usage par un public/usager du service/produit ou de l’offre, du côté de l’organisation.
     
10. ***Pratique prescrite*** : C’est la solution existante, c’est-à-dire le résultat concret de la conception initiale, proposé par l’organisation aux publics/usagers.
     

11. ***Pratique vécue*** : C'est la représentation que se fait le public/usager du service/produit ou de l’offre. La pratique vécue correspond au point de vue subjectif d’une personne, capté dans son discours (par exemple sous forme d’entretien ou en écoute incognito des commentaires). Le discours est par essence filtrant, de plus certaines personnes n’hésitent pas à mentir, ainsi toujours mettre en regard cette pratique avec la pratique constatée.
     

12. ***Pratique constatée*** : Ce sont les usages et comportements constatés des publics/usagers, lors de l’observation.
-------------------------------------------------------------------------------
