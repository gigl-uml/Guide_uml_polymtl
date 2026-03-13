---
layout: page
title: Diagrammes de paquetages
permalink: /diagrammes-de-paquetages/
nav_order: 3
has_children: true
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

# Diagrammes de paquetages

Visualiser, spécifier, construire et documenter de grands systèmes implique la manipulation d’un grand nombre de classes, interfaces, composantes, noeuds, diagrammes et autres éléments.  
Il est donc utile de regrouper les éléments communs en **paquetages** afin de pouvoir les comprendre et les
manipuler plus facilement.

## Représentation

Un simple paquetage est représenté ainsi:  
![](/out/plant_uml/singlePackagesRepresentation/singlePackagesRepresentation.svg)

Il y a deux façons de représenter le contenu des paquetages:

|                      À l'intérieur du paquetage                       |                         À l'aide de relations                          |
| :-------------------------------------------------------------------: | :-------------------------------------------------------------------: |
| ![](/out/plant_uml/packageReprésentation1/packageReprésentation1.svg) | ![](/out/plant_uml/packageReprésentation2/packageReprésentation2.svg) |

## Relations

| ------------ | ----------- | ----------- |
| _Containment_ | ![](/out/plant_uml/containmentRelationshipExample/containmentRelationshipExample.svg) | Indique que le paquetage A contient l'élément B. |
| _Import_ | ![](/out/plant_uml/importRelationshipExample/importRelationshipExample.svg) | Indique que le paquetage A importe les éléments du paquetage B. Donc, A aura accès au contenu de B. Cette relation est transitive, donc si A *<<import>>* B, alors tout paquetage qui importe A aura aussi accès aux éléments de B. |
| _Access_ | ![](/out/plant_uml/accessRelationshipExample/accessRelationshipExample.svg) | Indique que le paquetage A importe les éléments du paquetage B avec une visibilité privée. Ainsi, cette relation n'est pas transitive; si A *<<access>>* B, alors un paquetage qui importe A n'aura pas accès aux éléments de B. |
| _Merge_ | ![](/out/plant_uml/mergeRelationshipExample/mergeRelationshipExample.svg) | Indique que le paquetage A fusionne le paquetage B en fonction des règles suivantes: {::nomarkdown}<ul><li>Les membres privés d'un paquetage ne sont pas fusionnés.</li><li>Si des classes ont le même nom et le même type, alors l'élément source ajoute conceptuellement les caractéristiques de l'élément cible à ses propres caractéristiques, ce qui donne un élément qui combine les caractéristiques des deux dans le paquetage résultant (similaire à une généralisation).</li><li>Les classes qui n'existent que dans les paquetages fusionnés restent inchangés et sont ajoutés au paquetage résultant.</li><li>Si deux sous-paquetages porte le même nom existe dans les paquetages fusionnés, une autre fusion est lancée entre les deux sous-paquetages.</li><li>Toutes les importations de paquetage des paquetages fusionnés deviennent des importations du paquetage résultant.</li><li>Les sous-paquetages des paquetages fusionnés sont ajoutés au paquetage résultant s'ils n'existent pas déjà.</li></ul>{:/} |

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
