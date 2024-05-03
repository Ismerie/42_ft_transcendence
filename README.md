# 42_ft_transcendence
42_ft_transcendence est le dernier projet du tronc commun de l'école 42. Ce projet consiste à créer un site web SPA (Single Page Application) permettant de jouer au **jeu Pong** en mode 1 vs 1 ou en mode Tournoi.
Ce projet a été réalisé avec [@ThibautCharpentier](https://github.com/ThibautCharpentier)

## 📋 Fonctionnalités

### ⌨️ Les Technos

* Back-end : **Django**
* Base de données : **PostgreSQL**
* Front-end : **Javascript**
* Toolkit Front-end : **Bootstrap**
* Bibliothèques :
  * **Three.js** -> animation 3D du jeu Pong
  * **Axios** -> récupération de données, API
  * **Socket.io** -> websockets pour changement d'information en temps réel (ex: status, demande d'amis etc...)
  * **Croppie** -> permet recadrage de l'avatar sélectionné pour son profil

### 📍 Exigences Obligatoires
### SPA
- [x] Site Web dynamique avec une seule page Web **(SPA)** en **Javascript natif**
- [x] Utilisateur doit pouvoir utiliser les boutons ⬅ ```back``` et  ➡ ```forward``` du navigateur
- [x] Compatible avec la dernière version de Chrome
- [x] Aucune erreur ou avertissement dans la console
### Sécurité
- [x] Mot de passe hachés
- [x] Protection contre les injections SQL/XSS
- [x] Connexion HTTPS
### Jeu
- [x] Le jeu doit être un PONG
- [x] Jeu en temps réel avec un autre joueur
- [x] Mode 1 vs 1 et mode Tournoi
- [x] Système de matchmaking

## 📚 Les Modules
Pour améliorer notre site web nous devions choisir parmis une vaste liste de module (Web, Gestion Utilisateur, IA-Algo, Cybersécurité, Devops, Graphiques, Accessibilité, Orienté objet).  
Chaque module vaut soit 1 ou 0.5 point. Nous devions implémenter une valeur de 7 pts.
Modules choisis : 
| Valeur |  Thèmes                |Modules                             | Descriptions                                                                                                       |
| ------ | ---------------------- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| 1      | 🌐 Web                 | Framework Back-end                 | Utiliser **Django**                                                                                                |
| 0.5    | 🌐 Web                 | Toolkit Front-end                  | Utiliser **Bootstrap**                                                                                             |
| 0.5    | 🌐 Web                 | Base de données                    | Avoir une bdd et utiliser **PostegreSQL**                                                                          |
| 1      | 👤 Gestion utilisateur | Gestion utilisateur standard       | Authentification, amis, historique, stats...                                                                       |
| 1      | 👤 Gestion utilisateur | Joueurs à distance                 | 2 joueurs peuvent s'affronter sur la même partie sur 2 ordis différents                                            |
| 1      | 🚨 Cybersécurité       | 2FA et JWT                         | Possibilité d'avoir le 2FA pour utilsateur et utiliser les JWT comme méthodes d'authentification et d'autorisation |
| 1      | 🎨 Graphique           | Techniques avancées 3D             | Amélioration du visuel du jeu en utilisant **Three.js**                                                            |
| 0.5    | 📱 Accessibilité        | Support sur tous types d'appareil  | Compatible ordinateur, tablette, smartphone (tactile)                                                              |
| 0.5    | 📱 Accessibilité        | Compatibilité navigateurs web      | Fonctionne sur Chrome, Firefox, ect..                                                                              |



## 🛠️ Usage
