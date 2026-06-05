# Kopparmossvägen 25 — Trädgårdsplanering

Interaktiv visualisering och kostnadsestimat för trädgården till Villa Lindbacken på
Vaksala-Lunda 39:4, Kopparmossvägen 25, Uppsala.

## 🌐 Live

GitHub Pages: <https://sebastianclaesson.github.io/Kopparmossvagen25/>

## 📁 Innehåll

| Fil | Beskrivning |
|---|---|
| [`index.html`](./index.html) | **2D-skiss** — situationsplan i skala 1:200, alla mått exakta |
| [`3d.html`](./3d.html) | **3D-vy** — interaktiv WebGL-rendering (Three.js), roterbar |
| [`priser.html`](./priser.html) | **Prislista** — kostnadsestimat per variant + jämförelse |
| [`planering.html`](./planering.html) | **Planering** — Gantt-tidslinje från inflyttning dec 2026 → 2031+ |

## 🏡 Fastighet

- **Adress:** Kopparmossvägen 25, 75472 Uppsala
- **Fastighetsbeteckning:** Vaksala-Lunda 39:4
- **Tomtarea:** 688,5 m² (20,25 × 34 m)
- **Hus:** A-hus Lindbacken R Flex (modern), 172 m² över 2 våningar
- **Carport + förråd:** 33,8 m²

## 🌱 6 Layout-varianter

| | Variant | Total (medel) |
|---|---|---|
| **A** | Pool i söder (kortsidan mot hus) | ~787 000 kr |
| **B** | Pool längs SV (vid carporten) | ~787 000 kr |
| **C** | Bubbelpool + bastu (utan pool) | ~640 000 kr |
| **D** | Bara fin trädgård (pergola + eldstad) | ~515 000 kr |
| **E** | Pool i söder (långsida mot hus) | ~790 000 kr |
| **⭐ F** | Familjeparadis — bastu + spa + utekök + pergola + plaskdam + odlingslådor + eldstad | ~881 000 kr |

Klicka mellan varianterna i toppen av 2D- och 3D-vyerna. Variant F är min ärliga rekommendation: året-runt-användning, lägre drift än pool, högre återförsäljningsvärde.

## ⚙️ Teknik

Helt statisk webbplats — fungerar direkt via GitHub Pages.

- **2D:** vanilj-SVG, koordinatsystem 1 m = 14 px (1:200-skala)
- **3D:** Three.js r162 (laddas från unpkg CDN), WebGL via ES-moduler
- **CSS:** ren CSS utan ramverk
- **JS:** vanilla, ingen build-process

## 🛠️ Lokal utveckling

ES-moduler i 3D-vyn kräver en lokal webserver (`file://` fungerar inte):

```powershell
# Python
python -m http.server 8000

# Eller Node.js
npx serve
```

Öppna sedan `http://localhost:8000/`.

## 📐 Mått (källa: bygglov 2025-11-27)

| Element | Mått | Källa |
|---|---|---|
| Tomt yttermått | 20,25 × 34 m | Förrättningskarta KA1 |
| Hus fotavtryck | 7,73 × 12,83 m | A-P01 |
| Carport totalt | 3,94 × 8,69 m | A-G01 |
| Hus → NÖ-granne | 3,0 m | användaruppgift |
| Carport → SV-granne | 1,5 m | användaruppgift |
| Hus → väg (NV) | 5,0 m | användaruppgift |
| Carport → väg (NV) | 5,0 m (i linje med hus) | användaruppgift |

## 📋 Status

- [x] 2D-skiss med alla 5 varianter
- [x] 3D-rendering med WebGL
- [x] Kostnadsestimat per variant
- [x] Pris-jämförelse + rekommendation
- [x] Korrekta mått från bygglov + förrättningskarta
- [ ] Verifierat på faktisk plats / med trädgårdsarkitekt

## 📜 Licens

Personlig projekt — inte avsett för publik användning.
