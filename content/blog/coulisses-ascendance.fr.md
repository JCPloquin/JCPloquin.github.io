---
title: "Behind the scenes : Création d'Ascendance"
date: 2025-07-05T15:00:00+02:00
slug: "behind-the-scenes-creation-dascendance"
draft: false
categories: ["Musique", "Développement", "Création"]
tags: ["ascendance", "behind the scenes", "composition", "développement", "généalogie"]
description: "Plongez dans les coulisses de la création d'Ascendance : de l'idée initiale aux défis techniques, découvrez le processus créatif derrière cette œuvre acousmatique interactive."
---

Trois semaines après le lancement d'*Ascendance*, il est temps de lever le voile sur les coulisses de cette création. Comment transforme-t-on une idée artistique en œuvre interactive ? Retour sur un processus créatif qui mêle composition électroacoustique et développement logiciel.

## L'étincelle créative : quand la généalogie rencontre l'acousmatique

L'idée d'*Ascendance* est née d'une observation simple : **nos arbres généalogiques ressemblent à des partitions**. Chaque branche évoque une ligne mélodique, chaque génération suggère une tessiture, chaque ancêtre porte en lui une histoire sonore unique.

Cette révélation s'est imposée lors d'une exploration de mes propres archives familiales. En contemplant les dates de naissance et de décès de mes ancêtres, j'entendais déjà résonner les cloches, les chœurs et les trompettes qui allaient devenir les objets sonores fondamentaux de l'œuvre.

## Le défi technique : faire dialoguer GEDCOM et audio

**Premier obstacle majeur :** comment faire "parler" un fichier GEDCOM ? Ces fichiers de généalogie contiennent une mine d'informations, mais dans un format purement textuel. Il fallait créer un **parseur** capable d'extraire les données pertinentes et de les transformer en paramètres musicaux.

### Qu'est-ce qu'un parseur ?

Un **parseur** (de l'anglais "parser") est un programme informatique qui analyse une chaîne de caractères et la décompose en éléments compréhensibles par la machine. Étymologiquement, le terme vient du latin "pars" (partie) : le parseur identifie les différentes parties d'un texte selon des règles précises.

Dans le contexte d'*Ascendance*, mon parseur GEDCOM doit :
- **Identifier** chaque individu dans l'arbre généalogique
- **Extraire** ses dates de naissance et de décès
- **Comprendre** les liens de parenté
- **Convertir** ces informations en coordonnées spatiales et temporelles pour la composition

### Le parallèle avec Xenakis et la musique stochastique

Cette approche rappelle les travaux révolutionnaires d'Iannis Xenakis dans les années 1950. Le compositeur grec utilisait les **mathématiques stochastiques** - basées sur le calcul des probabilités - pour transformer des données abstraites en matériau musical concret.

**Xenakis transformait :**
- Les **lois de la physique** (cinétique des gaz, chaînes de Markov) en **règles compositionnelles**
- Les **phénomènes naturels** (chant des cigales, manifestations de foule) en **masses sonores**
- Les **équations probabilistes** en **événements musicaux**

**Dans Ascendance, je transforme :**
- Les **données généalogiques** en **objets sonores spatialisés**
- Les **liens familiaux** en **relations harmoniques**
- Les **dates historiques** en **progressions temporelles**

Comme Xenakis qui "parsait" les phénomènes naturels pour en extraire des lois compositionnelles, mon parseur GEDCOM extrait la structure musicale cachée dans nos histoires familiales.

## L'architecture sonore : trois univers, trois esthétiques

*Ascendance* se structure en trois mouvements distincts, chacun nécessitant une approche compositionnelle spécifique :

### Le Préchauffage : voyage dans l'histoire musicale

**Défi artistique :** Comment représenter le passage du temps historique par la musique ? J'ai choisi de superposer des échantillons d'époques différentes - Pierre Henry, Léo Delibes, chant grégorien, musique antique - dans un ordre aléatoire. Cette cacophonie contrôlée prépare l'auditeur au voyage temporel qui l'attend.

### Le Voyage aller : chaque ancêtre, une signature sonore

**Innovation technique :** Chaque ancêtre génère automatiquement trois objets sonores symboliques. Les dates de naissance déclenchent des trompettes, les périodes de vie activent des chœurs, les dates de décès font résonner des cloches. La spatialisation quadriphonique permet de ne percevoir que les ancêtres "proches" dans l'arbre.

### Le Voyage retour : l'avalanche temporelle

**Choix esthétique radical :** Abandonner la mélodie individuelle pour une texture globale descendante. Cette "avalanche chromatique" symbolise la cascade des générations, créant un effet dramatique saisissant.

## Les défis de la spatialisation interactive

**Problème complexe :** Comment naviguer dans un espace sonore trop vaste pour être appréhendé globalement ? La solution résidait dans la création d'un "horizon sonore" - seuls les ancêtres dans un rayon de 4 générations restent audibles.

Cette limitation technique devient un choix artistique : elle mime notre perception naturelle de l'histoire familiale, où seuls les ancêtres "proches" nous sont vraiment accessibles.

## L'évolution harmonique : le comma comme guide temporel

**Découverte compositionnelle :** Plutôt qu'une progression par demi-tons (trop brutale), j'ai opté pour une montée par commas (neuvième de ton). Ce micro-intervalle crée une progression harmonique subtile qui accompagne l'exploration généalogique sans la dominer.

Chaque génération remontée élève légèrement la hauteur générale, créant une sensation d'élévation spirituelle vers les origines.

## Les outils de création : entre tradition et innovation

**Palette logicielle :**
- **Ardour** : Séquenceur principal pour l'assemblage et le mixage multicanal
- **Pure Data** : Programmation des algorithmes musicaux et traitement temps réel
- **Godot Engine** : Moteur de jeu pour l'interactivité et l'interface
- **Bibliothèques audio personnalisées** : Objets sonores composés spécifiquement pour le projet
- **Scripts de parsing GEDCOM** : Développés sur mesure pour l'analyse généalogique

**Pure Data** joue un rôle central dans mes créations. Ce langage de programmation visuelle me permet de développer les algorithmes musicaux complexes qui transforment les données généalogiques en objets sonores. Chaque ancêtre, chaque date, chaque lien familial passe par des patches Pure Data qui calculent en temps réel les paramètres de spatialisation, de hauteur et de timbre.

## Les retours d'expérience : quand l'art rencontre son public

Depuis le lancement, les retours révèlent des usages inattendus. Certains utilisateurs explorent *Ascendance* comme outil de méditation familiale, d'autres y trouvent une nouvelle façon d'appréhender leur héritage. Cette diversité d'approches confirme la richesse du medium interactif.

**Témoignages marquants :**
- "J'ai enfin 'entendu' mon arrière-grand-père"
- "Une expérience bouleversante qui donne une dimension sonore à ma généalogie"
- "Plus qu'un jeu, c'est un voyage intérieur"

## Vers de nouveaux horizons créatifs

*Ascendance* ouvre la voie à d'autres expérimentations. L'idée d'adapter cette approche à d'autres types de données - géographiques, historiques, scientifiques - germe déjà. Le principe reste le même : transformer l'information en expérience artistique immersive.

## Les leçons apprises

**Sur le plan artistique :** L'interactivité ne doit jamais dominer la dimension esthétique. Chaque choix technique doit servir l'intention musicale.

**Sur le plan technique :** La simplicité d'usage cache souvent une complexité de développement. Trois clics pour charger un GEDCOM représentent des centaines d'heures de programmation.

**Sur le plan humain :** L'art interactif crée des liens uniques entre créateur et public. Chaque utilisateur devient co-créateur de sa propre expérience.

*Ascendance* démontre qu'il est possible de repenser les frontières entre composition, programmation et expérience utilisateur. Cette œuvre hybride ouvre de nouvelles perspectives pour l'art sonore du XXIe siècle, dans la lignée des innovations de Xenakis qui transformait déjà les mathématiques en musique.

---

*Découvrez Ascendance gratuitement sur [jcploquin.itch.io/ascendance](https://jcploquin.itch.io/ascendance) et explorez votre propre voyage généalogique musical.*

