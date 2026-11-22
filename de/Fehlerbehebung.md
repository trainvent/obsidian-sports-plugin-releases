# Fehlerbehebung

## Nächsten Schritt wählen

| Problem | Hier beginnen |
| --- | --- |
| Arbeitsmappe wird nicht heruntergeladen | [Cloud-Links](#cloud-links) |
| Werte oder Einheiten fehlen | [Import prüfen](#import-prüfen) |
| Automatische Aktualisierung lief nicht | [Synchronisierungszeitpunkte](#synchronisierungszeitpunkte) |
| Notizen fehlen oder melden Konflikte | [Notizen und Wiederherstellung](#notizen-und-wiederherstellung) |
| Uhr- oder Kalenderaktualisierung schlägt fehl | [Verbindungsprobleme](#verbindungsprobleme) |

## Cloud-Links

Verwende einen HTTPS-Link direkt zur XLSX- oder ODS-Datei. Nextcloud-Freigabelinks
wie `https://cloud.example/s/SHARE_TOKEN` funktionieren; Sports ergänzt `/download` automatisch.
Der Link muss Downloads ohne Anmeldung oder Passwort erlauben. Ordnerfreigaben,
Adressen von Tabellen-Editoren, lokale Pfade und verschlüsselte Arbeitsmappen werden nicht unterstützt.
Downloads sind auf **5 MB** und **30 Sekunden** begrenzt; Weiterleitungen sind nur
auf denselben HTTPS-Server erlaubt.

## Synchronisierungszeitpunkte

Die Synchronisierung beim Start ist aktiviert, das Standardintervall beträgt zehn Minuten. Unter **Quellen → Synchronisieren** wählst du fünf,
zehn oder fünfzehn Minuten, eine Stunde oder **Nur manuell**. Die Synchronisierung beim Start
hat einen eigenen Schalter. Automatische Synchronisierung läuft, solange Obsidian geöffnet ist; geschlossene Apps und
Ruhezustand beenden oder verzögern sie. Garmin und Google Health werden höchstens stündlich automatisch aktualisiert.
Fehlgeschlagene Downloads oder ungültige Importe behalten den bisherigen Datenstand.

## Import prüfen

- Prüfe unter **Quellen → Arbeitsmappe → Blätter** und **Quellen → Zeitplan** die genauen Blattnamen in **Strategie-Blatt**, **Erfassungsblatt** und
  **Wochenplan-Blatt**. Eine leere Zuordnung deaktiviert diesen Import und behält
  bereits importierte Daten und Notizen.
- Berechne Formeln in deiner Tabellenkalkulation neu und speichere. Sports liest gespeicherte
  Ergebnisse und berechnet keine Formeln.
- Prüfe Datumsangaben, unterstützte Überschriften, stabile IDs und Tabellengrenzen anhand der
  [Arbeitsmappen-Anleitung](Arbeitsmappe.md#regeln-der-arbeitsmappe-einhalten). Sports erkennt die deutschen und englischen Standardnamen für Blätter, Abschnitte und Spalten.
- Prüfe die Erledigt-Markierungen anhand der [Erfassung](Erfassung.md). Vorausgefüllte Zielwerte sind
  keine Ergebnisse, und Uhr-Aufzeichnungen markieren Einheiten in Trainingstagebuch nicht als erledigt.
- Ein ungültiger Import behält den bisherigen Datenstand. Behebe den gemeldeten Fehler,
  bevor du dich auf eine neue Aktualisierung verlässt.

## Notizen und Wiederherstellung

Sports erkennt erstellte Abschnitte an versteckten Kommentaren `sports:begin` / `sports:end`.
Behalte diese Markierungen und schreibe Reflexionen außerhalb davon. Sie sind im
Quellmodus sichtbar und in der Leseansicht verborgen. Bearbeitete erstellte Inhalte oder beschädigte
Markierungen führen zu einem Konflikt; andere Notizen werden trotzdem aktualisiert.

Wähle die Maßnahme, die zum Problem passt:

| Situation | Maßnahme |
| --- | --- |
| Notizen aus dem letzten Import aktualisieren | **Notizen aus importierten Daten erstellen** |
| Eine erstellte Notiz wurde gelöscht | **Fehlende Notizen neu erstellen** |
| Ein erstellter Abschnitt wurde bearbeitet | Eigene Änderungen nach außerhalb verschieben, den vorherigen Abschnitt wiederherstellen, dann aktualisieren |
| Erstellte Abschnitte nach anhaltenden Problemen neu aufbauen | **Zwischengespeicherte Daten löschen**, dann **Jetzt synchronisieren** |

Das Zurücksetzen behält Einstellungen und Notizdateien, löscht aber importierte Daten aus Arbeitsmappe, Kalender und Uhren
sowie die gespeicherten Grundlagen der erstellten Abschnitte. Vorhandene Zielnotizen werden
im versteckten Plugin-Speicher gesichert, bevor ihre erstellten Abschnitte
neu aufgebaut werden. Reflexionen außerhalb dieser Abschnitte und andere Eigenschaften bleiben
erhalten. Änderungen innerhalb eines neu aufgebauten Abschnitts bleiben in der Sicherung, nicht in der neuen Ausgabe.

Die Wiederherstellung merkt sich ausstehende Notizen über mehrere Aktualisierungen hinweg, auch Tagesnotizen
mit Uhr-Daten und ältere Wochennotizen, die nach der Aktualisierung der Arbeitsmappe zurückkommen. Du musst
nicht erneut zurücksetzen, nur weil eine Quelle später zurückkommt. Fehlende oder beschädigte Markierungen
müssen weiterhin repariert werden; das Zurücksetzen umgeht diese Prüfungen nicht. Ergebnisse, die weder in
der Arbeitsmappe noch in den Uhr-Quellen stehen, lassen sich durch Synchronisieren nicht wiederherstellen.

Sicherungen sind Wiederherstellungskopien, keine aktiven Notizen und keine Synchronisierungsquelle. Die normale Synchronisierung
erstellt keine. Es werden höchstens 10 Kopien behalten; ist der Speicher voll, ersetzt jede neue Kopie
die älteste. Behalte die Dateinamen verwalteter Notizen bei.
Jede Kopie speichert den ursprünglichen Notizpfad, den Zeitpunkt und den vollständigen Inhalt
in der versteckten Plugin-Datei `recovery-backups.json`. Archive abgeschlossener Pläne sind davon getrennt
und laufen nicht ab; siehe [Plan abschließen oder wiederherstellen](Sports-verwenden.md#plan-abschließen-oder-wiederherstellen).

## Verbindungsprobleme

**Garmin:** Eine fehlgeschlagene Aktualisierung behält zwischengespeicherte Aktivitäten mit einer Warnung. Schlägt die Anmeldung
oder die Token-Erneuerung fehl, verbinde neu unter **Einstellungen → Sports → Quellen → Armbanduhr → Garmin → Garmin neu verbinden**.
Die Anbindung nutzt inoffizielle Schnittstellen und kann von Änderungen bei Garmin
oder Anmeldebeschränkungen betroffen sein. **Trennen** entfernt die Token und beendet die Anfragen;
zwischengespeicherte Aktivitäten bleiben, bis du sie löschst. Siehe [Garmin-Aktivitäten synchronisieren](Sports-verwenden.md#garmin-aktivitäten-synchronisieren).

**Kalender:** Prüfe, ob **ICS-Kalender** die aktive Quelle ist und der Link
einen ICS-Feed liefert. Private CalDAV-Adressen mit Anmeldung werden nicht unterstützt. Fehlgeschlagene
Aktualisierungen behalten zwischengespeicherte Termine. Unterstützte Links und den importierten Zeitraum findest du unter [ICS-Kalender verbinden](Sports-verwenden.md#ics-kalender-verbinden).

**Sprache:** Ordner- und Notiznamen folgen der Sprache von Obsidian. Nach einem Sprachwechsel verschiebt Sports
Notizen an ihrem Standardort beim nächsten Beginn. Liegt am neuen Standardort bereits eine Datei, meldet Sports
das Duplikat und lässt beide Dateien unverändert.

## Aktualisierte Anleitungen

Alle vier Anleitungen haben einen erstellten Abschnitt, der mit Sports aktualisiert wird. Schreibe eigene
Notizen darunter, außerhalb der versteckten Markierungen `sports:begin` / `sports:end`. Eine Änderung
innerhalb des erstellten Abschnitts führt zu einem Konflikt, statt überschrieben zu werden.

Wird eine ältere Arbeitsmappen-Anleitung ohne Markierungen zum ersten Mal aktualisiert, speichert Sports ihren genauen
Inhalt in einer verlinkten Notiz **Arbeitsmappe vorher**, bevor die aktuelle Anleitung eingefügt wird.
Deine bisherigen Änderungen bleiben in dieser Kopie. Übernimm eigene Hinweise, die du behalten möchtest,
in den Abschnitt **Meine Notizen** der aktuellen Anleitung.

## Hilfe erhalten

[Melde ein Problem](https://github.com/trainvent/obsidian-sports-plugin-releases/issues)
mit deiner Obsidian- und Sports-Version, der Fehlermeldung und den Schritten zum Nachstellen.
Entferne private Freigabelinks, Zugangsdaten und persönliche Trainingsdaten aus Anhängen.
