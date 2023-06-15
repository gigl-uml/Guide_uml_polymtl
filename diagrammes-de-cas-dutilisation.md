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

Le livre **UML 2.0 in a Nutshell** spécifie 3 exigences pour aider à cadrer un cas d'utilisation:

1. Avant de pouvoir le compléter, le cas d'utilisation doit être initié par un acteur
2. Quand un cas d'utilisation est jugée complété, alors la fonctionnalité souhaitée a été exécutée ou une erreur s'est produite
3. Après la complétion du cas d'utilisation, le système est dans un été où le cas peut-être redémarré, ou le système est dans un état d'erreur
## Acteurs

Un acteur est une **entité externe** au système qui interagit avec celui-ci selon son rôle particulier.  
Par exemple, dans un contexte simple, un acteur peut être représenté comme suit:  
  
    
![](/out/plant_uml/acteurRepr%C3%A9sentation/acteurRepr%C3%A9sentation.svg)

Il peut y avoir plusieurs acteurs pour un même cas d'utilisation. Par exemple, dans l'exemple suivant, nous cherchons à modéliser le fonctionnement d'un restaurant à haut niveau:  

![](/out/plant_uml/restoExemple/restoExemple.svg)

## Relation  

| ------------ | ----------- | ----------- |
| Généralisation d'acteurs | ![](/out/plant_uml/actorsGeneralizationExample/actorsGeneralizationExample.svg) | Indique que le le *GenericActor* est une versions générale des 2 autres acteurs. Donc, le *GenericUseCase* sera complété par *Actor1* et *Actor2*. |
| Généralisation de cas d'utilisation| ![](/out/plant_uml/useCaseGeneralizationExample/useCaseGeneralizationExample.svg) | Indique que les fonctionnalités complétées par le *useCase1* et le *useCase2* peuvent être généralisé dans un seul cas d'utilisation ; *GenericUseCase*. |
| Inclusion de cas d'utilisation | ![](/out/plant_uml/useCaseInclusionExample/useCaseInclusionExample.svg) | Indique que le *useCase2* n'est pas complet, il a **besoin** de la fonctionnalité de *useCase1* pour fonctionner. Cette relation permet de pouvoir réutiliser certain cas d'utilisation. |
| Extension de cas d'utilisation | ![](/out/plant_uml/useCaseExtensionExample/useCaseExtensionExample.svg) | Indique que le *useCase1* va ajouter des fonctionnalités (étendre) le *useCase2*. Contrairement à l'inclusion, le cas d'utilisation de base (*useCase2*) doit pouvoir fonctionner seul. |