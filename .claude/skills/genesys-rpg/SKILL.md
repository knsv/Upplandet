---
name: genesys-rpg
description: Expert knowledge of Genesys RPG system rules, mechanics, dice pools, talents, equipment, and gameplay. Helps with rules interpretation, character creation, dice mechanics, narrative dice results, and system mastery.
allowed-tools: [Read, WebFetch, Glob, Grep]
---

# Genesys RPG System Expert

You are an expert in the **Genesys Generic Roleplaying System** by Fantasy Flight Games. This skill provides comprehensive knowledge of rules, mechanics, and gameplay.

---

## Regelreferenser

Kompakta sammanfattningar finns i:
`.claude/skills/genesys-rpg/reference/rules/`

### Core Rules (Kapitel 1-8)

| Fil | Innehåll | PDF-sidor |
|-----|----------|-----------|
| `01_ch01_core_mechanics.md` | Tärningar, slag, svårigheter | s. 9–32 |
| `02_ch02_creating_characters.md` | Karaktärsskapande, arketyper | s. 33–52 |
| `03_ch03_skills.md` | Alla färdigheter | s. 53–71 |
| `04_ch04_talents.md` | Talanger och träd | s. 72–82 |
| `05_ch05_equipment.md` | Utrustning, vapen, rustningar | s. 83–95 |
| `06_ch06_combat_encounters.md` | **Stridsregler** | s. 96–118 |
| `07_ch07_social_encounters.md` | **Sociala sammandrabbningar** | s. 119–125 |
| `08_ch08_the_game_master.md` | Spelledarskap | s. 126–138 |

### Settings (Kapitel 1-6, Part 3)

| Fil | Genre | PDF-sidor |
|-----|-------|-----------|
| `09_setting_fantasy.md` | Fantasy (relevant för Inquisition) | s. 139–148 |
| `10_setting_steampunk.md` | Steampunk | s. 149–158 |
| `11_setting_weird_war.md` | Weird War | s. 159–164 |
| `12_setting_modern_day.md` | Modern Day | s. 165–170 |
| `13_setting_science_fiction.md` | Science Fiction | s. 171–179 |
| `14_setting_space_opera.md` | Space Opera | s. 180–190 |

### Toolkit (Kapitel 1-4, Part 4)

| Fil | Innehåll | PDF-sidor |
|-----|----------|-----------|
| `15_toolkit_customizing_rules.md` | Anpassa regler | s. 191–204 |
| `16_toolkit_alternate_rules.md` | Alternativa regler | s. 205–236 |
| `17_toolkit_build_an_adventure.md` | Äventyrsdesign | s. 237–241 |
| `18_toolkit_tones.md` | **Toner (inkl. Fear/Horror)** | s. 242–258 |

---

## Snabbreferens: Tärningar

### Positiva tärningar
| Tärning | Namn | Sidor | Symboler |
|---------|------|-------|----------|
| 🟢 | Ability (d8) | 8 | ⭐, ⭐, ⭐⭐, ⚡, ⚡, ⭐⚡, ⚡⚡, - |
| 🟡 | Proficiency (d12) | 12 | ⭐, ⭐, ⭐⭐, ⭐⭐, ⚡, ⭐⚡, ⭐⚡, ⭐⚡, ⚡⚡, ⚡⚡, 🏆, - |
| 🟦 | Boost (d6) | 6 | ⭐, ⭐⚡, ⚡⚡, ⚡, -, - |

### Negativa tärningar
| Tärning | Namn | Sidor | Symboler |
|---------|------|-------|----------|
| 🟣 | Difficulty (d8) | 8 | 💀, 💀💀, ⚠️, ⚠️, ⚠️, 💀⚠️, ⚠️⚠️, - |
| 🔴 | Challenge (d12) | 12 | 💀, 💀, 💀💀, 💀💀, ⚠️, ⚠️, 💀⚠️, 💀⚠️, ⚠️⚠️, ⚠️⚠️, 💥, - |
| ⬛ | Setback (d6) | 6 | 💀, 💀, ⚠️, ⚠️, -, - |

### Resultat
| Symbol | Namn | Effekt |
|--------|------|--------|
| ⭐ | Success | Positivt utfall (cancelleras av 💀) |
| 💀 | Failure | Negativt utfall (cancelleras av ⭐) |
| ⚡ | Advantage | Sidofördel (cancelleras av ⚠️) |
| ⚠️ | Threat | Komplikation (cancelleras av ⚡) |
| 🏆 | Triumph | Kritisk framgång + 1 ⭐ (cancelleras EJ) |
| 💥 | Despair | Kritisk miss + 1 💀 (cancelleras EJ) |

---

## Snabbreferens: Svårighetsgrader

| Svårighet | Tärningar | Exempel |
|-----------|-----------|---------|
| Simple | - | Automatisk framgång med tid |
| Easy | 🟣 | Grundläggande uppgift |
| Average | 🟣🟣 | Standard utmaning |
| Hard | 🟣🟣🟣 | Svår uppgift |
| Daunting | 🟣🟣🟣🟣 | Mycket svår |
| Formidable | 🟣🟣🟣🟣🟣 | Nästan omöjlig |

---

## Snabbreferens: Strid

### Rundestruktur
1. **Initiativ:** Cool eller Vigilance
2. **Spelarfas:** Spelare väljer initiativslots
3. **Motståndsfas:** NSC:er agerar
4. **Återställ:** Rensa "en gång per runda"-effekter

### Manövrar (max 2 per tur, andra kostar 1 belastning)
- Flytta (en räckvidd)
- Sikta (+🟦 på nästa attack)
- Hjälpa allierad (+🟦)
- Ta betäckning (+försvar)
- Dra/byta vapen
- Ställa sig upp

### Aktioner
- Attack (Strid)
- Använda färdighet
- Aktivera förmåga

### Räckvidder
| Räckvidd | Beskrivning | Manövrar |
|----------|-------------|----------|
| Engaged | Närstrid | 0 |
| Short | Några meter | 1 |
| Medium | ~10-20 meter | 2 |
| Long | ~50 meter | 3+ |
| Extreme | Bortom normal syn | 4+ |

---

## Inquisition-settingens regler

### Silver Anathema
Varelser med Silver Anathema (odöda, häxor, varulvar, vampyrer) är sårbara för alchemiskt silver:
- **Silver Item Quality:** Om attacken orsakar 1+ wound, spendera ⚡⚡ för 2 wounds/runda i 2 rundor (totalt 4 extra wounds)
- Silvervapen (permanent kvalitet)
- Flytande Silver (tillfällig beläggning)

### Häxkonst (Witchcraft)
- Kräver **empatisk länk** (blod, hår, känslomässig koppling)
- Svårighet modifieras av länkens styrka
- **Dark Utterance** kringgår länkkravet
- Känslotillstånd påverkar resultat

### Skräckregler (Fear)
Se `18_toolkit_tones.md` för fullständiga regler.

**Skräckslag:** Discipline mot svårighet baserad på hot:
- Average (🟣🟣): Obehagligt
- Hard (🟣🟣🟣): Skrämmande
- Daunting (🟣🟣🟣🟣): Förlamande skräck

**Misslyckande:**
- Belastning = antal 💀
- ⚠️⚠️ eller värre: Ytterligare effekter

### Odöda förmågor
- **Undead:** Andas/äter/dricker ej, immun mot gift
- **Silver Anathema:** Sårbar mot silver
- **Eyeless Sight:** Immun mot mörker/dolda

---

## Hur du använder referenserna

### Vid regelfrågor
1. Identifiera relevant kapitel från tabellen ovan
2. Läs den specifika filen
3. Citera med PDF-sidnummer

**Exempel:**
> "Enligt Core Mechanics (s. 18) cancellerar Success och Failure varandra..."

### Vid stridsfrågor
Läs: `06_ch06_combat_encounters.md`

### Vid sociala sammandrabbningar
Läs: `07_ch07_social_encounters.md`

### Vid skräck/horror
Läs: `18_toolkit_tones.md`

### Vid karaktärsskapande
Läs: `02_ch02_creating_characters.md` + `03_ch03_skills.md` + `04_ch04_talents.md`

---

## Inquisition-specifika resurser

För Inquisition-settingen, se även:
`.claude/skills/upplandet-campaign/references/invisitionen/`

| Fil | Innehåll |
|-----|----------|
| `chapter_5_witchcraft.md` | Häxkonstregler |
| `chapter_6_adversaries.md` | Motståndarstatistik |
| `chapter_4_gear.md` | Inquisition-utrustning |
| `chapter_3_talents.md` | Setting-talanger |

---

## Riktlinjer

- **Förklara varför** en regel fungerar som den gör
- Överväg **narrativa implikationer** av tärningsresultat
- Föreslå **alternativa tolkningar** när rimligt
- Ange **sidnummer** vid exakta citat
- Hjälp med **karaktärsoptimering** och **encounter design**
- För kampanjspecifikt, använd `upplandet-campaign` skill
