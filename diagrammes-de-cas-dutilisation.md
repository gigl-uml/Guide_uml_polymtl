---
layout: page
title: Diagrammes de cas d'utilisation
permalink: /diagrammes-de-cas-dutilisation/
nav_order: 4
has_children: true
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

# Diagrammes de cas d'utilisation

Le diagramme de **cas d'utilisation** permet de visualiser en détail un cas d'utilisation d’un système. Il illustre :
  - Les limites du système modélisé.
  - Les acteurs du cas d'utilisation.
  - Le cas d’utilisation principal et ses sous-cas.

## Cas d'utilisation

Un **cas d'utilisation** décrit un ensemble de séquences dans
lequel chacune des séquences représente l’interaction des acteurs
avec le système lui-même. Il représente les fonctions du système
visibles par les acteurs.  
Dans un **diagramme de cas d'utilisation**, chaque cas est représenté par un ovale contenant son nom et son numéro.

![](/out/plant_uml/useCase/useCase.svg)

Le livre **UML 2.0 in a Nutshell** spécifie trois exigences pour aider à cadrer un cas d'utilisation:

1. Avant de pouvoir le compléter, le cas d'utilisation doit être initié par un acteur.
2. Quand un cas d'utilisation est jugée complété, alors la fonctionnalité souhaitée a été exécutée ou une erreur s'est produite.
3. Après la complétion du cas d'utilisation, le système est dans un état où le cas peut-être redémarré, ou le système est dans un état d'erreur.

## Frontières du système

Les **cas d'utilisation** capturent par définition les **fonctionnalités d'un sujet spécifique**. Toute fonctionnalité qui n'est pas implémentée par ce sujet est considérée comme étant en dehors des limites du système et doit être **représentée sous forme d'acteur**. Ceci permet de déterminer clairement la portée et les responsabilités associées.  
Les **frontières du système** sont représentées par un rectangle avec le nom du système en haut.

## Acteurs

Un acteur est une **entité externe** au système qui interagit avec celui-ci selon son rôle particulier.  
Par exemple, dans un contexte simple, un acteur peut être représenté comme suit:

![](/out/plant_uml/acteurReprésentation/acteurReprésentation.svg)

Il peut y avoir plusieurs acteurs pour un même cas d'utilisation. Par exemple, dans l'exemple suivant, nous cherchons à modéliser le fonctionnement d'un restaurant à haut niveau:

![](/out/plant_uml/restoExemple/restoExemple.svg)

## Relations

| ------------ | ----------- | ----------- |
| Inclusion de cas d'utilisation | ![](/out/plant_uml/useCaseInclusionExample/useCaseInclusionExample.svg) | Indique que le _casUtilisation1_ n'est pas complet, il a **besoin** de la fonctionnalité de _CasUtilisation2_ pour fonctionner. Cette relation permet de pouvoir réutiliser certains cas d'utilisation. |
| Extension de cas d'utilisation | ![](/out/plant_uml/useCaseExtensionExample/useCaseExtensionExample.svg) | Indique que le casUtilisation1 va ajouter des fonctionnalités (étendre) au casUtilisation2, lequel doit pouvoir fonctionner seul. |

## Exemples

Voici des exemples d'un **diagramme de cas d'utilisation** basé sur le cas d'étude [PolyCal](../polycal/).  

![Cas 1](/assets/images/cu1.png)

![Cas 2](/assets/images/cu2.png)