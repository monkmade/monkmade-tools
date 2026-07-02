# DECISIONS — monkmade-tools

> Ausführender Distributions-/Sammel-Arm von FounderOS. PROBE im 28-Tage-Build-in-Public-Test. **Kein Geld-/SaaS-Produkt.**
> Übergeordnetes System: FounderOS (Vault `00_CORE` = read-only Wahrheit; siehe `.claude/CLAUDE.md`).

## 2026-06-09 — Setup + Tool #1
- **Was:** Maker-Hub `monkmade-tools` (GitHub Pages) + Tool #1 = client-side Bild-Resizer/Kompressor/Konverter (PNG/JPG/WebP). Michel hat den vorgeschlagenen Default bestätigt (leicht umkehrbar).
- **Architektur:** rein statisch, je Tool eine eigenständige `index.html` (HTML+CSS+JS inline, **null Dependencies**). Hub-`index.html` listet die Tools. Hosting GitHub Pages (gratis, null Wartung).
- **Bild-Resizer-Technik (nur Browser-APIs):** `createImageBitmap` (EXIF-Orientierung) mit `<img>`-Fallback → `<canvas>` (`drawImage`) → `canvas.toBlob(mime, quality)` → Object-URL-Download. JPG bekommt weißen Hintergrund (keine Transparenz). Strg+V-Paste für Screenshots. **Kein Upload, keine Daten verlassen den Browser.**
- **Feedback-Pfad (inbound, keine PII):** GitHub-Issue-Link (vorbefüllt) statt mailto → kein E-Mail-Leak, sammelbar im Asks-Log. Kein Tracking/Analytics.
- **Test-Ende:** 28-Tage-Test endet Tag 28 = **2026-07-07**. Auf Tool-Ebene kein eigener Abbruch-Punkt (Probe).
- **Bewusst NICHT gebaut (Scope):** Batch/mehrere Bilder gleichzeitig, ZIP-Export, Crop, Backend, Account. Mögliche v2, falls Asks es verlangen.

## 2026-06-13 — Tool #2 = Photo Privacy Check
- **Was:** `photo-privacy/index.html` — zeigt versteckte Metadaten (EXIF) eines Fotos an und entfernt sie per „saubere Kopie".
- **Funktion:** (1) Bild laden per Drag&Drop / Klick / Strg+V. (2) EXIF-Anzeige: GPS-Standort (mit deutlicher Warnung „dieses Foto verrät deinen Standort" + Koordinaten als Text), Aufnahmedatum, Kamera/Modell, Software. Kein EXIF → beruhigende Meldung. PNG/WebP → Hinweis statt Tiefenparse. (3) „Saubere Kopie speichern" entfernt ALLE Metadaten, Format-/Qualitätswahl wie Tool #1, Download als `<name>_clean.<ext>`.
- **EXIF-Technik (nur Browser-APIs, ~180 Zeilen vanilla JS):** rohe Bytes per `FileReader.readAsArrayBuffer` → `DataView`. JPEG-Marker durchlaufen bis APP1 (`0xFFE1`) mit „Exif\0\0"; TIFF-Header (Byte-Reihenfolge II/MM) → IFD0 (Make/Model/Software) → ExifIFD (`0x8769` → DateTimeOriginal) → GPS-IFD (`0x8825` → Breiten-/Längengrad als 3 Rationals + Referenz N/S/E/W). KEINE Library, kein externer Request.
- **Saubere Kopie = Metadaten-Strip via Canvas:** `createImageBitmap` mit `imageOrientation:"from-image"` (+ `<img>`-Fallback) → `<canvas>` → `canvas.toBlob(mime, quality)`. Das Neu-Kodieren wirft alle EXIF-/GPS-Daten weg; Orientierung bleibt korrekt. JPG bekommt weißen Hintergrund.
- **Privacy = Produktkern:** Bild-Daten und Koordinaten verlassen NIE den Browser, keine externen Requests, KEINE Karten-Einbettung (GPS nur als Text). Feedback-Pfad = vorbefüllter GitHub-Issue-Link (inbound, kein Tracking).
- **Test-Ende:** 28-Tage-Test endet Tag 28 = **2026-07-07**. Auf Tool-Ebene kein eigener Abbruch-Punkt (Probe).
- **Bewusst NICHT gebaut (Scope):** KEIN Batch/mehrere Fotos, KEIN Video/PDF, KEINE Karten-API/Karten-Einbettung, KEIN PNG/WebP-Chunk-Tiefen-Editor (nur Canvas-Strip), KEIN Schreiben/Editieren einzelner EXIF-Felder, KEIN Backend/Account. Mögliche v2, falls Asks es verlangen.
