🦇 WayneTech Tactical HUD - Batman GCC


Un assistant tactique mobile de table pour le jeu de plateau Batman: Gotham City Chronicles. Cette application permet de filtrer les personnages par scénario ou par mode Versus, d'afficher les compétences nettoyées des artefacts SQL, et de consulter les statistiques des tuiles "carton" en temps réel.
🚀 Fonctionnalités
🎮 Modes de Jeu
Mode Scénario (Aventure) : Sélection par mission, filtrage automatique par slots de héros, et affichage complet des vilains de l'Overlord.
Mode Versus (Escarmouche) : Composition libre d'équipes (Héros vs Vilains) avec filtrage intelligent des personnages possédant des statistiques de "tuiles".
🧠 Intelligence & Ergonomie
Hiérarchie Visuelle : Les Leaders (Héros/Vilains) apparaissent en pleine opacité, tandis que les troupes (Sbires/Civils) sont en retrait visuel (style pâle).
Accordéons Dynamiques : Les descriptions de compétences sont masquées par défaut pour économiser l'espace sur mobile ; elles s'ouvrent au toucher.
Nettoyage Auto : Correction automatique des erreurs de texte SQL (\rn, mots collés comme relancesrngratuites).
Stats "Carton" : Affichage des icônes tactiques pour la Défense (🛡️), le Mouvement (🥾), l'Envergure (📐) et le Prix (💰).
🛠 Administration
Hub Console : Interface d'édition pour créer des personnages, lier des compétences et gérer les déploiements en mission sans toucher au code JSON.
📁 Structure du Projet
text
├── db_to_json.py       # Script Python d'exportation MySQL vers JSON
├── www/
│   ├── index.html      # Interface tactique principale (HUD)
│   ├── admin.html      # Console d'administration de la base
│   ├── style.css       # Design futuriste Cyberpunk
│   ├── data.json       # Base de données exportée
│   └── sound/          # Alertes sonores WayneTech
│       ├── cyberpunk-alerte.mp3
│       └── cyberpunk-message.mp3
Utilisez le code avec précaution.
🛠 Installation
1. Préparation des données
Utilisez le script db_to_json.py pour transformer votre base de données MySQL en fichier utilisable par l'interface :
bash
pip install mysql-connector-python
python db_to_json.py
Utilisez le code avec précaution.
2. Déploiement avec Docker
Placez le dossier www dans un conteneur Nginx ou Apache :
bash
docker run --name waynetech-hud -v /chemin/vers/www:/usr/share/nginx/html:ro -p 8080:80 -d nginx
Utilisez le code avec précaution.
Accédez ensuite à l'interface via http://localhost:8080.
🎨 Design System
L'interface utilise un thème Cyber-WayneTech :
Bleu Néon (#00f2ff) : Alliés et système.
Rouge Néon (#ff003c) : Menaces et Overlord.
Police : Share Tech Mono (Style Terminal).
📝 Licence
Ce projet est un outil de fan non officiel pour le jeu de plateau de Monolith Board Games. Batman et tous les personnages associés sont la propriété de DC Comics.
