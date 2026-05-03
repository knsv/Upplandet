# Session 9 — Red Team-granskning

**Granskat material:** session-09-prep.md, session-08-summary.md, session-08-prep.md, campaign-status.md, befintliga NPC-JSON-filer
**Datum:** 2026-05-03
**Allvarlighetssammanfattning:** 🔴 5 kritiska | 🟡 9 varningar | 🟢 6 noteringar

---

## Exekutiv sammanfattning

Sessionen är **dramatiskt välskriven** men **operationellt halvfärdig**. Strukturen funkar, Mjöd-scenen är stark, cliffhangern brutal och tematiskt korrekt. Men: huvudantagonisten Utgårdaloke har inga JSON-stats, hans förmågor är delvis fabricerade ("Magic Mastery", "Bound Sorcerer" — finns ej i Genesys-grunden), tre boss-encounters i rad riskerar att kännas repetitiva, och tidsplanen för 4 timmar är optimistisk (8 delar med kompletta scen-läs-upp och en strukturerad strid med 3 faser räcker enkelt till 5+ timmar). Den största risken är **stridsbalansen i runda 1** där Utgårdaloke i full kraft (Adversary 3, Soak 6, Bindningsmagi) kan slå ut en spelarkaraktär innan sällskapet förstått mekaniken.

## Beredskapsgrad

```
NÄSTAN REDO ⚠️
```

Motivering: Narrativ-struktur är solid. Praktisk prep saknar JSON-stats för Utgårdaloke och Severin, har odefinierade custom-talanger, och tidsplanen behöver kortas eller delas upp på två sessioner.

---

## Fynd

### A. NPC-komplettering

| NSC | Markdown | JSON | Stats OK | Status |
|-----|----------|------|----------|--------|
| **Utgårdaloke** (huvudantagonist) | ✅ i prep | ❌ | ⚠️ fabricerade talanger | 🔴 |
| **Broder Severin** (S10-frö) | ✅ i prep | ❌ | ⚠️ Adversary 2 låg för Nemesis | 🟡 |
| **Unge Bror** (NPC-räddning) | ⚠️ minimal | ❌ | N/A (icke-stridande) | 🟡 |
| **Maja** (NPC-räddning) | ⚠️ minimal | ❌ | N/A (icke-stridande) | 🟢 |
| **Tomma-ögda aggressiva** (3 minions) | ✅ i prep | ❌ | ⚠️ ad-hoc i prep | 🟡 |
| **Ida** | ✅ tierp-npcs.md | ❌ | N/A (icke-stridande) | 🟢 |
| **Inkvisitionsryttare** (för S10) | ⚠️ minimal | ❌ | ⚠️ saknas helt | 🟢 (akut för S10) |
| **Mjöd** | ✅ befintlig | ❌ | N/A (ej strid) | 🟢 |
| **Drottning Månskära** | ✅ befintlig | ❌ | N/A (ej strid) | 🟢 |
| **Alva, Kvick** | ✅ befintliga | ❌ | N/A | 🟢 |

🔴 **Utgårdaloke saknar JSON.** Det är kvällens boss som dyker upp i tre encounter-faser. Utan token i Foundry blir initiativ, skadeapplicering och statusuppdatering ad hoc. **Risk:** repris av S8:s Foundry-friktion fast värre.

🔴 **"Magic Mastery" och "Bound Sorcerer" finns inte i Genesys-kärnreglerna.** "Magic Mastery" är ett namn som låter Genesys-aktigt men jag hittar det inte. "Bound Sorcerer" är uttryckligen markerat som custom. Båda behöver definieras i regelvänlig form INNAN spel — annars bränner SL tid på att improvisera regelmekanik mitt i strid.

🟡 **Tomma-ögda aggressiva har bara fragment-stats** ("Br 2, Soak 2, Wounds 4, klor Br+1"). Som minions OK om bordet är van, men inget JSON och inget namn. När striden öppnar och SL säger "tre aggressiva varelser springer mot er" — vilken token? Vilken initiativ-pool?

🟡 **Severin Adversary 2 är lågt för en Nemesis** som ska driva S10. Jämför Broder Egil från S5 — han var Adversary 3. Severin är inte fysiskt farlig men ska vara *psykologiskt* dominant. Adversary 3 motiverar det.

🟢 **Brors enkla token räcker.** Han är NPC-frö, inte stridande. OK att hålla minimal nu.

---

### B. Plotlogik

🔴 **"Han teleporterar mellan runorna" — hur vet sällskapet vart de ska?**
Prepen säger att Alva pekar mot Trollkyrkan efter stugans brand. Men efter runa 1 — hur vet de att gå till Drottningens träd? Och efter runa 2 — hur vet de att tredje runan är vid stugan? Två av runorna är redan lokaliserade från S8 (Trollkyrkan + Drottningens träd), men den tredje sägs ligga "där dimman är tätast". Sällskapet har aldrig hittat den. Riskerar att bli search-and-fail.

**Lösning:** Alva följer med och **kan känna runorna** (hon var Gretas lärares lärare, hon nämnde själv att hon "sett dem brinna rött"). Skriv in att hon leder dem till varje. Eller: Utgårdaloke själv pekar dit — *"jag är vid nästa, om ni vågar"* — varje gång han teleporterar.

🟡 **"Han håller löftet — bindningsmagin håller honom till hans ord på marknaden"** — men sällskapet vill att han LÄMNAR marknaden. Det är direkt kontradiktion. Antingen binder magin honom på marknaden OCH till hans löfte överallt (svår sell) eller magin släpper när runorna släpper. Klargör.

🟡 **"Bror har vandrat och kan ha sett saker."** Vad har han faktiskt sett? Spelarna kommer fråga honom så fort de kommer hem. Förbered konkret: Han var nära Tierp för 2-3 veckor sedan. Såg ryttare på vägen norrifrån. Hörde talas om "den bleke mannen". Inget mer. Annars improviserar SL i panik.

🟡 **Hur visste Utgårdaloke att de skulle komma till stugan?** I S8-cliffhangern står han på verandan när de springer fram. *"Jag har väntat. Alla kommer till slut."* OK för stugan — alla kommer dit förr eller senare. Men i S9 vet han att de jagar honom mellan runor. Han verkar veta deras position. Etablera: bindningsmagin gör att han känner var någon står ovanpå en runa. Annars känns han allvetande på fel sätt.

🟡 **Skogens Krona står ovetande — varför?** Severin har varit i Tierp i 2 veckor, gått till värdshuset en gång, frågat ut värden, gått igen. Om sällskapet är efterlysta vore det första logiska Severin gör att stationera en man vid värdshuset. Att Skogens Krona inte är konfiskerat är ett plotbeslut för spelmekanik (sällskapet behöver bas) men sviktar logiskt. Min förklaring: Greven har **tillsagt Severin** att Skogens Krona är hans privatkrog, hands off — gör det till Greven-frö. Eller: värden har betalat tystnadspengar till någon. Lös det före spel.

🟡 **Anders-replik via Ida.** *"Brevet brann för det skulle brinna. Inte för min skull."* — exakt så ordet "brann" i preteritum. Anders brände brevet i S6, vilket var för 1+ månad sedan. Men *cirkulärbrevet brände han för att skydda sällskapet*. Att han säger "inte för min skull" antyder att han offrade sig själv för dem — vilket han faktiskt gjorde. Repliken funkar, men SL behöver kunna förklara vad Anders menar om någon spelare frågar.

🟢 **Greven oklar.** Han hyser Inkvisitionen i sin herrgård. Är han kollaboratör (ny i S10), rädd, lojal mot kyrkan? Detta är OK att skjuta till S10-prep, men flagga det.

🟢 **"Maja söker sin mans namn"** — vacker tråd men helt oanvänd i S9. Onödig komplikation om den inte följs upp i S10.

---

### C. Stridbalans

#### Encounter 1 — De tomma-ögda aggressiva (Del 2)

3 minion-aggressiva. Br 2, Soak 2, Wounds 4. Sällskapet är fullt återställt från S8 (badet + Alvas salva). Lätt strid avsedd som öppning. Bedömning: **OK**.

#### Encounter 2 — Utgårdaloke runda 1 (vid Trollkyrkan)

**Hans pool i full kraft:**
- Bindningsmagi action: Will 5 + Magic 4 = 4 yA + 1 G, mot Discipline. Hard ◆◆◆ (3 lila) att bryta. Adversary 3 lägger 3 svarta tärningar på ALLA attacker mot honom.
- Stenstav: Br 3 + Melee → 3 yA. Br+2 = 5 skada, Crit 4, Stun 2.
- Eventuellt 1-2 minions från Stenröst.

**Sällskapets skadepotential per runda:**
- Sören med Ljusbringaren: ~10-12 skada per träff (efter Soak 6 → 4-6 skada faktiskt). Med Adversary 3 kan han missa.
- Lusse longbow: ~7-9 skada (efter Soak 6 → 1-3 skada faktiskt). Adversary 3 gör många bommar.
- Finn yxa: ~7-8 skada (Soak 6 → 1-2 skada). Adversary 3 = möjlig miss.

**Räkning:** För att slita 25 wounds från Utgårdaloke behöver sällskapet ~6-8 träffar. Med Adversary 3 (3 svarta) och Soak 6 är det 4-5 rundor minst. Under tiden kan han binda en spelare per runda.

🔴 **Bindningsmagi är överoptimerad.** En PC bunden = 1 strain/runda OCH ingen handling? Det står inte uttryckligen att bunden = ingen handling, men prepen antyder det ("Hard ◆◆◆ Discipline för att bryta"). Om Sören blir bunden runda 1 → resten av sällskapet bryter aldrig genom Adversary 3 + Soak 6 ensam.

**Lösning:** Bunden = 🟦🟦 setback på alla actions, NOT obegränsat handling. Eller: bryt-checken är Average ◆◆ (inte Hard). Klargör mekaniken.

🔴 **Adversary 3 + Soak 6 + 25 wounds är hård för en boss runda 1 i en kväll med tre boss-encounters.** Antingen sänker du Adversary 3 → 2, eller Soak 6 → 4, eller Wounds 25 → 18. Annars rinner runda 1 ut till 6+ rundor av "ingen träffar" → frustration. **Min rekommendation:** Adversary 3 är OK om du sänker Soak till 4 ELLER lägger in att stugbrand-explosionen i Del 1 redan har gjort 5 wounds skada på honom (narrativt motiverad försvagning).

#### Encounter 3 — Utgårdaloke runda 2 (vid Drottningens träd)

Adversary 2, Soak 5, Wounds 20. + Drottningens träd ger sällskapet 🟦. Mer balanserad, OK.

🟡 **Minnesryck-förmågan är tematiskt cool men mekaniskt vag.** "Förlorar tillfälligt en talang till nästa session" — vilken talang? Hur väljs den? Vad om talangen är passiv (t.ex. Toughened — försvinner då 2 wound threshold mid-strid)? Klargör: målet förlorar 1 RANG i en SKILL till nästa session, INTE en talang. Skill är tydligare och mer återställbar.

#### Encounter 4 — Utgårdaloke final (vid stugan)

Adversary 0, Soak 3, Wounds 12. Sällskapet kan slå honom ner snabbt — 1-2 träffar. **Risk: antiklimax.**

🟡 **Final-striden riskerar bli för snabb.** Om sällskapet sparat sina resurser (Lyckostenen, Alvas kristall används aldrig — se C nedan) och Sören öppnar med Ljusbringaren-triumph — Utgårdaloke är död runda 1. Finalen blev längre i runda 1 än i runda 3. Det är fel kurva.

**Lösning:** vid final, ge Utgårdaloke **en sista akt av desperation** — han brister in i sin sanna form (Adversary 2, Soak 4, regenerar 3 wounds/runda i 2 rundor) ELLER kallar 4-5 av de tomma-ögda aggressiva som omger sällskapet. **Detta står delvis i prepen ("kallar 2-3 tomma-ögda runda 1") men behöver förstärkas.** Annars tappas dramatik.

🟡 **Lyckostenen och Alvas kristall används aldrig.** Sällskapet fick två konkreta engångsföremål i S8. Om finalen är lätt (se ovan) använder de dem aldrig — Lyckostenen och kristallen åker med till nästa kampanj och förlorar relevans.

**Lösning:** Designa minst en situation där föremålen är frestande att använda. T.ex. om Sören blir bunden av Bindningsmagi och nästa Discipline är Daunting ◆◆◆◆, är Lyckostenen +🟦 frestande. Om Emma kritas av Stenrösten kallande en troll-rest, är Alvas kristall det enda som räddar henne snabbt.

#### Total kvällsbedömning

3 strider mot samma boss + 1 öppningsstrid mot tomma-ögda + en eventuell mid-fight mot stenröst-kallade minions = **4-5 stridsmoment på en kväll**. Det är mycket. Sömpressen kommer landa i runda 2 — sällskapet kommer vara trötta och börja säga "kan vi inte bara bryta runan?"

---

### D. Pacing

**Tidsuppskattning från prepen:**
- Del 1: 5-10 min
- Del 2: 20-30 min
- Del 3a: 25-30 min
- Del 3b: 25-30 min
- Del 3c: 30-40 min
- Del 4: 10-15 min
- Del 5: 15-20 min
- Del 6: 10-15 min

**Summa:** 140-190 minuter. Plus initiativ-fix, regelpaus, småprat, paus = 200-240 min minst. **Det är 4 timmar i optimistiskt scenario.**

🔴 **Tidsplanen är trångprägd.** Med S8:s erfarenhet (Mjöd-scenen tog 30 min trots 200-rader prep, badhusscenen + strid tog 90 min med Foundry-friktion) räknar jag med att S9 enkelt kan landa på 5-6 timmar.

**Lösningar:**
- **A) Kort version:** Klipp en av runa-encounters. Två runor istället för tre. Magikern blir svagare snabbare.
- **B) Splitt:** Acceptera att S9 går till Drottningens skuggmärken (Del 6). Mjöds avsked + Tierp-cliffhanger flyttas till S10 (som öppning).
- **C) Hard cut-off:** Spela tills cliffhangern naturligt landar; om vi är vid runa 2 kl 23:00, bryt där. Men då dör hela hemkomst-momentet.

**Min rekommendation:** Plan B. Mjöds avsked är för viktig för att jaga klockan. Spela klimax + skuggmärket + farväl i S9. Mjöds avsked + Tierp-cliffhanger som S10-öppning. Detta räddar också Mattias-momentet — han får inte en utbränd avsked-scen efter 5 timmars strid.

🟡 **Dramatisk kurva.** Tre nästan identiska boss-encounters (jaga → konfrontera → bryt runa) riskerar att bli repetitivt. Variera:
- Runa 1: konfrontation + dialog (han försöker övertala)
- Runa 2: kapplöpning (sällskapet måste nå runan innan han stärker den)
- Runa 3: full strid (ingen flykt)

🟡 **Öppningen är bra** — direkt återupptag från cliffhangern, ingen administration.

🟢 **Mjöd-scen + cliffhanger är väl-designade pacing-momenten.** Lugn → krasch.

---

### E. Stöddokument

**Finns:**
- ✅ Handout-kortet till Mattias (Mjöds ord)
- ✅ POST-IT-anteckningar
- ✅ Foundry-prep-checklista

**Saknas:**
- ❌ **Karta över marknaden med 3 runa-positioner.** Prepen säger "förbered karta" men inget existerande material. Behövs som visuell referens när sällskapet jagar.
- ❌ **Karta över Tierp** med Skogens Krona, kyrkan, Grevens herrgård. Kommer behövas direkt vid cliffhangern och definitivt i S10.
- ❌ **Snabbreferens för Utgårdaloke** — hans pool, hans förmågors svårigheter, hans aktuella status (Adversary, Soak, Wounds) som lätt uppdateras i strid. Skriv en 1-sidig SL-snabblapp.
- ❌ **Tabell över de tomma-ögda** — vilken är skal, vilken är förvirrad, vilken är aggressiv. SL behöver kunna säga "den fjärde är Bror" snabbt.

🟡 **Battle map för final-striden.** Aska, runan, dimma — behöver visualiseras. Snabbskiss räcker.

---

### F. Regelkorrekthet

🔴 **"Magic Mastery" och "Bound Sorcerer" finns inte i Genesys-kärnreglerna.** Skapa custom-stat tydligt:
- Magic skill (Genesys core) använder normalt Intellect eller Willpower.
- Custom: "Bound Sorcerer" = magi-attacker har räckvidd ENGAGED→SHORT förutom mellan ankarrunor (där han teleporterar).

🟡 **Bindningsmagi mekanik vag.** Vad gör det exakt? Mitt förslag:
> **Bindningsmagi (Action):** Magic check Hard ◆◆◆ (Will 5 + Magic 4 = 4 yA + 1 G). Targets PC i short range. Vid succé: mål bunden, +🟦🟦 setback på alla actions, kan inte röra sig. Bryt: Discipline Average ◆◆ som Action på efterföljande rundor.

🟡 **Minnesryck — välj skill, inte talang.** Som ovan: målet förlorar 1 rang i en specifik skill till nästa session.

🟡 **Stenröst** kallar tomma-ögda — det är en åtgärd som kostar 2 strain. Han har strain 18, så han kan göra det 9 ggr. Med 3 actions per encounter = ingen begränsning. Funkar.

🟡 **Terrifying 2** flaggas i POST-IT men inte uttryckligen i Utgårdalokes stat-block. Lägg till explicit i blocket.

🟢 **Severins Coercion 5 + Inquisitor's Eye** — funkar mekaniskt, men "Inquisitor's Eye" är custom utan tydlig regel. Definiera: vid förhör (Coercion mot Discipline), målet slår med 2 ⬛ setback, och Severin lägger till 🟦.

🟢 **Initiativ-skill** flaggad i POST-IT. Bra.

---

### G. Kontinuitet

🔴 **Sällskapets aktuella wounds/strain är ej uppdaterad.** Campaign-status visar S7 status. Efter S8: alla i stort sett återställda (badet + salvor). Men det står inte uttryckligen.

**Konkret för S9:**
- Sören: ~12-13/13 wounds, fortfarande har Critical Limp ELLER ej (avgör!)
- Lusse: ~10-11/11 wounds, Limp aktiv eller ej
- Finn: ~10-12/12 wounds, ⬛ från Näckens fiol — gick det bort vid morgonen? Det har gått en natt + en dag i marknadens tidsbubbla.
- Emma: 8/10 wounds (Alvas salva helade kritten)
- XP: 58 per spelare totalt

🟡 **Lusses Limp** — POST-IT flaggar avgör status, men mekaniken är inte längre relevant om sällskapet helt rörde sig till fots i S8 utan problem. Antagligen läkt narrativt. Bekräfta.

🟡 **Finns ⬛ från Näckens fiol** sade prepen S8 skulle försvinna "tills nästa morgon". Marknadens tid är konstig. Avgör: borta nu, eller fortfarande aktiv i S9?

🟡 **Bror i S3-summary:** *"Visade vänlighet mot Emma."* — inget specifikt om vad han gjorde. För att Emmas igenkänningsmoment ska landa, hjälper det att SL har en konkret detalj: t.ex. han gav henne en filt när hon skakade, eller han satt nära henne medan hon var rädd. Skriv in.

🟢 **Ulf Grönlöv saknas i S9-prepen.** Han var den som gav stölduppdraget, han är "byns ledare", hans lojalitet är okänd. När sällskapet kommer hem efter en månad kommer de fråga om Ulf. Förbered en mening: *"Ulf har försökt prata med Severin. Severin lyssnade inte."* (Står faktiskt i Idas berättelse — bra.)

🟢 **Cirkulärbrevet** — kontinuiteten håller. Anders brände det i S6, Severin kom ändå två veckor sedan = ny rapport från någon annanstans (Fader Daniel i Öregrund? Det skulle vara perfekt callback till S2).

🟢 **Sörens ~953/1000 Fader Vår** — har han fortsatt räkna under marknadssessionen? Kampanjen kan välja: ja (han har ~990 nu) eller nej (paus). Avgör.

---

## Åtgärdslista (prioriterad)

### 🔴 Kritiskt (måste fixas innan spel)

- [ ] **Skriv ut Utgårdalokes JSON för Foundry.** Stat-block i prep behöver konverteras. Använd nattmarknaden-npcs.md som referens för stil.
- [ ] **Definiera "Magic Mastery" och "Bound Sorcerer" som tydliga custom-talanger** med pool/effekt/kostnad. Lägg som custom-rules-block i prepen.
- [ ] **Specificera Bindningsmagi-mekaniken.** Vad innebär "bunden"? Setback eller no-action? Bryt-svårighet?
- [ ] **Sänk Utgårdalokes Soak runda 1 ELLER inför "skadad-av-stugbrand" (5 wounds redan tagna).** Annars riskerar runda 1 att kännas omöjlig.
- [ ] **Bestäm sessionsplan:** Plan B (klimax + skuggmärken + farväl i S9; Mjöds avsked + cliffhanger i S10) eller risken för 5-timmars-session.

### 🟡 Varning (bör fixas)

- [ ] **Skriv kort Severin-JSON** även om han bara nämns i ord — dyker upp i S10 omedelbart, prep ska vara klar i förväg.
- [ ] **Höj Severins Adversary till 3.** Han ska vara psykologiskt dominant.
- [ ] **Förstärk final-striden:** Utgårdaloke kallar 4-5 tomma-ögda runt sig OCH/eller "sann form" med wound-regen i 2 rundor.
- [ ] **Designa in användning av Lyckostenen och Alvas kristall.** Skriv in en bind-situation där Lyckostenen lockar, eller en kritsituation där kristallen behövs.
- [ ] **Förbered karta över marknaden** med 3 runor markerade.
- [ ] **Förbered enkel karta över Tierp.**
- [ ] **Skriv 1-sidig snabblapp för Utgårdaloke** med uppdateringsbar status (Adversary, Soak, Wounds — kryssa av allteftersom).
- [ ] **Klargör "håller sitt löfte"-mekaniken** om sällskapet låter Utgårdaloke leva.
- [ ] **Etablera hur Alva guidar sällskapet mellan runorna.** Annars kan jaktscenen kännas slumpmässig.

### 🟢 Noteringar (kan fixas)

- [ ] **Avgör Lusses Limp** och Finns ⬛-status. Skriv in i recap-anteckningarna.
- [ ] **Skriv en konkret detalj för Bror i S3** för att Emma-igenkänningen ska landa (vilken vänlig handling exakt).
- [ ] **Definiera kort vad som händer med Maja-tråden i S10** eller stryk henne (alternativt halvera tomma-ögda räddningsbara från 2 till 1).
- [ ] **Skriv en mening om Greven** för Idas berättelse — varför hyser han Severin?
- [ ] **Skriv in Sörens fortsatta böneräkning** (eller paus). Mattias kommer fråga.
- [ ] **Etablera vem som tipsade Inkvisitionen om Tierp** efter Anders brände brevet. (Fader Daniel? Logiskt.)

---

## Worst Case-scenarion

| Scenario | Vad händer | Förberett? | Risk |
|----------|-----------|------------|------|
| **Sören blir bunden runda 1 av Utgårdaloke** | Utan Sörens Ljusbringare har sällskapet svårt att bryta Soak 6. Striden drar ut. Möjlig knockout av annan PC. | ⚠️ Delvis (Bindningsmagi vag) | 🔴 |
| **Lusse försöker bryta runan utan att slå ut Utgårdaloke först** | Per-spelaren är taktisk — han kanske inser att man kan ignorera bossen och bryta runan direkt. Vad gör Utgårdaloke då? | ❌ | 🟡 |
| **Spelarna väljer "låt honom leva" vid finalen** | Bra förberett — han håller löfte, försvinner österut, lämnar öppen tråd. | ✅ | 🟢 |
| **Spelarna dödar Utgårdaloke direkt vid runa 1** | Han ska teleporta vid wounds < 8. Men vad om en triumf-träff gör 15 skada? Behövs "han teleporterar oavsett vid kritiskt läge"-regel. | ⚠️ | 🟡 |
| **Mattias är trött vid Mjöd-scenen efter 4h spel** | Scenen blir avhandlad snabbt, Mjöds ord landar inte. | ❌ (planera Plan B) | 🔴 |
| **Spelarna vill genast rusa till Tierp efter cliffhangern** | Ingen plan för "vi går nu". Sessionen är slut. | ✅ (cliffhanger = brytpunkt) | 🟢 |
| **Spelarna hoppas att rädda fler tomma-ögda än 2** | Magin släpper, fler dör som skal. Emotionell vikt — beredd? | ⚠️ | 🟡 |
| **Spelarna ifrågasätter varför Knös inte ingriper** | Knös = marknadsvakt. Marknaden är på sällskapets sida nu. Säg det uttryckligen vid behov. | ❌ | 🟡 |
| **Bror dör i strid (en aggressiv tomma-ögd träffar honom)** | Han är räddad, men inte stridande. Var står han fysiskt? | ❌ | 🟡 |

---

## Sammanfattande omdöme

**Styrkor:**
- Mjöd-scenen + cliffhanger = perfekt tematisk konstruktion. Använd Plan B så den inte tappas.
- Strukturen för 3-runa-jakt är dramaturgiskt rätt.
- Cliffhangern levererar momentum till S10.
- Utgårdalokes nedtrappning (Adversary 3→0) är smart designtanke.

**Svagheter:**
- Mekanisk halvfärdighet (custom-talanger, ingen JSON, vag bindningsregel).
- Tidsplan för optimistisk för 4 timmar — säker 5+.
- Final-striden riskerar antiklimax om Utgårdaloke faller på 1 runda.
- Sällskapets resurser (Lyckosten, kristall) saknar uppenbara användningstillfällen.

**Den enda stora frågan:** kör vi 8-delar-i-en-kväll och accepterar tidspressen, eller delar vi upp på två sessioner? Min starka rekommendation är dela. Mjöds avsked är för viktig för att tappas i en utdragen kvällsavslutning.
