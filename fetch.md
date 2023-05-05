# oclockevaluation


**Fetch Javascript** permet d'envoyer des requêtes réseau au serveur et charger de nouvelles informations. 
Par exemple, nous pouvons faire une requête pour enregistrer des données, mettre à jour, chercher des informations, charger des informations sans que cela recharge la page.
La syntaxe de base est : let promise = fetch(url, [options])
   url – l’URL cible, ça peut être une API.
  2.options – paramètres facultatifs : méthode, en-têtes, etc…
  
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




## Table of Contents
1. [General Info](#general-info)
2. [Technologies](#technologies)
3. [Installation](#installation)
4. [Collaboration](#collaboration)
5. [FAQs](#faqs)
### General Info
***
Write down the general informations of your project. It is worth to always put a project status in the Readme file. This is where you can add it. 
### Screenshot
![Image text](https://www.united-internet.de/fileadmin/user_upload/Brands/Downloads/Logo_IONOS_by.jpg)
## Technologies
***
A list of technologies used within the project:
* [Technologie name](https://example.com): Version 12.3 
* [Technologie name](https://example.com): Version 2.34
* [Library name](https://example.com): Version 1234
## Installation
***
A little intro about the installation. 
```
$ git clone https://example.com
$ cd ../path/to/the/file
$ npm install
$ npm start
```
Side information: To use the application in a special environment use ```lorem ipsum``` to start
## Collaboration
***
Give instructions on how to collaborate with your project.
> Maybe you want to write a quote in this part. 
> It should go over several rows?
> This is how you do it.
## FAQs
***
A list of frequently asked questions
1. **This is a question in bold**
Answer of the first question with _italic words_. 
2. __Second question in bold__ 
To answer this question we use an unordered list:
* First point
* Second Point
* Third point
3. **Third question in bold**
Answer of the third question with *italic words*.
4. **Fourth question in bold**
| Headline 1 in the tablehead | Headline 2 in the tablehead | Headline 3 in the tablehead |
|:--------------|:-------------:|--------------:|
| text-align left | text-align center | text-align right |
