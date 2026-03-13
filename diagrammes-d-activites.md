---
layout: page
title: Diagrammes d'activités
permalink: /diagrammes-d-activites/
nav_order: 7
has_children: true
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

# Diagrammes d'activités

Un **diagramme d'activités** est utilisé pour modéliser et représenter visuellement le **déroulement d'un processus**. Il permet de visualiser les étapes, les actions, les décisions et les boucles d'un processus, ce qui facilite la compréhension, l'analyse et l'amélioration des activités.  
Les **diagrammes d'activités** sont utiles pour **clarifier** les responsabilités, **planifier** les projets, **documenter** les systèmes et **faciliter** la communication **entre les parties prenantes**.

## Activités et actions

Une **activité** se réfère à un comportement qui est divisé en une ou plusieurs **actions**. Chaque **action** représente une **étape unique** (il n'est pas nécessaire de décomposer davantage l'action dans le diagramme, bien que cela ne garantisse pas que l'action soit simple ou atomique) au sein de l'activité, où des données sont manipulées ou traitées.

Les **activités** sont généralement réutilisées plusieurs fois au sein du système, tandis que les **actions** sont plus spécifiques et utilisées uniquement au sein d'une seule activité.

## Représentation

Une **activité** est représentée par un rectangle aux coins arrondis, avec son nom et ses paramètres associés dans le coin supérieur gauche.  
Une **action** est elle aussi représentée par un rectangle aux coins arrondis.

Le flux au sein des activités est représenté à l'aide d'arêtes d'activités entre les **actions**. Elles sont matérialisées à l'aide de flèches. Les arêtes spécifient **comment les données circulent d'une action à la suivante**. Les actions qui ne sont pas ordonnées par des arêtes peuvent s'exécuter de manière concurrente.

![](/out/plant_uml/custom/activityRepresentation.svg)

Les **activités** possèdent généralement un **point de départ** ainsi qu'un ou plusieurs **points d'arrivée**. Lorsqu'un point d'arrivée est atteint, l'activité prend fin. On les représente de la sorte :

![](/out/plant_uml/custom/activityStartNode.svg)

Certaines actions se déroulent en parallèle. Pour qu'un point d'arrivée d'un flux ne mette pas fin à toute l'activité, UML 2.0 fournit des **points d'arrivées de flux**, représentés par un cercle contenant une croix.

## Préconditions et postconditions

Les activités et les actions peuvent être accompagnées de certaines **conditions**.  
Les **activités** peuvent avoir des **pré**conditions et des **post**conditions **globales**. Elles sont indiquées dans le coin supérieur droit de l'activité et sont dénotées par les mots clés **<<precondition>>** et **<<postcondition>>**.

![](/out/plant_uml/custom/activityGlobalCondition.svg)

Les **actions** peuvent avoir des **pré**conditions et des **post**conditions **locales**. Ces conditions sont indiquées à travers des notes avec les mots clés **<<localPrecondition>>** et **<<localPostcondition>>**.

![](/out/plant_uml/custom/activityLocalCondition.svg)

## Décisions et fusions

Dans un diagramme d'activités, il est possible de définir un **nœud de décision**. Ce nœud permet de choisir **un unique chemin** dans le flux d'actions en fonction d'une **condition donnée**. Il possède **une entrée** et **plusieurs sorties**.

On représente un **nœud de décision** à l'aide d'un diamant, et les conditions des chemins entre crochets. Une condition dépendante de paramètres peut aussi être représentée sous forme de note avec le mot clé **<<decisionInput>>**.

Les **nœuds de fusion** permettent à plusieurs flux de se **rejoindre en un seul et même flux**. Ils sont aussi représenté à l'aide d'un diamant.

![](/out/plant_uml/custom/activityChoice.svg)

## Bifurcation et jonction

Un **nœud de bifurcation** divise le flux courant en **plusieurs flux concurrents**. Les actions suivant un **nœud de bifurcation** s'exécutent de manière concurrente et se terminent indépendamment.  
À l'inverse, un **nœud de jonction** synchronise plusieurs flux concurrents pour atteindre **un seul flux d'exécution**.

Les **nœud de bifurcation** et de **jonction** sont représentés par une barre. On distingue les deux en regardant les flux entrants et sortants.

![](/out/plant_uml/custom/activityForkJoin.svg)

## Connecteurs

Dans les diagrammes plus complexes, il est possible d'utiliser des **connecteurs**. Ces derniers n'ajoutent pas d'actions ni d'étapes supplémentaires aux activités. Leur but est de **relier deux parties du diagramme** afin de le rendre plus lisible. Les connecteurs sont reliés par leur nom.

![](/out/plant_uml/custom/activityConnector.svg)

## Objets

Un **nœud d'objet** permet de représenter les données plus complexes. Il représente l'existence d'un objet généré par une action dans une activité, et est représenté par un rectangle.

![](/out/plant_uml/custom/activityObject.svg)

Il existe une notation alternative pour les **nœuds d'objets**. On peut les représenter sous forme de pins.

![](/out/plant_uml/custom/activityPins.svg)

Les **nœuds d'objets** peuvent aussi être utilisés pour indiquer les paramètres d'entrée et de sortie de l'activité. Pour ce faire, on positionne les rectangles sur les bords du diagramme.

![](/out/plant_uml/custom/activityObjectParameters.svg)

Les **nœuds d'objets** peuvent bénéficier des **flux d'objets** pour faire de la **séléction**.  
La **sélection** se fait à l'aide d'une note identifiée par le mot clé **<<selection>>**.

![](/out/plant_uml/custom/activitySelection.svg)

## Stockage de données

Un **nœud de stockage de données** effectue une copie de toutes les données qui le traversent. Si le même objet passe plusieurs fois par un **nœud de stockage de données**, la version précédente de l'objet sera remplacée.  
On le représente comme un **nœud d'objet** avec le mot clé **<<datastore>>**.

Dans l'exemple ci-dessous, les nouveaux utilisateurs sont ajoutés à la base de données :

![](/out/plant_uml/custom/activityData.svg)

## Couloirs

Les **couloirs** sont utilisés pour **organiser et catégoriser les actions** en fonction du **rôle** ou de la **responsabilité** de l'entité effectuant l'action.  
Les actions au sein d'un couloir sont effectuées par l'entité associée à ce couloir.  
On peut les représenter de manière horizontale ou verticale. Le nom de l'entité est indiqué au début de chaque couloir.

![](/out/plant_uml/custom/activitySwimlane.svg)

## Exemple

Voici un exemple complet d'un **diagramme d'activités** basé sur le cas d'étude [PolyAuto](../polyauto/).  
Le processus choisi correspond à la validation d'une réservation d'un véhicule du point de vue de l'application.

![](/out/plant_uml/custom/activityExemple.svg)
