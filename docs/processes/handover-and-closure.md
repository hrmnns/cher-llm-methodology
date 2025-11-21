# Handover & Closure  
Dieses Dokument definiert verbindliche Regeln, Formate und Templates für:

- den **Abschluss von Chats und Chat-Einheiten**  
- die **Übergabe** von Ergebnissen an Folge-Chats, Issues oder Personen  
- den **Neustart eines Chats**, wenn Kontextgrenzen erreicht werden  
- die **Dokumentation und Persistenz** von Zwischenständen  

Es operationalisiert besonders **Phase 6 – Abschluss & Übergabe** des Makroprozesses und die Übergangspunkte im Mikroprozess.

Ziel ist eine **reproduzierbare, konsistente und klare Übergabestruktur**, die Kontextverlust, Drift und Redundanzen vermeidet.

## 1. Regeln für den Chat-Abschluss

Ein Chat gilt als **abgeschlossen**, wenn folgende Bedingungen erfüllt sind:

### 1.1 Abschlusskriterien
- Die Fragestellung oder Aufgabe ist **in der aktuellen Iteration vollständig beantwortet**.  
- Alle relevanten Ergebnisse liegen in **strukturierter Form** vor (Tabellen, Listen, Modelle).  
- **Offene Punkte** sind klar markiert und als Issues vorgeschlagen.  
- Eine **Übergabe oder Persistenz** ist vorbereitet (siehe Templates).  
- Es ist klar definiert, **wie und in welcher Form weitergearbeitet wird**.

### 1.2 Pflichtschritte beim Abschluss
- Kurze **Zusammenfassung des Erreichten**  
- Formulierung der **konkreten offenen Punkte**  
- **Empfehlung für den nächsten Schritt** (weiter im Chat, neuer Chat, Issue, Persistenz)  
- **Verweis auf betroffene Dokumente** im Repository  
- Falls relevant: kurze **Risiko-/Konsistenzprüfung**

### 1.3 Gründe für den Abschluss
- Ende einer Mikroprozess-Einheit  
- Übergang zwischen Makroprozessphasen  
- Abstraktionswechsel / Strukturwechsel  
- Output ist „gut genug“ für Persistenz oder Konsolidierung  
- Vermeidung unnötiger Chat-Länge  

## 2. Kriterien für „Neuer Chat notwendig“

Ein neuer Chat ist notwendig, wenn mindestens einer der folgenden Punkte zutrifft:

### 2.1 Inhaltliche Kriterien
- **Kontextdrift** erkennbar  
- Themen- oder Aufgabenwechsel  
- Wechsel der Granularität („Wechsel in ein anderes Kapitel“, „andere Ebene“)

### 2.2 Strukturelle Kriterien
- Start einer **neuen Prozessphase** (Makroprozess)  
- Wechsel der Rolle des LLM (z. B. Methodiker → Reviewer)  
- Wechsel des Arbeitsmodus (Brainstorming → Konsolidierung)  
- Die Projektanweisung wäre andernfalls überlastet

### 2.3 Technische/Pragmatische Kriterien
- Chat wurde sehr lang  
- Die Übersicht geht verloren  
- Ein Teilprozess soll sauber abgegrenzt dokumentiert werden  
- Ein strukturiertes Ergebnis soll „frisch“ erzeugt werden

### 2.4 Absolute Grenzen
- Wenn ein Zwischenstand ins Repository geschrieben wurde → neuer Chat  
- Wenn ein anderer Mensch übernimmt → neuer Chat  
- Wenn ein Issue geschlossen/eröffnet wird → idealerweise neuer Chat  


## 3. Übergabevorlagen (Handover-Templates)

Diese Templates werden **am Ende eines Chats** genutzt oder können als **erster Beitrag eines neuen Chats** eingefügt werden.

### 3.1 Template: Übergabe an neuen Chat

```
# Handover an neuen Chat

## Kontext
- Thema:
- Ziel der bisherigen Arbeit:
- Relevante Dokumente:
- Bearbeitete Makro-/Mikroprozessphase:

## Bisherige Ergebnisse (Kurzfassung)
- …
- …

## Offene Punkte
- …
- …

## Konkreter nächster Schritt
- …
```


### 3.2 Template: Übergabe an neues Issue

```
# Übergabe an Issue

**Thema:**  
**Aktueller Stand (Kurz):**  
**Was bereits geklärt ist:**  
- …

**Offen:**  
- …

**Benötigte Rolle:** (Methodiker / Reviewer / Fachexperte / Dokumentationsverantwortlicher)

**Erwartetes Ergebnis:**  
…

**Betroffene Dateien:**  
- …
```


### 3.3 Template: Übergabe an Repository / Persistenz

```
# Übergabe zur Persistenz (Repository)

## Inhalte zur Übertragung
- Dokument/X aktualisieren
- Abschnitt Y konsolidieren
- Tabelle Z vereinheitlichen

## Quelle
- Link auf Chat
- Zusammenfassung des relevanten Outputs

## Zielort im Repo
- docs/processes/…
- docs/structure/…
- wiki/…

## Hinweise & Anforderungen
- Formatvorgaben
- Verlinkungen
- Versionierung
```

### 3.4 Template: Übergabe an Person/Rolle

```
# Übergabe an Rolle/Person

## Kontext
- Thema:
- Stand:
- Ziel der Übergabe:

## Was benötigt wird
- Review
- Ergänzung
- Persistenz
- Fachliche Klärung

## Materialien
- Relevante Abschnitte
- Dateien/Links

## Friktionen / Risiken
- …
```

## 4. Format für strukturierte Zwischenstände

Ein Zwischenstand hat immer die gleiche Form:

### Pflichtfelder
- **Titel / Arbeitseinheit**  
- **Ziel des Zwischenstands** (1–2 Sätze)  
- **Ergebnisse** (Listen, Tabellen, Modelle)  
- **Offene Punkte**  
- **Empfehlung für nächsten Schritt**  
- **Speicherort / Bezug zu Dokumenten**

### Optionale Felder
- Risiken  
- Varianten  
- Entscheidungsvorlagen  
- Betroffene Rollen  

### Abgrenzung
- Kein finaler Abschnitt → Persistenz erfolgt erst in Phase 5  
- Keine redundanten Inhalte → Fokus auf „strukturierte Verdichtung“  

## 5. Speicherorte & Versionierung

Übergaben und Abschlüsse erzeugen Ergebnisse, die **dauerhaft gesichert**, **auffindbar**, **versioniert** und **wiederverwendbar** sein müssen.  
Damit diese Ergebnisse nicht im Chat „verloren“ gehen, sondern korrekt in das Dokumentationssystem überführt werden, definiert dieser Abschnitt:

- **wo** bestimmte Typen von Informationen abgelegt werden  
- **wie** sie versioniert werden  
- **wie** sie mit der Informationsarchitektur abgestimmt bleiben  

Das stellt sicher, dass alle Teammitglieder (Menschen + LLM) jederzeit zuverlässig wissen, **wo welche Inhalte liegen**, und dass keine Inkonsistenzen entstehen.

## 5.1 Speicherorte

Die Ablage richtet sich nach der Informationsarchitektur, die das Repository in **funktionale Bereiche** gliedert. Jede Art von Inhalt hat einen **festen, vordefinierten Platz**:

| Kategorie | Speicherort | Zweck / Erklärung |
|----------|--------------|------------------|
| **Prozessdokumente** | `docs/processes/` | Alles, was Abläufe beschreibt: Makroprozess, Mikroprozess, Übergaben, Abschlussregeln. |
| **Rollen, Struktur, Definitionen** | `docs/structure/` | Beschreibt die fundamentalen Bausteine der Methode: Rollen, Artefakte, Modelle, Dokumententypen. |
| **Qualitätssicherung** | `docs/quality/` | Inhalte zur Stabilität des Systems: Persistenzmechanismen, Drift-Management, Qualitätsregeln. |
| **Meta (Entscheidungen & Historie)** | `docs/meta/` | Entscheidunglogs, Begründungen, methodische Metadaten, Änderungen am Vorgehen. |

**Warum ist das wichtig?**  
Damit alle Ergebnisse aus Übergaben **immer am richtigen Ort landen** und die Struktur langfristig stabil bleibt.

## 5.2 Regeln für Versionierung & Dokumentation

Jede Übergabe erzeugt ein **dauerhaftes Artefakt**. Damit diese Artefakte zuverlässig nachvollziehbar bleiben, gelten folgende Regeln:

### 1. **Jeder Übergabeprozess erzeugt mindestens einen Commit**  
Nichts bleibt im Chat – jede bestätigte Übergabe führt zu einer Repository-Aktualisierung.

### 2. **Commit-Messages folgen einem klaren Format**

```
Add/update <datei>: <kurze Beschreibung>
```

Beispiele:

- `Add handover-and-closure.md: initial version`
- `Update process-macro.md: phase 3 consolidated`
- `Add persistence rules: new quality section`

Damit bleibt die Commit-Historie eindeutig und maschinen-/menschenlesbar.

### 3. **Datei-Header (Metadaten) aktualisieren**

Jede Datei enthält zu Beginn einen standardisierten Block mit:

- Titel  
- Kategorie  
- Version  
- Status  
- Zuordnung/Links  

Dieser Header muss bei jeder Änderung aktualisiert werden (z. B. Version anheben).

Hier sind die beiden Abschnitte **klarer, präziser und ausführlicher formuliert**, ohne die Struktur aufzublähen.
Wenn du willst, kann ich sie anschließend direkt in deine Markdown-Datei einbauen.

### 4. **Backlinks setzen**

Jede Datei im `docs/`-Verzeichnis muss am Ende einen Abschnitt **„Weiterführende Dokumente“** enthalten.
Dieser Abschnitt ist nicht optional, sondern ein **zentrales Steuerungsinstrument**, das drei Funktionen erfüllt:

1. **Navigationslogik für das LLM**
   LLMs können nicht wie Menschen „durch das Repo blättern“.
   Backlinks erzeugen einen expliziten, textbasierten **Navigationsgraphen**, der es dem Modell ermöglicht:

   * Zusammenhänge korrekt zu erkennen
   * Inhalte über mehrere Dateien hinweg konsistent zu nutzen
   * kontextbezogen weiterzuarbeiten

2. **Vermeidung von Wissensinseln**
   Durch Backlinks wird sichergestellt, dass kein Dokument „verwaist“ bleibt.
   Das verhindert:

   * Doppelungen von Inhalten
   * Redundanzen
   * Abweichende Begriffsverwendung

3. **Orientierung für Menschen und Methode**
   Backlinks helfen nicht nur dem LLM, sondern auch Menschen.
   Sie machen transparent:

   * wo Dokumente thematisch hingehören
   * welche Dokumente logisch zusammenhängen
   * wo weitergelesen werden sollte

**Regel:**
Mindestens **2–4 Backlinks** pro Datei müssen gesetzt sein – idealerweise zu Dokumenten im selben Themenbereich (z. B. Prozesse, Struktur, Qualität).

### 5. **Bei größeren Arbeitspaketen: neues Issue + Mini-Release**

Nicht jede Übergabe ist klein.
Wenn ein Chat oder eine Konsolidierung **größere Mengen an Inhalten erzeugt**, gelten strengere Regeln, um Nachvollziehbarkeit und Stabilität zu sichern.

Ein Arbeitspaket gilt als „größer“, wenn mindestens eines zutrifft:

* Mehrere Dateien müssen angepasst werden
* Konsolidierte Inhalte betreffen **mehr als eine Prozessphase**
* Neue Dokumente entstehen mit übergreifendem Einfluss
* Die Änderung wäre schwer rückgängig zu machen
* Der Chat-Verlauf soll klar dokumentiert als Meilenstein erhalten bleiben

In solchen Fällen muss:

#### 1. **Ein neues Issue angelegt werden**

Beispiel:  `Persistenz: Konsolidierte Phase-3-Dokumente finalisieren`

Dieses Issue beschreibt:

* Worum es geht
* Welche Dateien betroffen sind
* Welche Schritte notwendig sind
* Welcher Commit zu welchem Teil gehört

Das erhöht die **Transparenz** und ermöglicht eine **klare Zuweisung** von Verantwortlichkeiten.

#### 2. **Ein Mini-Release erstellt werden**

Beispiel:
`v0.3.1 – Konsolidierte Prozessphase 3`

Ein Mini-Release ist notwendig, weil:

* größere Schritte sauber versioniert sein müssen
* andere Personen (oder das LLM) später darauf zurückgreifen können
* der Zustand jederzeit reproduzierbar bleibt
* es eine klare Markierung im Projektverlauf gibt

Diese Regel schützt das Projekt vor:

* Änderungen „unter dem Radar“
* schwer nachvollziehbaren Versionsständen
* versehentlichen Inkonsistenzen

**Kurz:**
Größere Übergaben → eigenes Issue + Mini-Release → vollständige Nachvollziehbarkeit.




## 5.3 Konsistenz zur Informationsarchitektur

Damit Übergaben nicht nur im Repository abgelegt werden, sondern sich sauber in die Gesamtstruktur einfügen, müssen sie konsequent an der Informationsarchitektur ausgerichtet sein. Die folgenden Grundsätze sichern diese Einbettung und sorgen dafür, dass Inhalte langfristig stabil und auffindbar bleiben:

- Neue oder geänderte Dateien müssen im docs/README.md verlinkt werden.
  Dieses README bildet das zentrale Inhaltsverzeichnis des gesamten Dokumentationssystems. Wenn eine Datei dort nicht aufgeführt wird, verliert sie schnell ihre Sichtbarkeit und damit ihre funktionale Einordnung. Die      Verlinkung stellt sicher, dass jede neue Information ihren Platz im Gesamtgefüge erhält.

- Jede Übergabe sollte einer klaren Makroprozessphase zugeordnet werden.
  Dadurch bleibt nachvollziehbar, zu welchem Zeitpunkt im methodischen Ablauf ein Ergebnis entstanden ist und welchem Zweck es dient. Konsolidierungen gehören in Phase 4, persistierte Inhalte in Phase 5, Übergaben an Stakeholder in Phase 6. Diese Zuordnung verhindert, dass Dokumente thematisch „zwischen den Phasen“ schweben oder falsch einsortiert werden.

- Jede Persistenz folgt den Qualitätsregeln von Phase 5.
  Das bedeutet, dass nur bereinigte und konsolidierte Inhalte übertragen werden: Struktur und Format müssen überprüft sein, Commit-Messages klar formuliert, Versionierungen eindeutig. Offene Punkte dürfen nicht im Dokument selbst verbleiben, sondern werden als Issues erfasst. Auf diese Weise gelangen keine halbfertigen oder widersprüchlichen Zwischenstände ins Repository, und die methodische Integrität bleibt gewahrt.


## 6. Beispiele

### 6.1 Gutes Übergabe-Beispiel
Ein gutes Handover zeichnet sich dadurch aus, dass der Kontext klar benannt ist, die erreichten Ergebnisse strukturiert zusammengefasst werden und offene Punkte eindeutig erkennbar sind. Außerdem zeigt es, wie es weitergeht und an welchem Ort im Repository die Informationen abgelegt werden sollen. Dadurch entsteht ein nachvollziehbarer, anschlussfähiger Übergabepunkt.

```
# Handover – Makroprozess Phase 3

## Ergebnisse
- Phase-3-Tabelle vollständig
- Rollen konsistent
- Übergabepunkte ergänzt

## Offene Punkte
- Beispielsektion fehlt
- Phase-3-Einleitung noch zu lang

## Nächster Schritt
-> Übergabe an Dokumentationsverantwortlichen zur Konsolidierung

## Speicherort
docs/processes/process-macro.md
```

### 6.2 Schlechtes Übergabe-Beispiel
Ein schlechtes Handover enthält weder Struktur noch Klarheit. Weder wird beschrieben, was erreicht wurde, noch welche Punkte offen sind oder wie weiter vorgegangen werden soll. Auch eine Referenz zum Repository fehlt – das macht eine solche Übergabe unbrauchbar für Folgearbeiten.

```
Hier ist alles, was wir haben. Mach einfach weiter.
```

## 7 Weiterführende Dokumente
- Makroprozess – Phase 6  
- Mikroprozess  
- Persistenzmechanismen  
- Informationsarchitektur  
