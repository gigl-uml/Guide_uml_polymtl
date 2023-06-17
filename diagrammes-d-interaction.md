---
layout: page
title: Diagrammes d'interaction
permalink: /diagrammes-d-interaction/
nav_order: 8
has_children: true
has_toc: false
---


# Diagrammes d'interaction
Un diagramme d'interaction permet de montrer **chronologiquement** les **messages échangés** entre les différents acteurs, objets ou composants d'un système pendant un **scénario spécifique**. Il met l'accent sur la **séquence des actions** et des **messages** échangés entre les différentes entités pour accomplir une tâche particulière.  

Un type spécifique de diagramme d'interaction est le **diagramme de séquence**. C'est celui que nous utiliserons dans ce chapitre.  

## Participants aux interactions
Les participants aux interactions d'un diagramme de séquence sont représenté à l'aide d'un rectangle et d'une ligne verticale pointillé, également appelées « lignes de vie ». Le nom du participant suit cette syntaxe:  

**nom_de_l'objet [sélecteur] : nom_de_la_classe**

| ------------ | ----------- |
| nom_de_l'objet | Le nom de l'instance impliqué dans l'intéraction |
| sélecteur | Permet de selectionner une instance particulière dans un tableau d'élement |
| nom_de_la_classe  | Le nom du type du participant |

## Message et Occurrence d'exécution 
Les messages sont des flèches représentant des communications entre participant. Le texte juste au-dessus de la flèche d'un message représente le nom ou la description du message échangé entre les objets.

Il est possible de représenter le temps de traitement ou l'attente d'un message par un participant à l'aid d'une occurrence d'exécution. Celles-ci sont illustrées par un rectangle vertical sur la ligne de vie.


## Invariants d'état
TODO  

## Conditions de garde et Opérateur d'intéraction
TODO  

## Représentation

Voici un exemple, montrant le participant **User** qui envoie une requête au participant **System**. Après un certain temps de traitement, illustré par l'occurrence d'exécution, **System** va renvoyer un message de réponse.  


TODO: NEED BIGGER EXAMPLE  

![](/out/plant_uml/interactionRepresentationExample/interactionRepresentationExample.svg)

## Relation  

|---|---|
| Message asynchrone | ![](/out/plant_uml/asyncMessageExample/asyncMessageExample.svg) |
| Message synchrone | ![](/out/plant_uml/syncMessageExample/syncMessageExample.svg) |
| Message de Réponse | ![](/out/plant_uml/responseMessageExample/responseMessageExample.svg) |
| Message de création | ![](/out/plant_uml/createMessageExample/createMessageExample.svg) |
| Message de destruction | ![](/out/plant_uml/destroyMessageExample/destroyMessageExample.svg) |
| Message perdu | ![](/out/plant_uml/custom/lostMessageExample.svg) |
| Message trouvé | ![](/out/plant_uml/custom/foundMessageExample.svg) |





## Exemple