# Slide Aulab — C#

Presentazioni interattive per le lezioni del corso C#.
Costruite con **Reveal.js** (presentazioni) + HTML/CSS puro (homepage).

---

## Struttura del progetto

```
/
├── index.html              ← homepage: lista di tutte le lezioni
├── shared/
│   ├── styles.css          ← stile condiviso per tutte le lezioni
│   └── DESIGN_SYSTEM.md    ← riferimento visivo per creare nuove slide
└── lessons/
    ├── 01-intro/
    │   └── index.html      ← presentazione lezione 1
    ├── 02-.../
    │   └── index.html      ← presentazione lezione 2 (da creare)
    ├── syllabus.md
    └── Intro_Completo.md
```

---

## Come usare le presentazioni

1. Apri `index.html` nel browser (doppio click sul file)
2. Clicca sulla lezione che vuoi mostrare
3. La presentazione si apre a schermo intero

### Navigazione durante la lezione

| Tasto | Azione |
|-------|--------|
| `→` / `Spazio` | Slide successiva |
| `←` | Slide precedente |
| `↓` | Slide verticale successiva (sotto-sezione) |
| `F` | Fullscreen |
| `ESC` | Panoramica di tutte le slide |
| `S` | Apri il pannello speaker notes |
| `B` | Schermo nero (pausa) |

> **Tip fullscreen:** premi `F` all'inizio della lezione, poi `ESC` per uscire dal fullscreen a fine lezione.

---

## Come aggiungere una nuova lezione

### 1. Copia la cartella di una lezione esistente

```
lessons/01-intro/  →  copia e rinomina in  lessons/02-sintassi/
```

Il file `index.html` al suo interno è già collegato a `../../shared/styles.css` — non serve cambiare nulla nei path.

### 2. Modifica il titolo della pagina

Nel nuovo `lessons/02-sintassi/index.html`, cambia il tag `<title>`:

```html
<title>C# - Sintassi Base</title>
```

### 3. Sostituisci le slide

Il contenuto delle slide si trova dentro:

```html
<div class="reveal">
  <div class="slides">
    <!-- ← qui ci sono tutte le sezioni -->
  </div>
</div>
```

Ogni capitolo è un blocco `<section>` che contiene le sue slide come `<section>` figlie:

```html
<!-- CAPITOLO -->
<section>

  <!-- Slide di apertura capitolo -->
  <section class="section-divider" data-state="is-section-divider">
    ...
  </section>

  <!-- Slide 1 del capitolo -->
  <section id="mia-slide">
    ...
  </section>

  <!-- Slide 2 del capitolo -->
  <section id="mia-slide-2">
    ...
  </section>

</section>
```

### 4. Aggiungi la lezione alla homepage

In `index.html` (root), trova la card "coming soon" corrispondente e trasformala in un link attivo.

**Prima (coming soon):**
```html
<div class="card disabled">
  <div class="card-top">
    <div class="card-icon inactive"><i class="fa-solid fa-code"></i></div>
    <span class="card-num inactive">02</span>
  </div>
  <div>
    <div class="card-title inactive">Sintassi Base</div>
    <div class="card-desc inactive">Descrizione...</div>
  </div>
  <div class="card-cta inactive">
    <i class="fa-solid fa-lock" style="font-size:0.6rem"></i>
    <span>In arrivo</span>
  </div>
</div>
```

**Dopo (attiva):**
```html
<a href="lessons/02-sintassi/index.html" class="card">
  <div class="card-top">
    <div class="card-icon active"><i class="fa-solid fa-code"></i></div>
    <span class="card-num active">02</span>
  </div>
  <div>
    <div class="card-title active">Sintassi Base</div>
    <div class="card-desc active">Descrizione...</div>
  </div>
  <div class="card-cta active">
    <span>Apri lezione</span>
    <i class="fa-solid fa-arrow-right" style="font-size:0.6rem"></i>
  </div>
</a>
```

Le differenze rispetto alla card disabilitata:
- `<div class="card disabled">` → `<a href="..." class="card">`
- tutte le classi `inactive` → `active`
- la CTA cambia da `fa-lock / In arrivo` a `fa-arrow-right / Apri lezione`

---

## Come creare nuove slide

Consulta `shared/DESIGN_SYSTEM.md` per la documentazione completa dei componenti visivi.

I pattern più usati sono:

### Slide di apertura capitolo
```html
<section class="section-divider" data-state="is-section-divider">
  <div class="flex flex-col items-center justify-center gap-8 text-center">
    <div class="flex items-center gap-3">
      <span class="block w-10 h-px bg-aulab-yellow/40"></span>
      <span class="text-xs font-bold uppercase tracking-[0.3em] text-aulab-yellow/60">Capitolo 02</span>
      <span class="block w-10 h-px bg-aulab-yellow/40"></span>
    </div>
    <div class="p-5 rounded-2xl bg-white/[0.04] border border-white/10">
      <i class="fa-solid fa-code text-7xl text-aulab-yellow"></i>
    </div>
    <div>
      <h1 class="text-[6.5rem] font-black tracking-[-0.04em] text-white leading-[0.88] uppercase">Sintassi</h1>
      <h1 class="text-[6.5rem] font-black tracking-[-0.04em] text-gradient leading-[0.88] uppercase">&amp; Tipi</h1>
    </div>
    <div class="w-16 h-px bg-white/10"></div>
    <p class="text-base font-semibold uppercase tracking-[0.22em] text-gray-500">Sottotitolo del capitolo</p>
  </div>
</section>
```

### Slide con card (layout più comune)
```html
<section id="mia-slide">
  <div class="flex flex-col h-full">

    <!-- Label in alto -->
    <div class="slide-header flex items-center gap-3 border-b border-white/5 pb-5">
      <span class="text-[0.65rem] font-bold uppercase tracking-[0.25em] text-aulab-yellow/60">02.01 &mdash; Label</span>
    </div>

    <!-- Contenuto centrato -->
    <div class="flex-1 flex items-center">
      <div class="grid grid-cols-12 gap-5 w-full">

        <!-- Card larga (12 colonne = full width) -->
        <div class="col-span-12 glass-card">
          <h3>Titolo</h3>
          <p>Contenuto...</p>
        </div>

        <!-- Due card affiancate (6+6 colonne) -->
        <div class="col-span-6 glass-card">...</div>
        <div class="col-span-6 glass-card">...</div>

      </div>
    </div>

  </div>
</section>
```

### Testo con keyword evidenziata
```html
<p>Il testo normale con <strong class="text-white font-bold">parola chiave</strong> evidenziata.</p>
```

### Lista con bullet
```html
<ul class="space-y-4">
  <li class="flex items-center gap-3 text-sm text-gray-400">
    <span class="w-1.5 h-1.5 rounded-full bg-aulab-yellow shrink-0"></span>
    <span>Elemento della lista</span>
  </li>
</ul>
```

### Icone disponibili

Le icone vengono da **Font Awesome 6** (free). Cerca l'icona su [fontawesome.com/icons](https://fontawesome.com/icons) e usa la classe `fa-solid fa-nome-icona`.

---

## Note tecniche

- Le presentazioni richiedono una connessione internet per caricare Reveal.js, Font Awesome e i font Google (tutti da CDN)
- Non è necessario installare nulla — tutto funziona aprendo i file HTML direttamente nel browser
- Testato su Chrome e Firefox

---

## Stack

| Libreria | Versione | Uso |
|----------|----------|-----|
| Reveal.js | 5.1.0 | Engine per le presentazioni |
| Tailwind CSS | v4 (browser CDN) | Utility CSS nelle slide |
| Font Awesome | 6.5.1 | Icone |
| Montserrat | — | Font principale |
| Chart.js | latest | Grafici (se necessari) |
