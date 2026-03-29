# Herbes Remeieres — Full de ruta de millores

Guardar a `.claude/ROADMAP.md` perquè Claude Code el tingui com a referència.

---

## Fase 1 — Fonaments (fer primer, afecta tot el portal)

### 1.1 Toggle mode clar/fosc
- Botó lluna/sol a la capçalera (dreta, abans del menú mòbil)
- Clic a 🌙 → activa mode fosc, canvia icona a ☀️
- Persistir preferència a `localStorage`
- Respectar `prefers-color-scheme` del sistema com a default
- Transició suau (300ms ease-in-out) entre modes
- **Eina:** Claude Code directament (component Astro natiu amb JS)
- **Referència:** els tokens `[data-theme="dark"]` ja estan al design-tokens.css

### 1.2 Layout responsive modern
- Eliminar `max-width: 1200px` rígid del `main`
- Implementar sistema fluid:
  - Contingut de text: `max-width: 780px` centrat (millor lectura)
  - Grids de cards: `max-width: 1400px` (o full-width amb padding)
  - Hero i seccions destacades: full-width
  - Padding lateral: `clamp(1rem, 5vw, 4rem)`
- Usar `container queries` on calgui
- **Eina:** Claude Code + skill UI/UX Pro Max

---

## Fase 2 — La Home (el primer impacte)

### 2.1 Redisseny radical del Hero
- Fora la imatge genèrica d'Unsplash
- Dues opcions a explorar:
  - **Opció A:** Il·lustració botànica lineal de fons (dona amb cistella al bosc,
    herbes reconegudes com rosella, romaní, espígol, dent de lleó en dibuix lineal)
    generada amb Nano-Banana, estil line art sobre fons crema/verd fosc
  - **Opció B:** Disseny minimalista tipus Anthropic, amb tipografia gran
    Cormorant Garamond i detalls botànics subtils (SVG line art)
- Text del hero: titular potent + subtítol + CTA cap a l'Herbari
- **Eina:** Nano-Banana per generar la il·lustració base, Claude Code per implementar

### 2.2 Seccions de la Home
- Secció "Plantes destacades" (3-4 cards de plantes populars)
- Secció "Explora per afecció" (cards amb les categories: sistema digestiu,
  respiratori, nerviós, pell, etc.)
- Secció "Sobre el projecte" (breu, amb link a /projecte)
- Animacions d'entrada amb stagger (Emil Kowalski, ja definides als tokens)
- **Eina:** Stitch per dissenyar el layout, 21st.dev per components interactius,
  Claude Code per implementar

---

## Fase 3 — Fitxa de planta (el cor del projecte)

### 3.1 Ampliar dades mostrades (les que ja tens al backend)
- Nom comú (ja es mostra)
- Nom científic (ja es mostra)
- **Altres noms comuns** ← afegir
- **Família botànica** ← afegir (amb link al filtre del catàleg)
- **Descripció breu** ← afegir
- Propietats medicinals (ja es mostra com a tags)
- Usos medicinals (ja es mostra)

### 3.2 Crear nous camps al backend WordPress
- **Preparacions:** tipus de preparació (infusió, decocció, cataplasma, oli
  macerat, xarop, tintura), amb instruccions per cadascuna
- **Precaucions:** text lliure + nivell (lleu/moderat/greu), amb icona
  d'advertència visual
- **Època de recol·lecció:** mesos de l'any (camp repeater o checkboxes
  amb els 12 mesos)

### 3.3 Redissenyar l'estructura de la fitxa
```
┌─────────────────────────────────────────────────────┐
│ ← Tornar a l'Herbari              Família botànica  │
├────────────────────────┬────────────────────────────┤
│                        │ h1: Nom comú               │
│    [Imatge gran]       │ Nom científic (cursiva)    │
│                        │ Altres noms: xxx, yyy      │
│                        │                            │
│                        │ Descripció breu            │
│                        │                            │
│                        │ [Tags de propietats]       │
├────────────────────────┴────────────────────────────┤
│                                                     │
│ ## Usos medicinals                                  │
│ Text descriptiu complet                             │
│                                                     │
│ ## Com preparar-la              [icones de tipus]   │
│ Infusió | Decocció | Cataplasma | ...               │
│ (tabs o acordió amb instruccions per cada tipus)     │
│                                                     │
│ ## Precaucions                  ⚠️ Nivell: moderat  │
│ Text de precaucions amb fons --accent-amber-soft    │
│                                                     │
│ ## Quan recollir-la                                 │
│ [Calendari visual: 12 mesos, destacats els actius]  │
│                                                     │
├─────────────────────────────────────────────────────┤
│ Plantes relacionades (3 cards)                      │
└─────────────────────────────────────────────────────┘
```

- **Eines:** Claude Code per la query GraphQL ampliada, Stitch per dissenyar
  el layout de la fitxa, 21st.dev per components React interactius (calendari,
  tabs de preparació), skill Emil Kowalski per animacions

---

## Fase 4 — Herbari / Catàleg millorat

### 4.1 Millorar filtres (referència: JustWatch)
- Filtres com a barra horitzontal o sidebar plegable
- Tags seleccionables amb estat actiu visual (fons --accent-green, text clar)
- Botó "Esborrar tots els filtres" ben visible
- Comptador de resultats ("12 plantes trobades")
- Filtres actius mostrats com a pills amb X per eliminar individualment
- Animació fade in/out al filtrar (200ms ease-out)
- **Eina:** 21st.dev per generar el component React de filtres, Claude Code
  per connectar amb les dades de WPGraphQL

### 4.2 Cards del catàleg
- Aplicar nou disseny de card definit al Design System
- Hover amb translateY(-2px) i border accent-green
- Mostrar família botànica a la card
- Stagger animation a l'entrada

---

## Fase 5 — Pàgines pendents

### 5.1 El Projecte (/projecte)
- Explicar la història: d'on neix la iniciativa
- Què volem preservar (coneixement etnobotànic del Bages i Moianès)
- L'equip (si escau)
- Disseny editorial, full-width, amb fotografies intercalades

### 5.2 Contacte (/contacte)
- Formulari simple (nom, email, missatge)
- Info de contacte
- Potser mapa de la zona del Bages/Moianès

### 5.3 Glossari millorat (/glossari)
- **Índex alfabètic fixe a l'esquerra** (A-Z, sticky on scroll)
  - Desktop: sidebar esquerra fixa
  - Mòbil: barra horitzontal scrollable a dalt
- Salt ràpid a cada lletra (anchor links)
- Cada terme del glossari com a element amb id
- **Linking automàtic a tota la web:** crear un component Astro que
  processi el text i converteixi paraules del glossari en links.
  Enfocament:
  1. Fer una query GraphQL de tots els termes del glossari
  2. Crear un component `<TextAmbGlossari text={contingut} termes={glossari} />`
  3. El component busca coincidències i les envolta amb `<a href="/glossari#terme">`
  4. Mostrar tooltip on hover amb la definició breu
- **Eina:** Claude Code (component Astro + lògica de matching)

---

## Ordre recomanat d'execució

```
Setmana 1:  Fase 1 (toggle + responsive) — afecta tot, fer primer
Setmana 2:  Fase 3.1-3.2 (ampliar dades fitxa + camps backend)
Setmana 3:  Fase 3.3 + Fase 4 (redisseny fitxa + filtres)
Setmana 4:  Fase 2 (home — amb les fitxes ja boniques es nota el canvi)
Setmana 5:  Fase 5 (pàgines pendents)
```

Les setmanes són orientatives — depèn del temps que hi puguis dedicar.

---

## Eines per fase

| Fase | Claude Code | Stitch | Nano-Banana | 21st.dev | UI/UX Pro | Emil anim |
|------|:-----------:|:------:|:-----------:|:--------:|:---------:|:---------:|
| 1    | ✓           |        |             |          | ✓         | ✓         |
| 2    | ✓           | ✓      | ✓           | ✓        | ✓         | ✓         |
| 3    | ✓           | ✓      |             | ✓        | ✓         | ✓         |
| 4    | ✓           |        |             | ✓        | ✓         | ✓         |
| 5    | ✓           |        | ✓           |          | ✓         |           |
