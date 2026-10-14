# Jeu de gestion médiéval

Jeu de stratégie au tour par tour développé en Python avec Tkinter dans le cadre du projet **Algorithmie et Programmation 5** (L3 Informatique, année universitaire 2024–2025).

Vous incarnez un noble qui cherche à étendre son domaine et à vaincre les autres seigneurs. Développez vos villages, gérez leurs habitants et leurs ressources, puis choisissez vos alliances et vos guerres avec soin.

## Fonctionnalités

- Carte générée aléatoirement, composée de plaines, forêts, montagnes et lacs.
- Trois niveaux de difficulté : facile (3 nobles à vaincre), normal (5) et difficile (10).
- Gestion des villages, de leur population, des ressources, de l’argent et des soldats.
- Actions stratégiques : accueillir des habitants, construire des villages et des églises, lever des impôts, vassaliser et déclarer la guerre.
- Événements aléatoires, tels que les épidémies, les incendies, les pillages, les famines et les récoltes abondantes.
- Interface dessinée avec le widget `Canvas` de Tkinter, comprenant un tutoriel, un historique et des panneaux d’information.

## Prérequis

- Python **3.10 ou supérieur**.
- Tkinter, généralement inclus avec Python. Sous Linux, installez au besoin le paquet système correspondant (par exemple `python3-tk`).

Le projet n’utilise pas de dépendances Python tierces.

## Lancer le jeu

Depuis la racine du projet :

```bash
python3 main.py
```

Au menu de démarrage, choisissez la difficulté, la couleur de votre domaine et si vous souhaitez suivre le tutoriel, puis cliquez sur **Commencer**.

## Principes du jeu

Une partie se déroule en années successives. À chaque tour, les habitants et les soldats vieillissent et doivent être nourris. Le joueur dispose ensuite de **10 points d’action** pour développer son domaine.

Les principales actions sont :

| Action | Coût en points d’action | Autres coûts |
| --- | ---: | --- |
| Accueillir des habitants | 1 à 10 | Selon le type et le nombre |
| Construire un village | 8 | 300 pièces et 150 ressources |
| Construire une église | 6 | 100 pièces et 50 ressources |
| Vassaliser un noble | 4 | Offre en argent et/ou en ressources |
| Lever des impôts | 5 | — |
| Déclarer la guerre | 8 | 100 ressources |

La construction d’un village nécessite une plaine suffisamment éloignée des villages voisins. Les églises apportent des bénédictions à certains habitants. Les impôts influent sur leur humeur, tandis qu’un bonheur trop faible peut provoquer une révolte. Les demandes de vassalisation rejetées déclenchent une guerre.

La partie se termine lorsque le joueur est éliminé ou qu’il a vaincu ou vassalisé tous les autres nobles.

## Commandes

- Cliquez sur la carte et les éléments de l’interface pour consulter les villages et sélectionner les actions.
- Faites glisser la souris sur la carte pour la déplacer.
- Suivez les indications du tutoriel intégré pour découvrir les actions et les panneaux de l’interface.

## Organisation du projet

```text
.
├── main.py                  # Démarrage de l’interface Tkinter
├── jeu.py                   # Règles, tours, événements et actions
├── eventmanager.py          # Traitement et affichage des événements
├── parameter.py             # Paramètres de jeu et de l’interface
├── Canvas/                  # Carte, canvas, widgets et panneaux d’interface
├── Perso/                   # Personnages : nobles, soldats et habitants
├── Territoire/              # Villages, églises et terrains
└── assets/                  # Images utilisées par l’interface
```

## Contexte

Projet pédagogique réalisé par **Léo Faucon** et **Eloïse Rullac**. La conception et les règles sont décrites plus en détail dans le compte rendu du projet, `README.pdf`.
