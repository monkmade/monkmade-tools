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

- **Marken-Mascot / Avatar erstellt**: süßer „digitaler Mönch" (chibi, Kapuze, Heiligenschein, Mint-Gesicht) via Recraft (V4 Vector, gratis). Liegt in `brand/` als `mascot.svg` (Vektor-Quelle, 1024²), `avatar.png` (400×400, Kopf-Zoom fürs X-Profilbild) und `avatar-full.png` (Ganzkörper, für Website/OG). Offen: Michel lädt `brand/avatar.png` bei X hoch.
- Reichweite aktiv gestartet (X): **Photo Privacy Check gepostet** (2026-07-01, @monkmadetools, EN) — live, og:image-Vorschaukarte zieht korrekt. Absetzweg: X-„intent"-Link (vorausgefüllter Compose, manueller Post-Klick — kein Bot/keine Automatisierung, X-konform). Image Resizer war bereits am 2026-06-10 gepostet (nicht erneut). Neue Datei `docs/SOCIAL-POSTS.md` sichert alle Post-Texte (EN/DE) + fertige intent-Links, damit nichts mehr als Chat-Artefakt verloren geht.
- OG-Feinschliff — committet (`b9938e5`) und gepusht: `og:site_name` = „monkmade tools" auf allen 3 Seiten; Seitentitel bei Image Resizer & Photo Privacy auf < 60 Zeichen gekürzt (statisches `<title>` und `I18N`-Titel EN/DE synchron). Auf opengraph.xyz gegengeprüft: **alle 3 Karten 0 Fehler**, die Warnungen „Site name missing" und „Page title too long" sind weg (verbleibend nur der ignorierbare opengraph.xyz-CTA-Hinweis).
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
- `docs/SOCIAL-POSTS.md` - fertige X-Post-Texte (EN/DE) + vorausgefüllte intent-Links + Sicherheits-Regeln
- `brand/` - Marken-Mascot/Avatar: `mascot.svg` (Vektor-Quelle), `avatar.png` (400×400 Kopf-Zoom, X-Profilbild), `avatar-full.png` (Ganzkörper)
- `sitemap.xml` / `robots.txt` - SEO-Discovery (Root)
- `INBOUND-ASKS-LOG.md` - eingehende „Kannst du …?"-Wünsche (nur inbound)
- `LICENSE` - MIT

---

## Offene Punkte

- Nächstes Tool (#3) ist noch nicht festgelegt — wartet auf Signal aus dem Inbound-Asks-Log.
- Erste echte Nutzer gewinnen / Reichweite aufbauen (Build in Public).
- **X-Posts (Reichweite):** Photo Privacy ✅ gepostet (2026-07-01). Image Resizer war schon Jun 10 (nicht erneut). **Offen: Hub als Pinned-Tweet** setzen (zeitversetzt, neuer Text) — Vorlage + Link liegen in `docs/SOCIAL-POSTS.md`.
- **X-Profilbild:** ✅ Mascot-Avatar erstellt (`brand/avatar.png`). Offen: Michel lädt ihn bei X hoch (optional auch als GitHub-Orga-Avatar). Später optional: Mascot als Favicon/Hub-Logo statt Hammer-Emoji.
- **Weitere Kanäle** (gestaffelt): Reddit (r/SideProject, r/privacy), Hacker News „Show HN", Indie Hackers, freie Verzeichnisse (Uneed/DevHunt/AlternativeTo) — Entwürfe kommen in `docs/SOCIAL-POSTS.md`.
- Share-Vorschauen sind live geprüft (opengraph.xyz, 0 Fehler) — kein weiterer Check nötig.

---

## Nächster sicherer Schritt

```text
Reichweite fortsetzen: auf frühe Interaktion beim Photo-Privacy-Post reagieren.
Zeitversetzt (anderer Tag) den Hub als Pinned-Tweet setzen. X-Profilbild ergänzen.
Danach weitere Kanäle gestaffelt (Reddit/Show HN/Indie Hackers/Verzeichnisse).
Parallel: Tool #3 aus Inbound-Asks ableiten, sobald ≥3 gleiche Asks eingehen.
Alle Post-Vorlagen liegen in docs/SOCIAL-POSTS.md.
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
steht & ist live geprüft: og:image-Preview-Karten (og/) mit og:site_name, Share-
Button je Seite, kurze Titel, sitemap/robots — opengraph.xyz meldet 0 Fehler.
Nächster Fokus: die vorbereiteten X-Posts absetzen (Reichweite) und Tool #3 aus
Inbound-Asks ableiten.
```

---

## Letzter Checkpoint

Datum/Uhrzeit: `2026-07-01`  
Durchgeführt von: `Claude Code`

Zusammenfassung:

```text
Schritt 2 (Reichweite) umgesetzt + gepolisht: Social-Preview-Bilder (3× 1200×630
PNG in og/, via Headless-Chrome gerendert), og:image/Twitter-Cards/canonical/
og:site_name + gekürzte Titel auf allen 3 Seiten, 1-Klick-Share-Button
(navigator.share + Copy-Fallback, EN/DE), sitemap.xml + robots.txt. Zwei Commits
(e82e8fb, b9938e5) + Doku, alles gepusht, main = origin/main, Working Tree sauber.
Live auf opengraph.xyz geprüft: 0 Fehler. Zusätzlich EXIF-Frage besprochen (wie
Photo Privacy den Standort aus den Bild-Metadaten liest — nicht aus Dateiname/IP)
und fertige X-Post-Vorlagen (EN/DE) erstellt (Chat-Artefakt, nicht im Repo).
Offen: X-Posts absetzen (Reichweite). Kein Technik-Schritt offen.
```
