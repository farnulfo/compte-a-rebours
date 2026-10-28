# À bientôt — Compte à rebours

Page statique autonome en français, sans dépendance, backend, cookie ni stockage local. Tous les paramètres figurent dans l’URL : `?title=Vacances&end=2027-07-01T12%3A00%3A00.000Z`.

L’option « Exclure les week-ends » ajoute `weekdays=1` et `tz=Europe%2FParis` (par exemple) au lien. Les heures du samedi et du dimanche sont ignorées selon ce fuseau, conservé pour tous les visiteurs. Le décompte est en pause pendant le week-end ; un jour affiché représente 24 heures comptées. Les changements d’heure sont pris en compte. Les jours fériés restent comptés. La date de fin reste inchangée, même si elle tombe un week-end ; dans ce cas, le temps compté peut atteindre zéro avant la date de fin.

Ouvrir `index.html` dans un navigateur, choisir un titre et une date, puis créer le compte à rebours. Le bouton « Copier le lien » permet de le partager. Le titre est limité à 200 caractères. Une date passée affiche zéro et « Le moment est arrivé ! ».

L’option « Ajouter une date de début de projet » ajoute le paramètre UTC `start` à l’URL. Le début doit précéder la fin. Une fusée indique la proportion du temps écoulé et restant entre ces deux dates. Avant le début, la progression reste à 0 % et le compteur affiche la durée du projet ; après la fin, la progression atteint 100 %. Avec les week-ends exclus, la durée et la progression sont calculées sur les mêmes heures du lundi au vendredi. Si toute la période tombe un week-end, le compteur reste à zéro et la progression passe de 0 à 100 % à la date de fin. Sans date de début, le compte à rebours conserve son fonctionnement habituel.

La saisie utilise le fuseau horaire du navigateur. La date est convertie en UTC dans le lien : tous les visiteurs comptent jusqu’au même instant. L’affichage de la date reste dans le fuseau du visiteur. Le décompte utilise l’horloge de son appareil.

## Hébergement sur GitHub Pages

1. Placer `index.html` à la racine du dépôt GitHub et l’envoyer sur la branche `main`.
2. Dans les paramètres du dépôt, ouvrir **Pages**, choisir **Deploy from a branch**, puis **main** et **/ (root)**, et enregistrer.
3. Ouvrir l’adresse fournie par GitHub et y créer le compte à rebours à partager.

Aucune compilation ni configuration supplémentaire n’est nécessaire. Les liens fonctionnent aussi sous un chemin de dépôt (`https://utilisateur.github.io/depot/`).

Les paramètres sont visibles dans l’URL et accessibles à toute personne possédant le lien. L’application n’enregistre rien, mais le navigateur et l’hébergeur peuvent conserver l’URL dans leur historique ou leurs journaux.
