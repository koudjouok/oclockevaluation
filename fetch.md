# oclockevaluation


**Fetch Javascript** permet d'envoyer des requêtes réseau au serveur et charger de nouvelles informations. 
Par exemple, nous pouvons faire une requête pour enregistrer des données, mettre à jour, chercher des informations, charger des informations sans que cela recharge la page.
La syntaxe de base est : let promise = fetch(url, [options])
  url – l’URL cible, ça peut être une API.
  options – paramètres facultatifs : méthode, en-têtes, etc…
  
Sans options, c’est une simple requête GET, téléchargeant le contenu de l’url.
Le navigateur démarre la requête immédiatement et renvoie une promesse que le code appelant devrait utiliser pour obtenir le résultat.

Obtenir une réponse est généralement un processus en deux étapes.
*Premièrement, la promise, renvoyée par fetch, se résout avec un objet de la classe intégrée Response dès que le serveur répond avec des en-têtes.
*Deuxièmement, pour obtenir le corps de la réponse, nous devons utiliser un appel de méthode supplémentaire.

**EXEMPLE** 
Vous devez ajouter la proprité onclick au niveau du bouton submit. EXEMPLE : <button type="submit" onclick="submit()" class="btn btn-primary btn-block mt-5">Valider</button> **onclick** exécute une certaine fonctionnalité quand un bouton est cliqué. Cela peut être quand un utilisateur soumet un formulaire, quand vous changez un certain contenu sur la page web ou d'autres choses du style. Dans notre cas, il va éxecuter la fonction submit() definit dans nortre script.

Nous devons utiliser les options fetch :
*method – HTTP-method, par exemple POST,
*body – le corps de la requête, un parmi ceux-ci :une chaîne de caractères (par exemple encodé en JSON),un objet FormData, pour soumettre les données en tant que multipart/form-data,

Le format JSON est utilisé la plupart du temps.
Ce scritp permet d'ajouter un étudiant sans charger toute la page.
Pour écrire un script javascript, vous devez le faire entre les balises <script> et </script>

<script>
  async function submit(){
     var firstname =document.getElementById("firstname").value;  **on recupère la valeur du champ firstname via ID. id de ce champ est "firstname"
     var lastname =document.getElementById("lastname").value;
    var teacher =document.getElementById("teacher").value; 
   var status =document.getElementById("status").value;
  
  let students={
    firstname:firstname,
    lastname:lastname,
    teacher:teacher,
    status:status,
  }
  
  let response = await('/students/add',{
    methode='POST',
    headers={
    'Content-Type':'application/json; charset=utf-8'
  }
  body:JSON.Stringify(students)
  });
  
  let result=await response.json();
  alert(result.message);
  }
</script>

Au niveau du controlleur, faut renvoyer en format JSON. EXEMPLE : response()->json('message'=>'Etudiant ajouté avec succès');
