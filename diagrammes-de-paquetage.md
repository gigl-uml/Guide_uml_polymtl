---
layout: page
title: Diagrammes de paquetages
permalink: /diagrammes-de-paquetages/
nav_order: 3
has_children: true
has_toc: false
---

# Diagrammes de paquetages

Visualiser, spécifier, construire et documenter de grands systèmes implique la manipulation d’un grand nombre de classes, interfaces, composantes, noeuds, diagrammes et autres éléments.  
Il est donc utile de regrouper les éléments communs en **paquetages** afin de pouvoir les comprendre et les
manipuler plus facilement.

## Représentation

Un simple paquetage est représenté ainsi:  
![](/out/plant_uml/singlePackagesRepresentation/singlePackagesRepresentation.svg)

Il y a 2 façons de représenter le contenu des paquetages.

|                      À l'intérieur du paquetage                       |                         À l'aide de relation                          |
| :-------------------------------------------------------------------: | :-------------------------------------------------------------------: |
| ![](/out/plant_uml/packageReprésentation1/packageReprésentation1.svg) | ![](/out/plant_uml/packageReprésentation2/packageReprésentation2.svg) |

## Relations

| ------------ | ----------- | ----------- |
| _Containment_ | ![](/out/plant_uml/containmentRelationshipExample/containmentRelationshipExample.svg) | Indique que le paquetage A contient l'élément B. |
| _Import_ | ![](/out/plant_uml/importRelationshipExample/importRelationshipExample.svg) | Indique que le paquetage A importe les éléments du paquetage B. Donc, A aura accès au contenu de B. |
| _Access_ | ![](/out/plant_uml/accessRelationshipExample/accessRelationshipExample.svg) | Indique que le paquetage A importe les éléments du paquetage B avec une visibilité privée. |
| _Merge_ | ![](/out/plant_uml/mergeRelationshipExample/mergeRelationshipExample.svg) | Indique que le paquetage A fusionne le paquetage B. Donc, le contenu du paquetage B va étendre celui du paquetage A. |

## Visibilité

Les éléments d'un paquetage peuvent être **publics** ou **privés**.  
La visibilité publique indique que cet élément est utilisable en dehors du paquetage.  
La visibilité privée indique le contraire : seulement les autres éléments du même paquetage peuvent utiliser l'élément privé.  
Un élément public est indiqué par un signe plus. Un élément privé est indiqué par un signe moins.

![](/out/plant_uml/packageVisibility/packageVisibility.svg)

## Importer et accéder aux paquetages

Il est possible d'importer des éléments d'un paquetage à l'autre. Pour ce faire, il faut qu'un paquetage `<<import>>` un autre paquetage, ce qui lui permettra d'accéder à toutes les classes de ce dernier. Par exemple:

![](/out/plant_uml/importRelationPackage/importRelationPackage.svg)

Dans ce cas-ci, le `PayrollSystem` pourra accéder aux classes présentes dans le paquetage `EmployeeTimeSheet`.

Par défaut, les éléments importés sont **publics**, c'est-à-dire qu'ils peuvent être accédés par d'autres paquetages qui importeraient, dans notre cas, `PayrollSystem`.
Il est possible d'importer des éléments de manière **privée** avec l'annotation `<<access>>`, c'est-à-dire qu'ils ne seront accessibles que par le paquetage qui les importe. Par exemple:

![](/out/plant_uml/accessRelationPackage/accessRelationPackage.svg)

## Fusionner les paquetages

L'UML offre la possibilité de fusionner des paquetages. Ce mécanisme plutôt complexe est rarement utilisé en industrie.  
Vous pouvez trouver plus de détails sur ce sujet dans la section **3.4. Merging Packages** du livre **UML 2.0 in a Nutshell** de Pilone et Pitman.

## Exemple

Voici un exemple complet d'un **diagramme de paquetages** basé sur le cas d'étude [PolyAuto](../polyauto/).

![](/out/plant_uml/exempleDiagPaquet/exempleDiagPaquet.svg)
