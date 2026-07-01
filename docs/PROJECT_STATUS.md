# PROJECT_STATUS.md

## Projekt

Name: `monkmade-tools`

---

## Stand

Datum: `2026-07-02`  
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

- **X-Profil komplett gebrandet + live (2026-07-02):** Header (`brand/header.png`) + `mascot-transparent.svg` committet (`2f859e2`, gepusht) und bei X hochgeladen; Avatar (`brand/avatar.png`) als Profilbild; Bio, Location („In your browser"), Website gesetzt. **Hub als Pinned-Tweet** gepostet und angepinnt. Doku-Update committet+gepusht (`f4e9f81`).
- **Reichweite Reddit gestartet (2026-07-02):** Erster Reddit-Post überhaupt — Hub in **r/buildinpublic** (u/monkmadetools), sauber gerendert, Hub-Link klickbar. Draft + Sub-Fahrplan in `docs/SOCIAL-POSTS.md` (R1 = gepostet).
- **Erkenntnis Kanal-Mix (offen, siehe unten):** Builder-Subs (r/buildinpublic, r/indiehackers) sind Maker-Echokammern — gut für Feedback/Karma/Proof, **schwach für echte Endnutzer**. Unsere realen Nutzer sitzen woanders (Foto-/Privacy-/Alltags-Subs). Kein Vault-/Strategie-Eingriff — nur bessere taktische Kanalwahl ab jetzt.
- **FounderOS als einziges System verankert** — committet (`7913744`) und gepusht: neuer Abschnitt „System-Zuordnung" ganz oben in `.claude/CLAUDE.md`. Kernaussage: FounderOS ist ab jetzt das einzige übergeordnete System; das alte CEO/IDEA LAB/BUILD ENGINE/§-Verfassungs-System ist aufgelöst. Rolle von monkmade-tools = ausführender Distributions-/Sammel-Arm. `00_CORE` = einzige Wahrheit, read-only; kein Direktzugriff/keine Auto-Pipeline; verdichtete Erkenntnisse hebt Michel manuell per FounderOS-Brain-Session in den Vault. (Read-only-Audits zuvor durchgeführt; die lokalen Alt-System-Reste in `DECISIONS.md`/`INBOUND-ASKS-LOG.md` sind noch nicht bereinigt — bewusst offen, Michel + FounderOS-Reviewer entscheiden.)
- **X-Header (Banner) erstellt**: 1500×500 im Marken-Stil (dunkel, Blau→Grün, Wortmarke + Claim + „no upload · no account · no tracking" + freigestellter Mascot). Liegt als `brand/header.png` (noch untracked). Wartet auf Michels „passt" + Upload bei X.
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
Git: `main lokal 2 Doku-Edits VOR origin (SOCIAL-POSTS.md + PROJECT_STATUS.md, noch nicht committet). Alle vorherigen Commits gepusht (zuletzt f4e9f81). Keine Untracked-Dateien mehr — brand/header.png + mascot-transparent.svg sind committet (2f859e2).`  
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

- **Kanal-Mix schärfen:** Nächste Subs bewusst Richtung echte Endnutzer wählen, nicht weitere Builder-Echokammern. Photo Privacy = stärkste Endnutzer-Story. (Rein taktisch, kein Vault-/Strategie-Eingriff.)
- Nächstes Tool (#3) ist noch nicht festgelegt — wartet auf Signal aus dem Inbound-Asks-Log.
- Erste echte Nutzer gewinnen / Reichweite aufbauen (Build in Public).
- **X-Posts (Reichweite):** Photo Privacy ✅ gepostet (2026-07-01). Hub ✅ gepostet **und angepinnt** (2026-07-02). Image Resizer war schon Jun 10 (nicht erneut) — später mit frischem Winkel. Alle Vorlagen in `docs/SOCIAL-POSTS.md`.
- **X-Profilbild + Header:** ✅ erledigt — Header (`brand/header.png`) + `mascot-transparent.svg` committet (`2f859e2`), Avatar (`brand/avatar.png`) + Header bei X hochgeladen, Bio/Location/Website gesetzt. Profil ist live und gebrandet. Später optional: Avatar als GitHub-Orga-Avatar; Mascot als Favicon/Hub-Logo statt Hammer-Emoji.
- **Reddit gestartet:** r/buildinpublic (Hub) ✅ gepostet 2026-07-02 (u/monkmadetools). Gestaffelt weiter: r/indiehackers, r/SomethingIMade, r/InternetIsBeautiful (Photo Privacy), r/webdev (Showoff Saturday), später r/privacy/r/degoogle (erst Karma). Drafts in `docs/SOCIAL-POSTS.md`. **Nicht** „Repost to more communities" nutzen.
- **Weitere Kanäle** (gestaffelt): Hacker News „Show HN", Indie Hackers, freie Verzeichnisse (Uneed/DevHunt/AlternativeTo) — Entwürfe in `docs/SOCIAL-POSTS.md`.
- **FounderOS-Migration (Alt-System-Bereinigung):** `.claude/CLAUDE.md` ist verankert (✅). Noch offen: Alt-System-Reste in `docs/Dokumente/DECISIONS.md` und `INBOUND-ASKS-LOG.md` bereinigen (§-Tags, CEO/BUILD ENGINE/IDEA LAB/Spoke, dangling Pfade). Bewusst nicht automatisch geändert — Michel + FounderOS-Reviewer entscheiden.
- Share-Vorschauen sind live geprüft (opengraph.xyz, 0 Fehler) — kein weiterer Check nötig.

---

## Nächster sicherer Schritt

```text
Die 2 offenen Doku-Edits (SOCIAL-POSTS.md + PROJECT_STATUS.md) committen + pushen.
Danach Reddit gestaffelt weiter — aber bewusst Richtung ECHTE Endnutzer statt nur
Builder-Subs: Photo-Privacy-Story für einen Endnutzer-Sub vorbereiten (r/privacy /
r/degoogle / r/InternetIsBeautiful), erst wenn u/monkmadetools etwas Karma hat;
bis dahin in r/buildinpublic auf Kommentare freundlich antworten. Post-Vorlagen +
Sub-Fahrplan in docs/SOCIAL-POSTS.md.
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
echte Nutzer (Distribution, kein SaaS). WICHTIG: FounderOS ist das einzige
übergeordnete System (siehe .claude/CLAUDE.md, „System-Zuordnung"); altes
CEO/BUILD-ENGINE-System aufgelöst. X-Profil ist jetzt komplett gebrandet + live
(Header/Avatar/Bio, Hub als Pinned-Tweet). Reddit gestartet: Hub in r/buildinpublic
(erster Reddit-Post). Post-Vorlagen + Sub-Fahrplan in docs/SOCIAL-POSTS.md.
Accounts: X @monkmadetools, Reddit u/monkmadetools (NICHT monkmade2). OFFEN:
2 Doku-Edits noch nicht committet/gepusht. Nächster Fokus: Kanäle bewusst Richtung
ECHTE Endnutzer (Photo-Privacy-Story), nicht nur Builder-Subs; Tool #3 aus Inbound-Asks.
```

---

## Letzter Checkpoint

Datum/Uhrzeit: `2026-07-02`  
Durchgeführt von: `Claude Code`

Zusammenfassung:

```text
Marke live + Reichweite ausgebaut. (1) X-Profil komplett: Header bestätigt,
brand/header.png + mascot-transparent.svg committet (2f859e2, gepusht), Header +
Avatar bei X hochgeladen, Bio/Location/Website gesetzt, Hub als Pinned-Tweet
gepostet + angepinnt. Doku-Update committet+gepusht (f4e9f81). (2) Reddit gestartet:
erster Post überhaupt — Hub in r/buildinpublic (u/monkmadetools), sauber gerendert.
Draft + Sub-Fahrplan in docs/SOCIAL-POSTS.md (R1 = gepostet). (3) Erkenntnis:
Builder-Subs = Feedback/Karma/Proof, aber schwach für echte Endnutzer — nächste
Kanäle bewusst Richtung Photo-Privacy-Endnutzer wählen. Kein Vault-/Strategie-
Eingriff (00_CORE/AUDIENCE bleibt read-only, wird nie von Projekt-Session berührt).
OFFEN am Sessionende: 2 Doku-Edits (SOCIAL-POSTS.md + PROJECT_STATUS.md) noch nicht
committet/gepusht — warten auf Michels Go. Sonst alles gepusht (zuletzt f4e9f81).
```
