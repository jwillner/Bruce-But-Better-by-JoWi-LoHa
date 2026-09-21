# BruceButBetter-Modul

© Louis Havet-Quillivic & Joachim Willner · Version 0.3 · 21. September 2026

## 1. Einleitung

Dieses Dokument beschreibt den Start des Projekts «BruceButBetter-Modul»: Louis und Joachim wollen ein eigenes Hardware-Modul entwickeln, das sich an BruceButBetter orientiert - einem Downstream-Fork der Bruce-Firmware für ein selbstgebautes ESP32-S3-Multitool mit Flipper-Zero-ähnlichen Funktionen. Es dient als gemeinsamer Ausgangspunkt und wird mit fortschreitendem Projekt ergänzt. Das Projekt wird im GitHub-Repository [github.com/jwillner/Bruce-But-Better-by-JoWi-LoHa](https://github.com/jwillner/Bruce-But-Better-by-JoWi-LoHa) geführt.

### 1.1 Ausgangslage

BruceButBetter ist ein bestehendes Open-Source-Projekt ([github.com/Yoursel71/BruceButBetter](https://github.com/Yoursel71/BruceButBetter)), das auf einem ESP32-S3 N16R8 mit 1,3"-OLED-Display aufbaut und optional Module wie CC1101 (Sub-GHz), PN532 (NFC/RFID), zwei NRF24-Funkmodule, einen Si5351-Signalgenerator, IR-Sender/-Empfänger, microSD und einen Buzzer unterstützt. Vorbild ist der Flipper Zero. Statt das dortige Referenzdesign nachzubauen, wollen wir eine eigene Platine entwerfen und dabei selbst festlegen, welche Module verbaut werden.

#### 1.1.1 Ziel des Projekts

Ziel der ersten Phase ist eine eigene, funktionsfähige Leiterplatte mit ESP32-S3, Display und einer noch festzulegenden Auswahl an Modulen, auf der die Bruce-/BruceButBetter-Firmware lauffähig ist. Der Eigenbau soll Erfahrung im Platinendesign (KiCad) vermitteln und Raum für spätere eigene Anpassungen an Hardware wie Firmware schaffen.

### 1.2 Leitgedanke

Wir bauen nicht das Referenzdesign nach, sondern entwickeln ein eigenes, zur Firmware kompatibles Layout. Umfang und Modulauswahl richten sich nach dem, was wir tatsächlich nutzen wollen - lieber ein kleineres, sauber funktionierendes Modul als ein Nachbau mit ungenutzten Funktionen.

## 2. Planung und Umsetzung

Die folgende Übersicht zeigt die geplanten Arbeitsschritte. Termine sind zum jetzigen Zeitpunkt noch offen und werden ergänzt, sobald der Modulumfang feststeht.

| Schritt | Zuständig | Termin |
|---|---|---|
| Entwicklungsumgebung auf Proxmox einrichten (Linux-VMs, Tools unter Versionskontrolle) | Louis & Joachim | offen |
| Referenzprojekt & Firmware sichten (Bruce/BruceButBetter, Schaltplan, BOM) | Louis & Joachim | offen |
| Modulumfang für Version 1 festlegen | Louis & Joachim | offen |
| Schaltplan und Platine in KiCad entwerfen | offen | offen |
| Prototyp fertigen und bestücken lassen | offen | offen |
| Firmware flashen und Module einzeln testen | offen | offen |

### 2.1 Entwicklungsumgebung

Die Entwicklungsumgebung läuft nicht lokal, sondern auf einem PC mit Proxmox: Darauf sind mehrere Linux-VMs eingerichtet, eine davon dient als eigentliche Entwicklungsumgebung, deren installierte Tools unter Versionskontrolle stehen. Für die Arbeit daran verbinden wir uns per VS Code Remote auf diese Linux-VM und nutzen dort Claude Code. Auf einer weiteren Linux-VM läuft Hermes zur Entwicklungsunterstützung. Der Projektcode liegt im öffentlichen GitHub-Repository [github.com/jwillner/Bruce-But-Better-by-JoWi-LoHa](https://github.com/jwillner/Bruce-But-Better-by-JoWi-LoHa).

### 2.2 Zusammenarbeit

Louis (louis.havetquillivic@gmail.com) und Joachim (joachim.willner@gmail.com) planen und entwickeln das Modul gemeinsam. Die konkrete Aufteilung von Hardware- und Firmware-Aufgaben wird beim ersten gemeinsamen Termin festgelegt und danach in diesem Dokument nachgetragen.

#### 2.2.1 Nächste Schritte

Als Nächstes werden das BruceButBetter-Repository und die zugrunde liegende Bruce-Firmware im Detail gesichtet (Referenzschaltplan, Stückliste, unterstützte Module), um daraus den Modulumfang für die erste eigene Version abzuleiten. Anschliessend wird das KiCad-Projekt im Verzeichnis `hardware/` angelegt.

## 3. Ausblick

Nach der ersten funktionierenden Version ist offen, ob das Modul um weitere Funktionen erweitert, in ein Gehäuse integriert oder in einer zweiten Revision überarbeitet wird. Diese Punkte werden nach Abschluss der ersten Iteration entschieden.

> **Hinweis:** Dieses Dokument ist der erste Entwurf und wird mit fortschreitendem Projekt aktualisiert. Termine und Aufgabenverteilung sind aktuell Platzhalter.
