Hello "Apprenant_fetch" !

`fetch()` en JS est une fonction qui te permet d'envoyer des requêtes HTTP vers des serveurs et de récupérer les données renvoyées.

Lorsque tu utilises fetch, tu dois fournir une URL pour spécifier l'endroit où tu veux envoyer ta requête. 
(Cette URL peut inclure des informations sur le type de données que tu souhaites obtenir ou envoyer.)

Une fois que tu as envoyé ta requête avec fetch, tu peux utiliser les méthodes de réponse pour traiter les données renvoyées par le serveur. Par exemple, tu peux convertir la réponse en JSON pour la manipuler plus facilement dans ton code.

Fetch utilise une approche basée sur les promesses, ce qui signifie qu'il te permet d'utiliser des méthodes comme `.then()` et `.catch()` pour gérer la réponse de manière asynchrone. Cela te permet d'effectuer des actions spécifiques en fonction du succès ou de l'échec de la requête.

_Ces sections expliquent bien le concept je trouve :_
- https://fr.javascript.info/fetch
- https://www.digitalocean.com/community/tutorials/how-to-use-the-javascript-fetch-api-to-get-data-fr

---
_Un exemple simple :_ 

```
fetch("https://www.une-url.com")
.then(response => response.json())
.then(response => alert(JSON.stringify(response)))
.catch(error => alert("Erreur : " + error));
```

Comme je te disais plus haut, la méthode `fetch()` a besoin d’un argument obligatoire, qui correspond à l’URL des ressources à récupérer.

`fetch()` retourne ensuite une promesse contenant la réponse (si tout se passe bien). On ne peut pas exploiter la réponse renvoyée dans cette promesse en l’état : il faut indiquer le format de réponse souhaité. Ici, on choisit `JSON` avec `response.json()`.

`response.json()` renvoie également une promesse contenant la réponse à ta demande en JSON. On utilise `JSON.stringify()` pour transformer notre objet JSON en une chaine ( et ici on l'affiche avec un petit `alert()` ).

Et enfin, on traite les erreurs avec le bloc `catch` et on affiche l’erreur rencontrée si on en rencontre une.

----

N'hésites pas à me solliciter si tu as la moindre question à ce sujet :wink:

