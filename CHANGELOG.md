# Changelog

Alle nennenswerten Änderungen an diesem Projekt.
Format nach [Keep a Changelog](https://keepachangelog.com/de/1.0.0/),
Versionierung nach [SemVer](https://semver.org/lang/de/).

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
