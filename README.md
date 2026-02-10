
# 🌍 Smart Container Area — Système de Tri Intelligent

> **Un écosystème IoT complet associant IA, Infrastructure Dockerisée, Application Mobile et Site Web.**

## 📖 À propos du projet

**Smart Container Area** est une solution de **Smart City** conçue pour automatiser et fiabiliser le tri sélectif. Grâce à une IA de reconnaissance visuelle, le système identifie la nature du déchet et commande l'ouverture mécanique du bac approprié. Toutes les données sont centralisées pour offrir un suivi précis aux usagers et aux gestionnaires via des interfaces connectées.

## 📦 Les Maquettes

Le projet s'appuie sur deux supports physiques pour les tests et la démonstration :

* **Maquette Prototype (Réalisation d'équipe)** : Trois poubelles en carton, peintes à la main selon les codes couleurs officiels (**Jaune, Bleu, Vert**) pour une ergonomie optimale.
* **Maquette Structurelle (Support fourni)** : Trois poubelles réalisées en **impression 3D**. Cette maquette présente des couleurs neutres (Vert et Gris) imposées par le matériel d'impression d'origine.

## 👥 L'Équipe et Répartition des Rôles

Le projet est le fruit d'une collaboration entre quatre pôles d'expertise :

* **🌐 Site Web (Chaïma)** : Développement de l'interface utilisateur (IHM), connexion des espaces sécurisés, système de discussion, gestion des notifications pour le gardien et accès à la visualisation des données historiques.
* **⚙️ Backend & IA (Camron)** : Conception de l'API REST (Node.js/Docker), gestion de la base de données SQLite et intégration du modèle de Computer Vision (Teachable Machine).
* **📱 Mobilité (Angelina)** : Développement de l'application Android pour un accès nomade, notifications d'alertes pour le gardien et accès rapide aux données.
* **🔌 IoT & Infrastructure (Yanis)** : Intégration électronique sur les supports physiques, câblage des composants, gestion logicielle des servomoteurs et établissement de la communication série avec l'Arduino.

## 🔄 Parcours Utilisateur : Le cycle du déchet

1. **Authentification** : Le résident scanne son badge **NFC**. L'API valide l'accès et déverrouille le local.
2. **Analyse IA** : L'utilisateur présente le déchet devant la caméra. L'IA l'identifie en temps réel.
3. **Validation & Ouverture** : Si le seuil de confiance est **> 75%**, l'API identifie le bac cible et l'Arduino actionne le servomoteur correspondant.
4. **Signalétique Claire** : Chaque bac est identifié par une **inscription textuelle** pour garantir un tri sans erreur, complétée par la couleur sur le prototype :
* 🟡 **PLASTIQUE**
* 🔵 **PAPIER**
* 🟢 **VERRE**


5. **Fermeture & Sync** : Le bac se referme automatiquement après ** minimum 15 secondes**. Les données sont synchronisées sur le **Site Web** et l'**Application Android**.

## 🛠️ Stack Technique Global

* **Infrastructure** : Docker & Docker Compose (Orchestration API & Node-RED).
* **Backend** : Node.js (Express), SQLite, JWT (Authentification).
* **Site Web** : HTML5, CSS3, JavaScript (Interface responsive).
* **Mobile** : Java/Kotlin (Android Studio).
* **Hardware** : Arduino (C++), Servomoteurs, Module NFC, Liaison Série USB.
* **IA** : Teachable Machine (Classification d'images).

## 🔑 Gestion des Accès

* **Résidents (par foyer)** : Consultation de l'historique de tri et messagerie avec la maintenance.
* **Gardiens (Admin)** : Supervision du remplissage, réception d'alertes automatiques (**70% et 90%**) et gestion technique du local.

## 🚀 Déploiement

```bash
docker compose up --build

```


> ### ⚠️ Copyright & Usage
> **© 2026 Cha130 - All rights reserved.**
> 
> ** Ce projet est public pour consultation uniquement. Aucune licence d'utilisation, de modification ou de redistribution n'est accordée.
> 
> **In English:** This repository is provided for viewing purposes only. No permission is granted to copy, modify, distribute, or use this code in any form.

---


*Projet collaboratif réalisé dans le cadre scolaire — Allier technologie et transition écologique.*
