# Vertrieben aus Schlesien — Interaktive Migrationskarte

Interaktive Karte für den Geschichtsunterricht: der Weg einer Familie aus
Schlesien nach Bayern nach 1945. Ein konstruiertes, aber historisch belegtes
Beispiel mit 6 Stationen. Per QR-Code auf dem Handy abrufbar.

**Live:** https://schlesien-migration.github.io/schlesien-migration/

## Dateien
- `index.html` — die komplette App (selbst-enthalten, nur Leaflet/CARTO + Google Fonts per CDN)
- `qr-code.png` / `qr-code.svg` — QR-Code auf die Live-URL, fürs Plakat
- `README.md` — diese Datei

## Lokal testen
```bash
cd schlesien-migrationskarte
python3 -m http.server 8753
# dann im Browser: http://localhost:8753/index.html
```

## Inhalt ändern
Alle Texte, Fakten und Koordinaten der Stationen stehen oben in `index.html`
im Array `STATIONS`. Anpassen, speichern, committen, pushen — GitHub Pages
aktualisiert sich automatisch in 1–2 Minuten.

## Aktualisieren / neu deployen
```bash
git add -A && git commit -m "update" && git push
```

## QR-Code neu erzeugen (falls URL sich ändert)
```bash
npx qrcode -o qr-code.png -w 1200 -e H "https://schlesien-migration.github.io/schlesien-migration/"
```

## Quellen (historische Einordnung)
- Lager Moschendorf — de.wikipedia.org/wiki/Lager_Moschendorf
- Heimatvertriebene in Bayern — bavariathek.bayern
- Operation Schwalbe / Aussiedlungstransporte — lwl.org, landsmannschaft-schlesien.de
- Flüchtlingslager — historisches-lexikon-bayerns.de

*Hinweis: Die dargestellte Familie ist ein konstruiertes Beispiel. Stationen,
Abläufe und Zahlen sind historisch belegt und stehen stellvertretend für das
Schicksal von Millionen Heimatvertriebenen.*
