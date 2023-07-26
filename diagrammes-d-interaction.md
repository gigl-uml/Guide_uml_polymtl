---
layout: page
title: Diagrammes d'interaction
permalink: /diagrammes-d-interaction/
nav_order: 8
has_children: true
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

# Diagrammes d'interaction

Un diagramme d'interaction fournissent une représentation visuelle claire des **messages échangés** entre les différents acteurs, objets ou composants d'un système pendant un **scénario spécifique**.

Deux types principaux de diagrammes d'interactions sont couramment utilisés : les diagrammes de séquence et les diagrammes de communication.

Le diagramme de séquence met en évidence **l'ordre chronologique** des messages échangés entre les différents objets d'un système.

Le diagramme de communication met davantage l'accent sur le **flux des messages échangés** entre les objets que sur leur ordre chronologique.

La section suivante comporte une comparaison des 2 types de diagramme, mais nous nous concentrerons sur les diagrammes de séquence dans le reste du chapitre.

## Représentation

Un diagramme de séquence doit montrer des messages échangés par des participants lors de la réalisation d'un scénario.
L'exemple suivant représente les **messages échangés**, lors d'une **requête HTTP** (scénario), entre le **participant Navigateur** et le **participant Serveur**.

![](/out/plant_uml/custom/interactionRepresentationExample.svg)

Voici le même scénario sous forme de diagramme de communication.

![](/out/plant_uml/custom/communicationRepresentationExample.svg)

## Participants aux interactions

Les participants aux interactions d'un diagramme de séquence sont représentés à l'aide d'un rectangle et d'une ligne verticale pointillée, appelée « ligne de vie ». Le nom du participant suit cette syntaxe:

**nom_de_l'objet [sélecteur] : nom_de_la_classe**

| ------------ | ----------- |
| nom_de_l'objet | Le nom de l'instance impliqué dans l'intéraction |
| sélecteur | Permet de selectionner une instance particulière dans un tableau d'élement |
| nom_de_la_classe | Le nom du type du participant |

## Message

Les messages sont des flèches représentant des communications entre participants. Le texte juste au-dessus de la flèche d'un message représente un appel de méthode, le nom ou la description du message échangé entre les participants.

|---|---|
| Message asynchrone | ![](/out/plant_uml/asyncMessageExample/asyncMessageExample.svg) | Représenté à l'aide d'une pointe de flèche ouverte. |
| Message synchrone | ![](/out/plant_uml/syncMessageExample/syncMessageExample.svg) | Représenté à l'aide d'une pointe de flèche remplie. |
| Message de Réponse | ![](/out/plant_uml/responseMessageExample/responseMessageExample.svg) | Représenté à l'aide d'une flèche pointillée et d'une pointe ouverte.|
| Message de création | ![](/out/plant_uml/createMessageExample/createMessageExample.svg) | Représenté à l'aide d'une flèche pointillée et d'une pointe ouverte et d'une fonction de création ou de l'étiquette <<create>>. |
| Message de destruction | ![](/out/plant_uml/destroyMessageExample/destroyMessageExample.svg) | Représenté à l'aide d'une pointe pleine et d'une fonction de destruction ou de l'étiquette <<destroy>>. On utilise une croix pour montré le moment où l'objet sera détruit. |
| Message perdu | ![](/out/plant_uml/custom/lostMessageExample.svg) | Représenté à l'aide d'une flèche pointant vers un cercle plein. Montre que le participant P1 envoie un message dont la destination est inconnue ou pas importante dans la séquence. |
| Message trouvé | ![](/out/plant_uml/custom/foundMessageExample.svg) | Représenté à l'aide d'une flèche partant d'un cercle plein. Montre que le participant P1 a reçu un message dont la provenance est inconnue ou pas importante dans la séquence. |

## Occurrence d'exécution

Il est possible de représenter le temps de traitement ou l'attente d'un message par un participant à l'aide d'une occurrence d'exécution. Celles-ci sont illustrées par un rectangle vertical sur la ligne de vie.

![](/out/plant_uml/execOccurence/execOccurence.svg)

## Invariants d'état

Les invariants d'états représente des conditions qui doivent rester vraies pour le reste des interactions du scénario. Chaque invariant est attaché à la ligne de vie pour laquelle la condition s'applique.  
Voici un exemple avec 2 invariants d'états dans un scénario de retrait d'argent.

![](/out/plant_uml/custom/stateInvariantsExample.svg)

## Opérateur d'interaction

Un opérateur d'interaction est un élément utilisé dans les diagrammes de séquence pour spécifier le comportement et la structure des interactions entre les objets. Il permet de définir des scénarios d'exécution plus complexes en déterminant comment les messages sont échangés.

|---|---|---|
| _Alternates_ | ![](/out/plant_uml/altOperatorExample/altOperatorExample.svg) | Représente différentes branches d'exécution, chaque branche étant associée à une condition qui détermine si cette branche est exécutée ou non. |
| _Option_ | ![](/out/plant_uml/optOperatorExample/optOperatorExample.svg) | Similaire à alt, mais avec une seul opérande |
| _Break_ | ![](/out/plant_uml/breakOperatorExample/breakOperatorExample.svg) | Indique une interruption du scénario, après l'exécution du fragment, si la condition est vraie. Par exemple, si P1.attr == True, alors message3() sera envoyé, mais pas message4(). |
| _Parallel_ | ![](/out/plant_uml/parOperatorExample/parOperatorExample.svg) | Indique que les 2 fragments d'interactions peuvent s'exécuter en parallèle, en gardant l'ordre des fragments originaux. Par exemple, message2() et message3() doivent être exécutés après message1(). |
| _Loop_ | ![](/out/plant_uml/loopOperatorExample/loopOperatorExample.svg) | Indique que le fragment d'interactions sera exécuté en boucle. La condition de sortie peut être représentée avec une condition de sortie ou comme ceci: loop(min, max). |
| _ref_ | ![](/out/plant_uml/refOperatorExample/refOperatorExample.svg) | Réfère à une interaction définie dans un autre diagram |

## Exemple

Voici un exemple d'un **diagramme d'interaction** basé sur le cas d'étude [PolyAuto](../polyauto/).

![](/out/plant_uml/custom/interactionGlobalExample.svg)
