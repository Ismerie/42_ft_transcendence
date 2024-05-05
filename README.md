# 42_ft_transcendence
42_ft_transcendence est le dernier projet du tronc commun de l'école 42. Ce projet consiste à créer un site web SPA (Single Page Application) permettant de jouer au **jeu Pong** en mode 1 vs 1 ou en mode Tournoi.  
Ce projet a été réalisé avec [@ThibautCharpentier](https://github.com/ThibautCharpentier) et [@tuturbo](https://github.com/tuturbo)

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
Pour améliorer notre site web nous devions choisir parmi une vaste liste de modules (Web, Gestion Utilisateur, IA-Algo, Cybersécurité, Devops, Graphiques, Accessibilité, Orienté objet).  
Chaque module vaut soit 1 ou 0.5 point. Nous devions implémenter une valeur de 7 pts.  
Modules choisis : 
| Valeur |  Thèmes                |Modules                             | Descriptions                                                                                                       |
| ------ | ---------------------- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| 1      | 🌐 Web                 | Framework Back-end                 | Utiliser framework **Django**                                                                                      |
| 0.5    | 🌐 Web                 | Toolkit Front-end                  | Utiliser toolkit **Bootstrap**                                                                                     |
| 0.5    | 🌐 Web                 | Base de données                    | Utiliser **PostegreSQL**                                                                                           |
| 1      | 👤 Gestion utilisateur | Gestion utilisateur standard       | Les utilisateur peuvent **s'inscrire/s'authentifier** sur l'application. Ils ont un **nom unique**. Ils peuvent **mettre à jour leur profil** et télécharger un **avatar**, avoir un **historique** de jeu et accéder à des **statistiques**. Ils peuvent ajouter d'autres utilisateurs comme **amis** et consulter leur status.                            |
| 1      | 👤 Gestion utilisateur | Joueurs à distance                 | Il est possible d'avoir deux joueurs distants. **Chaque joueur est sur un ordinateur différent et joue au même match de PONG**|
| 1      | 🚨 Cybersécurité       | 2FA et JWT                         | Les utilisateurs peuvent utiliser **l'authentification à deux facteurs (2FA)**. S'ils utilisent le 2FA, ils reçoivent **par email un code à usage unique** à utiliser comme double authentification. **Les jetons Web JSON (JWT)** sont implémentés comme méthode d'auhtentification et d'autorisation, garantissant que **les sessions utilisateur et l'accès aux ressources sont gérés en toute sécurité** |
| 1      | 🎨 Graphique           | Techniques avancées 3D             | Amélioration du visuel du jeu en utilisant **Three.js/WebGL**                                                      |
| 0.5    | 📱 Accessibilité        | Support sur tous types d'appareil  | Compatible **ordinateur, tablette, smartphone**. Les écrans **tactiles** sont gérés et le site Web est **responsive** |
| 0.5    | 📱 Accessibilité        | Compatibilité navigateurs web      | Le site Web fonctionne sur au moins un navigateur supplémentaire comme **Firefox**                                 |

## 📷 Aperçus

### Menu
![alt-text](https://github.com/Ismerie/42_ft_transcendence/blob/master/preview/view_menu.jpg)
### Statistiques
![alt-text](https://github.com/Ismerie/42_ft_transcendence/blob/master/preview/view_stats.jpg)
### Liste d'amis
![alt-text](https://github.com/Ismerie/42_ft_transcendence/blob/master/preview/view_friends.jpg)
### Historique
![alt-text](https://github.com/Ismerie/42_ft_transcendence/blob/master/preview/view_history.jpg)
### Profil
![alt-text](https://github.com/Ismerie/42_ft_transcendence/blob/master/preview/view_profil.jpg)
### Notifications
![alt-text](https://github.com/Ismerie/42_ft_transcendence/blob/master/preview/view_notif.jpg)
### Paramètres
![alt-text](https://github.com/Ismerie/42_ft_transcendence/blob/master/preview/view_parameters.jpg)
### Jeu

## 🛠️ Usage
Premièrement, vous devez créer un fichier **.env** à la racine du projet, qui ressemblera à ceci :
```
FRONT_URL=https://localhost:8080
FRONT_URL2=https://127.0.0.1:8080

#ifconfig enp4s0f0 | grep 'inet' | awk '{print $2}' | head -n 1
#OR
#ip addr show enp4s0f0 | grep 'inet ' | awk '{print $2}' | cut -d/ -f1 | head -n 1
HOST_IP=

#Settings of your database, by default it can be:
DB_HOST=db
DB_PORT=5432
DB_USER=postgres
DB_PASSWORD=password
DB_NAME=transcendence

#Put whatever you want for this one:
JWT_SECRET_KEY=ItIsASecretTokenKey

#You have to use an email communication platform to send email (like sendgrid for example) and put your settings here:
EMAIL_HOST =
EMAIL_HOST_USER =
EMAIL_HOST_PASSWORD =
EMAIL_PORT =

#Put whatever you want for this one too:
SECRET_KEY= 'ItIsASecretKey'

```
Ensuite, exécutez le projet avec :
```
docker compose up --build
```
Si le projet est déjà construit, utilisez :
```
docker compose up
```

Ensuite, accédez à votre adresse IP locale sur le port 8080 :
```
https://localhost:8080/
```
```
https://127.0.0.1:8080/
```
