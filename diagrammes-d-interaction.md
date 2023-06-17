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

## Représentation

### Participants aux interactions
Les participants aux interactions d'un diagramme de séquence sont représenté à l'aide d'un rectangle et d'une ligne verticale pointillé, également appelées « lignes de vie ». Le nom du participant suit cette syntaxe:  

**nom_de_l'objet [sélecteur] : nom_de_la_classe**

| ------------ | ----------- |
| nom_de_l'objet | Le nom de l'instance impliqué dans l'intéraction |
| sélecteur | Permet de selectionner une instance particulière dans un tableau d'élement |
| nom_de_la_classe  | Le nom du type du participant |

### Message
Les messages sont des flèches représentant des communications entre participant.

### Boîte d'activation
Il est possible d'utilisé une boîte d'activation, représenté par une boîte sur la ligne de vie, pour montré que l'objet du participant attend un message réponse ou est occupé dans un processus.

Voici un exemple, montrant le participant **User** qui envoie une requête au **System**. Après un certain temps de calcul, illustré par la boîte d'activation, le **System** va renvoyer un message de réponse.

![](/out/plant_uml/interactionRepresentationExample/interactionRepresentationExample.svg)

## Relation  

|---|---|---|
| Message asynchrone | TODO |  |
| Message synchrone | TODO |  |
| Message de Réponse | TODO |  |
| Message de Création | TODO |  |
| Message perdu | TODO |  |
| Message trouvé | TODO |  |





## Exemple