# Upplandet Kampanj - Claude-instruktioner

## Språk

**VIKTIGT:** Allt kampanjmaterial ska skrivas på **svenska**. Detta inkluderar:
- Sessionssammanfattningar
- NPC-beskrivningar
- Platsbeskrivningar
- Kampanjstatus
- Alla anteckningar och dokument

## Projektöversikt

Detta är en rollspelskampanj som använder **Genesys**-systemet med **Inquisition**-settingen, anpassad till svensk geografi (Uppland).

### Spelvärlden
- Kampanjen utspelar sig i **Uppland**, Sverige
- Året är **1532** (sen medeltid)
- Magisk isolering: För 200 år sedan höjdes Uppland och omvärlden blev farlig
- Havsmonster i Östersjön förhindrar handel
- Fyrsystemet håller monster borta från kusten
- Katolska kyrkan jagar häxor (som faktiskt är farliga)

### Nuvarande äventyr
**Döende Ljus** (Dying Light) - Fyren i Östhammar har slocknat.

## Namnkonventioner

Använd svenska namn:
| Originalt | Svenska |
|-----------|---------|
| Darkwood Cove | Östhammar |
| Baron Rowan Lewis | Baron Ragnvald Levin |
| Father Daniel | Fader Daniel |
| Brown family | Familjen Brun |
| Dancing Crab Inn | Dansande Krabban |
| Darkwood Bay | Gråviken |

## Speltermer på svenska

| English | Svenska |
|---------|---------|
| Templar | Tempelriddare |
| Monster Hunter | Monsterjägare |
| Rogue | Skurk |
| Scholar | Lärd |
| Witch | Häxa |
| Banshee | Banshee/Dödsskrikare |
| Success | Framgång |
| Failure | Misslyckande |
| Advantage | Fördel |
| Threat | Hot |
| Triumph | Triumf |
| Despair | Förtvivlan |

## Filstruktur

```
campaign/
├── adventures/          # Äventyrsmoduler
├── characters/          # Spelarkaraktärer och NSC:er
├── locations/           # Platsbeskrivningar
├── sessions/
│   ├── incoming/                # Rå transkript från sessioner
│   ├── session-NN-summary.md      # Sammanfattningar
│   └── session-NN-transcript.md   # Råtranskript från sessioner
├── resources/           # Referensmaterial
└── campaign-status.md   # Aktuell kampanjstatus
```

## Skills

- `genesys-rpg` - För regelfrågor och tärningsmekanik
- `upplandet-campaign` - För kampanjhantering
- `summarizer` - För att skriva sessionssammanfattningar dvs summera spelsessioner.

## Viktiga påminnelser

1. Skriv alltid på svenska
2. Använd svenska ortnamn och personnamn
3. Behåll den mörka, isolerade atmosfären
4. Häxor är verkliga hot i denna värld
5. Fyren är avgörande för Östhammars överlevnad
6. Använd mermaid flowchart diagram för att skapa översikter
