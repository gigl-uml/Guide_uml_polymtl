---
layout: page
title: Diagrammes de contexte
permalink: /diagrammes-de-contexte/
nav_order: 3
has_children: true
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

# Diagramme de contexte

Le diagramme de **cas de contexte** présentent les cas
d’utilisation primaires d’un système sans aller dans les détails.

- Ceci permet de voir rapidement les principales
  fonctions d’un système.
- Plus particulièrement, le diagramme de contexte définit:
  - Les limites du système modélisé.
  - Les principaux acteurs du modèle.
  - Les cas d’utilisation primaires.

## Comment savoir si un cas d'utilisation est primaire ? 

Les **tests de pertinence** servent à identifier les cas primaires.

- Le **test du patron** : mon patron sera-t-il satisfait de moi si je passe ma journée à effectuer ce cas d’utilisation ?​
- Le **test du processus d’affaire élémentaire** : un processus d’affaire élémentaire est une tâche accomplie par une personne à un endroit et un moment donnés, en réponse à un évènement d’affaire, qui ajoute une quantité mesurable de valeur et laisse les données dans un état consistant.​
- Le **test de la dimension** : un cas d’utilisation est extrêmement rarement constitué d’une seule action ou étape. Un cas d’utilisation comprend typiquement plusieurs étapes, et dans un format étendu nécessite souvent de 3 à 10 pages de texte afin de le décrire.​

Dans un **diagramme de cas d'utilisation**, chaque cas est représenté par un oval contenant son nom et son numéro. **Le nom commence par un verbe.**

![Diagramme de contexte](/assets/images/diagramme_contexte.png)

## Frontières du système

Les **cas d'utilisation** capturent par définition les **fonctionnalités d'un sujet spécifique**. Toute fonctionnalité qui n'est pas implémentée par ce sujet est considérée comme étant en dehors des limites du système et doit être **représentée sous forme d'acteur**. Ceci permet de déterminer clairement la portée et les responsabilités associées.  
Les **frontières du système** sont représentées par un rectangle avec le nom du système en haut.

## Acteurs

Un acteur est une **entité externe** au système qui interagit avec celui-ci selon son rôle particulier.  
Par exemple, dans un contexte simple, un acteur peut être représenté comme suit:

![](/out/plant_uml/acteurRepr%C3%A9sentation/acteurRepr%C3%A9sentation.svg)

Il peut y avoir plusieurs acteurs pour un même cas d'utilisation. C'est le cas du CU 3 du diagramme de contexte ci-dessus.