---
kapitel: 3
titel: "Første værktøjer: fra Excel til webapp på én eftermiddag"
status: gennemskrevet
adgang: betalt
sidst_opdateret: 2026-05-17
---

# Kapitel 03 Første værktøjer: fra Excel til webapp på én eftermiddag

## 3.1 Tilbage til prisberegneren

I februar 2026, næsten to år efter den første Excel-fil, sad jeg med den samme fil åben foran mig.

Den var vokset til seks faneblade. Det første faneblad var stadig det fra maj 2024, komplet med dollarkursen 6,91 fra den 13. maj. Rundt om det var der faneblade til Coop, Normal, Harald Nyborg, Løvbjerg og én med det sigende navn "BRUG DENNE".

Det konkrete øjeblik, der udløste det, var ikke dramatisk. En af vores sælgere spurgte mig om en kopi af filen. Igen. Det var formentlig den femte eller sjette gang over de foregående måneder.

Jeg sendte hende en kopi og tænkte: dette er ikke en løsning. Dette er en arbejdsgang, vi gentager manuelt, fordi vi ikke har gjort det ordentligt.

To ting var galt. For det første fandtes der ikke ét autoritativt sted, filen lå. For det andet var filen ikke mulig at opdatere for alle på én gang.

Begge problemer har et fælles svar: stop med at arbejde i en fil, og begynd at arbejde i et system. Det behøvede en eftermiddag.

## 3.2 Den første eftermiddag

Jeg åbnede claude.ai omkring klokken to om eftermiddagen.

Jeg havde ingen teknisk baggrund i webudvikling. Jeg vidste, hvad HTML var, nogenlunde, men jeg havde aldrig bygget en webside fra bunden. Det var ikke et problem, fordi det heller ikke var det, jeg skulle.

Jeg forklarede Claude, hvad Excel-filen indeholdt, og hvad jeg ville have: den samme beregningslogik, men som en webside, der kunne ligge ét sted. Jeg uploadede et screenshot af filen.

Den første version kom ti minutter senere. Den var grim. Den manglede halvdelen af variablerne. Men beregningslogikken virkede. Indtastede jeg en FOB-pris, kom der en landed cost og en kædepris ud i den anden ende. Det er det vigtige, der sker i den situation: man holder op med at se på, hvad der mangler, og begynder at se på, hvad der virker.

Det er præcis den tilgang, som gør at mange SMV'er ender med at fortænke deres løsning: de ser prototype og tror, de ser slutprodukt. Magien ligger ikke i at have den perfekte plan. Den ligger i samspillet med den sprogmodel, du arbejder med, iteration efter iteration.

Anden time gik med at tilføje variablerne, der manglede. Told. Forsikring. Transporttype. Jeg forklarede beregningslogikken til Claude for hvert felt — ikke i kode, men i sætninger. "Toldsatsen beregnes som denne procentdel af FOB-prisen plus fragtomkostningerne." Claude omsatte det til kode.

En konkret læring: når du beder Claude om at justere layoutet — "stram op på designet, det fylder for meget" — er du nødt til at være mere specifik. Fortæl Claude hvad grid-layoutet skal være, hvad fontstørrelsen skal være, og hvilke felter der skal grupperes. Ellers optimerer Claude konservativt. Vær præcis i samtalen.

Da jeg lukkede computeren klokken seks, havde jeg en webside. Den var ikke pæn. Men den virkede — og den lå ét sted.

## 3.3 Hvor det gik galt

Seks forsøg, inden vi kom i mål. Det er ikke en dårlig score. Det er en normal score, når man eksperimenterer med ny teknologi uden en IT-afdeling i ryggen.

**Den danske talformat-fælde**

Bruttoavancen viste 361,0% i stedet for 38,1. Omsætningen viste 225 i stedet for 225.000.

Årsagen: beregninger blev gemt som dansk-formateret tekst med punktum som tusindtalsseparator. JavaScripts parseFloat forventer engelsk format. Det læste "38,1" som 38.

Løsningen er generel: gem altid rå tal i koden, og formater kun ved visning. Aldrig omvendt.

**Safari-fælden**

Prisberegneren virkede ikke på Mac. Safari blokerer JavaScript i lokale HTML-filer som sikkerhedsforanstaltning. Chrome gør det ikke. Da alle Windows-brugere brugte Chrome og alle Mac-brugere brugte Safari, fandt vi fejlen sent.

Løsning: host filen på en rigtig webserver, så den ikke åbnes som en lokal fil.

**Hardcoded data**

Den første version havde 168 HS-koder hardcodet direkte i HTML-filen. Over 25 KB rå data midt i koden. Adskil data fra interface fra dag ét.

## 3.4 Hvad gjorde det det hele værd

Salgschefen begyndte at bruge prisberegneren den første uge. Hun fandt tre ting, der ikke fungerede, inden der var gået to dage. Alle tre observationer var korrekte. Ingen af dem ville have dukket op i en testplan.

En testplan beskriver, hvad du forventer kan gå galt. En rigtig bruger viser, hvad der faktisk går galt.

Der skete desuden noget andet, som vi ikke havde forudset. Salgschefen begyndte at bruge prisberegneren direkte i kundemøder, så i stedet for at notere ned, hvad kunden spurgte om, og sende et tilbud to dage senere, åbnede hun siden på sin bærbare, tastede tallene ind, og kunden kunne se resultatet i realtid.

Det var ikke en funktion, vi havde designet. Det var blot en adfærd, der opstod, fordi et værktøj gjorde noget muligt, der ikke havde været muligt før.

Hvert nyt værktøj derefter tog kortere tid at bygge end det foregående — ikke fordi Claude blev bedre, men fordi jeg lærte mønstrene og kendte fejlene.

## 3.5 Mønsteret bag de første værktøjer

I løbet af de første otte uger byggede vi tolv værktøjer. Prisberegner, kontraktgenerator, produktmanager, emballageberegner, opstartsskema, INCI-validator og flere til. Uden IT-afdeling.

**Byg først, integrer bagefter**

Hvert værktøj startede som en selvstændig HTML-side uden forbindelser til andre systemer. Infrastrukturen er svær at ændre. En HTML-side er nem at smide ud og bygge forfra. Stabiliser logikken i det enkle, inden du forbinder det med det komplekse.

**Én daglig bruger er mere værd end ti strategiske visioner**

Da vi byggede Produktmanager til vores produktadministrator, afslørede hendes daglige brug inden for den første uge fejl, vi aldrig ville have identificeret i en workshop. At INCI-tjek sker to gange i processen, og ikke kun én. At GTIN-nummeret skal auto-genereres, og der kan være flere koder til samme produkt. At der er et felt, hun aldrig bruger, og tre felter, hun savner.

Al den viden sidder i hende. Det eneste, der hentede den ud, var at give hende et virkeligt værktøj.

**Domæneviden trumfer teknologi**

Claude ved ikke, hvad en INCI-liste er, medmindre du forklarer det. Din ekspertise om din forretning er langt mere værdifuld end nogen teknisk viden om, hvordan man spørger en AI.

**Forenkling er den sværeste feature**

Opstartsskemaet startede med at vise 34 felter for alle brugere. I version to viste det ni felter for den daglige bruger og de resterende 25 kun for administratoren. Ingen klagede. Husk altid at designe til den konkrete opgave, ikke til den fulde funktionalitet.

## 3.6 Hvad jeg ville have ønsket nogen havde fortalt mig

**Brug claude.ai frem for ChatGPT til at bygge ting**

Jeg startede med ChatGPT, for det var det, jeg kendte. Anbefalingen om at skifte til claude.ai kom fra en deltager i Tech Circle-workshops i Aarhus i efteråret 2025 — særligt til iterativt arbejde over længere samtaler med mange gensidigt afhængige trin. Det er ikke en anbefaling om at alle skal bruge Claude. Det er en anbefaling om at bruge det værktøj, der bedst kan holde konteksten over et helt byggeforløb.

**Adskil data fra interface fra dag ét**

Hver eneste gang jeg ikke har gjort det, har jeg fortrudt det. Hardcoded data er usynlig gæld i version et og dyr gæld i version tre.

**Forvent at det første forsøg ikke er det rigtige**

Version tre var det første, der virkede godt nok til daglig produktion. Planlæg tre iterationer og brug to eftermiddage i alt. Det er realistisk.

## 3.7 Hvor det førte hen

Prisberegneren var ikke et afsluttet projekt, men den blev starten på et mønster.

Den spanske version kom to måneder senere. International rollout var ikke et stort projekt — det var en ny side, bygget på samme skelet som den første.

Derefter kom kontraktgeneratoren. Produktmanager. Emballageberegner. Opstartsskema. INCI-validator. Et dashboard, der samlede det hele.

Tolv værktøjer på otte uger. Nul IT-afdeling.

Men friheden har et modstykke: jo flere værktøjer, jo mere nødvendig er integrationen. Tolv selvstændige HTML-sider er tolv isolerede øer, og at forbinde dem via API'er og MCP er det, kapitel 09 handler om.

Og imellem de to faser er der noget, der let overses, men som viste sig at være hele fundamentet: compliance.

Uden compliance-laget bryder selv det bedste værktøj sammen, så snart der kommer rigtig brug af det i en reguleret industri. Det er hvad kapitel 04 handler om.
