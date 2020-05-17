# Bases de Données Relationnelles

## TP3 - Algèbre Relationnelle

Soit la base de données relationnelle définie par les relations suivante :

__Person(<ins>Id_Person</ins>, Firstname, Lastname, Birthdate, Sex, Nationality)__<br>
__Character(<ins>Id_Character</ins>, #Id_Movie, #Id_Person, Firstname, Lastname)__<br>
__Movie(<ins>Id_Movie</ins>, Title, Year, Duration, Nationality, #Director__ *ref. Person.Id_Person*__)__<br>
__Movie_Genre(<ins>#Id_Movie, #Id_Genre</ins>)__<br>
__Genre(<ins>Id_Genre</ins>, Name)__

### Requêtes

En utilisant l'algèbre relationnelle, donnez une expression algébrique pour chacune des requêtes suivantes, ainsi que l'arbre algébrique correspondant.

1. Donnez tous les genres (tous les attributs).
2. Donnez le titre ainsi que leur année de sortie de tous les films.
3. Donnez la liste des réalisateurs (prénom et nom) ayant sorti des films après 2015.
4. Donnez le nom des genres du film "Imitation Game".
5. Donnez le nom et le prénom de tou.te.s les acteur.rice.s ayant joué dans le film _"Pirates of Silicon Valley"_, en précisant le rôle dans lequel ils/elles ont joué.
6. Donnez la liste des acteur.rice.s ayant déjà joué dans un film avec 
7. Donnez la liste des acteur.rice.s ayant joué à la fois dans _"Imitation Game"_ et dans "The Social Network"_.
