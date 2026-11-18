# Training erfassen

Nutze zuerst das mitgelieferte Trainingstagebuch-Layout. Passe es nur an, wenn sich die Art ändern soll,
wie du Training erfasst. Für die Einrichtung und die Bedeutung der Blätter siehe die
[Arbeitsmappen-Anleitung](Arbeitsmappe.md).

Die deutschen XLSX-Vorlagen verwenden deutsche Blatt-, Abschnitts- und Spaltennamen. Sports erkennt auch die englischen Entsprechungen.
Inhalte wie Übungen, Titel, Vorgaben und Notizen schreibst du in jeder Sprache.

## Eine Einheit in der mitgelieferten Arbeitsmappe erfassen

1. Öffne die Zeile der Einheit in **Trainingstagebuch**. Ersetze nach dem Training die vorausgefüllten Satzwerte
   durch das, was du gemacht hast, und leere nicht genutzte Sätze.
2. Trage die tatsächlichen Minuten und eventuelle Notizen ein. Hast du mit Zusatzgewicht trainiert, ändere
   **Gewicht** des Abschnitts auf die tatsächlich verwendeten Kilogramm; leer bedeutet keine
   Gewichtsangabe, null bedeutet ausdrücklich Körpergewicht.
3. Wähle WAHR unter **Einheit erledigt**. FALSCH oder leer lässt die Satzeingaben
   unerfasst. Positive Runden bei Cal-Intervals werden mit Einheit erledigt erfasst;
   null oder leer bedeutet, dass der Zirkel nicht gemacht wurde.
4. Trage optional **Anstrengung** ein, von 1 (leicht) bis 5 (sehr schwer).
5. Berechne neu, falls deine Arbeitsmappe Formeln verwendet, speichere die Cloud-Datei und wähle dann
   in Sports **Jetzt synchronisieren**.

Einheit erledigt markiert in den mitgelieferten Dateien die ganze Einheit als erledigt. Eine eigene
Status-Spalte gibt es dort nicht. Gewicht gilt für jeden Satz im Übungsabschnitt;
vor dem Erledigen ist es das geplante Gewicht, danach das erfasste.

Wiederkehrende Aktivitäten gehören in Wochenplan. Ein Kalendertermin oder eine Uhr-Aufzeichnung
erledigt keine manuelle Einheit in Trainingstagebuch. Künftige Ergebnisse und unbekannte Messwerte bleiben
leer; null ist ein erfasster Wert.

### Notizen und Zeitangaben

Mit **Notizthema** ordnest du eine Reflexion zu. Allgemein bleibt bei der Einheit;
Muscle-up, HSPU und Pistol erscheinen zusätzlich auf der gewählten Zielseite. Fertigkeiten A,
Fertigkeiten B, T, Schwimmen, Laufen und Cal-Intervals führen zur passenden
Routine. Wähle einen der vorgegebenen Werte; die englischen Entsprechungen werden ebenfalls erkannt. Notizen sind Kommentare, keine gemessenen Zielergebnisse.

Für zeitbasierte Satzeingaben verwendest du eine Zahl in der Einheit der Vorgabe oder eine Dauer im Uhrzeitformat.
Native Tabellenzeiten können als `mm:ss` erscheinen; gib `0:00:15` für
fünfzehn Sekunden ein, damit die Tabelle es nicht als fünfzehn Minuten deutet.

## Ergebnis ansehen

Wähle ein Datum im Dashboard oder öffne die datierte Tagesnotiz für Sätze, Notizen und die Abdeckung
der Einheit. Für deinen Rückblick nutzt du die Wochennotiz, für Trends die **Statistik**.
Die vollständige Übersicht der Notizen steht unter [Sports verwenden](Sports-verwenden.md#deine-notizen), die Skalen der Diagramme unter
[Trainingsdiagramme](Sports-verwenden.md#trainingsdiagramme).

Nutzt du das Blatt Bewertung aus dem Beispiel, misst die Leistung, wie gut Zielwerte erreicht wurden;
auch Teilergebnisse können eine Bewertung ergeben, prüfe daher **Erfasste Messwerte / Planned
metrics**. Die gefühlte Anstrengung ändert die Leistung nicht. Formeln und Berechnungen
sind unter [Bewertung und Übungsbibliothek](Arbeitsmappe.md#bewertung-und-übungsbibliothek) beschrieben.

## Andere Trainingstagebuch-Layouts

Das ausgefüllte Beispiel verwendet die Übungsgruppen A–E, die leere Vorlage beginnt mit A/B/C.
Gruppennamen, Cal-Intervals und fünf Satzspalten sind Beispiele, keine vorgeschriebenen Übungsnamen
oder Grenzen. Das Plugin liest das Blatt, das unter **Erfassungsblatt** gewählt ist.
Behalte beim Ausfüllen das mitgelieferte Layout bei. Beim Umbau bewahrst du Session-IDs
und erfassten Verlauf und passt abhängige Formeln, Tabellen und Gültigkeitsregeln an.

### Eine Zeile pro Einheit anpassen

Benenne Übungsgruppen um, füge welche hinzu oder entferne sie, oder erweitere die Satzspalten. Eine gruppierte
Überschrift kann `Squat`, `D`, `Intervals` oder jeder andere Name sein, über **Erledigt** und
**1, 2, 3, …** (oder **Runden**). Strukturelle Spalten behalten ihre Namen.
Fasse keine zwei Übungsgruppen unter demselben Namen zusammen.

Flache Entsprechungen sind `Squat erledigt`, `Squat 1 Ergebnis`, `Squat 2 Ergebnis` usw.
`Circuit erledigt` mit `Circuit Runden Ergebnis` funktioniert ebenfalls. Nummerierte Eingaben und Runden
zählen nur mit der zugehörigen Erledigt-Markierung.

Für ein flaches Layout sind die Überschriften `Datum`, `Baustein` und `Plan` erforderlich.
Optional sind `Titel`, `Geplante Minuten`, `Tatsächliche Minuten`, `Status`,
`Notizen`, `Einheit-ID`, `Bausteinversion` und `Sportart`. Eigene Messspalten enden
auf ` Ergebnis`; Erledigt-Spalten enden auf ` erledigt` und enthalten WAHR, FALSCH oder
nichts. Verwende `Reps Ergebnis` statt einer beliebigen Überschrift `Reps`. Gruppierte Überschriften
sind die Ausnahme: Ihre Unterspalten werden als `<Gruppe> 1 Ergebnis` usw. importiert.

Für Zahlenvergleiche nennst du den Gruppennamen in Plan, eine Vorgabe pro Zeile:

```text
Squat) Kniebeuge: 6 x 5
Carry) Farmer's Walk: 4 x 30 m
Hold) Wandhalten: 3 x 20 s
Circuit: 4 Runden
```

Gruppennamen, Übungsnamen, Einheiten und Satzzahlen sind frei wählbar. Für Zeiten erkennt Sports `s`, `Sek.`, `Sekunden`, `min` und `Minuten`,
für Runden `Runden` oder `Runden`. Zusammengesetzte Anweisungen bleiben als Text lesbar. Für wechselnde
Zielwerte je Satz oder mehrere Messgrößen ist das zeilenbasierte Format besser, statt sie in Fließtext zu kodieren.
Die Metadaten `Max. Sätze` und `Max. Wiederholungen` im Beispiel sind beschreibend; sie begrenzen den Import nicht
und verändern die Größe der Arbeitsmappe nicht.

### Eine Zeile pro Satz oder Messwert

Wähle dieses Format für wechselnde Zielwerte je Satz oder mehrere Messgrößen pro Satz.

Verwende genau diese Überschriften. Weitere Sätze und Übungen ergeben neue Zeilen, keine neuen Spalten.

| Datum | Einheit-ID | Übung | Satz | Einheit | Soll | Ergebnis | Erledigt |
| --- | --- | --- | --- | --- | --- | --- | --- |
| JJJJ-MM-TT | kraft-1 | Kniebeuge | 1 | Wdh. | 8 | 8 | WAHR |
| JJJJ-MM-TT | kraft-1 | Kniebeuge | 1 | kg | 60 | 55 | WAHR |
| JJJJ-MM-TT | kraft-1 | Kniebeuge | 2 | Wdh. | 6 | | FALSCH |
| JJJJ-MM-TT | kraft-1 | Kniebeuge | 2 | kg | 65 | | FALSCH |
| JJJJ-MM-TT | kraft-1 | Farmer's Walk | 1 | m | 30 | 25 | WAHR |
| JJJJ-MM-TT | kraft-1 | Wandhalten | 1 | Sekunden | 00:30 | 00:25 | WAHR |
| JJJJ-MM-TT | intervalle-1 | Laufen Belastung | 1 | Sekunden | 60 | | FALSCH |
| JJJJ-MM-TT | intervalle-1 | Laufen Erholung | 1 | Sekunden | 90 | | FALSCH |

Diese Zeilen sind Beispiele, keine importierten Trainingsleistungen.

- Erforderliche Überschriften: **Datum, Übung, Satz, Einheit, Soll, Ergebnis**. Eine optionale
  **Einheit-ID** unterscheidet Einheiten am selben Tag; halte die IDs stabil.
  Ohne sie ergibt sich die Einheit aus Datum + Baustein, wiederhole Baustein also in jeder Zeile
  der Einheit (oder lass ihn überall leer).
- **Übung** ist ein beliebiger Name. **Satz** ist eine beliebige positive ganze Zahl, nicht auf
  1–5 begrenzt. Zeilen werden nach Satznummer sortiert; Lücken behalten ihre Bezeichnung.
- **Einheit** wird ausdrücklich angegeben und ist frei wählbar: Wdh., Wdh./Bein, Sekunden, Minuten, m, km,
  kg, Runden, RPE, % oder eine andere Messgröße. Zeitangaben erkennt Sports auch als `Sekunden` oder `Minuten`.
  Mehrere Zeilen mit gleicher Übung und gleichem Satz können verschiedene Messgrößen erfassen, etwa Wiederholungen und Last.
  Übung + Einheit + Satz müssen innerhalb einer Einheit eindeutig sein. Jede Einheit bleibt in Tabellen und Diagrammen getrennt.
- Die optionale Spalte **Zusammenfassung** steuert das Diagramm je Übung und Einheit: `Summe` (Standard),
  `Mittelwert`, `Minimum`, `Maximum` oder `Letzter Wert`. Setze sie in allen Zeilen dieser Übung und Einheit gleich.
  Nutze zum Beispiel `Mittelwert` für kg oder RPE, `Maximum` für Höchstlast
  und `Summe` für Umfang oder Zeit. Einzelne Satzwerte bleiben immer sichtbar.
- **Soll** und **Ergebnis** sind unabhängige nichtnegative Zahlen oder leer. Zielwerte
  können sich mit jedem Satz ändern. Ein leeres Soll bedeutet kein Zahlenziel, ein leeres Ergebnis
  nicht erfasst. Null ist ein echter Wert. Textanweisungen gehören in **Plan** oder **Notizen**.
- Zeiteinheiten akzeptieren Zahlen, native Excel-Zeiten, `mm:ss` oder `hh:mm:ss`. Zahlen
  in Minuten werden in Sekunden umgerechnet; Angaben mit Doppelpunkt bedeuten immer eine Dauer, unabhängig von
  der gewählten Zeiteinheit. Andere Einheiten bleiben genau wie benannt (keine Umrechnung von km in m).
- Mit einer Spalte **Erledigt** zählt nur WAHR als Ergebnis. FALSCH und leer sind verschiedene
  unerfasste Zustände. Ohne diese Spalte ist ein nicht leeres Ergebnis ein ausdrückliches Ergebnis.
  Zielwerte allein werden nie zu Leistungen.
- Optionale Felder der Einheit: **Baustein, Bausteinversion, Titel, Sportart, Plan, Status,
  Geplante Minuten, Tatsächliche Minuten, Notizen** und eigene Spalten, die auf ` Ergebnis` enden.
  Setze Baustein und Bausteinversion in der ersten Zeile einer verknüpften Einheit. Andere gemeinsame
  Angaben dürfen einmal stehen oder sich gleichlautend wiederholen. Widersprüchliche Werte werden abgelehnt;
  Notizen aus verschiedenen Zeilen bleiben erhalten. Datum ist in jeder Zeile Pflicht.
- **Plan** ist freier Text. Strukturierte Zielwerte und Ergebnisse speisen die Diagramme, ohne
  Anweisungen auszuwerten. Nutze ihn für Supersätze, Tempo, Pausen, AMRAP/EMOM-Anweisungen,
  Technikhinweise oder die Beschreibung eines Trainingsablaufs.
- Der Status einer Einheit ist unabhängig vom Erledigt-Stand der Sätze. Setze `Abgeschlossen` ausdrücklich,
  wenn es passt. Ohne Status bedeuten erfasste Ergebnisse `Begonnen`.
- Zielmesswerte führst du in eigenen Spalten auf ` Ergebnis` mit genau den Namen,
  die die Zielzuordnung in Strategie verwendet. Sie sind unabhängig von den Satzmessgrößen.

In diesem Format gibt es keine feste Zahl an Übungen, keine Pflicht zu Cal-Intervals und keine Grenze von fünf Sätzen.
Es unterstützt Zahlenmesswerte für verschiedenste Trainingsformen; das Plugin
leitet keine Beziehungen zwischen Übungen ab und bewertet keine Trainingsform automatisch.

## Dauer und Last

Verwende alltagstaugliche Einheiten: Ein 20-minütiger Lauf hat die Einheit `Minuten` und den Wert pro Satz
`20`, nicht `Sekunden` und `1200`. Kurze Halteübungen können in Sekunden bleiben. Halte Zielwert und
Ergebnis in derselben Einheit. `Handstand-Gehen: 3 x 3 m` verwendet zum Beispiel drei Satzfelder
in Metern, auch mit Dezimalwerten. Sports zeigt sie als Meter an.
Das ausgefüllte Beispiel gewichtet die geplante Intensität nach Sätzen,
ohne Zeit in Wiederholungen umzurechnen. Eine Laufaktivität,
die nur in Wochenplan steht, verwendet ihr Feld Minuten und braucht keine Zeile in Bewertung.

Bei manueller gruppierter Erfassung liefert `A) Lockerer Lauf: 1 x 20 Minuten` ein Ziel in Minuten;
ein reines Zahlenergebnis `22` bedeutet 22 Minuten. Auch die Uhrzeitform `22:00` bedeutet 22
Minuten. Bei Vorgaben in Sekunden sind Zahlenergebnisse Sekunden. Obsidian
vereinheitlicht Zeiten intern und zeigt minutenbasierte Messwerte in Minuten;
kurze Halteübungen in Sekunden behalten ihre Einheit.

Optionale Gewichte je Abschnitt und die Formeln des Beispiels findest du unter
[Übungsgewichte](Arbeitsmappe.md#übungsgewichte).
