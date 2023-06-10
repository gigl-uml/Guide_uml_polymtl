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
Un **nœud** est un élément physique qui existe au moment de l'exécution et qui représente une ressource ayant des possibilités d'exécution.

// TODO

## Représentation

Voici un exemple illustrant un artéfact "Application Web" déployé dans le noeud "Serveur Web" et un artéfact "Base de données MySQL" déployé dans le noeud "Serveur de Base de Données".

![](/out/plant_uml/deploymentRepresentation/deploymentRepresentation.svg)
## Relation 

|---|---|---|
| Manifestation | ![](/out/plant_uml/manifestationRelationshipExample/manifestationRelationshipExample.svg) | Indique que l'artéfacte est une manifestation (ou une implémentation) logiciel de la composante. |
| Communication | ![](/out/plant_uml/communicationRelationExample/communicationRelationExample.svg) | Indique que le Noeud1 et le Noeud2 communiquent entre eux à l'aide du protocole de communication P1. |
| Déploiement | ![](/out/plant_uml/deployRelationExample/deployRelationExample.svg) | C'est une autre façon de représenter qu'un artéfact est contenu dans un noeud. Donc que l'artéfact est déployé dans le noeud. |

## Déploiement

## Variations
