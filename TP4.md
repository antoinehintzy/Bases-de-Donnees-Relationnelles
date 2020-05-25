## TP4 - SQL

Avant de commencer ce TP, assurez-vous d'avoir bien installé et lancé WAMP (Windows) ou MAMP (MacOS) ou XAMPP (Linux/Windows/MacOS).

### Installation de la base de données

Vous aurez également à configurer la base de données que nous allons utiliser dans ce TP. Pour ce faire, suivez les instructions suivantes :

1. Télécharger le _repository_ [https://github.com/datacharmer/test_db](https://github.com/datacharmer/test_db) (bouton vert __Clone or download__)
2. Vérifiez que la commande `mysql` focntionne depuis un terminal. Si ce n'est pas le cas, vous devrez l'ajouter au __PATH__.
Sur MacOS, exécutez les commandes suivantes : `export PATH="/Applications/MAMP/Library/bin:$PATH"` puis `source ~/.bash_profile`.
3. Depuis le terminal, allez dans le _repository_ que vous venez de télécharger avec la commande `cd`.
4. Exécutez la commande : `mysql -u root -p < ./employees.sql` (le mot de passe est souvent `root` par défaut)

### Énoncé de TP

Dans ce TP, nous allons travailler sur la base de données représentée par le schéma suivant :

<p align="center">
	<img src="https://github.com/datacharmer/test_db/blob/master/images/employees.png" width="70%">
</p>

