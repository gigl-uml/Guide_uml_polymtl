---
layout: page
title: Diagrammes d'états
permalink: /diagrammes-etats/
nav_order: 8
has_children: true
has_toc: false
---

# Diagrammes d'états


Les diagrammes d'états illustrent les comportements d'un logiciel. Les machines à états peuvent être utilisées pour modéliser le comportement d'une classe, d'un sous-système ou d'une application entière. Elles offrent également un excellent moyen de modéliser les communications qui se produisent avec des entités externes via un protocole ou un système basé sur des événements.
UML comprend deux types de machines à états :

### Machines à états comportementales:  
Une machine à états comportementale représente une **implémentation** spécifique d'**un élément**.

### Machine à états de protocole:  
Elles montrent le **comportement d'un protocole**. Les machines à états de protocole montrent comment les participants peuvent déclencher des changements dans l'état d'un protocole et les changements correspondants dans le système (c'est-à-dire le nouvel état du protocole). 

# États

Les états modélisent un moment spécifique dans le comportement d'un système. Ce moment est défini par une condition qui est vraie dans le système. Plus simplement, un état est une "condition d'être" pour la machine à états.

Par exemple, une machine à café peut être dans l'état *Moudre les grains*, *Infuser*, *Réchauffer le café*, *Distribuer*, etc. Un état peut représenter une situation statique, comme *En attente d'un nom d'utilisateur*, ou une situation dynamique où l'état traite activement des données, comme *Chiffrer le message*.



## Représentation



## Exemple

Voici un exemple complet d'un **diagramme de cas d'utilisation** basé sur le cas d'étude [PolyAuto](../polyauto/).  
Le cas d'utilisation choisis représente la réservation d'un véhicule par l'utilisateur.

![](/out/plant_uml/useCaseGlobalExample/useCaseGlobalExample.svg)
