## TP4 - SQL

Avant de commencer ce TP, assurez-vous d'avoir installé et lancé WAMP (Windows) ou MAMP (MacOS) ou XAMPP (Linux/Windows/MacOS).

### Installation de la base de données

Dans ce TP, nous allons exécuter des requêtes d'écriture et de sélection de données. Afin d'avoir des données à requêter, nous allons utiliser une base de données de test, représentant le système RH d'une entreprise. Nous allons pour cela utiliser des scripts permettant de configurer la base de données sur notre ordinateur :

1. Télécharger le _repository_ [https://github.com/datacharmer/test_db](https://github.com/datacharmer/test_db) (bouton vert __Clone or download__)
2. Vérifiez que la commande `mysql` fonctionne sur votre ordinateur depuis un terminal. Si ce n'est pas le cas, vous devrez l'ajouter au __PATH__.
Sur MacOS, exécutez les commandes suivantes : `export PATH="/Applications/MAMP/Library/bin:$PATH"` puis `source ~/.bash_profile`.
3. Depuis un terminal, allez dans le _repository_ que vous venez de télécharger avec la commande `cd`.
4. Exécutez la commande : `mysql -u root -p < ./employees.sql` (le mot de passe est souvent `root` par défaut). Cette commande va exécuter les instructions présentes dans le fichier `employees.sql`. Ce fichier construit d'abord les __tables__ de notre base de données, ajoute les contraintes (clé primaire/étrangères...) puis y insère un gros volume de données.
5. Vous pouvez supprimer le _repository_ téléchargé, nous n'en auront plus besoin.

### Énoncé de TP

#### Compréhension de la base de données

Avant de travailler sur une base de données, il faut comprendre les relations (tables) et associations qui la composent. Voici le schéma de la base de données que nous venons de configurer :

<p align="center">
	<img src="https://github.com/datacharmer/test_db/blob/master/images/employees.jpg" width="70%">
</p>

1. Identifiez les relations et associations de la base de données.
2. Identifiez les clés primaires/étrangères.
3. Essayez également de comprendre le fichier [`employees.sql`](https://github.com/datacharmer/test_db/blob/master/employees.sql) permettant de créer la base de données.

#### Aide

- En SQL, tout ce qui se trouve à droite de `-- ` est un __commentaire__.
- Sauvegardez vos réponses dans un fichier `.sql` (surtout si vous travaillez sur MySQL Workbench).
- La base de données contenant énormément de données, ajoutez une limite au nombre de lignes du résultat en ajoutant `LIMIT 100` à la fin de votre requête par exemple pour limiter à 100 tuples.


#### Exercices

Pour ces exercices, vous pouvez exécuter vos requêtes depuis la page __PhpMyAdmin__, dans le logiciel __MySQL Workbench__ ou dans un terminal via le shell MySQL (`mysql -u root -p`, déconseillé car pas très visuel).

1. Donnez le nombre d'employés présents dans la table `employees`.<br>_Résultat : 300024_
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
