# swb-entscheidet.github.io

Website von schwalbach-entscheidet.de.

- `site/` enthält alles, was ausgeliefert wird. Nur dieses Verzeichnis geht nach GitHub Pages.
- `.github/workflows/qualitaet.yml` prüft jeden PR (Links, HTML, Barrierefreiheit, Lighthouse) und deployt bei Push auf `main` nach GitHub Pages, sobald alle Checks grün sind.
- Lokal prüfen: `npm ci && npm run check:html` (bzw. `check:a11y` mit `python3 -m http.server 8080 --directory site`, `check:lighthouse`).
- Ein toter externer Link stoppt auch den Deploy. Ist die fremde Seite nur vorübergehend down, den Link in `.lycheeignore` aufnehmen und später wieder entfernen.
- Die Custom Domain steht in den Pages-Einstellungen; `site/CNAME` ist beim Actions-Deploy nur Dokumentation.
