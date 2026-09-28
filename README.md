# Smaakboek

Smaakboek is een persoonlijke receptenapp waarin gebruikers hun favoriete recepten kunnen bewaren, nieuwe recepten kunnen ontdekken en recepten met behulp van AI kunnen toevoegen vanuit foto's en screenshots.

De app is ontworpen als een rustig, overzichtelijk en persoonlijk digitaal kookboek. Gebruikers kunnen hun eigen recepten beheren, openbare recepten van anderen bekijken en bewaren, favorieten markeren en recepten met AI laten uitlezen.

---

## Over Smaakboek

Smaakboek is gemaakt om recepten op één centrale plek te bewaren.

In plaats van recepten verspreid te hebben over screenshots, social media, kookboeken, websites en notities, kunnen gebruikers ze in Smaakboek verzamelen en overzichtelijk terugvinden.

De app ondersteunt onder andere:

- eigen recepten toevoegen
- recepten toevoegen vanaf een foto
- recepten van social media toevoegen via screenshots
- AI-herkenning van ingrediënten en bereidingsstappen
- openbare en privé-recepten
- recepten van andere gebruikers ontdekken
- recepten bewaren
- favorieten
- categorieën en zoeken
- persoonlijke profielen
- meerdere talen
- installatie als webapp op telefoon of tablet

---

## Belangrijkste functies

### Eigen recepten toevoegen

Gebruikers kunnen handmatig een recept invoeren.

Per recept kunnen onder andere worden opgeslagen:

- naam van het gerecht
- ingrediënten
- bereidingswijze
- bereidingstijd
- categorie
- afbeelding
- zichtbaarheid

Een recept kan privé of openbaar worden opgeslagen.

### Recept toevoegen vanaf een foto

Een gebruiker kan een foto maken of uploaden van bijvoorbeeld:

- een kookboek
- een tijdschrift
- een uitgeprint recept
- een handgeschreven recept
- een receptkaart

De foto wordt met AI geanalyseerd.

Smaakboek probeert vervolgens automatisch onder andere te herkennen:

- titel
- ingrediënten
- hoeveelheden
- bereidingsstappen
- bereidingstijd

De gebruiker kan het resultaat altijd controleren en aanpassen voordat het recept wordt opgeslagen.

### Recept van social media toevoegen

Socialmediarecepten worden toegevoegd via screenshots.

De gebruiker kan maximaal **3 screenshots** uploaden van bijvoorbeeld:

- TikTok
- Instagram
- Facebook
- Pinterest
- andere socialmediaplatformen

Dit is bijvoorbeeld handig wanneer:

- ingrediënten in één screenshot staan
- de bereidingswijze verdeeld is over meerdere screenshots
- informatie alleen in de video zichtbaar is
- het originele recept niet als normale webpagina beschikbaar is

Smaakboek analyseert de screenshots met AI en combineert de informatie tot één recept.

De gebruiker controleert daarna het resultaat voordat het recept wordt opgeslagen.

### Openbare en privé-recepten

Bij het opslaan van een recept kan worden gekozen tussen:

**Privé**

Het recept is alleen zichtbaar voor de gebruiker zelf.

**Openbaar**

Het recept kan worden bekeken door andere gebruikers van Smaakboek.

Persoonlijke e-mailadressen worden niet weergegeven bij openbare recepten.

### Ontdek

Via de ontdekfunctie kunnen gebruikers openbare recepten van andere gebruikers vinden.

Gebruikers kunnen recepten bekijken en bewaren in hun eigen verzameling.

### Voorgesteld voor jou

Op de startpagina kan Smaakboek openbare recepten tonen als inspiratie.

Hierdoor ontdekken gebruikers makkelijker recepten die al door anderen zijn toegevoegd.

### Favorieten

Recepten kunnen als favoriet worden gemarkeerd zodat ze later snel terug te vinden zijn.

### Zoeken en categorieën

Recepten kunnen worden gevonden via het zoekveld en categorieën.

Voorbeelden van categorieën:

- Snel
- Pasta
- Gezond
- Bakken

De zoekfunctie is bedoeld om recepten eenvoudig terug te vinden op naam, ingrediënt of categorie.

### Profiel

Iedere gebruiker heeft een eigen profiel.

Gebruikers kunnen onder andere:

- een profielnaam instellen
- een profielfoto uploaden
- een voorkeurstaal kiezen

Het e-mailadres van een gebruiker wordt niet openbaar weergegeven.

---

## AI-functionaliteit

Smaakboek gebruikt AI om receptinformatie uit afbeeldingen te halen.

De AI kan bijvoorbeeld:

- tekst op een foto lezen
- ingrediënten herkennen
- hoeveelheden herkennen
- bereidingsstappen herkennen
- informatie uit meerdere screenshots combineren
- ontbrekende velden herkennen

AI-resultaten zijn niet gegarandeerd foutloos.

Daarom wordt de gebruiker gevraagd het resultaat altijd te controleren voordat een recept wordt opgeslagen.

---

## Gebruikte techniek

Smaakboek bestaat uit een frontend en een backend.

### Frontend

De frontend is een webapp en wordt momenteel opgebouwd met:

- HTML
- CSS
- JavaScript

De app wordt gepubliceerd via Vercel.

### Database en gebruikersaccounts

Voor backendfunctionaliteit wordt Supabase gebruikt.

Supabase verzorgt onder andere:

- gebruikersaccounts
- authenticatie
- database
- recepten
- ingrediënten
- bereidingsstappen
- favorieten
- profielen
- opslag van afbeeldingen
- Edge Functions

### AI

Voor AI-herkenning wordt de Gemini API gebruikt via een Supabase Edge Function.

De Gemini API-key staat niet in de openbare frontendcode.

Geheime API-sleutels worden als server-side secret opgeslagen in Supabase.

---

## Projectstructuur

De GitHub-repository is ongeveer als volgt opgebouwd:

```text
/
├── index.html
├── manifest.webmanifest
├── service-worker.js
├── robots.txt
├── README.md
│
└── icons/
    ├── apple-touch-icon.png
    ├── favicon-32.png
    ├── favicon-48.png
    ├── icon-192.png
    ├── icon-512.png
    ├── icon-maskable-192.png
    ├── icon-maskable-512.png
    └── smaakboek-logo.png
```

### index.html

Bevat de gebruikersinterface en de belangrijkste frontendlogica van Smaakboek.

### manifest.webmanifest

Bevat instellingen voor de webapp, zoals:

- appnaam
- korte naam
- themakleur
- achtergrondkleur
- app-iconen
- startpagina
- standalone-weergave

Hierdoor kan Smaakboek op ondersteunde apparaten als webapp worden toegevoegd aan het beginscherm.

### service-worker.js

Wordt gebruikt voor PWA-functionaliteit en caching.

Belangrijke API-aanvragen naar Supabase worden niet offline gecachet.

### robots.txt

Bevat basisinstructies voor zoekmachines.

### icons

Bevat de verschillende formaten van het Smaakboek-logo die nodig zijn voor:

- browserfavicons
- iPhone
- iPad
- Android
- geïnstalleerde webapps
- maskable app-icons

---

## PWA

Smaakboek is voorbereid als Progressive Web App.

Hierdoor kan de website op ondersteunde apparaten worden toegevoegd aan het beginscherm.

De app kan dan meer als een normale mobiele app worden geopend.

Afhankelijk van browser en apparaat kunnen functies verschillen.

---

## Installeren op een telefoon

### iPhone of iPad

Open Smaakboek in Safari.

Tik op de deelknop en kies:

**Zet op beginscherm**

Daarna verschijnt Smaakboek met het eigen app-icoon op het beginscherm.

### Android

Open Smaakboek in Chrome.

Afhankelijk van het apparaat verschijnt een optie zoals:

**App installeren**

of:

**Toevoegen aan startscherm**

---

## Veiligheid

Gevoelige informatie hoort nooit in de GitHub-repository te staan.

Plaats daarom geen geheime sleutels in:

- `index.html`
- JavaScript in de browser
- `README.md`
- openbare GitHub-bestanden

Voorbeelden van informatie die geheim moet blijven:

- Gemini API-key
- service-role keys
- privé API-tokens
- wachtwoorden

De publieke Supabase-key die bedoeld is voor gebruik in de browser kan wel in de frontend worden gebruikt, mits de database goed is beveiligd met Row Level Security.

---

## Supabase

Smaakboek gebruikt Supabase als backend.

Belangrijke onderdelen zijn:

### Authentication

Gebruikers kunnen een account aanmaken en inloggen.

### Database

De database bevat onder andere informatie over:

- profielen
- recepten
- ingrediënten
- bereidingsstappen
- favorieten

### Storage

Afbeeldingen kunnen worden opgeslagen in Supabase Storage.

Voorbeelden:

- receptafbeeldingen
- profielfoto's

### Edge Functions

AI-aanvragen worden via een Edge Function uitgevoerd.

Hierdoor hoeft de geheime Gemini API-key niet in de browser te staan.

---

## Privacy

Smaakboek is ontworpen met aandacht voor privacy.

Belangrijke uitgangspunten:

- privé-recepten zijn alleen zichtbaar voor de eigenaar
- openbare recepten mogen door andere gebruikers worden bekeken
- e-mailadressen worden niet openbaar getoond
- geheime API-sleutels worden niet in de frontend geplaatst

Voor een publieke lancering is het verstandig om daarnaast een eigen:

- privacyverklaring
- gebruiksvoorwaarden
- cookiebeleid indien van toepassing
- contactpagina

toe te voegen.

---

## AI en betrouwbaarheid

AI kan fouten maken.

Voorbeelden:

- een hoeveelheid kan verkeerd worden gelezen
- een ingrediënt kan worden overgeslagen
- tekst op een onscherpe screenshot kan verkeerd worden geïnterpreteerd
- bereidingsstappen kunnen onvolledig zijn

Daarom blijft de gebruiker verantwoordelijk voor het controleren van een recept voordat het wordt opgeslagen of gebruikt.

Bij voedselallergieën, intoleranties of andere gezondheidsrisico's moet altijd de oorspronkelijke bron of productinformatie worden gecontroleerd.

---

## Social media

Smaakboek downloadt geen TikTok-, Instagram- of Facebookvideo's.

In plaats daarvan kan de gebruiker screenshots uploaden van een recept.

Er kunnen maximaal **3 screenshots per import** worden gebruikt.

De gebruiker is zelf verantwoordelijk voor het gebruik van screenshots en receptinhoud volgens de voorwaarden en rechten van de oorspronkelijke bron.

---

## Talen

Smaakboek ondersteunt meerdere talen.

De huidige opzet bevat ondersteuning voor onder andere:

- Nederlands
- Engels
- Duits
- Frans

De gekozen taal kan worden gebruikt voor zowel de interface als AI-herkenning.

---

## Publiceren via Vercel

Smaakboek wordt vanuit GitHub via Vercel gepubliceerd.

Bij een nieuwe commit in GitHub kan Vercel automatisch een nieuwe versie van de website bouwen en publiceren.

Een gebruikelijke werkwijze is:

1. bestanden aanpassen
2. wijzigingen naar GitHub uploaden
3. commit maken
4. Vercel start automatisch een nieuwe deployment
5. na succesvolle deployment staat de nieuwe versie online

---

## Ontwikkeling

Bij toekomstige ontwikkeling kunnen functies worden toegevoegd zoals:

- boodschappenlijst
- weekplanner
- porties automatisch omrekenen
- voedingswaarden
- receptbeoordelingen
- reacties
- delen via WhatsApp
- recepten volgen van andere gebruikers
- persoonlijke aanbevelingen
- tags
- filters op bereidingstijd
- filters op dieet
- recepten importeren vanaf websites
- notificaties
- eigen domeinnaam
- betere offline ondersteuning

---

## Mogelijke toekomstige structuur

Wanneer Smaakboek groter wordt, kan het verstandig zijn om de huidige code verder op te splitsen.

Bijvoorbeeld:

```text
/
├── index.html
├── css/
│   └── style.css
├── js/
│   ├── app.js
│   ├── auth.js
│   ├── recipes.js
│   └── ai.js
├── icons/
├── manifest.webmanifest
├── service-worker.js
└── README.md
```

Dit maakt onderhoud makkelijker wanneer de app steeds groter wordt.

---

## Status

Smaakboek is momenteel in ontwikkeling.

Functies kunnen nog veranderen en nieuwe onderdelen worden regelmatig toegevoegd en getest.

---

## Merk en ontwerp

Naam:

**Smaakboek**

Smaakboek gebruikt een warme, rustige en culinaire uitstraling.

De huisstijl bestaat uit natuurlijke kleuren en afgeronde elementen.

Het officiële Smaakboek-logo en de bijbehorende app-iconen staan in de map `icons`.

---

## Beheer

Het project wordt beheerd via GitHub en gepubliceerd met Vercel.

Backend, accounts, database en opslag worden beheerd via Supabase.

AI-functionaliteit wordt server-side gekoppeld via Supabase Edge Functions.

---

## Belangrijk voor bijdragen

Voordat wijzigingen worden gepubliceerd:

1. test de app op desktop
2. test de app op mobiel
3. test inloggen en uitloggen
4. test privé- en openbare recepten
5. test fotoherkenning
6. test socialmedia-import met 1, 2 en 3 screenshots
7. controleer of API-sleutels niet in GitHub terechtkomen
8. controleer de Vercel-deployment
9. test na publicatie de productieversie opnieuw

---

## Licentie en gebruik

De broncode, huisstijl, naam en het logo van Smaakboek mogen niet automatisch worden beschouwd als vrij te gebruiken materiaal.

Wanneer het project publiek op GitHub staat zonder open-source licentie, betekent dit niet automatisch dat anderen toestemming hebben om de code, naam of huisstijl te kopiëren of commercieel te gebruiken.

Voor een professionele publieke lancering kan later een aparte licentie of auteursrechtvermelding worden toegevoegd.

---

## Contact

Een officiële contactmogelijkheid kan later aan deze README worden toegevoegd wanneer Smaakboek publiek wordt gelanceerd.

---

**Smaakboek — uw persoonlijke digitale kookboek.**
