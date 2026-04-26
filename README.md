# 🦇 WayneTech Tactical HUD - Batman GCC

> **STATUS:** `ACCESS_GRANTED`
> **INTERFACE:** `CYBERPUNK_V3.1`
> **DEPLOYMENT:** `DOCKER_READY`

Un assistant tactique mobile de table pour le jeu de plateau **Batman: Gotham City Chronicles**. Cette application permet de gérer ses escouades, de consulter les statistiques des tuiles "carton" et de vérifier les points de règles sans quitter la table de jeu.

---

## 🚀 Fonctionnalités Majeures

### 🎮 Modes de Jeu & Déploiement
*   **Mode Scénario (Aventure) :**
    *   Filtrage automatique par slots de héros prévus par la mission.
    *   **Zone de Renforts :** Recrutement dynamique d'alliés ou de civils (Type 1 & 4) avec **exclusivité mutuelle** (une unité prise par un camp disparaît pour l'autre).
*   **Mode Versus (Escarmouche) :** Composition libre d'équipes (Héros vs Vilains) avec détection automatique des fiches de statistiques.

### 🧠 Logique de Grade & Visuel
*   **Tri Hiérarchique :** Les **Lieutenants (Grade 3)** sont priorisés en haut de liste. Les unités de soutien et civils sont classés ensuite par ordre alphabétique.
*   **Distinction de Grade :**
    *   **Leaders :** Pleine opacité, cadre néon plein.
    *   **Minions/Alliés :** Opacité 50%, cadre en pointillés (`dashed`) pour une lecture rapide du plateau.
*   **Smart Stats :** Affichage intelligent sous le nom. Les icônes **Soutien (🤝)** et **Coût (💰)** se masquent automatiquement si leur valeur est à zéro.

### 📖 Codex WayneTech
*   **Dictionnaire des Compétences :** Page dédiée (`dictionnaire.html`) pour rechercher n'importe quel pouvoir de la base de données par nom ou effet.
*   **Nettoyage SQL Gravé :** Correction chirurgicale des artefacts de base de données (`\rn`, mots collés, doubles espaces).

---

## 📁 Structure du Projet

```text
├── db_to_json.py       # Script Python d'exportation MySQL vers JSON (Clean Text v2)
├── www/
│   ├── index.html      # HUD Tactique & Gestionnaire de combat
│   ├── dictionnaire.html # Codex de recherche des compétences
│   ├── style.css       # Design System (Grilles Versus & Styles de Grades)
│   ├── data.json       # Base de données exportée et nettoyée
│   └── sound/          # Alertes sonores système
```

---

## 🛠 Installation & Update

### 1. Synchronisation des données
Avant de lancer le HUD, exportez vos dernières modifications SQL :
```bash
python3 db_to_json.py
```

### 2. Exécution avec Docker
```bash
git clone https://github.com/metitloup/bgcc-hub.git
docker compose up -d
```
L'interface est accessible à l'adresse : 👉 `http://localhost:8080`

---

## 🎨 Design System
L'interface respecte les protocoles visuels de la Batcave :
*   **Héros & Alliés :** Système de bordures **Bleu Néon** (`#00f2ff`).
*   **Menaces & Overlord :** Système de bordures **Rouge Néon** (`#ff003c`).
*   **Typographie :** `Share Tech Mono` pour l'aspect terminal tactique.

---
**[ SYSTEM_STABLE ]** - *Gotham is under your watch.*
