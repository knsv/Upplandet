# AI-prompter för bergtroll-tokens (Holmgången)

**Syfte:** Generera karaktärs-tokens för Grimtand, Lurkna och Bullrik till Foundry VTT.
**Rekommenderad stil:** Dark fantasy, hand-painted, RPG portrait. Testa i Midjourney, DALL-E 3, Flux, eller Stable Diffusion.

---

## Gemensam stilgrund (använd i alla prompter)

```
dark nordic folklore fantasy, hand-painted RPG character portrait,
top-down circular token for tabletop VTT, neutral dark background,
dramatic rim lighting, painterly brushwork, 512x512 square composition,
muted earth tones with subtle glowing accents
```

---

## Grimtand — ledaren, aggressiv

```
Mountain troll brother from a Swedish iron mine, young adult,
stocky broad-shouldered warrior, standing two meters tall but barrel-chested,
skin like cracked pumice stone in grey with faintly glowing green and red veins,
teeth filed to sharp points, menacing wide grin, painted green stripes across his chest,
eyes like shifting orange-red crystals, matted hair with coal dust and mountain grit,
worn leather armor with iron studs and rivets, fingerless gloves,
carrying a spiked iron-wrapped fist-club (nävklubba),
aggressive posture, shouting challenge, battle-scarred,
dark nordic folklore fantasy, hand-painted RPG character portrait,
top-down circular token for tabletop VTT, neutral dark background,
dramatic rim lighting, painterly brushwork, 512x512 square composition,
muted earth tones with subtle glowing accents
```

**Negativ prompt (om stödd):** `cartoon, anime, photorealistic, modern clothing, weapons, guns, sci-fi, bright cheerful colors, cute, chibi`

---

## Lurkna — den smala, listiga

```
Mountain troll brother from a Swedish iron mine, young adult, lean and wiry,
smaller and narrower than typical trolls but sinewy with taut muscles,
skin like cracked pumice stone in grey with faintly glowing green and red veins,
sharp cunning face, yellow crystalline eyes with vertical pupils, smirking mockingly,
long sharp black claws on fingers, pointed ears, matted hair with coal dust,
ragged leather vest with iron studs, scar across one eye,
crouching agile posture, ready to dart forward,
dark nordic folklore fantasy, hand-painted RPG character portrait,
top-down circular token for tabletop VTT, neutral dark background,
dramatic rim lighting, painterly brushwork, 512x512 square composition,
muted earth tones with subtle glowing accents
```

**Negativ prompt (om stödd):** `cartoon, anime, photorealistic, modern clothing, guns, sci-fi, bright cheerful colors, cute, feminine, elegant`

---

## Bullrik — den tysta muskelklumpen

```
Mountain troll brother from a Swedish iron mine, young adult but enormous,
massive muscular giant, thick-necked, stone-like skin resembling cracked granite,
grey with faintly pulsing green and red mineral veins, blunt heavy features,
small dull eyes like dim orange coals, slack expression, bald or nearly bald head
with coal dust and stone grit, thick leather kilt and iron-banded boots,
no weapon - just massive knotted stone-hard fists raised, heavy breathing,
lumbering stance, like a walking mountain,
dark nordic folklore fantasy, hand-painted RPG character portrait,
top-down circular token for tabletop VTT, neutral dark background,
dramatic rim lighting, painterly brushwork, 512x512 square composition,
muted earth tones with subtle glowing accents
```

**Negativ prompt (om stödd):** `cartoon, anime, photorealistic, modern clothing, weapons, guns, sci-fi, bright cheerful colors, cute, thin, athletic`

---

## Tips för konsistent stil över alla tre

1. **Generera alla tre i samma sitting** (samma AI-modell, samma session) för att få konsekventa ansikten och färgpaletter.
2. **Använd en seed/referens** om din generator stödjer det — generera Grimtand först, använd sedan dess seed eller stil-referens för Lurkna och Bullrik.
3. **Keyword-lås:**
   - "mountain troll brother" (samma fras i alla tre)
   - "cracked pumice stone skin with green and red veins" (samma hudbeskrivning)
   - "coal dust, mountain grit" (samma miljö-tillhörighet)
4. **Fysiska skillnader att betona:**
   - Grimtand: **medelstor, bred, tandad grinande aggression**
   - Lurkna: **smal, ryckig, listig**
   - Bullrik: **enorm, trög, mure-lik**

## Alternativ stil — om du vill ha mörkare tonbild

Byt ut slutraden mot:
```
dark horror fantasy, gritty digital painting, low-key lighting,
atmospheric shadows, subtle bioluminescent mineral glow, 512x512 token
```

## För Foundry VTT — efterbehandling

- Skär ut cirkel ur bilden (verktyg: Photopea, GIMP, eller online token-makers)
- Lägg till Foundry token-ring (system → prototypeToken → ring.enabled: true)
- Spara som PNG med transparent bakgrund
- Importera via drag-drop på actor

---

## Som kompletteringsbild — scenen i ringen

Om du vill ha en scenbild snarare än tokens:

```
Three mountain troll brothers standing in a glowing stone runic arena,
raised fist-pumps to jeering crowd of trolls, vittror, and goblins,
a medieval fantasy market at night around them, blue and green floating lanterns,
dramatic torchlight, Swedish nordic folklore fantasy setting,
painterly dark fantasy illustration, atmospheric, cinematic wide angle,
the biggest troll (Grimtand) pointing aggressively toward the viewer,
the lean one (Lurkna) grinning behind him, the massive silent one (Bullrik)
with arms crossed, runes glowing red in the stone circle around them
```
