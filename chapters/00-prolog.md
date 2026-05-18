---
kapitel: 0
titel: "Prolog — fra Mural-tavle til AI-platform"
status: gennemskrevet
adgang: gratis
sidst_opdateret: 2026-05-17
---

# Prolog — fra Mural-tavle til AI-platform

## En ganske almindelig tirsdag

Det startede en tirsdag i maj 2024.

Vores salgschef stod i min dør og spurgte, om jeg kunne hjælpe hende med noget. En kunde havde bedt om en masse priser til et helt sortiment af produkter. Hun skulle nå at sende et tilbud inden for de kommende 3 dage. Problemet var at hun ikke helt vidste hvilke priser hun kunne give.

Jeg var lige startet i virksomheden i marts måned, så jeg spurgte ind til hvordan vi normalt beregnede priser, og det gik op for mig, at der ikke fandtes nogen fast fremgangsmåde. Der var ingen skabelon eller regler der var nedskrevet noget sted. Hidtil havde det været direktøren der havde beregnet priserne, og han havde regnet det i hovedet samt indført det i en kolonne i et Excel ark. Der var ikke direkte regnet med de variable omkostninger ifm. importtold, transport og logistik, men han havde flere års erfaring i at beregne kostpriser ud fra hvad det skulle koste i butikken til forbrugeren, hvorefter hun havde gået videre med priserne til kunden. Nu stod hun og havde behov for hurtigt selv at kunne beregne priserne til hendes kunder. Men der var ingen faste regler eller logik for udefrakommende, og hun havde behov for hjælp.

TBP Supply er en typisk lille SMV vækstvirksomhed, hvor mange af firmaets vigtige informationer og viden er oparbejdet gennem flere år og besiddes af ejeren. Vores ejer/direktør ville derfor gerne gøre TBP mere skalerbart, så vi kan vækste i fremtiden, hvilket kræver at viden bliver delt for at tage hurtigere beslutninger.

Jeg satte mig ved computeren og byggede en simpel Excel-prisberegner med opslagsfunktioner ift. kunder og importtold samme eftermiddag. Salgschefen skulle kunne indsætte en FOB-pris fra leverandøren og så regne sig frem til en landet kostpris. Derfra kunne hun lægge en avance på og ende med en kædepris, hun kunne give kunden. Det var ikke elegant, men det virkede. Hun kunne svare kunden inden fyraften.

Jeg lukkede computeren og tænkte, at det var det, endnu en god dag hvor vi fik tingene løst og bygget lidt fundament i forhold til fremtidige prisberegninger.

## Det var ikke løst

Det viste sig hurtigt, at der var variable, jeg ikke havde regnet med i den første udgave. Transport med skib, tog eller fly, der ændrede prisen løbende pga. krig og anden uro. Forsikring på lasten. Toldsatser. Samples til kunden som sikkerhed mod fejlproduktion. En tester, som butikken kunne placere ved hylden. En bonustrappe baseret på hvor meget kunden aftog. Marketing-omkostninger. Og senest, og måske det mest underfundigt komplicerede, emballage-afgiften under det udvidede producentansvar, som jeg kun var i gang med at finde ud af overhovedet eksisterede, samt vigtigheden heraf.

Excel-filen voksede. Ét faneblad blev til to, to blev til seks. Dollarkursen 6,91 fra den 13. maj stod stadig øverst i arket, men omkring den var der pludselig kolonner til alle tænkelige butikskæder: Normal, Coop Danmark, Harald Nyborg, Løvbjerg m.fl. Hver kæde havde sin egen logistikomkostninger og markedsføringskampagner, der skulle tages højde for ved hver enkelt prisberegning.

Det gik op for mig over de næste par uger, at prisberegneren aldrig kom til at være færdig. Ikke fordi den var dårlig, den fungerede perfekt i Excel. Men fordi hver gang jeg troede jeg havde den sidste variabel med, dukkede der en ny op. Nogle gange fordi en lov ændrede sig. Nogle gange fordi en kunde bad om noget nyt. Nogle gange fordi jeg opdagede, at vi havde regnet forkert på noget, uden at bemærke det.

Det er den første lærdom jeg tog med herfra, og den står stadig stærkest for mig:

> *Den virkelige kompleksitet er altid større end den skabelon der findes på skrivebordet. Og derfor er det aldrig skabelonen man skal arbejde på. Det er virkeligheden.*

`[Figur-idé: Dette citat fremhæves som visuelt callout i Ghost-temaet]`

## Tavlen på væggen — juni 2024

Knapt en måned senere satte jeg mig for at kortlægge hele virksomhedens processor og rutiner fra første idé til færdigt produkt leveret hos kunden. Jeg startede med en ren tavle, nogle Post-It og en meget manuel fremgangsmåde, uden brug af nogen systemer. Det virkede rigtig godt fordi vi kunne diskutere det i plenum eller i de enkelte afdelinger, hvordan vores proces så ud lige nu (AS-IS).

Efterfølgende brugte jeg Mural og satte mig for at tegne hvad der faktisk sker hos TBP, fra det øjeblik vi kontakter en ny kunde, til produktet er på en butikshylde hurtigst muligt. Roller ned ad venstre side: Salg, P&D, P&L, Design, administrativ koordinator. Værktøjer hen over toppen: Business Central, Monday, GS1 Packaging, Excel-arkene. Og så begyndte jeg at tegne pile mellem dem.

Det var et af de mest udfordrende projekter, jeg har lavet, der krævede en hel del tålmodighed.

For det første, fordi jeg opdagede, at jeg ikke selv vidste, hvad der skete flere steder. Jeg var nødt til at gå rundt og spørge. Folk beskrev det samme flow på tre forskellige måder, afhængigt af hvem der fortalte. Ofte var det samme data, der blev registreret tre gange: én gang i Excel, én gang i Business Central, én gang i Monday. Ingen af stederne var det forkert. Men ingen af dem talte sammen.

For det andet, fordi jeg måtte acceptere, at TBP Supply ikke kunne skaleres som virksomheden var opbygget. Ikke fordi vi ikke arbejdede hårdt nok — det gjorde vi alle sammen. Men fordi selve processen og rutinerne bestod af et usynligt system af mails, regneark, møder og hukommelse, der krævede at alle vidste alt. Det virker når man er få personer, men det bliver en udfordring når man bliver mere end 4-5 personer.

Tavlen fra juni 2024 er ikke pæn. Den er rodet. Den har gule sticky notes med ting som *"SRP-skabeloner udvikles ad hoc i samarbejde med Logistik"* og *"Altox-godkendelse efter Art Work sendes — nogen følger op, andre glemmer det"*. Det var første gang jeg kunne præsentere virkeligheden som den var lige nu.

Det var også første gang jeg tænkte: hvad hvis vi byggede noget af det selv, og styrede alle vores data selv?

## Systemlandskabet — juli 2024

I juli 2024 lavede jeg en ny tavle. Denne gang ikke om mennesker og processer, men om systemerne alene.

Der stod: GS1Trade Sync, GS1Trade Packaging, GS1Trade Activate, Kollektivordningen VANA, Business Central, Shopify, WordPress. Og i midten, med en lille note i parentes: *"E-conomic (udfases)"*.

Ved siden af listen tegnede jeg kundetyperne: OEM-kunder, Private Label-kæderne Løvbjerg, 365 Discount, Harald Nyborg. Private Brand-kæden Normal. Own Brands New:In til dagligvarehandlen. Hver af dem havde sin egen vej ind i vores data, sit eget dataudvekslingsformat, sit eget sæt af krav.

Der forstod jeg den dag, at TBP ikke havde ét system. Vi havde tolv. Og tolv systemer betyder, at data bor tolv steder. Det vi troede vi havde som ét samlet billede, var i virkeligheden tolv halve billeder, som vi samlede manuelt hver gang vi havde brug for at vide noget.

Ud fra det board blev beslutningen truffet at udfase e-conomic og konsolidere på Business Central som single source of truth. Det er et arbejde jeg forventer kører sideløbende med anden udvikling hele 2026. Men beslutningen blev taget der, på en tavle, uden at jeg åbnede et eneste system.

## AI lagt ovenpå — oktober 2025

Et års tid efter den første procestavle satte jeg mig ned med en kopi af den. Jeg kopierede hele strukturen over i et nyt Mural-board: TBP AI Processor. Samme roller, samme arbejdsgange, samme pile.

Men denne gang lagde jeg små bobler ind der, hvor jeg kunne se, at mennesker brugte tid på arbejde, som en maskine kunne hjælpe med. *AI-forslag til brugsanvisninger. AI-tjek af symboler på produkter, før de sendes til godkendelse hos Altox. Fremhævning af vigtigste ingredienser i forhold til EU-lovgivning. INCI-rapport verifikation. AI-genereret forslag til claims. Prisberegner. AI Dashboard.*

Boblerne erstattede ikke folk. De erstattede ventetid, fejltjek og det trættende administrative arbejde, der sad mellem de steder, hvor folk faktisk tog beslutninger. En INCI-rapport skal stadig godkendes af en fagperson — men fagpersonen skal ikke længere sidde og krydstjekke 87 ingredienser mod en Excel-fil fra leverandøren. Det kan en AI gøre på sekunder, og så præsentere de afvigelser i et fast format, der kræver beslutning.

Det var den dag, bogen begyndte. Uden at jeg selv vidste det. For det der skete, var at jeg i praksis havde tegnet en metode til, hvor AI skulle indgå i den daglige drift. Blot ved at beskrive steder hvor mennesker venter på information, og lægge AI ind netop der.

Jeg havde lavet tre versioner af den samme tavle over tretten måneder. Den første viste virkeligheden. Den anden viste systemerne. Den tredje viste, hvor AI kunne gøre en forskel. Til sammen var de en metode til at digitalisere en SMV uden at starte med en AI-strategi.

## Februar 2026: fra Excel til HTML

Først i februar 2026 tog jeg skridtet fra Excel til en rigtig webapp. Prisberegneren fra maj 2024 var stadig i brug. Den var vokset til seks faneblade, og hver gang en ny sælger skulle bruge den, var hun nødt til at bede mig om en kopi — for ingen kunne huske, hvilken version der var den nyeste.

Jeg byggede den samme prisberegner om til en HTML-side. Det tog en eftermiddag. Claude skrev koden, jeg sagde til, hvor jeg ville have ting. Da vi var færdige, havde jeg en webapp, der kunne ligge ét sted på vores fælles OneDrive, og hvor alle altid brugte den nyeste version.

Det er det kapitel 03 handler om. Men det hører også hjemme her, fordi det er her, rejsen bliver håndgribelig. Fra et regneark, der var udarbejdet ud fra ejerens viden og erfaring, til et værktøj, der er dokumenteret gennem kode, og som kan opdateres i løbet af minutter, når virkeligheden ændrer sig.

## Denne bog

Det her er historien fra tiden omkring den første Mural-tavle og frem til i dag. Jeg har valgt at skrive den i jeg-form, fordi jeg tror det er den ærligste måde. Jeg sælger ikke en metode. Jeg fortæller, hvad jeg har gjort, hvilke fejl jeg har lavet, og hvilke genveje jeg har fundet undervejs.

Én af de vigtigste erkendelser fra det arbejde er, at man som regel gør det sværere end det behøver at være. Jeg har mødt mange SMV'er, der fortænker deres løsning, fordi de vil have det fulde overblik inden de bygger noget. Det er forståeligt — men det er sjældent den rigtige rækkefølge. Magien i AI-assisteret byggearbejde ligger ikke i at have den perfekte plan fra start. Den ligger i samspillet med den sprogmodel, du arbejder med. Prøv, juster, prøv igen.

Et lille sidespor, der faktisk hører hjemme her: denne bog er selv et eksempel på præcis det. Den er ikke skrevet færdig og derefter sat i system. Den er bygget med de samme metoder, den beskriver — i samarbejde med claude.ai, med en fast ugentlig rutine, der henter ugens læring, sorterer dem i kapitelstruktur og foreslår, hvad der skal med. Det er den eneste måde, jeg har kunnet holde et løbende projekt i gang ved siden af en fuld arbejdsuge.

Bogen er ikke skrevet færdig. Jeg publicerer kapitler og opdateringer løbende de kommende 12-18 måneder, i takt med at projektet hos TBP Supply skrider frem. Du vil kunne se datoen for sidste opdatering på hvert kapitel.

### Fire faser

**Idé.** Backlog, koncepter, ideer man endnu ikke har bygget. Kapitel 1-2.

**Eksperiment.** Prototyper, der testes med kolleger. Integreret med eksisterende systemer. Kapitel 3-4.

**Pilot.** Værdifulde værktøjer der bruges i produktion, i et begrænset team. Kapitel 5-9.

**Skala.** Fuld produktion, AI-agenter, autonome flows. Det er det, jeg arbejder henimod. Kapitel 10-12.

### Det gratis spor

Prologen, kapitel 1 og kapitel 2 er gratis og uden binding. Derefter koster det 39 kroner om måneden inklusive moms at læse videre.

### Hvor skal du starte

Hvis du er ny i det her felt, fortsæt til kapitel 1.

Hvis du er midt i et projekt og har brug for at placere dig selv på kortet, spring direkte til kapitel 2 og tag modenhedstesten.

Hvis du er teknisk nysgerrig og bare vil se noget byggearbejde, start på kapitel 3.

Der er ingen forkert rækkefølge.
