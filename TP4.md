## TP4 - SQL

Avant de commencer ce TP, assurez-vous d'avoir installé et lancé WAMP (Windows) ou MAMP (MacOS) ou XAMPP (Linux/Windows/MacOS).

### Installation de la base de données

Dans ce TP, nous allons exécuter des requêtes d'écriture et de sélection de données. Afin d'avoir des données à requêter, nous allons utiliser une base de données de test, représentant le système RH d'une entreprise. Nous allons pour cela utiliser des scripts permettant de configurer la base de données sur notre ordinateur :

1. Télécharger le _repository_ [https://github.com/datacharmer/test_db](https://github.com/datacharmer/test_db) (bouton vert __Clone or download__)
2. Vérifiez que la commande `mysql` fonctionne sur votre ordinateur depuis un terminal. Si ce n'est pas le cas, vous devrez l'ajouter au __PATH__.
	- [MacOS] dans un terminal : 
		- exécuter la commande : `nano ~/.bash_profile`
		- rajouter la ligne : `export PATH="/Applications/MAMP/Library/bin:$PATH"`
		- `control` + `X`
		- `Y`
		- appuyer sur __Entrée__
		- exécuter la commande : `source ~/.bash_profile`
	- [Windows] 
		- Ouvrir XAMPP et lancer les services Apache et MySQL.
		- Cliquer sur le bouton Shell dans l'interface de WAMPP. 
3. Depuis un terminal, allez dans le _repository_ que vous venez de télécharger avec la commande `cd` (tapez `cd` suivi d'un espace, puis faites glisser le dossier téléchargé dedans).
	- `cd test_db`
4. Exécutez la commande : `mysql -u root -p < ./employees.sql` (le mot de passe est souvent `root` ou vide par défaut). Cette commande va exécuter les instructions présentes dans le fichier `employees.sql`. Ce fichier construit d'abord les __tables__ de notre base de données, ajoute les contraintes (clé primaire/étrangères...) puis y insère un gros volume de données.
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
- Ordre des mots-clés :
	1. `SELECT`
	2. `FROM` (avec `,`/(`INNER`/`NATURAL`/`CROSS`/`RIGHT`/`LEFT`(`OUTER`))) `JOIN`)
	3. `WHERE`
	4. `GROUP BY`
	5. `HAVING` (sorte de `WHERE` pour les éléments regroupés (`AVG`, `SUM`...))
	6. `ORDER BY`
	7. `LIMIT` `OFFSET`


#### Exercices

Pour ces exercices, vous pouvez exécuter vos requêtes depuis la page __PhpMyAdmin__, dans le logiciel __MySQL Workbench__ ou dans un terminal via le shell MySQL (`mysql -u root -p`, déconseillé car pas très visuel).

1. Donnez le nombre d'employés présents dans la table `employees`.<br>_Résultat : 300024_
2. Donnez la liste de tous les départements, triés par ordre alphabétique de leur nom.<br>Vous ne donnerez que le nom et renommerez la colonne correspondante en `Nom du département`.<br>_Résultat : 9 tuples_
3. Donnez les noms et prénoms des employés dont le nom de famille commence par un `'C'` (majuscule ou minuscule).<br>Vous trierez les résultats alphabétiquement par nom croissant, puis par prénom décroissant.<br>Limitez le résultat à 500 tuples et veillez à éliminer les doublons.
4. Combien de personnes s'appellent __Georgi Facello__ ?<br>_Résultat : 2_
5. Donnez la liste des employés ainsi que leurs salaires.<br>Vous limiterez le résultat à 500 lignes.
6. Donnez la liste des employés qui travaillent ou ont travaillé au départemant de recherche.<br>Vous limiterez le résultat à 500 lignes.
7. Donnez la liste des employés ayant le même nom de famille.<br>Limitez le résultat à 500 lignes.
8. Quel était le montant du salaire de __Hinrich Randi__ en 1998 ?<br>Les salaires étant actualisés chaque année, le résultat doit comporter 2 lignes (avant et après actualisation).
9. Donnez l'ID, le nom et le prénom des employés étant passés par au moins 3 titres différents au sein de l'entreprise.<br>Vous limiterez le résultat à 500 lignes.
10. Donnez pour chaque employé la somme de ses salaires cumulés au sein de l'entreprise dans la colonne "`Total des salaires`", ainsi que le nombre de salaires différents qu'il a perçu dans la colonne "`Nombre de salaires`".<br>Vous limiterez le résultat à 500 lignes.
11. Quels employés ont toujours eu le même salaire ?<br>Vous limiterez le résultat à 500 lignes.
12. Donnez la liste des personnes qui travaillent ou ont travaillé dans le département de recherche ET/OU dans le département de développement.
13. Donnez la liste des employés ayant eu les titres d'ingénieur et d'ingénieur senior.<br>Vous limiterez le résultat à 500 lignes.
14. Donnez la liste des employés ayant eu le titre d'ingénieur senior mais pas celui d'ingénieur.<br>Vous limiterez le résultat à 500 lignes.
15. Rajoutez vous à la base de données, vous ferez en sorte d'avoir le titre d'ingénieur, de travailler au département de développement, et vous vous fixerez le salaire de votre choix pour la durée de votre choix. 
