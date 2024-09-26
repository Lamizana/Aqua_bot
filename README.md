# Aqua-bot

> By alex LAMIZANA, Mathys VITIELLO, Nathan TRIJAUD
-------------------------------------------------------------------------------
## Introduction

Développer et implémenter un système de mission dans un drone de surface (USV) virtuel au sein d’un environnement de développement et de simulation mis à disposition par les organisateurs.

L’édition 2024 de la compétition Aqua.Bot propose de vous affronter par équipe autour d’une mission simulée de maintenance d’un champ éolien. Les équipes participantes seront amenées à ***développer et implémenter un système de mission dans un drone de surface (USV)* virtuel au sein d’un environnement de développement et de simulation mis à disposition par les organisateurs***.

L’environnement de simulation proposé permet de s’affranchir des étapes de fabrication de l’USV, pour se concentrer sur la réalisation de l’automatisation du système durant les missions.

L’environnement proposé permet d’assurer la répétabilité de vos essais et ainsi d’évaluer les compétiteurs avec un échantillon de simulation suffisamment représentatif.

Les compétences minimums requises pour cette mission sont : **C++, Python, ROS2, Gazebo**

https://www.sirehna-challengeaquabot.com/program/challenge-aquabot-2

### Objectifs

L’automatisation complète de l’USV est demandée aux participants.

Dans le cadre de la maintenance du parc éolien, ***le drone doit réaliser trois tâches successives*** pour compléter la mission WINDWATCH :

- Inspection du statut de chaque éolienne
    
- Identification de l’éolienne défaillante dans le champ

- Stabilisation & Maintenance devant l’éolienne défaillante


### Deroulement du Challenge

Le challenge se déroulera en 4 phases :

- **Observation** (1 semaine) :
    - Installation et prise en main de l’environnement de simulation
    - Se référer au manuel utilisateur fourni au lancement de la compétition.

- **Idéation** (1 semaine) :
    - Organisation des équipes et projets.
    - Adoptez une approche agile en divisant l'objectif en sous-objectifs.

- **Prototypage** (8 semaines) :
    - Développement et mise en œuvre de l’USV et de son système de mission en suivant une approche collaborative et participative.
    
- **Pitch** (2 semaines) :
    - Mise en forme du dossier final et préparation à la présentation orale.

### Livrable de mi-parcours

Merci de ***télécharger votre livrable de mi-parcours d'ici le 18 octobre 2024 23h***.

Voici la structure attendue (3/4 slides) : 

- 1 slide qui présente votre équipe et votre organisation au quotidien (fréquences de vos réunions, présentiel/distanciel,...) ;
    
- 1 à 2 slides sur vos avancées aujourd’hui (matériel et logiciels utilisés, état d'avancement de votre prototype) ;
    
- 1 slide présentant vos objectifs et vos attentes (formation, intervenants,..) pour la suite du programme. 


### Description de l’environnement de simulation

L’environnement de développement de simulation **Gazebo ainsi que le framework de robotique ROS2 sont imposés**. Il sera mis à la disposition de chaque équipe inscrite un manuel utilisateur comprenant le guide d’installation de l’environnement ainsi que le guide de prise en main de ces outils.

Cet environnement se charge de simuler l’environnement marin (mer, bateaux, houle …), ainsi que le comportement de votre USV et de ses capteurs. Il met également à disposition des scénarios d’entrainement qui permettent aux équipes d’évaluer la performance de leurs algorithmes avec les mêmes critères que ceux qui seront utilisés pour le classement des équipes.

> [!IMPORTANT]
> L’USV mis à votre disposition est un monocoque de 6 mètres de long avec deux propulseurs azimutaux. Il aura une vitesse maximale de 12 nœuds.

### Environnement

L’environnement marin dans lequel évolue les bateaux est soumis à une faible houle, mais sans aucun courant ni vent.

La taille de la zone de jeu est définie par défaut autour du point d’apparition de votre USV, par un carré de taille de ***600 mètres x 600 mètres***.

L'environnement maritime contient des obstacles statiques, tel que des éoliennes, des ilots ou encore des rochers.

### Les scénarios

Vos algorithmes seront évalués sur des scénarios différents, allant d’un niveau facile jusqu’à difficile. Nous mettons à votre disposition pour vous aider durant la compétition un certain nombre de scénarios de façon à faciliter votre autoévaluation.

> Les équipes seront libres d’ajouter des scénarios complémentaires pour leur entrainement.

**Chaque scénario durera 20 minutes durant lesquels il faudra compléter les 3 étapes, ainsi que potentiellement l’étape BONUS**.

Les éléments d’un scénario pouvant être amenés à changer automatiquement sont :

- La position des éoliennes.

- Le statut des éoliennes.

- L’orientation du QR code d’identification.

- L’éolienne sur laquelle effectuer la maintenance,

- Les vagues et le vent.

Nous fixerons des valeurs maximales pour chaque élément au début de la compétition.

### Développements à réaliser

> [!IMPORTANT]
> L’automatisation complète de votre USV est demandée.

3 étapes clés seront à réaliser pour compléter la ***mission WINDWATCH*** :

- **Étape 1** : *Inspection du statut de chaque éolienne* :
    Il devra naviguer au sein de l’environnement en évitant les collision pour aller identifier chacune des éoliennes en scannant leur QR code et en renvoyant leurs données à la plateforme.

- **Étape 2** : *Identification de l’éolienne défaillante dans le champ* :
    - Un ping de la plateforme leur sera envoyé avec l’identification de l’éolienne sur laquelle l’équipage doit intervenir, votre USV devra donc retrouver l’éolienne correspondant à la demande de la plateforme et la rallier.

- **Étape 3** : *Stabilisation & Maintenance devant l’éolien défaillante* :
    - Maintenir la position de l’USV devant l’éolienne pour la bonne conduite de la maintenance.

- **Étape Bonus** : *Round trip* :
    - Effectuer 2 tours complet de l’éolienne en conservant un cap précis afin de s’assurer du bon état de celle-ci.

Les modules suivants devront être développés :

- Un module de perception pour traiter les données capteur, détecter les éoliennes et lire les QR code.

- Un module de guidage et contrôle de l’USV faisant les choix de route et envoyant les ordres de contrôle à la propulsion.

### Paramètres de notation

Chaque équipe devra fournir avant la date spécifiée :

- Le **code source** des modules développés compatibles avec l’environnement de simulation fournit.

- **Un rapport** précisant :
    - L’organisation de l’équipe mise en place dans le cas d’un développement collectif.
    - Une description des algorithmes mis en place.
    - Une notice d’installation (préciser le cas échéant la méthode d’installation de librairies complémentaires par exemple).
    - Les difficultés rencontrées et leur résolution si résolus.

> [!IMPORTANT]
> Chaque équipe recevra une note qui sera la somme d’une évaluation sur le rapport, d’une évaluation sur la performance et d’une évaluation sur leur pitch de présentation durant la finale.

- Il sera également demandé à l’issue de la phase d’IDEATION une présentation des équipes et projets.

#### Evaluation du rapport et de la qualité de codage :

- Qualité générale du rapport : observation et design thinking, gestion de projet et roadmap.
    
- Niveau technique des solutions proposées, et clarté de la description.
    
- Qualité générale du code livré.

- 15 pages maximum.

> [!WARNING]
> Une pénalité par jour de retard (date de réception, quelle que soit l’heure) sur la livraison du code source et/ou du rapport sera comptabilisée.

#### Evaluation de la performance selon des critères spécifique et écart type :

**Toute collision entrainera la fin du scénario**. Les points accumulés avant la collision resteront comptabilisé

Seront comptabilisés comme collision : La collision avec un obstacle fixe (rochers, phare, éolienne...).

Une inspection du code livré sera réalisée pour identifier toute tentative de triche. En cas de doute sur ce qui autorisé ou non, contacter l’équipe organisatrice.

#### Evaluation du pitch :

Une finale réunissant l’ensemble des participants sera organisée dans les locaux de Sirehna, au Technocampus Océan, 5 rue de l’Halbrane, **44340 BOUGUENAIS, France**.

Durant la finale, votre équipe devra ***présenter ses travaux pendant un pitch de courte durée (entre 5 et 7 minutes) devant un jury***, à l’aide d’un support visuel composé d’un ***maximum de 10 slides*** pour votre pitch-deck*. A l’issu des présentations, une note vous sera attribuée.

Celle-ci sera alors pondérée avec votre rapport et la performance de votre USV durant les tests.

Les équipes victorieuses seront annoncées durant l’événement final.

-------------------------------------------------------------------------------

## Observation

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



### Les limites planétaires 

Comme le corps à ses limites, la planète aussi.

Il s'agit d'un outil de mesure scientifique qui permet d'améliorer l’information sur les risques de changements environnementaux. Des changements environnementaux qui résultent des activités humaines susceptibles d’affecter les écosystèmes et le bien-être de manière générale.

> [!IMPORTANT]
> Ce concept des limites planétaires définit un espaace de développement sûr et juste pour l'humanité.

Actuellement, il est fondé sur ***9 processus biophysiques*** qui, ensemble, régulent la stabilité de la planète :

- le changement climatique
- l’érosion de la biodiversité
- la perturbation des cycles biogéochimiques de l’azote et du phosphore
- les changements d’utilisation et l'usage des sols
- l’acidification des océans
- l’utilisation mondiale de l’eau douce
- l’appauvrissement de l’ozone stratosphérique
- l’augmentation des aérosols dans l’atmosphère
- l’introduction d’entités nouvelles dans la biosphère.

Ce sont des seuils quantitatifs à ne pas dépasser sont définis pour chacun d'entre eux sous peine de perdre la stabilité du système et donc l'hospitalité de la Terre.

**Pourquoi les avoir en tête tout au long du CPi ?**

Même si elle sont encore le sujet de recherches par les scientifiques et les limites planétaire ***sont un parfait rappel que les enjeux environnementaux ne concernent pas seulement le climat et le CO2***. 

Gardez les en tête quand vous abordez les enjeux environnementaux de votre projet et ne réfléchissez pas seulement en terme d'émission carbone (même si c'est déjà un bon début 🙂).

**S'inspirer du droit à la nature pour changer notre vision du monde**

Evidemment prendre en compte les besoins de la nature n'est pas une chose facile, faut-il encore "rentrer en empathie" avec elle. Afin de mieux, cerner les enjeux environnementaux de votre problématique et de mettre les besoins de la planète au même niveau que celui des êtres humains. Je te propose un petit jeux à mettre en place tout au long du CPI, inspiré directement du droit à la nature : 

> Le droit à la nature, c'est donner une personnalité juridique aux fleuves, aux lacs et autres espaces naturels : c'est à dire que des fleuves, des montagnes, des forêts se voient progressivement reconnaître comme des personnes juridiques.


### Reproblématiser

Bienvenue dans cette capsule sur la reproblématisation. Nous verrons ce à quoi sert une problématique et intégrerons les notions de nuance de problématique.

Vous avez vu, dans un précédent module, comment analyser une problématique. Grâce aux premières recherches que vous avez réalisées, vous êtes désormais capable de la préciser et la transformer en une problématique d’innovation.

En suivant la méthodologie du Design Thinking, une problématique de projet d’innovation fait apparaître trois éléments :

- ***L'action*** : "Quoi"
- ***L'utilisateur*** : "Qui"
- ***Le bénéfice de la résolution du problème***: "Pour quoi"

Nous arrivons donc à des question de types : 

- Comment pourrions-nous  pour afin de ?
- Comment pourrions-nous aider , à afin de ?

Exemple concret : 

- Comment pourrions nous ***simplifier la réservation de voyage de vacances*** pour ***les étudiants*** dans le supérieur afin de leur ***permettre d’organiser des voyages facilement avec leurs amis*** ?

Cette formulation permet de mettre à plat et de toujours garder en tête l’objectif, *l’enjeu* et *la cible* à qui *s’adresse le projet*. Vous remarquerez que chaque élément est décrit de manière claire. Il faut trouver le juste milieu entre simplicité et exhaustivité dans la formulation pour que la problématique soit précise tout en restant simple à comprendre. Elle évoluera au fur et à mesure de vos observations afin de définir le plus précisément possible le besoin de votre utilisateur. 

Cette problématique vous suivra tout au long du projet. La finalité des phases d’observation et de définition des besoins est d’arriver à définir les différents éléments qui se concrétisent en une problématique qui prend en compte les enseignements clés récoltés. 

Maintenant c’est à vous de reformuler le problème qui vous a été posé en prenant en compte les premières recherches que vous avez réalisées de manière à ce qu’elle prenne la forme d’une problématique d’innovation !

-------------------------------------------------------------------------------

## Idéation

### La fiche idée

A l’issue de la phase d’idéation, il est important de développer plusieurs concepts pour tester différentes propositions de valeur, prioriser les fonctionnalités à intégrer dans un prototype et affiner la solution qui saura répondre aux besoins utilisateurs.

La fiche idée permet de formaliser les concepts ayant vu le jour durant la phase de créativité afin de faciliter les choix lors de l’étape suivante. 

Elle permet d’expliciter la solution envisagée, les problèmes adressés, les raisons d’y croire ainsi que les premières fonctionnalités ou caractéristiques imaginées. 

Il est important de donner un nom à chaque fiche idée par souci de lisibilité mais aussi pour projeter les valeurs portées par le concept. Dessiner la solution vous permet de réfléchir à un premier prototype.

Voici les différentes parties à remplir d'une fiche idée : 

- ***Nom de la solution*** : Ici, rien de plus que le nom de votre produit/service. Pas de panique, il pourra changer au cours de votre avancée !
    Problèmes adressés : Dans cette seconde case, explicités sous formes de tirets tous les problèmes de vos utilisateurs que vous souhaitez résoudre grâce à votre solution.
    
- ***Détails de la solution*** : Ensuite, détaillez la solution : quelle forme prend-elle ?, comment s'utilise-t-elle ?, comment vous ferez en sorte que vos utilisateurs l'utiliserons et la garderons ?... 
    
- ***Raisons d'y croire*** : Rédigez cette partie comme si vous vendiez la solution à un investisseur : des mots précis qui donneront envie de vous suivre car on croit en votre projet.
    
- ***Dessin de la piste d'innovation*** : "1 image vaut 1000 mots" : dessinez, tant bien que mal, un aperçu de l'idée que vous vous faites de la solution : c'est important pour faire passer des idées.

- ***Obstacles*** : Pour finir : la transparence. Si des points vous semblent bloquants, n'hésitez pas à les mettre en avant, vous serez accompagnés et challengés dessus.


### La proposition de valeur

Une proposition de valeur efficace peut se résumer en une phrase. 

Celle-ci doit contenir : 
- Le nom du concept ou du projet.
- Le type de solution proposée.
- La cible d’utilisateurs.
- Leur problème.
- La fonction clef du projet.
- Comment celui-ci permet de répondre au problème des utilisateurs. 

Une fois clairement définie, **cette proposition de valeur sera le fil rouge du développement du produit**. Elle peut également être très utile pour tester la désirabilité du concept ou du projet, notamment  à travers des tests utilisateurs, et se prête bien aux méthodes digitales d’AB Testing. 

Pour bien mettre au clair votre proposition de valeur, le canva qui lui est associé est très utile.

> [!NOTE]
> Ce canva se dessine sur deux grands axes : la proposition de valeur et le segment client.

**Le premier axe** sert à visualiser la valeur créée par votre solution, on y trouvera 3 sous-catégories :

- ***Produits et services*** : fonctionnalités du concept qui répondent au problème
    
- ***Problèmes résolus*** : les problèmes auxquels ces produits et services répondent
    
- ***Bénéfices créés*** : comment les produits et services maximisent la satisfaction des utilisateurs

**Le second** sert à bien comprendre son utilisateur :

- ***Aspiration client*** : ce que l’utilisateur veut réaliser (fonctionnel, social, émotionnel). 
    
- ***Bénéfices*** : ce que les utilisateurs espèrent tirer de la satisfaction de leur besoin

- ***Problèmes*** : ce qui empêche l’utilisateur de satisfaire son besoin

Bon courage pour mettre au clair votre proposition de valeur !
