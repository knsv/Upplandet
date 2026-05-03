# AI-prompter för Nattmarknadens tokens

**Syfte:** Generera karaktärs-tokens för Grimske, Vettarvakterna, Fader Sten och Knös till Foundry VTT.
**Rekommenderad stil:** Dark fantasy, hand-painted, RPG portrait. Testa i Midjourney, DALL-E 3, Flux, eller Stable Diffusion.

---

## Gemensam stilgrund (använd i alla prompter)

```
dark nordic folklore fantasy, hand-painted RPG character portrait,
top-down circular token for tabletop VTT, neutral dark background,
dramatic rim lighting, painterly brushwork, 512x512 square composition,
John Bauer inspired forest atmosphere
```

---

## Grimske — Slavhandlaren (Vettarnas Badhus)

```
Tall lean supernatural being called a vettir, older and more defined
than ordinary vettar, standing rigid with unmoving face - unlike the
other shifting vettir faces, his is fixed like carved wood,
cold grey eyes without warmth, mouth a straight line,
bark-like skin with mossy patches in deep forest green,
wearing a bark apron and dark leather vest with iron buckles,
a small iron key hanging on a leather cord around his neck,
long black iron claws on each finger like hooks,
hands held low and ready, coiled stillness,
steam from a bathhouse rising behind him,
dark nordic folklore fantasy, hand-painted RPG character portrait,
top-down circular token for tabletop VTT, neutral dark background,
dramatic rim lighting, painterly brushwork, 512x512 square composition,
John Bauer inspired forest atmosphere
```

**Negativ prompt:** `cartoon, anime, photorealistic, modern clothing, guns, sci-fi, bright cheerful colors, cute, feminine beauty, smiling`

---

## Vettarvakter — Minion-grupp (×4)

```
Thin supernatural forest beings called vettar, spindly and gray-skinned,
shifting unclear faces that blur between human, animal, and blank -
one moment a human face, the next a badger, the next empty,
bark aprons worn over grey woven fabric, long fingers with iron claws,
spectral ghost-like presence, half-transparent at the edges,
moving in unison as if one creature, standing guard posture,
minor guardian creatures, steam and dim lantern light around them,
dark nordic folklore fantasy, hand-painted RPG character portrait,
top-down circular token for tabletop VTT, neutral dark background,
dramatic rim lighting, painterly brushwork, 512x512 square composition,
John Bauer inspired forest atmosphere
```

**Negativ prompt:** `cartoon, anime, photorealistic, modern clothing, guns, sci-fi, bright cheerful colors, cute, distinct individual features`

**Tips:** Generera 4 varianter eller ett enda "gruppformat" med 2-3 vettar bredvid varandra.

---

## Fader Sten — Trollpräst (Trollkyrkan)

```
Enormous forest troll standing three meters tall, hulking but earnest posture,
grey-green rough skin like moss-covered bark, large yellow eyes the size of fists,
wide gentle face with tusks, massive clumsy hands held together in prayer,
wearing a stolen Catholic priest's stola that is far too small for him,
the stola draped awkwardly over massive shoulders, embroidered with faded crosses,
a necklace of crude pine-stick cross around his thick neck,
holding a piece of stolen communion bread reverently in one hand,
an upside-down Latin prayer book clutched in the other,
devout expression, trying desperately to understand something holy,
candle light and a mossy altar behind him,
dark nordic folklore fantasy, hand-painted RPG character portrait,
top-down circular token for tabletop VTT, neutral dark background,
dramatic rim lighting, painterly brushwork, 512x512 square composition,
John Bauer inspired forest atmosphere
```

**Negativ prompt:** `cartoon, anime, photorealistic, modern clothing, guns, sci-fi, evil grin, menacing pose, bright cheerful colors`

**Notering:** Fader Sten är INTE en fiende. Bilden ska kommunicera naivitet, fromhet och förvirring — inte hot. Fokus på "ett troll som försöker förstå det heliga".

---

## Knös — Marknadens ordningsvakt

```
Colossal ancient troll the size of two oxen stacked together,
massive immobile silhouette with moss and lichen growing on stone-like skin,
weathered grey granite flesh with deep cracks filled with glowing orange embers,
slow ember-orange eyes barely open, deeply set in a heavy brow,
no clothing - ancient stone-flesh, knotted shoulders like boulders,
standing perfectly still in shadow, arms at his sides,
small trees and plants have grown from his back and shoulders,
like a creature carved from a mountain that learned to stand,
intimidating presence but not moving, mossy, primordial,
dim orange lantern light from the market behind him,
dark nordic folklore fantasy, hand-painted RPG character portrait,
top-down circular token for tabletop VTT, neutral dark background,
dramatic rim lighting from below, painterly brushwork, 512x512 square composition,
John Bauer inspired forest atmosphere, towering giant
```

**Negativ prompt:** `cartoon, anime, photorealistic, modern clothing, guns, sci-fi, small troll, cute, fast motion, active pose`

**Notering:** Knös ska kommunicera OVERWHELMING threat genom storlek och stillhet — inte genom aggression. Han är en naturkraft. Han behöver inte röra sig. När han rör sig är det försent.

---

## Tips för konsistent marknadens-stil

Alla marknadens väsen delar:
- **Skogens material** — bark, mossa, sten, lava, järn
- **Halv-mänsklig, halv-fenomen** — de är fysiska men inte helt
- **John Bauer-atmosfär** — den svenska illustratören från tidigt 1900-tal
- **Lykt-ljus** — blå, grön eller orange sken i bakgrunden

**Keyword-lås över alla prompter:**
- "supernatural being/troll/vettir"
- "John Bauer inspired forest atmosphere"
- "dark nordic folklore fantasy"

**Alternativ för mer skräck-känsla:**
Lägg till i slutet: `unsettling, liminal horror, beautiful but wrong`

---

## Foundry VTT — efterbehandling

1. Skär ut cirkel ur bilden
2. Lägg till Foundry token-ring
3. Spara som PNG med transparent bakgrund (512x512 eller 1024x1024)
4. För Knös: eventuellt **double-size token** (width: 2, height: 2) för att visuellt visa hans storlek

## Som scenbilder (inte tokens)

**Vettarnas Badhus — scenbild:**
```
Underground dim bathhouse with stone steam rooms,
three beautiful glowing-winged fairy women in thin spun-light clothing,
iron collars with pulsing control-stones around their necks,
their smiles perfect but their eyes looking downward in silent plea,
vettar guards in background with shifting faces, lanterns and steam,
John Bauer fantasy illustration, atmospheric horror,
painterly dark fantasy, slave market disguised as spa
```

**Trollkyrkan — scenbild:**
```
Crude church inside a supernatural market, constructed from logs,
moss, and stolen Catholic church textiles, altar cloth with embroidered crosses
hanging as door curtain, inside a circle of troll congregation -
young trolls, vittror, a stone with eyes all sitting attentively,
three-meter tall troll priest Fader Sten in ill-fitting stole,
holding bread reverently, upside-down prayer book in other hand,
candlelight, reverent atmosphere, earnest and absurd,
John Bauer fantasy illustration
```
