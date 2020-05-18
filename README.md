# Bases de Données Relationnelles

## TP3 - Algèbre Relationnelle

Soit la base de données relationnelle définie par les relations suivante :

__Person(<ins>id_person</ins>, firstname, lastname, birthdate, sex, nationality)__<br>
__Character(<ins>id_character</ins>, #id_movie, #id_person, firstname, lastname)__<br>
__Movie(<ins>id_movie</ins>, title, year, duration, nationality, #director__ *ref. Person.id_person*__)__<br>
__Movie_Genre(<ins>#id_movie, #id_genre</ins>)__<br>
__Genre(<ins>id_genre</ins>, name)__

### Requêtes

En utilisant l'algèbre relationnelle, donnez une expression algébrique pour chacune des requêtes suivantes, ainsi que l'arbre algébrique correspondant.

1. Donnez tous les genres (tous les attributs).
2. Donnez le titre ainsi que leur année de sortie de tous les films.
3. Donnez la liste des réalisateur.rice.s (prénom et nom) ayant sorti des films après 2015.
4. Donnez le nom des genres du film "Imitation Game".
5. Donnez le nom et le prénom de tou.te.s les acteur.rice.s ayant joué dans le film _"Pirates of Silicon Valley"_, en précisant le rôle dans lequel ils/elles ont joué.
6. Donnez la liste des acteur.rice.s ayant joué à la fois dans _"Imitation Game"_ et dans _"The Social Network"_.
7. Donnez la liste des acteur.rice.s ayant déjà joué dans un film avec _Kaira Knightley_, mais pas avec _Benedict Cumberbatch_.
8. Donnez pour chaque réalisateur.rice, la liste des genres dont il/elle n'a réalisé aucun film.
