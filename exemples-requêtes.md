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

Cette commande permet de créer une base de données appelée 'nom de la base'<br>
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
AUTO_INCREMENT --> Ajoute automatiquement un ID incrémenté 1,2,3 à chaque nouvelle ligne
NOT NULL --> Ne peut pas être vide

```

### 4. 📊Exemples pratiques de requêtes SQL 

🔹 Sélectionner `SELECT` toutes les données `*` d’une table
```bash
SELECT * FROM `nom_de_la_table`;
```
🔹 Insérer `INSERT INTO` des nouvelles données 
```bash
INSERT INTO `nom_de_la_table`(nom, email) VALUES ('Alice', 'alice@example.com');
```

🔹 Mettre à jour des données `UPDATE`
```bash
UPDATE `nom_de_la_table` SET email = 'nouveau@example.com' WHERE nom = 'Alice';
```
🔹 Supprimer des données `DELETE FROM`
```bash
DELETE FROM `nom_de_la_table` WHERE nom = 'Alice';
```

### 📌 Comment manipuler les différentes requêtes  ?

🔹 Sélectionner des colonnes spécifiques `SELECT` et `FROM`
```bash
SELECT nom, email FROM `nom_de_la_table`;
```

🔹 Filtrer les résultats avec `WHERE`
```bash
SELECT * FROM `nom_de_la_table` WHERE nom = 'Alice';
```

🔹 Trier les résultats avec `ORDER BY`
```bash
SELECT * FROM `nom_de_la_table` ORDER BY nom ASC;
```

🔹 Limiter le nombre de résultats avec `LIMIT`
```bash
SELECT * FROM `nom_de_la_table`s LIMIT 5;
```

🔹 Compter le nombre d’utilisateurs avec `COUNT`
```bash
SELECT COUNT(*) FROM `nom_de_la_table`;
```

### 📊 Fonctions d'agrégation<br>

🔹 Calculer la `moyenne` d’une colonne
```bash
SELECT AVG(age) FROM `nom_de_la_table`;
```

🔹 Trouver la valeur minimale `MIN` et maximale `MAX` d’une colonne
```bash
SELECT MIN(age) FROM `nom_de_la_table`;
SELECT MAX(age) FROM `nom_de_la_table`;
```

📌 Filtrer avec `LIKES`

Le caractère % est un caractère joker qui remplace tous les autres caractères.
* Rechercher toutes les chaines de caractère qui se termine par un “A”.<br>

```bash
SELECT * FROM `nom_de_la_table` WHERE nom LIKE '%A';
```
* Rechercher toutes les lignes de “colonne” qui commence par un “a”.
```bash
SELECT * FROM `nom_de_la_table` WHERE nom LIKE 'a%;
```
* Rechercher tous les enregistrement qui utilisent le caractère “a”.
```bash
SELECT * FROM `nom_de_la_table` WHERE nom LIKE '%a%';
```

#### 📌 Utilisation de `OR` et `AND`
```bash
SELECT * FROM `nom_de_la_table` WHERE nom = 'Alice' OR nom = 'Bob';
SELECT * FROM `nom_de_la_table` WHERE nom = 'Alice' AND email LIKE '%@gmail.com';
```

#### 📌 Regrouper les résultats avec `GROUP BY`
```bash
SELECT email, COUNT(*) FROM `nom_de_la_table` GROUP BY email;
``` 

#### 📌 Filtrer des groupes avec `HAVING`
```bash
SELECT email, COUNT(*) FROM `nom_de_la_table` GROUP BY email HAVING COUNT(*) > 1;
```

#### 📌 Utiliser `INNER JOIN` pour lier des tables
```bash
SELECT utilisateurs.nom, commandes.produit FROM `nom_de_la_table`
INNER JOIN commandes ON utilisateurs.id = commandes.utilisateur_id;
```

#### 📌 Concatenation de colonnes avec `CONCAT`
```bash
SELECT CONCAT(nom, ' ', email) AS nom_email FROM `nom_de_la_table`;
```

<br>
<p align="center">
  <a href="commandes-SQL.md">Précédent</a> | <a href="README.md">Retour</a> | <a href="assets/schema-voyage-db.png">Suivant</a><br>
 </p> 