---
layout: page
title: Diagrammes d'activités
permalink: /diagrammes-d-activites/
nav_order: 7
has_children: true
has_toc: false
---

# Diagrammes d'activités  
Un **diagramme d'activités** est utilisé pour modéliser et représenter visuellement le **déroulement d'un processus**. Il permet de visualiser les étapes, les actions, les décisions et les boucles d'un processus, ce qui facilite la compréhension, l'analyse et l'amélioration des activités.  
Les **diagrammes d'activités** sont utiles pour **clarifier** les responsabilités, **planifier** les projets, **documenter** les systèmes et **faciliter** la communication **entre les parties prenantes**. 

## Activités et actions
Une **activité** se réfère à un comportement qui est divisé en une ou plusieurs **actions**. Chaque **action** représente une **étape unique** (il n'est pas nécessaire de décomposer davantage l'action dans le diagramme, bien que cela ne garantisse pas que l'action soit simple ou atomique) au sein de l'activité, où des données sont manipulées ou traitées.  

Les **activités** sont généralement réutilisées plusieurs fois au sein du système, tandis que les **actions** sont plus spécifiques et utilisées uniquement au sein d'une seule activité.

## Représentation 
Une **activité** est représentée par un rectangle aux coins arrondis, avec son nom et ses paramètres associés dans le coins supérieur gauche.  
Une **action** est elle aussi représentée par un rectangle aux coins arrondis.  

Le flux au sein des activités est représenté à l'aide d'arêtes d'activités entre les **actions**. Elles sont matérialisées à l'aide de flèches. Les arêtes spécifient **comment les données circulent d'une action à la suivante**. Les actions qui ne sont pas ordonnées par des arêtes peuvent s'exécuter de manière concurrente. 

![](/out/plant_uml/custom/activityRepresentation.svg)

Les **activités** possèdent généralement un **point de départ** ainsi qu'un ou plusieurs **points d'arrivés**. Lorsqu'un point d'arrivé est atteint, l'activité prend fin. On les représente de la sorte :  

![](/out/plant_uml/custom/activityStartNode.svg)

## Préconditions et postconditions
Les activités et les actions peuvent être accompagnées de certaines **conditions**.  
Les **activités** peuvent avoir des **pré**conditions et des **post**conditions **globales**. Elles sont indiquées dans le coins supérieur droit de l'activité et sont dénotées par les mots clés **<<precondition>>** et **<<postcondition>>**.  

![](/out/plant_uml/custom/activityGlobalCondition.svg)

Les **actions** peuvent avoir des **pré**conditions et des **post**conditions **locales**. Ces conditions sont indiquées à travers des notes avec les mots clés **<<localPrecondition>>** et **<<localPostcondition>>**.

![](/out/plant_uml/custom/activityLocalCondition.svg)

## Décisions et fusions
Dans un diagramme d'activités, il est possible de définir un **nœud de décision**. Ce nœud permet de choisir **un uniduqe chemin** dans le flux d'actions en fonction d'une **condition donnée**. Il possède **une entrée** et **plusieurs sorties**.  

On représent un **nœud de décision** à l'aide d'un diamant, et les conditions des chemins entre crochets. Une condition dépendante de paramètres peut aussi être représentée sous forme de note avec le mot clé **<<decisionInput>>**.  

Les **nœuds de fusion** permettent à plusieurs flux de se **rejoindre en un seul et même flux**. Ils sont aussi représenté à l'aide d'un diamant.

![](/out/plant_uml/custom/activityChoice.svg)


## Exemple