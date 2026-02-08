---
name: adversary-creator
description: Skapar balanserade motståndare för Genesys RPG med stöd för Inquisition-settingen. Genererar fullständiga stat blocks med egenskaper, färdigheter, talanger, utrustning och förmågor. Kan även generera Foundry VTT-kompatibla JSON-filer.
allowed-tools: [Read, Write, Glob, Grep, Bash]
---

# Genesys Adversary Creator

Denna skill skapar balanserade motståndare för Genesys-systemet, optimerad för Inquisition-settingen.

Motståndare kan skapas i två format:
1. **Markdown stat block** — för kampanjdokumentation och sessionsförberedelser
2. **Foundry VTT JSON** — för direkt import till Foundry VTT (Genesys-systemet)

---

## Motståndartyper

### Minion (Mängdfiende)
- **Syfte:** Talrika fiender som är farliga i grupp
- **Wounds:** Låg (3-6 individuellt)
- **Strain:** Ingen (hanterar strain som wounds)
- **Skills:** Gruppregler (+1 rank per extra medlem)
- **Talanger:** Inga eller mycket få
- **Tumregel:** 2-3 minions ≈ hot mot 1 startkaraktär

### Rival (Viktig NSC)
- **Syfte:** Namngivna motståndare, förenklade "PC-lika"
- **Wounds:** Måttlig (8-15)
- **Strain:** Ingen (hanterar strain som wounds)
- **Skills:** Individuella, 1-3 relevanta färdigheter
- **Talanger:** 1-3 relevanta talanger
- **Tumregel:** 1 rival ≈ hot mot 1-2 erfarna karaktärer

### Nemesis (Boss)
- **Syfte:** Centrala antagonister, "fullständiga" motståndare
- **Wounds:** Hög (15-30)
- **Strain:** Separat (10-18)
- **Skills:** Flera färdigheter med höga ranks
- **Talanger:** Flera, ofta Adversary 1-3
- **Tumregel:** 1 nemesis ≈ hot mot hela gruppen

---

## Egenskapsriktlinjer

### Karakteristika per typ

| Typ | Totala poäng | Typiskt intervall | Max enskilt |
|-----|--------------|-------------------|-------------|
| Minion | 12-14 | 1-3 | 3 |
| Rival | 14-18 | 2-3 | 4 |
| Nemesis | 18-24 | 2-4 | 5 |

### Karakteristika efter roll

| Roll | Primär | Sekundär |
|------|--------|----------|
| Stridare (närstrid) | Brawn | Agility eller Willpower |
| Stridare (avstånd) | Agility | Cunning |
| Magiker/Häxa | Willpower | Intellect eller Cunning |
| Social manipulatör | Presence | Cunning |
| Scout/Smygare | Agility | Cunning |
| Tank/Brute | Brawn | Brawn igen (för Soak) |

---

## Beräknade värden

### Formler

```
Soak = Brawn + rustning
Wound Threshold = Bas (typ) + Brawn
Strain Threshold = Willpower + 10 (endast Nemesis)
Melee Defense = Från talanger/utrustning (0-2)
Ranged Defense = Från talanger/utrustning (0-2)
```

### Basvärden för Wound Threshold

| Typ | Bas |
|-----|-----|
| Minion | 3-5 |
| Rival | 8-12 |
| Nemesis | 12-20 |

---

## Färdighetsriktlinjer

### Skills per typ

| Typ | Antal skills | Ranks |
|-----|--------------|-------|
| Minion | 2-4 (gruppbonus) | 0-1 |
| Rival | 3-5 | 1-2 |
| Nemesis | 5-8 | 2-4 |

### Vanliga stridfärdigheter

| Färdighet | Användning |
|-----------|------------|
| Brawl | Obeväpnad strid |
| Melee (Light) | Dolkar, kortsvärd |
| Melee (Heavy) | Svärd, yxor, stridsklubba |
| Melee | Generell närstrid |
| Ranged (Light) | Kastade vapen, armborst |
| Ranged (Heavy) | Långbåge, tunga vapen |
| Ranged | Generell avståndsstrid |

### Vanliga stödfärdigheter

| Färdighet | Användning |
|-----------|------------|
| Athletics | Klättring, simning, förföljelser |
| Coordination | Akrobatik, balans |
| Resilience | Uthållighet, motstå miljö |
| Vigilance | Initiativ (förberedda) |
| Cool | Initiativ (sociala), stresshantering |
| Perception | Upptäcka hot |
| Stealth | Smyga, bakhåll |
| Survival | Spårning, vildmark |
| Coercion | Hot, skrämma |
| Discipline | Mental motstånd, magi |
| Deception | Ljuga |
| Charm | Övertyga |

---

## Talanger för motståndare

### Universella NPC-talanger

| Talang | Effekt | Tier |
|--------|--------|------|
| **Adversary 1-3** | Uppgradera svårigheten på stridsslag mot denna karaktär | - |
| **Durable 1-3** | Minska kritiska skador | 1 |
| **Parry** | Lida 3 strain för att minska närstridsskada med 5 | 1 |

### Offensiva talanger

| Talang | Effekt |
|--------|--------|
| Berserk | +1 skada per slag, -1 försvar |
| Hamstring Shot | Mål lider strain vid manöver |
| Precise Aim | Ignorera engaged-straff vid skott |
| Quick Strike | +🟦 mot mål som inte agerat |

### Defensiva talanger

| Talang | Effekt |
|--------|--------|
| Dodge | Lida strain för att uppgradera attacksvårighet |
| Side Step | Lida strain för att uppgradera svårighet på avstånd |
| Defensive Stance | Manöver: +1 försvar, -1 på attacker |

### Ledarskap

| Talang | Effekt |
|--------|--------|
| Field Commander | Manöver: ge order till allierade |
| Inspiring Rhetoric | Läk strain hos allierade |
| Scathing Tirade | Ge strain till fiender |

---

## Inquisition-specifika förmågor

### Övernaturliga egenskaper

| Förmåga | Beskrivning |
|---------|-------------|
| **Silver Anathema** | Tar +2 skada från alchemiskt silver |
| **Undead** | Behöver inte andas/äta/dricka, immun mot gift, kan inte använda elixir |
| **Eyeless Sight** | Immun mot mörker/concealment-modifierare |
| **Corrosive Blood** | Nära angripare tar 1 sår |
| **Regeneration X** | Återställ X sår i början av varje runda |
| **Fear X** | Tvingar Discipline-slag vid möte |

### Häxförmågor

| Förmåga | Beskrivning |
|---------|-------------|
| **Witchcraft** | Kan använda häxkonst via empatisk länk |
| **Dark Utterance** | Kringgår kravet på empatisk länk |
| **Häxblod** | Lida sår för att hela strain (1:2 ratio) |

### Vampyrförmågor

| Förmåga | Beskrivning |
|---------|-------------|
| **Blood Potency** | Lida strain för att höja Brawn/Agility |
| **Entranced** | Paralysera mål med blick |
| **Shapechange** | Förändra form (fladdermus, varg) |

### Varulvsförmågor

| Förmåga | Beskrivning |
|---------|-------------|
| **Werewolf** | Kan byta till vargform |
| **Rending Strike** | Farliga klor i vargform |
| **Warning Howl** | Skada angripare med strain |

---

## Utrustningsriktlinjer

### Vapenprofiler (närstrid)

| Vapen | Skill | Skada | Kritisk | Egenskaper |
|-------|-------|-------|---------|------------|
| Obeväpnad | Brawl | +0 | 5 | Knockdown |
| Dolk | Melee (Light) | +1 | 3 | Accurate 1 |
| Svärd | Melee | +2 | 2 | Defensive 1 |
| Yxa | Melee | +3 | 3 | Vicious 1 |
| Stridsklubba | Melee (Heavy) | +4 | 4 | Knockdown |
| Storsvärd | Melee (Heavy) | +4 | 2 | Cumbersome 3 |

### Vapenprofiler (avstånd)

| Vapen | Skill | Skada | Kritisk | Räckvidd | Egenskaper |
|-------|-------|-------|---------|----------|------------|
| Kastdolk | Ranged (Light) | +2 | 3 | Short | Accurate 1 |
| Kortbåge | Ranged | 5 | 3 | Medium | - |
| Långbåge | Ranged (Heavy) | 7 | 3 | Long | Cumbersome 2 |
| Armborst | Ranged | 8 | 2 | Medium | Pierce 1, Prepare 1 |

### Rustningsvärden

| Rustning | Soak | Defense | Egenskaper |
|----------|------|---------|------------|
| Tjocka kläder | +1 | 0 | - |
| Läderdräkt | +1 | 0 | - |
| Ringbrynja | +2 | 0 | - |
| Kedjerustning | +2 | 0 | - |
| Plåtrustning | +3 | 1 | Cumbersome 3 |

---

## Stat Block-mall

### Minion-mall

```markdown
### [NAMN] (Minion)

**Roll:** [Kort beskrivning]

#### Egenskaper

| Egenskap | Värde |
|----------|-------|
| Brawn | X |
| Agility | X |
| Intellect | X |
| Cunning | X |
| Willpower | X |
| Presence | X |

| Stat | Värde |
|------|-------|
| Soak | X |
| Sårtröskel | X |
| Försvar (N/A) | X/X |

#### Färdigheter (Endast grupp)
- [Skill] 1, [Skill] 1

#### Talanger
Inga.

#### Förmågor
- **[Förmåga]:** [Beskrivning]

#### Utrustning
- [Vapen]: [Skill]; Skada X; Kritisk X; Räckvidd [Engaged/Short/etc]; [Qualities]
```

### Rival-mall

```markdown
### [NAMN] (Rival)

**Roll:** [Kort beskrivning]
**Plats:** [Var de finns]

#### Egenskaper

| Egenskap | Värde |
|----------|-------|
| Brawn | X |
| Agility | X |
| Intellect | X |
| Cunning | X |
| Willpower | X |
| Presence | X |

| Stat | Värde |
|------|-------|
| Soak | X |
| Sårtröskel | X |
| Försvar (N/A) | X/X |

#### Färdigheter
- [Skill] X (🟢🟡...), [Skill] X

#### Talanger
- **[Talang]:** [Beskrivning]

#### Förmågor
- **[Förmåga]:** [Beskrivning]

#### Utrustning
- [Vapen]: [Profil]
- [Rustning]: +X Soak
```

### Nemesis-mall

```markdown
### [NAMN] (Nemesis)

**Roll:** [Kort beskrivning]
**Plats:** [Var de finns]
**Motivationer:**
- **Begär:** [Vad de vill ha]
- **Rädsla:** [Vad de fruktar]
- **Styrka:** [Positiv egenskap]
- **Brist:** [Negativ egenskap]

#### Egenskaper

| Egenskap | Värde |
|----------|-------|
| Brawn | X |
| Agility | X |
| Intellect | X |
| Cunning | X |
| Willpower | X |
| Presence | X |

| Stat | Värde |
|------|-------|
| Soak | X |
| Sårtröskel | X |
| Belastningströskel | X |
| Försvar (N/A) | X/X |

#### Färdigheter
- [Skill] X (🟢🟡...), [Skill] X, etc.

#### Talanger
- **Adversary X:** Uppgradera svårigheten på alla stridsslag mot denna karaktär X gånger
- **[Talang]:** [Beskrivning]

#### Förmågor
- **[Förmåga]:** [Beskrivning]

#### Utrustning
- [Vapen]: [Fullständig profil]
- [Rustning]: [Profil]

#### Stridsbeteende
- [Hur de agerar i strid]
- [Prioriteringar]
- [Speciella taktiker]
```

---

## JSON-format (Foundry VTT)

När användaren begär en motståndare i JSON-format (eller för import till Foundry VTT), generera en JSON-fil som exakt följer schemat i referenstemplates. **Avvik ALDRIG från templatens schema** — lägg inte till fält som saknas i templaten och utelämna inte fält som finns.

### Arbetsflöde

1. **Läs in rätt template** från `.claude/skills/adversary-creator/references/`:
   - `minion-template.json` för minions
   - `rival-template.json` för rivals
   - `nemesis-template.json` för nemesis
2. **Kopiera hela templatens struktur** — alla fält, inklusive `prototypeToken`, `_stats`, `ownership`
3. **Fyll i motståndarens värden** i `system`-blocket och `items`-arrayen
4. **Generera unika ID:n** för alla `_id`-fält (16 tecken alfanumeriska)
5. **Validera JSON** med `python3 -c "import json; json.load(open('filnamn'))"`
6. **Spara filen** i `campaign/characters/npcs/` med namnkonventionen `npc-[namn]-[_id].json`

### Kritiska schemaskillnader mellan typer

| Fält | Minion | Rival | Nemesis |
|------|--------|-------|---------|
| `type` | `"minion"` | `"rival"` | `"nemesis"` |
| `system.groupSize` | **Finns** (number) | Saknas | Saknas |
| `system.wounds` | `{ value, threshold }` | `{ value, max }` | `{ value, max }` |
| `system.strain` | **Saknas** | **Saknas** | `{ value, max }` |
| `prototypeToken.actorLink` | `false` | `false` | `true` |
| `prototypeToken.bar2.attribute` | `"members"` | `null` | `"strain"` |

**VIKTIGT:** Minions använder `"threshold"` i wounds, medan Rival och Nemesis använder `"max"`. Blanda ALDRIG ihop dessa.

### Fält att anpassa

Följande fält ska sättas per motståndare (resten kopieras rakt från templaten):

**Aktör-nivå:**

| Fält | Beskrivning |
|------|-------------|
| `name` | Motståndarens namn |
| `type` | `"minion"`, `"rival"`, eller `"nemesis"` |
| `img` | Ikon-sökväg (default: `"icons/svg/mystery-man.svg"`) |
| `system.characteristics` | Brawn, Agility, Intellect, Cunning, Willpower, Presence |
| `system.soak` | Beräknat: Brawn + rustningsbonus |
| `system.defense` | `{ melee, ranged }` — från utrustning/talanger |
| `system.description` | HTML-beskrivning av förmågor och speciella regler |
| `system.wounds` | Minion: `{ value: 0, threshold: X }`. Rival/Nemesis: `{ value: 0, max: X }` |
| `system.strain` | **Bara nemesis:** `{ value: 0, max: X }` |
| `system.groupSize` | **Bara minion:** Standardstorlek på gruppen |
| `system.motivations` | `strength`, `flaw`, `desire`, `fear` — vardera med `name` och `description` |
| `prototypeToken.name` | Samma som aktörens namn |
| `_id` | Generera 16 tecken alfanumeriskt ID |

### Item-typer i `items`-arrayen

Alla items läggs i `items`-arrayen. Det finns tre typer:

#### Skill-item

Lägg **bara till skills som har rank > 0**. Inkludera INTE skills med rank 0.

```json
{
  "name": "Coercion",
  "type": "skill",
  "img": "icons/svg/mystery-man.svg",
  "system": {
    "description": "",
    "source": "",
    "characteristic": "willpower",
    "category": "social",
    "initiative": false,
    "career": false,
    "rank": 1
  },
  "effects": [],
  "folder": null,
  "flags": {},
  "_stats": {
    "compendiumSource": null,
    "duplicateSource": null,
    "exportSource": null,
    "coreVersion": "13.351",
    "systemId": "genesys",
    "systemVersion": "0.2.18",
    "createdTime": null,
    "modifiedTime": null,
    "lastModifiedBy": null
  },
  "_id": "XXXXXXXXXXXXXXXX",
  "sort": 0,
  "ownership": {
    "default": 0
  }
}
```

Giltiga värden för `characteristic`: `"brawn"`, `"agility"`, `"intellect"`, `"cunning"`, `"willpower"`, `"presence"`

Giltiga värden för `category`: `"general"`, `"combat"`, `"social"`, `"knowledge"`, `"magic"`

Vanliga skills och deras characteristic/category:

| Skill | Characteristic | Category |
|-------|---------------|----------|
| Athletics | brawn | general |
| Brawl | brawn | combat |
| Coercion | willpower | social |
| Cool | presence | general |
| Coordination | agility | general |
| Deception | cunning | social |
| Discipline | willpower | general |
| Melee | brawn | combat |
| Melee (Light) | brawn | combat |
| Melee (Heavy) | brawn | combat |
| Perception | cunning | general |
| Ranged | agility | combat |
| Ranged (Light) | agility | combat |
| Ranged (Heavy) | agility | combat |
| Resilience | brawn | general |
| Skulduggery | cunning | general |
| Stealth | agility | general |
| Streetwise | cunning | general |
| Survival | cunning | general |
| Vigilance | willpower | general |
| Charm | presence | social |
| Leadership | presence | social |
| Negotiation | presence | social |
| Medicine | intellect | general |
| Knowledge | intellect | knowledge |
| Häxkonst | cunning | magic |
| Arcana | intellect | magic |
| Divine | willpower | magic |
| Primal | cunning | magic |

#### Weapon-item

```json
{
  "name": "Dagger",
  "type": "weapon",
  "img": "icons/svg/mystery-man.svg",
  "system": {
    "description": "",
    "source": "",
    "rarity": 1,
    "encumbrance": 1,
    "price": 60,
    "damage": "undamaged",
    "container": "",
    "quantity": 1,
    "state": "carried",
    "baseDamage": 2,
    "critical": 3,
    "range": "engaged",
    "skills": [
      "Melee (Light)"
    ],
    "qualities": [
      {
        "name": "accurate",
        "rating": 1,
        "description": "",
        "isRated": true
      }
    ],
    "damageCharacteristic": "brawn"
  },
  "effects": [],
  "folder": null,
  "flags": {},
  "_stats": {
    "compendiumSource": null,
    "duplicateSource": null,
    "exportSource": null,
    "coreVersion": "13.351",
    "systemId": "genesys",
    "systemVersion": "0.2.18",
    "createdTime": null,
    "modifiedTime": null,
    "lastModifiedBy": null
  },
  "_id": "XXXXXXXXXXXXXXXX",
  "sort": 0,
  "ownership": {
    "default": 0
  }
}
```

Giltiga värden för `range`: `"engaged"`, `"short"`, `"medium"`, `"long"`, `"extreme"`

Giltiga värden för `damageCharacteristic`: `"brawn"`, `"agility"`, `"intellect"`, `"cunning"`, `"willpower"`, `"presence"`, `"-"` (för vapen med fast skada)

Giltiga vapenegenskaper (`qualities`): `"accurate"`, `"blast"`, `"burn"`, `"cumbersome"`, `"defensive"`, `"disorient"`, `"ensnare"`, `"knockdown"`, `"pierce"`, `"prepare"`, `"stun"`, `"sunder"`, `"unwieldy"`, `"vicious"`

Vapenprofiler:

| Vapen | baseDamage | critical | range | skills | damageCharacteristic | qualities |
|-------|-----------|----------|-------|--------|---------------------|-----------|
| Dagger | 2 | 3 | engaged | Melee (Light) | brawn | accurate 1 |
| Sword | 2 | 2 | engaged | Melee | brawn | defensive 1 |
| Axe | 3 | 3 | engaged | Melee (Light) | - | vicious 1 |
| Mace | 3 | 4 | engaged | Melee (Light) | brawn | — |
| Greatsword | 4 | 2 | engaged | Melee (Heavy) | - | defensive 1, pierce 1, unwieldy 3 |
| Spear | 3 | 3 | engaged | Melee | brawn | defensive 1 |
| Bow | 7 | 3 | medium | Ranged | - | unwieldy 2 |
| Crossbow | 7 | 2 | medium | Ranged | - | pierce 2, prepare 1 |

#### Armor-item

```json
{
  "name": "Leather Armor",
  "type": "armor",
  "img": "icons/svg/mystery-man.svg",
  "system": {
    "description": "",
    "source": "",
    "rarity": 3,
    "encumbrance": 2,
    "price": 50,
    "damage": "undamaged",
    "container": "",
    "quantity": 1,
    "state": "carried",
    "defense": 0,
    "soak": 1,
    "qualities": []
  },
  "effects": [],
  "folder": null,
  "flags": {},
  "_stats": {
    "compendiumSource": null,
    "duplicateSource": null,
    "exportSource": null,
    "coreVersion": "13.351",
    "systemId": "genesys",
    "systemVersion": "0.2.18",
    "createdTime": null,
    "modifiedTime": null,
    "lastModifiedBy": null
  },
  "_id": "XXXXXXXXXXXXXXXX",
  "sort": 0,
  "ownership": {
    "default": 0
  }
}
```

Rustningsprofiler:

| Rustning | soak | defense | rarity | encumbrance | price |
|----------|------|---------|--------|-------------|-------|
| Leather Armor | 1 | 0 | 3 | 2 | 50 |
| Chain Mail | 2 | 0 | 4 | 4 | 500 |
| Plate Armor | 3 | 1 | 5 | 5 | 2500 |
| Shield* | 0 | +1 melee | 2 | 2 | 50 |

*Sköld läggs till som armor-item med `soak: 0` och `defense: 1`.

### ID-generering

Alla `_id`-fält ska vara **exakt 16 tecken** alfanumeriska strängar (a-z, A-Z, 0-9). Generera unika ID:n för:
- Aktörens rot-`_id`
- Varje item i `items`-arrayen

### Filnamn och placering

Spara genererade NPC JSON-filer som:
```
campaign/characters/npcs/npc-[namn-lowercase]-[aktörens-_id].json
```

Exempel: `campaign/characters/npcs/npc-torkel-halvhand-Abc123DefGhi456.json`

### Verifikation

**OBLIGATORISKT** efter att JSON-filen skapats:

1. Validera JSON-syntax:
   ```bash
   python3 -c "import json; json.load(open('filnamn.json')); print('JSON valid!')"
   ```

2. Kontrollera att:
   - `type` matchar rätt template (minion/rival/nemesis)
   - Minion har `groupSize` och `wounds.threshold`, saknar `strain`
   - Rival har `wounds.max`, saknar `strain` och `groupSize`
   - Nemesis har `wounds.max` och `strain`, saknar `groupSize`
   - `prototypeToken.bar2.attribute` matchar typen
   - `prototypeToken.actorLink` matchar typen
   - Alla `_id` är exakt 16 tecken
   - `system.soak` = Brawn + rustningsbonus (manuellt beräknad)
   - Bara skills med rank > 0 finns som items

---

## Balanseringsguide

### Hotbedömning

| Faktor | Ökar hotet | Minskar hotet |
|--------|-----------|---------------|
| Antal | Fler motståndare | Färre motståndare |
| Soak | Hög soak (5+) | Låg soak (2-3) |
| Skada | Hög skada (8+) | Låg skada (4-5) |
| Adversary | Adversary 2+ | Ingen Adversary |
| Initiativ | Dubbel initiativ | Normal initiativ |
| Silver | Ingen Silver Anathema | Silver Anathema (om spelarna har silver) |

### Encounter-design

**Lätt encounter:**
- Minion-grupp (antal = spelarna) ELLER
- 1 rival

**Medium encounter:**
- Minion-grupp (antal = spelarna × 1.5) + 1 rival ELLER
- 2-3 rivals

**Svår encounter:**
- 1 nemesis + minion-grupp ELLER
- 1 nemesis + 1-2 rivals

**Boss encounter:**
- 1 nemesis (Adversary 2+, dubbel initiativ) + rivals

---

## Snabbgenerator

### Steg 1: Välj typ och roll
1. Bestäm: Minion, Rival eller Nemesis?
2. Bestäm primär funktion (stridare, magiker, social, etc.)

### Steg 2: Sätt egenskaper
1. Tilldela primär egenskap (3-4)
2. Tilldela sekundär egenskap (2-3)
3. Fördela resterande (1-2)

### Steg 3: Beräkna grundvärden
1. Soak = Brawn + rustning
2. Wounds = Bas + Brawn
3. Strain = Willpower + 10 (nemesis)

### Steg 4: Välj färdigheter
1. Välj 2-4 relevanta skills
2. Sätt ranks (1-3 beroende på typ)

### Steg 5: Lägg till talanger/förmågor
1. Adversary (för nemesis)
2. 1-3 passande talanger
3. Övernaturliga förmågor om relevant

### Steg 6: Utrusta
1. Välj passande vapen
2. Välj rustning
3. Beräkna slutlig soak och defense

---

## Exempelmotståndare

### Banditminn (Minion)

**Roll:** Vanligt kriminellt fotfolk

| Egenskap | Värde |
|----------|-------|
| Brawn | 2 |
| Agility | 2 |
| Intellect | 1 |
| Cunning | 2 |
| Willpower | 1 |
| Presence | 1 |

| Stat | Värde |
|------|-------|
| Soak | 3 |
| Sårtröskel | 5 |
| Försvar | 0/0 |

**Färdigheter (Grupp):** Brawl, Melee, Ranged (Light), Vigilance
**Utrustning:** Svärd (Skada 4, Kritisk 2), Läderdräkt (+1 Soak)

---

### Inkvisitionens Tempelriddare (Rival)

**Roll:** Kyrkans väpnade arm

| Egenskap | Värde |
|----------|-------|
| Brawn | 3 |
| Agility | 2 |
| Intellect | 2 |
| Cunning | 2 |
| Willpower | 3 |
| Presence | 2 |

| Stat | Värde |
|------|-------|
| Soak | 5 |
| Sårtröskel | 13 |
| Försvar | 1/0 |

**Färdigheter:** Discipline 2, Melee (Heavy) 2, Resilience 1, Vigilance 1
**Talanger:**
- **Parry:** Lida 3 strain för att minska närstridsskada med 5

**Utrustning:**
- Silversvärd: Melee (Heavy); Skada 7; Kritisk 2; Silver
- Kedjerustning: +2 Soak
- Sköld: +1 Melee Defense

---

### Skuggvarg (Rival)

**Roll:** Övernaturligt rovdjur

| Egenskap | Värde |
|----------|-------|
| Brawn | 4 |
| Agility | 3 |
| Intellect | 1 |
| Cunning | 3 |
| Willpower | 2 |
| Presence | 1 |

| Stat | Värde |
|------|-------|
| Soak | 4 |
| Sårtröskel | 15 |
| Försvar | 0/0 |

**Färdigheter:** Brawl 2, Perception 2, Stealth 2, Vigilance 1
**Förmågor:**
- **Silver Anathema:** Tar +2 skada från alchemiskt silver
- **Pack Tactics:** +🟦 när allierad skuggvarg är engaged med samma mål

**Utrustning:**
- Klor och huggtänder: Brawl; Skada 7; Kritisk 3; Vicious 1

---

## Referensfiler

### JSON-templates (Foundry VTT)
- `.claude/skills/adversary-creator/references/minion-template.json` — Minion-schema
- `.claude/skills/adversary-creator/references/rival-template.json` — Rival-schema
- `.claude/skills/adversary-creator/references/nemesis-template.json` — Nemesis-schema

### Regler
- `.claude/skills/genesys-rpg/reference/rules/08_ch08_the_game_master.md`
- `.claude/skills/upplandet-campaign/references/invisitionen/chapter_6_adversaries.md`

### Existerande NSC:er
- `campaign/characters/npcs/*.json` — Foundry VTT JSON-filer
- `campaign/characters/npcs/*.md` — Markdown-beskrivningar
- `campaign/adventures/01-dying-light/npcs.md`
