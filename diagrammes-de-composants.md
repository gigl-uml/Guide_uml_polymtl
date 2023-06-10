---
layout: page
title: Diagrammes de composantes
permalink: /diagrammes-de-composantes/
nav_order: 4
has_children: true
has_toc: false
---


# Diagrammes de composantes
Un **diagramme de composantes** présente une vue **statique** de **l'implémentation d'un système**. Les composantes sont les parties d'un système qui réalisent un ensemble d'interfaces (celles des autres composantes). Il existe trois catégories de composantes:
- Composante de déploiement: Nécéssaire pour construire un système exécutable
- Composante de réalisation: Résultats physiques du travail de développement (ex: code source)
- Composante d'exécution: Créées au moment de l'exécution du système.

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

Les **relations UML** suivantes représentes différents types de connection entre les composantes.  

| ------------ | ----------- | ----------- |
| Dépendance     | ![](/out/plant_uml/dependencyRelationshipComponent/dependencyRelationshipComponent.svg)         | Indique que A dépend de B. Des modifications dans l'élément cible (B) peuvent affecter l'élément source (A). |
| Réalisation | ![](/out/plant_uml/realizationRelationshipComponent/realizationRelationshipComponent.svg) | Indique que A fournit l'implémentation des méthodes de B. Représente la mise en œuvre concrète d'une interface par une classe.  |
| Ball and Socket | ![](/out/plant_uml/BallAndSocketRelationComponent/BallAndSocketRelationComponent.svg) | Indique que A utilise l'implémentation de l'interface C fournie par B.  |

## Vues

Il existe 2 façons de représenter les interfaces requises et fournies d'une composante.  
Dans cet exemple, le Composant1 **requiert** l'Interface et le Composant2 **fournie** l'Interface.

| *Assembly Connectors* | *Interface dependencies* |
|        :---:           |         :----:           |
| ![](/out/plant_uml/assemblyConnectorsExample/assemblyConnectorsExample.svg) | ![](/out/plant_uml/interfaceDependenciesExample/interfaceDependenciesExample.svg) |

Pour représenter les composantes, il existe 2 vues

| Boîte noire | Boîte blanche |
|        :---           |         :----           |
| Cette vue ne montre que les interfaces associées aux composantes. Elle ne contient aucun détail sur l'implémentation interne de la composante. | En plus de représenter les interfaces associées aux composantes, cette vue fournit les détails de l'implémentation interne de la composante. |

## Autres types de modélisation

Puisque les composantes représentent souvent des "morceaux" importants du système, il faut aussi savoir comment modéliser ces morceaux. Voici 3 exemples de modélisation architecturale:

### Modélisation de code source

![](/out/plant_uml/codeSourceModel/codeSourceModel.svg)

### Modélisation d'exécutable

![](/out/plant_uml/executableDiagram/executableDiagram.svg)

### Modélisation de base de données