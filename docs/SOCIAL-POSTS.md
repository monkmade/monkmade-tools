# SOCIAL-POSTS.md

Fertige Post-Texte + vorausgefüllte X-Links für die Reichweite von monkmade-tools.
Damit gehen die Vorlagen nie wieder als Chat-Artefakt verloren.

- **X-Account:** @monkmadetools
- **Standard-Sprache:** Englisch (größte Reichweite; Seiten sind EN by default)
- **Absetzen:** X-„intent"-Link öffnen → Compose ist vorausgefüllt → manuell „Post" klicken.
  Kein Bot, keine API, kein Scraping (X's eigene Tweet-Button-Technik).

## Sicherheits-Regeln (X, recherchiert)

- KI-*Texte* sind erlaubt; verboten ist nur *Account-Automatisierung* (Bots, Scripting,
  Scraping, Massenaktionen, doppelte Posts).
- **Zeitversetzt** posten, nicht alles am selben Tag (natürliches Muster, 2–10/Tag ok).
- Pro Tool **eine Sprache** — EN+DE desselben Tools nicht direkt hintereinander („duplicative").

## Post-Historie & Reihenfolge

- **Image Resizer** — ⚠️ **bereits gepostet am 2026-06-10** (kombiniert mit
  Build-in-Public-Intro + „next annoying task?"-Frage). **Nicht identisch erneut
  posten** (duplicative). Nur später mit frischem Winkel (z. B. „paste screenshot
  with Ctrl+V").
- **Photo Privacy** (stärkste Story) — ✅ gepostet am 2026-07-01
- **Hub** — ✅ gepostet **und angepinnt** am 2026-07-02. Neuer Text (2 Tools live),
  kein Duplikat des Jun-10-Intros.

---

## 1) Photo Privacy Check  ✅ gepostet 2026-07-01

Link: https://monkmade.github.io/monkmade-tools/photo-privacy/

**EN (gepostet):**
```
Your photos quietly carry your GPS location, camera & timestamp.
Drop one in → see exactly what it reveals → strip it all before sharing.
100% in your browser. No upload, no account, no tracking.
#privacy #EXIF #buildinpublic
```

**DE (Alternative):**
```
Deine Fotos verraten still deinen GPS-Standort, Kamera & Zeitstempel.
Bild reinziehen → sehen, was drinsteckt → alles entfernen vor dem Teilen.
100 % im Browser. Kein Upload, kein Account, kein Tracking.
#Datenschutz #EXIF #buildinpublic
```

**Intent-Link (EN, ready-to-post):**
```
https://twitter.com/intent/tweet?text=Your%20photos%20quietly%20carry%20your%20GPS%20location%2C%20camera%20%26%20timestamp.%0ADrop%20one%20in%20%E2%86%92%20see%20exactly%20what%20it%20reveals%20%E2%86%92%20strip%20it%20all%20before%20sharing.%0A100%25%20in%20your%20browser.%20No%20upload%2C%20no%20account%2C%20no%20tracking.%0A%23privacy%20%23EXIF%20%23buildinpublic&url=https%3A%2F%2Fmonkmade.github.io%2Fmonkmade-tools%2Fphoto-privacy%2F
```

---

## 2) Image Resizer & Converter  — offen (zeitversetzt posten)

Link: https://monkmade.github.io/monkmade-tools/image-resizer/

**EN (Standard):**
```
Resize, compress & convert images to PNG / JPG / WebP - right in your browser.
No upload, no account, no tracking. Your files never leave your device.
#tools #webdev #buildinpublic
```

**DE (Alternative):**
```
Bilder verkleinern, komprimieren & umwandeln in PNG / JPG / WebP — direkt im Browser.
Kein Upload, kein Account, kein Tracking. Deine Dateien verlassen dein Gerät nie.
#Tools #webdev #buildinpublic
```

**Intent-Link (EN, ready-to-post):**
```
https://twitter.com/intent/tweet?text=Resize%2C%20compress%20%26%20convert%20images%20to%20PNG%20%2F%20JPG%20%2F%20WebP%20-%20right%20in%20your%20browser.%0ANo%20upload%2C%20no%20account%2C%20no%20tracking.%20Your%20files%20never%20leave%20your%20device.%0A%23tools%20%23webdev%20%23buildinpublic&url=https%3A%2F%2Fmonkmade.github.io%2Fmonkmade-tools%2Fimage-resizer%2F
```

---

## 3) Hub (monkmade tools)  ✅ gepostet + angepinnt 2026-07-02

Link: https://monkmade.github.io/monkmade-tools/

**EN (Standard):**
```
I'm building a small set of tiny tools that run 100% in your browser.
No upload, no account, no tracking, free. One tool, one clear job.
Building in public - first tools live now 👇
#buildinpublic #indiehackers #tools
```

**DE (Alternative):**
```
Ich baue eine kleine Sammlung winziger Tools, die 100 % im Browser laufen.
Kein Upload, kein Account, kein Tracking, kostenlos. Ein Tool, ein klarer Zweck.
Build in Public — erste Tools sind live 👇
#buildinpublic #indiehackers #tools
```

**Intent-Link (EN, ready-to-post):**
```
https://twitter.com/intent/tweet?text=I'm%20building%20a%20small%20set%20of%20tiny%20tools%20that%20run%20100%25%20in%20your%20browser.%0ANo%20upload%2C%20no%20account%2C%20no%20tracking%2C%20free.%20One%20tool%2C%20one%20clear%20job.%0ABuilding%20in%20public%20-%20first%20tools%20live%20now%20%F0%9F%91%87%0A%23buildinpublic%20%23indiehackers%20%23tools&url=https%3A%2F%2Fmonkmade.github.io%2Fmonkmade-tools%2F
```

---

## Rezept: neuen Intent-Link bauen

`https://twitter.com/intent/tweet?text=<URL-encoded Text>&url=<URL-encoded Link>`

- `text` + `url` zusammen → X hängt den Link hinten an. Text so lang, dass
  Text + ~23 Zeichen (t.co-Link) unter 280 bleibt.
- Encoding in PowerShell: `[uri]::EscapeDataString($text)`.

## Reddit

**Account:** u/monkmadetools (neu → in freundlichen Subs starten, Karma aufbauen).
Reddit: kein Intent-Link, manuell posten. Value-first, kein Verkaufston, keine
Hashtags. Gestaffelt, nicht mehrere Subs am selben Tag.

### R1) r/buildinpublic — Hub  ✅ gepostet 2026-07-02

Submit: https://www.reddit.com/r/buildinpublic/submit?type=TEXT

**Titel:**
```
Building tiny browser tools that run 100% client-side — no upload, no account, no tracking (2 live)
```

**Text:**
```
I got tired of "simple" online tools that make you upload your files to some
server, sign up for an account, or sit through tracking + ads. So I started
building the opposite: tiny, single-purpose tools that run entirely in your
browser. Your files never leave your device.

Two are live so far:

• Image Resizer & Converter — resize/compress/convert to PNG/JPG/WebP
• Photo Privacy Check — see the hidden GPS location, camera & timestamp (EXIF)
  in your photos, and strip it all before sharing

All free, no account, no backend, no tracking. Static site, open on GitHub.

Hub: https://monkmade.github.io/monkmade-tools/

It's a build-in-public experiment — goal is to reach the first 100 real users
and learn what people actually find useful. I'd love feedback, and honestly:
what's a small, annoying manual task in your workflow that a tiny browser tool
could solve? That's how I pick the next one.
```

### R2) r/SideProject — Hub  — offen, bereit zum Posten

Submit: https://www.reddit.com/r/SideProject/submit?type=TEXT

Anderer Winkel als R1 (problem-first statt Build-in-Public-Journey, kein Duplikat):

**Titel:**
```
Made two tiny tools that run entirely in your browser — because I was tired of "simple" tools that need an upload or an account
```

**Text:**
```
Every time I needed to quickly resize an image or check what's hidden in a
photo's metadata, I'd end up on some site that wanted me to upload the file,
create an account, or sit through ads/tracking for something that should take
5 seconds.

So I built two small tools that do the whole thing in the browser — nothing
ever gets uploaded:

• Image Resizer & Converter — resize/compress/convert to PNG/JPG/WebP, paste
  a screenshot straight in with Ctrl+V
• Photo Privacy Check — shows the hidden GPS location, camera model & timestamp
  in your photos, and lets you strip all of it before sharing

Both free, no account, no backend, no tracking — static site, code's open.

https://monkmade.github.io/monkmade-tools/

Would love feedback, and if there's a small annoying task like this in your
own workflow, tell me — that's basically how I pick what to build next.
```

### Nächste Reddit-Subs (gestaffelt, je 1–2 Tage Abstand)

- **r/indiehackers** — gleicher Hub-Text, Titel ggf. leicht anders.
- **r/SomethingIMade** — „ich hab das gebaut"-Ton.
- **r/InternetIsBeautiful** — nur 1 Tool (Photo Privacy), strenges Format.
- **r/webdev** — nur „Showoff Saturday"-Thread.
- Später/vorsichtig: **r/privacy**, **r/degoogle** — Photo-Privacy-Story, aber
  strenge Self-Promo-Regeln → erst Karma / Mods fragen.

## Weitere Kanäle (Fahrplan)

Siehe `docs/PROJECT_STATUS.md` → Offene Punkte. Gestaffelt, nicht alles am selben Tag:
Hacker News „Show HN", Indie Hackers, freie Verzeichnisse (Uneed, DevHunt,
AlternativeTo). Texte kommen hier dazu.
