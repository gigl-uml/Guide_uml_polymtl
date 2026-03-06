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

## Frontières du système et acteurs

Comme dans le diagramme de contexte, les **frontières du système** des cas d'utilisation sont représentées par un rectangle avec le nom du système en haut. Les acteurs sont les mêmes.

## Relations

| ------------ | ----------- | ----------- |
| Inclusion de cas d'utilisation | ![](/out/plant_uml/useCaseInclusionExample/useCaseInclusionExample.svg) | Indique que le _casUtilisation1_ n'est pas complet, il a **besoin** de la fonctionnalité de _CasUtilisation2_ pour fonctionner. Cette relation permet de pouvoir réutiliser certains cas d'utilisation. |
| Extension de cas d'utilisation | ![](/out/plant_uml/useCaseExtensionExample/useCaseExtensionExample.svg) | Indique que le casUtilisation1 va ajouter des fonctionnalités (étendre) au casUtilisation2, lequel doit pouvoir fonctionner seul. |

## Exemple

Voici des exemples d'un **diagramme de cas d'utilisation** basé sur le cas d'étude [PolyCal](../polycal/).  

![Cas 1](/assets/images/cu1.png)

![Cas 2](/assets/images/cu2.png)