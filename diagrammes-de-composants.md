---
layout: page
title: Diagrammes de composants
permalink: /diagrammes-de-composants/
nav_order: 4
has_children: true
has_toc: false
---


# Diagrammes de composants
Un **diagramme de composantes** présente une vue **statique** de **l'implémentation d'un système**.

## Représentation  
Une composante est une partie **physique** et **remplaçable** d'un système qui se conforme et réalise un ensemble d'interfaces.  
Une composante est **l'implémentation physique** de classes ou de paquetages.

![](/out/plant_uml/représentationComponentDiagram/représentationComponentDiagram.svg)

Les noms de composantes sont des noms tirés de **l'implémentation** du système. Par exemple, pour le diagramme ci-haut, on aurait pu avoir les [stéréotypes](https://fr.wikipedia.org/wiki/St%C3%A9r%C3%A9otype_(UML)) suivants: 
- ClientUI.dll (librairie)
- ProductAPI.exe (exécutable)
- OrderService.csv (document)
- PaymentService.py (fichier)  

## Relations

## Dépendances

## Vues

Il existe 2 façons de représenter les interfaces requises et fournies d'un composant.  
Dans cet exemple, le Composant1 **requiert** l'Interface et le Composant2 **fournie** l'Interface.

| *Assembly Connectors* | *Interface dependencies* |
|        :---:           |         :----:           |
| ![](/out/plant_uml/assemblyConnectorsExample/assemblyConnectorsExample.svg) | ![](/out/plant_uml/interfaceDependenciesExample/interfaceDependenciesExample.svg) |

Pour représenter les composants, il existe 2 vues

| Boîte noire | Boîte blanche |
|        :---           |         :----           |
| Cette vue ne montre que les interfaces associées aux composants. Elle ne contient aucun détail sur l'implémentation interne du composant. | En plus de représenter les interfaces associées aux composants, cette vue fournit les détails de l'implémentation interne du composant. |