# Session 10 — Red Team-granskning

**Granskat material:** session-10-prep.md, session-09-prep.md, campaign-status.md, befintliga NPC-JSON-filer, tierp-npcs.md
**Datum:** 2026-05-03
**Allvarlighetssammanfattning:** 🔴 4 kritiska | 🟡 9 varningar | 🟢 7 noteringar

---

## Exekutiv sammanfattning

Sessionen har en **stark öppning** (Mjöd) och en **stark cliffhanger-position** (hemkomsten till Tierp), men **mittsektionen är farligt öppen** — Del 4 är tre uppslag utan tydlig drivkraft, Del 5 är "öppet utfall", och cliffhangern är "TBD". Det här är medvetet sandbox men risken är att kvällen rinner ut utan dramatisk topp. Den största praktiska risken är **Mjöd-scenen kontra svartstenarna** — Sören har en sten som "fångas ni inte" mot Maria, och scenen är tänkt att vara emotionellt fångande. Mekaniskt motsäger det varandra. Severin saknar JSON och två custom-talanger är odefinierade. Ida-scenen förlitar sig på antagandet att Skogens Krona är ovetande — om en spelare frågar "varför är inte värdshuset under uppsikt?" har du inget svar utan på-stället-improvisation.

## Beredskapsgrad

```
NÄSTAN REDO ⚠️
```

Motivering: Mjöd-scenen och Tierp-cliffhangern är solida. Mittsektionen behöver tydligare drivkraft eller minst en backup-händelse som triggar action. Severin behöver JSON innan spel.

---

## Fynd

### A. NPC-komplettering

| NSC | Markdown | JSON | Stats OK | Status |
|-----|----------|------|----------|--------|
| **Mjöd** | ✅ befintlig | ❌ | N/A (ej strid) | 🟢 |
| **Broder Severin** | ✅ i prep | ❌ | ⚠️ custom-talanger vaga | 🔴 |
| **Inkvisitionsryttare** | ✅ i prep | ❌ | ⚠️ ej Foundry | 🟡 |
| **Greve Bertil** | ✅ i prep | ❌ | ⚠️ Soak/rustning oklar | 🟡 |
| **Ida** | ✅ tierp-npcs.md | ❌ | N/A (ej strid) | 🟢 |
| **Idas moster** | ❌ | ❌ | N/A | 🟢 (namn saknas) |
| **Värdshusvärden** | ✅ tierp-npcs.md | ❌ | N/A | 🟡 (kan dyka upp ovetad) |
| **Ulf Grönlöv** | ✅ befintlig | ✅ | ✅ | 🟢 |
| **Fader Sten** | ✅ befintlig | ✅ | ✅ | 🟢 |
| **Anders** | ✅ befintlig | ✅ | ✅ | 🟢 |
| **Greta** | ✅ befintlig | ✅ | ✅ | 🟢 |
| **Bror** | ⚠️ minimal | ❌ | N/A | 🟡 |
| **Fader Daniel** (callback) | ✅ befintlig | ❌ | N/A | 🟢 |

🔴 **Severin saknar JSON.** Trots att hans stat-block finns i prepen behöver Foundry-token och färdig stat-block för smidig användning. Han är kvällens etablerings-NSC och troligen S11-bossen.

🔴 **"Inquisitor's Eye" är överoptimerad.** Som skrivet: *+🟦 till Severin OCH ⬛ till motståndaren* — det är effektivt två fördelar i en talang. Standard Genesys-effekt skulle vara EN av dessa. Adversary 3 ger redan ⬛⬛⬛ till motståndaren. Ackumulerad: 4 svarta tärningar + en blå. Det blir närapå omöjligt för någon att prata Severin. Klargör eller sänk.

🔴 **"Cold Logic" är vag.** *"Immun mot empati-baserade argument"* — vad är en "empati-baserad argument" mekaniskt? Vid bordet kommer det landa som SL-veto: *"nej, det räknas inte"*. Skriv konkret regel: *"Vid Charm- eller Negotiation-slag mot Severin med argument om empati/familj/synd, slå svårighet uppgraderas (lila → röd, eller +1 lila)."*

🟡 **Greve Bertil Soak 3** men ingen rustning specificerad. Br 2 + 1 läderkappa? Klargör i stat-block.

🟡 **Värdshusvärden från S4 var fientlig** mot sällskapet (kastade ut dem, tog 30 silver). Ida-scenen antar att han inte är i frontrummet vid morgonen, men om han ser dem genom ett fönster eller är i köket — han kan tipsa Severin. Förbered svar.

🟡 **Idas moster** har en nyckel + karta — central i räddningsplanen — men har inget namn. Improvisation kan kännas tunn.

🟡 **Bror har ingen markdown alls.** Han är räddad, han följer med, han ger info i Del 3. Han behöver minst 5 rader (vilka han var, vad han säger, hur han hanteras vid bordet).

---

### B. Plotlogik

🔴 **Mjöd + svartstenarna = mekanisk kontradiktion.** Sällskapet fick i S8 fyra svarta stenar från Ljuva: *"Håll dem mot hjärtat när ni talar med henne. Så fångas ni inte."* Mjöd-scenen i S10 är **känslomässigt fångande** — det är hela poängen, hennes ord ska landa hos Sören. Om Sören håller stenen mot hjärtat (vilket är klokt), borde scenens magi inte fungera. Antingen:
- (a) Etablera att stenarna skyddar mot **förtrollning**, inte mot **äkta sanning**
- (b) Sören har inte stenen i handen i denna scen (han är i en annan känsla)
- (c) Mjöd ser stenen, ler, säger *"du behöver inte den ikväll. Jag ska inte ta något."*

**Min rek:** (c). Det är en elegant lösning som visar Mjöds godhet och frigör scenen.

🟡 **"Severin har inte förstått Skogens Krona-kopplingen"** är skört. Praktiska hål:
- Värdshuset är öppet morgonen. Värden finns i huset. Severins ryttare patrullerar by:n. Vad om en ryttare ser sällskapet komma in?
- Om Severin frågar Ida (som han har gjort en gång), har Ida svarat sanning eller ljugit? Om hon ljög finns risk att Severin upptäcker det.
- Vad om värden ser sällskapet och **omedelbart** rapporterar? (Han var ovänlig i S4. Skäl att vara hämndlysten.)

**Lösning:** Etablera tydligare. Antingen är värden inte i huset (avresa till någon annan stad?) eller hans relation till sällskapet är förändrad (Ida har försonat med honom?). Eller: Severin har varit i Tierp i 2 veckor och allt redan rapporterats. Värden känner sällskapet som "ungar som rymde till skogen". Han har inget att tipsa om.

🟡 **"Anders har inte gett namn på sällskapet" efter 2 veckors förhör.** Severins stat-block säger Coercion 5 + Inquisitor's Eye + Cold Logic. Det är en man som bryter folk effektivt. Anders är ung präst, inte en stridskonditionerad veteran. **2 veckor är lång tid.** Antingen:
- Severin har inte fokuserat fullt på Anders (har fokuserat på Greta som häxa)
- Anders har gett *delar* — kanske namn men inte detaljer
- Anders bryts NU, denna vecka — Idas berättelse antyder det (*"han bryts. han säger saker"*)

**Min rek:** modifiera Idas berättelse — Anders har precis börjat ge namn. Severin vet *"Sören och två till"* men inte deras nuvarande plats. Det ger sessionen tickande klocka.

🟡 **Tre uppslag i Del 4 utan tydlig drivkraft.** Spelarna kommer fråga *"vad är vår plan?"* — det finns ingen given. Det är OK för sandbox, men SL bör ha en **NPC som föreslår handling** (Bror? Ulf? Idas moster?). Eller en **tickande händelse** (Severin planerar förhör imorgon, sällskapet har en deadline).

🟡 **"Ulf Grönlöv har silver att ge"** — 80 silver. Kompletterande, men spelarnas pengar är typ 0 (de fick 6 bärnstenar i S8). Värt nämna explicit i status att de är pank.

🟡 **Greven som "potentiellt hemlig allierad"** är intressant men oanvänt. Hans stat-block finns men ingen scenan beskriver hur sällskapet möter honom utom som "möjligen en lapp via en tjänare". Förbered en konkret scen.

🟡 **Trollkyrka-scenen** är optional men beroende av att sällskapet besöker. Om Sören (Mattias) verkligen vill agera på Mjöds ord, behöver scenen öppnas tydligare. Vad triggar att sällskapet går dit just denna kväll? Mjöds ord är färska, men Anders öde är akut. Logiskt prioriterar Sören Anders. Trollkyrka-scenen kommer aldrig.

🟢 **Fader Daniel som tipsare** — bra logiskt callback. Risk: spelarna minns inte vem Daniel är. Spara namnet till SL-info, säg bara *"prästen i Öregrund"* om någon frågar.

🟢 **"Klockan: 3-4 dagar Anders bryts, 5-7 Greta dödas, 2 veckor Severin lämnar"** — bra ramverk. Risk: spelarna vet inte detta och kan spela för lugnt. **Lösning:** låt Bror ha hört från Idas moster att *"Severin sade att han har två veckor till. Sedan blir det rep."* Konkret deadline.

---

### C. Stridbalans

#### Inga avsedda strider

Sessionen är spaning + planering. Bra. Men:

🟡 **Vad om spelarna anfaller Grevens herrgård direkt?** Severin (Adv 3) + 4 ryttare (minions) i samma scen. Spelarens skadepotential mot 4×Soak 4 minion-grupp + Severin (Soak 4, Wounds 16): teoretiskt möjligt men *mycket* farligt. Anders och Greta hålls inomhus = svårare räddning under strid.

**Lösning:** etablera explicit i prepen att direkt anfall = nästan TPK. Eller: ge spelarna en "smyg-väg" via Idas mosters nyckel som tydligt alternativ till våld.

🟡 **Inkvisitionsryttare antal-konflikt:** Stat-block säger "6 totalt, aldrig fler än 4 i samma scen". Idas berättelse säger "6-7 ryttare". Justera till samma antal. Min rek: 6 totalt, 4 hos herrgården, 2 patrullerande.

🟡 **Severin Coercion 5** — vid förhörsscen mot Anders/Greta är det redan över. Vid social scen mot sällskapet (om de väljer att möta honom) — han kan dominera samtalet. Det är OK om han ska vara skrämmande, men förbered hur du spelar att han *bryter* en spelarkaraktär socialt om han vill. Eller etablera att han är hövlig vid första mötet, sparar pressen för senare.

🟢 **Greven slåss inte.** Hans Wounds 12 är där för säkerhet. Bra.

---

### D. Pacing

**Tidsuppskattning från prepen:**
- Del 1 (Mjöd): 20-30 min
- Del 2 (Tröskeln): 15-20 min
- Del 3 (Skogens Krona): 20-30 min
- Del 4 (Spaning): 30-45 min
- Del 5 (Första akten): 30-45 min

**Summa:** 115-170 minuter. Plus recap, småprat, Mattias-paus efter Mjöd, eventuell Trollkyrka-scen (15 min) = 150-220 min. Ungefär 3-4 timmar.

🔴 **Cliffhangern är "TBD".** Det är fel ord på fel plats. En cliffhanger måste vara förberedd, inte improviserad. Om sessionen rinner ut utan tydlig avslutspunkt går spelarna hem med en fadd känsla.

**Lösning:** förbered TRE cliffhanger-scenarion baserat på spelarval:
- **Om de spanat:** Severin promenerar i mörkret, stannar upp, ser rakt mot deras gömställe. *"Ni borde inte vara där. Kom fram."* Bryt.
- **Om de planerar:** Greven söker upp dem genom Idas moster — *"jag vill prata. Ladan vid älven. Ensamma. Ikväll."* Bryt vid de går mot ladan.
- **Om de gör en första aktion:** den misslyckas precis. En ryttare skadas men flyr. Severin vet nu att de finns.

🟡 **Mittsektionen riskerar att rinna ut.** Tre uppslag i Del 4 = beslutsångest. *"Vad gör vi?"* kan ta 15 min av real-time prat. **Lösning:** låt Ida vid slutet av Del 3 säga något konkret: *"ni har två val tror jag — spaning eller direkt aktion. Båda är farliga. Men ni kan inte vänta."*

🟡 **Mjöd-scenen 30 min** kan svälla till 60 min om Mattias är i form. Det är OK men resten av kvällen krymper. Plan B: om Mjöd-scenen drar ut, klipp Trollkyrka-scenen helt (spara till S11) och flytta direkt till spaning.

🟢 **Öppning är bra.** Direkt återupptag från cliffhanger. Ingen administration.

🟢 **Variation god.** Social (Mjöd) → exploratorisk (skogen) → social (Ida) → planering → eventuell action. Rytm är OK.

---

### E. Stöddokument

**Finns:**
- ✅ Handout-kortet till Mattias (Mjöds ord) — utmärkt
- ✅ POST-IT-anteckningar
- ✅ Stat-blocks i prep

**Saknas:**
- ❌ **Karta över Tierp** — checklist säger "förbered". Behövs idag.
- ❌ **Skiss över Grevens herrgård** för Idas karta-handout. Idas mosters karta är central till räddningsplanen.
- ❌ **Severins JSON för Foundry**
- ❌ **Snabbreferens för Severin** vid social konfrontation (hans pool, förmågor, motivation-key)
- ❌ **Idas mosters namn** — improvisation
- ❌ **Foundry-tokens för Inkvisitionsryttare**

🟡 **Mjöd-handouten kan ges först EFTER scenen.** Bra noterat i prep. Förbered fysiskt papper INNAN spel.

---

### F. Regelkorrekthet

🔴 **"Inquisitor's Eye" och "Cold Logic" är custom-talanger utan tydlig regel.** Som ovan i sektion A.

🟡 **Severin Knowledge (Religion) 5 + Knowledge (Lore) 4** — Genesys tillåter Knowledge-specialiseringar (verifierat i 03_ch03_skills.md). OK.

🟡 **Inkvisitionsryttare: Riding 1** — Riding är en ovanlig skill i Genesys core. Verifiera om det finns. Om inte: byt till Survival eller Athletics för rid-relaterade slag.

🟡 **Greven Smooth Talker** — finns det i Genesys-grunden? Verifiera. Om inte: använd Convincing Demeanor (✦ till Charm) eller Plausible Deniability.

🟢 **Severin Soak 4** — Br 2 + 2 (lätt rustning under prästkåpa). Antagligen OK men specificera.

🟢 **Cool/Vigilance-flaggning** finns i POST-IT.

---

### G. Kontinuitet

🔴 **Sörens böneräkning ~990 → 1000 under Trollkyrka-scenen** är timing-känsligt. Han kan nå 1000 vid många olika tillfällen — en runda i strid, under spaning, under förhör. **Vad om han når 1000 *innan* Trollkyrka-scenen?** Då tappas den dramatiska kraften. **Lösning:** låt böneräkningen vara mjukt på 990, säg att den är "nära" och låt SL välja exakt timing. Eller: låt spelaren bestämma när Sören räknar de sista — det blir hans dramatiska val.

🟡 **Bror's konkreta info** — listad i Del 3. Funkar. Men Bror är räddningsbar VILLKORLIGT — beroende på spelarnas val i S9 (om de dödade Utgårdaloke är Bror död). Om Bror inte är med, vem ger informationen? Förbered alternativ.

🟡 **"Vad sällskapet gjorde för Idas familj"** är improvisation. Bra för flexibilitet men risk för icke-konsekvent svar. Bestäm i förväg, även om SL inte avslöjar förrän bordet kräver det. Förslag: *"Ni var de enda som inte skrattade åt min mor när hon dök upp efter att ha somnat i en lerig grav efter en begravning. Ni hjälpte henne hem."* Etablerar Idas mors karaktär (lite trasig, sårbar) och förklarar sympatin.

🟡 **"Idas hemliga rum"** nämnt i flödesschema men inte beskrivet. Är det rum bakom köket eller källaren? Mer detalj behövs.

🟡 **Skogens Krona-mysteriet** — "frö, ej aktivt än". OK, men SL behöver veta vad det är så att eventuella spelar-frågor inte etableras inkonsistens. **Förslag:** Skogens Krona står på en gammal kraftpunkt — lokalbefolkningen vet inte men marknadens väsen känner det. Det är *därför* sällskapet skyddades där (Ida väntade utan att veta varför). Detta öppnar för senare intriger där sällskapet upptäcker det.

🟢 **Mjöd-stenarna** (4 svarta) — adresserat i sektion B. Lös scenmekaniskt.

🟢 **Skuggmärket återställs vid sessionsstart** — Minnesryck-effekter. Bra.

🟢 **Anders och Greta JSON finns** — kan användas vid räddningsscen i S11.

🟢 **Maja-tråden** — borttagen. Men i S9-prep står det "räddningsbar 1" (Bror). Konsistent.

---

## Åtgärdslista (prioriterad)

### 🔴 Kritiskt (måste fixas innan spel)

- [ ] **Lös Mjöd + svartstenarna-konflikten.** Lägg in att Mjöd ler åt stenen och säger *"du behöver inte den ikväll. Jag tar inget."* Frigör scenen från mekanisk motsägelse.
- [ ] **Skriv Severins JSON för Foundry.** Stat-block finns redan, konvertera till JSON-format.
- [ ] **Definiera "Inquisitor's Eye" och "Cold Logic" som tydliga mekaniska effekter.** Min rek:
  - **Inquisitor's Eye:** Vid Coercion-uppgörelse, Severin uppgraderar svårigheten en gång (lila → röd ELLER +1 lila). Inte både +🟦 OCH ⬛.
  - **Cold Logic:** Vid Charm/Negotiation/Coercion mot Severin med argument som baseras på empati, familj, ångerfullhet eller barmhärtighet, uppgradera svårigheten en gång.
- [ ] **Förbered tre konkreta cliffhanger-scenarion** (spaning / Greven söker upp / första aktion misslyckas) istället för "TBD".

### 🟡 Varning (bör fixas)

- [ ] **Etablera vad värdshusvärden gör i Skogens Krona-scenen.** Är han hemma? Sett ut till sällskapet positivt eller negativt?
- [ ] **Modifiera Idas berättelse:** Anders har precis börjat ge namn. Severin vet *"Sören och två till"* men inte plats. Skapar tickande klocka.
- [ ] **Lägg till en NPC-driven plan-trigger** efter Del 3 (Ida säger *"ni måste välja: spaning eller aktion. Inte vänta."*). Annars rinner Del 4 ut.
- [ ] **Klargör Inkvisitionsryttare-numerär** (6 totalt, max 4 i scen). Justera Idas berättelse om hon säger 6-7.
- [ ] **Skriv kort markdown för Bror** (3-5 rader: vem, vad säger, hur hanteras).
- [ ] **Förbered alternativ informationskälla om Bror är död** (Utgårdaloke dödad-vägen i S9). Förslag: Maja återinförs som räddad i hans ställe, eller Idas moster har samma info.
- [ ] **Förbered konkret Greven-scen** för spelarna som vill möta honom. Lapp via tjänare → ladan vid älven → samtal.
- [ ] **Klargör "tickande klocka"** för spelarna. Bror eller Ida nämner *"Severin har sagt två veckor till. Sedan rep."*
- [ ] **Verifiera "Riding"-skill och "Smooth Talker"-talang** i Genesys-grunden. Byt om de inte finns.

### 🟢 Noteringar (kan fixas)

- [ ] **Bestäm vad sällskapet gjorde för Idas familj** i förväg (konsistens).
- [ ] **Etablera vad Skogens Krona är speciellt** (för SL, ej spelarna). Förslag: gammal kraftpunkt.
- [ ] **Namnge Idas moster.** Förslag: Birgit, Karin, Märta.
- [ ] **Beskriv "Idas hemliga rum"** (bakom köket, källare?).
- [ ] **Sörens böneräkning** — låt SL/Mattias välja exakt timing istället för att binda till Trollkyrka-scenen.
- [ ] **Specificera Severins rustning** för Soak 4 (lätt brigantine under prästkåpa?).
- [ ] **Specificera Grevens rustning** för Soak 3.

---

## Worst Case-scenarion

| Scenario | Vad händer | Förberett? | Risk |
|----------|-----------|------------|------|
| **Sören håller stenen mot hjärtat under Mjöd-scenen** | Mekanisk konflikt: scenen ska beröra honom men stenen "fångar honom inte". Stannar fram-frågan. | ❌ | 🔴 |
| **Värdshusvärden ser sällskapet komma in** | Vad gör han? Anmäler? Tigger om silver? Inte beskrivet. | ❌ | 🟡 |
| **Spelarna anfaller herrgården utan plan** | TPK-risk. 4 ryttare + Severin. | ⚠️ delvis | 🔴 |
| **Spelarna går aldrig till Trollkyrkan** | Mjöds uppdrag aldrig spelat. Rimlig konsekvens, men förlorad scen. | ✅ (optional) | 🟢 |
| **Bror dog i S9 (Utgårdaloke dödad)** | Hans info i Del 3 saknas. Vem berättar då? | ❌ | 🟡 |
| **Spelarna försöker prata med Severin direkt** | Han spelar artig, försöker värva Sören. Risk att social scen drar ut utan utfall. | ⚠️ delvis | 🟡 |
| **Spelarna går till Greven direkt och hotar honom** | Greven är feg, samarbetar tillfälligt — men sedan tvingas han välja kyrkans sida. Förrar dem. | ❌ | 🟡 |
| **Sessionen går snabbt och de planerar räddning på sista 30 min** | Cliffhanger oklart. Vad bryter vi vid? | ❌ | 🔴 |
| **Mattias är frånvarande igen** | Mjöd-scenen kan inte spelas. Hela kvällen tappar sin tematiska tyngd. | ⚠️ tänk | 🟡 |
| **Spelarna vill genast fly Tierp och hämta hjälp utifrån** | Var? Sigtuna? Anders och Greta dör under tiden. Är detta en accepterad väg? | ❌ | 🟡 |

---

## Sammanfattande omdöme

**Styrkor:**
- Mjöd-scenen är välskriven, känslomässigt tung, väl förberedd.
- Cliffhanger-strukturen (uppgång → fall) är tematiskt stark.
- NPC:er (Severin, Greven, Ida) har tydliga personligheter och roller.
- Bra integration av Bror som S9 → S10-länk.
- Realistic timing — 3-4 timmar fungerar.

**Svagheter:**
- Mjöd + svartstenarna är mekanisk kontradiktion som måste lösas.
- Severin custom-talanger för optimerade och vaga.
- Mittsektion (Del 4) saknar drivkraft — risk att rinna ut.
- Cliffhanger TBD = fel ord. Förbered tre alternativ.
- Skogens Krona-säkerhet (värden, Severins ovetande) hänger på lös tråd.
- Anders 2 veckor under förhör utan att ge namn är orealistiskt.

**Den enda stora frågan:** vad är spelarnas drivkraft från Del 3 till sessionsslutet? Om de är paralyserade av valens komplexitet drar Del 4 ut, Del 5 blir kort, cliffhangern blir platt. Lösningen är **en NPC eller händelse som tvingar handling** — Ida som säger "ni måste välja", eller en ryttare som ses i närheten av Skogens Krona som triggar adrenalin.

Lös de 4 kritiska + de 2-3 viktigaste varningarna, så är prepen redo.
