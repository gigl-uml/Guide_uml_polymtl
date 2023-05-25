---
layout: page
title: Diagrammes de classes
permalink: /diagrammes-de-classes/
nav_order: 2
has_children: true
---



# Diagrammes de classes
{: .no_toc }

Les diagrammes de classes sont utilisés pour :
-   Explorer les concepts d'un domaine
-   Analyser les besoins à l'aide d'un modèle conceptuel 
-   Décrire de façon détaillée une conception orienté objet


## Sommaire
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Classes
Une classe est le schéma de construction d'un objet. Elle décrit une collection d'objets qui
partagent les mêmes attributs, les mêmes opérations, les mêmes relations et la même sémantique.  
Elles sont représentées par des rectangles séparés en trois parties:  

1. Le nom de la classe. Il doit être unique, constitué d'une chaine de caractères, centré et la première lettre doit être en majuscule
2. Les attributs
3. Les opérations

![](/out/classexample/classexample.svg)


## Attributs
Il existe 2 notations permettant de représenter des attributs:  

1. En ligne (*inlined attributes*):  
    **visibilité / nom : type multiplicité = défaut**

    | ------------ | ----------- |
    | Visibilité   | {public: +, privé: -, protégé: #, paquet: ~} |
    | /            | La présence de ce symbole indique que la valeur de cet attribut peut être obtenue à l'aide d'autres attributs déjà dans le modèle                           |
    | Nom          | Le nom de l'attribut                          |
    | Type         | Le type de l'attribut                         |
    | Multiplicité | Le nombre d'instances de l'attribut [min..max]            |
    | Défaut       | La valeur par défaut de l'attribut            |

    ![](/out/attributesInlineExample/attributesInlineExample.svg)

2. Par relation:

    Permet de montrer plus de détails des attributs sur le diagramme  
    
    ![](/out/attributeRelationExample/attributeRelationExample.svg)  

## Opérations

Il est important de faire la distinction entre une **opération** et une **méthode**. Une opération permet de représenter comment **déclencher** un comportement, tandis qu'une méthode montre l'implémentation de ce comportement. Voici quelques exemples d'opérations:
- `- getFuelAmount(): Rectangle`
- `+ setFuelAmount(quantity: int): void`
- `# accelerate()`

*Notez bien que depuis la sortie de la norme UML 2.0, il n'est plus obligatoire de spécifier le type de retour d'une opération. Lorsque le type de retour n'est pas spécifié, on ne peut rien supposer quant au type de retour*



## Méthodes
Une **méthode** est une **implémentation** d'une **opération**. Cette implémentation peut être définie par la classe en elle même, ou héritée de sa superclasse. Si aucune implémentation n'est fournie, l'opération est dite **abstraite**.  
Dans le diagramme de classes, on ne fait pas de distinctions entre méthodes et opérations.

## Classes abstraites

## Relations

Les relations UML représentes différents types de connection entre les classes.  

| ------------ | ----------- | ----------- |
| Dépendance     | ![](/out/dependencyRelationshipExample/dependencyRelationshipExample.svg)         | Indique que A dépend de B. Des modifications dans l'élément cible (B) peuvent affecter l'élément source (A). |
| Association    | ![](/out/associationRelationshipExample/associationRelationshipExample.svg)       | Relation plus forte que la dépendance. Indique qu'il existe un lien sémentique ou structurel entre A et B.  |
| Agrégation    | ![](/out/aggregationRelationshipExample/aggregationRelationshipExample.svg)       | Relation plus forte que l'association. Indique que A possède B. |
| Composition    | ![](/out/compositionRelationshipExample/compositionRelationshipExample.svg)       | Relation plus forte que l'agrégation. Indique que B est une partie de A. |
| Généralisation | ![](/out/generalizationRelationshipExample/generalizationRelationshipExample.svg) | Indique que A est une version générale de B. Exprime une hiérarchie d'héritage. |
| Réalisation | ![](/out/realizationRelationshipExample/realizationRelationshipExample.svg) | Indique que A fournit l'implémentation des méthodes de B. Représente la mise en œuvre concrète d'une interface par une classe.  |




## Interfaces

Une interaface est un élément de modélisation qui représente un ensemble de spécifications pour les services fournis par une classe ou un composant. Elle possède les déclarations des attributs et des méthodes, mais pas d'implémentation. C'est l'équivalent d'une classe abstraite pure en C++.

Il existe 2 façons de représenter une interface:  

1. Notation Standard:

    Dans cette exemple, la classe *Array* implémente les interfaces *ICollection*, *IList* et *IEnumerable*.
    ![](/out/interfaceStandardNotationExample/interfaceStandardNotationExample.svg)  

    Si une classe *User* veut utiliser l’implémentation de IList de la classe Array:  

    ![](/out/interfaceStandardNotationExample2/interfaceStandardNotationExample2.svg)  

2. Notation *ball-and-socket*:

    On représente la class *Array* comme ceci:  

    ![](/out/interfaceBallAndSocketNotationExample/interfaceBallAndSocketNotationExample.svg)

    Si une classe *User* veut utiliser l'implémentation de IList de la classe *Array*:  

    ![](/out/interfaceBallAndSocketNotationExample2/interfaceBallAndSocketNotationExample2.svg)

## Modèles
