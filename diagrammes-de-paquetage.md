---
layout: page
title: Diagrammes de paquetages
permalink: /diagrammes-de-paquetages/
nav_order: 7
has_children: true
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

# Diagrammes de paquetages

Visualiser, spécifier, construire et documenter de grands systèmes implique la manipulation d’un grand nombre de classes, interfaces, composantes, noeuds, diagrammes et autres éléments.  
Il est donc utile de regrouper les éléments communs en **paquetages** afin de pouvoir les comprendre et les
manipuler plus facilement.

## Représentation

Un simple paquetage est représenté ainsi:  
![](/out/plant_uml/singlePackagesRepresentation/singlePackagesRepresentation.svg)

Il y a deux façons de représenter le contenu des paquetages:

|                      À l'intérieur du paquetage                       |                         À l'aide d'un connecteur d'imbrication                         |
| :-------------------------------------------------------------------: | :-------------------------------------------------------------------: |
| ![](/out/plant_uml/packageReprésentation1/packageReprésentation1.svg) | ![](/out/plant_uml/packageReprésentation2/packageReprésentation2.svg) |

## Relations

| ------------ | ----------- | ----------- |
| _Imbrication (Nesting)_ | ![](/out/plant_uml/containmentRelationshipExample/containmentRelationshipExample.svg) | Indique que le paquetage A contient l'élément B (qui est généralement une classe). |
| _Import_ | ![](/out/plant_uml/importRelationshipExample/importRelationshipExample.svg) | Indique que le paquetage A importe les éléments du paquetage B. Donc, A aura accès au contenu de B. Cette relation est transitive, donc si A *<<import>>* B, alors tout paquetage qui importe A aura aussi accès aux éléments de B. |
| _Access_ | ![](/out/plant_uml/accessRelationshipExample/accessRelationshipExample.svg) | Indique que le paquetage A importe les éléments du paquetage B avec une visibilité privée. Ainsi, cette relation n'est pas transitive; si A *<<access>>* B, alors un paquetage qui importe A n'aura pas accès aux éléments de B. |  

## Importer et accéder aux paquetages

*Note: La notion d'éléments **publics** et **privés** sont détaillés dans la [section suivante](#visibilité-des-éléments/)*

Il est possible d'importer des éléments (classes) d'un paquetage à l'autre. Pour ce faire, il faut qu'un paquetage `<<import>>` un autre paquetage, ce qui lui permettra d'accéder aux classes de ce dernier. Par exemple:

![](/out/plant_uml/importRelationPackage/importRelationPackage.svg)

Dans ce cas-ci, les `Utilisateurs` pourront accéder aux classes présentes dans le paquetage `Reunions`. Tous les éléments **publics** importés peuvent être accédés indirectement, c'est-à-dire par d'autres paquetages qui importeraient `Utilisateurs`dans l'exemple ci-haut.  

Il est possible d'importer des éléments de manière **privée** avec l'annotation `<<access>>`, c'est-à-dire qu'ils ne seront accessibles que par le paquetage qui les importe directement. Par exemple:

![](/out/plant_uml/accessRelationPackage/accessRelationPackage.svg) 


## Visibilité des éléments

Les éléments d'un paquetage peuvent être **publics** ou **privés**.  

![](/out/plant_uml/packageVisibility/packageVisibility.svg)

Visibilité **publique (+)**: indique que cet élément est utilisable en dehors du paquetage. Dans l'exemple, le paquetage **Utilisateurs** peut accéder à la classe **Réunion** du paquetage **Réunions**.  

Visibilité **privée (-)**: indique que seulement les autres éléments du même paquetage peuvent utiliser l'élément privé. Dans l'exemple, le paquetage **Utilisateurs** n'a pas accées à l'élément **Participants** du paquetage **Réunions**.  


<!-- ## Fusionner les paquetages

L'UML offre la possibilité de fusionner des paquetages. Ce mécanisme plutôt complexe est rarement utilisé en industrie.  
Vous pouvez trouver plus de détails sur ce sujet dans la section **3.4. Merging Packages** du livre **UML 2.0 in a Nutshell** de Pilone et Pitman. -->

*Les sections suivantes ne font pas partie de la norme UML, mais illustrent des exemples de leur utilisation dans la représentation d'architectures logicielles.*  

## Architecture Multiniveaux

Une architecture classique pour la conception d’applications comprenant une interface usager 
et des services techniques, dont un système de sauvegarde des données, est l’**architecture multiniveaux**. Voici un sommaire des couches généralement retrouvées dans ce type d'architecture:  
1. **Présentation** :  représente les composantes de l'interface utilisateur.
2. **Logique d’application** : représente les objets clés et les services de l'application. Elle est souvent décomposée en couches plus minces organisées autour de classes. Par exemple, les classes Services d'une application peuvent être sub-divisés ainsi (voir la section [Exemples](#exemple) ci-bas pour un diagramme d'architecture multiniveaux complet):
- Haut niveau: génération de réunions, envoi des invitations, algorithmes de calcul
- Bas niveau: gestion de fichiers, communication avec des tiers partis.
3. **Services techniques** : représente, entre autres, les systèmes où sont stockées les données utilisées par l'application (base de données, *logging* des métadonnées), les tiers partis avec lesquels communiquent l'application et le moteur de régles.

**Visibilité entre les paquetages**  
- Accès aux paquetages de **présentation**: Aucun autre paquetage n’a un accès direct aux entités de la couche de présentation.  
- Accès aux paquetages de la **logique d'application**: Les paquetages de la présentation et certains autres paquetages de la logique d'application peuvent accéder aux paquetages de cette couche.  
- Accès aux paquetages du **système de sauvegarde**: Les paquetages de la logique d'application peuvent accéder aux éléments de la persistance. À noter que les paquetages de la présentation n'accèdent généralement jamais directement au système de sauvegarde.  

## Architecture MVC  

Le principe de l'**architecture MVC** est de séparer les classes de la Présentation des autres paquetages du système. Normalement, les éléments de la Présentation sont uniques à l’application alors que les classes de la logique d'application pourraient être réutilisées dans d’autres projets.  

- **Modèle (M)**: Gère l’état et les comportements logiques du  modèle.
- **Vue (V)**: Visualisation du modèle et capture des évènements externe (eg. venant des utilisateurs), ne contient aucun donnée ou fonctionnalité.
- **Contrôleur (C)**: Synchronise le **Modèle** aux changements venant de la **Vue**. Il ne contient aucune donnée.  

**Visibilité entre les paquetages**  
- La **Vue** déclenche des évènements et les envoie au **Contrôleur**.
- La seule responsabilité du **Contrôleur** est de rediriger les évènements venant de la **Vue** aux objets dans le **Modèle** pour le mettre à jour.
- Le **Modèle** Met à jour *indirectement* la **Vue** par un patron de conception (aucune interaction *directe*).  

La section [Exemples](#exemple) ci-bas comporte un diagramme de paquetage représentant l'architecture MVC d'une application.

## Exemples

Voici un exemple complet d'un **diagramme de paquetages** utilisant l'architecture **multiniveaux** et basé sur le cas d'étude [PolyCal](../polycal/).

![Architecture multiniveaux](/assets/images/paquetages.png)

Voici un exemple complet d'un **diagramme de paquetages** utilisant l'architecture **MVC** et basé sur le cas d'étude [PolyCal](../polycal/).

![Architecture MVC](/assets/images/paquetages_mvc.png)

<!-- Voici un exemple complet d'un **diagramme de paquetages** basé sur le cas d'étude [PolyAuto](../polyauto/).

![](/out/plant_uml/exempleDiagPaquet/exempleDiagPaquet.svg) -->
