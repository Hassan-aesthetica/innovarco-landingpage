# Innovarco Landingpage

Conversion-Landingpage für Werbeanzeigen (Meta/Google Ads) für [Innovarco](https://www.innovarco.de/) –
Agentur für End-to-End-App-Entwicklung aus Hamburg.

## Aufbau

Eine einzelne Datei: `index.html` (HTML + CSS + JS inline, keine Build-Tools nötig).
Kann direkt auf jedem Hosting (Netlify, Vercel, GitHub Pages, eigener Server) abgelegt werden.

**Struktur der Seite (Ad → Conversion):**

1. **Hero** – Problem-Hook („Ihre Prozesse fressen Zeit") + CTA + Trust-Elemente
2. **Probleme** – 3 Zeitfresser, die die Zielgruppe wiedererkennt
3. **Lösung** – Zeiteffizienz, Speed durch FlutterFlow, alles aus einer Hand
4. **Prozess** – 5 Schritte (Analyse → Design → Entwicklung → Testing → Support)
5. **Referenz** – Case Study Justmatch + Kundenstimmen
6. **FAQ** – Einwandbehandlung
7. **Formular** – Name, E-Mail, Telefon, Vorhaben + Datenschutz-Checkbox
8. **Footer** – Impressum/Datenschutz

## Anpassen

### CI / Farben

Alle Farben und Schriften liegen als CSS-Variablen am Anfang des `<style>`-Blocks
(`:root { … }`). Dort lassen sich Akzentfarbe, Hintergründe etc. in einer Minute
exakt an das Innovarco-CI angleichen.

### Formular anbinden

Das Formular zeigt aktuell nur die Erfolgsmeldung (Demo-Modus). Für echten Versand
in `index.html` die Konstante `FORM_ENDPOINT` setzen, z. B. auf einen
[Formspree](https://formspree.io)-, Make-/Zapier-Webhook- oder eigenen Server-Endpoint:

```js
var FORM_ENDPOINT = "https://formspree.io/f/XXXXXXXX";
```

### Wichtig vor Live-Gang

- [ ] **Kundenstimmen prüfen/ersetzen:** Die zwei Zitate im Referenz-Bereich sind
      Platzhalter und müssen durch echte, freigegebene Kundenstimmen ersetzt werden.
- [ ] **Kennzahlen prüfen:** Werte wie „bis zu 8 h Zeitersparnis" sind plausible
      Platzhalter – durch echte Projektzahlen ersetzen oder entfernen.
- [ ] Datenschutz-Link (`#datenschutz`) auf die echte Datenschutzerklärung zeigen lassen.
- [ ] `FORM_ENDPOINT` setzen (siehe oben).
- [ ] `noindex` im `<meta name="robots">` ggf. entfernen, falls die Seite indexiert werden soll.
