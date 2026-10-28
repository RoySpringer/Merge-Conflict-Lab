# Merge Conflict Lab

Buildless oefenwebsite voor een online ICT-les over Git merge-conflicten. De site gebruikt alleen HTML, CSS en JavaScript.

## Lokaal bekijken

Open index.html rechtstreeks, of start in deze map:

~~~bash
python3 -m http.server 8000
~~~

Open daarna http://localhost:8000.

## Publiceren met GitHub Pages

1. Maak een GitHub-repository, bijvoorbeeld merge-conflict-lab.
2. Zet de **inhoud van deze map** in de hoofdmap van de repository; index.html staat dan direct op rootniveau.
3. Commit en push naar main.
4. Ga op GitHub naar **Settings → Pages**.
5. Kies **Deploy from a branch**.
6. Selecteer **main** en **/(root)** en klik **Save**.
7. De URL wordt https://<gebruikersnaam>.github.io/merge-conflict-lab/.

Er is geen buildstap, package manager, database of geheime sleutel nodig.

## Inhoud

- index.html: les en oefeningen;
- challenge.html: uitdagende vervolgroute;
- style.css: responsive ontwerp en printweergave;
- app.js: feedback en lokale voortgang;
- challenge.css en challenge.js: vormgeving, tests en voortgang van de vervolgroute;
- DOCENTHANDLEIDING.md: lesplan, antwoorden en misconcepties;
- .nojekyll: voorkomt Jekyll-verwerking.

Voortgang staat alleen in localStorage en kan met **Wis mijn voortgang** worden verwijderd. Doorloop na wijzigingen alle vijf missies en de vier uitdagende dossiers op desktop en mobiel.

