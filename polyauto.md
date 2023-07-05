---
layout: page
title: PolyAuto (cas d'étude)
permalink: /polyauto/
nav_order: 11
has_children: false
has_toc: false
---

# PolyAuto

Ce guide UML vous fournit des exemples récapitulatifs pour chaque diagramme.  
Ces derniers se basent sur un même et unique cas d'étude : **PolyAuto**.  
Afin de mieux comprendre les exemples, nous vous invitons à prendre conscience des spécifications ci-dessous.

---

## Contexte

**PolyAuto** est un _système de réservation de véhicules en libre-service (voitures, scooters, vélos et trottinettes)_ conçu spécialement pour les étudiants et le personnel de l'école Polytechnique, et plus généralement pour toute l'Université de Montréal. Son objectif est de fournir une solution pratique et flexible pour répondre aux besoins de déplacement sur le campus et dans les environs. **PolyAuto** permettra aux utilisateurs de _réserver, déverrouiller et utiliser_ facilement des véhicules à travers une application mobile intuitive, facilitant ainsi leur mobilité quotidienne.

Le but de **PolyAuto** est de _simplifier les déplacements des étudiants et du personnel_ de l'école Polytechnique en mettant à leur disposition un service de réservation de véhicules en libre-service. Le système vise à offrir une alternative pratique aux transports en commun, en permettant aux utilisateurs de réserver un véhicule selon leurs besoins, de le déverrouiller facilement via l'application mobile et de l'utiliser pour leurs déplacements personnels.

Certains véhicules disponibles sur **PolyAuto** nécessitent un permis de conduire. Pour utiliser ces derniers, l'usager doit _fournir une preuve_ qu'il détient un permis de conduire valide et une assurance. Si l'usager est un résident du Québec, il doit fournir son numéro de permis de conduire, qui sera alors validé électroniquement par le système auprès de la Société de l'assurance automobile du Québec (SAAQ). Si l'usager n'est pas résident du Québec ou s'il possède un permis de conduire étranger, il doit transmettre une copie de son permis de conduire étranger.

Pour faciliter l'utilisation de **PolyAuto**, la facturation est effectuée automatiquement grâce au matricule de l'utilisateur.

## Fonctionnalités

- **Réservation de véhicules** : Les utilisateurs pourront consulter la disponibilité des véhicules et réserver un véhicule spécifique pour une période donnée.
- **Déverrouillage des véhicules** : Une fois la réservation confirmée, les utilisateurs pourront utiliser l'application mobile pour déverrouiller le véhicule réservé en toute simplicité.
- **Gestion des réservations** : Le système permettra aux utilisateurs de gérer leurs réservations, d'effectuer des modifications ou des annulations si nécessaire.
- **Localisation des véhicules** : Les utilisateurs pourront localiser les véhicules disponibles à proximité grâce à une fonction de géolocalisation intégrée à l'application.
- **Facturation et paiement** : Le système prendra en charge la facturation automatique des utilisateurs en fonction de la durée d'utilisation des véhicules.
