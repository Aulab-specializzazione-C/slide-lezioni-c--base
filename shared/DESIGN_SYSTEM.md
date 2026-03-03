# Design System — C# Aulab Slides

Stack: **Reveal.js 5.1** · **Tailwind CSS v4 (browser CDN)** · **Font Awesome 6.5** · **Montserrat**

---

## Colori

| Token | Valore | Uso |
|-------|--------|-----|
| `aulab-yellow` | `#ffed00` | Accenti primari, highlight, testo gradient |
| `aulab-cyan` | `#38bdf8` | Accenti secondari, bordi card |
| `dark-bg` | `#0B0E14` | Background globale |
| `white/[0.05]` | rgba bianco 5% | Fill glass card |
| `white/[0.12]` | rgba bianco 12% | Bordo glass card |
| `gray-400` | `#9CA3AF` | Testo body muted |
| `gray-500` | `#6B7280` | Testo molto muted, label secondari |
| `gray-600` | `#4B5563` | Footer micro-label nelle card |

### Gradient testo
```html
<span class="text-gradient">testo</span>
```
Definito in Tailwind: `bg-clip-text text-transparent bg-linear-to-r from-aulab-yellow via-aulab-cyan to-aulab-cyan font-extrabold`

---

## Note Architetturali — CSS Conflict

> ⚠️ **Reveal.js usa `* { margin: 0; padding: 0 }` non-layered.** Tailwind v4 mette le utility in `@layer utilities`. Le regole non-layered battono quelle layered indipendentemente dalla specificità. Risultato: **`p-*`, `m-*`, `mb-*`, `mt-*`, `py-*`, `px-*` di Tailwind non applicano mai.**

**Regola pratica:** margin e padding si definiscono sempre in `styles.css` con `!important`.

| Proprietà CSS | Usa Tailwind? | Note |
|---------------|---------------|------|
| `padding` | ❌ Mai | Definire in `styles.css` con `!important` |
| `margin` | ❌ Mai | Definire in `styles.css` con `!important` |
| `border-radius` | ✅ | Non resettato da Reveal |
| `gap` | ✅ | Proprietà flex/grid, non resettata |
| `background`, `color` | ✅ | Non resettati da Reveal |
| `font-size` su `<p>`, `<h4>` | ❌ | `.reveal p/h4` ha specificità più alta; override in `styles.css` |
| `h-full` su div slide | ✅ | Funziona perché `styles.css` setta `height: 100%` sulle section |

---

## Tipografia

**Font:** Montserrat (Google Fonts) — pesi usati: 300, 400, 600, 700, 800, 900

| Elemento | Classe Tailwind | Valore reale (CSS) | Contesto |
|----------|----------------|--------------------|----------|
| Titolo section divider | `text-[6.5rem] font-black tracking-[-0.04em] uppercase leading-[0.88]` | — | Solo slide capitolo |
| Eyebrow label | `text-[0.65rem] font-bold uppercase tracking-[0.25em] text-aulab-yellow/60` | — | `.slide-header` |
| Heading card h3/h4 | — | `14pt` via `.reveal .glass-card h3,h4` | Dentro `.glass-card` |
| Body card p/li | — | `12pt` via `.reveal .glass-card p,li` | Dentro `.glass-card` |

---

## Slide Capitolo (Section Divider)

Prima slide di ogni sezione. Classe `section-divider` + `data-state="is-section-divider"`.

### Alternanza Colori
Per dare ritmo alla presentazione, i colori di accento (linee eyebrow e icone) alternano tra Giallo e Cyan:
- **Capitoli Dispari (01, 03, ...)**: Usano `aulab-yellow`.
- **Capitoli Pari (02, 04, ...)**: Usano `aulab-cyan`.
- **Titoli**: Rimangono sempre gialli/gradient per coerenza di brand.

```html
<section class="section-divider" data-state="is-section-divider">
  <div class="flex flex-col items-center justify-center gap-8 text-center">

    <!-- Eyebrow con linee laterali -->
    <div class="flex items-center gap-3">
      <span class="block w-10 h-px bg-aulab-yellow/40"></span>
      <span class="text-xs font-bold uppercase tracking-[0.3em] text-aulab-yellow/60">Capitolo 01</span>
      <span class="block w-10 h-px bg-aulab-yellow/40"></span>
    </div>

    <!-- Icon container -->
    <div class="p-5 rounded-2xl bg-white/[0.04] border border-white/10 shadow-[0_0_60px_rgba(255,237,0,0.08)]">
      <i class="fa-solid fa-[icon-name] text-7xl text-aulab-yellow"></i>
    </div>

    <!-- Titolo: riga 1 bianca, riga 2 gradient -->
    <div class="space-y-0">
      <h1 class="text-[6.5rem] font-black tracking-[-0.04em] text-white leading-[0.88] uppercase">Parola Uno</h1>
      <h1 class="text-[6.5rem] font-black tracking-[-0.04em] text-gradient leading-[0.88] uppercase">&amp; Parola Due</h1>
    </div>

    <!-- Divisore -->
    <div class="w-16 h-px bg-white/10"></div>

    <!-- Sottotitolo -->
    <p class="text-base font-semibold uppercase tracking-[0.22em] text-gray-500">Descrizione breve del capitolo</p>

  </div>
</section>
```

---

## Slide Normale (pattern 01.01)

Struttura obbligatoria: `.slide-header` + wrapper centrato + grid.

```html
<section id="slide-id">
  <div class="flex flex-col h-full">

    <!-- Eyebrow header — margin-bottom 50px via .slide-header in styles.css -->
    <div class="slide-header flex items-center gap-3 border-b border-white/5 pb-5">
      <span class="text-[0.65rem] font-bold uppercase tracking-[0.25em] text-aulab-yellow/60">
        01.01 &mdash; Label
      </span>
    </div>

    <!-- Wrapper: flex-1 + items-center centra le card verticalmente -->
    <div class="flex-1 flex items-center">
      <div class="grid grid-cols-12 gap-5 w-full">
        <!-- cards -->
      </div>
    </div>

  </div>
</section>
```

> **Regola:** usare sempre il wrapper `flex-1 flex items-center` attorno al grid. Le card prendono altezza naturale e risultano centrate nello spazio disponibile.

---

## Componenti

### Glass Card

```html
<div class="glass-card">...</div>
```

Tailwind (`@theme`): `bg-white/[0.05] border border-white/[0.12] backdrop-blur-xl rounded-2xl shadow-2xl`

Padding da `styles.css` (non Tailwind):
```css
.reveal .glass-card { padding: 2.5rem 3rem !important; }
```

> **Consistenza Layout**: Per allineare più card nella stessa slide, preferire sempre un layout `flex-col` interno. Evitare di mescolare card con icone a sinistra (row) e card con icone in alto (col) nella stessa visualizzazione.

#### Varianti bordo

```html
<!-- Accent sinistro cyan -->
<div class="glass-card border-l-4 border-aulab-cyan/50">

<!-- Accent sinistro yellow -->
<div class="glass-card border-l-4 border-aulab-yellow/50">

<!-- Linea top grigia (legacy) -->
<div class="glass-card relative">
  <div class="absolute inset-x-0 top-0 h-0.5 bg-gray-700 rounded-t-2xl"></div>

<!-- Linea top cyan (attivo) -->
<div class="glass-card relative">
  <div class="absolute inset-x-0 top-0 h-0.5 bg-aulab-cyan rounded-t-2xl"></div>
```

#### Card con hover glow

```html
<div class="glass-card relative overflow-hidden group hover:border-aulab-yellow/40 transition-all duration-300">
  <div class="absolute -right-16 -top-16 w-56 h-56 bg-aulab-yellow/5 rounded-full blur-3xl
              group-hover:bg-aulab-yellow/10 transition-colors duration-500"></div>
  <div class="relative z-10">...</div>
</div>
```


### Icon Badge

```html
<!-- Taglia normale (w-9) -->
<div class="w-9 h-9 rounded-lg bg-aulab-cyan/10 flex items-center justify-center border border-aulab-cyan/20 shrink-0">
  <i class="fa-solid fa-[icon] text-aulab-cyan text-base"></i>
</div>

<!-- Taglia grande (w-11), per card feature -->
<div class="w-11 h-11 rounded-xl bg-aulab-yellow/10 flex items-center justify-center border border-aulab-yellow/20 shrink-0">
  <i class="fa-solid fa-[icon] text-aulab-yellow text-lg"></i>
</div>
```

### Bullet List

```html
<ul class="space-y-4">
  <li class="flex items-center gap-3 text-sm text-gray-400">
    <span class="w-1.5 h-1.5 rounded-full bg-aulab-yellow shrink-0"></span>
    <span>Testo. <strong class="text-white font-semibold">Keyword</strong> continua.</span>
  </li>
</ul>
```

### Card "Anno" Accent

```html
<div class="shrink-0 text-center relative z-10 w-24">
  <span class="block text-[4.5rem] font-black text-aulab-yellow/10 leading-none tracking-tighter">90s</span>
  <span class="inline-block text-[0.6rem] font-bold uppercase tracking-[0.2em] text-aulab-yellow
               border border-aulab-yellow/30 rounded bg-aulab-yellow/5">Late</span>
</div>
```

---

## Layout Patterns

### 1+2 colonne (pattern 01.01)

```html
<div class="flex-1 flex items-center">
  <div class="grid grid-cols-12 gap-5 w-full">
    <div class="col-span-12 glass-card ..."><!-- Hero card full width --></div>
    <div class="col-span-6 glass-card ..."><!-- Card sx --></div>
    <div class="col-span-6 glass-card ..."><!-- Card dx --></div>
  </div>
</div>
```

### Concept Row Cards (Vertical Stack)

Utilizzato per impilare concetti che richiedono spazio orizzontale per la descrizione (es. slide 02.01).

```html
<div class="flex-1 flex items-center">
  <div class="grid grid-cols-12 gap-5 w-full">
    <!-- Card Hero / Row -->
    <div class="col-span-12 glass-card p-10 border-l-4 border-aulab-cyan/50 relative overflow-hidden group">
      <!-- Glow background -->
      <div class="absolute -right-16 -top-16 w-56 h-56 bg-aulab-cyan/5 rounded-full blur-3xl ..."></div>
      
      <div class="relative z-10 flex flex-col gap-4">
        <!-- Header row -->
        <div class="flex items-center gap-4">
          <div class="w-11 h-11 rounded-xl bg-aulab-cyan/10 ...">
            <i class="fa-solid fa-... text-aulab-cyan text-lg"></i>
          </div>
          <h3 class="text-xl font-black uppercase tracking-tight">Titolo Concetto</h3>
        </div>
        <!-- Description row -->
        <p class="text-base text-gray-400 leading-relaxed">
          Descrizione estesa del concetto con <strong class="text-white">keyword</strong> evidenziate.
        </p>
      </div>
    </div>
  </div>
</div>
```

### 2 colonne (pattern 01.02)

```html
<div class="flex-1 flex items-center">
  <div class="grid grid-cols-2 gap-6 w-full">
    <div class="glass-card flex flex-col gap-6 ..."><!-- Feature card --></div>
    <div class="glass-card flex flex-col gap-6 ..."><!-- Feature card --></div>
  </div>
</div>
```

### Timeline orizzontale con frecce (pattern 01.03)

Tutte le card usano `glass-card`. La differenziazione avviene solo con il colore del testo del titolo.
L'altezza è fissa via `style="height: 280px"` per uniformità visiva.

```html
<div class="flex-1 flex items-center">
  <div class="flex items-stretch gap-4 w-full" style="height: 280px;">

    <!-- Fase 1 — titolo grigio chiaro -->
    <div class="flex-1 glass-card flex flex-col items-center justify-center text-center group">
      <div class="flex flex-col items-center gap-4">
        <span class="text-[0.6rem] font-bold uppercase tracking-[0.2em] text-gray-600
                     opacity-0 group-hover:opacity-100 transition-opacity">Label</span>
        <div>
          <span class="block text-4xl font-black text-gray-300 italic tracking-tighter leading-none">Titolo</span>
          <span class="block text-xl font-black text-gray-400 italic tracking-tight">Sottotitolo</span>
        </div>
        <p class="text-xs text-gray-500 leading-relaxed uppercase tracking-wider">Anno · Descrizione</p>
      </div>
    </div>

    <div class="flex items-center shrink-0 px-2">
      <i class="fa-solid fa-chevron-right text-gray-700 text-xl"></i>
    </div>

    <!-- Fase 2 — titolo cyan -->
    <div class="flex-1 glass-card flex flex-col items-center justify-center text-center">
      <div class="flex flex-col items-center gap-4">
        <span class="text-[0.6rem] font-bold uppercase tracking-[0.2em] text-gray-600">Label</span>
        <div>
          <span class="block text-4xl font-black text-aulab-cyan italic tracking-tighter leading-none">Titolo</span>
          <span class="block text-xl font-black text-aulab-cyan italic tracking-tight">Sottotitolo</span>
        </div>
        <p class="text-xs text-gray-400 leading-relaxed uppercase tracking-wider">Anno · Descrizione</p>
      </div>
    </div>

    <div class="flex items-center shrink-0 px-2">
      <i class="fa-solid fa-chevron-right text-gray-500 text-xl"></i>
    </div>

    <!-- Fase 3 — titolo yellow -->
    <div class="flex-1 glass-card flex flex-col items-center justify-center text-center">
      <div class="flex flex-col items-center gap-4">
        <span class="text-[0.6rem] font-bold uppercase tracking-[0.2em] text-gray-600">Label</span>
        <div>
          <span class="block text-4xl font-black text-aulab-yellow italic tracking-tighter leading-none">Titolo</span>
          <span class="block text-xl font-black text-aulab-yellow/70 italic tracking-tight">Sottotitolo</span>
        </div>
        <p class="text-xs text-gray-300 leading-relaxed uppercase tracking-wider">Anno · Descrizione</p>
      </div>
    </div>

  </div>
</div>
```

---

## Struttura HTML Obbligatoria

```
section[id="..."]
  div.flex.flex-col.h-full
    div.slide-header                   ← eyebrow, margin-bottom 50px via CSS
    div.flex-1.flex.items-center       ← wrapper centramento verticale
      div.grid.w-full                  ← layout (grid-cols-12 o grid-cols-2)
        div.glass-card                 ← card con padding da styles.css
```
