# BruceButBetter-Modul (Eigenbau-Hardware)

Repository: [github.com/jwillner/Bruce-But-Better-by-JoWi-LoHa](https://github.com/jwillner/Bruce-But-Better-by-JoWi-LoHa)

## Projektziel

Louis und Joachim bauen ein eigenes Hardware-Modul im Stil von [BruceButBetter](https://github.com/Yoursel71/BruceButBetter) - einem selbstgebauten Multitool auf Basis eines ESP32-S3, das mit einem Downstream-Fork der Bruce-Firmware Flipper-Zero-ähnliche Funktionen bietet (Sub-GHz, NFC/RFID, IR, 2,4-GHz-Funk u.a.). Statt das Referenzdesign nachzubauen, entwickeln wir eine eigene Platine in KiCad und legen selbst fest, welche Module (CC1101, PN532, NRF24, Si5351, IR, microSD, Buzzer, OLED) verbaut werden.

Siehe [docs/](docs/) für die ausführliche Projektbeschreibung.

## Aktueller Fokus

1. **Jetzt**: BruceButBetter- und Bruce-Firmware sowie Referenzschaltung/BOM sichten, Modulumfang für die erste Version festlegen.
2. Als Nächstes: Schaltplan und Platine in KiCad entwerfen, Prototyp bestellen und bestücken.
3. Später: Firmware flashen, Module einzeln testen, Gehäuse.

## Entwicklungsumgebung

Die Entwicklungsumgebung läuft nicht lokal, sondern auf einem PC mit Proxmox: Darauf sind mehrere Linux-VMs eingerichtet, eine davon dient als eigentliche Entwicklungsumgebung, deren installierte Tools unter Versionskontrolle stehen. Für die Arbeit daran verbinden wir uns per VS Code Remote auf diese Linux-VM und nutzen dort Claude Code. Auf einer weiteren Linux-VM läuft Hermes zur Entwicklungsunterstützung.

## Verzeichnisstruktur

```text
.
├── docs/       Projektdokumentation (u.a. Projektbeschreibung)
├── hardware/   KiCad-Schaltplan, Platine, Bauteile, Gerber
├── firmware/   Notizen/Fork zur Bruce-/BruceButBetter-Firmware
└── notes/      Recherchen und Quellen
```

## Team

- Louis Havet-Quillivic (louis.havetquillivic@gmail.com)
- Joachim Willner (joachim.willner@gmail.com)
