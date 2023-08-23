---
layout: page
title: Diagrammes de composantes
permalink: /diagrammes-de-composantes/
nav_order: 4
has_children: true
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

# Diagrammes de composantes

Un **diagramme de composantes** permet de décomposer la représentation d’un logiciel en sous-systèmes, représenté par des composantes. Celles-ci réalisent un ensemble d'interfaces (celles des autres composantes).

## Représentation

Une composante est une partie **physique** et **remplaçable** d'un système qui se conforme et réalise un ensemble d'interfaces.  
Une composante est **l'implémentation physique** de classes ou de paquetages.

![](/out/plant_uml/représentationComponentDiagram/représentationComponentDiagram.svg)

Les noms de composantes sont des noms tirés de **l'implémentation** du système. Par exemple, pour le diagramme ci-haut, on aurait pu avoir :

- ClientUI.dll (librairie)
- ProduitsAPI.exe (exécutable)
- CommandeService.csv (document)
- PaiementService.py (fichier)

## Relations

Les **relations UML** suivantes représentent différents types de connexion entre les composantes.

| ------------ | ----------- | ----------- |
| Dépendance | ![](/out/plant_uml/dependencyRelationshipComponent/dependencyRelationshipComponent.svg) | Indique que A dépend de B. Cette relation est souvent utilisée dans un contexte où un composant A nécessite une interface B.  |
| Réalisation | ![](/out/plant_uml/realizationRelationshipComponent/realizationRelationshipComponent.svg) | Indique que A fournit l'implémentation d'une interface B. |
| Ball and Socket | ![](/out/plant_uml/BallAndSocketRelationComponent/BallAndSocketRelationComponent.svg) | Indique que A utilise l'implémentation de l'interface C fournie par B. |

## Vues

Il existe deux façons de représenter les interfaces requises et fournies d'une composante.  
Dans cet exemple, le Composant1 **requiert** l'Interface et le Composant2 **fournit** l'Interface.

|                            _Assembly Connectors_                            |                             _Interface dependencies_                              |
| :-------------------------------------------------------------------------: | :-------------------------------------------------------------------------------: |
| ![](/out/plant_uml/assemblyConnectorsExample/assemblyConnectorsExample.svg) | ![](/out/plant_uml/interfaceDependenciesExample/interfaceDependenciesExample.svg) |

Pour représenter les composantes, il existe deux vues

| Boîte noire                                                                                                                                    | Boîte blanche                                                                                                                                |
| :--------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------- |
| Cette vue ne montre que les interfaces associées aux composantes. Elle ne contient aucun détail sur l'implémentation interne de la composante. | En plus de représenter les interfaces associées aux composantes, cette vue fournit les détails de l'implémentation interne de la composante. |

## Autres types de modélisation

Puisque les composantes représentent souvent des "morceaux" importants du système, il faut aussi savoir comment modéliser ces morceaux. Voici 3 exemples de modélisation architecturale:

|                       Code source                       |                         Exécutable                          |                            Base de données                            |
| :-----------------------------------------------------: | :---------------------------------------------------------: | :-------------------------------------------------------------------: |
| ![](/out/plant_uml/codeSourceModel/codeSourceModel.svg) | ![](/out/plant_uml/executableDiagram/executableDiagram.svg) | ![](/out/plant_uml/databaseRepresentation/databaseRepresentation.svg) |

## Exemple

Voici un exemple d'un **diagramme de composantes** basé sur le cas d'étude [PolyAuto](../polyauto/).

![](/out/plant_uml/exempleDiagComponent/exempleDiagComponent.svg)
