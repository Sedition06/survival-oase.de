# Deployment Guide – Survival-Oase

## Projektübersicht

Dies ist eine statische Website für **survival-oase.de** ohne CMS, Datenbank oder Server-seitige Verarbeitung. Die Website besteht aus reinem HTML, CSS und statischen Dateien und kann direkt auf klassisches Webhosting (z.B. Netcup) hochgeladen werden.

## Projektstruktur

```
survival-oase.de/
├── index.html                                    # Startseite (Positionierungsseite)
├── css/
│   └── styles.css                               # Gemeinsames Stylesheet
├── artikel/
│   ├── warum-survival-tipps-gefaehrlich-sind.html
│   ├── bewegung-ist-selten-die-loesung.html
│   └── risiken-richtig-priorisieren.html
├── includes/
│   └── article-template.html                    # Template für zukünftige Artikel
├── impressum.html                               # Impressum (zu personalisieren)
├── datenschutz.html                             # Datenschutzerklärung (zu personalisieren)
├── robots.txt                                   # SEO: Anweisungen für Suchmaschinen
├── sitemap.xml                                  # SEO: Sitemap für Suchmaschinen
├── .htaccess                                    # Apache-Konfiguration (optional)
└── DEPLOYMENT_GUIDE.md                          # Diese Datei
```

## Inhalte

### Startseite (index.html)
- **Zweck:** Positionierungsseite mit klarer Kernbotschaft
- **Kernbotschaft:** "Survival ist kein Abenteuer. Es ist eine Serie von Entscheidungen unter Risiko."
- **Struktur:**
  - Hero-Text mit Kernbotschaft
  - Abschnitt: "Warum Bauchgefühl problematisch ist"
  - Abschnitt: "Warum Bewegung, Optimismus und Improvisation oft falsch priorisiert werden"
  - Abschnitt: "Warum Wissen ≠ Entscheidungskompetenz ist"
  - Abschnitt: "Worum es hier geht" (3 Kernthemen)
  - Abschnitt: "Worum es hier bewusst nicht geht" (3 Ausschlusskriterien)
  - Abschnitt: "Weiterführende Analysen" (Links zu den 3 Artikeln)
  - Abschnitt: "Vom Wissen zur Entscheidung" (WES-Integration)
  - Haftungsausschluss

### Artikel (artikel/*.html)

#### 1. Warum die meisten Survival-Tipps gefährlich sind
- **URL:** `/artikel/warum-survival-tipps-gefaehrlich-sind.html`
- **Inhalt:** Kritische Analyse populärer Survival-Tipps und deren Fallstricke
- **Struktur:** H2-Überschriften, Listenelemente, Blockquotes

#### 2. Bewegung ist selten die Lösung – und oft das Problem
- **URL:** `/artikel/bewegung-ist-selten-die-loesung.html`
- **Inhalt:** Psychologischer Bewegungsdrang, Energieverlust, Wärmeverlust, Verletzungsrisiken
- **Struktur:** H2/H3-Überschriften, Szenarien, Blockquotes

#### 3. Risiken richtig priorisieren: Hunger ist fast nie das akute Problem
- **URL:** `/artikel/risiken-richtig-priorisieren.html`
- **Inhalt:** Falsche Gefahrenhierarchien, reale Prioritäten, 3er-Regel
- **Struktur:** H2/H3-Überschriften, Listenelemente, Blockquotes

### Rechtliche Seiten
- **impressum.html:** Muss mit Ihren Kontaktdaten und Impressum-Informationen personalisiert werden
- **datenschutz.html:** Muss mit Ihrer vollständigen Datenschutzerklärung personalisiert werden

## Design & Styling

### Farbschema
- **Dunkelgrün:** `#1a4d2e` (Primärfarbe, Header, Buttons)
- **Akzent-Grün:** `#2d6a3e` (Hover-States, Borders)
- **Helles Beige:** `#f5f1e8` (Hintergrund, Hero-Sektion)
- **Text-Dunkelgrau:** `#222222` (Haupttext für hohe Lesbarkeit)
- **Text-Hellgrau:** `#666666` (Sekundärtext)

### Responsive Design
- **Desktop:** Optimiert für Bildschirme ab 900px Breite
- **Tablet:** Angepasstes Layout ab 768px
- **Mobile:** Vollständig responsive ab 480px

### Typografie
- **Font:** System-Schriften (Apple System Font, Segoe UI, Roboto)
- **Zeilenhöhe:** 1.6 für Fließtext, 1.4 für Überschriften
- **Kontrast:** Hoher Kontrast für Barrierefreiheit

## SEO-Optimierung

### Technische SEO
- ✅ Semantische HTML-Struktur (H1, H2, H3)
- ✅ Meta-Descriptions auf jeder Seite
- ✅ Sprechende URLs (z.B. `/artikel/warum-survival-tipps-gefaehrlich-sind.html`)
- ✅ Canonical-Tags zur Vermeidung von Duplicate Content
- ✅ Open Graph Meta-Tags für Social Sharing
- ✅ Mobile-Optimierung (Viewport-Meta-Tag, responsive CSS)
- ✅ robots.txt für Suchmaschinen-Crawler
- ✅ sitemap.xml für Suchmaschinen

### Inhaltliche SEO
- ✅ Fokus auf Themenautorität (nicht Keyword-Dichte)
- ✅ Semantisch verwandte Begriffe im Text
- ✅ Interne Verlinkung zwischen Artikeln
- ✅ Klare Struktur mit aussagekräftigen Überschriften
- ✅ Keine gekauften Backlinks
- ✅ Keine KI-Massencontent-Strategie

### Performance
- ✅ Minimales CSS (keine Frameworks)
- ✅ Keine externen Abhängigkeiten (außer Google Fonts optional)
- ✅ GZIP-Kompression aktiviert (.htaccess)
- ✅ Browser-Caching konfiguriert (.htaccess)
- ✅ Schnelle Ladezeiten durch statische HTML

## Deployment auf Netcup

### Schritt 1: Vorbereitung
1. Loggen Sie sich in Ihr Netcup-Kundenportal ein
2. Navigieren Sie zum Dateimanager oder FTP-Zugang
3. Notieren Sie sich Ihre FTP-Zugangsdaten (Host, Benutzername, Passwort)

### Schritt 2: Upload via FTP

#### Option A: Mit FTP-Client (z.B. FileZilla)
1. Öffnen Sie Ihren FTP-Client
2. Verbinden Sie sich mit den Netcup-Servern:
   - **Host:** ftp.survival-oase.de (oder Ihre Netcup-FTP-Adresse)
   - **Benutzername:** Ihr FTP-Benutzername
   - **Passwort:** Ihr FTP-Passwort
   - **Port:** 21 (Standard)
3. Navigieren Sie zum öffentlichen Verzeichnis (meist `public_html/` oder `www/`)
4. Laden Sie alle Dateien und Ordner aus dem `survival-oase.de/`-Verzeichnis hoch:
   - `index.html`
   - `css/` (Ordner mit styles.css)
   - `artikel/` (Ordner mit den 3 HTML-Dateien)
   - `impressum.html`
   - `datenschutz.html`
   - `robots.txt`
   - `sitemap.xml`
   - `.htaccess` (falls Apache verwendet wird)

#### Option B: Mit Netcup Dateimanager
1. Loggen Sie sich im Netcup-Kundenportal ein
2. Navigieren Sie zum Dateimanager
3. Navigieren Sie zum öffentlichen Verzeichnis
4. Laden Sie die Dateien direkt über die Web-Oberfläche hoch

### Schritt 3: Überprüfung
1. Öffnen Sie `https://survival-oase.de/` in Ihrem Browser
2. Überprüfen Sie:
   - ✅ Startseite lädt korrekt
   - ✅ CSS wird korrekt angewendet (Farben, Layout)
   - ✅ Navigation funktioniert
   - ✅ Links zu Artikeln funktionieren
   - ✅ Responsive Design funktioniert (auf Mobilgerät testen)
   - ✅ Impressum und Datenschutz sind erreichbar

### Schritt 4: Personalisierung

Bevor Sie die Website live nehmen, personalisieren Sie folgende Dateien:

#### impressum.html
- Ersetzen Sie "Max Mustermann" mit Ihrem Namen
- Ersetzen Sie die Adresse mit Ihrer Adresse
- Ersetzen Sie Telefon und E-Mail mit Ihren Kontaktdaten
- Ergänzen Sie alle erforderlichen Angaben gemäß deutschem Recht (§ 5 TMG)

#### datenschutz.html
- Schreiben Sie eine vollständige Datenschutzerklärung gemäß DSGVO
- Geben Sie Informationen über Datenverarbeitung durch Ihren Hosting-Provider an
- Beschreiben Sie Ihre Datenschutzmaßnahmen

### Schritt 5: SSL/HTTPS aktivieren
1. Überprüfen Sie, ob Netcup ein kostenloses SSL-Zertifikat anbietet (meist Let's Encrypt)
2. Aktivieren Sie HTTPS in den Domain-Einstellungen
3. Optional: Aktivieren Sie die HTTP-zu-HTTPS-Umleitung in `.htaccess` (siehe Kommentare in der Datei)

### Schritt 6: Suchmaschinen-Registrierung
1. Registrieren Sie Ihre Website bei Google Search Console:
   - Gehen Sie zu https://search.google.com/search-console
   - Fügen Sie Ihre Domain hinzu
   - Laden Sie die `sitemap.xml` hoch
2. Registrieren Sie Ihre Website bei Bing Webmaster Tools:
   - Gehen Sie zu https://www.bing.com/webmasters
   - Fügen Sie Ihre Domain hinzu

## Wartung & Updates

### Neue Artikel hinzufügen
1. Erstellen Sie eine neue HTML-Datei im `/artikel/`-Verzeichnis
2. Verwenden Sie die Struktur aus `includes/article-template.html` als Vorlage
3. Schreiben Sie den Artikel-Inhalt
4. Fügen Sie einen Link auf der Startseite hinzu (in der Sektion "Weiterführende Analysen")
5. Aktualisieren Sie `sitemap.xml` mit der neuen URL
6. Laden Sie die neue Datei via FTP hoch

### Inhalte aktualisieren
1. Bearbeiten Sie die entsprechende HTML-Datei lokal
2. Laden Sie die aktualisierte Datei via FTP hoch
3. Leeren Sie den Browser-Cache (Strg+F5 / Cmd+Shift+R)

### Regelmäßige Überprüfungen
- Überprüfen Sie monatlich die Google Search Console auf Fehler
- Überprüfen Sie Links auf Funktionsfähigkeit
- Überprüfen Sie die Website auf Responsive Design auf verschiedenen Geräten

## Technische Anforderungen

### Webhosting
- **Unterstützung:** Statisches HTML, CSS
- **Nicht erforderlich:** PHP, Node.js, Datenbank, Build-Tools
- **Empfohlen:** GZIP-Kompression, Browser-Caching, SSL/HTTPS

### Browser-Kompatibilität
- Chrome/Edge (alle modernen Versionen)
- Firefox (alle modernen Versionen)
- Safari (alle modernen Versionen)
- Internet Explorer 11 (begrenzte Unterstützung)

## Fehlerbehebung

### Problem: CSS wird nicht angewendet
- **Lösung:** Überprüfen Sie, ob der `/css/`-Ordner mit `styles.css` hochgeladen wurde
- **Lösung:** Leeren Sie den Browser-Cache (Strg+F5)

### Problem: Links zu Artikeln funktionieren nicht
- **Lösung:** Überprüfen Sie, ob der `/artikel/`-Ordner mit allen 3 HTML-Dateien hochgeladen wurde
- **Lösung:** Überprüfen Sie die Pfade in den Links (sollten relativ sein: `artikel/dateiname.html`)

### Problem: Website ist sehr langsam
- **Lösung:** Überprüfen Sie, ob GZIP-Kompression aktiviert ist (.htaccess)
- **Lösung:** Überprüfen Sie, ob Browser-Caching aktiviert ist
- **Lösung:** Kontaktieren Sie Ihren Hosting-Provider

### Problem: Impressum und Datenschutz zeigen Platzhalter
- **Lösung:** Personalisieren Sie `impressum.html` und `datenschutz.html` mit Ihren Daten

## Support & Kontakt

Diese Website wurde mit statischem HTML und CSS erstellt. Bei Fragen zur Struktur oder zum Deployment kontaktieren Sie Ihren Hosting-Provider oder einen Web-Developer.

---

**Letzte Aktualisierung:** Januar 2025
