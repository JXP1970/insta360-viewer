# Changelog

Alle nennenswerten Änderungen an diesem Projekt.
Format nach [Keep a Changelog](https://keepachangelog.com/de/1.0.0/),
Versionierung nach [SemVer](https://semver.org/lang/de/).

## [1.2.0] - 2026-07-26

### Hinzugefügt
- **Wählbares Export-Format**: JPG / PNG / WebP mit Qualitätsregler (für JPG/WebP) — gilt für Ansicht, volles 360°-Frame und Serien-Export

## [1.1.0] - 2026-07-26

### Hinzugefügt
- **Little-Planet-Ansicht** 🪐 (stereografische Projektion) — Umschalter + Taste `P`; ziehen = drehen, scrollen = zoom
- **Galerie** 🗂️ — mehrere Fotos gleichzeitig laden (Mehrfachauswahl oder Drag&Drop), Thumbnail-Leiste, Klick zum Wechseln
- **Serien-Export** 🎞️ — aus einem Video alle N Sekunden ein volles 360°-Frame, gebündelt als ZIP (eingebauter Store-ZIP-Writer, keine Abhängigkeiten)
- GitHub Pages Einstiegsseite (`index.html`)

## [1.0.0] - 2026-07-26

### Hinzugefügt
- Interaktiver 360°-Viewer (WebGL) für equirectangular Fotos und Videos
- Dual-Fisheye-Projektion (`.insp`) mit Reglern für FOV, „hinten drehen" und „Objektive tauschen" sowie **X4-Preset**
- Automatische Erkennung equirectangular vs. Dual-Fisheye
- Einzelbild-Export: aktuelle Ansicht (PNG) und volles 360°-Frame; Dual-Fisheye wird zu equirectangular gestitcht
- Video-Steuerung: Play/Pause, Einzelbild-Schritt, Zeitleiste
- Auto-Load per URL-Parameter `?src=Datei&proj=equirect|fisheye`
- Eingebaute Demo- und Fisheye-Demo-Generatoren
- Maus-, Touch- und Tastaturbedienung, Vollbildmodus

### Behoben
- Non-Power-of-Two-Texturen (echte Fotos wie 5888×2944) wurden schwarz gerendert — Textur-Wrapping auf `CLAMP_TO_EDGE` umgestellt
