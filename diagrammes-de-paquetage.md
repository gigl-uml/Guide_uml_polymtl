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
Un simple paquet est représenté ainsi:  
![](/out/plant_uml/singlePackagesRepresentation/singlePackagesRepresentation.svg)

Il y'a 2 façons de représenter le contenu des paquetages.

| ------------ | ----------- | ----------- |
| À l'intérieur du paquet | ![](/out/plant_uml/packageReprésentation1/packageReprésentation1.svg) | TODO |
| À l'aide de relation | ![](/out/plant_uml/packageReprésentation2/packageReprésentation2.svg) | TODO |

## Visibilité
Les éléments d'un paquet peuvent être **publicss** ou **privés**.  
La visibilité publique indique que cet élément est utilisable en dehors du paquet.  
La visibilité privée indique le contraire : seulement les autres éléments du même paquet peuvent utiliser l'élément privé.  
Un élément public est indiqué par un signe plus. Un élément privé est indiqué par un signe moins.

![](/out/plant_uml/packageVisibility/packageVisibility.svg)

## Importer et Accéder aux paquets

## Fusionner les paquets