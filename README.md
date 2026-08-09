# Innovarco Landingpage

Conversion-Landingpage für Werbeanzeigen (Meta/Google Ads) für [Innovarco](https://www.innovarco.de/) –
Agentur für End-to-End-App-Entwicklung aus Hamburg.

**Design: 1:1 im Original-CI von innovarco.de** (Webflow-Seite):

- Original-Schrift **BDO Grotesk** (Variable Font, direkt vom Innovarco-CDN geladen)
- Original-Farbtokens (`--neutral-1: #f6f6f3`, `--dark: #000`, Radius 6px/4px usw.)
- Original-Typografie (102/51/40/32/25/20px, Weight 400)
- Original-Bilder & -Icons (Hero-Handy, FlutterFlow-Logo, Plus-Icons, Footer-Logo) vom Webflow-CDN gehotlinkt
- Animationen wie im Original: gestaffeltes Fade-in beim Laden, Zoom-out des Hero-Bilds,
  Scroll-Einblendungen, Accordion-Panels, Endlos-Marquee der Technologie-Karten

## Aufbau

Eine einzelne Datei: `index.html` (HTML + CSS + JS inline, keine Build-Tools).
Läuft auf jedem Hosting (Netlify, Vercel, GitHub Pages, eigener Server).

**Sektionen:**

1. Navbar (INNOVARCO · Team / Services / Pakete)
2. Hero: Handy-Bild mit Zoom-out-Animation + „Deine Agentur für Apps, die funktionieren…"
3. „Mehr Effizienz. Weniger Kosten." mit 60% / 30% / 50%-Metrik-Boxen
4. FlutterFlow-Partner-Kachel (Gradient `45deg, #4b39ef → #fff`)
5. „Der Entwicklungsprozess" – 5 Accordion-Panels (Umfang, Design, Entwicklung, Test & Feedback, Support)
6. „Modernste Technologien." – Logo-Marquee
7. **Lead-Formular** (Name, E-Mail, Telefon, Vorhaben + Datenschutz-Checkbox) in der
   „Bereit für Deine App? Lass uns sprechen."-Kachel
8. FAQ-Accordions
9. Schwarzer Footer mit großem INNOVARCO-Logo, Kontakt & Adresse

## Formular anbinden

Das Formular zeigt aktuell nur die Erfolgsmeldung (Demo-Modus). Für echten Versand in
`index.html` die Konstante `FORM_ENDPOINT` setzen (Formspree, Make/Zapier-Webhook o. ä.):

```js
var FORM_ENDPOINT = "https://formspree.io/f/XXXXXXXX";
```

## Hinweise vor Live-Gang

- [ ] `FORM_ENDPOINT` setzen (siehe oben)
- [ ] Assets werden vom Webflow-CDN der Original-Seite geladen (`cdn.prod.website-files.com`).
      Für volle Unabhängigkeit die Bilder/Schrift herunterladen und lokal ins Repo legen.
- [ ] FAQ-Antworten sind kurz formuliert – bei Bedarf durch die Original-Antworten ersetzen.
- [ ] `noindex` im `<meta name="robots">` entfernen, falls die Seite indexiert werden soll.
