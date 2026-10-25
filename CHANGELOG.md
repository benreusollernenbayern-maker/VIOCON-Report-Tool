# Changelog

Alle Änderungen am VIOCON Report Tool (Profiles). Die neueste Version steht oben.

## [1.0.0] – 25.10.2026

Erste Version der neuen Profil-Plattform. Die Report-Technik (Dateierkennung, Excel/Rechnung-Abgleich,
LIS- und Flotten-Report) ist unverändert aus Version 3.2 übernommen.

### Neu
- **Kundenprofile** mit Name, Beschreibung, Quell- und Zielordner, eingerichtet über einen Assistenten in fünf Schritten.
- **Eigene Report-Dateien pro Profil:** `.vrsettings` legt fest, was erstellt wird, `.vrdesign` legt fest,
  wie es aussieht. Beide enthalten vollständigen Python-Code. Ohne eigene Datei gilt der Standard.
- **Dateierkennung per Fingerabdruck:** Das Programm lernt aus Beispieldateien, wie die Dateien eines
  Kunden aussehen, und findet sie im Quellordner wieder. Dateien anderer Kunden im selben Ordner werden
  aussortiert.
- **Auswahl bei mehreren passenden Dateien.** Die neueste ist vorausgewählt.
- **Multi-Export:** mehrere Profile in einem Durchgang, gespeichert oder temporär. Pro Profil lassen sich
  eine eigene Quelle und ein Unterordner im Ziel festlegen.
- **Hinweise, Warnungen und Fehler** in drei Stufen, unter anderem:
  - unterschiedliche Monate in den Dateien
  - in Excel geöffnete Dateien
  - auffällig wenige Datensätze
  - Kunde passt nicht zum Profil
  - Report für diesen Monat existiert schon
  - Fehler in Profil-Dateien, mit Zeilennummer
- **Report-Verlauf** mit Suche und Filter. „Letzte Reports“ auf der Startseite.
- **Export und Import** aller Einstellungen als Ordner. Vor jedem Import wird automatisch gesichert.
- **Updates über GitHub Releases** mit Ladebalken in der App. Die Einstellungen bleiben dabei erhalten.
- **Schneller Start trotz einzelner EXE:** Das Programm wird einmal pro Version eingerichtet.
  Danach erscheint das Intro nach ca. 1 s statt nach 6–7 s.
- **Selbsttest der EXE** vor jeder Veröffentlichung, damit keine defekte Version ausgeliefert wird.
- **Komplett neue Oberfläche:**
  - Dark Mode mit dem VIOCON-Schriftzug als Vektorgrafik und eigenem App-Icon
  - Intro-Animation mit echtem Ladefortschritt
- **Lebendige Seitenwechsel:** Die alte Seite fliegt nach oben hinaus, die neue baut sich zusammen wie
  das Intro:
  - Karten setzen sich aus zwei Hälften zusammen
  - Kacheln fallen nacheinander herein
  - Buttons ploppen auf
  - der Schriftzug auf der Startseite setzt sich Stück für Stück zusammen
- **Passt sich dem Arbeitstempo an:** Wer schnell klickt, bekommt kurze, knackige Animationen, wer ruhig
  arbeitet, die ausführlichen.
- **Mehr Rückmeldung beim Drüberfahren und Klicken:**
  - ein Licht folgt dem Mauszeiger über die Karten
  - Profil-Kacheln neigen sich leicht in 3D
  - Klick-Wellen auf Buttons
  - der Haupt-Button wird magnetisch angezogen
  - eine gleitende Markierung in der Seitenleiste
  - ein Glanz auf orangen Buttons
- **Weiche Übergänge** für Dialoge, Auswahllisten und Menüs (auf- und zuklappen, mit runden Ecken),
  dazu gestaffelt erscheinende Listen.
- Beispiel-Vorlage „Standard-Reports + Excel-Tabelle“ und Format-Doku für eigene Report-Dateien.

### Geändert
- Reports werden direkt im Zielordner des Profils gespeichert. Existiert die Datei schon, wählst du
  „Überschreiben“ oder „Beide behalten“.
- Die Report-Erstellung läuft im Hintergrund und nacheinander statt parallel. Das ist stabiler.
