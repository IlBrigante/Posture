# Posture Studio Pilates - WordPress + Elementor

Sito web ufficiale di Posture Studio Pilates - Studio Pilates a Rubiera e Fontana (RE)

## 🎯 Stack Tecnologico
- **CMS**: WordPress
- **Page Builder**: Elementor Pro
- **Theme**: Inspiro Pro (WPZOOM)
- **Fonts**: Montserrat (titoli) + Open Sans (corpo)

## 🎨 Design System
```css
--primary: #D8B284;      /* Beige dorato */
--secondary: #B89968;    /* Marrone caldo */
--text: #2C2C2C;        /* Grigio scuro */
--accent: #7D9D7C;      /* Verde salvia */
--bg-light: #F8F5F0;    /* Crema */
```

## 📁 Struttura Progetto
```
posture-studio-pilates/
│
├── docs/               → Documentazione e guide
├── css/                → CSS globali (CSS_MASTER)
├── theme/              → File tema personalizzati (footer.php)
├── assets/             → Immagini e screenshot
│
└── pages/              → Codice HTML/CSS per ogni pagina
    ├── 01_HOME/
    ├── 02_CHI_SIAMO/
    ├── 03_SERVIZI/
    ├── 04_CONTATTI/
    ├── 05_DOVE_SIAMO/
    ├── 06_FAQ/
    ├── 07_COOKIE_POLICY/
    └── 08_PRIVACY_POLICY/
```

## 📋 Stato Progetto

### ✅ Completato
- [x] Homepage 100%
- [x] Chi Siamo 100%
- [x] I Nostri Servizi 100%
- [x] Contatti 100%
- [x] Dove Siamo 100%
- [x] FAQ 100%
- [x] Cookie Policy 100%
- [x] Privacy Policy 100%

### 🔄 In Corso
- [ ] Nuova pagina "Lavora con Noi"
- [ ] SEO Optimization
- [ ] Performance Optimization
- [ ] Schema Markup Local Business

## 🚀 Come Usare Questo Repository

### Struttura CSS
- **CSS_MASTER** → `Aspetto > Personalizza > CSS Aggiuntivo` (WordPress)
- **Widget CSS** → `Tab Avanzato > CSS Personalizzato` (Elementor)

### Ogni file nelle cartelle PAGES contiene:
1. HTML del widget Elementor
2. CSS specifico per quel widget
3. Note di implementazione

## 📞 Contatti
**Posture Studio Pilates**

STUDIO FONTANA
- 📍 Via Galli Marchiò, 3 - 42048 Fontana (RE)

STUDIO FONTANA
- 📍 Via Emilia Ovest, 54/1d - 42048 Rubiera (RE)
  
- 📱 351 3618222
- 📧 info@posturestudiopilates.it
- 🌐 www.posturestudiopilates.it

## 📝 Note Tecniche

### Workflow CSS
1. CSS globale → `css/CSS_MASTER_v5.4.md`
2. CSS specifico widget → `pages/XX_PAGINA/XX_WIDGET.md`
3. NO Autoptimize (interferisce con transizioni)

### Transizioni
- Standard: 0.5s ease
- Slow: 0.7s ease
- Fast: 0.3s ease

---

**Ultimo aggiornamento**: Dicembre 2025
