# 05_METODO - Homepage

## Descrizione

Sezione a 2 colonne: a sinistra widget HTML con “carte” sovrapposte + foto studio (hover movimento), a destra testo sul metodo Posture Studio.

---

## Colonna sinistra: Widget HTML (carte + foto)

### HTML

```html
<!-- WIDGET HTML ELEMENTOR - Carte Metodo + Foto Studio -->
<div class="carte-container">
    <!-- Quadrato Verde (sotto) -->
    <div class="carta carta-verde"></div>

    <!-- Quadrato Beige (sopra) -->
    <div class="carta carta-beige"></div>

    <!-- Foto Studio -->
    <div class="foto-studio">
        <img src="https://posturestudiopilates.it/wp-content/uploads/2025/08/MS5_2340-2-scaled.jpg" alt="Studio Pilates">
    </div>
</div>
```

### CSS

```css
/* ============================================
   05_METODO - CARTE SPAIATE + FOTO STUDIO
   ============================================ */

selector .carte-container {
    position: relative;
    width: 100%;
    height: 500px;
    display: flex;
    align-items: center;
    justify-content: center;
}

/* Base carte */
selector .carta {
    position: absolute;
    border-radius: 12px;
    transition: all 0.3s ease;
    pointer-events: none; /* evita che coprano l’immagine al click */
}

/* Carta verde (sotto) */
selector .carta-verde {
    width: 280px;
    height: 380px;
    background: #7D9D7C;
    opacity: 0.15;
    top: 20px;
    left: 20px;
    z-index: 1;
    transform: rotate(-5deg);
}

/* Carta beige (sopra) */
selector .carta-beige {
    width: 280px;
    height: 380px;
    background: #D8B284;
    opacity: 0.2;
    bottom: 20px;
    right: 20px;
    z-index: 2;
    transform: rotate(3deg);
}

/* Contenitore foto */
selector .foto-studio {
    position: relative;
    z-index: 3;
    width: 100%;
    max-width: 450px;
    box-shadow: 0 20px 60px rgba(0,0,0,0.1);
    border-radius: 8px;
    overflow: hidden;
}

selector .foto-studio img {
    width: 100%;
    height: auto;
    display: block;
}

/* Hover: movimento leggero */
selector .carte-container:hover .carta-verde {
    transform: rotate(-7deg) translateX(-10px);
    opacity: 0.2;
}

selector .carte-container:hover .carta-beige {
    transform: rotate(5deg) translateX(10px);
    opacity: 0.25;
}

/* RESPONSIVE TABLET / MOBILE */
@media (max-width: 768px) {
    selector .carte-container {
        height: 350px;
    }

    selector .carta-verde,
    selector .carta-beige {
        width: 200px;
        height: 280px;
    }

    selector .foto-studio {
        width: 85%;
    }
}
```

---

## Colonna destra: Widget Elementor nativi (testo)

### Contenuti

**Pretitolo (Label)**
VALUTAZIONE PERSONALE E BIOMECCANICA

**Titolo (H2)**
Il nostro metodo

**Testo**
Progettiamo il tuo percorso su misura e ti accompagniamo passo dopo passo fra resistenze intelligenti e movimenti che scolpiscono la postura.
Joseph Pilates lo chiamava "Contrology": il controllo consapevole di ogni movimento.
Nei nostri studi utilizziamo i grandi attrezzi del Pilates perché la loro ingegneria biomeccanica è insuperabile.

Ogni molla calibrata. Ogni angolo studiato.
Ogni resistenza dosata per il massimo beneficio con il minimo stress articolare.

### Widget usati

* Widget Intestazione (pretitolo)
* Widget Intestazione (titolo H2)
* Widget Testo (paragrafo)

---

## Impostazioni Elementor

### Sezione

* Layout: 2 colonne (consigliato 40% / 60%)
* Gap colonne: 60px
* Padding: 120px top/bottom, 80px left/right
* Background: Bianco (#FFFFFF)

### Colonna sinistra

* Widget HTML (carte + foto)
* Allineamento verticale: Centro

### Colonna destra

* Widget nativi Elementor (label + H2 + testo)
* Allineamento verticale: Centro

---

## Note implementazione

### Step 1: Struttura

1. Aggiungi Sezione con 2 colonne
2. Imposta larghezza colonne (es. 40% / 60%)

### Step 2: Colonna sinistra

1. Aggiungi Widget HTML
2. Incolla il codice HTML
3. Tab Avanzato → CSS Personalizzato → Incolla il CSS

### Step 3: Colonna destra

1. Aggiungi Widget Intestazione (pretitolo)
2. Aggiungi Widget Intestazione (titolo H2)
3. Aggiungi Widget Testo (paragrafo)

### Step 4

1. Aggiorna pagina
2. Test responsive

---

## Responsive

* Desktop: 2 colonne affiancate
* Tablet: mantiene 2 colonne (foto ridimensionata)
* Mobile: colonne in stack verticale (foto sopra, testo sotto)
