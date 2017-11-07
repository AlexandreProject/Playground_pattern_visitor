# Présentation rapide du Design Pattern Visiteur

## Sa famille

Le Design Pattern Visiteur appartient à la famille des patterns **comportementaux**. Cette famille s'intéresse principalement aux comportements entre différents objets, en effet le visiteur est une classe définissant une opération sur une autre classe.

## Principe
 
Le Pattern Visiteur permet de séparer des données et les traitements associés pour ces données. Ce modèle de conception permet à une classe externe d'être informée du type exact d'instances d'un ensemble de classes.

> En pratique, le modèle de conception visiteur est réalisé de la façon suivante : chaque classe pouvant être « visitée » doit mettre à disposition une méthode publique « accepter » prenant comme argument un objet du type « visiteur ». La méthode « accepter » appellera la méthode « visite » de l'objet du type « visiteur » avec pour argument l'objet visité. De cette manière, un objet visiteur pourra connaître la référence de l'objet visité et appeler ses méthodes publiques pour obtenir les données nécessaires au traitement à effectuer (calcul, génération de rapport, etc.). 

::: Plus d'infos
+ [Définition Pattern Visiteur](https://fr.wikipedia.org/wiki/Visiteur_(patron_de_conception))
+ [Explications détaillés (en anglais)](https://sourcemaking.com/design_patterns/visitor)

:::

![Schéma d'utilisation Pattern Visiteur](https://upload.wikimedia.org/wikipedia/commons/f/fc/Visitorpattern.png)
Schéma du pattern Visiteur

## Caractéristiques

### Problématique
On peut parfois avoir à faire des opérations distinctes et indépendantes qui doivent être effectuées sur des noeud d'objet dans un ensemble de classes. Vous voulez éviter de "polluer" les classes "nœuds" (interface) avec ces opérations. De plus, vous ne voulez pas avoir à interroger le type de chaque nœud et à le caster sur le type correct avant d'effectuer l'opération souhaitée.

### Solution

### Conséquences

//Comment l'utiliser 
  //explication en détails
