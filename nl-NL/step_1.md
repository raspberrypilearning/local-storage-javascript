When your user navigates to another page (or reloads the current one), any changes they have made will be lost.

Je kunt de keuze van de gebruiker behouden met de `localStorage` eigenschap.

`localStorage` houdt gegevens vast als sleutel-waardeparen. A **key** is a 'label' for a value.

### localStorage methoden

- setItem(key, value):
  Voegt een sleutel-waardepaar toe aan localStorage.
  Voorbeeld: `localStorage.setItem("gebruikersnaam", "raspberry")`

- getItem(key):
  Haalt de waarde op die aan de opgegeven sleutel is gekoppeld.
  Voorbeeld: `var gebruikersnaam = localStorage.getItem("gebruikersnaam")`

- removeItem(key):
  Verwijdert het sleutel-waardepaar dat aan de opgegeven sleutel is gekoppeld.
  Voorbeeld: `localStorage.removeItem("gebruikersnaam")`

- clear():
  Verwijdert alle sleutel-waardeparen uit localStorage.
  Voorbeeld: `localStorage.clear()`

### LocalStorage controleren wanneer een pagina wordt geladen

Je kunt `.addEventListener` gebruiken om een functie te activeren als reactie op een pagina laden gebeurtenis.

Hier is een voorbeeld van het Stripfiguur project in het Meer web pad:

## --- code ---

## language: js

document.addEventListener("DOMContentLoaded", function () {

if (localStorage.getItem("lightMode") == "true") {
document.body.classList.toggle("light-mode");
lightModeSwitch.checked = true;
}

});

\--- /code ---

`"DOMContentLoaded"` is een `eventType` dat wordt geactiveerd wanneer de webpagina klaar is.

**Tip:** Het is beter om hier `"DOMContentLoaded"` te gebruiken in plaats van het eventType `"load"`, dat alleen wordt geactiveerd wanneer alle afbeeldingen zijn geladen.
