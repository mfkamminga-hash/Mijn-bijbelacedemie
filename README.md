# 📖 Onze Bijbelacademie

Zelfstandige statische website voor volwassen Bijbelstudie: 53 lessen in zes modules, 159 toetsvragen, 10 discussielessen met 30 oefengesprekstappen, 106 begrippen, eigen argumentenboek, lokale voortgang, JSON-back-up en apparaatgestuurde voorleesfunctie.

## Lokaal gebruiken

Open `dist/index.html`, of serveer de map `dist` met een statische webserver. Geen build, externe JavaScriptbibliotheken, API-sleutel of betaalde audiodienst nodig. Bij openen als lokaal bestand verschilt ondersteuning voor browseropslag per browser; hosting via HTTPS heeft de voorkeur.

## GitHub Pages

1. Maak onder `mfkamminga-hash` een nieuwe repository `Mijn-Bijbelacademie`.
2. Upload de **inhoud** van `dist` in de hoofdmap van de nieuwe repository. `index.html`, `app.js`, `data.js`, `styles.css` en `assets` moeten naast elkaar staan. Voeg `.nojekyll` toe.
3. Kies Settings → Pages → Deploy from a branch → main → /(root) → Save.
4. GitHub meldt de definitieve Pages-URL nadat de publicatie voltooid is.

Wijzig geen bestaande cursusrepository of gezinsplanner. De huidige gehoste Sites-versie gebruikt een apart bronrepository; dit is geen repository onder het GitHub-account van de gebruiker.

## Inhoud uitbreiden

`dist/data.js` bevat vier eenvoudige verzamelingen: LESSONS, DISCUSSIONS, SOURCES en DISCUSSION_SOURCES. Iedere les heeft een vast id, verwijzingen, tekstblokken, achtergrond, theologische uitleg, termen en een toets. Modulebereiken staan bovenaan `dist/app.js`. Een volgend leerjaar kan eigen gegevens, modulebereiken en een eigen opslagsleutel krijgen zonder bestaande voortgang te overschrijven.

De JSON-bestanden in de projectroot zijn de bewerkbare broninhoud; `package_content.py` bundelt ze. De bronbestanden content-a/b, discussions en sources zijn eveneens bewaard. Pas bij verdere wijzigingen de broninhoud aan en draai de bundelaar opnieuw. Alleen `dist` wordt gepubliceerd. Voer `node --check dist/app.js` en `node --check dist/data.js` uit voor publicatie.

## Bronnen en grenzen

De website bevat bronverwijzingen naar o.a. NBG, Yale Bible Study, museumcollecties en primaire kerkelijke documenten. Kerkelijke bronnen zijn gelabeld als standpunten uit een traditie; historische onzekerheid en betwiste interpretaties worden benoemd. Er is geen volledige onafhankelijke vakredactie of uitputtende bronnoot per bewering uitgevoerd.

De Bijbeltekst zelf staat niet integraal in de app. Verwijzingen leiden naar een zoekopdracht bij debijbel.nl; kies daar BGT. De app bevat eigen samenvattingen, geen lange beschermde Bijbelcitaten.

Zes originele met AI gemaakte module-illustraties (WebP, 1536×1024, samen ca. 1,78 MB) worden tussen lessen gedeeld. Er zijn nog geen 53 afzonderlijke verhaalillustraties. Prompts staan in image-prompts.md. Kaarten zijn schematische studiekaarten met historische plaatsnamen, geen nauwkeurige historische grenzen of bewezen routes.

De audio gebruikt SpeechSynthesis. Stemmen hangen van apparaat, browser en geïnstalleerde talen af. Een warme natuurlijke Nederlandse stem en foutloze werking op ieder Android-apparaat zijn niet gegarandeerd; geen echte Android-hardwaretest uitgevoerd.

## Privacy

Voortgang en notities staan lokaal onder de eigen sleutel `onze-bijbelacademie-v1`. Geen analytische trackers of serveropslag van notities. De gekozen platformhosting kan voor toegang eigen login vereisen. Een export bevat persoonlijke notities; bewaar deze zelf zorgvuldig. Import voegt voortgang en nieuwe notities samen, met behoud van bestaande notities met hetzelfde id.
