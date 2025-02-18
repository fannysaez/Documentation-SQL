
### 📌 Qu’est-ce qu’une base de données (base de données relationnelles) ?
Une base de données est un ensemble structuré de données stockées et organisées de manière à faciliter leur accès et leur gestion.<br>

Une base de données relationnelle stocke des données sous forme de tables composées : <br>
* ***lignes (ou enregistrements)***
* ***colonnes (ou champs)***<br>

Chaque table possède une **clé primaire** pour identifier de manière unique chaque ligne.

### 2. Clés primaires et étrangères<br>

#### a. Clé primaire<br>

```bash
- Une **clé primaire** est `une colonne ou un groupe de colonnes dans une table` qui permet d’identifier de manière **unique** `chaque ligne.`
- Elle doit être unique pour `chaque enregistrement` et ne peut pas être ***NULL***.
 ```

#### b. Clé étrangère<br>

```bash
- Une `clé étrangère` est une colonne qui fait référence à la clé primaire d’une autre table. Cela permet de lier deux tables ensemble. Par exemple, dans la table commandes, la colonne utilisateur_id est une clé étrangère qui fait référence à la clé primaire id dans la table utilisateurs.
```

### 3. Les types de données dans une base de données relationnelle<br>

Les bases de données relationnelles utilisent différents types de données pour définir la nature des informations stockées dans chaque colonne. Quelques types de données courants sont :<br> 

```bash
* INT : Entier
* VARCHAR(n) : Chaîne de caractères de longueur variable
* TEXT : Texte long
* DATE : Date (format YYYY-MM-DD)
* DECIMAL : Nombre décimal avec une précision définie <br>
```

[Précédent](commandes-SQL.md) | [Suivant](exemples-requêtes.md)  <br>


