# Sports verwenden

Starte mit **Dashboard öffnen** oder füge deiner eigenen Startseite einen `sports-dashboard`-Block hinzu. Plane in den Wochennotizen, trage Ergebnisse
in die Arbeitsmappe ein und schreibe eigene Kommentare außerhalb der erstellten Abschnitte.

Das Dashboard zeigt Montag bis Sonntag. Mit den Pfeilen wechselst du wochenweise,
**Heute** springt zurück zu heute, und ein Tag in der Leiste zeigt seine Einheiten.
**Diese Woche**, **Statistik**, **Protokoll** und **Pläne**
öffnen die Wochennotiz, die Trends, das Trainingsprotokoll und die Pläne. Das Zahnrad öffnet die Sports-Einstellungen.
Abschließen, Wiederherstellen und die Anleitungen erreichst du über die Befehlspalette.

## Einstellungen

**Quellen** enthält **Arbeitsmappe**, **Zeitplan**, **Smartwatch** und **Synchronisieren**. Unter Smartwatch wählst du zuerst
dein **Gerät**; danach erscheinen nur dessen Einstellungen. Mehrere Geräte können gleichzeitig aktiv sein. Unter Arbeitsmappe
liegen in **Einrichtung** die Anleitung und die Vorlagen, in **Blätter** die Blattnamen.
**Anzeige** steuert Notizordner, Diagramme und Dashboard. **Erweitert → Standardwerte setzen** setzt Synchronisierungs- und Anzeigeeinstellungen zurück und stellt den Verlauf von Garmin und Google Health auf vor 90 Tagen. Notizordner, Quellen und Daten bleiben erhalten. **Erweitert** enthält außerdem die Wiederherstellungswerkzeuge.

## In dieser Anleitung

- [Deine Notizen](#deine-notizen)
- [Eigenschaften und Tags](#eigenschaften-und-tags)
- [Trainingsdiagramme](#trainingsdiagramme)
- [Zeitpläne und Kalender](#zeitpläne-und-kalender)
- [Garmin-Aktivitäten synchronisieren](#garmin-aktivitäten-synchronisieren)
- [Google-Health-Aktivitäten synchronisieren](#google-health-aktivitäten-synchronisieren)
- [Trainingsdateien (Apple Watch und andere Uhren)](#trainingsdateien-apple-watch-und-andere-uhren)
- [Plan abschließen oder wiederherstellen](#plan-abschließen-oder-wiederherstellen)

## Deine Notizen

Nutze die Einbettung auf deiner Startseite oder das Dashboard für aktuelle Fortschritte und anstehendes Training, das Protokoll für vergangene Trainingstage und die Statistik für Trends. Pläne und Strategie liegen unter Struktur. Die Statistik verlinkt über ihre Eigenschaft **related** auf die Diagramme aus Tabelle und Uhr.

Der Standard-Notizordner ist `Sports/`. Dateien entstehen, sobald ihre Quelldaten vorliegen. Ordner- und Notiznamen folgen der Sprache von Obsidian. Wechselst du die Sprache, verschiebt Sports Notizen an ihrem Standardort an den neuen Standardort. Notizen, die du selbst verschoben hast, bleiben, wo sie sind.

Nachdem du über eine Woche nachgedacht hast, hake **reviewed** in den Eigenschaften der Wochennotiz an. Der Sonntagsknopf im Dashboard und im vollständigen Widget wechselt dann zu **✓ Woche reflektiert**. Entferne den Haken, um die Erinnerung zurückzuholen. Die Synchronisierung behält deine Wahl bei.

| Pfad | Inhalt |
| --- | --- |
| `Struktur/Sports.base` (vorhandene Übersicht) | Sortierbare Ansichten für Wochen und Routinen über Notizeigenschaften |
| `Auswertung/Statistik.md` | Summen je Quelle und Trainingstrends |
| `Journal/Wochen/JJJJ-MM-TT.md` | Wichtigste Notiz für Wochenplanung, Ergebnisse und Rückblick |
| `Struktur/Pläne.md` | Ziele, wöchentliche Steigerung und anstehende Einheiten |
| `Struktur/Strategie.md` | Programmaufbau und wiederkehrender Zeitplan |
| `Protokoll.md` | Trainingseinträge: Wähle das Datum für die Tagesnotiz oder den Trainingsnamen für die Routine |
| `Journal/Tage/JJJJ-MM-TT.md` | Details der Einheiten, Sätze, Aufzeichnungen und eigene Reflexion |
| `Auswertung/Tabelle.md` | Trends für geplante Intensität, Leistung und gefühlte Anstrengung |
| `Auswertung/Uhr.md` | Uhr-Umfang sowie Lauf- und Schwimmdiagramme |
| `Ziele/<goal_id>.md` | Zielwerte, zugeordnete Ergebnisse, passende Aktivitäten und Rückblicke |
| `Routinen/` | Erklärungen, Übungen und Steigerungen je Routine; verlinkt aus Plänen und Protokoll |
| `Anleitung/` | Arbeitsmappe, Erfassung, Sports verwenden und Fehlerbehebung |

Wochennotizen gibt es für die aktuelle Woche, für importierte Einheiten und für Week plans.
Tagesnotizen unter Journal gibt es für heute und frühere Tage mit Einträgen aus Arbeitsmappe oder Uhr
sowie für aktivierte Kalendertermine. Öffnest du im Dashboard einen künftigen Tag, entsteht auch dessen geplante Tagesnotiz. Plane in Journal/Wochen; im Protokoll findest du die erfassten Tage.
Zielkategorien unterscheiden Entwicklung und Erhaltung; beide können Ergebnisse aus der Arbeitsmappe
und Uhr-Aktivitäten nutzen. Die Zuordnung der Quellen legst du in Strategie fest.

Das importierte Training verwaltet Sports. Schreibe eigene Beobachtungen in die Abschnitte für Reflexion oder Rückblick darunter. Erledigt-Status aus der Arbeitsmappe, Uhr-Aufzeichnungen und erreichte Ziele sind voneinander unabhängig.

Du kannst verwaltete Notizen innerhalb des Vaults umbenennen oder verschieben. Lösche eine optionale erstellte Notiz, damit sie nicht mehr aktualisiert wird; **Einstellungen → Sports → Erweitert → Fehlende Notizen neu erstellen** stellt gelöschte Seiten wieder her. Routinen erscheinen nur, wenn sie in deinem Plan oder im importierten Training vorkommen. Ältere Notizen bleiben mit deinem Text erhalten, wenn ihre Routine den Plan verlässt.

Übersicht, Kalender, der Routinen-Index und der separate Tagesindex werden nicht mehr erstellt. Eine unveränderte Übersicht ohne eigenen Text wird entfernt; angepasste Kopien werden archiviert. Andere vorhandene Kopien bleiben in `Archive/Previous pages/` erhalten, einschließlich deines Textes. Strategie und die ausführlichen Diagrammseiten bleiben verfügbar.

## Eigenschaften und Tags

Das Dashboard und die Einbettung auf deiner Startseite dienen der Navigation. Statistik und Anleitungen verweisen über die Eigenschaft **related** auf zugehörige Notizen; die Pläne verlinken Routinen und datierte Einheiten. Links stehen dort, wo sie eine Beziehung beschreiben: Ziel-Links in den Eigenschaften
der Routinen, ein Link zur Wochennotiz an jedem Tag und datierte Links in Protokoll und Plänen.

| Notiz | Verwaltete Eigenschaften | Quelle |
| --- | --- | --- |
| `Auswertung/Statistik.md` | `related` (Links zu Tabelle und Uhr) | Ausführliche Diagrammseiten |
| `Anleitung/` | `related` (Links zu den anderen Anleitungen) | Begleitende Anleitungen |
| `Ziele/<goal_id>.md` | `goal_id`, `category`, `garmin_types` | Tabelle Goals und aufgelöste Quellenzuordnung |
| `Routinen/<Name>.md` | `targets` (Liste von Ziel-Links) | Beziehungen zwischen Teilen und Zielen; Lauf- und Schwimmziele |
| `Journal/Tage/JJJJ-MM-TT.md` | `date`, `week` (Link zur Wochennotiz) | Datum des Eintrags und seine Woche ab Montag |
| `Journal/Wochen/JJJJ-MM-TT.md` | `week_start`, `week_end`, `program_week`, `phase` | Kalenderdaten und passende Zeile in Week plans |

Zielkategorien erscheinen als **Entwicklung** oder **Erhaltung**. Ausgangswert, Ziel und
Teststandard stehen im Text der Zielnotiz. Leere optionale Eigenschaften entfallen;
eine Woche ohne Zeile in Week plans hat zum Beispiel weder program_week noch phase.

Die Eigenschaften einer Routine können so aussehen:

```yaml
---
targets:
  - "[[Sports/Ziele/muscle-up|Muscle-up]]"
  - "[[Sports/Ziele/pistol|Pistol Squat]]"
tags:
  - sports/planning
  - sports/goals
---
```

Sports verwendet in den Links deinen eingestellten Notizordner. Die Synchronisierung aktualisiert die verwalteten
Eigenschaften aus den importierten Daten. Zielzuordnungen und Plandaten änderst du in der
Arbeitsmappe; Änderungen an diesen Eigenschaften in Obsidian werden nicht zurückgeschrieben.
Andere eigene Eigenschaften bleiben erhalten. Eigenschaftsnamen und Tags bleiben in jeder Sprache gleich.

| Gemeinsamer Tag | Seiten |
| --- | --- |
| `sports/planning` | Pläne, Strategie, Routinen, Wochen |
| `sports/goals` | Pläne, Ziele, Routinen |
| `sports/training` | Protokoll, Tage, Wochen |
| `sports/analytics` | Statistik, Tabelle, Uhr |
| `sports/guide` | Alle vier Anleitungen |
| `sports/running`, `sports/swimming` | Passende Routinen und Ziele mit diesen aufgelösten Garmin-Typen |

Nutze den Tag-Bereich von Obsidian oder suche nach einem Tag wie `tag:#sports/planning`, um
zusammengehörige Notizen zu finden. Sports aktualisiert diese Tag-Gruppen bei der Synchronisierung, entfernt veraltete verwaltete
Tags und behält deine eigenen. Für eigene Gruppen verwendest du eigene Tag-Namen.

### Wochen und Routinen durchsuchen

Wenn du die frühere Sports-Übersicht genutzt hast, liegt sie jetzt in `Struktur/Sports.base`. Ihre
Ansicht **Weeks** zeigt Daten, Programmwoche und Phase; **Routines** zeigt verknüpfte Ziele.
Aktiviere das Kern-Plugin **Bases**, um diese sortierbaren Tabellen zu nutzen. Nur Notizen
in deinem aktuellen Sports-Ordner werden berücksichtigt; Sicherungen und der Routinen-Index sind ausgeschlossen.

Die Base liest vorhandene Eigenschaften und braucht keine eigene Synchronisierung. Spalten,
Sortierung und Filter kannst du frei anpassen: Sports behält vorhandene Base-Ansichten und aktualisiert bei der Migration ihre Ordnerangaben. Änderungen an verwalteten Eigenschaften über
eine Base werden bei der Synchronisierung trotzdem ersetzt. Ändere diese Werte in der Arbeitsmappe.

### Training in eine andere Notiz einbetten

Das vollständige Widget zeigt heute, anstehende Einheiten und Links zu **Diese Woche**, **Statistik** und **Protokoll**:

````markdown
```sports-dashboard
```
````

Aktiviere **Einstellungen → Sports → Anzeige → Letztes Training anzeigen**, um die letzten Ergebnisse und die Zusammenfassung der letzten sieben Tage einzublenden.

Nur das heutige Training, ohne Navigation, letzte Ergebnisse oder anstehende Einheiten:

````markdown
```sports-today
```
````

Beide funktionieren in der Leseansicht und in Live Preview. Wähle ein Datum, um seine Tagesnotiz zu öffnen, auch wenn kein Training geplant oder aufgezeichnet ist.
Vorhandene `sports-today`-Blöcke zeigen jetzt nur noch heute; ändere sie zu `sports-dashboard`, um das vollständige Widget zu behalten.

## Trainingsdiagramme

Übungsvergleiche zeigen ausdrückliche Ziele und aufgezeichnete Ergebnisse, jede Einheit
getrennt. Tagesnotizen enthalten Satztabellen und Diagramme für Plan und Ergebnis: farbige Umrisse
zeigen Pläne, grüne Balken Ergebnisse. Jedes Diagramm unterstützt zwei Einheitentypen mit eigener linker und rechter Achse.
Wiederholungen und Runden teilen sich eine Zählachse; Zeit wird als min:ss angezeigt. Ein dritter Einheitentyp bekommt ein eigenes Diagramm.
Die Reihenfolge der Übungen bleibt in jedem Diagramm erhalten; Höhen verschiedener Einheiten sind nicht vergleichbar. Zeilenbasierte Erfassung verwendet die eingestellte Zusammenfassung
(standardmäßig die Summe); einzelne Satzwerte bleiben verfügbar. Teilsummen sind gekennzeichnet.

**Statistik** hält Summen aus Arbeitsmappe und Uhr getrennt und vergleicht die gefühlte Anstrengung mit
vorhandenen HF-Zonen der Uhr. Dasselbe Training kann in beiden Quellen erscheinen.
**Auswertung/Uhr** zeigt aufgezeichneten Umfang, Lauf- und Schwimmpace, Herzfrequenz
und vorhandene Zonendaten. Uhr-Aufzeichnungen erledigen nie manuelle Einheiten.

Das Blatt Bewertung im Beispiel liefert geplante Intensität (0–10), Leistung (%)
und Abdeckung der Messgrößen. Die optionale Spalte Anstrengung (1–5) hält fest, wie anstrengend sich das Training angefühlt hat.
Die Berechnungsgrundlagen findest du unter [Bewertung und Übungsbibliothek](Arbeitsmappe.md#bewertung-und-übungsbibliothek).

Die Tabelle zeigt drei Zeitreihen, alle mit dem Datum auf der waagrechten Achse:

1. Leistung × Intensität und geplante Intensität auf einer gemeinsamen Skala.
   Angezeigte Leistung = Intensität der Einheit × tatsächliche Leistung / 100. Bei
   100 % liegen die Linien übereinander; bei 80 % liegt der Leistungspunkt 20 % tiefer. Werte
   über 100 % können über 10 hinausgehen; die Darstellung wächst mit, ohne abzuschneiden.
2. Gefühlte Anstrengung (linke Achse 0–5, erfasste Bewertungen 1–5) und Intensität (rechte Achse 0–10).
3. Nur die tatsächliche Tagesleistung auf einer festen Skala von 0–200 %: 0 % unten,
   100 % in der Mitte und 200 % oben. Eine Reihe für erwartete Leistung gibt es nicht.
   Werte über 200 % werden oben markiert; die tatsächlichen Werte stehen in der
   Punktbeschriftung. Ohne Ergebnisse bleiben die Achsen ohne Datenpunkte sichtbar.

Die Leistung wird je Einheit skaliert, bevor der Tagesmedian gebildet wird. Die anderen Reihen
verwenden den Median der vorhandenen Werte je Tag. Die Intensität
kann erscheinen, bevor Leistung oder Anstrengung erfasst sind. Fehlende Werte sind keine
erfassten Nullen. Abdeckung und gefühlte Anstrengung je Einheit stehen in den Tagesnotizen, die du über das Protokoll erreichst.
Die getrennten Achsen vergleichen Trends verschiedener Einheiten, keine gleichen Werte.
Eine Bewertung misst, wie gut ein Ziel erreicht wurde, nicht die absolute Trainingsqualität. Schreibe
Kommentare außerhalb der geschützten erstellten Abschnitte.

Diagramme werden lokal in der Leseansicht oder in Live Preview gezeichnet, solange Sports aktiviert ist.
Der Quellmodus zeigt lesbare Codeblöcke; ein externer Diagrammdienst wird nicht verwendet.

## Zeitpläne und Kalender

Aktiviere **Zeitplan anzeigen**, um den gewählten Zeitplan im Dashboard und in den
Wochennotizen zu zeigen. Standardmäßig ist er aus; ein Wechsel der **Quelle des Zeitplans** schaltet ihn ein.
Wähle **Wiederholungen aus der Arbeitsmappe** oder **ICS-Kalender**. Die nicht gewählte Quelle wird
weder synchronisiert noch angezeigt. Wiederkehrende Einträge beschreiben Pläne, keine erledigten Einheiten.

### ICS-Kalender verbinden

Wähle in **Einstellungen → Sports → Quellen → Zeitplan** als Quelle **ICS-Kalender**, füge den ICS-Abonnementlink eines eigenen Trainingskalenders ein und wähle dann **Jetzt synchronisieren**. Bei Google Calendar verwendest du die geheime Adresse im iCal-Format. Bei Nextcloud fügst du den öffentlichen Freigabelink des Kalenders oder einen ICS-Abonnement- bzw. Exportlink ein. Öffentliche Freigabelinks werden automatisch in ICS-Exporte umgewandelt; private CalDAV-Adressen mit Anmeldung werden nicht unterstützt. HTTPS- und `webcal://`-Links funktionieren (`webcal` wird über HTTPS geladen).

Kalendertermine erscheinen im Dashboard, in eingebetteten Widgets und in den Wochennotizen. Die Aktualisierung folgt **Beim Start synchronisieren** und dem **Synchronisierungsintervall**. Nach einem erfolgreichen Download ersetzen Änderungen und Löschungen die zwischengespeicherten Termine; bei einem Fehler bleibt der bisherige Zwischenspeicher. ICS ist schreibgeschützt: Termine legst du in Google Calendar oder Nextcloud an, verschiebst und löschst sie dort. Workouts werden dadurch weder als erledigt markiert noch wird die Arbeitsmappe geändert.

Jede Aktualisierung importiert Termine mit Beginn in den letzten 30 Tagen bis zu den nächsten 365 Tagen, einschließlich Serien und Ausnahmen. Termine mit Uhrzeit verwenden die Zeitzone des Geräts; ganztägige Termine behalten ihr Kalenderdatum. Mehrtägige Termine erscheinen an ihrem ersten Tag. Spätere Termine kommen mit einer späteren Aktualisierung. Feeds sind auf 5 MB begrenzt, Serien auf 50.000 Vorkommen je Aktualisierung.

Der Abonnementlink und die importierten Termine werden lokal in den Plugin-Daten des Vaults gespeichert und können durch Vault-Synchronisierung oder Sicherungen kopiert werden. Behandle einen geheimen Abonnementlink wie ein Passwort. Anfragen gehen direkt an den eingestellten Kalenderanbieter; es werden keine Vault-Daten hochgeladen. Leere den Link und synchronisiere, um die Verbindung zu trennen und importierte Termine aus den erstellten Notizen zu entfernen. Für erstellte Notizen gilt der übliche Bearbeitungsschutz.

### Kalenderpläne und Uhr-Aufzeichnungen zuordnen

Wochen- und Tagesnotizen, Dashboard und eingebettete Widgets zeigen eine Uhr-Aktivität innerhalb ihrer geplanten Workout-Kachel, wenn die Sportart passt und sich die Aufzeichnung weitgehend mit der geplanten Zeit überschneidet. Eine Schwimmeinheit von 08:00–09:00 kann zum Beispiel eine Garmin-Aufzeichnung von 08:10–09:00 enthalten. Die Kachel hält geplante Minuten und aufgezeichnete Messwerte getrennt. Nicht zugeordnete Aktivitäten bekommen eigene Kacheln; gleich plausible Zuordnungen bleiben getrennt. Ganztägige Termine und Einträge ohne Dauer werden nicht automatisch zugeordnet.

Die Zuordnung funktioniert für ICS-Kalendertermine und für den Wochenplan der Arbeitsmappe. Verknüpfungen werden nach jeder Aktualisierung aus den aktuellen Quelldaten neu berechnet; Kalender, Garmin-Aufzeichnungen, manueller Erledigt-Status und Summen der Auswertung bleiben unverändert. Mehrere Aufzeichnungen können zu einem geplanten Termin gehören, eine Aufzeichnung erscheint aber nur einmal. Vorhandene Änderungen und Reflexionen behalten ihren üblichen Schutz.

### Kalendertermine mit Zielen verknüpfen

Füge der Beschreibung eines Termins eine Zeile hinzu, um ihn einem Ziel aus Strategie zuzuordnen:

```text
goal-id: swimming
```

Verwende die genaue `goal_id` aus Strategie, nicht den angezeigten Titel. Mehrere Ziele schreibst du als `goal-ids: swimming, running`. Der Termin erscheint dann auf der Seite des Ziels und in den Routinen, die über die Verknüpfung von Teilen und Zielen in Strategie oder über die Zuordnung von Garmin-Typen damit verbunden sind. Ein eigenes Ziel mit dem Garmin-Typ `swimming` speist zum Beispiel **Routinen/Schwimmen**. Diese Verknüpfungen helfen auch, Garmin-Aufzeichnungen zuzuordnen, wenn ein Termin einen allgemeinen Titel wie „Morgentraining“ trägt.

Genaue Ziel-IDs aus Strategie funktionieren in der Beschreibung auch ohne Bezeichnung: `swimming` oder `Verein swimming`. IDs müssen für sich stehen, getrennt durch Leerzeichen, Kommas oder Semikolons; Wortteile werden nicht erkannt. Ein ausdrückliches `goal-id:` hat Vorrang. Nur diese IDs ordnen Kalendertermine Zielen und Routinen zu. Termintitel und angezeigte Zieltitel können in jeder Sprache sein; Beschreibungen ohne bekannte ID bleiben unzugeordnet. Im Hauptkalender bleiben alle Termine sichtbar. Die Zeile mit der ID wird in Workout-Kacheln ausgeblendet. Auf Routinen- und Zielseiten teilen passende Aufzeichnungen die datierte Tabellenzeile des Termins. Wochen- und Tagesnotizen zeigen sie innerhalb der Terminkachel.

### Kompakte Sportseiten

Routinen- und Zielseiten verwenden kompakte Tabellen. **Wiederkehrender Zeitplan** führt jede Kalenderserie einmal mit Wochentagen, Uhrzeit und Wiederholung auf. Die datierten Tabellen enthalten einmalige Termine, verschobene Vorkommen und aufgezeichnete Einheiten; eine verknüpfte Garmin-Aufzeichnung bleibt in der Zeile ihres geplanten Termins. Nicht aufgezeichnete Vorkommen einer Serie werden nicht als eigene Zeilen wiederholt. Wochen- und Tagesnotizen behalten ihre Workout-Kacheln.


## Garmin-Aktivitäten synchronisieren

Wähle am Desktop **Einstellungen → Sports → Quellen → Smartwatch**, wähle **Garmin** als Gerät und dann **Garmin verbinden**. Melde dich mit
E-Mail-Adresse und Passwort deines Garmin-Kontos an und gib bei Bedarf den Bestätigungscode ein. Python,
Terminalbefehle oder eine separate Installation sind nicht nötig. Diese Verbindung ist experimentell,
bis Anmeldung, Zwei-Faktor-Bestätigung und Token-Erneuerung mit einem echten Konto geprüft sind.

Mit dem Verbinden erlaubst du ausdrücklich Netzwerkzugriffe auf Garmin und startest einen Aktivitätsimport.
Passwörter und Bestätigungscodes existieren nur im Anmeldedialog und werden nie
gespeichert. Sitzungstoken liegen im geschützten Speicher von Obsidian, getrennt von den
Plugin-Einstellungen und den erstellten Notizen. Erforderlich ist Obsidian 1.11.4 oder neuer.

Der mitgelieferte Client [garminconnect-js](https://github.com/DynamicsNinja/garminconnect-js)
nutzt inoffizielle Schnittstellen von Garmin Connect. Er lädt außerdem öffentliche OAuth-Anwendungsschlüssel
von `https://thegarth.s3.amazonaws.com/oauth_consumer.json`; an diesen Host werden weder
Zugangsdaten noch Aktivitätsdaten gesendet. Es handelt sich um JSON-Daten, nicht um ausführbaren
Code. Garmin kann diese Schnittstellen ändern oder Anmeldungen begrenzen. Unterstützt werden
derzeit Garmin-Konten auf garmin.com, nicht auf garmin.cn.

Lege mit **Beginn des Garmin-Verlaufs** das erste zu importierende Datum fest. Standard ist vor 90
Tagen. Solange Obsidian läuft, prüft die automatische Synchronisierung Garmin höchstens einmal pro Stunde
im eingestellten Intervall. **Jetzt synchronisieren** fordert sofort eine Aktualisierung an.
Garmin wird auch aktualisiert, wenn der Import der Arbeitsmappe fehlschlägt. Sind alle drei Blattzuordnungen
leer, funktioniert Garmin auch ganz ohne Arbeitsmappe.

Aktivitäts-ID, lokales Datum und Uhrzeit, Name, Typ, Dauer, Distanz, durchschnittliche Herzfrequenz
und die Zusammenfassung der Herzfrequenzzonen werden in den Plugin-Daten des Vaults zwischengespeichert und im **Protokoll**, in den Wochennotizen und im
Dashboard angezeigt. GPS-Strecken und vollständige Kontoantworten werden nicht gespeichert. Aktivitäten verwenden
Garmins lokale Startzeit; Einträge nur mit GMT verwenden die Zeitzone des Plans oder ohne Plan deine
lokale Zeitzone. Garmin-Aufzeichnungen markieren manuelle Einheiten nie als erledigt.

Jede erfolgreiche Aktualisierung ersetzt den gewählten Zeitraum, sodass geänderte oder gelöschte
Aktivitäten keine Duplikate erzeugen. Bei einem Fehler bleibt der bisherige Stand mit einer Warnung
sichtbar. **Trennen** löscht die gespeicherten Token und beendet alle Garmin-Anfragen;
zwischengespeicherte Aktivitäten bleiben verfügbar. **Zwischengespeicherte Daten löschen** entfernt den importierten
Aktivitätsspeicher und behält die Verbindungseinstellungen. Erstellte Notizen und Reflexionen
behalten ihren Bearbeitungsschutz.

### Optionale Garmin-Coach-Pläne

Aktiviere **Garmin-Coach-Pläne anzeigen**, um veröffentlichte adaptive Coach-Workouts
der nächsten 28 Tage in den Plänen zusammenzufassen. Die Option ist standardmäßig aus und
muss noch mit einem echten Konto geprüft werden. Vollständige Workout-Schritte, selbst geplante Workouts
und feste Trainingspläne sind ausgenommen. Die aktuelle Vorgabe findest du in Garmin Connect.
Bei einer fehlgeschlagenen Aktualisierung bleiben die zwischengespeicherten Zusammenfassungen mit einer Warnung erhalten. Schaltest du die Option aus,
enden die Coach-Anfragen; Trennen beendet alle Garmin-Anfragen.

## Google-Health-Aktivitäten synchronisieren

Trainings, die in Google Health aufgezeichnet werden, zum Beispiel von einer Fitbit oder
Pixel Watch, kommen über dein Google-Konto. Richte zuerst die Google-Health-App auf deinem
Smartphone mit diesem Konto ein. Wähle dann am Desktop
**Einstellungen → Sports → Quellen → Smartwatch**, wähle **Google Health** als Gerät und dann **Google Health verbinden** und melde dich
im Browser bei Google an. Sports fragt nur Lesezugriff auf deine Aktivitäts- und Fitnessdaten an.

Anmeldetoken liegen im geschützten Speicher von Obsidian, getrennt von Plugin-Einstellungen
und Notizen. Sports ruft Trainings höchstens einmal pro Stunde bei Google ab, ab
**Google-Health-Verlauf ab** (standardmäßig vor 90 Tagen). Übernommen werden Startzeit, Sportart,
Name, aktive Dauer, Distanz und durchschnittliche Herzfrequenz; Routen werden nie abgefragt.
**Trennen** entfernt die gespeicherte Anmeldung; zwischengespeicherte Aktivitäten bleiben, bis du sie löschst.

Solange die Google-App im Testmodus ist, können sich nur eingeladene Konten verbinden, und Google
verlangt alle 7 Tage eine neue Anmeldung. Einzelheiten stehen in der [Datenschutzerklärung](https://sports.trainvent.com/de/privacy/).

## Trainingsdateien (Apple Watch und andere Uhren)

Die Apple Watch und die meisten anderen Uhren lassen sich nicht direkt verbinden,
können Trainings aber als FIT-, TCX- oder GPX-Dateien exportieren. Lege diese Dateien in einen
Ordner im Vault und trage ihn unter **Einstellungen → Sports → Quellen → Smartwatch** ein, nachdem du **Apple Watch und andere** als Gerät gewählt hast.
Unterordner werden mitgelesen.

Für die Apple Watch kann eine iPhone-App wie HealthFit oder RunGap Trainings automatisch
in einen iCloud-Drive-Ordner exportieren. Wähle diesen Ordner als Vault-Ordner oder als
Unterordner davon. Polar, Suunto, Coros, Wahoo und Strava bieten ähnliche Exporte.

Jede Synchronisierung liest nur neue oder geänderte Dateien. Sports übernimmt Startzeit,
Sportart, Dauer, Distanz und durchschnittliche Herzfrequenz; Routen und einzelne Trackpunkte
werden nie gespeichert. Herzfrequenzzonen werden aus Dateien nicht importiert. Die Aktivitäten
erscheinen überall dort, wo auch andere Uhr-Aktivitäten erscheinen: im Log, in Tages- und Wochennotizen,
Routinen, Diagrammen und im Dashboard. Kommt dasselbe Training von Garmin und aus einer Datei
oder aus zwei Dateien, wird es nur einmal angezeigt. Nicht lesbare Dateien werden mit einer
Warnung übersprungen; andere Aktivitäten bleiben sichtbar.

## Plan abschließen oder wiederherstellen

Führe **Sports: Plan abschließen** in der Befehlspalette aus. Als Ziel ist
`Archive/<Planname>` vorgeschlagen; du kannst es ändern. **Abschließen und Notizen verschieben** verschiebt die
aktuellen Notizen dorthin (auch verwaltete Notizen, die an anderer Stelle im Vault liegen), trennt die Arbeitsmappe und beendet den aktiven Plan.

Jeder abgeschlossene Ordner enthält `settings.md` mit dem ursprünglichen Link zur Arbeitsmappe,
den Blattnamen, dem importierten Plan und den Grundlagen der erstellten Notizen. Diese gespeicherten Pläne
sind unabhängig von den 10 rotierenden Sicherungskopien und laufen nicht automatisch ab.
Arbeitsmappe, Uhr-Verbindungen und Plugin-Einstellungen bleiben erhalten.

Führe **Sports: Aus Ordner wiederherstellen** in der Befehlspalette aus, gib den abgeschlossenen Ordner ein
und wähle **Gespeicherten Plan lesen**. Den Link zur Arbeitsmappe kannst du kopieren, ohne wiederherzustellen.
**Plan wiederherstellen** verschiebt die Notizen zurück und stellt den gespeicherten Plan samt Link wieder her.
Schließe vorher einen aktiven Plan ab; vorhandene Zielordner werden nie überschrieben.
Die Synchronisierung der Arbeitsmappe bleibt pausiert, bis du **Jetzt synchronisieren** wählst. So kannst du
den wiederhergestellten Link vorher prüfen oder ersetzen. Für einen neuen Plan wählst du stattdessen eine Arbeitsmappe.

Zu Cloud-Downloads, Synchronisierungszeitpunkten und Wiederherstellung siehe [Fehlerbehebung](Fehlerbehebung.md).
