---
kapitel: 2
titel: "Kortlæg din virkelighed, og AI som processor"
status: gennemskrevet
adgang: gratis
sidst_opdateret: 2026-05-17
---

# Kapitel 02 — Kortlæg din virkelighed, og AI som processor

## Hvad skal du have med fra dette kapitel

Hvis du er nået hertil, har du læst prologen om Mural-whiteboardtavlen, og du har læst kapitel 01 om paradokset mellem adgang og modenhed. Nu vil jeg give dig to ting, du kan bruge med det samme.

For det første: en metode til at kortlægge dine egne arbejdsgange, så du kan se præcis hvor AI vil give din virksomhed en fordel. Jeg kalder den workflow-dekomposition, og det er præcis den metode, jeg brugte til at lave mine Mural-tavler i prologen, bare forklaret som metode, så du kan bruge den selv.

For det andet: en modenhedstest. Den korte test bestående af tre spørgsmål, eller den længere version med otte spørgsmål, der kræver en time sammen med ledelsen. Resultatet af modenhedstesten placerer dig på AI-modenhedsstigen og fortæller dig hvilke kapitler i den her bog, der er mest relevante for dig lige nu.

Lad os starte med metoden.

## Workflow-dekomposition i fem trin

Denne fremgangsmetode udarbejdede jeg henover de måneder, jeg arbejdede med Mural-whiteboardtavlerne. Metoden var noget der fremkom i processen, fordi det var sådan, jeg kunne se hvor AI passede ind.

**Trin 1: Vælg ét konkret workflow.**
Vælg et workflow med en tydelig start og slutning — ikke "vores produktudvikling", men "fra en kunde beder om en pris, til vi har sendt et tilbud". Sæt mål i timer eller dage, ikke uger.

**Trin 2: Beskriv 5–10 trin i rækkefølge.**
Skriv hvert trin på én linje. Inkluder hvem der gør det. Du kommer formentlig til ti trin hurtigere, end du tror.

**Trin 3: Markér hvert trin som enten REGEL eller VURDERING.**
Regler er trin hvor svaret er givet, hvis du har data nok. Vurderinger er trin hvor menneskelig erfaring bestemmer udfaldet. Mange trin er blandinger — markér det der dominerer.

**Trin 4: Regler er automatiseringspotentiale.**
Hvert regel-trin er en kandidat til AI eller kode. Hvis det kræver at læse noget og forstå det, er det her AI har sine klare fordele.

**Trin 5: Vurderinger er beslutningsstøtte-potentiale.**
Vurderinger skal ikke automatiseres, men de kan have et beslutningsstøtte-lag: *"De sidste 12 sammenlignelige rabatter blev givet på følgende vilkår..."* Beslutningen er stadig sælgerens. Grundlaget er bedre.

`[Figur 2.1: Workflow-dekomposition på prisberegner-flowet]`

## 2.2 — Workflow-dekomposition: et konkret eksempel

Lad os tage metoden fra det forrige afsnit og prøve den af på et workflow, du allerede kender: prisberegneren fra prologen.

Flowet starter, når en sælger modtager en kundeforespørgsel, og det slutter, når hun har sendt et tilbud. Det lyder enkelt. Det er det ikke. Da jeg for første gang satte mig ned og skrev trinene op, kom jeg til ti trin, og jeg var ikke en gang sikker på, at jeg havde fået dem alle med.

**Workflow-grænsen er vigtigere end du tror**

Før du skriver et eneste trin, skal du definere to ting: hvad starter flowet, og hvad slutter det.

I prisberegneren: flowet starter, når sælger modtager en forespørgsel — via mail, telefon eller ved et kundemøde. Det slutter, når tilbuddet er sendt, og sælger har logget det i Business Central. Ikke "når kunden svarer". Sendt.

Et typisk prisberegner-flow hos TBP tager to til fire timer fordelt over én til tre dage. Ikke fordi det arbejdsmæssigt tager så lang tid, men fordi der er ventetid indlejret. Den ventetid er usynlig, når man taler om flowet, men den er meget synlig, når man kortlægger det trin for trin.

**Ni trin fra forespørgsel til tilbud**

1. Sælger modtager forespørgsel fra kunde — via mail, telefon eller ved et møde
2. Sælger noterer, hvad kunden vil have: produkt, antal, ønsket leveringstidspunkt
3. Sælger åbner Excel-prisberegneren og finder den rigtige fane for den pågældende kundekanal
4. Sælger finder og kopierer FOB-prisen fra leverandørens seneste prisliste eller mail
5. Sælger udfylder transportvariable: skib, tog eller fly, plus forsikring og told
6. Excel beregner landed cost automatisk ud fra formlerne i arket
7. Sælger lægger avance på baseret på kundetype, volumen og eventuel markedsaftale
8. Sælger formaterer tilbuddet — enten i Word-skabelon eller direkte i en mail
9. Sælger sender tilbuddet og registrerer det i Business Central

**Regel eller vurdering?**

Trin 1 og 2 er vurderinger. Trin 3 er tilsyneladende en handling — men det skjulte et problem hos TBP: hvilken fil, hvilken version, hvilken fane. Trin 4 er en ren regel. Trin 5 er overvejende regler med en hybrid i transportvalget. Trin 6 er ren regel. Trin 7 er vurdering. Trin 8 er hybrid. Trin 9 er regel.

Det overraskende: fem ud af ni trin er regelbaserede. De fleste SMV'er undervurderer, hvor stor en del af deres arbejde der faktisk følger faste mønstre.

**Hvor passer AI ind?**

Trin 4 er et oplagt sted at starte: AI kan læse en leverandørmail og udtrække FOB-prisen automatisk — 5-10 min sparet pr. tilbud. Trin 7 skal ikke automatiseres, men AI kan vise hvilke avancer der er givet på sammenlignelige ordrer de seneste tolv måneder.

`[Figur 2.1: Swimlane med de ni trin, farvekodet efter regel/vurdering/hybrid, med AI-muligheder markeret til højre]`

## Hvor moden er din organisation?

Modenhedstesten bygger på en model, inspireret af Jesper Luff Olesen, partner hos BCT:

1. **Passiv.** ChatGPT bruges til mails. Ingen strategi. Ingen integration.
2. **Fragmenteret.** Enkelte medarbejdere eksperimenterer. Ledelsen ved det knap.
3. **Bevidst.** Ledelsen har prioriteret AI. Budget allokeret. Use cases valgt.
4. **Integreret.** RAG i produktion. Fine-tunede modeller. ROI måles.
5. **Autonom.** AI-agenter eksekverer. Human-in-the-loop.

`[Figur 2.2: AI-Modenhedsmodellen. Inspireret af Jesper Luff Olesen, BCT]`

Mellem niveau 2 og 3 er der en kløft — "the gap". 90% af virksomheder krydser den aldrig.

`[Embed: ai-modenhedstest-teaser.html]`

## 2.3 — Claude som processor: fra opslagsværk til sparringspartner

Mange bruger AI på den samme måde. De åbner ChatGPT, stiller et spørgsmål, læser svaret, lukker vinduet og går videre. Det er nyttigt. Det er ikke transformativt.

Der er tre niveauer i den måde, man kan arbejde med AI på. De fleste er på niveau ét. Niveau tre er det, der faktisk rykker noget.

**Niveau 1: AI som opslagsværk**

Du stiller et spørgsmål, får et svar, går videre. Det fungerer til enkle faktuelle spørgsmål. Begrænsningen: AI'en ved ikke noget om *din* virksomhed.

**Niveau 2: AI som processor af dine egne data**

Du giver AI'en din kontekst *først* — og så spørger. "Her er INCI-listen fra vores leverandør. Her er EU's krav. Hvad er afvigelserne?" Da vi testede INCI-verifikation første gang, identificerede Claude tre afvigelser på fire minutter. Det ville have taget en eftermiddag manuelt.

**Niveau 3: AI som sparringspartner i dialog**

Du arbejder iterativt over tid — AI foreslår, du tester, opdager hvad der mangler, forklarer tilbage. Næste version er bedre. Det er det, nogen kalder "vibe coding". Det kræver ikke, at du kan skrive kode. Det kræver, at du ved, hvad du vil have, og hvad der ikke virker.

Din ekspertise om din forretning er langt mere værdifuld end nogen teknisk viden om, hvordan man spørger en AI. Forretningslogikken er råmaterialet. AI omsætter det til form.

**Den vigtigste designregel**

Byg dine prompts og dine værktøjer, så AI'en kan udtrykke usikkerhed — ikke gætte sig til et svar. Da vi byggede vores personalehåndbog, instruerede vi Claude specifikt: markér med [AFKLARES] og fortsæt, når du støder på noget, der kræver en ledelsesafgørelse. Vi fik et brugbart dokument og en liste over præcis de steder, der krævede vores egne beslutninger. Det er forskellen på en AI-assistent der sparer tid, og en der skaber mere arbejde bagefter.

## Hvad er det næste?

I kapitel 03, det første bag paywall, viser jeg konkret hvordan jeg byggede prisberegneren om fra Excel til en HTML-app på én eftermiddag.
