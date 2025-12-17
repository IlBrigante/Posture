# 🎨 DESIGN SYSTEM - Posture Studio Pilates

Guida completa al sistema di design del sito.

---

## 🎨 PALETTE COLORI
```css
:root {
    /* Colori Principali */
    --primary: #D8B284;      /* Beige dorato - CTA, accenti */
    --secondary: #B89968;    /* Marrone caldo - testi evidenziati */
    --text: #2C2C2C;        /* Grigio scuro - corpo testo */
    --accent: #7D9D7C;      /* Verde salvia - elementi decorativi */
    --bg-light: #F8F5F0;    /* Crema - sfondi alternati */
    --white: #FFFFFF;       /* Bianco puro - sfondi principali */
    --gray: #7A7A7A;        /* Grigio medio - testi secondari */
}
```

### Utilizzo Colori

| Colore | Dove Usare | Esempio |
|--------|------------|---------|
| **Primary** | Bottoni, link, hover | CTA "Prenota ora" |
| **Secondary** | Strong, evidenziazioni | Parole chiave nei testi |
| **Text** | Corpo testo, paragrafi | 90% del testo |
| **Accent** | Decorazioni, badge | "Apertura 8 Settembre" |
| **BG Light** | Sfondi sezioni alternate | Sezione "Metodo" |
| **Gray** | Info secondarie, caption | "Risposta entro 1 ora" |

---

## ✍️ TIPOGRAFIA

### Font Families
```css
/* Titoli */
font-family: 'Montserrat', sans-serif;
font-weight: 300; /* Extra Light */

/* Corpo Testo */
font-family: 'Open Sans', sans-serif;
font-weight: 400; /* Regular */

/* Strong/Bold */
font-family: 'Open Sans', sans-serif;
font-weight: 600; /* Semi Bold */
```

### Scala Tipografica
```css
/* H1 - Titoli Pagina */
font-size: 52px;      /* Desktop */
font-size: 32px;      /* Mobile */
font-weight: 300;
line-height: 1.2;
letter-spacing: 0.02em;

/* H2 - Titoli Sezione */
font-size: 42px;      /* Desktop */
font-size: 28px;      /* Mobile */
font-weight: 300;
line-height: 1.3;

/* H3 - Sottotitoli */
font-size: 24px;      /* Desktop */
font-size: 20px;      /* Mobile */
font-weight: 400;
line-height: 1.4;

/* Body - Paragrafi */
font-size: 16-18px;   /* Desktop */
font-size: 14-16px;   /* Mobile */
line-height: 1.8;
opacity: 0.85;

/* Label - Pretitoli */
font-size: 11-14px;
font-weight: 400-600;
text-transform: uppercase;
letter-spacing: 0.2em;
color: var(--secondary);
```

---

## 📏 SPACING SYSTEM

### Padding Sezioni
```css
/* Desktop */
padding: 100-140px 80px;

/* Tablet */
padding: 80-100px 60px;

/* Mobile */
padding: 60-80px 30px;
```

### Gap tra Elementi
```css
--space-xs: 8px;      /* Margini minimi */
--space-sm: 16px;     /* Tra elementi correlati */
--space-md: 24px;     /* Tra paragrafi */
--space-lg: 32px;     /* Tra blocchi */
--space-xl: 48px;     /* Tra sezioni interne */
--space-xxl: 64px;    /* Tra macro-sezioni */
```

---

## 🎭 COMPONENTI

### Pretitolo (Label)
```css
.section-label {
    font-family: 'Montserrat', sans-serif;
    font-size: 11-14px;
    font-weight: 400-600;
    text-transform: uppercase;
    letter-spacing: 0.2em;
    color: var(--secondary);
    margin-bottom: 40px;
}
```

**Esempi:**
- "IL NOSTRO APPROCCIO"
- "ESPERIENZA ESCLUSIVA"
- "IL TUO PERCORSO"

---

### Titoli Grandi
```css
.elegant-title {
    font-family: 'Montserrat', sans-serif;
    font-size: clamp(32px, 5vw, 52px);
    font-weight: 300;
    line-height: 1.1;
    color: var(--text);
    margin-bottom: 40px;
}
```

**Esempi:**
- "Scienza del<br>movimento"
- "Il tuo equilibrio<br>inizia qui"

---

### Link con Linea
```css
.link-with-line {
    font-size: 14px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.15em;
    color: var(--secondary);
    display: inline-flex;
    align-items: center;
    gap: 20px;
}

.link-with-line::after {
    content: '';
    width: 30px;
    height: 1px;
    background: var(--secondary);
    transition: width 0.5s ease;
}

.link-with-line:hover::after {
    width: 50px;
}
```

---

### Bottoni

#### Primario
```css
.btn-primary {
    padding: 14-18px 35-45px;
    background: var(--primary);
    color: white;
    border-radius: 30px;
    font-size: 14-16px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    transition: all 0.5s ease;
}

.btn-primary:hover {
    background: var(--secondary);
    transform: translateY(-3px);
}
```

#### Secondario
```css
.btn-secondary {
    padding: 14-18px 35-45px;
    background: transparent;
    color: var(--primary);
    border: 1-2px solid var(--primary);
    border-radius: 30px;
    /* resto uguale a primario */
}

.btn-secondary:hover {
    background: rgba(216, 178, 132, 0.08);
    border-color: var(--secondary);
}
```

---

### Card
```css
.card {
    background: white;
    padding: 30-40px;
    border-radius: 8-12px;
    border: 1px solid rgba(216, 178, 132, 0.1);
    transition: all 0.5s ease;
}

.card:hover {
    transform: translateY(-5px);
    border-color: var(--primary);
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
}
```

---

### Icone Circolari
```css
.icon-circle {
    width: 70-90px;
    height: 70-90px;
    border-radius: 50%;
    background: rgba(125, 157, 124, 0.15);
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
}

.icon-circle:hover {
    background: rgba(125, 157, 124, 0.25);
    transform: scale(1.05);
}
```

---

## 🎬 ANIMAZIONI

### Transizioni Standard
```css
/* Veloce */
transition: all 0.3s ease;

/* Standard */
transition: all 0.5s ease;

/* Lenta/Delicata */
transition: all 0.7s ease;
```

### Easing Functions
```css
--ease-smooth: cubic-bezier(0.25, 0.1, 0.25, 1);
--ease-out-smooth: cubic-bezier(0, 0, 0.2, 1);
--ease-in-smooth: cubic-bezier(0.4, 0, 1, 1);
```

### Hover Effects Comuni

#### Lift (sollevamento)
```css
.hover-lift:hover {
    transform: translateY(-5px);
}
```

#### Scale (ingrandimento)
```css
.hover-scale:hover {
    transform: scale(1.05);
}
```

#### Color Change
```css
element:hover {
    color: var(--primary);
}
```

---

## 📐 LAYOUT PATTERNS

### Sezione Standard
```html
<section class="section-spacing bg-white">
    <div class="container">
        <p class="section-label">PRETITOLO</p>
        <h2 class="elegant-title">Titolo<br>Spezzato</h2>
        <p class="elegant-text">Testo intro...</p>
        
        <!-- Contenuto -->
        
        <a href="#" class="link-with-line">SCOPRI DI PIÙ</a>
    </div>
</section>
```

### Alternanza Sfondi
```
Bianco → Crema (bg-light) → Bianco → Crema → ...
```

---

## 🎯 ELEMENTI DECORATIVI

### Rettangoli/Cerchi Sfondo
```css
.decorative-shape {
    position: absolute;
    width: 200-350px;
    height: 200-350px;
    background: linear-gradient(135deg, var(--primary) 0%, transparent 70%);
    opacity: 0.08-0.15;  /* SEMPRE bassa */
    border-radius: 0-50%;
    z-index: 0;
}
```

**Regole:**
- Max 2 per sezione
- Opacità sempre < 0.15
- Posizionamento asimmetrico
- Non devono disturbare la lettura

---

## 📱 RESPONSIVE BREAKPOINTS
```css
/* Mobile */
@media (max-width: 767px) {
    /* Smartphone */
}

/* Tablet */
@media (min-width: 768px) and (max-width: 1024px) {
    /* iPad e simili */
}

/* Desktop */
@media (min-width: 1025px) {
    /* PC */
}

/* Large Desktop */
@media (min-width: 1200px) {
    /* Monitor grandi */
}
```

### Regole Responsive
- **Mobile First**: parti da mobile, aggiungi per desktop
- **Touch Target**: min 44x44px per elementi cliccabili mobile
- **Font Size**: usa `clamp()` per scaling fluido
- **Padding**: riduci del 40-50% su mobile

---

## ✅ CHECKLIST QUALITÀ

Quando crei un nuovo componente:

- [ ] Font corretti (Montserrat titoli, Open Sans body)
- [ ] Colori dalla palette (no hardcoded)
- [ ] Transizioni smooth (0.5s standard)
- [ ] Hover states definiti
- [ ] Responsive su 3 breakpoint
- [ ] Spacing coerente con sistema
- [ ] Opacity text 0.8-0.85
- [ ] Border radius 8-12px per card
- [ ] Max 2 elementi decorativi per sezione

---

## 🚫 DA EVITARE

❌ **Font diversi** da Montserrat/Open Sans  
❌ **Colori inventati** fuori dalla palette  
❌ **Transizioni < 0.3s** (troppo brusche)  
❌ **Opacity decorazioni > 0.2** (troppo visibili)  
❌ **Padding fissi** senza responsive  
❌ **Bold weight 700+** (usa 600 max)  
❌ **Troppi elementi decorativi** (max 2)  
❌ **Box shadow troppo marcate**  

---

**✨ Usa sempre questo documento quando crei nuovi componenti!**
