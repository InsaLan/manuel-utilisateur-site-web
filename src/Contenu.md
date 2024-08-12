# Contenu du site 
Certains éléments du site peuvent être modifiés directiement depuis l'interface
back-office. Ce chapitre présente et détaille les constantes et contenus déjà
implementés sur le site.

Les constantes et contenus doivent êtres vérifiés et changés chaque année pour
s'assurer que les informations affichées sur le site sont à jour.

## Fonctionnement du CMS

Le CMS, ou Content System Management, est un morceau du site l'insalan développé
afin de rendre dynamique certaines parties, sensibles aux changements.

On distingue pour le moment 2 types de ressources: les **constantes** et les
**contenus**.

### Les constantes

Une constante sur le site est définie comme un élément dynamique court et qui
peut changer souvent. Par exemple, le nom des responsables ou les dates de
l'insaLan. une constante doit être défini par son **nom** et sa **valeur**. Une
constante peut être référencée dans un contenu en utilisant la syntaxe
`${nom_de_la_constante}`.
#### Liste des constantes

Les constantes définies sur le site sont disponibles depuis le [back-office du
site](https://api.insalan.fr/v1/admin/cms/constant/).

### Les contenus

Un contenu sur le site est définie comme un texte d'une longueur arbitraire sur
le site. Ce texte peut être rédigé en [Markdown](https://commonmark.org/) et
faire référence à des constantes definies. Le back-office du site vérifie à la
publication d'un contenu que toutes les constantes utilisées sont bien définies.

#### Liste des contenus

Les contenus définis sur le site sont disponibles depuis le [back-office du
site](https://api.insalan.fr/v1/admin/cms/content/).


