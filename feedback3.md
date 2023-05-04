# oclockevaluation

Première observation : Ajouter le fichier .htaccess pour rediriger vos requêtes vers le fichier "index.php" sinon, votre page d'accueil ne s'affichera pas.

2ème observation : Vous devez protéger vos routes en créant une classe ou une méthode pour gérer les autorisations à ces routes.

3ème observation : Vous devez structurer votre template La structuration de vos vues vous permet d'éviter la repetition des codes HTML communs à toutes les pages de votre application
Tout d'abord, vous devez créer un dossier contenant votre squelette HTML qui sera commeun à toutes les pages de votre application. On appelle souvent ce dossier "layout" et peut être sauvegardé à la racine du dossier "app/views/".

Dans ce dosssier "layout", vous allez créer les fichiers header.html , footer.html, nav.html,... bref tous les fichiers communs à votre application.

Lorsque nous verrons les cours sur le framework Laravel, ce concept des layouts et heritage sera encore abordé.

4ème observaation : Vous n'avez pas implementé la route '/' au niveau de la description de vos routes. Sans cette route, on ne peut acceder à la page d'accueil de votre site.
