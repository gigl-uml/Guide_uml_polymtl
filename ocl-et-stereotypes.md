---
layout: page
title: OCL et Stéréotypes
permalink: /ocl-stereotypes/
nav_order: 10
has_children: true
has_toc: false
---

# OCL et Stéréotypes

Les **stéréotypes** et **l'OCL** (_Object Constraint Language_) sont deux concepts importants de l'UML.  
Les **stéréotypes** permettent d'étendre et de personnaliser les concepts de base d'UML, tandis que **l'OCL** est un langage de contraintes utilisé pour spécifier des règles et des conditions sur les modèles UML.

## OCL

L'**OCL** (_Object Constraint Language_) est un **langage de contraintes** utilisé pour spécifier des règles et des conditions sur les modèles UML. Il permet d'exprimer des invariants, des préconditions et des postconditions pour les opérations, ainsi que d'autres types de contraintes sur les modèles UML.

OCL est un langage d'expression qui garantit qu'il n'y a pas d'effet secondaire. Il **ne peut pas modifier le modèle** et n'entraînera aucun changement d'état dans le système. Même si une expression OCL peut être utilisée pour spécifier un changement d'état, toutes les valeurs des objets, y compris les liens, restent inchangées.

Chaque contrainte OCL est **liée à un contexte spécifique**, c'est-à-dire à l'élément auquel la contrainte est attachée.  
On retrouve généralement trois types de contraintes :

- **Invariants**  
  Un invariant est une règle ou une condition qui doit toujours être vraie pour un élément spécifique d'un modèle. Les invariants sont souvent des règles qui doivent être respectées par les objets du monde réel, sur lesquels les objets logiciels sont basés.  
  Un invariant respecte la syntaxe suivante :

  > context {**classifier**}  
  > inv [{**constraint name**}]: {**Boolean OCL expression**}

  Par exemple, pour un compte gardant un solde toujours possitif, on pourrait avoir :

  > context **Compte**  
  > inv : **solde > 0**

  ou encore

  > context **Compte:solde**  
  > inv : **self.value > 0**

- **Préconditions**  
  Une précondition est une contrainte qui doit être vraie juste avant l'exécution d'une opération.  
   Une précondition respecte la syntaxe suivante :

  > context {**classifier**}::{**operation**} ({**parameters**})  
  > pre [{**constraint name**}]: {**Boolean OCL expression**}

  Par exemple, pour un retrait d'argent sur un compte, on pourrait avoir :

  > context **Compte::retirer(int montant)**  
  > pre : **solde > montant**

- **Postconditions**  
  Une postcondition est une contrainte qui doit être vraie juste après l'exécution d'une opération.  
   Une postcondition respecte la syntaxe suivante :

  Par exemple, pour un dépot d'argent sur un compte, on pourrait avoir :

  > context **Compte::déposer(int montant)**  
  > post : **solde@pre == solde - montant**

## Stéréotypes

Les **stéréotypes** permettent de définir de nouveaux concepts et d'**adapter les concepts existants** aux **besoins spécifiques** d'un domaine ou d'un système. Ils sont utilisés pour ajouter des attributs, des opérations et des contraintes aux éléments de base de l'UML tels que les classes ou les associations. Les **stéréotypes** sont représentés par des noms placés entre chevrons **(<< >>)** et peuvent être appliqués à des éléments dans les diagrammes UML.

![](/out/plant_uml/stereotypes/stereotypes.svg)
