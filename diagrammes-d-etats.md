---
layout: page
title: Diagrammes d'états
permalink: /diagrammes-etats/
nav_order: 9
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

Par exemple, une machine à café peut être dans l'état _Moudre les grains_, _Infuser_, _Réchauffer le café_, _Distribuer_, etc. Un état peut représenter une situation statique, comme _En attente d'un nom d'utilisateur_, ou une situation dynamique où l'état traite activement des données, comme _Chiffrer le message_.

## Représentation

Voici un exemple de diagramme d'états qui illustre le comportement d'un lave-vaisselle. Il y a 3 états: **Lavage**, **Rinçage** et **Séchage**:

![](/out/plant_uml/stateDiagRepresentation/stateDiagRepresentation.svg)


### Lien avec le Patron État

Les diagrammes d'états sont en quelque sorte une représentation visuelle du [Patron État](https://refactoring.guru/design-patterns/state){:target="\_blank"}. Ce patron de conception permet à un objet de changer de comportement en fonction de son état. L'objet se comportera comme s'il avait changé de classe.  
Durant l'exécution, l'état de l'objet va varier et son comportement suivra les instructions d'un switch-case, par exemple.

## Exemple
