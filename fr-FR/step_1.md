Lorsque ton utilisateur accède à une autre page (ou recharge la page en cours), toutes les modifications qu'il a apportées sont perdues.

Tu peux conserver les choix de l'utilisateur avec la propriété `localStorage`.

`localStorage` contient les données comme paires clé-valeur. Une **clé** est un 'label' pour une valeur.

### Méthodes localStorage

- setItem(key, value):
  Ajoute une paire clé-valeur à localStorage.
  Exemple : `localStorage.setItem("nom d'utilisateur", "raspberry")`

- getItem(key):
  Récupère la valeur associée à la clé spécifiée.
  Exemple : `var username = localStorage.getItem("nom d'utilisateur")`

- removeItem(key):
  Supprime la paire clé-valeur associée à la clé spécifiée.
  Exemple : `localStorage.removeItem("nom d'utilisateur")`

- clear():
  Supprime toutes les paires clé-valeur de localStorage.
  Exemple : `localStorage.clear()`

### Vérifier localStorage lors du chargement d'une page

Tu peux utiliser `.addEventListener` pour déclencher une fonction en réponse à un événement de chargement de page.

Voici un exemple provenant du projet Personnage de Comics du parcours Plus de web :

--- code ---
---
language: js
---

document.addEventListener("DOMContentLoaded", function () {    
  
  if (localStorage.getItem("lightMode") == "true") {
    document.body.classList.toggle("light-mode");
    lightModeSwitch.checked = true;
  }

});
      
--- /code ---

`"DOMContentLoaded"` est un `eventType` qui est déclenché lorsque la page web est prête.

**Astuce :** il est préférable d'utiliser `"DOMContentLoaded"` ici plutôt que le type d'événement `"load"`, qui n'est déclenché que lorsque toutes les images sont chargées.
