---
layout: page
title: Diagrammes de cas d'utilisation
permalink: /diagrammes-de-cas-dutilisation/
nav_order: 6
has_children: true
has_toc: false
---


# Diagrammes de cas d'utilisation
Le diagramme de **cas d'utilisation** permet de visualiser les cas
d’utilisation primaires d’un système.
- Ceci permet de voir rapidement les principales
fonctions d’un système.
- Plus particulièrement, le diagramme de contexte définit:
    - Les limites du système modélisé.
    - Les principaux acteurs du modèle.
    - Les cas d’utilisation primaires.  

## Cas d'utilisation
Un **cas d'utilisation** décrit un ensemble de séquences dans
lequel chacune des séquences représente l’interaction des acteurs
avec le système lui-même. Il représente les fonctions du système
visibles par les acteurs.  
Dans un **diagramme de cas d'utilisation**, chaque cas est représenté par un oval contenant son nom et son numéro.

![](/out/plant_uml/useCase/useCase.svg)


## Acteurs

Un acteur est une **entité externe** au système qui interagit avec celui-ci selon son rôle particulier.  
Par exemple, dans un contexte simple, un acteur peut être représenté comme suit:  
  
    
![](/out/plant_uml/acteurRepr%C3%A9sentation/acteurRepr%C3%A9sentation.svg)

Il peut y avoir plusieurs acteurs pour un même cas d'utilisation. Par exemple, dans l'exemple suivant, nous cherchons à modéliser le fonctionnement d'un restaurant à haut niveau:  

![](/out/plant_uml/restoExemple/restoExemple.svg)

## Modélisation avancée des cas d'utilisation