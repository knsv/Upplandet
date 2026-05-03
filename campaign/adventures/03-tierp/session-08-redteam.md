# Session 8 — Red Team-granskning

**Granskat material:**
- `session-08-prep.md`
- `session-09-prep.md`
- `nattmarknaden.md`
- `session-07-analysis.md`
- `session-07-summary.md`
- `campaign-status.md`
- `npc-grimske-slavhandlare-Gk2pVr6sWx9Ly3Mn.json`
- `npc-vettarvakter-minion-Vv4rTu8wXy2Kl7Mn.json`
- `npc-knos-marknadsvakt-Kn8sPq2rWx5Jv9Bz.json`

**Datum:** 2026-04-19
**Allvarlighetssammanfattning:** 🔴 1 kritisk | 🟡 9 varningar | 🟢 8 noteringar

---

## Exekutiv sammanfattning

Prepen är **strukturellt stark** efter de senaste omarbetningarna. Plan B utan Mattias fungerar, Alva som ledtrådsnav bryter S7:s förlustmönster, och Drottningens kontrakt levererar ett konkret svar på spelarnas "fast"-känsla. Den **sociala encountern med Mjöd** är välgenomtänkt men har några mekaniska oklarheter som kan störa flytet. **Grimske-striden** är rimligt balanserad men prepen säger ett om Terrifying som JSON inte stödjer. **Sören som passiv NPC** är otillräckligt specificerat — spelarna kan ställa honom frågor som Knut måste improvisera. Inga dödsproblem, men några saker som kan skapa hicka om inte åtgärdade.

## Beredskapsgrad

```
NÄSTAN REDO ⚠️
```

Motivering: Kvällen kan köras som den står, men 3–4 varningar bör rättas för att minimera friktion. Inga strukturella hål, men detaljoklarheter.

---

## Fynd

### A. NPC-komplettering

| NSC | Markdown | JSON | Stats OK | Status |
|-----|----------|------|----------|--------|
| Mjöd | ✅ (nattmarknaden.md) | ❌ | ⚠️ inkonsistens | 🟡 |
| Finn (förtrollad) | PC | PC | ⚠️ oklar | 🟡 |
| Grimske | ✅ | ✅ | ⚠️ Terrifying fel | 🟡 |
| Vettarvakter | ✅ (JSON) | ✅ | ✅ | 🟢 |
| Knös | ✅ (JSON) | ✅ | ⚠️ Terrifying saknas | 🟡 |
| Alva | ✅ | N/A (passiv) | N/A | 🟢 |
| Ljuva | ✅ | N/A (passiv) | N/A | 🟢 |
| Silvertråd | ✅ | N/A (passiv) | N/A | 🟢 |
| Rot-Lisa | ✅ (bonus) | N/A | N/A | 🟢 |
| Eldätaren | ✅ (bonus) | N/A | N/A | 🟢 |
| Tomtarna | ✅ (bonus) | N/A | N/A | 🟢 |
| Kvick | ✅ | N/A (guide) | N/A | 🟢 |
| Drottningen | ✅ | N/A (dialog) | N/A | 🟢 |

**🟡 Grimske JSON saknar Terrifying** — Prepen listar Grimske under "Varelser med Terrifying i session 8", men JSON-filen har bara Adversary 1 och Nobody's Fool. Detta är en direkt inkonsistens. Antingen ta bort Grimske från Terrifying-listan i post-it, eller lägg till Terrifying 1 i JSON.

**🟡 Mjöd saknar Foundry JSON** — Mjöd är en Rival med Adversary 2 som används i kvällens viktigaste sociala scen, men det finns ingen JSON-fil i `campaign/characters/npcs/`. Knut får förlita sig på markdown-stats i prepen. Om Foundry behöver stat block för att representera henne (för social initiative), måste det göras nu.

**🟡 Knös JSON listar inte Terrifying** — Knös beskrivs som "naturkraft" med SPRING-varning men inte formellt Terrifying. Prepens post-it säger "Terrifying 2 minst". Inte relevant för S8 (han triggas inte) men bör rättas inför S9.

---

### B. Plotlogik

**🟡 Sören som passiv NPC — odefinierade gränser**
Prepen säger Sören är "passiv, korta repliker, tänker, ber". Men spelarna kommer oundvikligen att tilltala honom direkt: *"Sören, vad tycker du om Mjöds erbjudande?"* eller *"Ska vi slåss eller smyga?"*. Prepen ger ingen vägledning för dessa stunder.

**Fix:** Förbered 3–5 standardrepliker Knut kan använda:
- *(Sören nickar långsamt, återvänder till sina tankar.)*
- *"Jag litar på ditt omdöme, broder."*
- *"Som Herren vill. Eller... som ni vill."*
- *(Han räknar en böneräkning. 956. 957. Han hör inte.)*

**🟡 "Vi går utan Finn"-scenariot saknas**
Vad händer om spelarna säger: *"Han får stanna. Vi går."* Prepens sociala encounter antar att de vill få ut Finn. Prepen svarar inte på detta.

**Troligt resultat:** Fredrik (Finns spelare) kommer säga nej. Men prepen bör täcka scenariot. Kanske: Om sällskapet aktivt lämnar utan Finn, Mjöd surmulen men accepterar. Fredrik får välja: spelar han en permanent förlorad Finn, eller signalerar han att Finn vill bort?

**🟢 Lerpöls-sprattet utan agens**
Mjöd "puffar till" en PC och de hamnar i lerpöl. PC:erna har inget val i saken. Enligt railroading-feedback (*"inte kör över spelarval"*) kan detta kännas tvingat. Gör det lekfullt och skrattretande, men tvinga inte — kanske ge en Coordination Lätt ◆ för att duck, så det är spelarens val att "falla".

**🟡 Kvicks säkerhetsförsäkran blir en halvsanning**
Kvick säger: *"Vettarna är lagtrogna i grunden."* Men de håller fångar — vilket spelarna upptäcker 20 minuter senare. Spelarna kan uppfatta detta som Kvicks lögn snarare än hans begränsade kunskap. Förtydliga att Kvick **inte vet** om regelbrottet, annars skadar det förtroendet för honom.

**Fix:** Lägg till SL-not: *"Kvick vet inte att vettarna bryter reglerna nere. Om spelarna senare klagar på att han vilseledde dem, är Kvick genuint chockad."*

**🟢 Drottningens kontrakt — "minst 4 av 6 pusselbitar"**
Triggern är rimlig, men efter Badhuset har sällskapet **alla 6**. Det är tight: Drottningens kallelse sker direkt efter Badhuset. Rimligt men signalera det inte som "bara om de har 4" — i praktiken har de 6.

**🟢 Mjöds Fear-appellering ger effekt men ⬛**
Prepen säger hot mot Mjöd "fungerar men känns fult — ⬛ på uppföljning". Logiken är oklar: om det fungerar, varför straff? Förtydliga: appellering till Fear ger effekt (strain till Mjöd) men framtida tilltal mot henne får ⬛ (hon är nu försiktig).

---

### C. Stridbalans — Grimske + 4 Vettarvakter

**Motståndare:**
- Grimske (Rival): Br 3, Ag 4, Soak 5, Wounds 16, Adversary 1, Nobody's Fool, Skuggsmältning
- Vettarvakter (Minions ×4): Br 2, Soak 3, Wounds 4 per ruta (total 16 som grupp), Klor (Br+1 Crit 4)

**Sällskapets status efter pysselrummet:**
- Wounds återställda +2 per PC, strain återställd
- Finn: fortfarande ⬛ från Näcken, 1 permanent strain
- Emma: 8/10 wounds, hjärnskakning (narrativt)
- Sören: NPC, stödspelare
- Artefakter: Ljusbringaren, Jägarens Öga, Skuggklingan (alla med blå tärning mot övernaturliga)

**Beräkning:**
- Vettarvakter är minions = en grupp. När hälften dödas halveras skadeeffekten. Lätt att ta ut.
- Grimske: Soak 5 gör att han tar 1-2 wounds per bra träff. 16 wounds / ~2 = 8 rundor teoretiskt, men med advantage/triumph cuts snabbare.
- Praktiskt: ~3-5 rundor för hela striden.

**Action economy:**
- Sällskapet: 3 PC-ageranden + Emma + Sören (stöd) = ~4-5 actions/runda
- Motståndare: Grimske + 1 minion-grupp = 2 actions/runda

**Bedömning: 🟢 Balanserad**

**🟡 Grimskes Skuggsmältning och Ensnare 1 kan bli problem**
- Skuggsmältning låter honom dyka upp Short range var som helst — risk för isolering av en PC
- Ensnare 1 på Järnklor immobiliserar — om Lusse eller Finn fastnar i närstrid är de i svårigheter
- Inget TPK-hot, men kan skapa "en PC i kris"-moment

**🟢 Terrifying för Grimske?**
Prepen säger "verifiera JSON" — verifierat, **Grimske har INTE Terrifying**. Ta bort från Terrifying-listan.

**🟢 Badhuset som stridsterräng**
Prepen nämner "trånga utrymmen". Bra — det betyder spelarna inte kan utnyttja avstånd lika lätt. Bra för att balansera Lusses pilbåge.

**🟡 Silver Anathema för vettar?**
Vettar och vettrar är traditionellt sårbara för järn (inte silver). JSON nämner inte Silver Anathema för Grimske eller Vettarvakter. Ljusbringaren (silver) ger blå tärning mot övernaturliga, men triggar inte Silver Anathema automatiskt. Knut bör avgöra: är vettar tillräckligt övernaturliga för att räknas?

---

### D. Pacing och sessionsstruktur

**Tidsuppskattning totalt:**
| Segment | Tid |
|---------|-----|
| Trädgården (social encounter) | ~30-40 min |
| Kvicks vägledning | ~5 min |
| Badhuset övre (pyssel + frestelse) | ~15-20 min |
| Strid/smyg mot Grimske | ~20-30 min |
| Alvas berättelse + kristall + Ljuva + Silvertråd | ~20-25 min |
| Marknadsbonus (valfritt) | ~15-30 min |
| Drottningens kontrakt | ~15 min |
| Cliffhanger | ~5 min |

**Total:** 125-170 min = **2h 5min – 2h 50min**

**🟢 Pacing är rimlig för 3h-session** om man räknar in paus och spelarbrus. Bonus-scener är buffert.

**Dramatisk kurva:**
- **Öppning:** Emotionell (Mjöd, Finn förtrollad) — bra
- **Mitt:** Badhuset = lugn + frestelse + upptäckt — kontrast
- **Klimax:** Strid mot Grimske + Alvas exposition — bra kulmination
- **Slut:** Drottningens kontrakt + cliffhanger — aktivt avslut

**🟢 Stark kurva.** Variation mellan social, fysisk, och emotionell.

**🟢 Naturlig avslutningspunkt** — om tiden tar slut vid Alvas berättelse, kan sessionen sluta där med löftet om Drottningens kontrakt nästa gång.

**🟡 Trädgårdens social encounter kan svälla**
Strukturerade sociala encounters tenderar att ta längre tid än planerat, särskilt om Knut inte har spelat dem förut. 30 min är optimistiskt. Realistiskt 40-50 min.

**Fix:** Ha en mental "timer" — om encountern går över 45 min, pressa mot avslut. Låt Mjöd göra ett större drag mot att släppa Finn.

---

### E. Stöddokument

**🟢 Finns:**
- POST-IT till SL-skärmen med påminnelser ✅
- Terrifying-regelreferens ✅
- Nattmarknadens valutor som SL-referens ✅
- Pre-session handout till Mattias (förberedd text) ✅
- Ledtrådsöversikt-tabell ✅

**🟡 Saknas:**
- **1-sidig snabblapp för marknaden** (listad i checklistan men ej färdig)
- **Battle map eller skiss för Badhuset** (listad i checklistan men ej färdig)
- **Mjöds stat block i kompakt form** — stats finns spridda i prepen, ingen snabbreferens

**Fix:** Minst 15 minuter före sessionen, gör snabblappen för marknaden. Även en rough skiss av badhusets layout (3 bassänger övre, trappa bakom 3:e, nedre våning).

---

### F. Regelkorrekthet

**🟢 Genesys Social Encounter (Core s. 119-125)**
Prepen använder "strukturerad social encounter" med strain-threshold som "damage". Detta är **inte strikt RAW** — Genesys-reglerna är mer narrativa och abstrakta. Strain-threshold för social combat är en tolkning/husregel.

**Bedömning:** OK enligt "narrative över regler"-feedbacken. Men Knut bör veta att han förenklar — om spelarna vill argumentera reglerna, är det en extension, inte Core.

**🟡 "Finn 1 permanent strain" — oklart**
Betyder det:
A. Finns strain-threshold sänks permanent med 1? (hårt)
B. Finn börjar varje scen med 1 strain? (medium)
C. Bara narrativ påminnelse, ingen mekanik? (svagt)

Prepen säger "notera på karaktärsblad" — antyder (B). Förtydliga.

**🟡 PC "lockas" av Mjöd — oklar utväg**
Prepen säger: *"Den PC:n lockas — sätter sig bredvid Finn, accepterar te. Andra PC:er kan fortfarande vädja; återfår förnuftet när förtrollningen brutits för Finn."*

Men om Per (Lusses spelare) blir lockad, förlorar han aktiv roll i resten av scenen. Det kan kännas frustrerande.

**Fix:** Ge en tydlig "utväg" — kanske Discipline-slag varje runda med ökande svårighet för att bryta sig loss, ELLER en allierad som kan "skaka om" den lockade med Charm-slag.

**🟡 "Strain mot PC" — hur mycket?**
Om Mjöd lyckas med "Bjuda in en PC att stanna", tar PC:n strain. Prepen specificerar inte mängden. Förslag: strain = Mjöds Presence + success-symboler (typiskt 3-5 strain).

**🟢 Adversary-uppgradering**
Grimske Adversary 1 = uppgradera svårigheten 1 gång på alla stridsslag mot honom. Prepen sätter honom som "Svår ◆◆◆" i sociala encounter — det är INTE samma sak som Adversary-mekaniken. Oklar notation: Mjöds "Discipline Svår ◆◆◆ + ⬛⬛ (Adversary 2)" — Adversary ger upgrade, inte ⬛⬛. Rätt skulle vara: Svår uppgraderad 2 gånger = "Svår ◆◆◆ → Daunting ◆◆◆◆".

**Fix:** Om avsikten är två extra svarta tärningar, skriv "Svår ◆◆◆ + ⬛⬛ (från Mjöds träning)". Om Adversary 2, skriv "Daunting ◆◆◆◆ (Svår uppgraderad av Adversary 2)".

---

### G. Kontinuitet och kampanjlogik

**🟢 Öppna trådar från S7 som adresseras:**
- Finn räddad ✅
- Alva befriad ✅
- Stöldutredningen (kopplas via Rot-Lisas bekräftelse att väsen "betalar") ✅
- Marknadens bindning ✅

**🟢 Öppna trådar från S7 som väntar:**
- Runar har essens — ej aktiv ikväll, bra
- Inkvisitionen — inte närvarande på marknaden, OK
- Ljusets rörelse söderut — inte prioriterat ikväll, OK

**🟡 Emmas status vid sessionsstart**
Emma har "5/10 wounds, hjärnskakning från Bullrik". Hjärnskakning är narrativ men har ingen mekanisk effekt i prepen. Om Bullriks krit skulle ge **Critical Injury** enligt Genesys-regler, finns det en faktisk mekanisk effekt (strain threshold reduction, difficulty upgrade, etc.). Prepen hanterar det inte.

**Fix:** Bekräfta vad krit-tabellen gav Emma. Om det var "Stunned" eller "Unconscious", bör den ha lytt av nu. Om det var permanent, behövs notering.

**🟢 XP-status**
46 → 51 XP efter S7. Om spelarna köpt nya talanger/skills sedan S7, kanske prepen inte reflekterar det. Kolla innan session.

**🟢 Artefakterna används**
Ljusbringaren, Jägarens Öga, Skuggklingan är nämnda i stridsalternativet. Bra uppföljning.

**🟢 Bergtrollen (Grimtand, Lurkna, Bullrik)**
Ej direkt relevanta ikväll. Bra att de inte tvingas in — de fick sin tid i S7.

**🟢 Dannemora-hooken behålls via Ljuvas "bortanför gläntan"**
Förenklade profetian bibehåller hooket utan förvirring. Bra.

---

## Åtgärdslista (prioriterad)

### 🔴 Kritiskt (måste fixas)

- [ ] **Ingen kritisk åtgärd.** Prepen är kampabel som den står.

### 🟡 Varning (bör fixas innan spel)

- [ ] **Ta bort Grimske från Terrifying-listan** i POST-IT (line 42) — JSON har inte Terrifying för honom
- [ ] **Förbered 3-5 standardrepliker för Sören som NPC** — Knut behöver dem när spelarna direkt-frågar honom
- [ ] **Förtydliga "Finn 1 permanent strain"** — är det permanent threshold-sänkning, eller börjar han varje scen med 1 strain?
- [ ] **Förtydliga PC "lockas av Mjöd"** — ge explicit utväg (Discipline-slag per runda eller allierad-hjälp)
- [ ] **Specificera strain-skada mot PC** när Mjöd lyckas locka in dem (förslag: 3-5 strain)
- [ ] **Förtydliga "Svår ◆◆◆ + ⬛⬛" för Mjöd** — är det två svarta ELLER Adversary-uppgradering till Daunting? Välj ett och beskriv konsekvent
- [ ] **Lägg till SL-not om att Kvick inte vet om vettarnas regelbrott** — för att hans försäkran inte ska uppfattas som lögn
- [ ] **"Vi lämnar Finn"-scenario** — kort anvisning till Knut: om Fredrik signalerar att Finn vill stanna, låt honom göra det; annars står scenen stilla tills Fredrik agerar
- [ ] **Emmas hjärnskakning — mekanisk effekt?** — kontrollera kritträffen från S7 och avgör om det finns bestående effekt

### 🟢 Noteringar (kan fixas)

- [ ] Förbered 1-sidig snabblapp för marknaden (checklistan)
- [ ] Förbered rough skiss av Badhusets layout
- [ ] Förbered Mjöd stat block kompakt på ett kort
- [ ] Förtydliga "Fear-appellering fungerar men ⬛" — logiken
- [ ] Lerpöls-sprattet: ge en Coordination Lätt ◆ för att ducka (agensbevarande)
- [ ] Silver Anathema för vettar? — förbestämt ja/nej
- [ ] Knös JSON — lägg till Terrifying 2 inför S9
- [ ] Mjöd JSON i Foundry — skapas vid tillfälle

---

## Worst Case-scenarion

| Scenario | Vad händer | Förberett? | Risk |
|----------|-----------|------------|------|
| **Fredrik vill att Finn ska stanna i trädgården** | Finn förlorad som PC, eller Fredrik sätter Finn på paus | ❌ | 🟡 |
| **Per (Lusse) blir lockad av Mjöd** | Passiv spelare resten av scenen | ⚠️ delvis | 🟡 |
| **Spelarna vägrar förhandling — går direkt till våld mot Mjöd** | Förbannelse, ⬛⬛ på sociala slag resten av kvällen | ✅ | 🟢 |
| **Spelarna försöker smyga ur trädgården utan att väcka Finn** | Ej täckt i prep | ❌ | 🟡 |
| **Grimske använder Skuggsmältning och isolerar en PC** | Möjlig "PC i kris"-situation | ⚠️ | 🟡 |
| **Spelarna tar 150 silver någonstans (försök köpa Grimske)** | De har inget och kan inte | ✅ | 🟢 |
| **Knös triggas trots legitim strid** | Bör inte — marknadslagen på deras sida | ✅ | 🟢 |
| **Alva dör innan hon kan berätta** | Hela ledtrådssystemet faller | ✅ (hon är skyddad) | 🟢 |
| **Spelarna går direkt till Drottningen utan Badhuset** | De saknar pusselbitar, kontraktet utlöses inte | ⚠️ | 🟡 |
| **Mattias kommer oplanerat med** | Alla Sörens handouts relevanta igen, Del 2-3 kan aktiveras | ⚠️ | 🟢 |
| **Sören frågas direkt om viktiga beslut** | Knut improviserar | ⚠️ | 🟡 |
| **Tiden räcker inte för Drottningens kontrakt** | Cliffhanger blir svagare | ⚠️ | 🟡 |

---

## Sammanfattande bedömning

Prepen är **narrativt rik, strukturellt sund, och tydligt anpassad** till kvällens begränsningar (Mattias frånvarande, spelarnas "fast"-känsla). De största bristerna är **detaljoklarheter** i den sociala encountern — specifikt vad som händer när PC:er lockas, och hur Sören ska spelas när spelarna direkt-tilltalar honom.

**Styrkor:**
- Alva som ledtrådsnav löser S7:s förlustmönster
- Drottningens kontrakt ger konkret "imorgon bryter vi marknaden"-löfte
- Nattmarknadens valuta-sektion ger mekanisk konsistens
- Social encounter-ramen är välgenomtänkt

**Svagheter:**
- Sörens passivitet är underspecificerad
- Finn-permanent-strain oklar
- Mjöds Adversary-notation förvirrande
- Några edge cases (vi-lämnar-Finn, Per-lockas) ej täckta

**Total bedömning:** Med ~30 minuters förberedelse innan session (fixa gula varningar + snabblapp + skiss) är prepen klar för spel. Utan den förberedelsen: spelbar men med möjlig friktion.

---

*Red team-granskning utförd 2026-04-19, samma dag som sessionen spelas.*
