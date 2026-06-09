# DECISIONS — monkmade-tools (Spoke)

> Spoke der BUILD ENGINE. PROBE im 28-Tage-Build-in-Public-Test. **Kein §14-Geld-Produkt.**
> Übergeordnet: CEO `decisions\2026-06-09-hebel-A-launch-setup.md` · Briefing `…\Outbox\AN-BUILD_BuildInPublic-Tool1_2026-06-09.md`.

## 2026-06-09 — Setup + Tool #1
- **Was:** Maker-Hub `monkmade-tools` (GitHub Pages) + Tool #1 = client-side Bild-Resizer/Kompressor/Konverter (PNG/JPG/WebP). Founder hat den CEO-Default bestätigt (Type-2, §18).
- **Architektur:** rein statisch, je Tool eine eigenständige `index.html` (HTML+CSS+JS inline, **null Dependencies**). Hub-`index.html` listet die Tools. Hosting GitHub Pages (gratis, §20 null-Wartung).
- **Bild-Resizer-Technik (§2, nur Browser-APIs):** `createImageBitmap` (EXIF-Orientierung) mit `<img>`-Fallback → `<canvas>` (`drawImage`) → `canvas.toBlob(mime, quality)` → Object-URL-Download. JPG bekommt weißen Hintergrund (keine Transparenz). Strg+V-Paste für Screenshots. **Kein Upload, keine Daten verlassen den Browser.**
- **Feedback-Pfad (§25 inbound, keine PII):** GitHub-Issue-Link (vorbefüllt) statt mailto → kein E-Mail-Leak, sammelbar im Asks-Log. Kein Tracking/Analytics.
- **Stop-Loss (§5):** Test-Ebene Tag 28 = **2026-07-07**. Auf Tool-Ebene kein eigener Stop-Loss (Probe).
- **Bewusst NICHT gebaut (Scope, §7/§18):** Batch/mehrere Bilder gleichzeitig, ZIP-Export, Crop, Backend, Account. Mögliche v2, falls Asks es verlangen.
