# 08_INFO - Homepage

## Descrizione

Sezione con un unico widget HTML: call to action elegante per prenotare o richiedere informazioni (bottoni WhatsApp + Contatti), stile coerente con le altre sezioni.

---

## Widget HTML - CTA Prenotazione / Info

### HTML

```html
<!-- WIDGET HTML ELEMENTOR - CTA Info -->
<div class="cta-elegant-container">
    <!-- Icona decorativa con stesso stile delle altre sezioni -->
    <div class="value-icon-circle" style="margin: 0 auto 40px;">
        <svg width="40" height="40" viewBox="0 0 24 24" fill="#D8B284">
            <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8z" opacity="0.3"/>
            <circle cx="12" cy="12" r="3" fill="#D8B284" opacity="0.6"/>
            <path d="M12 7v5l3.5 2.1" stroke="#D8B284" stroke-width="1.5" fill="none" opacity="0.5"/>
        </svg>
    </div>

    <!-- Titolo principale -->
    <h2 class="cta-title-elegant">Il tuo corpo ti sta parlando</h2>

    <!-- Sottotitolo -->
    <div class="value-label" style="margin: 20px auto 40px; font-size: 14px;">È ORA DI ASCOLTARLO</div>

    <!-- Descrizione -->
    <p class="cta-description-elegant">
        Inizia oggi il tuo percorso verso l'equilibrio e il benessere
    </p>

    <!-- Bottoni -->
    <div class="cta-buttons-elegant">
        <a href="https://wa.me/393513618222?text=Ciao%20Marcello,%20vorrei%20informazioni%20sulla%20valutazione%20iniziale."
           class="btn-cta-primary"
           target="_blank">
            Inizia il tuo percorso
        </a>

        <a href="/contatti" class="btn-cta-secondary">
            Richiedi informazioni
        </a>
    </div>

    <!-- Info finale -->
    <div class="cta-info-elegant">
        <span class="cta-info-text">Risposta entro 24 ore • Valutazione personalizzata</span>
    </div>
</div>
```

### CSS

```css
/* ============================================
   08_INFO - CTA (STILE COERENTE)
   ============================================ */

/* Container principale (widget HTML) */
selector {
    background: #FFFFFF;
    position: relative;
    padding: 120px 80px;
}

/* Container centrato */
selector .cta-elegant-container {
    max-width: 700px;
    margin: 0 auto;
    text-align: center;
    transition: transform 0.3s ease;
}

selector .cta-elegant-container:hover {
    transform: translateY(-5px);
}

/* Icona con hover */
selector .value-icon-circle {
    width: 90px;
    height: 90px;
    margin: 0 auto 30px;
    background: rgba(216, 178, 132, 0.08);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
    cursor: pointer;
}

selector .value-icon-circle:hover {
    background: rgba(216, 178, 132, 0.15);
    transform: translateY(-10px) scale(1.05);
}

/* SVG interno */
selector .value-icon-circle svg {
    transition: transform 0.3s ease;
}

selector .value-icon-circle:hover svg {
    transform: scale(1.1);
}

/* Label/sottotitolo */
selector .value-label {
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    font-weight: 500;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: #D8B284;
    margin-bottom: 20px;
}

/* Titolo principale */
selector .cta-title-elegant {
    font-family: 'Montserrat', sans-serif;
    font-weight: 300;
    font-size: 55px;
    color: #494949;
    line-height: 1.3em;
    letter-spacing: 0.02em;
    margin-bottom: 15px;
}

/* Descrizione */
selector .cta-description-elegant {
    font-family: 'Open Sans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.75em;
    color: #2C2C2CC2;
    margin-bottom: 45px;
    opacity: 0.85;
}

/* Container bottoni */
selector .cta-buttons-elegant {
    display: flex;
    gap: 20px;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    margin-bottom: 50px;
}

/* Bottone primario */
selector .btn-cta-primary {
    display: inline-block;
    padding: 14px 38px;
    background: #D8B284;
    color: white;
    border-radius: 30px;
    font-family: 'Open Sans', sans-serif;
    font-size: 14px;
    font-weight: 500;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    transition: all 0.5s ease;
}

selector .btn-cta-primary:hover {
    background: #B89968;
    transform: translateY(-3px);
}

/* Bottone secondario */
selector .btn-cta-secondary {
    display: inline-block;
    padding: 14px 38px;
    background: transparent;
    color: #B89968;
    border: 1px solid #D8B284;
    border-radius: 30px;
    font-family: 'Open Sans', sans-serif;
    font-size: 14px;
    font-weight: 500;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    transition: all 0.5s ease;
}

selector .btn-cta-secondary:hover {
    background: rgba(216, 178, 132, 0.08);
    border-color: #B89968;
    transform: translateY(-3px);
}

/* Info finale */
selector .cta-info-elegant {
    text-align: center;
}

selector .cta-info-text {
    font-family: 'Open Sans', sans-serif;
    font-size: 13px;
    color: #999;
    position: relative;
    display: inline-block;
}

/* Linee decorative */
selector .cta-info-text::before,
selector .cta-info-text::after {
    content: '';
    position: absolute;
    top: 50%;
    width: 40px;
    height: 1px;
    background: #E8D2B4;
    opacity: 0.5;
}

selector .cta-info-text::before {
    left: -55px;
}

selector .cta-info-text::after {
    right: -55px;
}

/* RESPONSIVE TABLET */
@media (max-width: 1024px) and (min-width: 768px) {
    selector {
        padding: 100px 60px;
    }

    selector .cta-title-elegant {
        font-size: 36px;
    }

    selector .cta-description-elegant {
        font-size: 15px;
    }
}

/* RESPONSIVE MOBILE */
@media (max-width: 767px) {
    selector {
        padding: 80px 30px;
    }

    selector .cta-title-elegant {
        font-size: 28px;
    }

    selector .value-label {
        font-size: 12px;
    }

    selector .cta-description-elegant {
        font-size: 14px;
        margin-bottom: 35px;
    }

    selector .cta-buttons-elegant {
        flex-direction: column;
        gap: 15px;
    }

    selector .btn-cta-primary,
    selector .btn-cta-secondary {
        width: 100%;
        max-width: 260px;
    }

    selector .cta-info-text::before,
    selector .cta-info-text::after {
        display: none;
    }

    selector .btn-cta-primary:hover,
    selector .btn-cta-secondary:hover {
        transform: none;
    }
}
```

---

## Impostazioni Elementor

### Struttura widget

* 1 Widget HTML (CTA)

### Sezione (consigliato)

* Padding: lasciare neutro (gestito dal CSS del widget HTML)
* Background: neutro/bianco

---

## Note implementazione

### Step 1

1. Aggiungi sezione (1 colonna)
2. Inserisci Widget HTML

### Step 2

1. Incolla l’HTML nel Widget HTML
2. Tab Avanzato → CSS Personalizzato → Incolla il CSS

---

## Responsive

* Desktop: layout centrato con 2 bottoni affiancati
* Tablet: font ridotti, padding ridotto
* Mobile: bottoni in colonna, linee decorative disabilitate
