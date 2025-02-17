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

[Documentation sur SQL](https://fr.khanacademy.org/computing/computer-programming/sql-documentation)
[les bases du SQL](https://fr.khanacademy.org/computing/computer-programming/sql)

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
   - Clique gauche sur l'icone **verte**

   ``` bash 
    Allez sur PhpMyAdmin
    puis de nouveaux cliquez sur phpMyAdmin 5.2.1
   ```

## phpMyAdmin : Interface web pour MySQL 🖥️

### 📌 Qu’est-ce que phpMyAdmin ?
phpMyAdmin est une interface web qui permet de gérer facilement les bases de données MySQL.

### 🚀 Accéder à phpMyAdmin
1. **Démarrer WAMP** et vérifier que l’icône est **verte**.
2. Ouvrir un navigateur et entrer l’URL :  

```bash
http://localhost/phpmyadmin/
```
3. Se connecter avec PhpMyAdmin(MySQL):

``` bash
Utilisateur : root
Mot de passe : (laisser vide par défaut)
puis cliquez sur connexion
```

### ⌨️ Quelques commandes SQL essentielles :

| Commande | Description |
|----------|------------|
| `SELECT` | Récupère des données d'une table |
| `INSERT INTO` | Ajoute de nouvelles données |
| `UPDATE` | Met à jour des données existantes |
| `DELETE` | Supprime des données |

### Explication de l'onglet>Concepteur :

* Le concepteur permet de visualiser et de modifier les relations entre les tables de la base de données de manière intuitive et graphique.
* Il offre une vue d'ensemble des structures de tables et de leurs connexions, facilitant ainsi la gestion et l'optimisation des bases de données.

### 📌 Comment créer la base de données ?<br>
Création de la base de données en **requête SQL** via **terminal**<br>

📝 Exécuter une requête SQL

Dans l’onglet SQL, entrez une commande 
``` bash
CREATE DATABASE `nom_de_la_base_de_donnée`
DEFAULT CHARACTER SET utf8
DEFAULT COLLATE utf8_general_ci;

puis clique sur le bouton 'Exécuter'
```

Cette commande permet de 
``` bash 
créer une base de données appelée 'nom de la base'
``` 
avec le bon interclassement (utf8_general_ci)

### 📌 Comment créer la table ?<br>

📝 Exécuter une requête SQL

``` bash
CREATE TABLE `nom_de_la_table`(

    id INT PRIMARY KEY AUTO_INCREMENT NOT NULL,
    label VARCHAR(255) NOT NULL,
    title VARCHAR(255) NOT NULL,
    first_name VARCHAR(255) NOT NULL,
    last_name VARCHAR(255) NOT NULL,
    duration INT NULL,
    lauch_at DATE NULL,
    birth_at DATE NULL,
    description TEXT NULL

) ENGINE = INNODB;
``` 

### a) - Explication des commandes pour créer un Id Unique :

```bash

PRIMARY KEY --> Clé Unique
AUTO_INCREMENT --> Ajout automatiquement un id '1,2,3' à chaque nouvelle ligne
NOT NULL --> Ne peut pas être vide

```

### 4. Exemples pratiques de requêtes SQL 📊

🔹 Sélectionner toutes les données d’une table
```bash
SELECT * FROM `nom_de_la_table`;
```
🔹 Insérer des nouvelles données 
```bash
INSERT INTO `nom_de_la_table`(nom, email) VALUES ('Alice', 'alice@example.com');
```
🔹 Mettre à jour une donnée
```bash
UPDATE `nom_de_la_table` SET email = 'nouveau@example.com' WHERE nom = 'Alice';
```
🔹 Supprimer des données
```bash
DELETE FROM `nom_de_la_table` WHERE nom = 'Alice';
```

### Comment manipuler les différentes requêtes  ?

🔹 Sélectionner des colonnes spécifiques
```bash
SELECT nom, email FROM `nom_de_la_table`;
```