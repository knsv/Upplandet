---
name: summarizer
description: Sammanfatta en TTRPG-session från ett mötesstranskript till en underhållande och korrekt sessionssammanfattning på svenska. Använd denna skill när användaren vill skapa en sessionssammanfattning, sessionsreferat, eller recap från ett transkript av en rollspelssession. Triggas av omnämnanden av "sessionssammanfattning", "session summary", "recap", "referat", eller när ett transkript från en rollspelssession laddas upp.
---

# TTRPG Sessionssammanfattning

Denna skill skapar underhållande och korrekta sessionssammanfattningar från mötesstranskript av rollspelssessioner.

## Språk

**Sammanfattningen ska ALLTID skrivas på svenska.** Inga undantag. Även om transkriptet är på engelska eller blandat ska den färdiga sammanfattningen vara helt på svenska.

## Filhantering och arbetsflöde

### Ingående filer
Transkript från sessioner placeras i `campaign/sessions/incoming/` med valfritt filnamn (t.ex. `transcript-session-05.txt` eller `raw-meeting-notes.md`).

### Utgående filer
När sammanfattningen är klar ska DU skapa två filer i `campaign/sessions/`:

1. **`session-NN-summary.md`** — Den färdiga sessionssammanfattningen
2. **`session-NN-transcript.md`** — Det ursprungliga transkriptet (flyttat från incoming/)

där `NN` är sessionsnumret (t.ex. `05` för session 5).

### Städning
Efter att båda filerna skapats ska det ursprungliga transkriptet i `campaign/sessions/incoming/` **tas bort**.

**Sammanfattning av filflödet:**
```
campaign/sessions/incoming/transcript.txt
  ↓ (läs och analysera)
  ↓ (skapa sammanfattning)
  ↓ (flytta transkript)
  ↓
campaign/sessions/session-NN-summary.md (ny fil)
campaign/sessions/session-NN-transcript.md (flyttad fil)
  ↓
campaign/sessions/incoming/transcript.txt (radera)
```

## Steg-för-steg arbetsflöde

### 1. Läs in kampanjkontext

Innan du börjar skriva, läs in relevant kampanjmaterial:

1. **CLAUDE.md** — Läs projektets CLAUDE.md för kampanjregler, namnkonventioner, speltermer och världsbeskrivning.
2. **campaign-status.md** — Läs `campaign/campaign-status.md` för aktuell kampanjstatus, aktiva karaktärer, pågående uppdrag och relationer.
3. **Tidigare sammanfattningar** — Kontrollera `campaign/sessions/` för den senaste sessionssammanfattningen. Läs den för att förstå var handlingen befinner sig.
4. **Karaktärsfiler** — Bläddra i `campaign/characters/` vid behov för att verifiera karaktärsdetaljer.
5. **Platsbeskrivningar** — Konsultera `campaign/locations/` om sessionen utspelar sig på en specifik plats.

### 2. Analysera transkriptet

Du hittar transkriptet i `campaign/sessions/incoming/`. Datumet för sessionen finns inbäddat i filens innehåll.

Gå igenom transkriptet systematiskt och extrahera:

- **Nyckelscener och händelser** — Vad hände, i vilken ordning?
- **Dialog och interaktioner** — Memorabla konversationer, förhandlingar, konfrontationer.
- **Strider och tärningsslag** — Viktiga slag, framgångar, misslyckanden, triumfer och förtvivlan.
- **Föremål och utrustning** — EXAKT vilka föremål som hittades, köptes, förlorades eller gavs bort. Notera kvantiteter.
- **Erfarenhetspoäng (XP)** — Om XP nämns, notera EXAKTA värden och vem som fick dem.
- **Pengar och resurser** — Exakta summor av guld, silver, eller andra valutor.
- **NSC-interaktioner** — Vilka NSC:er träffades, vad avslöjades, vilka relationer förändrades.
- **Karaktärsutveckling** — Personliga ögonblick, beslut som definierar karaktärerna.

### 3. Skriv sammanfattningen

#### Längd
Sammanfattningen ska vara **mellan 1 500 och 1 600 ord**. Inte kortare, inte längre. Detta ger utrymme att fånga alla viktiga händelser med tillräcklig detalj och narrativt flöde. Behåll händelsernas kronologi, men kreativt anpassa för bättre läsbarhet. T.ex. om en dialog är avgörande, men innehåller inga händelser, kan den sammanfattas eller citeras kortare.

#### Ton och stil — Terry Pratchetts anda

Skriv i den humoristiska, observerande anda som kännetecknar Terry Pratchett. Det innebär:

- **Berättarröst med glimten i ögat** — En allvetande berättare som kommenterar händelserna med torr humor och skarp intelligens. Berättaren ser absurditeten i situationen men älskar sina karaktärer.
- **Fotnotsliknande utvikningar** — Korta, parentetiska kommentarer som ger kolorit eller kommenterar det uppenbara. T.ex. *"Baron Levin, en man vars mustasch ensam kunde ha förhandlat fram freden i Westfalen om den bara hade givits chansen..."*
- **Vardaglig visdom i extraordinära situationer** — Karaktärer som reagerar mänskligt på det övernaturliga. En häxa är skrämmande, men har man glömt att packa lunch är det också ett problem.
- **Metaforer och liknelser** — Kreativa, oväntade jämförelser. Undvik klichéer.
- **Satirisk kommentar** — Peka på absurditeter i byråkrati, religion, makt och mänskligt beteende, men alltid med värme snarare än cynism.

**VIKTIGT:** Humorn ska aldrig fabricera händelser. Allt som beskrivs måste ha faktisk grund i transkriptet. Pratchett-stilen appliceras på *hur* saker berättas, inte *vad* som berättas. Du får överdriva tonen och lägga till berättarkommentarer, men själva händelserna, besluten och utfallen ska vara trogna transkriptet.

#### Struktur

Sammanfattningen ska vara en löpande berättelse, inte en punktlista. Använd följande övergripande struktur:

1. **Inledning** — Sätt scenen. Var befinner sig äventyrarna? Vad hände sist? Skriv en atmosfärisk öppning som drar in läsaren.

2. **Berättelsens kropp** — Följ sessionens händelser kronologiskt men med narrativt flöde. Dela upp i naturliga scener eller kapitel med beskrivande underrubriker om det hjälper läsbarheten. Väv in:
   - Karaktärernas handlingar och beslut
   - Viktiga tärningsslag och deras konsekvenser (beskriv narrativt, t.ex. *"Ödet log mot Torsten den kvällen — tre framgångar och en triumf lyste upp tärningsbordet som midvinterblot"*)
   - Dialoghöjdpunkter (parafrasera eller citera om det var särskilt minnesvärt)
   - Stämning och atmosfär

3. **Avslutning** — Runda av sessionen. Var lämnades sällskapet? Vilka frågor hänger i luften? Avsluta gärna med en cliffhanger eller en Pratchett-värdig eftertanke.

4. **Sessionens skörd** — En kort, tydlig sektion i slutet som listar:
   - **Föremål**: Exakt vilka föremål som erhölls eller förlorades (med kvantitet och detaljer)
   - **Erfarenhetspoäng**: Exakta XP-värden per karaktär om det delades ut
   - **Pengar**: Exakta belopp som tjänades eller spenderades
   - **Viktiga kontakter**: Nya NSC-relationer eller förändrade relationer
   - **Öppna trådar**: Olösta mysterier eller kommande utmaningar (baserat ENBART på vad spelarna känner till)

### 4. Kontroller innan leverans

Gå igenom dessa kontrollpunkter innan du levererar sammanfattningen:

#### Korrekthet
- [ ] Alla föremål som nämns i transkriptet finns med — inga saknade, inga påhittade
- [ ] XP-värden är exakt korrekta enligt transkriptet
- [ ] Pengar och resurser stämmer exakt
- [ ] Inga händelser är fabricerade — allt har stöd i transkriptet
- [ ] Karaktärsnamn och NSC-namn använder rätt svenska namnkonventioner (se CLAUDE.md)
- [ ] Speltermer använder svenska termer (se CLAUDE.md)
- [ ] Ortnamn använder svenska ortnamn (se CLAUDE.md)

#### Kampanjhemligheter — FÖRBJUDET INNEHÅLL
- [ ] **Sammanfattningen innehåller INGA kampanjhemligheter.** Detta är kritiskt.
- [ ] Inga spoilers om kommande händelser i äventyret
- [ ] Inga avslöjanden om NSC:ers dolda motiv som spelarna inte känner till
- [ ] Inga ledtrådar om pussel eller mysterier som ännu inte lösts av spelarna
- [ ] Ingen information från äventyrsmodulen (`campaign/adventures/`) som inte explicit framkommit under sessionen
- [ ] Om du läst äventyrsmaterial för kontext: filtrera STRIKT bort allt spelarna inte upplevt

Tumregel: Om spelarna inte sa det, hörde det, eller upplevde det under sessionen — ska det inte finnas i sammanfattningen.

#### Kvalitet
- [ ] Texten är på svenska genomgående
- [ ] Längden är mellan 2 000 och 3 000 ord
- [ ] Pratchett-tonen är konsekvent men inte överdrivet forcerad
- [ ] Berättelsen flyter — det är en sammanhängande text, inte en lista
- [ ] "Sessionens skörd"-sektionen är komplett och korrekt

## Utdataformat

### 1. Sammanfattningsfilen (session-NN-summary.md)

Spara sammanfattningen som en markdown-fil med namnkonventionen:

```
campaign/sessions/session-NN-summary.md
```

där `NN` är sessionsnumret (hämta från transkriptets filnamn eller fråga användaren).

Filens metadata-header:

```markdown
# Session NN — [Beskrivande titel]

**Datum:** [Sessionens datum om känt]
**Spelare:** [Lista spelarna som deltog]
**Plats:** [Var sessionen utspelade sig i spelvärlden]

---
```

### 2. Transkriptfilen (session-NN-transcript.md)

Flytta det ursprungliga transkriptet från `campaign/sessions/incoming/` till:

```
campaign/sessions/session-NN-transcript.md
```

Transkriptet ska behållas i sin ursprungliga form. Om det är en textfil (.txt), konvertera den till markdown (.md) genom att lägga till en enkel header:

```markdown
# Session NN — Transkript

**Datum:** [Sessionens datum om känt]

---

[Ursprungligt transkriptinnehåll här]
```

### 3. Radera originalfilen

Efter att både `session-NN-summary.md` och `session-NN-transcript.md` har skapats, radera det ursprungliga transkriptet från `campaign/sessions/incoming/`.

## Vanliga misstag att undvika

1. **Att hitta på föremål eller XP** — Dubbelkolla ALLTID mot transkriptet. Om du är osäker, fråga hellre användaren.
2. **Att avslöja hemligheter** — Läs äventyrsmaterial för kontext men skriv ENBART utifrån spelarnas perspektiv.
3. **Att skriva på engelska** — Hela sammanfattningen ska vara på svenska. Kontrollera särskilt speltermer.
4. **Att överanvända humorn** — Pratchett-stilen är en krydda, inte huvudrätten. Händelserna och karaktärerna ska stå i centrum.
5. **Att göra sammanfattningen för kort** — 2 000 ord är minimum. Ge scenerna utrymme att andas.
6. **Att fabricera dialog** — Parafrasera eller citera bara det som faktiskt sades. Att "Pratchettifiera" en konversation är okej, att hitta på den är det inte.
7. **Att glömma tärningsslagen** — Viktiga slag (särskilt triumfer och förtvivlan) ska finnas med i berättelsen.
