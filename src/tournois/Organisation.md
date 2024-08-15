# Organisation

Le site de l'insalan et particulièrement la partie tournois est décomposé en
plusieurs parties entreconectées. Beaucoup de ces parties nécéssites une
définition et possèdent des limites au niveau de l'implémentation. En cas de
modification plus poussée que décrite dans cette documentation, il est
recommandé de contacter l'équipe dev pour planifier une amélioration du site.
N'hésitez pas ! C'est comme ça qu'on peut vous aider au mieux !

Pour la gestion des tournois, tout se fait depuis le panel admin du site. Il est
accessible depuis le menu de navigation en haut à droite si vous êtes connecté
en tant que membre de l'association (faîtes valider votre compte par un membre
de l'équipe dev si ce n'est pas déjà fait). Une fois sur le panel admin, vous
devriez avoir une section "Tournois" qui vous permettra de gérer les tournois et
les équipes.

![Panel admin tournois](../assets/images/admin-tournois.png)

## Événements

Un événement est une entité regroupant plusieurs tournois. Chaque itération de
l'insalan est considéré comme un événement. Pour l'instant seulement les
éditions sont représentable sur le site mais il est prévu (possiblement dans un
futur lointain) de pouvoir utiliser le site pour des tournois en mini.

Pour lister les événements, il suffit de se rendre sur la [page
correspondate](https://api.insalan.fr/v1/admin/tournament/event/) du panel
admin. Pour en créer un nouveau, il suffit de cliquer sur le bouton "Ajouter
événement" en haut à droite de la page. Un certain nombre d'information vous
sera demandé.

Parmis ces informations, certaines ont besoin d'explications : 
- Le champ "En cours" permet de définir si l'événement est actif ou non. Si
  l'événement est actif, les tournois associés seront affichés sur la page
  d'accueil du site en tant qu'événement courant. Sinon, il sera accessible dans
  la section archives.
- Le champ "Siège" contient un espace pour définir le plan de la Halle. Vous
  aurez besoin d'un petit peu d'esprit artistique pour représenter les tables
  sous forme de pixels. Pour plus d'exemple, vous trouverez un exemple (édition
  XVIII) ci dessous. Il n'est pas nécessaire de respecter les distances.
  Seulement de pouvoir reconnaître les groupes de tables.

![Plan Insalan XVIII](../assets/images/insalanXVIII.png) ![Pixel
XVIII](../assets/images/pixelXVIII.png)

Ces informations peuvent être changées à tout moment en cliquant sur le numéro
du tournois dans le panel admin.

## Jeux

Bon, vous allez peut-être avoir du mal à me croire mais les jeux présent lors de
la LAN sont appelés "jeux" dans le panel admin. C'est fou non ? De la même
manière que les évenement et si vous l'avez compris vous n'allez pas être
dépaysé par la suite, vous pouve les lister sur la [page
correspondante](https://api.insalan.fr/v1/admin/tournament/game/). Pour en
ajouter un, il suffit de cliquer sur le bouton "Ajouter jeu" en haut à droite de
la page. Les informations à remplir sont relativement simples et ne nécessitent
pas d'explications supplémentaires. Pour les différentes validations de nom,
cela doit être implémenté dans le code du site. Si vous avez besoin d'ajouter un
jeu, contactez l'équipe dev.

## Tournois

Un tournois est l'intersection entre un événement et un jeu. C'est plus ou moins
l'entité principale du site. Je ne vais pas revenir sur la manière de lister ou
ajouter un nouveau tournois, vous avez compris le principe. Par contre, il y a
quelques informations à savoir sur les tournois.

Un événement non annoncé apparaîtra sous forme d'un point d'interrogation sur la
page d'accueil du site. Aucun détail ne sera affiché et il ne sera pas possible
de s'inscrire. 

La description d'un tournois peut contenir du markdown, un format de texte qui
permet de mettre en forme le texte. Vous pouvez trouver plus d'informations sur
le markdown [ici](https://commonmark.org/). Il est vivement conseillé de
s'inspirer du règlement de l'édition précédente pour ne pas avoir à tout
réécrire.

Les dates d'inscription et de début de tournois sont des dates importantes. Les
joueurs ne pourront pas s'inscrire avant la date d'ouverture et ne pourront plus
s'inscrire après la date de fermeture. Il faut donc être attentif à ces dates
pour éviter des problèmes.

Le champ logo est l'image du tournois. Il est conseillé de mettre une image de
format vidéo (16:9) pour un meilleur rendu sur le site. Il est également
important de vérifier les droits d'utilisation de l'image avant de la mettre en
ligne. Afin d'améliorer le chargement du site, le format webp est privilégié. Si
vous ne savez pas comment convertir une image en webp, contactez l'équipe dev.

Les différents prix de l'inscription ne sont pas sans importance. Faîtes
attention, cela déterminera le prix de l'inscription en ligne. Ces prix doivent
être définis par le bureau en fonction du nombre de place et du budget
prévisionnel.

Le cashprize est une information importante pour les joueurs. Si le cashprize
n'a pas encore été défini, vous pouvez laisser le champ vide. L'affichage du
cashprize sur le site est automatique. Sinon, Ce champ doit contenir 3 valeurs
séparées par des virgules. La première valeur est le cashprize pour le premier,
la deuxième pour le deuxième et la troisième pour le troisième.

Les différents "produits" n'ont pas à être touchés, ils seront créés
automatiquement lors de la création du tournois. Si vous avez besoin de modifier
les produits, contactez l'équipe dev.

Le reste devrait être un jeu d'enfant et vous devriez avoir de jolis tournois sur la page d'accueil du site.

![Accueil du site](../assets/images/website.png)

