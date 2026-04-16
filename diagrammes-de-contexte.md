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
d’utilisation principaux d’un système sans aller dans les détails.

- Ceci permet de voir rapidement les principales
  fonctions d’un système.
- Plus particulièrement, le diagramme de contexte définit:
  - Les limites du système modélisé.
  - Les principaux acteurs du modèle.
  - Les cas d’utilisation principaux.

## Cas principaux

**Comment savoir si un cas d'utilisation fait partie des cas principaux ?**

On considère **importants** les cas d’utilisation qui:
1. Ont un **impact important sur l’architecture du système**, par exemple parce qu’ils introduisent beaucoup de concepts ou classes, ou exigent de la persistance.
2. Contiennent beaucoup **d’information sur la conception** sans nécessairement nécessiter beaucoup d’effort.
3. Contiennent des fonctions **risquées, complexes ou urgentes**. 
4. Impliquent des **efforts** importants de **recherche** ou l’utilisation de **nouvelles technologies**. 
5. Représentent **l’activité commerciale principale**. 
6. Impliquent directement des **revenus supplémentaires** ou des **réductions de coûts**.

Dans un **diagramme de contexte**, chaque cas est représenté par un oval contenant son nom et son numéro. **Le nom commence par un verbe.**

## Frontières du système

Les **cas d'utilisation** capturent par définition les **fonctionnalités d'un sujet spécifique**. Toute fonctionnalité qui n'est pas implémentée par ce sujet est considérée comme étant en dehors des limites du système et doit être **représentée sous forme d'acteur**. Ceci permet de déterminer clairement la portée et les responsabilités associées.  
Les **frontières du système** sont représentées par un rectangle avec le nom du système en haut.

## Acteurs

Un acteur est une **entité externe** au système qui interagit avec celui-ci selon son rôle particulier.  
Par exemple, dans un contexte simple, un acteur peut être représenté comme suit:

![](/out/plant_uml/acteurReprésentation/acteurReprésentation.svg)

Il peut y avoir plusieurs acteurs pour un même cas d'utilisation. C'est le cas du CU 3 du diagramme de contexte ci-dessous.

## Exemple

Voici un exemple d'un **diagramme de contexte** basé sur le cas d'étude [PolyCal](../polycal/).

![Diagramme de contexte](/assets/images/diagramme_contexte.png)
