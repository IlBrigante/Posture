# L'ECCELLENZA È NEI DETTAGLI - Homepage

## Descrizione
Sezione con pretitolo, titolo H2 e griglia 3 colonne con widget HTML (icone circolari + testo)

---

## Contenuti

**Pretitolo (Widget Intestazione):**
esperienza esclusiva

**Titolo (Widget Intestazione H2):**
L'eccellenza è nei dettagli

---

## GRIGLIA 3 COLONNE - Widget HTML

Ogni colonna contiene 1 widget HTML con questo codice:

### COLONNA 1 - Percorso su Misura

#### HTML
```html
<div class="value-box">
    <div class="value-icon-circle">
        <svg width="40" height="40" viewBox="0 0 24 24" fill="#D8B284">
            <circle cx="12" cy="12" r="3" fill="#D8B284" opacity="0.6"/>
            <circle cx="12" cy="12" r="8" fill="none" stroke="#D8B284" stroke-width="1.5"/>
            <circle cx="12" cy="12" r="11" fill="none" stroke="#D8B284" stroke-width="1" opacity="0.3"/>
        </svg>
    </div>
    <div class="value-label">PERCORSO SU MISURA</div>
    <p class="value-description">
        Ogni corpo è unico. Per questo iniziamo sempre con una valutazione individuale approfondita per creare il TUO programma specifico.
    </p>
</div>
```

---

### COLONNA 2 - Piccoli Gruppi

#### HTML
```html
<div class="value-box">
    <div class="value-icon-circle">
        <svg width="40" height="40" viewBox="0 0 24 24" fill="#D8B284">
            <circle cx="8" cy="10" r="2" fill="#D8B284" opacity="0.6"/>
            <circle cx="16" cy="10" r="2" fill="#D8B284" opacity="0.6"/>
            <circle cx="12" cy="16" r="2" fill="#D8B284" opacity="0.6"/>
            <path d="M8 10 L16 10 L12 16 Z" fill="none" stroke="#D8B284" stroke-width="1" opacity="0.4"/>
        </svg>
    </div>
    <div class="value-label">PICCOLI GRUPPI</div>
    <p class="value-description">
        Massimo 4 persone per classe. Questo ti garantisce l'attenzione personalizzata dell'istruttore e correzioni precise durante ogni esercizio.
    </p>
</div>
```

---

### COLONNA 3 - Esperienza Certificata

#### HTML
```html
<div class="value-box">
    <div class="value-icon-circle">
        <svg width="40" height="40" viewBox="0 0 24 24" fill="#D8B284">
            <path d="M12 2 L15 9 L22 10 L17 15 L18 22 L12 18 L6 22 L7 15 L2 10 L9 9 Z" 
                  fill="#D8B284" opacity="0.6" stroke="#D8B284" stroke-width="1"/>
        </svg>
    </div>
    <div class="value-label">ESPERIENZA CERTIFICATA</div>
    <p class="value-description">
        I nostri istruttori hanno oltre 13 anni di esperienza. Formazione continua e passione per il benessere dei nostri allievi.
    </p>
</div>
```

---

## CSS COMUNE (applica a TUTTE e 3 le colonne)

**Incolla questo CSS in Tab Avanzato > CSS Personalizzato di OGNI widget HTML:**
```css
/* WIDGET: Valori / Ascolto (isolato su questa istanza) */

/* Card singola */
selector .value-box {
  text-align: center;
  padding: 30px 20px;
  transition: var(--transition);
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 20px 0;
}
selector .value-box:hover { transform: translateY(-8px); }

/* Icona circolare */
selector .value-icon-circle {
  width: 70px;
  height: 70px;
  margin: 0 auto 25px;
  background: rgba(125,157,124,0.15);
  border-radius: 50%;
  display: flex; 
  align-items: center; 
  justify-content: center;
  font-size: 28px;
  transition: var(--transition);
}
selector .value-box:hover .value-icon-circle {
  background: rgba(125,157,124,0.25);
  transform: scale(1.05);
}

/* Tipografia */
selector .value-label {
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
  font-weight: 400;
  text-transform: uppercase;
  font-style: normal;
  text-decoration: none;
  line-height: 1.75em;
  letter-spacing: 1px;
  word-spacing: 0px;
  margin-bottom: 8px;
  color: var(--secondary);
}

selector .value-description {
  font-family: 'Open Sans', sans-serif;
  font-size: 18px;
  font-weight: 400;
  line-height: 1.75em;
  color: #2C2C2CC2;
  margin: 0;
  opacity: 0.8;
  max-width: 65ch;
}

/* Responsive */
@media (min-width: 768px){
  selector .value-icon-circle { width:75px; height:75px; }
}
@media (min-width: 1025px){
  selector .value-box { padding: 40px; }
  selector .value-icon-circle { width:80px; height:80px; font-size:32px; margin-bottom:30px; }
  selector .value-description { font-size:16px; line-height:1.8; }
}
@media (max-width: 767px){
  selector .value-label { font-size:12px; }
  selector .value-description { font-size:15px; }
}
```

---

## Impostazioni Elementor

### Sezione:
- Layout: 1 colonna unica
- Larghezza contenuto: Larghezza piena o Boxed (max 1200px)
- Padding: 100px top/bottom, 80px left/right
- Background: Bianco (#FFFFFF) o Crema (#F8F5F0)

### Widget Pretitolo:
- Widget Intestazione
- Tag HTML: P o H3
- Dimensione: 14px
- Colore: #B89968 (secondary)
- Allineamento: Centro

### Widget Titolo:
- Widget Intestazione
- Tag HTML: H2
- Dimensione: 42px desktop / 28px mobile
- Colore: #2C2C2C (text)
- Allineamento: Centro
- Margine bottom: 60px

### Griglia 3 Colonne:
- Aggiungi sotto il titolo una sezione interna con 3 colonne
- Gap colonne: 60px
- Ogni colonna: Widget HTML (codice sopra)

---

## Note Implementazione

### Step 1 - Struttura Base:
1. Aggiungi Sezione → Colonna singola
2. Aggiungi Widget Intestazione (pretitolo)
3. Aggiungi Widget Intestazione (titolo H2)

### Step 2 - Griglia 3 Colonne:
1. Sotto il titolo, aggiungi Sezione Interna → 3 colonne
2. Gap tra colonne: 60px

### Step 3 - Colonna 1:
1. Aggiungi Widget HTML
2. Incolla HTML Colonna 1 (Percorso su Misura)
3. Tab Avanzato → CSS Personalizzato → Incolla CSS COMUNE

### Step 4 - Colonna 2:
1. Aggiungi Widget HTML
2. Incolla HTML Colonna 2 (Piccoli Gruppi)
3. Tab Avanzato → CSS Personalizzato → Incolla CSS COMUNE

### Step 5 - Colonna 3:
1. Aggiungi Widget HTML
2. Incolla HTML Colonna 3 (Esperienza Certificata)
3. Tab Avanzato → CSS Personalizzato → Incolla CSS COMUNE

### Step 6:
1. Aggiorna pagina
2. Test responsive (3 colonne → 1 colonna mobile)

---

## Responsive
- Desktop: 3 colonne affiancate
- Tablet: 3 colonne (o 2+1 se stretto)
- Mobile: 3 colonne impilate verticalmente
- Hover disabilitato automaticamente su touch devices

---

## ⚠️ IMPORTANTE
Il CSS è **identico** per tutte e 3 le colonne. Copialo e incollalo solo nel contenitore che contiene i widget html(uno per ogni widget HTML).
