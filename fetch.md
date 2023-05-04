# oclockevaluation


Fetch Javascript permet d'envoyer des requêtes réseau au serveur et charger de nouvelles informations. 
Par exemple, nous pouvons faire uen requête pour enregistrer des données, mettre à jour, chercher des informations, charger des informations sans que cela recharge la page.
Vous devez ajouter la proprité onclick au niveau du bouton submit. EXEMPLE : <button type="submit" onclick="submit()" class="btn btn-primary btn-block mt-5">Valider</button>

Ce scritp permet d'ajouter un étudiant sans charger toute la page.
<script>
  async function submit(){
     var firstname =document.getElementById("firstname").value; 
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
