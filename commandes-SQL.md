### ⌨️ Quelques commandes SQL essentielles :

| Commande      | Description                       |
| ------------- | --------------------------------- |
| `SELECT`      | Récupère des données d'une table  |
| `INSERT INTO` | Ajoute de nouvelles données       |
| `UPDATE`      | Met à jour des données existantes |
| `ALTER TABLE` | Modifie la structure d’une table  |
| `DELETE`      | Supprime des données              |

## 1. Gestion des bases de données<br>

- Créer une base de données

```bash
CREATE DATABASE nom_de_la_base;
```

- Utiliser une base de données

```bash
USE nom_de_la_base;
```

- Supprimer une base de données

```bash
DROP DATABASE nom_de_la_base;
```

## 2. Gestion des tables<br>

- Créer une table :

```bash
CREATE TABLE utilisateurs (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nom VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    date_inscription DATE
);
```

* Afficher la structure d’une table :<br>

```bash
DESCRIBE utilisateurs;
```

* Supprimer une table :<br>

```bash
DROP TABLE utilisateurs;
```

* Ajouter une colonne :<br>

```bash
ALTER TABLE utilisateurs ADD age INT;
```

* Supprimer une colonne :<br>

```bash
ALTER TABLE utilisateurs DROP COLUMN age;
```

## 3. Manipulation des données<br>

* Insérer des données:
```bash
INSERT INTO utilisateurs (nom, email, date_inscription)
VALUES ('Alice Dupont', 'alice@example.com', '2024-02-01');
```

* Mettre à jour des données :<br>
```bash
UPDATE utilisateurs
SET email = 'alice.dupont@example.com'
WHERE id = 1;
```

* Supprimer des données :
```bash
DELETE FROM utilisateurs
WHERE id = 1;
```

## 4. Requêtes SQL de sélection<br>

Sélectionner toutes les données d’une table:
```bash
SELECT * FROM utilisateurs;
```

Sélectionner certaines colonnes:
```bash
SELECT nom, email FROM utilisateurs;
```

Filtrer les résultats avec WHERE:
```bash
SELECT * FROM utilisateurs WHERE nom = 'Alice Dupont';
```
Trier les résultats avec ORDER BY:
```bash
SELECT * FROM utilisateurs ORDER BY nom ASC;
```
Limiter le nombre de résultats:
```bash
SELECT * FROM utilisateurs LIMIT 5;
```

## 5. Fonctions SQL utiles<br>

Compter le nombre d’enregistrements:
```bash
SELECT COUNT(*) FROM utilisateurs;
```
Obtenir la moyenne d’une colonne:
```bash
SELECT AVG(age) FROM utilisateurs;
```
Obtenir la somme d’une colonne:
```bash
SELECT SUM(prix) FROM commandes;
```
Obtenir la valeur maximale et minimale:
```bash
SELECT MAX(prix) FROM produits;
SELECT MIN(prix) FROM produits;
```

## 6. Jointures SQL<br>

Jointure interne (INNER JOIN):
```bash
SELECT utilisateurs.nom, commandes.id, commandes.total
FROM utilisateurs
INNER JOIN commandes ON utilisateurs.id = commandes.utilisateur_id;
```

[Précédent](bases-de-donnees.md) | [Suivant](exemples-requêtes.md) <br>
