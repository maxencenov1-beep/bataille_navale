# ⚓ Bataille Navale — PHP OOP

[PHP 8]
[Orienté Objet]
[MySQL]
[Projet scolaire · BTS 2025-2026]

Projet réalisé dans le cadre du **Bloc 2 – Programmation Orientée Objet**.  
Il s'agit de la reprise et de l'amélioration d'un jeu de bataille navale en ligne, développé en PHP objet, permettant à un joueur humain d'affronter l'ordinateur.

---

## À propos du projet

Ce projet est une évolution d'une application existante de bataille navale. L'objectif est d'améliorer les fonctionnalités du jeu, de gérer les profils utilisateurs et d'implémenter des statistiques, tout en appliquant les principes de la programmation orientée objet en PHP.

---

## Fonctionnalités

- Jeu de bataille navale Joueur vs Ordinateur sur grille 20×20
- Placement aléatoire des navires (porte-avions, croiseur, sous-marin…)
- Interface de jeu interactive avec affichage des grilles en temps réel
- Résumé de fin de partie avec statistiques (précision, durée)
- Profil utilisateur et système de niveaux / progression
- IA améliorée (tirs ciblés après un impact)
- Classement général des joueurs

---

## Architecture

```
bataille-navale/
├── classes/
│   ├── Grille.php           # Gestion de la grille de jeu (placement, tirs, états des cases)
│   ├── JoueurHumain.php     # Joueur humain : nom, grille, tir sur une case
│   ├── JoueurOrdinateur.php # IA héritée de JoueurHumain, tirs aléatoires/ciblés
│   ├── Navire.php           # Modèle d'un navire : taille, position, touché/coulé
│   └── Partie.php           # Logique principale : tours de jeu, fin de partie
├── css/
│   ├── auth.css             # Styles de la page de connexion/inscription
│   ├── classement.css       # Styles du tableau de classement
│   ├── game.css             # Styles de l'interface de jeu (grilles, navires, tirs)
│   ├── index.css            # Styles de la page d'accueil
│   ├── page.css             # Styles globaux partagés entre les pages
│   └── profil.css           # Styles de la page de profil joueur
├── data/
│   ├── database.php         # Connexion à la base de données (PDO)
│   └── joueurs.json         # Stockage JSON des données joueurs (profils, stats)
├── images/                  # Ressources graphiques du jeu
├── vendor/
│   ├── composer/            # Fichiers internes générés par Composer
│   └── autoload.php         # Autoloading des classes via Composer
├── auth.php                 # Gestion de l'authentification (connexion/inscription)
├── classement.php           # Affichage du classement général des joueurs
├── composer.json            # Déclaration du projet et des dépendances
├── composer.lock            # Verrouillage des versions des dépendances
├── deconnexion.php          # Destruction de la session et redirection
├── Findepartie.php          # Écran de fin de partie : résumé et statistiques
├── gestionJeu.php           # Interface principale de jeu (grilles, tours, actions)
├── index.php                # Page d'accueil et saisie du nom du joueur
└── profil.php               # Profil joueur : stats, niveau, historique
```

---

## Technologies utilisées

| Technologie | Usage |
|-------------|-------|
| PHP 8 | Programmation Orientée Objet |
| MySQL | Stockage des profils et statistiques |
| HTML / CSS | Interface de jeu |
| Sessions PHP | Gestion de l'état de la partie |

---

## Contexte scolaire

Projet réalisé en 1ème année de BTS SIO (option SLAM) — Bloc 2 : Développement d'applications.  
Version `1.1`.
