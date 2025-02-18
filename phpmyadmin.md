## phpMyAdmin : Interface web pour MySQL 🖥️

### 📌 Qu’est-ce que phpMyAdmin ?
phpMyAdmin est une interface web qui permet de gérer facilement les bases de données MySQL

#### Guide d’utilisation de phpMyAdmin<br>

- PhpMyAdmin est un outil de gestion de bases de données MySQL via une interface web.<br>
- Il permet de créer, modifier et gérer des bases de données, des tables, des enregistrements, des utilisateurs, et d’exécuter des requêtes SQL, tout cela sans avoir besoin d’écrire de code directement dans la ligne de commande.<br>

### 1. Accéder à phpMyAdmin<br>
Une fois WAMP installé et démarré, tu peux accéder à phpMyAdmin en ouvrant ton navigateur et en entrant l’adresse suivante :<br>

```bash
http://localhost/phpmyadmin
```
Cela ouvrira la page de connexion à phpMyAdmin. Par défaut, le nom d’utilisateur est root et le mot de passe est vide (si tu n’as pas modifié cette configuration). <br>
Pour te connecter, utilise ces informations ou celles que tu as définies pendant l’installation de WAMP.

### 2. Interface de phpMyAdmin<br>

Une fois connecté, tu verras l’interface principale de phpMyAdmin, qui se compose de plusieurs sections :<br>

* Barre de navigation : Sur le côté gauche, tu peux voir une liste de tes bases de données. Cliquer sur une base de données te permet de voir ses tables.<br>

* Menu supérieur : Il permet de naviguer entre les différentes fonctions de phpMyAdmin, telles que la création de bases de données, l’exécution de requêtes SQL, l’importation/exportation de données, etc.<br>

* Zone principale : Affiche le contenu de la base de données ou de la table sélectionnée.

### 3. Créer une base de données<br>

Pour créer une nouvelle base de données, suis ces étapes :<br>

	1.	Dans la barre de navigation, clique sur l’option Base de données.
	2.	Entrez un nom pour ta nouvelle base de données (par exemple, gestion_utilisateurs).
	3.	Choisis un interclassement (par défaut, laisse le choix de utf8_general_ci).
	4.	Clique sur Créer.

La base de données apparaîtra ensuite dans la barre de navigation.<br>

### 4. Créer une table<br>

Une fois que tu as créé une base de données, tu peux créer des tables pour y stocker des données.<br>

	1.	Sélectionne la base de données où tu souhaites ajouter une table.
	2.	Dans la section Créer une table, entre un nom pour la table (par exemple, utilisateurs) et le nombre de colonnes que tu souhaites.
	3.	Clique sur Exécuter pour continuer.
	4.	Ensuite, tu peux définir les colonnes de la table :
    
* Nom : Le nom de la colonne (par exemple, id, nom, email).
* Type : Le type de données de la colonne (par exemple, INT, VARCHAR(100), TEXT).
* Index : Choisir si la colonne est une clé primaire, index, ou index unique.

Clique sur Enregistrer pour créer la table.<br>

### 5. Ajouter des données dans une table<br>

Une fois la table créée, tu peux ajouter des données en suivant ces étapes :<br>

	1.	Clique sur la table à laquelle tu veux ajouter des données.
	2.	Clique sur l’onglet Insérer.
	3.	Remplis les champs avec les données que tu souhaites ajouter. Par exemple, pour la table utilisateurs, tu peux entrer un nom, un     email, etc.
	4.	Clique sur Exécuter pour insérer les données.

### 6. Exécuter des requêtes SQL<br>

phpMyAdmin te permet d’exécuter des requêtes SQL directement à partir de son interface.<br>

	1.	Sélectionne la base de données dans laquelle tu veux exécuter une requête.
	2.	Clique sur l’onglet SQL.
	3.	Dans la zone de texte, entre ta requête SQL (par exemple, SELECT * FROM utilisateurs;).
	4.	Clique sur Exécuter pour exécuter la requête. Les résultats seront affichés sous la zone de saisie.

### 7. Modifier ou supprimer des données<br>

Pour modifier ou supprimer des données dans une table :<br>

	1.	Sélectionne la table et clique sur l’onglet Parcourir.
	2.	Tu verras une liste des enregistrements de la table.
	3.	Pour modifier un enregistrement, clique sur l’icône Modifier (souvent représentée par un crayon) à côté de l’enregistrement.
	4.	Pour supprimer un enregistrement, clique sur l’icône Supprimer (souvent représentée par une croix) à côté de l’enregistrement.

### 8. Exporter et importer des données<br>

PhpMyAdmin permet d’exporter et d’importer des bases de données ou des tables sous différents formats, comme SQL, CSV, ou XML.<br>

***Exporter une base de données***<br>
	1.	Sélectionne la base de données à exporter.
	2.	Clique sur l’onglet Exporter.
	3.	Choisis le format d’exportation (par exemple, SQL).
	4.	Clique sur Exécuter pour télécharger le fichier.

***Importer une base de données***<br>

	1.	Sélectionne la base de données dans laquelle tu souhaites importer des données.
	2.	Clique sur l’onglet Importer.
	3.	Choisis le fichier que tu veux importer (au format SQL, CSV, etc.).
	4.	Clique sur Exécuter pour démarrer l’importation.

### 9. Créer des utilisateurs et gérer les permissions<br>

phpMyAdmin permet de gérer les utilisateurs MySQL et leurs permissions :<br>

	1.	Clique sur l’onglet Utilisateurs.
	2.	Pour créer un nouvel utilisateur, clique sur Ajouter un utilisateur.
	3.	Remplis les informations nécessaires (nom d’utilisateur, mot de passe, hôte, etc.).
	4.	Définis les permissions (par exemple, pour un utilisateur donné, tu peux lui accorder des droits de lecture, d’écriture, ou d’administration).
	5.	Clique sur Exécuter pour créer l’utilisateur.

### 10. Sauvegarder et restaurer une base de données<br>

***Sauvegarder***<br>
* Pour sauvegarder une base de données, tu peux l’exporter en utilisant la méthode expliquée plus haut.<br>
***Restaurer***<br>
* Pour restaurer une base de données à partir d’un fichier d’export, clique sur Importer et sélectionne le fichier SQL ou autre format contenant les données sauvegardées.
