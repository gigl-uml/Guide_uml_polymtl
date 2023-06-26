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

Il est possible de représenter le temps de traitement ou l'attente d'un message par un participant à l'aide d'une occurrence d'exécution. Celles-ci sont illustrées par un rectangle vertical sur la ligne de vie.

## Représentation

Voici un exemple, montrant le participant **User** qui envoie une requête au participant **System**. Après un certain temps de traitement, illustré par l'occurrence d'exécution, **System** va renvoyer un message de réponse.  


![](/out/plant_uml/interactionRepresentationExample/interactionRepresentationExample.svg)

## Opérateur d'interaction
Un opérateur d'interaction est un élément utilisé dans les diagrammes de séquence pour spécifier le comportement et la structure des interactions entre les objets. Il permet de définir des scénarios d'exécution plus complexes en déterminant comment les messages sont échangés.

|---|---|---|
| *Alternates* | ![](/out/plant_uml/altOperatorExample/altOperatorExample.svg) | Représente différentes branches d'exécution, chaque branche étant associée à une condition qui détermine si cette branche est exécutée ou non. |
| *Option* | ![](/out/plant_uml/optOperatorExample/optOperatorExample.svg) | Similaire à alt, mais avec une seul opérande |
| *Break* | ![](/out/plant_uml/breakOperatorExample/breakOperatorExample.svg) | Indique une interruption du scénario, après l'exécution du fragment, si la condition est vrai. Par exemple, si P1.attr == True, alors message3() sera envoyé, mais pas message4(). |
| *Parallel* | ![](/out/plant_uml/parOperatorExample/parOperatorExample.svg) | Indique que les 2 fragments d'intéractions peuvent s'exécuter en parallèle, en gardant l'ordre des fragments originaux. Par exemple, message2() et message3() doivent être exécuté après message1(). |
| *Loop* | ![](/out/plant_uml/loopOperatorExample/loopOperatorExample.svg) | Indique que le fragment d'interactions sera exécuté en boucle. La condition de sortie peut être représenté avec une condition de sortie ou comme ceci: loop(min, max). |


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