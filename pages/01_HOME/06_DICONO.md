# 06_DICONO - Homepage

## Descrizione

Sezione in colonna con 3 widget: pretitolo (testo), titolo (heading), griglia testimonianze tramite widget HTML (HTML + CSS minimal con hover).

---

## Widget Elementor Nativi

### Pretitolo (Widget Testo)

le loro storie

### Titolo (Widget Titolo)

Dicono di noi

---

## Widget HTML - Testimonianze

### HTML

```html
<!-- WIDGET HTML ELEMENTOR - Testimonianze -->
<div class="testimonials-minimal-grid">
    <!-- Testimonianza 1 - Paola -->
    <div class="testimonial-minimal">
        <div class="testimonial-stars">⭐⭐⭐⭐⭐</div>
        <p class="testimonial-text">
            "Ho 81 anni e ho iniziato pilates con Marcello da pochissimo, sono tanto entusiasta!
            L'ambiente è bellissimo e molto pulito. Il mio obiettivo per il 2025 è ringiovanire di 1 anno!"
        </p>
        <div class="testimonial-author">Paola</div>
        <div class="testimonial-role">81 anni - La nostra guerriera</div>
    </div>

    <!-- Testimonianza 2 - Elvira -->
    <div class="testimonial-minimal">
        <div class="testimonial-stars">⭐⭐⭐⭐⭐</div>
        <p class="testimonial-text">
            "Nel 2009 mi hanno diagnosticato la fibromialgia. Ho provato tante cose senza risultato.
            Qui finalmente posso dire di sentirmi molto meglio e la notte dormo."
        </p>
        <div class="testimonial-author">Elvira Vacchiano</div>
        <div class="testimonial-role">Combatte la fibromialgia</div>
    </div>

    <!-- Testimonianza 3 - Nicole -->
    <div class="testimonial-minimal">
        <div class="testimonial-stars">⭐⭐⭐⭐⭐</div>
        <p class="testimonial-text">
            "Mi sono rivolta allo studio per mantenermi in movimento durante gravidanza e post parto.
            Marcello è professionale, divertente e ti trasmette la passione."
        </p>
        <div class="testimonial-author">Nicole Cavalieri</div>
        <div class="testimonial-role">Mamma in forma</div>
    </div>

    <!-- Testimonianza 4 - Sara -->
    <div class="testimonial-minimal">
        <div class="testimonial-stars">⭐⭐⭐⭐⭐</div>
        <p class="testimonial-text">
            "Da subito ho sentito quanto questa disciplina potesse farmi bene.
            Ogni lezione è un'occasione per ritrovare l'equilibrio."
        </p>
        <div class="testimonial-author">Sara Rubagotti</div>
        <div class="testimonial-role">2 mesi di trasformazione</div>
    </div>

    <!-- Testimonianza 5 - Elena -->
    <div class="testimonial-minimal">
        <div class="testimonial-stars">⭐⭐⭐⭐⭐</div>
        <p class="testimonial-text">
            "Ho cominciato per un problema di rigidità alla spalla.
            Essere max 4 persone consente di essere seguiti perfettamente."
        </p>
        <div class="testimonial-author">Elena Lombardo</div>
        <div class="testimonial-role">Spalla libera</div>
    </div>

    <!-- Testimonianza 6 - Chiara -->
    <div class="testimonial-minimal">
        <div class="testimonial-stars">⭐⭐⭐⭐⭐</div>
        <p class="testimonial-text">
            "L'ambiente è perfetto. Marcello è riuscito a farmi amare questa disciplina.
            Mi sono sentita a mio agio fin da subito!"
        </p>
        <div class="testimonial-author">Chiara Penati</div>
        <div class="testimonial-role">Come a casa</div>
    </div>
</div>
```

### CSS

```css
/* ============================================
   06_DICONO - TESTIMONIANZE (CSS MINIMAL)
   ============================================ */

/* Container principale (widget HTML) */
selector {
    background: #FFFFFF;
    position: relative;
}

/* Griglia testimonianze */
selector .testimonials-minimal-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 40px;
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Card testimonianza */
selector .testimonial-minimal {
    background: #FAFAFA;
    border-radius: 12px;
    padding: 35px;
    border: 1px solid #F0F0F0;
    transition: all 0.3s ease;
}

selector .testimonial-minimal:hover {
    transform: translateY(-5px);
    border-color: #E8D2B4;
    background: #FEFEFE;
}

/* Stelle */
selector .testimonial-stars {
    color: #D8B284;
    font-size: 16px;
    margin-bottom: 20px;
    letter-spacing: 2px;
}

/* Testo */
selector .testimonial-text {
    font-family: 'Open Sans', sans-serif;
    font-weight: 400;
    font-size: 15px;
    line-height: 1.75em;
    color: #2C2C2C;
    margin-bottom: 25px;
    font-style: italic;
    opacity: 0.85;
}

/* Autore */
selector .testimonial-author {
    font-family: 'Open Sans', sans-serif;
    font-weight: 600;
    color: #B89968;
    font-size: 16px;
    margin-bottom: 5px;
}

/* Ruolo */
selector .testimonial-role {
    font-family: 'Open Sans', sans-serif;
    font-size: 13px;
    color: #999;
    font-weight: 400;
    letter-spacing: 0.5px;
}

/* RESPONSIVE TABLET */
@media (max-width: 1024px) and (min-width: 768px) {
    selector .testimonials-minimal-grid {
        grid-template-columns: repeat(2, 1fr);
        gap: 30px;
    }

    selector .testimonial-minimal {
        padding: 30px;
    }
}

/* RESPONSIVE MOBILE */
@media (max-width: 767px) {
    selector .testimonials-minimal-grid {
        grid-template-columns: 1fr;
        gap: 25px;
        padding: 0 15px;
    }

    selector .testimonial-minimal {
        padding: 25px;
    }

    selector .testimonial-minimal:hover {
        transform: none;
    }

    selector .testimonial-text {
        font-size: 14px;
        line-height: 1.7em;
    }
}
```

---

## Impostazioni Elementor

### Struttura widget (ordine verticale)

1. Widget Testo (pretitolo)
2. Widget Titolo (titolo)
3. Widget HTML (testimonianze)

### Sezione (consigliato)

* Padding: 120px top/bottom, 80px left/right
* Background: Bianco (#FFFFFF)

---

## Note implementazione

### Step 1

1. Aggiungi sezione (1 colonna)
2. Inserisci i 3 widget in ordine

### Step 2 - Widget HTML

1. Incolla l’HTML nel Widget HTML
2. Tab Avanzato → CSS Personalizzato → Incolla il CSS

---

## Responsive

* Desktop: griglia auto-fit (fino a 3 colonne in base allo spazio)
* Tablet: 2 colonne
* Mobile: 1 colonna
