# Session 6 — Red Team-granskning

**Granskat material:**
- `campaign/adventures/03-tierp/session-06-prep.md`
- `campaign/adventures/03-tierp/nattmarknaden.md` (Del 1–4)
- `campaign/campaign-status.md`
- `campaign/sessions/session-05-summary.md`
- `campaign/characters/npcs/tierp-npcs.md`
- `campaign/characters/npcs/npc-skuggvarg-minion-Sm0hXy5dZs8Cv3Tu.json`
- `campaign/characters/npcs/npc-alfahanne-varg-Af7eUv2aWp5Zs0Qr.json`
- `campaign/characters/npcs/npc-dimvaktaren-Dv3kMn7pRs1Tw5Xz.json`

**Datum:** 22 mars 2026
**Allvarlighetssammanfattning:** 🔴 4 kritiska | 🟡 5 varningar | 🟢 5 noteringar

---

## Exekutiv sammanfattning

Sessionen har stark narrativ design med utmärkta läs-upp-texter, bra hook-struktur och en fascinerande marknad. Men det tekniska fundamentet har allvarliga brister. JSON-filerna för samtliga stridsvarelser har fel stats som inte matchar markdown-materialet — Foundry VTT kommer visa helt andra siffror än du har i preppen. Fyra av sju NSC:er som dyker upp i sessionen saknar JSON helt. Kampanjstatusen listar fortfarande Lusses pilbåge och Finns knivar som stulna, men i session 5 använde alla sina vapen — gruppen glömde subploten. **Rensa upp kampanjstatusen** och bestäm om stölden hände eller inte. Fixar du JSON-mismatcherna och städar kampanjstatusen är sessionen spelbar.

## Beredskapsgrad

```
NÄSTAN REDO ⚠️
```

Motivering: Narrativet är starkt, men tekniska JSON-problem och en ouppmärksammad vapenförlust riskerar att ställa till det vid bordet.

---

## Fynd

### A. NPC-komplettering

| NSC | Markdown | JSON | Stats matchar | Status |
|-----|----------|------|---------------|--------|
| Skuggvarg (minion ×3) | ✅ (3 ställen) | ✅ | ❌ **Soak, wounds, vapen FEL** | 🔴 |
| Alfahanne (rival) | ✅ | ✅ | ❌ **Brawn, soak, wounds ALLT FEL** | 🔴 |
| Vild vittra (minion ×4) | ✅ (nattmarknaden.md) | ❌ **Saknas helt** | N/A | 🔴 |
| Dimväktaren (rival) | ✅ | ⚠️ **Förkortad JSON** | ⚠️ Delvis | 🟡 |
| Kvick (tomtenisse) | ✅ (nattmarknaden.md) | ❌ **Saknas** | N/A | 🟡 |
| Knös (troll-vakt) | ⚠️ Nämns kort | ❌ **Saknas** | N/A | 🟢 |
| Ulf Grönlöv | ✅ | ✅ | ✅ | ✅ |
| Mor Greta | ✅ | ✅ | ✅ | ✅ |
| Fader Anders | ✅ | ✅ | ✅ | ✅ |
| Henrik Bågskansen | ✅ | ✅ | ✅ | ✅ |

---

#### 🔴 Skuggvarg (minion) — Tre versioner, ingen stämmer

Det finns **fyra olika stat blocks** för skuggvargar i materialet:

| Källa | Brawn | Agility | Soak | Wounds | Vapen-skada | Vapen-krit | Qualities |
|-------|-------|---------|------|--------|-------------|------------|-----------|
| `session-06-prep.md` | 3 | 3 | 3 | 4 | — | — | — |
| `nattmarknaden.md` | 3 | 3 | 3 | 4 | Br+2 | 3 | Vicious 1 |
| **JSON** (`npc-skuggvarg-minion`) | 3 | 3 | **2** | **5** | Br+2 | **4** | **Inga** |
| `tierp-npcs.md` | 3 | **4** | 3 | **6** | 5 | 4 | Vicious 1 |

**Problem:**
- JSON-soak är 2 men Brawn är 3 (utan rustning borde soak = Brawn = 3)
- JSON-wounds är 5, prep/nattmarknaden säger 4
- JSON-vapnet saknar Vicious 1 och har Crit 4 istället för 3
- Tierp-NPCs-filen har en helt annan version (Agility 4, Wounds 6)
- **Vid import till Foundry VTT får du FEL soak, FEL wounds, FEL vapendata**

**Åtgärd:** Bestäm vilken version som gäller (nattmarknaden.md verkar vara den senaste). Uppdatera JSON och tierp-npcs.md.

---

#### 🔴 Alfahanne (rival) — JSON är en helt annan varelse

| Fält | Markdown (nattmarknaden.md) | JSON |
|------|---------------------------|------|
| Brawn | **4** | **3** |
| Soak | **4** | **2** |
| Wounds | **14** | **10** |
| Brawl | **3** | **2** |
| Vapen-krit | **2** | **4** |
| Vapen qualities | **Vicious 2, Knockdown** | **Knockdown** (saknar Vicious) |

JSON-alfahannen har Brawn 3 och Soak 2 — den är svagare än en minion-skuggvarg i markdown. **Foundry VTT visar en papperstiger istället för en alfavarg.**

**Åtgärd:** Gör om JSON helt från nattmarknaden.md-specen.

---

#### 🔴 Vilda vittror — Ingen JSON alls

4 minions i encounter 2. Markdown-stats finns i nattmarknaden.md men **det finns ingen Foundry VTT JSON**. Du måste antingen:
- Skapa JSON för dem
- Köra dem helt manuellt (inga tokens, inga automatiska slag)

---

#### 🟡 Dimväktaren — JSON förkortad, importeras inte

`npc-dimvaktaren-Dv3kMn7pRs1Tw5Xz.json` har förkortade items utan standard Foundry VTT-schema (saknar `_stats`, `effects`, `folder`, `flags`, `ownership`, `sort`). **Filen importeras troligen inte korrekt i Foundry VTT.**

Stats i JSON matchar markdown (Brawn 4, Soak 5, Wounds 18, Adversary 1). Men formatet är fel.

**Åtgärd:** Expandera JSON till fullständigt Foundry VTT-schema (se templates i `.claude/skills/adversary-creator/references/`).

---

#### 🟡 Kvick — Saknar NPC-fil

Kvick är sessionens viktigaste nya NPC-interaktion (guide, regelförklarare, kampanjexposition). Han har en bra beskrivning i nattmarknaden.md men:
- Ingen separat NPC-markdown i `campaign/characters/npcs/`
- Ingen JSON
- Inga stats (behövs troligen inte för strid, men Charm/Deception kan vara relevant)

**Åtgärd:** Skapa en kort NPC-markdown. JSON behövs inte om han aldrig hamnar i strid.

---

### B. Plotlogik

#### 🟢 Hook-strukturen — Stark

Två separata hooks (Ulf = konkret, Greta = emotionell) som leder till samma plats utan att spelarna vet det. Smart design. Spelarna har information från minst två källor.

Men: **Three Clue Rule bara halvt uppfylld.** Om spelarna ignorerar BÅDE Ulf och Greta finns ingen tredje ledtråd. Förslag: låt en kolarbetare eller Frebo-bonde nämna marknaden spontant om spelarna dröjer.

#### 🟡 "Kan inte lämna" — Railroading-risk

Session-preppen säger: *"Spelarna kan INTE lämna. Kvick berättar ärligt."*

Det här är berättigat av plotten (jötunrunor binder marknaden), men det kan upplevas som railroading om spelarna reagerar starkt. **Vad händer om spelarna insisterar på att lämna?**

Nattmarknaden.md nämner Survival (Formidabel ◆◆◆◆) för att nå dimväggen — men aldrig att det finns en emotionell anledning att stanna frivilligt. Förslag: ge spelarna en omedelbar personlig anledning att vilja hjälpa INNAN de inser att de är fångade. T.ex. Gretas uppdrag (befria Alva) ger dem eget motiv.

#### 🟢 Stölduppdraget — Oavslutad tråd

Paddköpmannen på Stora Marknaden har Henriks salt och stulna varor. Men materialet adresserar aldrig hur Ulf reagerar på "tjuven var en magisk padda som betalade med ekollon." Kommer han att acceptera det? Vill han ha sakerna tillbaka? Kan spelarna köpa tillbaka dem?

Inte kritiskt för session 6 (det händer kanske i session 7), men värt att förbereda.

#### 🟡 Dimväktarens frågor — Sören-fällan

Sörens fråga: *"Vad tror du på?"* — dimväktaren accepterar tvivel men inte lögn. Sören har en aktiv troskris (session 3–5). Om spelaren svarar med Sörens dogmatiska "Gud och kyrkan" kan dimväktaren tolka det som lögn (Sören offrade på ett hedniskt altare). **Hur bedömer du det?** Materialet ger ingen vägledning om Sörens specifika situation.

**Förslag:** Förbered en intern linje: "Dimväktaren hör *intentionen*, inte orden. Sören som genuint kämpar med sin tro är ärlig nog."

---

### C. Stridbalans

#### 🟢 Lusses pilbåge — Spökproblem i kampanjstatusen

Kampanjstatusen listar Lusses pilbåge och Finns knivar som "stulna" sedan session 4 (Skogens Krona-incidenten). **Men i session 5-transkriptet använder Lusse sin pilbåge mot Broder Egil** (`[01:27:53]` "Min båge och en pil", `[02:38:54]` "Tryck i bågen") och **Sören har sin sköld** (`[02:12:44]` "Nu hakar jag av skölden"). Hela gruppen glömde bort stölden och spelade vidare normalt.

**Åtgärd:** Bestäm en av två saker:
1. **Retcon:** Vapnen var aldrig borta (eller de fick tillbaka dem off-screen). Rensa kampanjstatusen.
2. **Reaktivera subploten:** Påpeka det i session 6 — "Lusse, var fick du egentligen tag i din pilbåge?" Elegant men riskerar att skapa förvirring.

**Rekommendation:** Retcon. Ingen vinner på att gräva upp en glömd subplot. Ta bort "Stulna/saknade föremål" från kampanjstatusen.

#### Encounter 1: Skuggvargar — Rimlig (om stats fixas)

**Action economy:** 4 motståndare (3 minions agerar som grupp + 1 rival) = 2 ageranden vs 3 PCs = rimligt.

**Skadeckapacitet per runda:**
- Minion-grupp (3 st, Brawl): ~5 skada (Brawn 3 + baseDamage 2 = 5, minus soak)
- Alfahanne: ~6 skada (Brawn 4 + 2 = 6, minus soak)
- Sällskapets soak: Sören ~5 (Brawn 3 + ringbrynja 2), Lusse ~3 (Brawn 2 + läder 1?), Finn ~3

**Bedömning:** Rimlig. 2–3 rundor. Terrifying 1 kostar strain. Sällskapet bör vinna med måttliga förluster. ✅

Men: Lusse och Sören startar med ~8/12 och ~11/13 wounds. De tål inte lika mycket som i prep-designen.

#### Encounter 2: Vittror — Lätt (med social utväg)

4 minions med soak 2 och wounds 4 är ingen verklig utmaning. Social lösning (Charm Svår ◆◆◆) finns. Bra designval — varierar pacing efter en strid. ✅

#### 🟡 Encounter 3: Dimväktaren — Potentiellt brutal

**Om sällskapet måste slåss:**
- Soak 5 + halv skada från icke-magiska vapen = extremt slitstarkt
- Wounds 18 = långdragen strid
- Adversary 1 = svårare att träffa
- Brawl 3 + Ensnare 2 + "kan inte tala" = kvävning tar ur spelare

**Ljusbringaren gör full skada** (artefakt), men sällskapet har precis slagits mot vargar och vittror. Om Sören har ~7/13 wounds och ~5/14 strain vid det här laget, och Lusse ~5/12...

**Risknivå:** Dimväktaren kan knocka en PC om de ljuger och striden drar ut. Inte TPK-risk, men en redan sargad grupp mot en soak-5-rival med 18 wounds kan ta 4–5 rundor.

**Mildrande faktor:** Spelarna förväntas svara ärligt, inte slåss. Striden är ett fail-state. Men: vara förberedd på att det kan hända.

#### 🟡 Tre strider utan helning

Prep-materialet nämner INGEN helning mellan de tre encountrarna. Emma har Healing — ska hon hela under resan? Greta är inte med. Materialet borde adressera:
- Kan Emma hela mellan striderna? (Medicine Genomsnittlig ◆◆, kanske 1 gång per PC)
- Finns vila-tillfällen?
- Alternativt: ska resursutmattningen vara avsiktlig?

---

### D. Pacing

#### Tidsuppskattning

| Del | Uppskattad tid | Kommentar |
|-----|---------------|-----------|
| Återkomst | 20 min | Realistisk |
| Hooks | 15 min | **Troligen 25-30 min** — Greta-scenen har emotionellt djup, spelarna frågar |
| Eskilsta & Frebo | 10 min | Realistisk om effektivt |
| Encounter 1 | 15 min | Realistisk |
| Encounter 2 | 10 min | 5 min om social, 15 om strid |
| Encounter 3 | 15 min | **20-30 min** om strid, 10 om fredlig |
| Ankomst | 15 min | **20-30 min** — mycket exposition (Kvick, regler, "kan inte lämna") |
| Utforskning | 30+ min | **60+ min** — fritt utforskande, shopping, spelhåla, rollspel |
| **Total** | **~130 min prep** | **~180-240 min reell** |

**Bedömning:** Inom 3–4-timmarsfönstret, men tight om alla tre striderna tar tid. Buffert finns i utforskningen (kan kortas). ✅

#### 🟢 Dramatisk kurva — Bra uppbyggnad

```
Energi
  ▲
  │        ╱╲ Enc1  ╱╲ Enc3
  │   ╱╲  ╱  ╲   ╱╲╱  ╲     ╱──── Utforskning
  │  ╱  ╲╱    ╲ ╱       ╲  ╱
  │ ╱ Hooks    Enc2      ╲╱ Ankomst (wow-moment)
  │╱ Återkomst
  └─────────────────────────────────► Tid
```

Bra variation: social → strid → social möjlig → strid/prov → wow-ankomst → fri utforskning.

#### 🟢 Cliffhanger — Flexibel men vag

Fem föreslagna cliffhangers, alla bra. Men risken är att ingen faller naturligt. **Förslag:** Välj EN som default-ending om inget hakar spontant.

---

### E. Stöddokument

| Dokument | Status | Kommentar |
|----------|--------|-----------|
| Läs-upp-texter | ✅ | Flera utmärkta (ankomst, dimväktaren, marknaden) |
| Battle maps | ❌ | Inga nämnda för någon av tre encounters | 🟡 |
| Handouts | ⚠️ | Halvmåne-symbol nämns (ledtråd) men ingen fysisk handout | 🟢 |
| Snabbreferens | ✅ | Session-06-prep har encounter-stats-tabell |
| Marknadskarta | ✅ | ASCII-karta finns i nattmarknaden.md |
| Dimväktarens frågor | ✅ | Per karaktär, bra |
| Kvicks röst | ⚠️ | Noterat men inga övade repliker utöver nattmarknaden.md |

#### 🟡 Inga battle maps

Tre encounters utan battle maps. Skuggvargar i skog, vittror på kulle, dimväktaren vid portal. Behövs det? Beror på spelstil. Men om Foundry VTT används bör det finnas åtminstone enkla maps.

---

### F. Regelkorrekthet

#### 🔴 Soak-beräkningar i JSON

| Varelse | JSON Soak | JSON Brawn | Rustning | Korrekt Soak |
|---------|-----------|------------|----------|-------------|
| Skuggvarg (minion) | **2** | 3 | Ingen | **3** |
| Alfahanne | **2** | 3 | Ingen | **3** (eller 4 om Brawn=4 som i md) |
| Dimväktaren | 5 | 4 | +1 dimkropp? | Oklart — borde specificeras |

Soak = Brawn + rustning. Två av tre JSON-filer har fel soak.

#### 🟡 Dimväktarens "halv skada icke-magiskt"

Denna förmåga finns inte som standard i Genesys. Det är en hemmagjord regel. Det fungerar narrativt, men:
- Hur hanteras udda tal? Avrunda upp eller ner?
- Gäller det bara baseskada eller även Pierce?
- Materialet säger "artefakter gör full skada" — gäller det Skuggklingan (som inte har Silver-quality)?

**Förslag:** Förtydliga: "Icke-magiska vapen gör halv skada (avrunda uppåt). Ljusbringaren, Jägarens Öga-förstärkta anfall, och silvervapen gör full skada."

#### 🟢 Terrifying — Skill-referens

Alla skuggvargar har "Terrifying 1" — detta triggar en Fear-check (Discipline-slag). Preppen anger "Discipline Lätt ◆" — korrekt för Fear 1. ✅

---

### G. Kontinuitet

#### 🟢 Stulna vapen — Glömd subplot

Kampanjstatusen listar Lusses pilbåge, Finns knivar och Sörens sköld som stulna/borta sedan session 4. Men i session 5 använde alla sina vapen utan kommentar. Gruppen glömde bort det.

**Rekommendation:** Retcon det tyst. Ta bort "Stulna/saknade föremål" från kampanjstatusen. Alternativt: om du vill koppla det till paddköpmannen på marknaden (han samlar mänskovaror), kan det bli en kul koppling — men det riskerar att skapa förvirring snarare än drama.

#### 🟡 Emma under session 6

Emma följer med sällskapet men materialet nämner henne bara vid helning (Del 1). Under tre encounters och marknadsvandring:
- Vad gör hon under strid? Gömmer sig? Försöker hela?
- Hur reagerar hon på marknaden? (Övernaturlig tonåring möter övernaturlig marknad)
- Stör Terrifying-checks henne? (Hon har ingen Discipline-rank)
- Kvick nämner "mänskor" — inkluderar det Emma? (Hon är witchborn)

**Förslag:** Förbered 2–3 Emma-reaktioner (marknad, vittror, dimväktaren).

#### 🟢 Inkvisitionen — Rätt nivå

Anders bränner brevet i sessionens öppning. Hotet minskar men försvinner inte (andra prästgårdar). Bra balans — det ger andrum utan att eliminera spänningen.

#### 🟢 Sörens botgöring — Adresserad

Kort scen i öppningen. Bra — det visar att konsekvenser från session 5 följs upp utan att ta för mycket tid.

---

## Åtgärdslista (prioriterad)

### 🔴 Kritiskt (måste fixas)

- [ ] **Fixa Alfahanne-JSON.** Brawn ska vara 4, Soak 4, Wounds 14, Brawl 3, Vicious 2 + Knockdown, Crit 2. Nuvarande JSON visar en halvstark varelse.
- [ ] **Fixa Skuggvarg-minion-JSON.** Soak ska vara 3, Wounds 4 (inte 5), vapnet ska ha Crit 3 + Vicious 1.
- [ ] **Skapa Vittra-JSON.** 4 minions, Br 2, Ag 3, Soak 2, Wounds 4, Slunga (Br+1, Crit 5, Medium) + Stenklubba (Br+2, Crit 5, Engaged).
- [ ] **Fixa Dimväktaren-JSON.** Expandera till fullständigt Foundry VTT-schema. Nuvarande förkortade format importeras inte.

### 🟡 Varning (bör fixas)

- [ ] **Förbered Sörens dimväktar-svar.** Vad räknas som "ärligt" givet hans troskris?
- [ ] **Adressera helning mellan encounters.** Kan Emma hela 1 gång under vandringen?
- [ ] **Skriv Emma-reaktioner.** 2–3 korta reaktioner: marknad, vittror, dimväktaren.
- [ ] **Battle maps** — Skapa eller hitta enkla maps om Foundry VTT används.
- [ ] **Skapa NPC-markdown för Kvick.** Kort beskrivning, personlighet, vad han vet, eventuella stats.

### 🟢 Noteringar (kan fixas)

- [ ] **Rensa kampanjstatusen** — Ta bort "Stulna/saknade föremål" (alla använde sina vapen i session 5).
- [ ] **Synka tierp-npcs.md skuggvarg** med nattmarknadens version.
- [ ] **Förtydliga dimväktarens "halv skada"-regel.** Hur avrundas? Gäller Pierce? Gäller artefakter som inte har Silver?
- [ ] **Förbered plan B om ingen hook hakar** (tredje ledtråd till marknaden).
- [ ] **Välj en default-cliffhanger** om inget faller naturligt.

---

## Worst Case-scenarion

| Scenario | Vad händer | Förberett? | Risk |
|----------|-----------|------------|------|
| Spelarna vägrar BÅDA hooks | Inget leder dem till marknaden. Sessionen stannar. | ❌ Ingen tredje ledtråd | 🟡 |
| Spelarna ljuger för dimväktaren | Strid mot Soak 5, 18 wounds rival. Sällskapet redan sargat. | ✅ Stats + konsekvenser beskrivna | 🟡 |
| Spelarna dödar dimväktaren | ⬛ på sociala slag med Drottningen. | ✅ Beskrivs i nattmarknaden.md | 🟢 |
| Spelarna vägrar stanna på marknaden | Stigarna leder tillbaka. Survival Formidabel. | ✅ Beskrivet | 🟡 |
| Någon nämner de "stulna" vapnen | Förvirring — alla använde dem i session 5. Retcon eller förklara? | ⚠️ Kampanjstatus felaktig | 🟢 |
| Emma lockas av marknaden (häxkraft) | Inget förberett för hur marknadsväsen reagerar på witchborn | ❌ | 🟡 |
| Sören attackerar Paddköpmannen (han säljer stöldgods) | Knös ingriper. Men det bryter marknadens regler — konsekvenser? | ⚠️ Regler finns men inte specifik situation | 🟡 |
