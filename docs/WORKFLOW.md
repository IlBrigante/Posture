# ⚙️ WORKFLOW - Guida Operativa

Come lavorare sul progetto: dalla modifica al deploy.

---

## 🔄 WORKFLOW STANDARD
```
1. PIANIFICA → 2. MODIFICA → 3. TEST → 4. COMMIT → 5. DEPLOY
```

---

## 1️⃣ PIANIFICAZIONE

### Prima di Iniziare
- [ ] Leggi `QUICK_START.md`
- [ ] Controlla `PROJECT_STATUS.md` per priorità
- [ ] Verifica se c'è qualcosa in corso
- [ ] Definisci obiettivo della sessione

### Documenta l'Obiettivo
Scrivi nel `CHANGELOG.md`:
```markdown
## [DATA] - In Corso
- Obiettivo: [descrizione chiara]
- Pagine coinvolte: [elenco]
- Tempo stimato: [ore]
```

---

## 2️⃣ MODIFICA

### A. Modifiche CSS Globale

**File da modificare**: `css/CSS_MASTER_v5.4.md`

**Processo:**
1. Apri il file su GitHub
2. Clicca matita (Edit)
3. Modifica il CSS
4. **Commit** con messaggio chiaro: `"CSS: Aggiornato colore hover bottoni"`
5. Vai su WordPress
6. **Aspetto > Personalizza > CSS Aggiuntivo**
7. Copia TUTTO il contenuto di CSS_MASTER
8. **Pubblica**
9. **Test in Incognito** (Chrome)

⚠️ **IMPORTANTE**: Fai BACKUP prima di modifiche grandi!

---

### B. Modifiche Widget Specifico

**File da modificare**: `pages/XX_PAGINA/YY_WIDGET.md`

**Processo:**
1. Apri il file su GitHub
2. Modifica HTML o CSS
3. **Commit** con messaggio: `"Homepage: Aggiornato testo sezione prezzi"`
4. Vai su WordPress
5. Apri pagina in **Elementor**
6. Trova il widget
7. **Tab Avanzato > CSS Personalizzato**
8. Copia il CSS dal file .md
9. Oppure modifica HTML nel widget HTML
10. **Aggiorna** pagina
11. **Test in Incognito**

---

### C. Aggiungere Nuova Sezione

**Esempio**: Nuova sezione "Video Testimonianze" in Homepage

**Step:**

1. **Crea file**: `pages/01_HOME/05_VIDEO_TESTIMONIANZE.md`
```markdown
# VIDEO TESTIMONIANZE - Homepage

## Descrizione
Sezione con video testimonianze clienti

## HTML
[codice HTML del widget]

## CSS
selector .video-testimonials {
    /* CSS specifico */
}

## Note Implementazione
- Video caricati su Vimeo
- Lazy loading attivo
- Fallback immagine se video non carica
```

2. **Commit**: `"Homepage: Aggiunta sezione Video Testimonianze"`

3. **Implementa in Elementor**:
   - Aggiungi Widget HTML
   - Copia HTML
   - Tab Avanzato > CSS: copia CSS
   - Aggiorna pagina

4. **Aggiorna PROJECT_STATUS.md**:
```markdown
### Homepage
- [x] Video Testimonianze
```

5. **Commit**: `"Docs: Aggiornato status progetto"`

---

### D. Modificare Copy/Testi

**File sorgente**: `docs/10domande.md`

**Processo:**
1. Modifica il testo in `10domande.md`
2. **Commit**: `"Copy: Aggiornata bio Marcello"`
3. Copia il nuovo testo
4. Vai in Elementor
5. Modifica il widget testo
6. **Aggiorna** pagina
7. **Sincronizza** anche il file `.md` della pagina se necessario

---

## 3️⃣ TEST

### Checklist Test Obbligatori

#### Desktop
- [ ] Chrome (ultima versione)
- [ ] Safari (se disponibile)
- [ ] Edge (se disponibile)
- [ ] Firefox (opzionale)

#### Mobile
- [ ] Chrome Mobile (emulatore)
- [ ] Safari iOS (se disponibile)
- [ ] Dispositivo reale (sempre meglio)

#### Test Funzionali
- [ ] Tutti i link funzionano
- [ ] Form contatti funziona
- [ ] Bottoni WhatsApp corretti
- [ ] Mappe caricate
- [ ] Transizioni smooth
- [ ] Nessun errore console

#### Test Responsivi
- [ ] 375px (iPhone SE)
- [ ] 768px (iPad)
- [ ] 1920px (Desktop)

---

### Come Testare Correttamente

**1. Usa SEMPRE Chrome Incognito**
```
Perché: Evita cache
Come: Ctrl+Shift+N (Windows) / Cmd+Shift+N (Mac)
```

**2. Svuota cache se necessario**
```
Chrome: Ctrl+Shift+Delete > Ultima ora > Cancella
WordPress: WP Rocket > Svuota cache (se attivo)
Elementor: Tools > Regenerate CSS
```

**3. Test Responsive**
```
Chrome DevTools: F12 > Toggle Device Toolbar (Ctrl+Shift+M)
Testa: iPhone 12 Pro, iPad Air, Desktop HD
```

**4. Test Performance**
```
PageSpeed Insights: https://pagespeed.web.dev/
Inserisci: URL della pagina
Target: >80 mobile, >90 desktop
```

---

## 4️⃣ COMMIT SU GITHUB

### Nomenclatura Commit

**Formato**: `[TIPO]: Descrizione chiara`

**Tipi:**
```
CSS: Modifiche CSS globale
HTML: Modifiche HTML widget
Copy: Modifiche testi
Fix: Correzione bug
Feature: Nuova funzionalità
Docs: Aggiornamento documentazione
Style: Formattazione codice (no funzionalità)
Refactor: Ristrutturazione codice
```

**Esempi BUONI** ✅
```
CSS: Aggiornato hover bottoni CTA
Homepage: Aggiunta sezione testimonianze video
Fix: Corretto link WhatsApp in footer
Copy: Aggiornato testo bio Marcello
Docs: Aggiornato CHANGELOG con modifiche dicembre
```

**Esempi CATTIVI** ❌
```
fix
aggiornamenti
modifiche varie
test
wip
```

---

### Processo Commit

**Su GitHub.com:**
1. Vai al file da modificare
2. Clicca matita
3. Fai modifiche
4. Scroll in basso
5. Scrivi messaggio commit chiaro
6. **Commit changes**

**Con VS Code** (quando lo userai):
1. Modifica file
2. Source Control (Ctrl+Shift+G)
3. Stage changes (+)
4. Scrivi messaggio
5. Commit (✓)
6. Sync

---

## 5️⃣ DEPLOY SU WORDPRESS

### Deploy CSS Globale
```
GitHub → css/CSS_MASTER_v5.4.md
   ↓
WordPress → Aspetto > Personalizza > CSS Aggiuntivo
   ↓
Copia tutto il contenuto
   ↓
Pubblica
   ↓
Test in Incognito
```

---

### Deploy Widget
```
GitHub → pages/XX_PAGINA/YY_WIDGET.md
   ↓
WordPress → Modifica con Elementor
   ↓
Widget HTML: copia HTML
Widget Avanzato > CSS: copia CSS
   ↓
Aggiorna
   ↓
Test in Incognito
```

---

### Deploy Footer
```
GitHub → theme/footer.php
   ↓
WordPress → Aspetto > Editor Temi
   ↓ (⚠️ ATTENZIONE: Usa Child Theme!)
Incolla codice
   ↓
Aggiorna File
   ↓
Test tutto il sito
```

---

## 🔥 WORKFLOW RAPIDO (uso quotidiano)

### Modifica Veloce CSS
```bash
1. GitHub: Apri CSS_MASTER_v5.4.md
2. Edit (matita)
3. Modifica
4. Commit: "CSS: [cosa hai fatto]"
5. WordPress: Copia in CSS Aggiuntivo
6. Test Incognito
✅ FATTO (5 minuti)
```

---

### Aggiungere Testo/Immagine
```bash
1. Elementor: Apri pagina
2. Modifica widget
3. Aggiorna
4. Test
5. GitHub: Aggiorna file .md corrispondente
6. Commit: "Copy: [cosa hai fatto]"
✅ FATTO (3 minuti)
```

---

### Creare Nuova Pagina
```bash
1. GitHub: Crea cartella pages/09_NUOVA_PAGINA/
2. Crea 01_SEZIONE.md con HTML+CSS
3. Commit
4. WordPress: Crea nuova pagina
5. Elementor: Costruisci con i widget
6. Pubblica
7. GitHub: Aggiorna PROJECT_STATUS.md
8. Commit: "Feature: Aggiunta pagina [NOME]"
✅ FATTO (30 minuti)
```

---

## 📅 ROUTINE SETTIMANALE

### Lunedì (Pianificazione)
- [ ] Review PROJECT_STATUS.md
- [ ] Definisci obiettivi settimana
- [ ] Priorità 1-2-3

### Mercoledì (Checkpoint)
- [ ] Verifica avanzamento
- [ ] Test funzionalità
- [ ] Aggiorna CHANGELOG

### Venerdì (Chiusura)
- [ ] Test completo sito
- [ ] Aggiorna tutti i docs
- [ ] Commit finale settimana
- [ ] Backup database

---

## 🚨 EMERGENZE

### Sito Rotto (Panico!)

**1. Identifica problema**
```
- Cosa non funziona?
- Da quando?
- Ultimo commit?
```

**2. Rollback veloce**
```
WordPress:
- Aspetto > Personalizza > CSS: rimuovi ultimo CSS
- Elementor > Tools > Rollback (se disponibile)

GitHub:
- History del file
- Copia versione precedente
- Commit: "Fix: Rollback per problema [X]"
```

**3. Fix e test**
```
- Correggi con calma
- Test approfondito
- Commit: "Fix: Risolto [problema]"
```

**4. Documenta**
```
TROUBLESHOOTING.md:
- Aggiungi problema
- Aggiungi soluzione
- Commit
```

---

### CSS Non Si Applica

**Checklist:**
1. Hai fatto Publish in WordPress?
2. Cache svuotata? (Incognito test)
3. Selettore CSS corretto? (ispeziona elemento)
4. Autoptimize disattivato?
5. Elementor CSS rigenerato?

---

### Modifiche Non Visibili

**Soluzione:**
```bash
1. Ctrl+Shift+Delete (svuota cache)
2. Elementor > Tools > Regenerate CSS
3. WP Rocket > Svuota cache (se presente)
4. Test Incognito
5. Se ancora non va: verifica upload corretto
```

---

## 📝 TEMPLATE COMMIT MESSAGES

Copia e personalizza:
```markdown
CSS: Aggiornato [elemento] in [sezione]
HTML: Modificato [widget] in [pagina]
Copy: Cambiato testo [elemento] da "[vecchio]" a "[nuovo]"
Fix: Corretto [bug] in [posizione]
Feature: Aggiunta [nuova funzionalità] in [pagina]
Style: Formattazione codice [file]
Docs: Aggiornato [documento] con [info]
Refactor: Ristrutturato [componente] per [motivo]
Test: Verificato [funzionalità] su [dispositivi]
Performance: Ottimizzato [elemento] per [metrica]
SEO: Aggiunto [meta tag/schema] in [pagina]
```

---

## ✅ CHECKLIST FINE SESSIONE

Prima di chiudere:

- [ ] Tutti i commit fatti
- [ ] PROJECT_STATUS.md aggiornato
- [ ] CHANGELOG.md aggiornato con data
- [ ] Test completo funzionalità modificate
- [ ] Nessun errore console
- [ ] Cache svuotata
- [ ] Screenshot modifiche (se rilevanti)

---

**🎯 Segui sempre questo workflow per consistenza!**
