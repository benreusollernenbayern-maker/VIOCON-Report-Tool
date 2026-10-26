# Changelog

Alle Änderungen am VIOCON Report Tool (Profiles). Die neueste Version steht oben.

## [1.1.0] – 26.10.2026

### Neu
- **Monatsordner:** Unter Einstellungen einmal festlegen, wo die Dateien jeden Monat liegen
  (z. B. `H:\reports` und `H:\invoices` mit den Unterordnern `2026-09`, `2026-10` …). Ein Profil merkt sich
  nur noch seine Team-Ordner (z. B. `Muster_Fleet` und `Muster_LIS`) – der Monat wechselt automatisch.
  Ordner, die mit `charge_home` beginnen, werden ignoriert (einstellbar).
  - Beliebig viele Monatsordner, z. B. je einer für LIS-Dateien, Flotten-Dateien und Rechnungen. Mehrere
    lassen sich auf einmal hineinziehen; wird ein übergeordneter Ordner (z. B. `H:\`) gewählt, werden alle
    Monatsordner darin übernommen.
  - Jeder Monatsordner zeigt, was darin erkannt wurde (LIS-Dateien, Flotten-Dateien, Rechnungen) und den
    neuesten Monat, und lässt sich nachträglich ändern oder entfernen – die Profile bleiben dabei erhalten.
  - **Dateiarten je Ordner:** Pro Monatsordner ankreuzen, welche Dateien daraus genommen werden (z. B. aus
    `H:\invoices` nur Gutschriften und Rechnungen). Beim Hinzufügen wird das aus dem Inhalt vorgeschlagen.
- **Mehrere feste Ordner pro Profil** (auch zusammen mit Monatsordnern), jeweils mit eigener Auswahl der
  Dateiarten, ändern und entfernen.
- **Report erstellen:** Der neueste Monat wird automatisch genommen, die verwendeten Ordner werden angezeigt.
  Darunter lässt sich ein anderer Monat auswählen – die passenden Dateien werden selbst gefunden.
- **Profile einfacher anlegen:** Im Assistenten die Team-Ordner aus einer Suchliste wählen (der passende
  Fleet-/LIS-Partner wird mit ausgewählt), die Beispieldateien kommen automatisch aus dem neuesten Monat.
- **Profile aus Monatsordnern anlegen:** Für alle Team-Ordner ohne Profil auf einmal – Fleet und LIS derselben
  Firma werden zu einem Profil zusammengefasst.
- **Multi-Export „Alle Profile“:** enthält immer alle Profile, auch später angelegte. Beim Ausführen werden
  Profile ohne Dateien im Monat hervorgehoben und neue Team-Ordner ohne Profil angezeigt (mit „Profile anlegen“).
- **Multi-Export, erweiterte Optionen:** Monat für alle (neuester, Vormonat oder ein bestimmter Monat) und pro
  Profil ein eigener Monat sowie eigene Settings- und Design-Dateien nur für diesen Multi-Export.
- **Eine Design-Datei je Ausgabe:** z. B. eigene Design-Dateien für den LIS-Report, den Flotten-Report oder eine
  Zusatz-Tabelle aus der Settings-Datei.
- **Suche** nach Kunden auf der Startseite und unter „Kunden“.
- Hinweis beim Start, wenn ein neuer Monat dazugekommen ist.
- **Alles wieder herausnehmen:**
  - Monatsordner auch beim Bearbeiten eines Profils verwalten (hinzufügen, ändern, entfernen).
  - Gewählte Team-Ordner, feste Ordner und einzelne gelernte Dateiarten lassen sich im Assistenten entfernen.
  - Im Multi-Export mit „Alle Profile“ einzelne Profile herausnehmen; die Auswahl „Was wird erstellt“ eines
    Profils lässt sich auf „wie im Profil“ zurücksetzen.
  - Mehrere Profile auf einmal löschen (Kunden → Papierkorb).
  - Ordnerfelder lassen sich mit × leeren.

### Geändert
- Assistent: Schritt „Ordner“ kommt jetzt vor „Beispieldateien“.
- Dateiname: Der Teil nach der Belegnummer ist der Monta-Teamname aus dem Export, z. B.
  `Gutschrift_3508-2026-12345_Muster-LIS_2026-09.pdf`. Fehlt die Nummer in der PDF, wird sie aus dem
  PDF-Namen genommen.
- Export/Import der Einstellungen enthält jetzt auch die Monatsordner und die eigenen Dateien in Multi-Exporten.

### Behoben
- Gespeicherte Multi-Exporte ließen sich nicht mehr bearbeiten (das Fenster ging sofort wieder zu).
- Exporte mit dem Monat am Ende im Format `2026-09`: Der Monat stand im Kundennamen und im Dateinamen.
- Gutschrift und Rechnung (beide nur `<Nummer>.pdf`) wurden bei Profilen mit LIS und Flotte nicht sicher
  unterschieden – jetzt über den Team-Ordner.

## [1.0.1] – 25.10.2026

### Neu
- **Auswahl, was erstellt wird:** Pro Kundenprofil und pro Eintrag im Multi-Export lässt sich festlegen,
  welche der möglichen Dateien entstehen, z. B. nur LIS, nur Flotte oder beides ohne die Zusatz-Tabelle.
  Angeboten wird, was die Settings-Datei vorsieht und was die Beispieldateien hergeben. Geändert wird die
  Auswahl über „Auswahl bearbeiten“ bzw. „Bearbeiten“.
- **Einstellung „Auswahl beim Erstellen“:** Die Abfrage kommt bei jedem Klick auf „Erstellen“ oder nur
  beim ersten Mal. Beim Multi-Export gibt es zusätzlich „Nur über ‚Bearbeiten‘“. Das ist dort der Standard.
- Nicht ausgewählte Dateien stehen in der Report-Ansicht ausgegraut als „nicht ausgewählt“.

### Geändert
- **Neue Dateinamen** der Reports:
  - `Gutschrift_<Nr>_<Kunde>-LIS_<JJJJ-MM>.pdf`, z. B. `Gutschrift_3508-2026-15339_Voelkl-Einrichter-LIS_2026-05.pdf`
  - `Rechnung_<Nr>_<Kunde>-Fleet_<JJJJ-MM>.pdf`, z. B. `Rechnung_3508-2026-36144_Strama-Fleet_2026-07.pdf`

  Die Nummer stammt aus der LIS-Gutschrift bzw. der Monta-Rechnung. Fehlt die PDF, entfällt die Nummer
  im Namen, und ein Hinweis erscheint.
- Seitenwechsel etwas langsamer und weicher. Alte und neue Seite gehen fließend ineinander über.
- Elemente, die sich aus einer oberen und einer unteren Hälfte zusammensetzen, gleiten jetzt sanft
  zusammen statt hart einzurasten. Das gilt auch für Dialoge.
- Das Einrichtungsfenster beim ersten Start einer neuen Version sieht jetzt aus wie das Intro und erscheint
  an derselben Stelle in der Bildschirmmitte. Das Intro blendet sich nahtlos darüber ein.

### Behoben
- Kurzes Aufblitzen der fertigen Seite beim Seitenwechsel.
- Das Einrichtungsfenster erschien oft klein oben links.
- Die Schaltflächen „Abbrechen“ und „Später“ in einigen Dialogen hatten keine Wirkung.
- Nach einem Import konnten Änderungen auf der Einstellungsseite den importierten Stand überschreiben.

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
