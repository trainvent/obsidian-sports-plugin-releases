# Die Sports-Arbeitsmappe anpassen

Mit dieser Anleitung füllst du die mitgelieferte Vorlage aus oder passt eine Arbeitsmappe an. Für die tägliche
Erfassung siehe [Erfassung](Erfassung.md), für Notizen und Anbindungen
[Sports verwenden](Sports-verwenden.md).

Öffne in **Einstellungen → Sports** unter **Arbeitsmappen-Anleitung** die Schaltfläche **Anleitung öffnen** und wähle dann einen
Ausgangspunkt als XLSX oder ODS. Ist Obsidian auf Deutsch eingestellt, lädt Sports die deutschen XLSX-Vorlagen herunter. ODS-Vorlagen sind derzeit auf Englisch:

| Option | Inhalt | Wähle sie, wenn |
| --- | --- | --- |
| **Leere Vorlage XLSX** (`Training-Vorlage.xlsx`) | Sechs Blätter mit einem allgemeinen Trainingstagebuch-Layout aus drei Gruppen; Trainingsdaten und Formeln geleert | du die Arbeitsmappe selbst oder mit einem Chatbot ausfüllen willst |
| **Leere Vorlage ODS** (`Training-Vorlage.ods`) | Alle sechs Blätter, Tabellen und Formatierungen; Trainingsdaten und Formeln geleert | du LibreOffice Calc oder ODS bevorzugst |
| **Beispiel-Arbeitsmappe** (`Training-Beispiel.xlsx` oder `Training-Beispiel.ods`) | Ein ausgefüllter 12-Wochen-Plan mit Bibliothek, Übungsgewichten und Bewertung | du das Format kennenlernen oder ein funktionierendes Beispiel anpassen willst |

Diese Anleitung gilt für beide Dateien. Passe Ziele, Übungen, Zeitplan, Ausrüstung und
Trainingsumfang an, bevor du hochlädst und synchronisierst. Das Beispiel ist keine persönliche
Empfehlung. Sports liest die Arbeitsmappe. Zurück schreibt es nur deine Wochenrückblicke,
und nur in eine bearbeitbare Nextcloud-Freigabe (siehe [Wochenrückblick](#wochenrückblick)).

**Sprache:** Die deutschen XLSX-Vorlagen verwenden deutsche Blattnamen, Abschnittstitel, Spaltenüberschriften und Auswahlwerte.
Sports erkennt die deutschen und die englischen Bezeichnungen unabhängig von der Sprache der Oberfläche.
IDs und ihre Verknüpfungen, Garmin-Typschlüssel und interne Excel-Tabellennamen bleiben stabil.
Alles, was du selbst schreibst – Ziele, Übungen, Titel, Vorgaben, Notizen –, kann in jeder Sprache sein.

## In dieser Anleitung

- [Leere Vorlage ausfüllen](#leere-vorlage-ausfüllen)
- [Arbeitsmappe prüfen](#vor-der-rückgabe-prüfen)
- [Regeln der Arbeitsmappe](#regeln-der-arbeitsmappe-einhalten)
- [Strategie](#strategie), [Wochenplan](#wochenplan), [Trainingstagebuch](#trainingstagebuch) und [Wochenrückblick](#wochenrückblick)
- [Erfassten Verlauf schützen](#erfassten-verlauf-schützen)
- [Bewertung und Übungsbibliothek](#bewertung-und-übungsbibliothek)
- [ODS-Importe](#ods-importe)

## Leere Vorlage ausfüllen

Behalte standardmäßig alle Blätter, Abschnittsbezeichnungen, Überschriftenzeilen, nativen Excel-Tabellen, Formatierungen und
Eingabehilfen. Nicht genutzte **Datenzellen** dürfen leer bleiben. Leere keine ganzen Abschnitte
und entferne keine Überschriften, um eine Funktion abzuschalten. Ändere die Struktur nur, wenn es ausdrücklich gewünscht ist.

1. Trage in **Strategie → Plan** eine stabile Plan-ID, deinen Plannamen, die Zeitzone und
   ein Startdatum an einem Montag ein. Lass Formatversion auf 1. Fülle Ziele, Bausteine und Trainingswochen
   für den vereinbarten Plan aus und behalte ihre IDs und Verknüpfungen. Schreibe die Daten direkt unter
   die jeweilige Überschrift; Leerzeilen beenden Tabellen in Strategie. Behalte die Bezeichnungen in Planübersicht
   und die Fragen in Planrückblick, auch bevor Training erfasst wurde.
2. Trage in **Trainingstagebuch** datierte Einheiten mit gut lesbarem Plan, Titel und geplanten
   Minuten ein. Baustein verweist auf eine ID in Bausteine. Schreibe ausdrückliche Übungsziele wie
   `A) Kniebeuge mit Band: 3 x 10` in Plan. Jede Übung kommt in eine eigene echte Zeile,
   und ihr Gruppenname passt zu ihren Eingabespalten. Zeit, Aufwärmen, Pausen und
   andere Anweisungen stehen in eigenen Zeilen, nie vor oder nach einer Dosierung in derselben
   Zeile. Ein optischer Zeilenumbruch in der Zelle ist kein Zeilenwechsel. Für künftige Ergebnisse lässt du
   die nummerierten Wiederholungs- und Zeitzellen bis zum Training leer; die Zielwerte kommen aus Plan.
   Du kannst Zielwerte auch dort vorausfüllen und sie vor dem Setzen von Einheit erledigt durch die tatsächlichen Werte
   ersetzen. Behandle geplante Zielwerte nie als erledigte Ergebnisse.
   Vergib stabile Einheit-IDs, wenn ein Datum und ein Baustein mehrere Einheiten enthalten.
3. Trage in **Wochenplan** Aktivitäten ein, die als wiederkehrender Stundenplan geführt werden, etwa
   einen wöchentlichen Lauf, den Garmin aufzeichnet. Lege diese Aktivitäten **nicht** zusätzlich als datierte
   Zeilen in Trainingstagebuch an. Trainingstagebuch ist für die getrennten manuellen Workouts, die du dort planst und
   erfasst. Braucht ein Workout manuelle Satzergebnisse, gehört es nach Trainingstagebuch statt nach Wochenplan;
   dass es sich im Kalender wiederholt, macht ein manuelles Workout noch nicht zu einer Zeile in Wochenplan.
   Aktivität schaltet einen Eintrag ein; verwende positive Minuten oder Start- und Endzeit. Erfasst mit
   nennt die tatsächliche Aufzeichnungsquelle (zum Beispiel Garmin), keine Aufforderung,
   Termine nach Trainingstagebuch zu kopieren. Aktiviere **Zeitplan anzeigen**, um den
   Stundenplan neben den getrennten manuellen Workouts zu sehen. Wochenplan liefert keine manuellen
   Ergebnisse, keine Bewertungszeilen in Trainingstagebuch und keine Statistik zu erfasster Leistung.
4. Ergänze in **Übungsbibliothek** Übungen, Einheiten und Ausrüstung. Verwende Minuten für Läufe
   (20 Minuten, nicht 1200 Sekunden) und Sekunden für kurze Halteübungen. Intensitätsbewertungen und
   Zuwachs je kg sind für die Erfassung optional, aber nötig, wenn die vereinbarte
   Bewertungsmethode sie verwendet. Erfinde keinen gemessenen Widerstand für Bänder. Beschreibe
   das Band in den Notizen der Ausrüstung und in der Vorgabe; Gewicht nimmt nur zusätzliche kg auf.
5. Vereinbare die Bewertung, bevor du die Arbeitsmappe ausfüllst. Falls gewünscht, fülle in Bewertung
   Übungsziele, Formeln und Zusammenfassungen je Einheit aus, dazu in Trainingstagebuch die geplante
   Intensität. Datum und Trainingseinheit in Bewertung müssen zu Datum und genauem Titel in Trainingstagebuch passen, nicht zu Baustein.
   Verwende die Berechnungsgrundlage unten nur, wenn diese Methode gewählt wurde;
   kennzeichne vorläufige Bewertungen als Planungsschätzungen. Ist die Bewertung abgelehnt oder offen,
   behalte ihre Struktur und vermerke, dass sie noch nicht eingerichtet ist.
6. Speichere die berechneten Formelergebnisse, prüfe die Arbeitsmappe wie unten beschrieben, lade sie
   hoch, stelle die Blattzuordnung ein und wähle **Jetzt synchronisieren**.

Die leere Vorlage behält sechs Blätter, darunter Satzspalten für A/B/C,
Cal-Intervals, Übungsbibliothek, Bewertung, Planübersicht und Planrückblick. Diese Bezeichnungen
und Berechnungsfelder sind Struktur, keine vorgeschriebenen Übungen. Trainingsdaten und
alle Zellformeln und gespeicherten Ergebnisse sind leer; die Layoutvorgaben bleiben anpassbar.
Trage Daten und Vorgaben direkt ein. Baue nur die Berechnungen, die vereinbart wurden.
Die Formelbeispiele weiter unten beschreiben das ausgefüllte Beispiel, keine Formeln,
die in dieser Vorlage schon stehen. Die ODS-Vorlage hat dasselbe vollständige Layout mit sechs Blättern.
Andere Erfassungslayouts für einen gewünschten Umbau findest du unter [Erfassung](Erfassung.md).

## Optionale Abschnitte und Blätter

Optional heißt, dass ihre **Nutzung** abgelehnt werden kann, nicht dass vorhandene Struktur gelöscht werden soll.
Behalte jeden mitgelieferten Abschnitt und jedes Blatt, solange das Entfernen nicht ausdrücklich gewünscht ist.
Melde, welche Funktionen eingerichtet, ungenutzt oder offen sind. Wähle nicht stillschweigend eine reduzierte Arbeitsmappe.

| Bereich | Wenn ungenutzt | Wenn genutzt |
| --- | --- | --- |
| Ziele und Bausteine | Bezeichnungen und Überschriften behalten; ungenutzte Daten leer lassen | Ziele, Vorgaben und ihre ID-Verknüpfungen ausfüllen |
| Trainingswochen | Bezeichnungen und Überschriften behalten | Wochendaten, Fokus, Ziele und Minuten ausfüllen |
| Planübersicht | Überschriften Kennzahl/Wert und Bezeichnungen behalten | Zusammenfassungsformeln passend zum Plan ergänzen; nicht erfasste Leistung bleibt leer |
| Planrückblick | Überschriften Frage/Antwort und Fragen behalten | Künftige Reflexionen leer lassen; nützliche Entscheidungen festhalten, ohne Ergebnisse zu erfinden |
| Wochenplan | Wochentage und Überschriften behalten; Aktivität nur leer lassen, wenn kein Zeitplan vereinbart ist | Wiederkehrende Aktivitäten eintragen und angeben, wo Ergebnisse erfasst werden |
| Bewertung | Titel, Überschriften, native Tabelle und vorhandenen Einstellungsbereich behalten | Vereinbarte Berechnungen und gespeicherte Ergebnisse ergänzen; keine erfundene tatsächliche Leistung |
| Übungsbibliothek | Überschriften für Übungen, Ausrüstung und Intervalle behalten | Tatsächlich genutzte Referenzen ergänzen, Bewertungen nur, wenn die Bewertung sie braucht |
| Trainingstagebuch Gewicht | Bei Abschnitten ohne Gewicht leer lassen | kg für den Abschnitt eintragen und vor dem Erledigen auf das verwendete Gewicht ändern |

Nicht genutzte Cal-Intervals- oder Satzeingaben können leer bleiben, ohne ihre Überschriften zu löschen.
Ist ein Entfernen oder ein neues Erfassungslayout gewünscht, prüfe vor der Änderung Formeln, Tabellenbereiche,
Gültigkeitsregeln und Importzuordnungen.

### Mit einem Chatbot ausfüllen

Hänge die Arbeitsmappe und diese Anleitung an. Zum Beispiel:

```text
Nutze Arbeitsmappe.md, um die angehängte Arbeitsmappe Training-Vorlage für meine Bedürfnisse auszufüllen.
Frage nach fehlenden Zielen, verfügbarer Zeit, Erfahrung, Ausrüstung und Ausgangsniveau.
Vereinbare wiederkehrende Aktivitäten und ob bzw. wie Intensität und Bewertung berechnet werden.
Behalte alle Blätter, Tabellen, Abschnittsbezeichnungen, Überschriftenzeilen, Formatierungen und
Eingabehilfen. Behalte die vorhandenen Blatt-, Abschnitts- und Spaltennamen sowie die Auswahlwerte bei.
Lass ungenutzte Daten leer; lösche keine Struktur, außer ich verlange es.
Erfinde keine erledigten Workouts, gemessenen Ausgangswerte, Ausrüstungsgewichte oder Ergebnisse.
Lass künftige Ist-Werte leer. Berechne und speichere alle Formeln, die du ergänzt.
Prüfe die gesamte Arbeitsmappe gegen die ursprüngliche Vorlage, auch ungenutzte Bereiche.
Gib die Arbeitsmappe mit einer kurzen Liste der eingerichteten und ungenutzten Funktionen,
Annahmen und fehlenden Angaben zurück. Bezeichne den Plan nicht als fertig, solange
gewünschte Funktionen fehlen.
```

### Vor der Rückgabe prüfen

Vergleiche jedes mitgelieferte Blatt mit dem Original, einschließlich aller Abschnitte in Strategie,
der Überschriften und Tabellen in Bewertung, der Abschnitte in Übungsbibliothek und der Weight-Felder in Trainingstagebuch. Behalte native Excel-Tabellen
und ihre Überschriftenbereiche, nicht nur den sichtbaren Text. Schreibe unter die Überschriften;
der erste Eintrag in Ausrüstung gehört zum Beispiel nach Übungsbibliothek!A62, nicht A61.

Prüfe Datumsangaben und stabile Verweise auf Einheiten und Teile, den vereinbarten wiederkehrenden Zeitplan,
die Ausrüstung und die Abdeckung von geplanter Intensität und Bewertung. Prüfe, dass Aktivitäten aus Wochenplan
nicht zusätzlich als Einheiten in Trainingstagebuch angelegt wurden. Bewertungszusammenfassungen gehören nur zu
Einheiten in Trainingstagebuch; lege keine Trainingstagebuch-Zeilen an, nur um eine wiederkehrende Aktivität zu bewerten. Erfinde
keine Lastzeilen für Bänder und schreibe keine künftigen Rückblicke, nur um leere Zellen zu füllen.
Ist die Bewertung aktiv, prüfe, dass jede datierte Einheit ihre vorgesehene Zusammenfassung hat. Eine
künftige Einheit kann geplante Intensität und Geplante Messwerte haben; ihr Ergebnis und
ihre Leistung bleiben leer, Erfasste Messwerte ist 0. Teste eine erledigte Einheit in einer
Wegwerfkopie: Ergebnisse, Leistung und Abdeckung müssen sich korrekt aktualisieren und speichern lassen.
Prüfe, dass gelöschte Ergebnisse wieder leer werden statt zu einer erfundenen Null.

Bei einem bestehenden Plan bewahrst du außerdem den erfassten Verlauf. Melde fehlende Angaben oder
nicht unterstützte Messgrößen, statt die betroffene Tabelle zu löschen. Ein erfolgreicher Import
allein heißt nicht, dass die gewünschte Arbeitsmappe vollständig ist.

## Das ausgefüllte Beispiel lesen

Das ausgefüllte Beispiel hat drei wöchentliche Kraft- und Bewegungseinheiten und optional
leichtes Techniktraining. Freitags kommen Cal-Intervals dazu. Die Wochen 4 und 8 reduzieren
den Umfang; in Woche 12 wird getestet. Die Felder für Zusatzgewicht beginnen leer.

Der Plan-Text für A/B in Trainingstagebuch verweist auf die Blöcke der jeweiligen Woche in **Strategie!H:I**.
Ändere diese Blöcke, um den gemeinsamen Übungstext zu ändern. Aufwärm- und Pausenhinweise
bleiben in Trainingstagebuch. Diese Textverweise ändern weder Satzeingaben noch Zielwerte in Bewertung.

## Farbschlüssel der Beispiel-Arbeitsmappe

| Farbe | Bedeutung | Verwendung |
| --- | --- | --- |
| Grün, abwechselnde Töne | Eingabezellen | Trainingswerte eintragen oder anpassen. |
| Weiß / hellgrau, abwechselnde Töne | Referenzangaben und Formeln | Den Plan lesen und Formeln erhalten. |
| Neutrales Blaugrau | Überschriften | Strukturelle Spaltennamen behalten; Namen der Übungsgruppen sind anpassbar. |

Eingabe- und Referenzbereiche wechseln die Zeilenfarbe, damit du einer Einheit
über das ganze Blatt folgen kannst. Farben sind Hinweise, keine Zugriffsbeschränkungen.

In **Trainingstagebuch** sind tatsächliche Minuten, Einheit erledigt, die Eingaben der Übungsgruppen, Cal-Intervals, Notizen,
Notizthema und die Anstrengung bearbeitbar. Datum, Plan, Titel und geplante Minuten bleiben
neutral. In **Wochenplan** sind Start- und Endzeit, Aktivität, Erfasst mit und Notizen
grün; die berechnete Spalte Minuten bleibt neutral. Die Zellen `Max. Sätze` und
`Max. Wiederholungen` in Strategie und alle Überschriften bleiben neutral.

## Regeln der Arbeitsmappe einhalten

- Speichere als `.xlsx` oder `.ods`, kleiner als 5 MB. Füge keine Makros oder externen Arbeitsmappen-Verknüpfungen hinzu.
- Behalte die Blätter **Strategie**, **Wochenplan** und **Trainingstagebuch**. Wähle unter **Einstellungen → Sports → Quellen → Arbeitsmappe → Blätter**
  **Strategie** als Strategie-Blatt und **Trainingstagebuch** als Erfassungsblatt.
  Wähle unter **Quellen → Zeitplan** **Wochenplan** als Wochenplan-Blatt. Jede Zuordnung erwartet den genauen
  Blattnamen; lass eine Zuordnung leer, um diesen Import abzuschalten. Ältere Arbeitsmappen mit **Training log** werden weiter unterstützt.
- Abschnittsnamen stehen allein in Spalte A, ihre genauen Überschriften in der nächsten Zeile.
  Ein Abschnittsname allein in Spalte A beginnt die nächste Tabelle. Füge keine Leerzeilen
  innerhalb einer Tabelle in Strategie ein; sie beenden die Tabelle.
- Setze keine dekorativen Titel, Legenden oder Kommentare in die Datentabellen.
  Zusätzliche Spalten in Trainingstagebuch müssen den unten genannten unterstützten Namen folgen.
- Halte Bezeichner eindeutig und nicht leer. Verwende einfache IDs wie `zug-kraft`.
  Behalte Verweise bei, wenn du IDs in einem neuen, noch nicht erfassten Plan änderst.
- Verwende echte Datumswerte im Format `yyyy-mm-dd` oder ausdrücklichen Text `JJJJ-MM-TT`. Verwende
  nichtnegative Zahlen für Minuten. Leer bedeutet nicht erfasst, nicht null.
- Die leere Vorlage hat keine Zellformeln. Ergänzt du Formeln oder passt das
  ausgefüllte Beispiel an, berechne und speichere ihre Ergebnisse, bevor du die
  Datei zurückgibst. Das Plugin liest gespeicherte Werte, keine Formelausdrücke.

## Strategie

Die XLSX- und ODS-Vorlagen und die ausgefüllten Beispiele enthalten diese Abschnitte und Überschriften.
Lass Daten ungenutzter Abschnitte leer; entferne Struktur nur auf Wunsch:

| Abschnitt | Überschriften |
| --- | --- |
| Plan | `Formatversion`, `Plan-ID`, `Planname`, `Zeitzone`, `Startdatum`, `Max. Sätze`, `Max. Wiederholungen` |
| Ziele | `Ziel-ID`, `Titel`, `Zielwert`, `Ausgangswert`, `Prüfung`, `Kategorie`, `Garmin-Typen` |
| Bausteine | `Baustein-ID`, `Version`, `Titel`, `Trainingsvorgabe`, `Ziel-IDs` |
| Trainingswochen | `Woche`, `Beginn`, `Phase`, `Schwerpunkt`, `Wochenziele`, `Steigern wenn`, `Minuten`, `A`, `B` |
| Planübersicht | `Kennzahl`, `Wert` |
| Planrückblick | `Frage`, `Antwort` |

**Plan:** genau eine Zeile. `Formatversion` bleibt `1`. Verwende eine gültige IANA-Zeitzone
wie `Europe/Berlin`. Wähle eine stabile `Plan-ID`; wechselt die ID eines importierten Plans,
muss der zwischengespeicherte Plan gelöscht werden. `Startdatum` bleibt in **E3**. Wähle einen
Montag, bevor du Verlauf erfasst. Vom Plugin erstellte Arbeitsmappen beginnen am nächsten Montag im
lokalen Kalender und verwenden deine lokale Zeitzone.

Die Zellen `Max. Sätze` und `Max. Wiederholungen` im Beispiel beschreiben nur dessen Layout.
Sie legen keine Übungszahl fest, verlangen kein A/B/C/Cal-Intervals und begrenzen keine Satzzahlen.
Eine Änderung dieser Zellen verändert die Größe der Arbeitsmappe nicht.

**Ziele:** Verwende `Aufbauziel` für Fähigkeiten, die du erreichen willst (in den Notizen „Entwicklung“), oder `Erhaltungsziel` für Fähigkeiten,
die du erhalten willst („Erhaltung“). Ausgangswerte und Ergebnisse müssen echte Angaben sein; erfinde keine
Messwerte oder Erfolge.

Jedes Ziel erzeugt eine Notiz `Ziele/<Ziel-ID>.md` im eingestellten Sports-Notizordner.
Halte die ID stabil, damit Rückblicke beim Umbenennen eines Ziels erhalten bleiben. Der
Rückblicksbereich liegt außerhalb des erstellten Abschnitts und bleibt bei jeder Synchronisierung erhalten.
Zielkategorie und Garmin-Typen erscheinen in den Notizeigenschaften;
Ausgangswert, Ziel und Teststandard stehen im Text. Diese Eigenschaften folgen bei der Synchronisierung der
Arbeitsmappe. Ändere ihre Werte in Strategie; andere eigene Eigenschaften bleiben erhalten.

Erfasste Ergebnisse und Garmin-Aktivitäten sind unabhängige Quellen, die jedem Ziel zur Verfügung stehen.
Ergebnisse werden über ID oder Titel des Ziels sowie die Aliase für Muscle-up, HSPU und Pistol zugeordnet,
wenn es genau eine eindeutige Zuordnung gibt. Nicht leere Ergebnisse werden mit Datum, Status der Einheit
und gemeinsamen Notizen übernommen.

- `Garmin-Typen`: kommagetrennte, stabile Garmin-Typschlüssel. `running`
  passt zu Laufen, Bahn-, Trail-, Indoor- und Laufbandlauf sowie unterstützten Laufvarianten.
  `swimming` passt zu Schwimmen im Becken und im Freiwasser. Andere Schlüssel müssen genau passen.
  Aktivitätsnamen wie `Laufen` bestimmen die Zuordnung nicht. Ohne ausdrückliche
  Zuordnung werden Ziele erkannt, die als running oder swimming benannt oder gekennzeichnet sind.
  Eigene Ziele sollten ausdrückliche Typschlüssel verwenden, damit nichts aus dem Zieltext geraten wird.
- Ein Laufziel der Entwicklung kann `Laufen Ergebnis` und `running` haben; ein Schwimmziel
  der Erhaltung `Schwimmen Ergebnis` und `swimming`. Die passende Ergebnisspalte muss in Trainingstagebuch existieren.
- Das Beispiel enthält Schwimmen als Ziel der Erhaltung. Seine Ausgangsroutine ist eine
  Hintergrundangabe, keine erfasste Leistung und keine Änderung an Wochenplan.

**Bausteine:** `Baustein-ID` und `Version` bezeichnen zusammen einen Trainingsblock. Werte in `Baustein`
in Trainingstagebuch verweisen auf diese IDs. In `Ziel-IDs` trennst du Ziel-IDs mit Kommas, zum Beispiel
`muscle-up, pistol`. Jede ID muss in Ziele stehen. Eine ältere Tabelle `Bausteinziele` mit
`Baustein-ID`, `Version`, `Ziel-ID` wird ebenfalls unterstützt.

**Trainingswochen:** Verwende eindeutige positive Wochennummern und eindeutige Montage als Beginn.
Im ausgefüllten Beispiel verweisen die Start-Formeln auf `$E$3`; behalte oder passe sie
an, wenn du dieses Beispiel nutzt. In der formelfreien Vorlage trägst du ausdrückliche Startdaten ein.
`Minuten` ist das Zeitbudget für manuelles Training;
wiederkehrende Aktivitäten sind getrennt. `A` und `B` enthalten die wöchentlichen
Blockvorgaben und speisen die Plan-Formeln in Trainingstagebuch. Benennst du Blöcke um oder ergänzt
weitere Blockspalten, musst du auch die Formeln in Trainingstagebuch anpassen. Das Plugin
importiert derzeit A und B als Wochenvorgaben. Für andere Blöcke steht die vollständige Beschreibung
in Bausteine und im Plan in Trainingstagebuch.

## Wochenplan

`Wochenplan` bleibt in A1, diese Überschriften in Zeile 2:

`Wochentag`, `Startzeit`, `Endzeit`, `Minuten`, `Aktivität`, `Erfasst mit`, `Notizen`.

Verwende Wochentagsnamen (`Montag` bis `Sonntag` oder die englischen Entsprechungen). Weitere Zeilen können den Tag wiederholen oder ihn leer lassen,
dann gilt der vorherige Tag. Eine leere Aktivität erzeugt keinen Termin; leere Reservezeilen
sind erlaubt. Verwende native Tabellenzeiten im Format `hh:mm` oder Text `HH:mm`.
Bei Textzeiten ersetzt du die Formel für die Dauer durch eine positive Zahl.
Die Formel im Beispiel verwendet native Zeiten, lässt unvollständige Zeiten leer und
unterstützt Aktivitäten über Mitternacht. Gleiche Start- und Endzeiten ergeben null und müssen
für eine Aktivität korrigiert werden. Halte die Dauer positiv oder leer; eine fehlende gespeicherte Dauer
kann beim Import aus gültigen Start- und Endzeiten abgeleitet werden.

Wiederkehrende Aktivitäten sind geplante Termine, keine erledigten Einheiten. Sie erscheinen in
der Strategienotiz; aktiviere **Zeitplan anzeigen** für Dashboard und Wochennotizen.
Führe den Wochenplan nur in Wochenplan. Bei älteren Arbeitsmappen mit einem Abschnitt `Wochenplan` in Strategie wählst du
**Strategie** auch als Wochenplan-Blatt. Importiert wird nur der gewählte Zeitplan.

## Trainingstagebuch

Die mitgelieferten Arbeitsmappen verwenden eine Zeile pro manueller Einheit und zwei Überschriftenzeilen.
Das ausgefüllte Beispiel hat die Gruppen A–E, die leere Vorlage beginnt mit A/B/C.
Diese Gruppennamen, Cal-Intervals und fünf nummerierte Satzfelder sind Beispiele, keine vorgeschriebenen
Übungsnamen oder Grenzen. Behalte dieses Layout beim Ausfüllen der Vorlage; für einen Umbau siehe
[Erfassung](Erfassung.md#andere-trainingstagebuch-layouts).

| Feld | Spalten im ausgefüllten Beispiel | Spalten in der leeren Vorlage |
| --- | --- | --- |
| Datum, Baustein, Plan, Titel, Geplante Minuten, Tatsächliche Minuten | A–F | A–F |
| Einheit erledigt | G | G |
| Satzeingaben 1–5 für A/B/C | H–L, N–R, T–X | H–L, N–R, T–X |
| Satzeingaben 1–5 für D/E | Z–AD, AF–AJ | Bei Bedarf Gruppen ergänzen |
| Gewicht je Gruppe | M, S, Y, AE, AK | M, S, Y |
| Runden Cal-Intervals | AL | Z |
| Notizen, Notizthema | AM–AN | AA–AB |
| Geplante Intensität, Anstrengung | AO–AP | AC–AD |

Für XLSX und ODS gelten dieselben Spaltenpositionen. Behalte Gruppenüberschriften und
die Ausrichtung der Unterspalten bei, wenn du Felder ergänzt oder verschiebst.

**Identität einer Einheit:** Datum und Baustein bezeichnen eine Einheit, sofern du keine
ausdrückliche Einheit-ID ergänzt. Verwende eigene stabile IDs für Einheiten mit gleichem Datum und
Baustein. Baustein verweist auf eine `Baustein-ID` in den Bausteine von Strategie; nutze Bausteinversion, wenn diese ID
mehrere Versionen hat. Ein leerer Baustein oder `empty` bedeutet keinen verknüpften Strategieteil.

**Plan:** Jede Übung steht in einer eigenen echten Zeile, ihr Gruppenname passt zu
den Eingabespalten. Trainingseinheit Baustein A/B und die Übungsgruppen A–E sind getrennte Bezeichnungen.
Aufwärmen, Tempo, Pausen und andere Anweisungen stehen in eigenen Zeilen:

```text
18:00; 5 Minuten aufwärmen.
A) Kniebeuge mit Band: 3 x 10
B) Vorgebeugtes Rudern mit Band: 3 x 10
C) Brustpresse mit Band: 3 x 10
60 Sekunden Pause zwischen den Sätzen.
```

Ein optischer Umbruch ist kein Zeilenwechsel. Prüfe, dass jede Vorgabe im Vergleich die
gewünschte Gruppe, Satzzahl, Einheit und den Zielwert ergibt. Für Zeiten erkennt Sports `s`, `Sek.`, `Sekunden`, `min` und `Minuten`,
für Runden `Runden`. Die leere Vorlage hat keine automatischen Daten oder Vorgaben; trage sie direkt ein oder baue
Formeln für deinen eigenen Plan.

**Erledigt-Status:** Die mitgelieferten Dateien verwenden Einheit erledigt und haben keine Spalte Status.
Andere Layouts können Status verwenden: `Geplant`, `Begonnen`, `Abgeschlossen`, `Ausgelassen`
oder `Abgesagt`. Erledigt-Markierungen je Übung erfassen Übungsergebnisse, ohne die
Einheit zu erledigen. Ohne ausdrückliches Erledigt gelten erfasste Ergebnisse als
`Begonnen`. Erfassungsregeln und die Ziele von Notizthema stehen unter
[Erfassung](Erfassung.md#eine-einheit-in-der-mitgelieferten-arbeitsmappe-erfassen).

## Wochenrückblick

Das Blatt **Wochenrückblick** enthält eine Zeile pro Woche mit deinem Wochenrückblick.
**Wochenbeginn** ist der Montag der Woche. Die übrigen Spalten entsprechen den Abschnitten
der Wochennotiz: **Was besser wurde**, **Erholung und Wohlbefinden**, **Wiederholen oder
steigern** und **Was ich anpasse**. **Reflektiert** (WAHR oder FALSCH) entspricht der
Eigenschaft `reviewed` der Notiz, die das Dashboard als reflektiert anzeigt. Jeder Stichpunkt der Notiz ist eine Zeile in der Zelle. Nur die Rückblick-Spalten
und **Reflektiert** sind grüne Eingabezellen.

Im Beispiel sind **Wochenbeginn**, **Programmwoche** und **Phase** Formeln, die auf
**Strategie → Trainingswochen** verweisen; das Blatt folgt also deinem Startdatum. In der
leeren Vorlage sind diese Zellen zunächst leer; Sports füllt sie bei der ersten
Synchronisierung aus deinen Trainingswochen.

Sports hält das Blatt und deine Wochennotizen gleich:

- Ein Rückblick in der Notiz erscheint im Blatt und umgekehrt. Synchronisiert werden nur Wochen,
  die das Blatt enthält oder die Strategie plant.
- Eine Zeile für eine Woche ohne Notiz legt die Wochennotiz an.
- Löschst du einen Rückblick auf einer Seite oder änderst du denselben Abschnitt vor der
  nächsten Synchronisierung auf beiden Seiten unterschiedlich, ändert Sports keine Seite. Es
  zeigt diese Rückblicke mit beiden Fassungen, und du wählst für alle **Notizen behalten**
  oder **Arbeitsmappe behalten**.

Zum Schreiben ins Blatt braucht Sports einen Nextcloud-Freigabelink, der Bearbeiten erlaubt.
Bei einer passwortgeschützten Freigabe trage das Passwort unter **Einstellungen → Sports →
Quellen → Arbeitsmappe → Freigabe-Passwort** ein. Sports ändert nur dieses Blatt und prüft den
Rest der Datei vor dem Hochladen. Solange die Datei in Nextcloud Office geöffnet ist, prüft
Sports jede Minute erneut und aktualisiert sie, sobald du sie schließt. Nextcloud behält frühere Versionen der Datei, falls du zurück musst. Andere Links
übernehmen das Blatt nur in deine Notizen. Schreiben funktioniert bisher mit XLSX-Arbeitsmappen; ODS-Arbeitsmappen übernehmen das Blatt nur in deine Notizen.
Sports schreibt nur die Rückblick-Zellen, füllt leere Bezugszellen und ergänzt nur Zeilen für
Trainingswochen der Strategie, die noch fehlen. Rückblicke anderer Wochen bleiben in deinen Notizen.
Formeln und die Reihenfolge bestehender Zeilen ändert es nie.

Für eine bestehende Arbeitsmappe füge ein Blatt **Wochenrückblick** mit den obigen
Spaltentiteln in einer Zeile hinzu. Unter **Wochenrückblick-Blatt** kannst du einen anderen
Namen wählen oder das Feld leeren, um die Synchronisierung auszuschalten.

## Erfassten Verlauf schützen

Verschiebe nie das Startdatum, ändere nie die Identität einer Einheit und schreibe erledigtes Training nicht um,
wenn du künftige Wochen anpasst. Behalte erledigte Zeilen, Daten, IDs, Ergebnisse und Teilversionen.
Hat ein Teil erledigte Einheiten, behalte dessen Definition und lege für künftige Einheiten eine
neue Version an. Behalte die alte Version und wähle die Versionen in Trainingstagebuch.
Das Plugin lehnt Änderungen an verknüpften Teildefinitionen und Daten ab, die es als
erledigten Verlauf erkennt, und behält fehlende erledigte Einheiten. Stabile, ausdrückliche
Trainingseinheit IDs machen diese Prüfungen zuverlässiger.

Schreibe Reflexionen in Obsidian außerhalb der erstellten Abschnitte. Die Synchronisierung schützt diese
Abschnitte vor versehentlichen Änderungen; Pläne änderst du in der Arbeitsmappe.

## Bewertung und Übungsbibliothek

Wie diese Werte dargestellt werden, erklärt [Trainingsdiagramme](Sports-verwenden.md#trainingsdiagramme).

Das Beispiel enthält ein Formelblatt **Bewertung**. Behalte die drei Importzuordnungen
auf Strategie, Trainingstagebuch und Wochenplan. Das ausgefüllte Beispiel verwendet eine Bewertungstabelle
für Übungsziele, Ergebnisse, Intensität und Leistung. Bewertung wird zusammen mit Trainingstagebuch
automatisch gelesen; behalte seinen Blattnamen.

**Schlüssel in Bewertung:** Datum und Trainingseinheit müssen zu Datum und genauem **Titel** einer datierten Zeile in Trainingstagebuch
passen. Trainingseinheit ist nicht die Baustein-ID und nicht die Einheit-ID. Wiederhole Datum und Titel
für die Übungszeilen; die Zusammenfassung in P:S steht nur in der ersten Zeile
jeder Einheit. Verschiedene Einheiten am selben Tag brauchen für diese Zuordnung
verschiedene Titel. Geplante Intensität in Trainingstagebuch muss auf den Zusammenfassungswert in Bewertung verweisen.

Ergebnis verweist auf die ausdrücklichen Done- und Ergebnisfelder in Trainingstagebuch. Die Leistung je Übung
ist Ergebnis / Ziel × 100. Die erste Zeile jeder Einheit enthält ihre geplante
Intensität, den Median der Leistung, Erfasste Messwerte und Geplante Messwerte. Die Abdeckung
macht Teilergebnisse sichtbar. Cal-Intervals belegt eine Zeile pro Einheit, bewertet
erledigte Runden und verwendet für die Intensität die gemeinsame Definition aus Übungsbibliothek.

Das Beispiel berechnet die **geplante Intensität** aus Übungsannahmen und geplantem
Umfang, gerundet auf eine Nachkommastelle auf einer Skala von **0–10** (0 bedeutet keine geplante Belastung,
10 die höchste geplante Belastung). Trage optional danach ein **Anstrengung** (1–5) ein,
um festzuhalten, wie anstrengend es sich angefühlt hat, oder lass es leer. Keine der beiden Bewertungen beeinflusst
die Leistungsberechnung. Ein Wert aus Dauer × RPE ist weder nötig noch wird er abgeleitet.
Erweiterst du das Workout-Layout, passe in Bewertung die Verweise auf die Ist-Zellen,
die ausdrücklichen Zielwerte und die Median- und Zählbereiche in Trainingstagebuch für diese Einheit an.
Berechne und speichere die Arbeitsmappe vor dem Synchronisieren neu.

### Übungsbibliothek und Zusatzlast

**Übungsbibliothek** enthält die Referenzdaten. Behalte diesen Blattnamen: Es wird zusammen
mit Strategie oder Trainingstagebuch automatisch importiert.

Behalte Abschnittsbezeichnungen und Überschriftenzeilen; schreibe Einträge darunter. Im
unveränderten XLSX-Layout steht die Abschnittsbezeichnung Ausrüstung in **A60**, die Überschriften in
**A61:D61**, und der erste Ausrüstungseintrag gehört nach **A62:D62**.
Bei Widerstandsbändern lässt du Minimale kg und Maximale kg leer, sofern du keinen sinnvoll
gemessenen Bereich hast. Beschreibe Band und Widerstand in Notizen und nenne es in der
Vorgabe. Gewicht ist für zusätzliche Kilogramm; Bänder brauchen keinen Gewichtswert.
Grundintensität und Zuwachs je kg dürfen leer bleiben, wenn du keine Bewertung nutzt.

| Tabelle | Überschriften |
| --- | --- |
| Übungsauswahl | `Gruppe`, `Übung`, `Einheit`, `Grundintensität (0–10)`, `Zuwachs je kg` |
| Ausrüstung | `Ausrüstung`, `Minimale kg`, `Maximale kg`, `Notizen` |

Das Arsenal in XLSX belegt **Übungsbibliothek!A2:E58**. Einheiten stehen in **C**, die Grundintensität in
**D** und der Zuwachs pro kg in **E**. Der Zuwachs ist ein anpassbarer relativer Faktor:
4 % bedeutet, dass jedes zusätzliche kg die Bewertung der Übung um 4 % ihrer Grundbewertung erhöht.
Die vorgegebenen Werte sind Planungsschätzungen, keine gemessenen physiologischen Effekte.
Zug- und Muscle-up-Übungen beginnen bei 4 %/kg, aufrechte Übergangsübungen mit Band
und Pistol-Varianten bei 3 %/kg, Liegestütze, Kniebeugen und Dips bei 2 %/kg.
Pike-Liegestütze, Handstand/HSPU, Übungen an der niedrigen Stange, Arbeit kopfüber und Mobilität
lassen dieses Feld leer. Ein leerer Wert lässt die Grundintensität unverändert.
Die Werte schreiben keine Gewichtsweste vor: Nur Einträge in Gewicht in Trainingstagebuch fügen geplantes Gewicht hinzu.
Training mit und ohne Gewicht teilt sich denselben Übungseintrag; es gibt keine eigenen
Westen-Varianten. Die Definition von Cal-Intervals liefert ihre eigenen Arbeitssekunden.

**Übungsauswahl:** eine Übung pro Zeile, eindeutig im ganzen Arsenal. Wiederhole die
Gruppe in jeder Zeile oder lass Gruppe leer, um die vorherige Gruppe zu übernehmen. Beginne
mit einer nicht leeren Gruppe. **Setze nie ein Komma oder einen Doppelpunkt in einen Übungsnamen.** Diese
Zeichen trennen Einträge und Vorgaben im Blocktext des Beispiels.
Schreibe `Hoher Zug (Brust zur Stange)`, nicht `Hoher Zug, Brust zur Stange`.
Halte die Dosierung aus dem Namen heraus: hier `Pike-Liegestütz` und im Wochenblock
`Pike-Liegestütz: 3 x 5`. Kommas sind zwischen Übungen in Blockvorgaben erlaubt
und in `Ziel-IDs` als Trenner erforderlich.
Das Arsenal wird als Referenz importiert; es schreibt freie Vorgaben nicht um
und prüft sie nicht. Passenden Text aktualisierst du selbst.
Die ältere Tabelle `Übungen` wird nicht unterstützt.

### Übungsgewichte

Jeder Abschnitt in Trainingstagebuch (**A**, **B**, **C** oder eine eigene Übungsgruppe) kann nach seinen Satzfeldern eine
Unterspalte **Gewicht** haben. Trage Kilogramm ein oder lass sie leer.
Der Wert gilt für jeden Satz dieses Abschnitts; null bedeutet ausdrücklich Körpergewicht.
Ein eigenes Blatt für Lasten gibt es nicht. Behalte **Gewicht** unter seiner Gruppenüberschrift, damit
Sports es der passenden Übung im Plan zuordnen kann.

Das Beispiel hat keine voreingestellten Zusatzlasten. Cal-Intervals bleibt ohne Gewicht.
Trage das tatsächlich verwendete Gewicht ein, bevor du
**Einheit erledigt** setzt. Bis zum Erledigen erscheinen die kg nur als geplantes Gewicht;
ein erledigter Abschnitt erfasst das eingetragene Gewicht zusammen mit seinen Satzergebnissen.

Bewertung liest Gewicht direkt aus Trainingstagebuch: **M, S, Y, AE, AK** für die Gruppen A–E
im ausgefüllten Beispiel. Übungsbibliothek liefert Übungsbewertungen und den Zuwachs pro kg.

### Einheiten für Dauer

Verwende für Zielwert und Ergebnis dieselbe sichtbare Einheit. Handstand-Gehen verwendet Meter,
zeitbasierte Übungen Sekunden oder Minuten. Zahlen und Eingaben im Uhrzeitformat beschreibt
[Dauer und Last](Erfassung.md#dauer-und-last).

### Formel für lastangepasste Intensität

```text
loaded_intensity_i = MIN(10, base_intensity_i × (1 + planned_kg_i × growth_per_kg_i))
set_weight_i = prescribed_sets_i
circuit_set_weight = rounds × station_count
circuit_intensity = SUM(station_intensity × work_seconds) / SUM(work_seconds)
session_intensity = ROUND(SUM(loaded_intensity_i × set_weight_i)
                          / SUM(set_weight_i), 1)
```

Eine Grundbewertung von 5 mit 2 %/kg wird zum Beispiel **bei 6 kg zu 5,6**. Bleibt Gewicht leer,
sind die geplanten kg 0 und die Grundbewertung bleibt unverändert. Bewertungen werden vor dem
Mitteln auf 10 begrenzt. Das ausgefüllte Beispiel gewichtet die Bewertungen nach vorgegebenen Sätzen. Wiederholungen, Meter
und Sekunden bleiben getrennte Zielwerte; keiner wird in eine andere Einheit umgerechnet.

In der Bewertungstabelle stehen in **C:F** Übung, Einheit, Sätze und Menge pro Satz,
in **G:I** Ziel, Ergebnis und Übungsleistung, in **J:M** Grundintensität,
geplante kg, Zuwachs und lastangepasste Intensität. **N:O** enthalten Satzgewichtung und Beitrag.
**P:S** enthalten die Zusammenfassung der Einheit in ihrer ersten Zeile. Zum Beispiel:

```excel
=MIN(10,J5*(1+K5*L5))
```

**Bewertung!P3** fasst die Zeilen der Einheit zusammen; **Trainingstagebuch!AO3** verweist auf dieses Ergebnis:

```excel
=IF(COUNT(O3:O7)<>COUNT(N3:N7),"",ROUND(SUM(O3:O7)/SUM(N3:N7),1))
```

Eine Änderung des Plantexts ändert Sätze und Mengen in Bewertung nicht. Ändere sie zusammen
mit den Leistungszielen. **Übungsbibliothek!A65:F70** definiert Cal-Intervals einmal:
vier Übungen, jede mit anpassbaren Arbeits- und Pausensekunden. Anfangs sind es
30 Sekunden Arbeit + 20 Sekunden Pause. Die Intensität einer Station wird nach ihrem Anteil an der
Arbeitszeit gewichtet; die geplanten Runden vervielfachen die Zahl der Stationssätze. Pausen zählen nicht.
Fehlende oder doppelte Übungszuordnungen und ungültige Eingaben
lassen die Intensität offen. Leistung aus Wiederholungen und Zeit sowie gefühlte Anstrengung bleiben
getrennt; zusätzliche kg erscheinen als eigene Vergleichsgröße und werden nicht zu Wiederholungen addiert.

### Rückblick am Planende

Unten in Strategie zeigt **Planübersicht** geplante und erledigte Einheiten,
erfasste manuelle Minuten und den Median der erfassten Leistung. **Planrückblick** hat sechs
kurze Antwortfelder für Zielfortschritt, was funktioniert hat, Änderungen, Erholung, Beobachtungen zur Last
und den nächsten Plan. Als erledigt zählt **Einheit erledigt** in den mitgelieferten Dateien oder ein ausdrücklicher **Status** in anderen
Layouts. Tracker-Importe und Erledigt-Markierungen je Übung erledigen keine Einheit.

## ODS-Importe

ODS verwendet dieselben Blattzuordnungen und Erfassungslayouts wie XLSX. Speichere in LibreOffice
Calc eine Kopie als `.ods`, berechne neu und speichere, und aktualisiere dann den Cloud-Link
zur Arbeitsmappe im Plugin. Sports importiert gespeicherte Zellwerte einschließlich Formelergebnissen;
Formeln werden nicht ausgewertet. Prüfe berechnete Intensität und Done-Werte nach der
Umwandlung. Wähle in den Einstellungen **XLSX herunterladen** oder **ODS herunterladen**. Beide beginnen am nächsten Montag.
Beide Ausgangspunkte verwenden für **Einheit erledigt** eine manuelle Auswahl WAHR/FALSCH. Im
ausgefüllten Beispiel verwenden Notizthema, Weight-Felder, Übungsbibliothek, Bewertung und Cal-Intervals in
beiden Formaten dieselbe Struktur. Beide leeren Vorlagen behalten alle sechs Blätter
mit ihren Tabellen, Formatierungen und Eingabehilfen; Trainingsdaten und Zellformeln sind geleert.
