# Session 7 — Red Team-granskning

**Granskat material:**
- `campaign/adventures/03-tierp/session-07-prep.md`
- `campaign/adventures/03-tierp/nattmarknaden.md` (Del 3–6)
- `campaign/campaign-status.md`
- `campaign/sessions/session-06-summary.md`
- `campaign/sessions/session-06-analysis.md`
- `campaign/characters/npcs/nattmarknaden-npcs.md`
- NPC JSON-filer för bergtroll-bröderna

**Datum:** 5 april 2026
**Allvarlighetssammanfattning:** 🔴 3 kritiska | 🟡 6 varningar | 🟢 5 noteringar

---

## Exekutiv sammanfattning

Sessionen har en stark struktur med nu-justerad Holmgången-strid, ett väl dokumenterat navigationsdiagram, och tydlig ledtrådsstruktur enligt Three Clue Rule. **Men tre områden där spelarna KAN hamna i strid saknar helt JSON-filer eller har ofullständiga stats**: Vettarnas Badhus (Grimske + 4 vettarvakter), Knös (om någon bryter marknadsfreden), och potentiellt Fader Sten. Om spelarna går för våldslösning i Badhuset står du utan Foundry-tokens och ofullständiga stats vid bordet. Kampanjstatus är inte uppdaterad efter session 6 vilket betyder att du inte har en exakt bild av spelarnas wounds/strain inför sessionen. Fixar du JSON-filerna för Grimske + vettarvakter och uppdaterar kampanjstatus är sessionen spelbar — men **pacing-risken är hög** eftersom preppen rymmer 9 områden + huvudplot-ledtrådar + en strid på 3 timmar.

## Beredskapsgrad

```
NÄSTAN REDO ⚠️
```

**Motivering:** Narrativ och stridsbalans är i ordning, men tekniska luckor i NPC-dokumentationen och hög pacing-risk gör sessionen sårbar om spelarna går åt oväntat håll.

---

## Fynd

### A. NPC-komplettering

| NSC | Markdown | JSON | Stats matchar | Status |
|-----|----------|------|---------------|--------|
| **Grimtand** (bergtroll) | ✅ prep + nattmarknaden.md | ✅ | ✅ | 🟢 |
| **Lurkna** (bergtroll) | ✅ prep + nattmarknaden.md | ✅ | ✅ | 🟢 |
| **Bullrik** (bergtroll) | ✅ prep + nattmarknaden.md | ✅ | ✅ | 🟢 |
| **Kvick** | ✅ nattmarknaden-npcs.md | ❌ | N/A (ej strid) | 🟢 |
| **Knös** | ✅ nattmarknaden-npcs.md | ❌ | ⚠️ **Inkonsekvens** | 🟡 |
| **Drottning Halvmåne** | ✅ nattmarknaden.md | ❌ | N/A (ej strid) | 🟢 |
| **Grimske** (Vettarnas Badhus) | ✅ nattmarknaden.md | ❌ **Saknas** | N/A | 🔴 |
| **Vettarvakter ×4** (minions) | ✅ nattmarknaden.md | ❌ **Saknas** | N/A | 🔴 |
| **Mjöd** (Trädgårdsmästaren) | ✅ nattmarknaden.md | ❌ | ⚠️ (social utmaning) | 🟡 |
| **Fader Sten** (Trollkyrkan) | ✅ nattmarknaden.md | ❌ | N/A (ej strid) | 🟢 |
| **Alva, Ljuva, Silvertråd** | ✅ nattmarknaden.md | ❌ | N/A (ej strid) | 🟢 |
| **Skuggflickan, Räven, Mossskägg** (Lögnarkungen) | ✅ nattmarknaden.md | ❌ | ⚠️ (social) | 🟡 |

---

#### 🔴 Grimske + Vettarvakter — JSON saknas helt

Om spelarna väljer **våld** i Vettarnas Badhus (alternativ 1 av 4 i preppen) blir det strid mot:
- **Grimske** (Rival): Br 3, Ag 4, Soak 5, Wounds 16, Järnklor (Br+2, Crit 3, Pierce 1, Ensnare 1) + Skuggsmältning
- **4 vettarvakter** (Minions): Br 2, Ag 3, Soak 3, Wounds 4 var, Klor (Br+1, Crit 4)

Detta är **rimligt troligt** att hända. Sörens moraliska profil och Lusses temperament gör att våldslösning är en naturlig första instinkt när de ser älvorna i järnhalsband.

**Problem:**
- Inga tokens i Foundry VTT
- Inget stat block att dra upp snabbt
- Ensnare 1 och Skuggsmältning är icke-triviala mekaniker att komma ihåg på stående fot

**Åtgärd:** Skapa JSON för Grimske (Rival) + Vettarvakter (Minion-grupp) FÖRE sessionen. Använd samma mönster som bergtroll-filerna.

---

#### 🟡 Knös — Stats-inkonsekvens (20 vs 48 wounds)

**Session 6 summary säger:** *"Det sägs att Knös har 48 wound,"* — Kvicks varning.

**nattmarknaden-npcs.md säger:** Wounds 20, Soak 7, Adversary 2, Durable 2, skada 8+Knockdown, Regeneration 2.

**Två möjliga tolkningar:**
1. Kvick ljög/överdrev för att skrämma spelarna (fungerar narrativt)
2. Stats i markdown är fel

Om spelarna utmanar Knös med full kraft och finner att han har "bara" 20 wounds kan de tro att de kan vinna — vilket markdown själv säger är en "naturkraft de inte kan vinna mot".

**Åtgärd:** Bestäm vilket som gäller. Rekommendation: behåll 20 wounds mekaniskt men låt Kvick fortsätta hävda 48 (han vet inte bättre). Notera detta i preppen.

---

#### 🟡 Lögnarkungen-motståndare — bara rankningar, inga stats

Skuggflickan, Räven och Mossskägg har bara Deception-rangningar (3, 4, 1) i preppen. Om spelet blir socialt intensivt kanske du vill ha fler stats (Presence, Willpower, Cunning) för att svara på spelarnas slag.

**Åtgärd:** Inte kritiskt, men förbered 2-3 punkter per motståndare (Deception, Charm, eventuellt stridsstats om Skuggflickan någonsin blir hotfull).

---

#### 🟡 Mjöd (Njutningens Trädgård) — saknar fullständiga stats

nattmarknaden.md har delstats för Mjöd (Charm 5, Deception 4, Discipline 3, Adversary 2) men:
- Ingen soak/wounds (vad händer om spelarna bryter marknadsfreden och attackerar?)
- Ingen JSON

Om Finn förlorar i "Tre lögner och en sanning" och en annan PC försöker våld: oförberett.

**Åtgärd:** Notera soak/wounds för Mjöd som säkerhetsåtgärd, även om strid inte är planerad.

---

### B. Plotlogik

#### 🟢 Three Clue Rule — Tillräckligt täckt

5 huvudplot-ledtrådar från 5 olika källor + 5 bonusledtrådar = god redundans. Även om spelarna bara besöker 2-3 områden bör de nå alla tre kärninsikter.

#### 🟡 Drottningens implicit löfte — Kan vara för subtilt

Den nya formuleringen *"skulle jag vara mycket uppskattsam"* är bra, men:

**Problem:** Spelarna måste **först gå tillbaka till Drottningen** efter att ha samlat ledtrådar. Om de inte gör det, når de aldrig denna dialog.

**Vad om de bara fokuserar på Alva och går tillbaka till Portalen för att lämna?** De stannar fast. Kvick säger "ni behöver skuggmärket". De frågar "hur får vi det?". Då har du två val:
1. Kvick säger: *"Drottningen ger det. Gå till henne."* (direkt anvisning)
2. De söker själva svar → tidspress

**Åtgärd:** Förbered Kvicks formulering om spelarna inte själva tänker besöka Drottningen. Han bör säga det som en uppmuntran, inte en pil.

#### 🟡 Ulf-uppdraget — ofullständigt löst

Spelarna fick Ulfs uppdrag i session 4. I session 6 upptäckte de att "tjuvar" egentligen är väsen som "köper" med tre viskningar. Men:
- Hur rapporterar de detta till Ulf?
- Vill Ulf ha sakerna tillbaka?
- Vad är acceptabel lösning?

Session 7-preppen nämner inte hur denna plottråd avslutas. Det riskerar att bli en olöst tråd i session 8.

**Åtgärd:** Förbered Ulfs reaktion på sanningen. Är det nog att stölderna upphör (om de gör det efter S8)? Vill han ha 25 silver tillbaka av förskottet?

#### 🟢 Skuggvandrarna utanför Siarens Stuga — Bra varningssignal

De tysta, tomma figurerna utanför stugan ger visuell varning. Bra designval — spelarna ser konsekvensen av Utgårdalokes verk utan att SL behöver säga det rakt ut.

#### 🟡 Dannemora-kopplingen — kräver SL-aktivitet

Bergtroll-bröderna kommer från Dannemora. Skymning (Tomtarna) nämner Dannemora. Ljuvas profetia nämner Dannemora. Men:
- Tre separata källor nämner det utan att explicit koppla
- Om spelarna inte frågar varför bergtrollen lämnade sin gruva, försvinner kopplingen
- Efter-strid-scenen där Grimtand berättar är den enda garanterade kopplingen

**Åtgärd:** Säkerställ att minst EN NSC spontant kopplar: *"Har ni hört? Bergtrollen kom också från Dannemora. Jag har hört det flera gånger nu. Något händer där."*

---

### C. Stridbalans

#### Encounter 1: Holmgången (Bergtroll-bröderna)

**Balans (justerad):**
- 3 rivals, total wounds 34
- Grimtand (12w, Adversary 1, Slagregn, Knockdown) = farligast
- Lurkna (10w, Brawl 3, Accurate) = snabb flanke
- Bullrik (12w, Soak 5, Stenhud) = slitstark

**Spelarnas kapacitet:**
- Sören (troligen full efter helning på marknaden eller Ljusbringaren i strid): ~13 wounds, Soak 5
- Finn: ~12 wounds, Soak 3
- Lusse: ~12 wounds, Soak 3
- Emma: ~10 wounds (stödjande)

**Bedömning:** ✅ Balanserad efter justering. 3-4 rundor. Ringens regler eliminerar TPK-risk.

**Risk:** Om Grimtand fixerar Finn eller Lusse (Soak 3) + Slagregn + Knockdown → PC knockad snabbt. Men ingen dör pga ringens regler.

**Action economy:** 3v3 (+ Emma). Jämnt. Lurkna och Bullrik kan flankas bort med Athletics/Coordination ◆◆ → skapar 1v1 + 2v2.

#### Encounter 2: Grimske + Vettarvakter (om spelarna väljer våld)

**Farligt scenario:** Spelarna i Vettarnas Badhus, ser älvorna i järnhalsband, Sören/Lusse reagerar med våld.

**Balans:**
- Grimske (Rival): Soak 5, Wounds 16, Adversary 1, Järnklor med **Pierce 1 + Ensnare 1**
- Vettarvakter (4 minions): Soak 3, Wounds 4 var, Klor Br+1 Crit 4

**Action economy:** 2 ageranden (Grimske + minion-grupp) vs 3 PCs = balanserat, MEN:

**Kritiska risker:**
1. **Trånga utrymmen** i badhuset → PC:er kan bli fångade i Engaged
2. **Ensnare 1** = immobilized, farligt vid hög damage
3. **Bryter marknadsfreden** → Knös kommer inom 2-3 rundor
4. **Ingen helning garanterad efteråt** (till skillnad från Holmgången)
5. **Wet hot slippery bathhouse** — miljöfaktorer är inte specificerade

**Total risk:** 🟡 Utmanande men balanserad på pappret. Risk för knockouts om striden drar ut.

**Problem:** Detta är en plausibel strid, men **JSON saknas** och **Ensnare-mekaniken** kan vara svår att applicera snabbt.

**Åtgärd:** Förbered detta som en riktig stridsencounter, inte bara som en fotnot. Skapa JSON.

#### 🟢 Knös är INTE en strid

Knös är en naturkraft. Preppen är tydlig — om spelarna attackerar honom ska det vara hopplöst. Det är OK att hoppa över balansering eftersom striden är fail-state.

#### 🟢 Ingen vila mellan encounters specificerad

Preppen nämner inte helning mellan Holmgången och eventuell Grimske-strid. Men Holmgången helar båda sidor automatiskt, så det är inbyggd i mekaniken.

---

### D. Pacing

#### 🔴 Sessionens omfattning är för stor

**Tidsuppskattning (3 timmar session):**

| Del | Tid (optimistisk) | Tid (realistisk) |
|-----|-------------------|-------------------|
| Knös & skuggmärket | 15 min | 20 min |
| Samla information | 15 min | 25 min |
| **Holmgången-strid** | 20 min | 30 min |
| 3 sidouppdrag (Trollkyrkan, Trädgården, Tomtarna) | 30 min | 60 min |
| **Vettarnas Badhus + Alva** | 30 min | 45 min |
| Drottningens återbesök | 15 min | 20 min |
| Huvudplot-samling | 15 min | 20 min |
| Cliffhanger | 5 min | 10 min |
| **Total** | **~145 min** | **~230 min (3h 50min)** |

**Problem:** Realistisk tidsåtgång överstiger sessionstiden. Spelarna har 9 områden + sidouppdrag att välja bland. De kommer INTE hinna med allt.

**Risk:** Session 7 blir för ambitiös och alla viktiga saker hinns inte med. Session 8 får börja mitt i marknaden istället för med Utgårdaloke-striden.

**Åtgärd:**
1. **Prioritera Alva-befrielsen + huvudplot-ledtrådarna.** De MÅSTE hinnas med.
2. **Holmgången-striden är BRA att få in** men inte kritisk för framsteg.
3. **Sidouppdrag (Trollkyrkan, Trädgården, Tomtarna) är ICKE-kritiska** — låt spelarna välja 1-2, inte alla.
4. **Förbered en snabbare väg för Drottningens återbesök** om tiden tryter.

#### 🟡 Sessionens öppning — samma risk som session 6

Sessionens första 30 minuter i session 6 gick åt till smalltalk + inköp. Session 7 öppnar med Knös-konfrontationen, vilket är bättre, men:
- Spelarna har varit borta i 2 veckor
- De kan behöva 10 min för att komma ihåg var de var

**Åtgärd:** Öppna med **dramatik** (Knös närmar sig, marken skakar) innan prat. Visa vad som är på spel.

#### 🟢 Dramatisk kurva — Bra uppbyggnad

```
Energi
  ▲
  │         ╱╲ Holmgången               Siarens
  │        ╱  ╲                ╱─╲      Stuga
  │   ╱───╯    ╰─── Utforskning ─╯  ╲  ╱
  │  ╱                               ╲╱ Drottningen
  │ ╱ Knös                            Cliffhanger
  └──────────────────────────────────► Tid
```

Strid tidigt + spänning mot slutet. ✅

#### 🟢 Cliffhanger — Flera alternativ förberedda

4 olika cliffhangers beroende på vad som hänt. Bra flexibilitet.

---

### E. Stöddokument

| Dokument | Status | Kommentar |
|----------|--------|-----------|
| Läs-upp-texter | ✅ | Flera utmärkta (Holmgången, Portalen, Drottningen) |
| Battle map för Holmgången | ❌ | Ingen specifik karta — bara generell marknadskarta |
| Marknadens karta | ✅ | Mermaid-diagram + ASCII i nattmarknaden.md |
| Battlemap-prompt | ✅ | AI-prompt finns för AI-generation |
| Handouts | ⚠️ | Halvmånestenen nämns men ingen fysisk handout |
| Snabbreferens | ✅ | Snabbreferenstabell i session-07-prep |
| Ledtrådsguide | ✅ | Klart dokumenterad (efter diskussion) |

#### 🟡 Inget battle map för Holmgången

Holmgången är en cirkulär arena. Om du kör striden i Foundry behöver du en arena-karta (även enkel).

**Åtgärd:** En enkel cirkulär ring ritad i Foundry eller hämtad från stock-maps räcker. 30 min arbete.

---

### F. Regelkorrekthet

#### 🟢 Bergtroll-stats verifierade

JSON matchar markdown efter justering. Adversary 1 + Terrifying 1 tydligt noterade.

#### 🔴 Terrifying-checks kom aldrig med i session 6

Enligt session-06-analysis: *"Preppen specificerade Terrifying 1 för alla skuggvargar → triggar Discipline Lätt ◆ Fear-check. Det slogs ALDRIG."*

Bergtrollen har också Terrifying 1 (Grimtand). **Om du glömmer det igen förlorar du en strain-mekanik.**

**Åtgärd:** Skriv post-it: **"Terrifying 1 = Discipline Lätt ◆ första rundan"**. Ha framme på skärmen.

#### 🟡 "Slagregn" är en hemmagjord förmåga

Grimtands "Slagregn" (2 attacker en runda) är inte standard Genesys. Det fungerar men:
- Hur löses 2 attacker mekaniskt? Två separata pooler? Samma pool med delad framgång?
- Kostar det strain? Motståndare är Rivals, inte Nemesis — de har ingen strain-pool

**Åtgärd:** Förtydliga: *"En action → två Brawl-attacker mot samma eller olika mål. Slå två separata pooler."*

#### 🟡 "Stenhud" — första träff halv skada, men hur räknas "första"?

Bullriks Stenhud halverar första träffen. Men:
- Räknas det första SOM TRÄFFAR eller första SOM RIKTAS MOT?
- Vad om två PC:er attackerar samtidigt?

**Åtgärd:** Specificera: *"Första träffen som GÖR SKADA efter soak. Efterföljande träffar räknas normalt."*

#### 🟢 Athletics/Coordination ◆◆ för flanke-hindring

Standardmekanik för att "grabba" en motståndare. Korrekt.

---

### G. Kontinuitet

#### 🔴 Kampanjstatus ej uppdaterad efter session 6

**Kampanjstatus säger:** *"Senast uppdaterad: Efter session 5. Nuvarande plats: Brödernas Grav — Dag 3."*

**Verkligheten:** Sällskapet är på Nattmarknaden, Emma med dem, alla är i olika skador efter skuggvargarna.

**Problem:** Du har ingen sammanfattad bild av:
- Exakta wounds/strain per PC inför session 7
- XP-totaler efter session 6
- Aktuella artefakter och deras tillstånd
- Subplot-status (Ljusbringaren glöder blått när? Jägarens Öga triggas mot vad?)

**Åtgärd:** Uppdatera kampanjstatus-filen inför sessionen. Minst wounds/strain-kolumnen och "Nuvarande plats"-sektionen.

#### 🟢 Stulna vapen retconade ✅

Från kampanjstatus: *"Betrakta vapnen som aldrig förlorade."* Rent.

#### 🟡 Emma — rollen oklar i session 7

Preppen nämner Emma som "witchborn-kompass" men:
- Har Emma ett eget sidouppdrag/moment? (Nej)
- Vad händer om hon försöker hela under Holmgången? (Ringens regler - kan hon?)
- Triggers specifikt för henne: paddköpmannen bugar för henne, väsen vill handla med hennes hår/mjölk/blod

**Åtgärd:** Förbered 2-3 Emma-specifika reaktioner: när de går förbi Svamphandlaren, i Vettarnas Badhus, vid älvorna.

#### 🟡 Inkvisitionen — var är de under marknadens-tid?

Spelarna har varit på marknaden i vad som känns som en natt men är i verkligheten flera dagar enligt nattmarknaden.md Del 6. Inkvisitionen rör sig i Uppland. När de kommer tillbaka till Tierp:
- Har inkvisitionen hunnit fram till Tierp?
- Är Anders fortfarande trygg?

**Åtgärd:** Inte kritiskt för session 7 (de är fortfarande fast), men bör förberedas för session 8.

#### 🟢 Artefakternas signaler

Preppen listar artefakt-signaler som checklista. Bra (detta missades i session 6).

---

## Åtgärdslista (prioriterad)

### 🔴 Kritiskt (måste fixas)

- [ ] **Skapa JSON för Grimske.** Stats från nattmarknaden.md: Br 3, Ag 4, Soak 5, Wounds 16, Adversary 1. Järnklor Br+2 Crit 3 Pierce 1 Ensnare 1. Skuggsmältning-förmåga.
- [ ] **Skapa JSON för Vettarvakter (minion-grupp ×4).** Br 2, Ag 3, Soak 3, Wounds 4 var. Klor Br+1 Crit 4.
- [ ] **Uppdatera kampanjstatus.** Minst wounds/strain och nuvarande plats. Helst XP-totaler och artefakt-status.
- [ ] **Förbered tempo-prioritering.** Session 7 kan inte hinna med allt. Vilken är din minsta acceptabla "success"-nivå?

### 🟡 Varning (bör fixas)

- [ ] **Bekräfta Knös wounds** — 20 eller 48? Skriv in i nattmarknaden-npcs.md.
- [ ] **Terrifying 1 post-it** — Ha framme. Glömdes i session 6.
- [ ] **Förtydliga Slagregn-mekaniken.** 2 pooler eller delad?
- [ ] **Förtydliga Stenhud-triggern.** Första träff som GÖR SKADA.
- [ ] **Battle map för Holmgången.** Cirkulär arena, röda runor runt kanten.
- [ ] **Förbered Ulfs reaktion** på sanningen om stölderna.
- [ ] **Förbered 2-3 Emma-specifika moment** för marknaden.
- [ ] **Förbered Kvicks "prod" mot Drottningen** om spelarna inte själva tänker besöka henne.

### 🟢 Noteringar (kan fixas)

- [ ] Skapa stats för Lögnarkungen-motståndare (om Finn går dit).
- [ ] Notera Mjöds soak/wounds som säkerhet.
- [ ] Säkerställ att Dannemora nämns spontant av minst en NSC.
- [ ] Förbered Inkvisitionens rörelse under tidsskippen.
- [ ] Halvmåne-handout fysiskt (papper eller bild i Foundry).

---

## Worst Case-scenarion

| Scenario | Vad händer | Förberett? | Risk |
|----------|-----------|------------|------|
| Spelarna går direkt till Vettarnas Badhus och attackerar Grimske | Strid mot 1 Rival + 4 Minions, trånga utrymmen, Knös på 2-3 rundor | ❌ **JSON saknas** | 🔴 |
| Spelarna vägrar utmaningen i Holmgången | Bergtrollen hånar men går ej vidare. Ingen helning. | ⚠️ | 🟡 |
| Spelarna ignorerar Drottningen | Får aldrig höra "mycket uppskattsam"-erbjudandet | ⚠️ Plan B via Kvick | 🟡 |
| Spelarna dödar Grimtand trots ringens regler | Ringens magi aktiveras — knockout istället för död. Bröderna har inget kvar att ge spelarna | ✅ | 🟢 |
| Spelarna hittar nedre våningen MEN köper fri älvorna för 150 silver | Ingen strid. Diamant-elegant lösning. De har ~225 silver. | ✅ | 🟢 |
| Spelarna tar sig till Siarens stuga för tidigt | Spegeln drar in dem (⬛ på Willpower tills de lämnar). Ej strid | ✅ | 🟡 |
| Spelarna dricker blått honung/svart drömvatten från Stora Marknaden | Oförutsägbart — beror på SL-improvisation | ❌ | 🟡 |
| Trollkyrkan triggar Sörens troskris på ett nytt sätt | Rollspelstung scen. Trons Eld-frestelsen (Discipline ◆◆◆) | ✅ | 🟢 |
| Emma försöker hjälpa någon på marknaden (helar ett väsen) | Väsens-reaktion: bugar, ger gåva, vill handla vidare? | ⚠️ | 🟡 |
| Spelarna försöker bryta bindningsrunorna direkt | De ger upp stugans läge. Kan de göra det utan att möta Utgårdaloke? | ✅ (session 8-material) | 🟢 |

---

## Sammanfattande bedömning

**Session 7 är VÄLBYGGD ur narrativt perspektiv** — hook-struktur, ledtrådar, Drottningens implicita löfte, och Holmgången som "helnings-strid" är alla smarta designval. **Men sessionen har 3 tekniska luckor** som kan svida vid bordet: Grimske + vettarvakterna saknar JSON, kampanjstatus är förinlagd, och pacingen är för ambitiös för 3 timmar.

**Om du fixar JSON-filerna och prioriterar rigoröst** (Alva + huvudplot > sidouppdrag) är sessionen spelbar och förmodligen kul. Holmgången-striden ger adrenalin, Alva-befrielsen ger narrativ payoff, och Drottningens implicita löfte ger riktning mot session 8.

**Största hotet:** Pacing. Förbered dig mentalt på att skippa minst 2 av de 4 sidouppdragen (Trollkyrkan, Trädgården, Tomtarna, Spelhålan) om tiden tryter.

**Tre ord:** Välbyggd, tempo-utmanande, nästan-redo.
