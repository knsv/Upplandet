---
name: session-analyzer
description: Analyserar en TTRPG-spelsession genom att jämföra transkript mot förberedelsematerial. Identifierar vad som fungerade, vad som inte fungerade, regelproblem, pacing, stridbalans och spelledarprestation. Ger konkreta förbättringsförslag. Triggas av "analysera session", "session review", "vad gick bra", "vad kan vi förbättra", eller liknande.
allowed-tools: [Read, Glob, Grep, Agent]
---

# Sessionsanalys — Spelledarens efterarbete

Denna skill analyserar en avslutad spelsession i detalj. Den jämför vad som faktiskt hände (transkriptet) med vad som var planerat (prep-materialet) och utvärderar allt från regelanvändning till stämning och pacing.

## Språk

**Analysen ska ALLTID skrivas på svenska.**

## Syfte

Syftet är att hjälpa spelledaren att:
- Förstå vad som fungerade och varför
- Identifiera vad som inte fungerade och hur det kan undvikas
- Hitta regelfel och lära sig rätt tillämpning
- Optimera för maximalt kul vid bordet

---

## Filhantering

### Ingående filer (läs)
Skillen behöver läsa följande filer:

1. **Transkriptet** — `campaign/sessions/session-NN-transcript.md` (det råa transkriptet)
2. **Sammanfattningen** — `campaign/sessions/session-NN-summary.md` (för överblick)
3. **Prep-materialet** — Sessionsförberedelsen i `campaign/adventures/`. Sök efter filer med `session-NN-prep.md` eller relevanta eventfiler
4. **Kampanjstatus** — `campaign/campaign-status.md`
5. **Genesys-regler** — `.claude/skills/genesys-rpg/reference/rules/` (slå upp specifika regler vid behov)
6. **Inquisition-setting** — `.claude/skills/upplandet-campaign/references/invisitionen/` (vid settingfrågor)
7. **NPC-filer** — `campaign/characters/npcs/` (för att verifiera stat blocks)
8. **CLAUDE.md** — Projektets grundregler och namnkonventioner

### Utgående fil (skriv)
Analysen sparas som:
```
campaign/sessions/session-NN-analysis.md
```

---

## Steg-för-steg arbetsflöde

### 1. Samla material

Innan analysen börjar, läs in allt relevant material:

1. Identifiera sessionsnumret (från argument eller fråga användaren)
2. Läs transkriptet (`session-NN-transcript.md`) — det råa, ofiltrerade transkriptet
3. Läs sammanfattningen (`session-NN-summary.md`) — för snabb överblick
4. Hitta och läs prep-materialet:
   - Sök i `campaign/adventures/` efter `session-NN-prep.md`
   - Sök efter relaterade eventfiler (t.ex. `event-brodernas-grav.md`)
   - Om inget prep-material finns, notera det och analysera sessionen utan jämförelse
5. Läs kampanjstatus för kontext
6. Läs relevanta regelkapitel vid behov (se regelreferenser nedan)

### 2. Analysera

Gå igenom transkriptet systematiskt och utvärdera följande områden:

---

#### A. Prep vs verklighet — Använde vi materialet väl?

Jämför prep-materialet med vad som faktiskt hände. **Fokus ligger på kvaliteten i hur materialet användes — inte på hur mycket som hanns med.** Att bara nå hälften av planerade moment är helt okej om det som spelades var bra. Det intressanta är:

- **Vad avvek?** Identifiera avvikelser från planen. För varje avvikelse:
  - Beskriv vad som hände istället
  - Bedöm: var avvikelsen **bra** (organisk, spelardriven, bättre än planen) eller **dålig** (förvirring, tappat tråd)?
  - Om bra: vad kan vi lära oss för framtida prep?
  - Om dålig: vad orsakade avvikelsen och hur undviker vi den?
- **Användes prep-elementen som var designade?** Det viktigaste är inte om alla moment nåddes, utan om de moment som spelades använde preppen väl. Hoppades viktiga element över (vilopauser, NPC-repliker, taktiska ledtrådar) trots att momentet spelades? Det är ett större problem än att ett helt moment skjuts till nästa session.
- **Tillkom bra saker spontant?** Spelardriven RP, kreativa lösningar, oväntade vändningar — lyft fram dessa som styrkor, inte som avvikelser.

---

#### B. Regelanvändning — Spelade vi rätt?

Gå igenom alla tärningsslag och regelinteraktioner i transkriptet:

- **Rätt använda regler:** Notera kort att de fungerade (behöver inte detaljeras)
- **Felaktiga eller osäkra regler:** För varje regelproblem:
  1. Beskriv situationen i sessionen
  2. Vilken regel tillämpades (eller borde ha tillämpats)?
  3. Vad var felet?
  4. **Slå upp den korrekta regeln** i `.claude/skills/genesys-rpg/reference/rules/` och citera den relevanta passagen
  5. Ge en kort, praktisk sammanfattning av hur det borde fungera
  6. Bedöm: påverkade felet spelet negativt, eller var det en rimlig förenkling?
- **Regelförvirring:** Identifiera moment där spelarna eller SL verkade osäkra på reglerna (pauser, diskussioner, "hur funkar det?"-frågor)
  - Lista vilka regler som orsakade förvirring
  - Föreslå konkret: "Läs på [regelkapitel X, avsnitt Y] inför nästa session"

**Regelreferenser att använda:**
| Område | Fil |
|--------|-----|
| Tärningsmekanik, slag, svårigheter | `01_ch01_core_mechanics.md` |
| Färdigheter (vilken skill för vad) | `03_ch03_skills.md` |
| Talanger (hur de fungerar) | `04_ch04_talents.md` |
| Utrustning, vapen, rustningar | `05_ch05_equipment.md` |
| **Stridsregler** (initiativ, tur-ordning, skada, kritiska, soak) | `06_ch06_combat_encounters.md` |
| Sociala sammandrabbningar | `07_ch07_social_encounters.md` |
| Spelledarskap, svårighetsgrader | `08_ch08_the_game_master.md` |

---

#### C. Stridbalans — Var striderna bra?

För varje strid i sessionen:

- **Motståndare:** Vem/vad kämpade sällskapet mot?
- **Avsedd svårighet:** Vad var tanken enligt prep? (Lätt, utmanande, dödlig?)
- **Faktisk svårighet:** Hur gick det? Var det:
  - **För lätt:** Sällskapet vann utan verklig risk. Varför? (För låga stats? För få motståndare? Spelarna hade oväntade resurser?)
  - **Lagom:** Känsla av fara men inte hopplöst. Spelarna behövde tänka och använda resurser
  - **För svårt:** Någon knockades/dog, spelarna kände sig maktlösa. Var det avsiktligt?
- **Tempo:** Hur lång tid tog striden? Var det:
  - **Snabbt och spännande:** Bra pacing, alla engagerade
  - **Utdraget:** För många rundor, spelarna tappade intresse
  - **Abrupt:** Slutade för snabbt, antiklimax
- **Slutstridsproblem:** Om det var en boss fight / kulmen på sessionen — gick den för fort? En slutstrid som är över på 1-2 rundor kan vara antiklimatisk. Analysera varför och föreslå justeringar (mer HP, fler förmågor, miljöhot, etc.)
- **Tärningarnas inverkan:** Avgjordes striden av skicklighet/taktik eller av tur? Var det rimligt?
- **Alla deltog:** Hade alla spelare meningsfulla val i striden? Eller satt någon passiv?

**Balanseringsverktyg (från Genesys):**
- Minion-grupper: Grupp om N minions slår N gröna tärningar
- Rival: Har wounds men ingen strain. Vanliga motståndare
- Nemesis: Har wounds OCH strain. Bossar och viktiga fiender
- Soak: Skada minus soak = faktisk skada. Hög soak gör fienden slitstark
- Kritiska träffar: Kumulativa — varje ny krit adderar +10

---

#### D. Pacing och energi — Var hade vi kul?

Analysera sessionens energinivå genom transkriptet:

- **Höjdpunkter:** Identifiera 2-3 moment där energin var som högst:
  - Vad hände? Varför var det kul?
  - Var det planerat eller spontant?
  - Kan vi skapa liknande moment i framtiden?
- **Dödpunkter:** Identifiera moment där energin sjönk:
  - Vad hände? Varför blev det tråkigt/långsamt?
  - Var det regelkrångel, otydlig situation, eller passiv väntan?
  - Hur hade vi kunnat undvika det?
- **Pacingkurva:** Beskriv sessionens tempo som helhet:
  - Började det starkt och avslutade svagt? (Vanligt vid tidspress)
  - Var det en bra uppbyggnad mot klimax?
  - Fanns det variation (lugna scener vs intensiva)?
- **Spelarprat vs spel:** Hur mycket off-topic-prat förekom? Var det:
  - Lagom (socialt, gemenskap, del av upplevelsen)
  - För mycket (sessionen tappade fart)
  - Om för mycket: vid vilka tillfällen, och vad kan SL göra för att mjukt styra tillbaka?

---

#### E. Spelledarprestanda — Vad gjorde SL bra och dåligt?

Utvärdera spelledarens insats ärligt men konstruktivt:

- **Bra:**
  - Stämningsfulla beskrivningar som fångade spelarna
  - Smidiga regelavgöranden
  - Improvisation som berikade sessionen
  - Bra NPC-porträttering
  - Moment där SL anpassade sig till spelarnas val
- **Förbättringsområden:**
  - Moment där SL körde fast — beskriv situationen och analysera varför
  - Otydliga beskrivningar som ledde till förvirring
  - Regelosäkerhet som bröt immersionen
  - Tillfällen där SL styrde för hårt (railroading) eller för lite (spelarna visste inte vad de kunde göra)
  - Missade möjligheter att spela på spelarnas idéer
- **Materialanvändning:** Var prep-materialet hjälpsamt?
  - Användes de förberedda beskrivningarna?
  - Var stat blocks korrekta och användbara i stunden?
  - Saknades något i preppen som hade behövts?
  - Var något överflödigt eller onödigt detaljerat?

---

#### F. Spelarengagemang — Var alla med?

- **Per spelare:** Bedöm varje spelares engagemang:
  - Aktiv/passiv? I vilka scener?
  - Hade de meningsfulla val?
  - Utnyttjades deras karaktärs styrkor?
- **Gruppdynamik:**
  - Samarbetade spelarna eller spelade de solo?
  - Fanns det konflikter (bra = karaktärsdrama, dålig = frustration)?
  - Fick alla "sin stund i rampljuset"?

---

### 3. Skriv analysen

Analysen ska vara **praktisk och konkret**. Undvik vaga uttalanden som "det gick bra" — beskriv *vad* som gick bra och *varför*.

#### Struktur

```markdown
# Session NN — Analys

**Datum:** [sessionens datum]
**Analyserat:** [transkript + prep-material]

---

## Sammanfattning (3-5 meningar)
[Övergripande bedömning av sessionen]

## Betyg
| Område | Betyg | Kommentar |
|--------|-------|-----------|
| Prep vs verklighet | ⭐⭐⭐⭐⭐ | [kort] |
| Regelanvändning | ⭐⭐⭐⭐⭐ | [kort] |
| Stridbalans | ⭐⭐⭐⭐⭐ | [kort] |
| Pacing och energi | ⭐⭐⭐⭐⭐ | [kort] |
| Spelledarprestanda | ⭐⭐⭐⭐⭐ | [kort] |
| Spelarengagemang | ⭐⭐⭐⭐⭐ | [kort] |

---

## 1. Prep vs verklighet
[Detaljerad analys]

## 2. Regelanvändning
[Detaljerad analys med regelcitat]

## 3. Stridbalans
[Detaljerad analys]

## 4. Pacing och energi
### Höjdpunkter
### Dödpunkter
### Pacingkurva

## 5. Spelledarprestanda
### Bra
### Förbättringsområden

## 6. Spelarengagemang
[Per spelare + gruppdynamik]

---

## Konkreta åtgärder inför nästa session

### Regler att läsa på
- [ ] [Specifik regel + var den finns + varför]

### Prep-förbättringar
- [ ] [Specifik förbättring + varför]

### Saker att behålla
- [ ] [Specifik sak som fungerade + varför den ska upprepas]

### Saker att undvika
- [ ] [Specifik sak + varför + alternativ]
```

#### Ton

- **Ärlig men konstruktiv.** Inte smickrande, inte syrlig. Saklig med konkreta exempel.
- **Specifik.** Referera till exakta tidsstämplar eller citat från transkriptet där det är relevant.
- **Handlingsorienterad.** Varje observation ska leda till en konkret åtgärd eller insikt.
- **Positiv balans.** Lyft alltid fram vad som fungerade, inte bara problem. Det som fungerar bra förtjänar lika mycket uppmärksamhet — att veta *varför* något var kul är lika värdefullt som att veta varför något inte var det.

---

## Speciella fall

### Om inget prep-material finns
Skippa "Prep vs verklighet"-sektionen. Analysera sessionen på sina egna meriter. Notera att prep-material hade kunnat hjälpa vid specifika moment.

### Om det inte var någon strid
Skippa "Stridbalans"-sektionen. Fokusera istället mer på sociala encounters, utforskning och narrativt flöde.

### Om transkriptet är ofullständigt
Notera vilka delar som saknas. Analysera det som finns. Var tydlig med att analysen baseras på ofullständigt underlag.

---

## Vanliga misstag att undvika

1. **Att vara för snäll.** Syftet är förbättring, inte bekräftelse. Var specifik om problem.
2. **Att vara för hård.** Det här är ett fritidsnöje. Alla sessioner behöver inte vara perfekta.
3. **Att glömma det positiva.** De bästa momenten förtjänar analys — att förstå varför något funkade är nyckeln till att upprepa det.
4. **Vaga rekommendationer.** "Läs på reglerna" är värdelöst. "Läs kapitel 6 (Combat), avsnittet om Critical Injuries (s. 112-114) — vi hanterade kumulativa kritiska träffar fel" är användbart.
5. **Att ignorera off-topic-pratet.** Det är en del av gruppen dynamik och kan ge insikter om energinivå och timing.
6. **Att döma spelarnas val.** Analysera *upplevelsen*, inte om spelarna "spelade rätt". Det finns inget rätt sätt att spela.
