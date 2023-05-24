---
layout: page
title: Diagrammes de classes
permalink: /diagrammes-de-classes/
nav_order: 2
---



# Diagrammes de classes
{: .no_toc }

Les diagrammes de classes sont utilisés pour :
-   Explorer les concepts d'un domaine
-   Analyser les besoins à l'aide d'un modèle conceptuel 
-   Décrire de façon détaillée une conception orienté objet


## Sommaire
{: .no_toc .text-delta }

1. TOC
{:toc}

## Classes
Une classe est le schéma de construction d'un objet. Elle décrit une collection d'objets qui
partagent les mêmes attributs, les mêmes opérations, les mêmes relations et la même sémantique.  
Elles sont représentées par des rectangles séparés en trois parties:  

1. Le nom de la classe. Il doit être unique, constitué d'une chaine de caractères, centré et la première lettre doit être en majuscule
2. Les attributs
3. Les opérations

![](/out/classexample/classexample.svg)

## Attributs
Il existe 2 notations permettant de représenter des attributs:  

1. En ligne (*inlined attributes*):  
    **visibilité / nom : type multiplicité = défaut**

    | ------------ | ----------- |
    | Visibilité   | {public: +, privé: -, protégé: #, paquet: ~} |
    | /            | La présence de ce symbole indique que la valeur de cet attribut peut être obtenue à l'aide d'autres attributs déjà dans le modèle                           |
    | Nom          | Le nom de l'attribut                          |
    | Type         | Le type de l'attribut                         |
    | Multiplicité | Le nombre d'instances de l'attribut [min..max]            |
    | Défaut       | La valeur par défaut de l'attribut            |

    ![](/out/attributesInlineExample\attributesInlineExample.svg)

2. Par relation:

    Permet de montrer plus de détails des attributs sur le diagramme  
    
    ![](/out/attributeRelationExample\attributeRelationExample.svg)  

## Opérations

## Methodes

## Classes abstraites

## Relations

## Interfaces

## Modèles
