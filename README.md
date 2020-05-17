# Bases de Données Relationnelles

## TP3 - Algèbre Relationnelle

Soit la base de données relationnelle définie par les relations suivante :

__Person(<ins>Id_Person</ins>, Firstname, Lastname, Birthdate, Sex, Nationality)__<br>
__Cast(<ins>#Id_Movie, #Id_Person</ins>, Role)__<br>
__Movie(<ins>Id_Movie</ins>, Title, Year, Duration, Nationality, #Id_Director ref. Person.Id_Person)__<br>
__Movie_Genre(<ins>#Id_Movie, #Id_Genre</ins>)__<br>
__Genre(<ins>Id_Genre</ins>, Nom)__
