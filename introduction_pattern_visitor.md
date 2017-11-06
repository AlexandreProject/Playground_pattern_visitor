# Bienvenue

Bonjour à tous, ce playground va vous permettre d'apprendre et comprendre brièvement le Design Pattern Visiteur.

# Pattern ?

Lorsqu'on parle de pattern, il peut s'agir d'un motif, un modèle, une structure... C'est un phénomène que l'on observe de façon répétée, par exemple dans un jeu vidéo, un "boss" possède très souvent des patterns, dont il faudra exploiter pour le vaincre.

![Image Super Mario Bros](https://img4.hostingpics.net/pics/620119SuperMarioBrosVsBowser.png)
Dans _Super Mario Bros._, Bowser crache des boules de feu et saute à des intervalles réguliers, il suit donc certains patterns.

Dans le développement, un pattern constitue une solution générique pour un type de problème rencontré.

# Origine des Design Patterns 

L'origine des Designs Patterns viens des travaux d'un architecte, Christopher Alexander. Il remarque que la phase de construction en architecture possède des problèmes récurrents, il écrit alors un livre _A Pattern Language_ en 1977, il établi alors un nouveau langage avec 253 patterns, qui couvrent tous les aspects de la construction.

![Image de couverture "A Pattern Language"](https://img4.hostingpics.net/pics/130549apatternlanguage.jpg)

Ce n'est que plus tard dans les années 90, que l'idée d'Alexander va être reprise, plus particulièrement dans le domaine de conception de logiciel. Dans le livre _Design Patterns : Elements of Reusable Object-Oriented_ .

![Image de couverture "Design Patterns : Elements of Reusable Object-Oriented Software"](https://img4.hostingpics.net/pics/918603designpatternsgof.jpg)                                                                                                                                              
Publié en 1995 par Erich Gamma, Richard Helm, Ralph Johnson et John Vlissides, et plus généralement appélé **"Gang of Four"** (GoF), cette équipe présente 23 Design Patterns qui sont aujourd'hui des références dans le domaine de l'informatique.

# Design Pattern ?

Selon les personnes, un Design Pattern peut être appelé **"motif de conception"**, **"modèle de conception"** ou encore **"patron de conception"**, mais la signification reste la même.

## Définition

Finalement un Design Pattern est une **solution** à un **problème** récurrent dans la **conception** d'applications orientées objet. Nous allons voir que le Design Pattern Visiteur permet de concevoir un application où il sera facile d’ajouter des fonctionnalités à une classe sans la modifier. 

## Caractéristiques 

Un Design Pattern est représenté par 4 caractéristiques :
   - **Nom** : qui permet de l’identifier clairement
   - **Problématique** : description du problème auquel il répond
   - **Solution** : description de la solution souvent accompagnée d’un schéma UML
   - **Conséquences** : les avantages et les inconvénients de cette solution

## Les différents Design Patterns

Les 23 Designs Patterns peuvent être regroupés en 3 familles : 
- **Création** : ils permettent d’instancier et de configurer des classes et des objets.
- **Structure** : ils permettent d’organiser les classes d’une application.
- **Comportement** : ils permettent d'organiser les objets pour qu’ils collaborent entre eux.


## Comment s'en servir ?

1. Trouver le problème
2. Identifier le Design Pattern qui pourrait résoudre le problème
3. Créer sa propre solution en utilisant la solution générique du Design Pattern

Il est important de bien identifier le problème de conception avant de choisir un pattern, sinon le pattern choisi s'adaptera mal avec le problème et pourrait créer encore plus de problème qu'au départ.

# QCM

?[De quel design pattern va-t-on parler aujourd'hui ?]
-[ ] Je ne sais pas
-[ ] Singleton
-[x] Visiteur
-[ ] La réponse D

?[Qui à crée les premiers Designs Patterns pour la conception de logiciel ?]
-[x] "Gang of Four"
-[ ] Christopher Alexander

?[Qu'est-ce que n'est pas un Design Pattern ?]
-[ ] Un motif de conception
-[x] Un composant réutilisable et paramétrable
-[x] Un algorithme
-[ ] Une solution générique pour un ou plusieurs problèmes
-[ ] Ensemble de bonnes pratiques
-[x] Un framework

?[A votre avis, à quelle famille appartient le Design Pattern Visiteur ?]
-[ ] Création
-[ ] Structure
-[x] Comportement
