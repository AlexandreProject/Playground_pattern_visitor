# Présentation rapide du Design Pattern Visiteur

## Sa famille

Le Design Pattern Visiteur appartient à la famille des patterns **comportementaux**. Cette famille s'intéresse principalement aux comportements entre différents objets, en effet le visiteur est une classe définissant une opération sur une autre classe.

## Principe
 
Le Pattern Visiteur permet de séparer des données et les traitements associés pour ces données. Ce modèle de conception permet à une classe externe d'être informée du type exact d'instances d'un ensemble de classes.

> En pratique, le modèle de conception visiteur est réalisé de la façon suivante : chaque classe pouvant être « visitée » doit mettre à disposition une méthode publique « accepter » prenant comme argument un objet du type « visiteur ». La méthode « accepter » appellera la méthode « visite » de l'objet du type « visiteur » avec pour argument l'objet visité. De cette manière, un objet visiteur pourra connaître la référence de l'objet visité et appeler ses méthodes publiques pour obtenir les données nécessaires au traitement à effectuer (calcul, génération de rapport, etc.). 

::: Plus d'infos
+ [Pattern Visiteur](https://fr.wikipedia.org/wiki/Visiteur_(patron_de_conception))
+ [Explications détaillés sur la structure (en anglais)](https://sourcemaking.com/design_patterns/visitor)

:::

Schéma du Design Pattern Visiteur
![Schéma d'utilisation Pattern Visiteur](https://upload.wikimedia.org/wikipedia/commons/f/fc/Visitorpattern.png)

Il est possible de créer des dérivées de la classe visiteuse, on peut créer autant d’opérations différentes pouvant être appliquée à la classe visitée sans avoir à en modifier le code.


## Intérêt

On peut facilement ajouter de nouveaux traitements sans toucher à la hiérarchie de nos objets (en POO "classique", on aurait implémenté de nouvelles méthodes pour ajouter de nouvelles fonctionnalités). Grâce aux Visiteurs :

   + le code est plus clair (des fonctionnalités différentes se trouvent dans des Visiteurs différents)
   + des équipes différentes peuvent travailler sur des fonctionnalités différentes sans gêner les autres équipes
   + on n'est pas obligé de tout recompiler à chaque ajout d'une fonctionnalité (seul le code du Visiteur est recompilé)


## Quand l'utiliser



# Quizz


