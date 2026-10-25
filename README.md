# VIOCON Report Tool

Erstellt aus den Monta-Exporten (Excel/PDF) fertige **LIS- und Flotten-Reports**. Jeder Kunde
bekommt ein eigenes Profil mit eigenen Ordnern und auf Wunsch einem komplett eigenen Report-Layout.

![Vorschau](https://github.com/benreusollernenbayern-maker/VIOCON-Report-Tool/releases/latest/download/Vorschau.png)

## Download

**[⬇ VIOCON_Report_Tool.exe herunterladen](https://github.com/benreusollernenbayern-maker/VIOCON-Report-Tool/releases/latest/download/VIOCON_Report_Tool.exe)**
(neueste Version) · [Alle Versionen](https://github.com/benreusollernenbayern-maker/VIOCON-Report-Tool/releases) ·
[Änderungen](CHANGELOG.md)

## Installation

1. `VIOCON_Report_Tool.exe` herunterladen und in einen eigenen Ordner legen, z. B. `Dokumente\VIOCON`.
2. Starten. Zeigt Windows beim ersten Mal eine SmartScreen-Warnung, „Weitere Informationen“ und dann
   „Trotzdem ausführen“ wählen.
3. Beim ersten Start einer neuen Version richtet sich das Programm einmalig ein. Das dauert ein paar
   Sekunden und zeigt einen Fortschrittsbalken. Danach startet es jedes Mal sofort.

## Updates

Das Programm prüft beim Start, ob es eine neue Version gibt. Ist eine verfügbar, erscheint ein Hinweis
mit den Änderungen. Ein Klick auf **„Jetzt updaten“** lädt sie herunter, installiert sie und startet neu.
Alle Profile und Einstellungen bleiben dabei erhalten.

## Funktionen

- **Kundenprofile:** Name, Beschreibung, Quellordner (wo die Dateien liegen) und Zielordner (wo die
  Reports landen). Eingerichtet wird jedes Profil in fünf Schritten.
- **Automatische Dateierkennung:** Einmal Beispieldateien hineinlegen, danach findet das Programm die
  Dateien des Kunden jeden Monat selbst. Gibt es mehrere passende Dateien, wählst du aus.
- **Eigene Reports pro Kunde:** Mit einer eigenen `.vrsettings`- und `.vrdesign`-Datei lässt sich ein
  völlig anderer Report erstellen, auch mit mehreren PDFs oder einer zusätzlichen Excel-Tabelle.
- **Multi-Export:** mehrere Profile auf einmal erstellen, mit eigener Quelle und einem Unterordner pro Profil.
- **Hinweise und Warnungen**, wenn etwas merkwürdig ist, zum Beispiel:
  - Dateien aus unterschiedlichen Monaten
  - eine Datei ist noch in Excel geöffnet
  - deutlich weniger Datensätze als sonst
- **Report-Verlauf**, dazu **Export und Import** aller Einstellungen, etwa für einen neuen PC.

## Wo liegen meine Daten?

| Was | Ordner |
|---|---|
| Profile, Einstellungen, Verlauf | `%APPDATA%\VIOCON Report Tool (Profiles)` |
| Eingerichtetes Programm | `%LOCALAPPDATA%\VIOCON Report Tool (Profiles)\runtime` |
