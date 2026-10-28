# Docenthandleiding - Merge Conflict Lab

## Doelgroep en leerdoelen

Voor beginnende HBO-ICT-studenten die al weten wat branches en commits zijn. De les focust uitsluitend op inhoudelijke Git merge-conflicten. Er is voor de website geen Git-installatie nodig.

Na afloop kan de student:

1. een conflict herkennen via Git-uitvoer, git status en markers;
2. uitleggen wat HEAD, ======= en de inkomende branch betekenen;
3. een oplossing kiezen vanuit de bedoelde werking;
4. markers verwijderen, code inhoudelijk samenvoegen en testen;
5. afronden met git add en git commit of git merge --continue.

## Bewijs van leren

Een student laat beheersing zien wanneer die alle vijf missies voltooit, in missie 4 “limit = 30” combineert met “participants.length < limit”, de tests uitvoert en in de afsluitcheck uitlegt waarom “Accept Current” niet automatisch veilig is.

Voortgang blijft alleen in de browser. Laat studenten hun eindsamenvatting tonen of als pdf bewaren.

## Lesopzet (75 minuten)

| Tijd | Docent | Studenten | Formatieve informatie |
|---|---|---|---|
| 0-7 min | Toon alleen de foutmelding uit de hero. Vraag: “Is Git stuk?” | Eerst voorspellen, dan in de chat reageren. | Voorkennis over status en foutmeldingen. |
| 7-12 min | Bespreek leerdoelen; demonstreer nog geen oplossing. | Lezen de missiebriefing. | Gewenst eindgedrag is duidelijk. |
| 12-22 min | Laat missies 1 en 2 doen. Vraag: “Van welke branch is HEAD?” | Herkennen en ontleden. | Spoor “HEAD = feature-branch” op. |
| 22-32 min | Maak breakout-duo’s. Laat studenten vóór het klikken argumenteren. | Vergelijken de wijzigingen in missie 3. | Redeneren ze vanuit bedoeling? |
| 32-47 min | Laat missie 4 doen. Geef vooraf geen inhoudelijke hint; laat falende tests het gesprek starten. | Herschrijven, testen en gericht verbeteren. | “Markers weg” is nog geen werkende merge. |
| 47-55 min | Laat missie 5 individueel doen. | Reconstrueren de procedure zonder steun. | Retrieval practice. |
| 55-65 min | Geef een klein conflict uit het eigen project. | Passen de vijf stappen toe. | Transfer naar professionele context. |
| 65-72 min | Laat de afsluitcheck invullen en in duo’s toelichten. | Verwoorden beslisregel en kwaliteitscheck. | Begripscontrole en peerfeedback. |
| 72-75 min | Vat de stappen samen. | Delen één inzicht. | Exit-check. |

## Didactische keuzes

- **Constructive alignment:** doelen, missies en afsluitcheck vragen hetzelfde handelen.
- **Scaffolding en fading:** meerkeuze en koppelen → oplossingen beoordelen → zelfstandig code bewerken → procedure reconstrueren.
- **Eerst denken:** de perfecte oplossing verschijnt niet vooraf. Feedback expliciteert de redenering pas na een poging.
- **Cognitive load:** één hoofdtaak per missie; rebase, GitLab-inrichting en complexe strategieën zijn weggelaten.
- **Formatief handelen:** feedback benoemt de beslissende aanwijzing of grensvoorwaarde.
- **Transfer:** sluit af met een conflict uit het eigen studentenproject.

## Antwoorden

### Missie 1

“both modified: register.js” onder “Unmerged paths”. Een bestand onder “Changes not staged” is niet automatisch conflicterend.

### Missie 2

Boven de scheidslijn staat de huidige branch (main); eronder de inkomende branch; HEAD wijst naar de huidige positie toen de merge startte.

### Missie 3 en 4

Correcte kern:

~~~js
const limit = 30;
return participants.length < limit;
~~~

Bij 30 aanwezige deelnemers mag niemand meer inschrijven. De vergelijking “<= 30” zou deelnemer 31 toelaten.

### Missie 5

1. git status;
2. beide versies lezen en bedoeling bepalen;
3. code bewerken en markers verwijderen;
4. volledige applicatie testen;
5. git add <bestand>;
6. git commit of git merge --continue.

Git merge --abort is een geldige uitweg als de merge niet moet doorgaan, maar geen stap in de normale afronding.

## Misconcepties en feedforward

- **“HEAD is altijd mijn feature-branch.”** Vraag: “Op welke branch stond je toen je merge uitvoerde?”
- **“Accept Both lost het op.”** Laat de resulterende code regel voor regel traceren.
- **“Als de markers weg zijn, is het klaar.”** Laat eerst een grensgeval voorspellen en dan testen.
- **“De inkomende branch is nieuwer, dus beter.”** Vraag welk productbesluit iedere regel ondersteunt.
- **“Git bepaalt welke code juist is.”** Git voegt tekst samen; het kent de bedoeling niet.

## Online begeleiding en differentiatie

Laat vóór ieder antwoord 30-60 seconden individueel denken. Gebruik breakout-duo’s bij missie 3: student A verdedigt HEAD, student B de inkomende versie; daarna ontwerpen ze samen het eindresultaat. Vraag bij vastlopen naar huidige branch, bedoelde werking en bewijs dat de oplossing werkt.

Snelle studenten schrijven twee extra grensgevallen of ontwerpen een tweede conflict. Studenten die steun nodig hebben, krijgen tijdelijk de stappenkaart uit de debrief; neem die bij missie 5 weer weg.

## Techniek, privacy en toegankelijkheid

De site heeft geen backend of externe bibliotheken. Voortgang staat alleen in localStorage; er worden geen persoonsgegevens verstuurd. De pagina ondersteunt toetsenbordbediening, zichtbare focus, tekstuele feedback, responsive weergave en gereduceerde beweging.

## Bronnen

- Aangeleverde presentatie *Sprint 1 HBO-ICT x Studiekiezers - online les - Retrospective, merging en mergeconflicts*, slides 17-23.
- Git merge, “How to resolve conflicts”: https://git-scm.com/docs/git-merge#_how_to_resolve_conflicts
- Pro Git, “Basic Merge Conflicts”: https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging#_basic_merge_conflicts
- Git gitattributes, conflictmarkers: https://git-scm.com/docs/gitattributes#_built_in_merge_drivers

