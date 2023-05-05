# L'application ne renvoie pas à la page d'accueil.

Pour gérer ce problème, Vous devez ajouter dans votre dossier **public** le fichier **.htaccess** pour rediriger toutes les requêtes vers le fichier **index.php**. 
Le fichier **.htaccess** est un fichier texte qui permet de modifier certains paramètres du serveur apache.  Ce fichier est utilisé pour réécrire les URL, contrôler l'accès à un repertoire ou un fichier,...

Sachez que vous devez activez la réécriture d'URL sur votre serveur pour rediriger les requêtes vers le fichier **index.php**.


**Pour activer la fonctionnalité Apache de réécriture d'URL. Ajouter "RewriteEngine On" en debut du fichier .htaccess





