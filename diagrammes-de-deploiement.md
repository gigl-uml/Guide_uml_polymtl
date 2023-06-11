---
layout: page
title: Diagrammes de déploiement
permalink: /diagrammes-de-deploiement/
nav_order: 5
has_children: true
has_toc: false
---


# Diagrammes de déploiement
Un **diagramme de déploiement** présente la **configuration physique** des ordinateurs et
périphériques ainsi que les **composantes qui s‘y exécutent**.

## Artéfacts
Un Artéfact représente un morceau de logiciel, de matériel ou de données qui est déployé sur un nœud du système. Il peut être un fichier exécutable, une bibliothèque, une base de données, un fichier de configuration, etc.


## Nœuds
Un **nœud** est un élément physique qui existe au moment de l'exécution et qui représente une ressource ayant des possibilités d'exécution. La taille des nœud est variable : elle peut varier d'un simple dispositif embarqué à un ensemble de serveurs.  
Les nœuds indiquent le **lieu d'exécution** du code et comment les différentes parties du système **communiquent lors de l'exécution**.  




## Représentation

Généralement, on représente les nœuds sous forme d'une boîte en trois dimensions. Cependant, il est courant d'utiliser des représentations d'icônes spécifiques pour les nœuds afin d'aider à transmettre le type de matériel utilisé

Voici un exemple illustrant un artéfact "Application Web" déployé dans le noeud "Serveur Web" et un artéfact "Base de données MySQL" déployé dans le noeud "Serveur de Base de Données".

![](/out/plant_uml/deploymentRepresentation/deploymentRepresentation.svg)
## Relation 

|---|---|---|
| Manifestation | ![](/out/plant_uml/manifestationRelationshipExample/manifestationRelationshipExample.svg) | Indique que l'artéfacte est une manifestation (ou une implémentation) logiciel de la composante. |
| Communication | ![](/out/plant_uml/communicationRelationExample/communicationRelationExample.svg) | Indique que le Noeud1 et le Noeud2 communiquent entre eux à l'aide du protocole de communication P1. |

## Déploiement

Il existe 2 façons de montrer le déploiement d'un artéfact dans un noeud.  


| À l'intérieur du noeud | À l'aide d'une relation de dépendance |
|        :---:           |         :----:           |
| ![](/out/plant_uml/deployRelationExample2/deployRelationExample2.svg) | ![](/out/plant_uml/deployRelationExample/deployRelationExample.svg) |

## Variations
