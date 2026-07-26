# 360° Viewer

Ein **eigenständiger 360°-Betrachter** für Insta360-Aufnahmen (X4 & Co.) — als **einzelne HTML-Datei**, ganz ohne Installation, ohne Server und ohne Internet. Deine Fotos und Videos verlassen dabei **nie deinen Rechner**.

> Standalone WebGL 360° photo/video viewer for Insta360 cameras. One self-contained HTML file — runs fully offline, your media never leaves your machine.

**▶ Live:** https://jxp1970.github.io/insta360-viewer/ (Foto per Drag&Drop laden — nichts wird hochgeladen, alles läuft im Browser)

## Funktionen

- 🖼️ **360°-Fotos** anzeigen — equirectangular **und** rohes Dual-Fisheye (`.insp`)
- 🎬 **360°-Videos** abspielen (mit Play/Pause, Zeitleiste, Einzelbild-Schritt)
- 🧭 **Frei umsehen** per Maus/Touch, zoomen per Scrollen/Pinch
- 🔎 **Auto-Erkennung**: equirectangular vs. Dual-Fisheye
- 📸 **Einzelbilder exportieren**:
  - *Ansicht* — der aktuelle Blick als flaches PNG
  - *Volles 360°-Frame* — komplettes Panorama; bei Dual-Fisheye wird zu **equirectangular gestitcht**
- 🐟 **Dual-Fisheye-Regler** (FOV / hinten drehen / Objektive tauschen) + **X4-Preset**
- 🪐 **Little-Planet-Ansicht** (stereografisch) — Taste `P`
- 🗂️ **Galerie** — mehrere Fotos laden, Thumbnails, Klick zum Wechseln
- 🎞️ **Serien-Export** — aus Video alle N Sekunden ein 360°-Frame, als ZIP
- ✨ Eingebaute **Demos** zum Ausprobieren ohne eigene Dateien
- 🔗 **Direkt-Öffnen** per URL-Parameter: `360-viewer.html?src=foto.jpg`

## Nutzung

1. `360-viewer.html` doppelklicken (öffnet im Browser).
2. Eine Datei hineinziehen oder über **🖼️ Foto** / **🎬 Video** laden.
3. Umsehen: **Maus ziehen** · Zoomen: **Scrollen** · Speichern: **📸 Ansicht**.

### Tastatur

| Taste | Funktion |
|------|----------|
| `Leertaste` | Video Play/Pause |
| `←` / `→` | Video einzelbildweise |
| `S` | Aktuelle Ansicht speichern |
| `F` | Vollbild |

## Dateiformate

| Format | Status |
|--------|--------|
| Equirectangular JPG/PNG (2:1) | ✅ Direkt (Insta360 exportiert Fotos meist so) |
| Rohes Dual-Fisheye `.insp` | ✅ Über Fisheye-Modus (Naht per Regler justierbar) |
| Video H.264 (MP4/`.insv`) | ✅ Abspielbar |
| Video H.265 / HEVC (5.7K/8K der X4) | ❌ Browser können HEVC nicht dekodieren — vorher nach H.264 wandeln |

## Hinweise

- Die exakte Fisheye-Geometrie der X4 ist **nicht** fest einkalibriert; die Naht wird über **FOV / hinten drehen / tauschen** von Hand justiert (Startwert: X4-Preset).
- Rein clientseitig (WebGL). Keine Daten gehen nach außen.

## Technik

Reines HTML + WebGL, keine Abhängigkeiten. Die Kugelprojektion läuft als Fragment-Shader über ein Vollbild-Dreieck (equirectangular Reprojektion bzw. Dual-Fisheye-Sampling).

## Lizenz

[MIT](LICENSE)
