# oclockevaluation

**1ère observation :**  Controlleur pour gérer les erreurs et la page home.


Vous n'avez pas implementer plusieurs controllers, notamment le controller pour gérer les erreurs. C'est très important que l'utilisateur sache ce qui se passe sur votre site.
La gestion des erreurs vous permet aussi de maintenir rapidement son site.

Le controlleur pour gérer l'affichage de la page "home" est inexistant. Sachez que les controlleurs sont au coeur de vos applications. Ce sont eux qui traitent les requêtes et les formulaires.


**2ème observation :** Pas de structuration de vos vues.


Vous devez structurer votre template La structuration de vos vues vous permet d'éviter la repetition des codes HTML communs à toutes les pages de votre application Tout d'abord, vous devez créer un dossier contenant votre squelette HTML qui sera commeun à toutes les pages de votre application. On appelle souvent ce dossier "layout" et peut être sauvegardé à la racine du dossier "app/views/".

Dans ce dosssier "layout", vous allez créer les fichiers header.html , footer.html, nav.html,... bref tous les fichiers communs à votre application.

Lorsque nous verrons les cours sur le framework Laravel, ce concept des layouts et heritage sera encore abordé.


**3ème observation:** Votre méthode students() du controlleur StudentsController est mal écrite.

**4ème observation :** problème de redirection 
Pour gérer ce problème, Vous devez ajouter dans votre dossier "public" le fichier ".htaccess" pour rediriger toutes les requêtes vers le fichier "index.php". Le fichier ".htaccess" est un fichier texte qui permet de modifier certains paramètres du serveur apache. Ce fichier est utilisé pour réécrire les URL, contrôler l'accès à un repertoire ou un fichier.

Sachez que vous devez activez la réécriture d'URL sur votre serveur pour rediriger les requêtes vers le fichier "index.php".

Pour activer la fonctionnalité Apache de réécriture d'URL. Ajouter "RewriteEngine On" en debut du fichier .htaccess


**5ème observation: Veuillez revoir vos notions de Modèle Vue Controller.** 
