# Herbes Remeieres — Sistema de disseny "Bosc Místic"

Identitat visual per al portal de plantes medicinals del Bages i el Moianès.

---

## Essència

El disseny evoca el bosc a la penombra, la saviesa ancestral de les dones
que coneixien cada planta pel seu nom, la connexió profunda amb la terra.
Un portal que respira natura sense artificiositat: seriós en el rigor
botànic, càlid en el tracte amb l'usuari, i místic en l'estètica.

**Paraules clau:** arrels, penombra, saviesa, terra, molsa, ambre.

---

## 1. Paleta de colors

### Mode clar (per defecte)

| Token                | Hex       | Ús                                          |
|----------------------|-----------|----------------------------------------------|
| `--bg-primary`       | `#F2EDE4` | Fons principal (crema natural)               |
| `--bg-secondary`     | `#EAE4D8` | Superfícies, cards, seccions                 |
| `--bg-tertiary`      | `#E0D8C8` | Hover de superfícies                         |
| `--text-primary`     | `#3D2B1F` | Text principal (terra fosca)                 |
| `--text-secondary`   | `#6B5744` | Text secundari, descripcions                 |
| `--text-tertiary`    | `#8B7355` | Text subtle, metadades, escorça              |
| `--accent-green`     | `#4A6741` | Accent primari (molsa)                       |
| `--accent-green-soft`| `#5B7D51` | Hover del verd                               |
| `--accent-amber`     | `#D4A843` | Accent secundari (ambre)                     |
| `--accent-amber-soft`| `#C49A35` | Hover de l'ambre                             |
| `--border-default`   | `#D4C9B8` | Bordes principals                            |
| `--border-subtle`    | `#E0D8C8` | Bordes subtils                               |
| `--tag-bg`           | `rgba(74,103,65,0.12)` | Fons de tags/badges              |
| `--tag-text`         | `#4A6741` | Text de tags                                 |

### Mode fosc

| Token                | Hex       | Ús                                          |
|----------------------|-----------|----------------------------------------------|
| `--bg-primary`       | `#1A3C2A` | Fons principal (bosc profund)                |
| `--bg-secondary`     | `#1F4432` | Superfícies, cards                           |
| `--bg-tertiary`      | `#24503A` | Hover de superfícies                         |
| `--text-primary`     | `#F2EDE4` | Text principal (crema)                       |
| `--text-secondary`   | `#C5D4B5` | Text secundari (verd clar)                   |
| `--text-tertiary`    | `#8B9E7D` | Text subtle                                  |
| `--accent-green`     | `#7DB56A` | Accent primari (verd clar)                   |
| `--accent-green-soft`| `#90C47E` | Hover del verd                               |
| `--accent-amber`     | `#D4A843` | Accent secundari (ambre, es manté)           |
| `--accent-amber-soft`| `#E0B84F` | Hover de l'ambre                             |
| `--border-default`   | `#2D5A3F` | Bordes principals                            |
| `--border-subtle`    | `#24503A` | Bordes subtils                               |
| `--tag-bg`           | `rgba(125,181,106,0.15)` | Fons de tags              |
| `--tag-text`         | `#7DB56A` | Text de tags                                 |

### Colors semàntics (iguals en ambdós modes)

| Token               | Clar       | Fosc       | Ús                           |
|----------------------|------------|------------|-------------------------------|
| `--color-caution`    | `#B8860B`  | `#D4A843`  | Precaucions, toxicitat lleu   |
| `--color-danger`     | `#8B3A3A`  | `#C75050`  | Plantes tòxiques, alertes    |
| `--color-info`       | `#4A6741`  | `#7DB56A`  | Propietats, info general     |
| `--color-highlight`  | `#D4A843`  | `#D4A843`  | Noms científics en cursiva   |

---

## 2. Tipografia

### Fonts

| Rol           | Font               | Pes              | Mida          |
|---------------|--------------------|------------------|---------------|
| Titulars h1   | Cormorant Garamond | 400 (Regular)    | 40px / 2.5rem |
| Titulars h2   | Cormorant Garamond | 500 (Medium)     | 28px / 1.75rem|
| Titulars h3   | Cormorant Garamond | 500 (Medium)     | 22px / 1.375rem|
| Cos de text   | Lato               | 400 (Regular)    | 16px / 1rem   |
| Text petit    | Lato               | 400 (Regular)    | 14px / 0.875rem|
| Nom científic | Cormorant Garamond | 400 Italic       | hereta del pare|
| Tags/badges   | Lato               | 500 (Medium)     | 12px / 0.75rem|
| Nav/UI        | Lato               | 400 (Regular)    | 15px / 0.9375rem|

### Importació (Google Fonts)

```html
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Lato:wght@300;400;500;700&display=swap" rel="stylesheet">
```

### Regles tipogràfiques

- Títols en Cormorant Garamond, mai en majúscules. Preferir minúscules naturals.
- Noms científics sempre en cursiva amb `--accent-green` (clar) o `--accent-amber` (fosc).
- Noms populars catalans en negreta suau (500), mai en CAPS.
- `letter-spacing: -0.02em` en h1 per a un aire editorial.
- `line-height: 1.7` per al cos de text (lectura confortable).
- `line-height: 1.2` per als títols.

---

## 3. Espaiats i layout

### Sistema d'espaiats

| Token    | Valor  | Ús                                  |
|----------|--------|--------------------------------------|
| `--sp-1` | 4px    | Gaps mínims, padding de tags         |
| `--sp-2` | 8px    | Gaps interns petits                  |
| `--sp-3` | 12px   | Gap entre tags, padding cards intern |
| `--sp-4` | 16px   | Marge entre elements                 |
| `--sp-5` | 24px   | Padding de cards                     |
| `--sp-6` | 32px   | Separació entre seccions             |
| `--sp-7` | 48px   | Marge vertical entre blocs           |
| `--sp-8` | 64px   | Separació de seccions grans          |
| `--sp-9` | 96px   | Hero, header, footer                 |

### Grid

- Contingut principal: `max-width: 1200px` centrat.
- Catàleg (cards): `grid-template-columns: repeat(auto-fill, minmax(320px, 1fr))` amb `gap: 24px`.
- Fitxa de planta: layout de 2 columnes (imatge + info) a desktop, 1 columna a mòbil.
- Breakpoints: `768px` (tablet), `1024px` (desktop).

### Border radius

| Ús                  | Valor   |
|---------------------|---------|
| Tags, badges        | `20px`  |
| Botons              | `8px`   |
| Cards               | `12px`  |
| Imatges dins cards  | `8px`   |
| Contenidors grans   | `16px`  |

---

## 4. Components

### Card de planta (catàleg)

```
┌─────────────────────────────┐
│ [Imatge .webp 4:3]          │
│                             │
├─────────────────────────────┤
│ Família: Lamiàcies          │ ← text-tertiary, 12px
│                             │
│ Herba de la feridura        │ ← Cormorant, h3, text-primary
│ Sideritis hirsuta           │ ← Cormorant italic, accent-green/amber
│                             │
│ ┌──────┐ ┌────────────┐    │
│ │ Tag  │ │ Tag llarg  │    │ ← tags amb bg verd suau
│ └──────┘ └────────────┘    │
│                             │
│ Text breu dels usos...      │ ← Lato, text-secondary, max 3 línies
│                             │
│ Saber-ne més →              │ ← accent-green, hover underline
└─────────────────────────────┘
```

- Fons: `--bg-secondary`
- Border: `0.5px solid --border-subtle`
- Hover: eleva la card amb `transform: translateY(-2px)` + `border-color: --accent-green`
- Transició: `200ms ease-out` (Emil Kowalski: entrades amb ease-out)

### Fitxa individual de planta

```
┌─────────────────────────────────────────────────────┐
│ ← Tornar al catàleg            Família: Lamiàcies   │
├──────────────────────┬──────────────────────────────┤
│                      │ h1: Herba de la feridura     │
│   [Imatge gran]      │ Sideritis hirsuta (cursiva)  │
│                      │                              │
│                      │ Noms populars:               │
│                      │ Cua de gat, presa de la creu │
│                      │                              │
│                      │ [Tags de propietats]         │
├──────────────────────┴──────────────────────────────┤
│                                                     │
│ ## Usos medicinals                                  │
│ Text descriptiu complet...                          │
│                                                     │
│ ## Preparació                                       │
│ Infusió / Decocció / Cataplasma                     │
│                                                     │
│ ## Precaucions                                      │
│ (amb icona d'advertència en --color-caution)        │
│                                                     │
│ ## Època de recol·lecció                            │
│ Calendari visual amb mesos destacats                │
│                                                     │
├─────────────────────────────────────────────────────┤
│ 🌿 Plantes relacionades (3 cards)                   │
└─────────────────────────────────────────────────────┘
```

### Navegació

- Fons transparent amb blur (`backdrop-filter: blur(12px)`) sobre scroll.
- Logo: "Herbes Remeieres" en Cormorant Garamond 500.
- Enllaços en Lato 400, 15px.
- Hover: underline animat amb `--accent-green` (slide from left, 200ms).
- Mòbil: menú hamburguesa amb overlay a pantalla completa, fons `--bg-primary`.

### Botons

| Tipus      | Fons              | Text            | Border                    |
|------------|-------------------|-----------------|---------------------------|
| Primari    | `--accent-green`  | `--bg-primary`  | cap                       |
| Secundari  | transparent       | `--accent-green`| `1px solid --accent-green`|
| Ghost      | transparent       | `--text-secondary`| cap                     |

- Hover: `transform: translateY(-1px)` + lleugera variació de color.
- Active: `transform: scale(0.98)` — feedback tàctil instantani.
- Transició: `150ms ease-out`.

### Footer

- Fons: `--bg-secondary` (clar) / `#152E20` (fosc, més profund que el body).
- Estructura: 3 columnes (sobre el projecte, navegació, legal + contacte).
- Logo + frase: Cormorant Garamond italic, `--text-tertiary`.

---

## 5. Imatges i recursos visuals

### Fotografies

- Format: `.webp`, qualitat 80%.
- Aspect ratio de cards: `4:3`.
- Aspect ratio de fitxa individual: lliure, mínim `600px` d'ample.
- Totes les fotos pròpies (les que ja tens són excel·lents).
- Si cal complementar: Nano-Banana per generar il·lustracions botàniques.

### Estil d'il·lustració (per a Nano-Banana)

Quan generis imatges amb IA, usa aquest prompt base:

> "Botanical illustration of [PLANTA], ink and watercolor style on aged
> parchment paper, detailed scientific illustration with visible brush
> strokes, muted earth tones, herbarium specimen style, no background"

### Iconografia

- Icones simples, traç fi (1.5px), estil line art.
- Usa Lucide Icons o Heroicons (outline).
- Color: `--text-tertiary` per defecte, `--accent-green` en hover.
- Mida: 20px en navegació, 24px en seccions.

---

## 6. Animacions (Emil Kowalski)

### Principis

- Invisibles: l'usuari nota que la interfície es percep bé, no nota l'animació.
- Ràpides: micro-interaccions < 200ms, transicions < 300ms.
- ease-out per entrades, ease-in per sortides.
- Només `transform` i `opacity` (GPU-accelerat).
- Sempre respectar `prefers-reduced-motion`.

### Catàleg d'animacions

| Element              | Propietat                    | Durada | Easing              |
|----------------------|------------------------------|--------|----------------------|
| Card hover           | `translateY(-2px), opacity`  | 200ms  | `ease-out`           |
| Card tap             | `scale(0.98)`                | 100ms  | `ease-out`           |
| Entrada de pàgina    | `opacity 0→1, y 8→0`        | 250ms  | `cubic-bezier(0.22, 1, 0.36, 1)` |
| Tags stagger         | `opacity, y 6→0`            | 150ms  | `ease-out` + 40ms stagger |
| Nav link hover       | `width 0→100%` (underline)  | 200ms  | `ease-out`           |
| Toggle mode clar/fosc| colors, backgrounds          | 300ms  | `ease-in-out`        |
| Imatge fitxa zoom    | `scale(1→1.02)`             | 300ms  | `ease-out`           |
| Filtre catàleg       | `opacity` (fade in/out)      | 200ms  | `ease-out`           |

### Implementació amb Motion (React)

Per als components React (isles d'Astro):

```jsx
// Entrada de card
<motion.div
  initial={{ opacity: 0, y: 8 }}
  animate={{ opacity: 1, y: 0 }}
  transition={{ duration: 0.25, ease: [0.22, 1, 0.36, 1] }}
/>

// Stagger de tags
<motion.ul
  initial="hidden"
  animate="visible"
  variants={{
    visible: { transition: { staggerChildren: 0.04 } }
  }}
>
  {tags.map(tag => (
    <motion.li
      key={tag}
      variants={{
        hidden: { opacity: 0, y: 6 },
        visible: { opacity: 1, y: 0 }
      }}
    />
  ))}
</motion.ul>
```

### CSS per a components Astro natius

```css
@media (prefers-reduced-motion: no-preference) {
  .card {
    transition: transform 200ms ease-out, border-color 200ms ease-out;
  }
  .card:hover {
    transform: translateY(-2px);
  }
  .card:active {
    transform: scale(0.98);
  }
  .page-enter {
    animation: fadeUp 250ms cubic-bezier(0.22, 1, 0.36, 1) forwards;
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }
}
```

---

## 7. Mode clar / fosc

### Implementació CSS

```css
:root {
  color-scheme: light dark;
  /* Mode clar per defecte */
  --bg-primary: #F2EDE4;
  --bg-secondary: #EAE4D8;
  --text-primary: #3D2B1F;
  --accent-green: #4A6741;
  --accent-amber: #D4A843;
  /* ... resta de tokens */
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg-primary: #1A3C2A;
    --bg-secondary: #1F4432;
    --text-primary: #F2EDE4;
    --accent-green: #7DB56A;
    /* ... resta de tokens */
  }
}
```

### Toggle manual (opcional)

Si vols afegir un botó per canviar de mode, implementa-ho amb un
component React (illa d'Astro) que afegeixi `data-theme="dark"` al `<html>`.

---

## 8. Noms alternatius per al projecte

En lloc de "catàleg":

- **Herbari** — el més natural i fidel a la tradició.
- **Recull** — neutre i proper.
- **Vademècum verd** — un punt més poètic.

Proposta per al menú de navegació:

```
Inici · Herbari · El projecte · Glossari · Contacte
```

---

## Arxius de referència

Guardar aquest document a `.claude/DESIGN_SYSTEM.md` dins del projecte
perquè Claude Code el consulti automàticament en cada sessió de treball.
