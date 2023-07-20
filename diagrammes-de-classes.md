---
layout: page
title: Diagrammes de classes
permalink: /diagrammes-de-classes/
nav_order: 2
has_children: true
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

# Diagrammes de classes

Les **diagrammes de classes** sont utilisés pour :

- Explorer les concepts d'un domaine
- Analyser les besoins à l'aide d'un modèle conceptuel
- Décrire de façon détaillée une conception orientée objet

---

## Classes

Une **classe** est le schéma de construction d'un objet. Elle décrit une collection d'objets qui
partagent les mêmes attributs, les mêmes opérations, les mêmes relations et la même sémantique.  
Elles sont représentées par des rectangles séparés en trois parties:

1. Le nom de la classe. Il doit être unique, constitué d'une chaine de caractères, centré et la première lettre doit être en majuscule.
2. Les attributs
3. Les opérations

[![](/out/plant_uml/classexample/classexample.svg)](https://github.com/justinlachap/justinlachap.github.io/blob/main/plant_uml/classexample.plantuml){:target="\_blank"}

## Attributs

Il existe 2 notations permettant de représenter des **attributs**:

1. En ligne (_inlined attributes_):  
   **visibilité / nom : type multiplicité = défaut**

   | ------------ | ----------- |
   | Visibilité | {public: +, privé: -, protégé: #, paquet: ~} |
   | / | La présence de ce symbole indique que la valeur de cet attribut peut être obtenue à l'aide d'autres attributs déjà dans le modèle |
   | Nom | Le nom de l'attribut |
   | Type | Le type de l'attribut |
   | Multiplicité | Le nombre d'instances de l'attribut [min..max] |
   | Défaut | La valeur par défaut de l'attribut |

   ![](/out/plant_uml/attributesInlineExample/attributesInlineExample.svg)

2. Par relation:  
   ![](/out/plant_uml/attributeRelationExample/attributeRelationExample.svg)

## Opérations

Il est important de faire la distinction entre une **opération** et une **méthode**. Une opération permet de représenter comment **déclencher** un comportement, tandis qu'une méthode montre l'implémentation de ce comportement. Voici quelques exemples d'opérations:

- `- getNiveauEssence(): float`
- `+ setNiveauEssence(quantite: int): void`
- `# accélérer()`

_Notez bien que depuis la sortie de la norme UML 2.0, il n'est plus obligatoire de spécifier le type de retour d'une opération. Lorsque le type de retour n'est pas spécifié, on ne peut rien supposer quant au type de retour_

### Opérations statiques

Il est possible de créer des opérations qui appartiennent à la classe plutôt qu'à ses instances. Ces opérations dites "statiques" sont appelées directement sur la classe, il n'est donc pas nécéssaire de créer une instance pour pouvoir engendrer un certain comportement. Les opérations statiques doivent être soulignées:

- <code style="text-decoration: underline;">+ kphVersMph(kph: float): float</code>

## Méthodes

Une **méthode** est une **implémentation** d'une **opération**. Cette implémentation peut être définie par la classe en elle même, ou héritée de sa superclasse. Si aucune implémentation n'est fournie, l'opération est dite **abstraite**.  
Dans le diagramme de classes, on ne fait pas de distinctions entre méthodes et opérations.

## Classes abstraites

Une **classe abstraite** est une classe pouvant fournir des **opérations** comprenant **aucune implémentation**.  
Les classes abstraites sont représentées par un nom en _italique_ ou sont identifiées par le classificateur _<<abstract>>_.  
Toutes les opérations ne possédant pas d'implémentation sont elles aussi représentées en _italique_. Contrairement à une interface, une classe abstraite **peut contenir des méthodes**.

![](/out/plant_uml/abstractClassExample/abstractClassExample.svg)

## Relations

Les **relations UML** représentent différents types de connexion entre les classes.

| ------------ | ----------- | ----------- |
| Dépendance | ![](/out/plant_uml/dependencyRelationshipExample/dependencyRelationshipExample.svg) | Indique que A dépend de B. Des modifications dans l'élément cible (B) peuvent affecter l'élément source (A). |
| Association | ![](/out/plant_uml/associationRelationshipExample/associationRelationshipExample.svg) | Relation plus forte que la dépendance. Indique qu'il existe un lien sémentique ou structurel entre A et B. |
| Agrégation | ![](/out/plant_uml/aggregationRelationshipExample/aggregationRelationshipExample.svg) | Relation plus forte que l'association. Indique que A possède B. |
| Composition | ![](/out/plant_uml/compositionRelationshipExample/compositionRelationshipExample.svg) | Relation plus forte que l'agrégation. Indique que B est une partie de A. |
| Généralisation | ![](/out/plant_uml/generalizationRelationshipExample/generalizationRelationshipExample.svg) | Indique que A est une version générale de B. Exprime une hiérarchie d'héritage. |
| Réalisation | ![](/out/plant_uml/realizationRelationshipExample/realizationRelationshipExample.svg) | Indique que A fournit l'implémentation des méthodes de B. Représente la mise en œuvre concrète d'une interface par une classe. |
| Ball and Socket | ![](/out/plant_uml/BallAndSocketRelationExample/BallAndSocketRelationExample.svg) | Indique que A utilise l'implémentation de l'interface C fournie par B. |

## Interfaces

Une interface est un élément de modélisation qui représente un ensemble de spécifications pour les services fournis par une classe ou un composant. Elle possède les déclarations des attributs et des méthodes, mais pas d'implémentation. C'est l'équivalent d'une classe abstraite pure en C++.

Il existe 2 façons de représenter une interface:

|                                                                                                          |                                      Notation Standard                                      |                                                                            Notation _ball-and-socket_ |
| :------------------------------------------------------------------------------------------------------- | :-----------------------------------------------------------------------------------------: | ----------------------------------------------------------------------------------------------------: |
| Dans cette exemple, la classe _Array_ implémente les interfaces _ICollection_, _IList_ et _IEnumerable_. |  ![](/out/plant_uml/interfaceStandardNotationExample/interfaceStandardNotationExample.svg)  |   ![](/out/plant_uml/interfaceBallAndSocketNotationExample/interfaceBallAndSocketNotationExample.svg) |
| Si une classe _Utilisateur_ veut utiliser l'implémentation de IList de la classe _Array_.                | ![](/out/plant_uml/interfaceStandardNotationExample2/interfaceStandardNotationExample2.svg) | ![](/out/plant_uml/interfaceBallAndSocketNotationExample2/interfaceBallAndSocketNotationExample2.svg) |

## Modèles

Un **modèle** de classe - ou classe **générique** - fournit un moyen de créer des classes qui peuvent fonctionner avec différents types de données sans avoir à réécrire le code pour chaque type spécifique.  
En UML, on peut les représenter de cette manière :

![](/out/plant_uml/templateExample/templateExample.svg)

## Exemple

Voici un exemple complet d'un **diagramme de classes** basé sur le cas d'étude [PolyAuto](../polyauto/).

![](/out/plant_uml/exempleDiagClasse/exempleDiagClasse.svg)
