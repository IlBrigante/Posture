# LA NOSTRA MISSIONE - Homepage

## Descrizione
Sezione a 2 colonne (30% / 70%): widget HTML sassi in equilibrio a sinistra, testo missionale a destra

---

## COLONNA SINISTRA - Widget HTML Sassi

### HTML
```html
<div class="stones-balance-container">
    <!-- Sasso grande in basso (base) -->
    <div class="stone stone-base"></div>
    <!-- Sasso medio al centro -->
    <div class="stone stone-middle"></div>
    <!-- Sasso piccolo in alto -->
    <div class="stone stone-top"></div>
</div>
```

### CSS
```css
/* ============================================
   SASSI IN EQUILIBRIO - STILE LOGO
   ============================================ */
selector .stones-balance-container {
    position: relative;
    height: 500px;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

/* Stile base per tutti i sassi */
selector .stone {
    position: absolute;
    transition: all 0.6s ease;
}

/* Sasso grande - BASE (il più grande, in basso) */
selector .stone-base {
    width: 200px;
    height: 120px;
    background: #7D9D7C;
    opacity: 0.25;
    bottom: 80px;
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
    transform: rotate(-3deg);
}

/* Sasso medio - CENTRO */
selector .stone-middle {
    width: 160px;
    height: 100px;
    background: #D8B284;
    opacity: 0.3;
    bottom: 190px;
    border-radius: 50% 50% 50% 50% / 55% 55% 45% 45%;
    transform: rotate(2deg);
}

/* Sasso piccolo - TOP (il più piccolo, in alto) */
selector .stone-top {
    width: 100px;
    height: 70px;
    background: #B89968;
    opacity: 0.2;
    bottom: 280px;
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
    transform: rotate(-2deg);
}

/* Hover effect delicato - oscillazione leggera */
selector .stones-balance-container:hover .stone-top {
    transform: rotate(0deg) translateY(-5px);
}

selector .stones-balance-container:hover .stone-middle {
    transform: rotate(0deg);
}

selector .stones-balance-container:hover .stone-base {
    transform: rotate(0deg);
}

/* RESPONSIVE TABLET */
@media (max-width: 1024px) {
    selector .stones-balance-container {
        height: 400px;
    }
    
    selector .stone-base {
        width: 170px;
        height: 100px;
        bottom: 60px;
    }
    
    selector .stone-middle {
        width: 130px;
        height: 85px;
        bottom: 150px;
    }
    
    selector .stone-top {
        width: 80px;
        height: 55px;
        bottom: 225px;
    }
}

/* RESPONSIVE MOBILE */
@media (max-width: 767px) {
    selector .stones-balance-container {
        height: 300px;
    }
    
    selector .stone-base {
        width: 140px;
        height: 80px;
        bottom: 40px;
    }
    
    selector .stone-middle {
        width: 110px;
        height: 70px;
        bottom: 115px;
    }
    
    selector .stone-top {
        width: 70px;
        height: 45px;
        bottom: 175px;
    }
    
    /* Disabilita hover su mobile */
    selector .stones-balance-container:hover .stone {
        transform: none;
    }
}
```

---

## COLONNA DESTRA - Widget Elementor Nativi

### Contenuti

**Pretitolo (Label):**
la nostra missione: uno spazio di benessere

**Titolo (H2):**
Posture Studio Pilates

**Testo:**
**Benessere** fisico attraverso il Pilates. Siamo specializzati nel migliorare la postura, alleviare dolori muscolari e aumentare la flessibilità. Le nostre lezioni personalizzate sono adatte a **tutti i livelli**, dai principianti agli esperti.

### Widget Usati
- Widget Intestazione (pretitolo)
- Widget Intestazione (titolo H2)
- Widget Testo (paragrafo)

---

## Impostazioni Elementor

### Sezione:
- Layout: 2 colonne (30% / 70%)
- Gap colonne: 60px
- Padding: 120px top/bottom, 80px left/right
- Background: Bianco (#FFFFFF)

### Colonna Sinistra:
- Widget HTML con codice sassi
- Allineamento verticale: Centro

### Colonna Destra:
- Widget nativi Elementor
- Allineamento verticale: Centro

---

## Note Implementazione

### Step 1 - Struttura:
1. Aggiungi Sezione con 2 colonne
2. Imposta larghezza colonne: 30% / 70%

### Step 2 - Colonna Sinistra:
1. Aggiungi Widget HTML
2. Incolla codice HTML sassi
3. Tab Avanzato → CSS Personalizzato → Incolla CSS sassi

### Step 3 - Colonna Destra:
1. Aggiungi Widget Intestazione (pretitolo)
2. Aggiungi Widget Intestazione (titolo)
3. Aggiungi Widget Testo (paragrafo)

### Step 4:
1. Aggiorna pagina
2. Test responsive

---

## Responsive
- Desktop: 30% / 70%
- Tablet: Mantiene layout
- Mobile: Colonne stack verticali (sassi sopra, testo sotto)
