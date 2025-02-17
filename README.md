## Procédure d'installation de git clone pour la documentation SQL

### Cloner le dépôt GitHub :
- Ouvrez l'invite de commande <b>(cmd)</b> ou <b>Git Bash.</b><br><br>

* Commencez par cloner le dépôt sur votre machine locale :<br>
* Une fois le dépôt cloné, il est nécessaire d'installer les dépendances du projet.<br>
* Pour ce faire, exécutez la commande suivante dans le terminal à la racine du projet :<br>

```bash
git clone https://github.com/fannysaez/Documentation-SQL.git
cd Documentation-SQL
```

## 🗂️ Structure de la documentation SQL
```bash
📂 Documentation-SQL
│── 📄 README.md         # Introduction et guide d'utilisation
```

## 1- Introduction à SQL 🛠️<br>
 **SQL** (**S**tructured **Q**uery **L**anguage) est un langage utilisé pour manipuler et gérer les bases de données relationnelles.

### 📌 Pourquoi apprendre SQL ?<br>
* Interagir avec des bases de données efficacement.
* Extraire des informations utiles grâce à des requêtes.
* Utilisé dans de nombreux systèmes de gestion de bases de données (MySQL ...).

### 🔹 Qu’est-ce qu’une base de données (base de données relationnelles) ?
Une base de données est un ensemble structuré de données stockées et organisées de manière à faciliter leur accès et leur gestion.<br>

Une base de données relationnelle stocke des données sous forme de tables composées : <br>
* **lignes (ou enregistrements)**
* **colonnes (ou champs)**<br>

Chaque table possède une **clé primaire** pour identifier de manière unique chaque ligne.

## Installation et utilisation de WAMP sur Windows 🖥️

### 📌 Qu'est-ce que WAMP ?
WAMP (*Windows, Apache, MySQL, PHP*) est un environnement de développement permettant d’exécuter un serveur web en local avec MySQL.

### 🚀 Installation de WAMP<br>
1. **Télécharger WAMP**  
   - Rendez-vous sur le site officiel : [https://www.wampserver.com/](https://www.wampserver.com/)  
   - Téléchargez la version correspondant à votre système (32 ou 64 bits).
   - Installez-le en suivant les instructions.

2. **Lancer WAMP**  
   - Ouvrez WAMP et assurez-vous que l’icône devient **verte** (cela signifie que le serveur fonctionne).

## phpMyAdmin : Interface web pour MySQL 🖥️

### 📌 Qu’est-ce que phpMyAdmin ?
phpMyAdmin est une interface web qui permet de gérer facilement les bases de données MySQL.

### 🚀 Accéder à phpMyAdmin
1. **Démarrer WAMP** et vérifier que l’icône est **verte**.
2. Ouvrir un navigateur et entrer l’URL :  

```bash
http://localhost/phpmyadmin/
```

