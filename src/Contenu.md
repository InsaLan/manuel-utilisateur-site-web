# Contenu du site 
Certains éléments du site peuvent être modifiés directiement depuis l'interface
back-office. Ce chapitre présente et détaille les constantes et contenus
déjà implementés sur le site.

## Comment le CMS marche

Le CMS, ou Content System Management, est un morceau de l'API du site développé
afin de rendre dynamique certaines parties du site de l'insalan, sensible aux changements.

On distingue pour le moment 2 types de ressources: les **constantes** et les **contenus**

### Les constantes

Une constante sur le site est définie comme un élément dynamique court et qui peut changer souvent. 
Par exemple, le nom des responsables ou les dates de l'insaLan. une constante doit être défini par 
son **nom** et sa **valeur**. Une constante peut être référencée dans un contenu 
en utilisant la syntaxe `${nom_de_la_constante}`.
#### Liste des constantes

Les constantes définies sur le site actuellement sont les suivantes:

- __date_insalan__: date de la prochaine insalan.
- __contact_insalan__: contact à privilégié pour contacter l'association. 
- __resp_tournoi__: coordonnées de la personne responsable des tournois.
- __resp_partos__: coordonnées de la personne en charge des partenariats.
- __tresorerie__: coordonnées de la personne en charge de la trésorerie.

### Les contenus

Un contenu sur le site est définie comme un texte d'une longueur arbitraire sur le site.
Ce texte peut être rédigé en [Markdown](https://commonmark.org/) et faire référence à 
des constantes definies. Le back-office du site vérifie à la publication d'un contenu
que toutes les constantes utilisées sont bien définies.

#### Liste des contenus

Les contenus définis sur le site actuellement sont les suivants:
- __main_content__: Contenu à afficher sur la page principale d'accueil (route `/`)
- __informations__: Contenu à afficher sur la page information (route `/info`)
- __contact__: Contenu à afficher sur la page information, à la suite de la carte d'accès (route `/info`)
- __cgu__:  Contenu à afficher sur la page "Conditions Générales d'Utilisation" (route `/cgu`)
- __association__: Contenu à afficher sur la page "Association" (route `/association`)


