# PROJECT_STATUS.md

## Projekt

Name: `monkmade-tools`

---

## Stand

Datum: `2026-07-01`  
Status: `Aktiv`

Kurzfassung:

```text
monkmade-tools ist ein Maker-Hub mit winzigen, einzweckigen Browser-Tools, die
zu 100 % client-seitig laufen — kein Upload, kein Account, kein Backend, kein
Tracking. Gehostet statisch auf GitHub Pages. Aktuell live: zwei Tools
(Image Resizer & Converter, Photo Privacy Check). Seiten sind standardmäßig
Englisch, deutsche Browser bekommen automatisch Deutsch (EN/DE-Umschalter).
Ziel ist Distribution/Audience, nicht ein SaaS-Produkt: die ersten 100 echten
Nutzer. Das Projekt ist Teil eines 28-Tage-Build-in-Public-Tests.
```

---

## Letzte Änderungen

- Reichweite/Shareability (Schritt 2) ergänzt — committet (`e82e8fb`) und gepusht:
  - **Social-Preview-Bilder**: 3 gebrandete PNGs (1200×630, monkmade-Dark-Stil, via Headless-Chrome gerendert) in `og/`; verdrahtet als `og:image` + Twitter `summary_large_image` + `og:url` + `canonical` auf allen 3 Seiten. Geteilte Links zeigen jetzt ein echtes Vorschaubild.
  - **Share-Button** auf allen 3 Seiten: 1-Klick (`navigator.share` auf Mobile, Copy-Link-Fallback am Desktop, „Copied!"-Feedback), EN/DE übersetzt, kein Tracking/keine Dependency.
  - **SEO-Hygiene**: `sitemap.xml` (3 URLs) + `robots.txt`.
- CLAUDE-Dateien konsolidiert: Es lagen zwei Versionen in `.claude/` (`CLAUDE.md` + `CLAUDE_monkmade_tools.md`). Die neue Version (mit zusätzlichem Abschnitt „Voice-/Transkript-Schutz") in die kanonische `.claude/CLAUDE.md` übernommen, die Duplikat-Datei gelöscht — committet (`bdaa058`, Rename inkl. Slash-Command-Dateien) und gepusht.
- Projektstruktur aufgeräumt: `CLAUDE.md` (umbenannt), `docs/PROJECT_STATUS.md` (neu aus Vorlage), `DECISIONS.md` ins Archiv `docs/Dokumente/` verschoben, Template entfernt — committet (`7d59c6d`) und gepusht.
- Tool #2 „Photo Privacy Check" ergänzt (EXIF-Anzeige + Canvas-Metadaten-Strip).
- Tool #1 + Hub auf Englisch als Standard umgestellt (Deutsch automatisch erkannt, EN/DE-Toggle).
- Maker-Hub + Tool #1 (client-seitiger Bild-Resizer/Konverter) initial veröffentlicht.

---

## Aktueller technischer Zustand

Build: `nicht vorhanden (rein statisch, kein Build-Schritt)`  
Tests: `nicht vorhanden`  
Git: `sauber (main = origin/main, alles committet und gepusht)`  
Dev-Server: `nicht relevant (lokal index.html im Browser öffnen)`

Bekannte Fehler:

- Keine bekannt.

---

## Wichtige Dateien

- `README.md` - Projektübersicht (Außensicht, für Besucher)
- `.claude/CLAUDE.md` - Arbeitsregeln & Leitplanken für Claude Code / KI-Sessions (inkl. Voice-/Transkript-Schutz)
- `docs/PROJECT_STATUS.md` - aktueller Stand & Übergabe (diese Datei)
- `docs/Dokumente/` - projektbezogene Materialien / Archiv
- `docs/Dokumente/DECISIONS.md` - Entscheidungs- & Architekturhistorie (Archiv, nicht aktiv geladen)
- `index.html` - Maker-Hub, listet alle Tools (EN/DE)
- `image-resizer/index.html` - Tool #1: Bild-Resizer & Konverter
- `photo-privacy/index.html` - Tool #2: Foto-Privatsphäre-Check
- `og/` - Social-Preview-Bilder (1200×630 PNG) für die Share-Vorschau
- `sitemap.xml` / `robots.txt` - SEO-Discovery (Root)
- `INBOUND-ASKS-LOG.md` - eingehende „Kannst du …?"-Wünsche (nur inbound)
- `LICENSE` - MIT

---

## Offene Punkte

- Nächstes Tool (#3) ist noch nicht festgelegt — wartet auf Signal aus dem Inbound-Asks-Log.
- Erste echte Nutzer gewinnen / Reichweite aufbauen (Build in Public).
- Share-Vorschauen nach dem GitHub-Pages-Redeploy final gegenchecken (opengraph.xyz / Card-Validatoren gegen die 3 Live-URLs; ggf. „scrape again" für Cache-Refresh). Danach echte Build-in-Public-Posts absetzen — die geteilten Links haben jetzt ein Vorschaubild.

---

## Nächster sicherer Schritt

```text
Reichweite jetzt aktiv nutzen: Share-Previews nach Pages-Redeploy prüfen und
Build-in-Public-Posts mit den Live-Links absetzen (Karten zeigen jetzt ein
Vorschaubild). Parallel: Tool #3 aus Inbound-Asks ableiten, sobald ≥3 gleiche
Asks eingehen. Repo ist sauber und gepusht.
```

---

## No-Gos / Vorsicht

- Kein Backend, kein Account, kein Tracking, keine externen Requests — Tools müssen 100 % client-seitig bleiben.
- Nicht zu einem SaaS-Produkt ausbauen, solange keine klare externe Nachfrage besteht.
- Keine Dependencies / kein Build-Pipeline einführen — jedes Tool bleibt eine eigenständige `index.html`.
- Nicht überengineeren: lieber veröffentlichen als polieren.

---

## Übergabe an nächste Session

Wenn eine neue ChatGPT-, Cursor- oder Claude-Code-Session startet, zuerst lesen:

1. `README.md`
2. `.claude/CLAUDE.md`
3. `docs/PROJECT_STATUS.md`

Kurzkontext für nächste Session:

```text
Maker-Hub mit 2 live Tools, rein statisch auf GitHub Pages. Ziel = erste 100
echte Nutzer (Distribution, kein SaaS). Repo ist sauber und gepusht. Shareability
steht jetzt: og:image-Preview-Karten (og/), Share-Button je Seite, sitemap/robots.
Nächster Fokus: Preview-Check nach Pages-Redeploy + Build-in-Public-Posts, und
Tool #3 aus Inbound-Asks ableiten.
```

---

## Letzter Checkpoint

Datum/Uhrzeit: `2026-07-01`  
Durchgeführt von: `Claude Code`

Zusammenfassung:

```text
Schritt 2 (Reichweite) umgesetzt: Social-Preview-Bilder (3× 1200×630 PNG in og/,
via Headless-Chrome gerendert) + og:image/Twitter-Cards/canonical auf allen 3
Seiten, 1-Klick-Share-Button (navigator.share + Copy-Fallback, EN/DE), sowie
sitemap.xml + robots.txt. Committet (e82e8fb) und gepusht. main = origin/main.
Offen: Preview nach Pages-Redeploy gegenchecken + Build-in-Public-Posts absetzen.
```
