---
layout: page
title: Diagrammes de cas d'utilisation
permalink: /diagrammes-de-cas-dutilisation/
nav_order: 6
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
| Généralisation d'acteurs | ![](/out/plant_uml/actorsGeneralizationExample/actorsGeneralizationExample.svg) | Indique que l' _ActeurGénérique_ est une version générale des 2 autres acteurs. Donc, le _CasGénérique_ sera complété par _Acteur1_ et _Acteur2_. |
| Généralisation de cas d'utilisation| ![](/out/plant_uml/useCaseGeneralizationExample/useCaseGeneralizationExample.svg) | Indique que les fonctionnalités complétées par le _casUtilisation1_ et le _casUtilisation2_ peuvent être généralisés dans un seul cas d'utilisation ; _CasGénérique_. |
| Inclusion de cas d'utilisation | ![](/out/plant_uml/useCaseInclusionExample/useCaseInclusionExample.svg) | Indique que le _casUtilisation1_ n'est pas complet, il a **besoin** de la fonctionnalité de _casUtilisation2_ pour fonctionner. Cette relation permet de pouvoir réutiliser certains cas d'utilisation. |
| Extension de cas d'utilisation | ![](/out/plant_uml/useCaseExtensionExample/useCaseExtensionExample.svg) | Indique que le _casUtilisation1_ va ajouter des fonctionnalités (étendre) au _casUtilisation2_, lequel doit pouvoir fonctionner seul. |

## Exemple

Voici un exemple complet d'un **diagramme de cas d'utilisation** basé sur le cas d'étude [PolyAuto](../polyauto/).  
Le cas d'utilisation choisis représente la réservation d'un véhicule par l'utilisateur.

![](/out/plant_uml/useCaseGlobalExample/useCaseGlobalExample.svg)
