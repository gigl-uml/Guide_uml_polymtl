---
layout: page
title: OCL et Stéréotypes
permalink: /ocl-stereotypes/
nav_order: 10
has_children: true
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

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

  > context {**classifier**}::{**operation**} ({**parameters**})  
  > post [{**constraint name**}]: {**Boolean OCL expression**}

  Par exemple, pour un dépot d'argent sur un compte, on pourrait avoir :

  > context **Compte::déposer(int montant)**  
  > post : **solde@pre == solde - montant**

## Stéréotypes

Les **stéréotypes** permettent de définir de nouveaux concepts et d'**adapter les concepts existants** aux **besoins spécifiques** d'un domaine ou d'un système. Ils sont utilisés pour ajouter des attributs, des opérations et des contraintes aux éléments de base de l'UML tels que les classes ou les associations. Les **stéréotypes** sont représentés par des noms placés entre chevrons **(<< >>)** et peuvent être appliqués à des éléments dans les diagrammes UML.

Il est important de ne pas confondre les **stéréotypes** les **classificateurs**. Tout ce qui est entre chevrons n'est pas forcément un stéréotype.  
En **UML**, les **classificateurs** sont des entités abstraites qui regroupent des objets similaires, quel que soit leur type (classe, interface, composant, etc.), pour faciliter la modélisation et la compréhension du système.  
Nous avons par exemple vu les classificateurs **<<device>>** et **<<interface>>**.

L'UML fournit un ensemble standard de stéréotypes :

| Stereotype            | Élément du modèle | Description                                                                                                                                                                |
| --------------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| «auxiliary»           | Classe            | Ce stéréotype est appliqué à une classe qui soutient une autre classe, généralement en fournissant des mécanismes de contrôle. La classe soutenue est une classe centrale. |
| «buildComponent»      | Composant         | Ce stéréotype est appliqué à un composant qui spécifie un ensemble de composants pour le développement organisationnel ou au niveau du système.                            |
| «create»              | Opération         | Ce stéréotype est appliqué à une opération qui crée une instance du classifieur ; par exemple, si l'opération est un constructeur.                                         |
| «destroy»             | Opération         | Ce stéréotype est appliqué à une opération qui détruit une instance du classifieur.                                                                                        |
| «document»            | Artéfact          | Ce stéréotype est appliqué à un artefact qui représente un document.                                                                                                       |
| «entity»              | Composant         | Ce stéréotype est appliqué à un composant qui représente un concept métier.                                                                                                |
| «executable»          | Artéfact          | Ce stéréotype est appliqué à un artefact qui peut être exécuté sur un nœud.                                                                                                |
| «file»                | Artéfact          | Ce stéréotype est appliqué à un artefact qui contient du code source ou des données.                                                                                       |
| «focus»               | Classe            | Ce stéréotype est appliqué à une classe qui spécifie la logique centrale ou le contrôle avec des classes auxiliaires fournissant des mécanismes subordonnés.               |
| «framework»           | Package           | Ce stéréotype est appliqué à un package qui contient des éléments réutilisables tels que des classes, des modèles et des patrons.                                          |
| «implement»           | Composant         | Ce stéréotype est appliqué à un composant qui n'a pas de spécification et est une implémentation d'une spécification dont il dépend.                                       |
| «implementationClass» | Classe            | Ce stéréotype est appliqué à une implémentation d'une classe où l'instance de la classe ne peut pas avoir plus d'une classe.                                               |
| «library»             | Artéfact          | Ce stéréotype est appliqué à un artefact qui est un fichier de bibliothèque statique ou dynamique.                                                                         |
| «metaclass»           | Classe            | Ce stéréotype est appliqué à une classe dont les instances sont d'autres classes qui sont conformes à la métaclass.                                                        |
| «metamodel»           | Modèle            | Ce stéréotype est appliqué à un package qui contient un modèle qui est une abstraction d'un autre modèle.                                                                  |
| «modelLibrary»        | Package           | Ce stéréotype est appliqué à un package qui contient des éléments de modèle réutilisables.                                                                                 |
| «perspective»         | Package           | Ce stéréotype est appliqué à un package qui ne contient que des diagrammes ou des sous-packages. Les extracteurs ignorent les packages qui ont ce stéréotype appliqué.     |
| «process»             | Composant         | Ce stéréotype est appliqué à un composant qui est basé sur des transactions.                                                                                               |
| «realization»         | Classificateur    | Ce stéréotype est appliqué à un classificateur qui spécifie le domaine des objets et leur implémentation.                                                                  |
| «responsibility»      | Note, Texte       | Ce stéréotype est appliqué à une note qui décrit l'obligation d'un élément du modèle envers d'autres éléments du modèle.                                                   |
| «script»              | Artéfact          | Ce stéréotype est appliqué à un fichier pouvant être interprété par un système informatique.                                                                               |
| «service»             | Composant         | Ce stéréotype est appliqué à un composant qui calcule une valeur. Ce composant n'a pas d'état.                                                                             |
| «source»              | Artéfact          | Ce stéréotype est appliqué à un fichier source d'un fichier exécutable.                                                                                                    |
| «specification»       | Classificateur    | Ce stéréotype est appliqué à un classificateur qui spécifie le domaine des objets, mais pas leur implémentation.                                                           |
| «subsystem»           | Composant         | Ce stéréotype est appliqué à un composant qui fait partie d'un système plus large.                                                                                         |
| «systemModel»         | Modèle            | Ce stéréotype est appliqué à un modèle ou un package qui contient les modèles décrivant les différentes perspectives d'un système.                                         |
| «type»                | Classe            | Ce stéréotype est appliqué à une classe qui décrit le domaine des objets et leurs opérations, sans définir l'implémentation des objets.                                    |
| «utility»             | Classe            | Ce stéréotype est appliqué à une classe qui n'a pas d'instances, mais dont les attributs et opérations ont une portée de classe.                                           |
