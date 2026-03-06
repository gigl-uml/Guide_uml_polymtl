---
layout: page
title: PolyCal (cas d'étude)
permalink: /polyauto/
nav_order: 2
has_children: false
has_toc: false
---

[↑](./#top){: .btn .btn-outline .back-to-top }

# PolyCal

Voici une mise en contexte qui sera réutilisée dans plusieurs les diagrammes. 

L’objectif général de PolyCal est de faciliter l’organisation de réunions, notamment en 
mettant à contribution les possibilités offertes par l’intelligence artificielle.
Les principales fonctionnalités offertes par PolyCal seront comme suit : 
1. **Création de demandes de réunion** : PolyCal permettra à un organisateur de créer 
des demandes de réunion et de spécifier, en langage naturel, la période 
approximative de tenue de la réunion, les personnes invitées à y participer, ainsi 
que la présence obligatoire ou non de chacune. 
2. **Qualification des plages** : Au moyen d’un algorithme d’apprentissage automatique, 
PolyCal proposera un ensemble de plages possibles pour une réunion, puis 
calculera automatiquement pour chaque plage et pour chaque personne un « fit 
score » sur une échelle de 1 à 5.  Ce score sera basé sur les disponibilités 
spécifiques, mais aussi les contraintes et préférences générales de chaque 
personne. 
3. **Gestion des comptes utilisateurs** : Toute personne possédant une adresse courriel 
pourra créer un compte utilisateur, lequel sera requis pour utiliser PolyCal.  Chaque 
utilisateur pourra, à sa guise, se connecter à son compte utilisateur et se 
déconnecter. Chaque compte utilisateur sera associé à un dossier qui contiendra : 
a. Le nom complet, l’adresse courriel et le numéro de téléphone cellulaire de 
la personne; 
b. Une liste de contraintes et préférences générales affectant la disponibilité 
de cet utilisateur, sous forme de règles en langage naturel (par exemple : 
« jamais disponible avant 8h30 », « disponible si nécessaire seulement entre 
8h30 et 9h30 », « préférence pour le mercredi à 15h30 », etc.); 
4. **Participation à la réunion** : L'organisateur et les participants doivent pouvoir 
échanger à l'oral et par messages. Ils ont l'option d'ouvrir leur caméra et de 
partager des fichiers.


## Diagrammes reliés

Tout au long de ce guide vous sont fournis des exemples basés sur le cas **PolyCal**. Il est toutefois important de noter que certains de ces exemples ne présentent **qu'une sous-partie** du système.

- [Diagramme de contexte](../diagrammes-de-contexte)
- [Diagramme de cas d'utilisation](../diagrammes-de-cas-dutilisation/#exemple) 
- [Diagramme de classes](../diagrammes-de-classes/#exemple) 
- [Diagramme de paquetages](../diagrammes-de-paquetages/#exemple)
- [Diagramme d'interaction](../diagrammes-d-interaction/#exemple)