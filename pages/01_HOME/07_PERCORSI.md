# 07_PERCORSI - Homepage

## Descrizione

Sezione in verticale con 4 widget: pretitolo (editor testo), titolo (heading), testo introduttivo (editor testo), blocco prezzi tramite widget HTML (HTML + CSS).

---

## Widget Elementor Nativi

### Pretitolo (Widget Editor di Testo)

i nostri percorsi

### Titolo (Widget Titolo)

Investi nel tuo benessere

### Testo (Widget Editor di Testo)

Prezzi <strong>trasparenti</strong>, risultati <strong>concreti</strong>.<br>
Ogni percorso inizia con una valutazione <strong>personalizzata</strong>.

---

## Widget HTML - Prezzi Percorsi

### HTML

```html
<!-- WIDGET HTML ELEMENTOR - Prezzi Percorsi -->
<div class="pricing-minimal-grid">
    <!-- Card 1: Valutazione Iniziale -->
    <div class="price-card-minimal">
        <div class="price-badge">PRIMO PASSO</div>
        <h3 class="price-title">Valutazione Iniziale</h3>
        <div class="price-duration">50 minuti • Obbligatoria</div>
        <div class="price-amount">
            <span class="currency">€</span>
            <span class="number">45</span>
        </div>
        <div class="price-period">Una tantum</div>
        <div class="price-divider"></div>
        <ul class="price-features">
            <li>Analisi posturale completa</li>
            <li>Valutazione referti medici</li>
            <li>Definizione obiettivi</li>
            <li>Programma su misura</li>
        </ul>
        <a href="https://wa.me/393513618222?text=Ciao%20Marcello,%20vorrei%20informazioni%20sulla%20valutazione%20iniziale."
           class="price-cta"
           target="_blank">
            Prenota ora
        </a>
    </div>

    <!-- Card 2: Duetto -->
    <div class="price-card-minimal">
        <div class="price-badge">IN DUE È MEGLIO</div>
        <h3 class="price-title">Duetto</h3>
        <div class="price-duration">50 minuti • Solo 2 persone</div>
        <div class="price-amount">
            <span class="currency">€</span>
            <span class="number">170/285</span>
        </div>
        <div class="price-period">Pacchetti 5 o 10 lezioni</div>
        <div class="price-divider"></div>
        <ul class="price-features">
            <li>Condividi con chi vuoi</li>
            <li>Attenzione personalizzata</li>
            <li>Ambiente intimo e protetto</li>
            <li>Motivazione reciproca</li>
            <li>Costo condiviso</li>
        </ul>
        <a href="https://wa.me/393513618222?text=Ciao%20Marcello,%20vorrei%20informazioni%20sul%20duetto."
           class="price-cta"
           target="_blank">
            Inizia in due
        </a>
    </div>

    <!-- Card 3: Mini Classe (featured) -->
    <div class="price-card-minimal featured">
        <div class="price-badge">PIÙ SCELTO</div>
        <h3 class="price-title">Mini Classe</h3>
        <div class="price-duration">50 minuti • Max 4 persone</div>
        <div class="price-amount">
            <span class="currency">€</span>
            <span class="number">100/170</span>
        </div>
        <div class="price-period">Pacchetti 5 o 10 lezioni</div>
        <div class="price-divider"></div>
        <ul class="price-features">
            <li>Massimo 4 partecipanti</li>
            <li>Programma personalizzato</li>
            <li>Dinamica di gruppo</li>
            <li>12 settimane per 10 lezioni</li>
            <li>Flessibilità oraria</li>
        </ul>
        <a href="/servizi#scopri" class="price-cta featured">Scopri di più</a>
    </div>

    <!-- Card 4: Lezioni Individuali -->
    <div class="price-card-minimal">
        <div class="price-badge">ESCLUSIVO</div>
        <h3 class="price-title">Individuale</h3>
        <div class="price-duration">50 minuti • One-to-one</div>
        <div class="price-amount">
            <span class="currency">€</span>
            <span class="number">200/345</span>
        </div>
        <div class="price-period">Pacchetti 5 o 10 lezioni</div>
        <div class="price-divider"></div>
        <ul class="price-features">
            <li>Attenzione totale</li>
            <li>Massima personalizzazione</li>
            <li>Progressi più rapidi</li>
            <li>Orari flessibili</li>
        </ul>
        <a href="https://wa.me/393513618222?text=Ciao%20Marcello,%20vorrei%20informazioni%20sulle%20lezioni%20individuali."
           class="price-cta"
           target="_blank">
            Inizia ora
        </a>
    </div>
</div>

<!-- Info importante sotto i prezzi -->
<div class="pricing-info-box">
    <h4>💡 Informazioni importanti</h4>
    <p><strong>Disdette:</strong> minimo 24 ore di preavviso per recuperare la lezione</p>
    <p><strong>Validità:</strong> pacchetto 10 lezioni valido 12 settimane (2 bonus per recuperi)</p>
    <p><strong>Pagamento:</strong> in sede o bonifico bancario</p>
</div>
```

### CSS

```css
/* ============================================
   07_PERCORSI - SEZIONE PREZZI (4 COLONNE)
   ============================================ */

/* Container principale (widget HTML) */
selector {
    background: linear-gradient(180deg, #F8F5F0 0%, #FEFEFE 100%);
}

/* Griglia prezzi */
selector .pricing-minimal-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 30px;
    max-width: 1300px;
    margin: 0 auto 60px;
}

/* Card prezzo base */
selector .price-card-minimal {
    background: white;
    border: 1px solid #E8E8E8;
    border-radius: 16px;
    padding: 35px 30px;
    text-align: center;
    position: relative;
    transition: all 0.3s ease;
}

selector .price-card-minimal:hover {
    transform: translateY(-8px);
    border-color: #D8B284;
}

/* Card featured - Mini Classe */
selector .price-card-minimal.featured {
    border: 2px solid #7D9D7C;
    transform: scale(1.08);
}

selector .price-card-minimal.featured:hover {
    transform: scale(1.08) translateY(-8px);
    border-color: #7D9D7C;
}

/* Badge */
selector .price-badge {
    font-family: 'Montserrat', sans-serif;
    font-size: 11px;
    font-weight: 400;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: #B89968;
    margin-bottom: 20px;
}

selector .featured .price-badge {
    color: #7D9D7C;
    font-weight: 600;
}

/* Titolo servizio */
selector .price-title {
    font-family: 'Montserrat', sans-serif;
    font-size: 22px;
    font-weight: 300;
    color: #2C2C2C;
    margin-bottom: 10px;
}

/* Durata */
selector .price-duration {
    font-family: 'Open Sans', sans-serif;
    font-size: 13px;
    color: #999;
    margin-bottom: 25px;
    font-weight: 400;
}

/* Prezzo */
selector .price-amount {
    margin-bottom: 10px;
}

selector .price-amount .currency {
    font-size: 18px;
    color: #D8B284;
    vertical-align: top;
}

selector .price-amount .number {
    font-family: 'Montserrat', sans-serif;
    font-size: 38px;
    font-weight: 300;
    color: #D8B284;
}

/* Periodo */
selector .price-period {
    font-size: 13px;
    color: #999;
    margin-bottom: 25px;
    font-weight: 400;
}

/* Divider */
selector .price-divider {
    width: 35px;
    height: 1px;
    background: #E8D2B4;
    margin: 0 auto 25px;
}

/* Features list */
selector .price-features {
    list-style: none;
    padding: 0;
    margin: 0 0 30px 0;
    text-align: left;
}

selector .price-features li {
    font-family: 'Open Sans', sans-serif;
    font-size: 13px;
    color: #666;
    padding: 7px 0;
    padding-left: 22px;
    position: relative;
    line-height: 1.5;
}

selector .price-features li:before {
    content: "✓";
    position: absolute;
    left: 0;
    color: #7D9D7C;
    font-weight: 600;
}

/* CTA Button */
selector .price-cta {
    display: inline-block;
    padding: 12px 30px;
    background: transparent;
    border: 2px solid #D8B284;
    border-radius: 30px;
    color: #D8B284;
    font-family: 'Open Sans', sans-serif;
    font-size: 13px;
    font-weight: 600;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    transition: all 0.3s ease;
}

selector .price-cta:hover {
    background: #D8B284;
    color: white;
}

selector .price-cta.featured {
    background: #7D9D7C;
    border-color: #7D9D7C;
    color: white;
}

selector .price-cta.featured:hover {
    background: #6a856a;
    border-color: #6a856a;
}

/* Info box */
selector .pricing-info-box {
    max-width: 700px;
    margin: 60px auto 0;
    background: white;
    border-radius: 12px;
    padding: 30px;
    text-align: center;
    border: 1px solid #F0F0F0;
}

selector .pricing-info-box h4 {
    font-family: 'Montserrat', sans-serif;
    font-size: 20px;
    color: #B89968;
    margin-bottom: 20px;
}

selector .pricing-info-box p {
    font-family: 'Open Sans', sans-serif;
    font-size: 18px;
    color: #666;
    margin-bottom: 10px;
    line-height: 1.6;
}

/* RESPONSIVE TABLET - 2 colonne */
@media (max-width: 1024px) and (min-width: 768px) {
    selector .pricing-minimal-grid {
        grid-template-columns: repeat(2, 1fr);
        gap: 25px;
        max-width: 700px;
    }

    selector .price-card-minimal.featured {
        transform: scale(1.05);
    }
}

/* RESPONSIVE MOBILE - 1 colonna */
@media (max-width: 767px) {
    selector .pricing-minimal-grid {
        grid-template-columns: 1fr;
        gap: 25px;
        margin-bottom: 40px;
    }

    selector .price-card-minimal {
        padding: 30px 25px;
    }

    selector .price-card-minimal.featured {
        transform: scale(1);
    }

    selector .price-card-minimal:hover {
        transform: none;
    }

    selector .price-amount .number {
        font-size: 34px;
    }

    selector .pricing-info-box {
        padding: 25px 20px;
    }
}
```

---

## Impostazioni Elementor

### Struttura widget (ordine verticale)

1. Widget Editor di Testo (pretitolo)
2. Widget Titolo (titolo)
3. Widget Editor di Testo (testo)
4. Widget HTML (prezzi + info box)

### Sezione (consigliato)

* Padding: 120px top/bottom, 80px left/right
* Background: lasciare neutro (il gradiente è nel CSS del widget HTML)

---

## Note implementazione

### Step 1

1. Aggiungi sezione (1 colonna)
2. Inserisci i 4 widget in ordine

### Step 2 - Widget HTML

1. Incolla l’HTML nel Widget HTML
2. Tab Avanzato → CSS Personalizzato → Incolla il CSS

---

## Responsive

* Desktop: 4 colonne
* Tablet: 2 colonne
* Mobile: 1 colonna (featured non ingrandita)
