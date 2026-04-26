# 🦇 WayneTech Tactical HUD - Batman GCC

[![Interface](https://shields.io)](#)
[![JS](https://shields.io)](#)
[![Docker](https://shields.io)](#)

Un assistant tactique mobile de table pour le jeu de plateau **Batman: Gotham City Chronicles**. Cette application permet de filtrer les personnages par scénario ou par mode Versus, d'afficher les compétences nettoyées des artefacts SQL, et de consulter les statistiques des tuiles "carton" en temps réel.

## 🚀 Fonctionnalités

### 🎮 Modes de Jeu
*   **Mode Scénario (Aventure) :** Sélection par mission, filtrage automatique par slots de héros, et affichage complet des vilains de l'Overlord.
*   **Mode Versus (Escarmouche) :** Composition libre d'équipes (Héros vs Vilains) avec filtrage intelligent des personnages possédant des statistiques de "tuiles".

### 🧠 Intelligence & Ergonomie
*   **Hiérarchie Visuelle :** Les Leaders (Héros/Vilains) apparaissent en pleine opacité, tandis que les troupes (Sbires/Civils) sont en retrait visuel (style pâle).
*   **Accordéons Dynamiques :** Les descriptions de compétences sont masquées par défaut pour économiser l'espace sur mobile ; elles s'ouvrent au toucher.
*   **Nettoyage Auto :** Correction automatique des erreurs de texte SQL (`\rn`, mots collés comme `relances gratuites`).
*   **Stats "Carton" :** Affichage des icônes tactiques pour la Défense (🛡️), le Mouvement (🥾), l'Envergure (📐) et le Prix (💰).

### 🛠 Administration
*   **Hub Console :** Interface d'édition pour créer des personnages, lier des compétences et gérer les déploiements en mission sans toucher au code JSON.

## 📁 Structure du Projet

```text
├── db_to_json.py       # Script Python d'exportation MySQL vers JSON
├── www/
│   ├── index.html      # Interface tactique principale (HUD)
│   ├── admin.html      # Console d'administration de la base
│   ├── style.css       # Design futuriste Cyberpunk
│   ├── data.json       # Base de données exportée
│   └── sound/          # Alertes sonores WayneTech
│       ├── cyberpunk-alerte.mp3
│       └── cyberpunk-message.mp3
```

## 🛠 Installation

### Exécution avec Docker Compose
Assurez-vous d'avoir Docker et Docker Compose installés, puis lancez la commande suivante à la racine du projet :

```bash
docker compose up -d
```

L'interface sera alors accessible via votre navigateur à l'adresse :
👉 `http://localhost:8080`

### Gestion du conteneur
*   **Arrêter le HUD :** `docker-compose stop`
*   **Relancer après modification :** `docker-compose up -d`
*   **Voir les logs :** `docker-compose logs -f`


## 🎨 Design System
L'interface utilise un thème **Cyber-WayneTech** :
*   **Bleu Néon (`#00f2ff`) :** Alliés et système.
*   **Rouge Néon (`#ff003c`) :** Menaces et Overlord.
*   **Police :** `Share Tech Mono` (Style Terminal).

---
**[ ACCESS_GRANTED ]** - *Gotham is under your watch.*
