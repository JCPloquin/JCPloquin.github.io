---
title: "HarpEK : L'instrument de geste continu arrive à maturité"
date: 2025-12-21T14:45:00+01:00
slug: "harpek-avancees-conception"
draft: false
categories: ["Musique", "Technologie", "Lutherie numérique"]
tags: ["HarpEK", "ESP32", "Pure Data", "instrument électronique", "OSC", "capteurs", "lutherie", "expérimental"]
description: "État des lieux du projet HarpEK : plateforme ESP32, harpe ultrason, pédales et encodeurs validés. Un instrument de contrôle gestuel continu pour dépasser les limites du MIDI."
image: "/img/harpek_projet.jpg"
---

# HarpEK : L'instrument de geste continu arrive à maturité

Après des mois de conception, de tests et d'ajustements, **HarpEK** franchit une étape décisive : presque tout le matériel critique est validé et documenté. L'instrument prend forme, et avec lui, une vision renouvelée du contrôle gestuel en musique électronique.

![HarpEK - Vue d'ensemble du boîtier](/img/harpek_projet.png)
*Modélisation 3D du boîtier HarpEK avec capteurs ultrason, encodeurs et joystick*

---

## 🎛️ Architecture matérielle validée

### Plateforme et alimentation

Le cœur du système repose sur un **ESP32-S3 DevKitC** pleinement opérationnel :
- Programmation via Arduino IDE stable
- Communication USB série à 115200 bps
- Protocole OSC-Serial vers Pure Data fonctionnel

L'alimentation 5V / 3,3V a été validée avec précision :
- Adaptateur 5V 3A
- Régulateur AMS1117-3.3V
- Tensions mesurées : **5,02V** et **3,28V**
- GND commun propre, sans bruit parasite

Interrupteur général, bornier d'alimentation et connecteur **USB-C panel-mount Chenyang** ont tous été testés et validés mécaniquement et électriquement.

---

## 🎵 Capteurs et contrôleurs : le corps au centre du jeu

### Harpe ultrason (3 × HC-SR04)

Le dispositif phare de HarpEK : **trois capteurs ultrason espacés de 80 mm** créent une zone de détection gestuelle continue.

**Performance mesurée** :
- Algorithme **Winner-Takes-All** stable
- **99% de détections correctes**
- Latence ≈ **60 ms**
- Portée utile : **5–177 cm**
- Mapping distance → pitch déjà exploitable musicalement

Chaque capteur dispose de sa **LED dédiée** (GPIO 45/46/47) pour un feedback visuel immédiat.

### Pédales d'expression (4 × Roland DP-10)

Brochage TRS et alimentation 5V mesurés avec précision. Diviseurs de tension **1kΩ / 2kΩ** convertissent les signaux 0–5V en plage ADC utilisable (≈0–3,3V), soit **0–2800 en résolution 12 bits**.

**Aucune diaphonie** entre les 4 pédales : chaque canal reste propre et stable.

### Encodeurs rotatifs (3 × KY-040)

Testés simultanément en mode circulaire **0–127 avec wrap-around**. Les boutons intégrés (SW) sont fiables, aucun problème de rebond ni de diaphonie.

### Joystick arcade (D400X-R4)

Version fonctionnelle validée : **3 axes analogiques** (0–4095) + bouton central. Intégration via diviseurs identiques aux pédales.

---

## 🧠 Interface mémoires et feedback

### Système de mémoires (4 boutons Gebildet 12 mm)

Câblage sur Eurocard terminé et testé. Schéma logique séparant **boutons et LEDs**, gestion firmware prévue avec sélection **exclusive d'une seule mémoire active** à la fois.

Chaque mémoire pourra stocker une configuration complète de mappings, gammes ou presets Pure Data.

---

## 🔧 Architecture électronique et mécanique

![Architecture interne HarpEK](/img/harpek_projet2.png)
*Vue éclatée : Eurocard, ESP32, connecteurs et câblage interne*

### Eurocard 100×80 mm

Carte principale achevée avec qualité professionnelle :
- Headers ESP32 soudés
- Bornier d'alimentation fixé
- Diviseurs de tension installés
- Inspection à la loupe : continuités vérifiées, **aucun court-circuit**

### Tableau de connexions complet

**85 connexions GPIO documentées** dans un tableur LibreOffice. Chaque signal, masse et alimentation a été vérifié en croisé. Aucune incohérence restante.

![Tableau de connexions ESP32-S3](/img/tableau-connexions-harpek.png)
*Tableau exhaustif des 85 connexions GPIO de l'ESP32-S3*

### Boîtier Hammond 1455N1602

Modélisation 3D complète sous **SketchUp**. Gabarits A4 pour les 4 faces validés :
- HC-SR04 affleurants (face avant)
- Encodeurs, joystick, boutons mémoire (face supérieure)
- Jacks TRS pédales, USB-C, interrupteur (face arrière)
- Clearances internes vérifiées : aucun conflit mécanique

---

## 💡 Philosophie instrumentale : le geste continu

HarpEK n'est pas un simple contrôleur MIDI. C'est un **instrument pensé pour le geste continu**, une réponse aux limites des protocoles traditionnels.

### Au-delà du MIDI

Le protocole **OSC-like sur USB série** permet d'exploiter toute la résolution **12 bits** des capteurs, sans la contrainte des 7 bits du MIDI. Le langage de l'instrument devient un alphabet personnel, mappé dans Pure Data en :
- Gammes microtonales
- Espaces spectraux
- Structures rythmiques non métriques
- Spatialisation 5.1 et 8.1

### Un héritage des années 1980

HarpEK s'inspire des **joysticks analogiques** et de la **synthèse modulaire** : le musicien modèle des flux continus plutôt que d'empiler des notes isolées. Avec la harpe ultrason, les pédales, le joystick et les encodeurs, **le corps redevient central** : chaque déplacement de main ou de pied devient une trajectoire sonore.

### Immédiateté instrumentale

L'objectif : que le musicien pense en **geste et en timbre**, pas en "paramètres" ou en "messages". HarpEK prolonge une tradition instrumentale jusque dans l'informatique musicale de 2025.

---

## 🚀 Prochaines étapes

Avec toutes les briques techniques majeures validées, les prochaines phases sont :
1. **Assemblage final** dans le boîtier Hammond
2. **Calibration complète** des capteurs en situation réelle
3. **Développement firmware** : gestion des mémoires et optimisation latence
4. **Patches Pure Data dédiés** pour premiers tests musicaux
5. **Documentation utilisateur** et premiers concerts tests

HarpEK approche de sa forme définitive. L'instrument est presque prêt à jouer.

---

🎸 *Projet open hardware — Conçu et documenté pour la communauté des musiques expérimentales.*

