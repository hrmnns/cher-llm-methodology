# Handover & Closure  
Dieses Dokument definiert verbindliche Regeln, Formate und Templates für:

- den **Abschluss von Chats und Chat-Einheiten**  
- die **Übergabe** von Ergebnissen an Folge-Chats, Issues oder Personen  
- den **Neustart eines Chats**, wenn Kontextgrenzen erreicht werden  
- die **Dokumentation und Persistenz** von Zwischenständen  

Es operationalisiert besonders **Phase 6 – Abschluss & Übergabe** des Makroprozesses und die Übergangspunkte im Mikroprozess.

Ziel ist eine **reproduzierbare, konsistente und klare Übergabestruktur**, die Kontextverlust, Drift und Redundanzen vermeidet.

## 1. Regeln für den Chat-Abschluss

Der Abschluss eines Chats markiert den formalen Endpunkt einer Arbeitseinheit im Mikroprozess. Damit dieser Übergang sauber, nachvollziehbar und anschlussfähig erfolgt, müssen bestimmte Kriterien erfüllt und definierte Schritte durchgeführt werden. Die folgenden Unterabschnitte erläutern, wie ein Chat korrekt abgeschlossen wird und welche Gründe zu einem Abschluss führen können.


### 1.1 Abschlusskriterien

Bevor ein Chat beendet wird, sollte geprüft werden, ob die fachliche und strukturelle Arbeit tatsächlich abgeschlossen ist. Ein Chat gilt als beendet, wenn die Kernfrage beantwortet, die Ergebnisse vollständig erarbeitet und die Anschlussarbeiten eindeutig vorbereitet sind. Typischerweise ist das der Fall, wenn:

* die Fragestellung oder Aufgabe in der aktuellen Iteration vollständig beantwortet wurde,
* alle relevanten Ergebnisse in strukturierter Form vorliegen (z. B. Tabellen, Listen oder Modelle),
* offene Punkte klar markiert und idealerweise bereits als Issues vorgeschlagen wurden,
* eine Übergabe oder Persistenz vorbereitet ist (siehe Templates),
* und klar definiert ist, wie und in welcher Form weitergearbeitet wird.

### 1.2 Pflichtschritte beim Abschluss

Der Abschluss ist nicht nur eine inhaltliche, sondern auch eine methodische Handlung. Damit Ergebnisse für Folgeprozesse (z. B. Persistenz, neue Chats, Issues) nutzbar bleiben, müssen bestimmte Schritte durchgeführt werden. Jeder Chat-Abschluss umfasst daher:

* eine kurze Zusammenfassung des Erreichten,
* eine klare Formulierung der offenen Punkte,
* eine Empfehlung für den nächsten Schritt (weiter im gleichen Chat, neuer Chat, neues Issue, Persistenz),
* einen Verweis auf betroffene Dokumente oder Speicherorte im Repository,
* und – falls relevant – eine kurze Risiko- oder Konsistenzprüfung.

Diese Pflichtschritte sichern die Anschlussfähigkeit und verhindern Informationsverlust.

### 1.3 Gründe für den Abschluss

Es gibt unterschiedliche Anlässe, an denen ein Chat sinnvoll abgeschlossen werden sollte. Ein Abschluss erfolgt nicht nur, wenn alle Inhalte final sind, sondern auch, wenn ein methodischer oder struktureller Übergang bevorsteht. Typische Gründe sind:

* das Ende einer Mikroprozess-Einheit,
* der Übergang zwischen zwei Makroprozessphasen,
* ein Wechsel der Abstraktionsebene oder ein struktureller Sprung (z. B. Wechsel in ein anderes Kapitel),
* ein Ergebnis ist „gut genug“ für Persistenz oder Konsolidierung,
* oder die Vermeidung unnötiger Chat-Länge und damit verbundener Kontextdrift.

Der Abschluss dient also sowohl der inhaltlichen Sauberkeit als auch der methodischen Stabilität.

## 2. Kriterien für „Neuer Chat notwendig“

Ein neuer Chat wird immer dann erforderlich, wenn die aktuelle Unterhaltung ihre funktionale Grenze erreicht hat – sei es inhaltlich, strukturell oder technisch. Ziel ist es, Kontextdrift zu vermeiden, klare methodische Übergänge einzuhalten und den Arbeitsfluss sauber zu strukturieren. Die folgenden Kategorien erläutern, wann ein Neustart sinnvoll oder sogar zwingend notwendig ist.

### 2.1 Inhaltliche Kriterien

Diese Kriterien greifen, wenn sich der fachliche Inhalt soweit verändert, dass der laufende Chat nicht mehr den passenden Rahmen bietet. Ein neuer Chat ist notwendig, wenn:

* eine deutliche Kontextdrift erkennbar wird,
* ein Themen- oder Aufgabenwechsel erfolgt,
* oder die Granularität wechselt (z. B. von einer Gesamtübersicht zu einem tiefen Detailkapitel oder umgekehrt).

Ein Neustart stellt in diesen Fällen sicher, dass der neue Fokus klar und ohne Altlasten verfolgt werden kann.

### 2.2 Strukturelle Kriterien

Hier geht es um methodische Wechsel, bei denen der laufende Chat seine Funktion verliert. Ein neuer Chat sollte begonnen werden, wenn:

* eine neue Prozessphase im Makroprozess startet,
* die Rolle des LLM wechselt (z. B. von Methodiker zu Reviewer),
* der Arbeitsmodus sich verändert (Brainstorming → Konsolidierung),
* oder die Projektanweisung sonst überladen würde.

Ein neuer Chat schafft in diesen Situationen einen klaren methodischen Rahmen und hält die Struktur stabil.

### 2.3 Technische/Pragmatische Kriterien

Manchmal ist ein neuer Chat weniger aus inhaltlichen Gründen erforderlich, sondern aus Gründen der Übersichtlichkeit oder technischen Begrenzung. Ein neuer Chat ist ratsam, wenn:

* der Chat sehr lang geworden ist,
* die Übersicht verloren geht,
* ein Teilprozess sauber abgegrenzt dokumentiert werden soll,
* oder ein strukturiertes Ergebnis bewusst „frisch“ erzeugt werden soll.

Damit bleibt der Arbeitsverlauf klar, und Ergebnisse werden nicht in langen Chatverläufen „versteckt“.

### 2.4 Absolute Grenzen

Diese Kriterien erzwingen einen neuen Chat. Sobald eine dieser Situationen eintritt, darf im alten Chat nicht weitergearbeitet werden:

* Wenn ein Zwischenstand ins Repository geschrieben wurde → neuer Chat.
* Wenn eine andere Person übernimmt → neuer Chat.
* Wenn ein Issue geschlossen oder eröffnet wird → idealerweise neuer Chat, um einen sauberen Übergabe- und Startpunkt zu setzen.

Diese Grenzen verhindern, dass Persistenz, Verantwortlichkeiten oder Arbeitsphasen ineinanderlaufen.


## 3. Übergabevorlagen (Handover-Templates)

Die folgenden Templates dienen dazu, Übergaben klar, vollständig und strukturiert zu gestalten. Sie kommen immer dann zum Einsatz, wenn eine Arbeitseinheit endet und eine neue beginnt, sei es innerhalb eines Chats, zwischen Chats, beim Anlegen eines Issues oder beim Überführen von Ergebnissen ins Repository.

### 3.1 Template: Übergabe an neuen Chat

Dieses Template wird genutzt, wenn ein neuer Chat gestartet werden soll, um Kontext sauber zu übergeben — z. B. nach einem Themenwechsel, einer abgeschlossenen Mikroprozess-Einheit oder zur Vermeidung von Kontextdrift. Es fasst den bisherigen Stand zusammen und bereitet den nächsten Chat so vor, dass er direkt anschlussfähig weiterarbeiten kann.

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

Dieses Template wird verwendet, wenn eine Aufgabe aus dem Chat heraus in ein GitHub-Issue überführt werden soll — typischerweise bei klar abgrenzbaren Teilaufgaben, offenen Punkten, Persistenzschritten oder Entscheidungen, die nicht im Chat selbst bearbeitet werden sollen. Es dient als vollständige, strukturierte Beschreibung für das Issue.

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

Dieses Template kommt zum Einsatz, wenn Ergebnisse endgültig in das Repository übertragen werden sollen — also bei konsolidierten Inhalten, überarbeiteten Dokumenten oder stabilen Zwischenständen. Es stellt sicher, dass der Persistenzschritt vollständig nachvollziehbar ist und strukturiert ausgeführt wird.

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

Dieses Template wird genutzt, wenn eine Aufgabe an eine spezifische Person oder Rolle übergeben wird — etwa für Reviews, fachliche Klärungen, strukturelle Ergänzungen oder Persistenzschritte. Es stellt sicher, dass die empfangende Person alle notwendigen Informationen sofort vorliegen hat.

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

Ein Zwischenstand dient dazu, den aktuellen Arbeitsfortschritt präzise festzuhalten und ihn für weitere Chats, Issues oder Persistenzschritte nutzbar zu machen. Damit diese Zwischenstände konsistent bleiben, folgen sie immer derselben Grundstruktur.

### Pflichtfelder

Ein vollständiger Zwischenstand enthält:

* **Titel / Arbeitseinheit:** eine kurze, eindeutige Bezeichnung.
* **Ziel des Zwischenstands:** 1–2 Sätze, die erklären, warum dieser Zwischenstand erstellt wird und welchen Zweck er erfüllt.
* **Ergebnisse:** die zentralen Inhalte in klarer Form, z. B. als Listen, Tabellen oder Modelle.
* **Offene Punkte:** alles, was bewusst noch ungeklärt ist oder in einer nächsten Einheit bearbeitet werden soll.
* **Empfehlung für den nächsten Schritt:** klare Orientierung, wie weitergearbeitet werden sollte.
* **Speicherort / Dokumentenbezug:** Hinweise darauf, wo die Inhalte später im Repository landen oder welche Dateien betroffen sind.

### Optionale Felder

Falls relevant, können zusätzlich enthalten sein:

* **Risiken:** mögliche Unklarheiten, Abhängigkeiten oder Problemstellen.
* **Varianten:** alternative Lösungswege, die bereits diskutiert oder angedeutet wurden.
* **Entscheidungsvorlagen:** strukturierte Vorbereitung für anstehende Entscheidungen.
* **Betroffene Rollen:** wer in der nächsten Einheit benötigt wird (Methodiker, Reviewer, Fachexperten usw.).

### Abgrenzung

Ein Zwischenstand ersetzt **keine Persistenz**. Er dokumentiert den aktuellen Stand, ist aber noch nicht die finale Version eines Dokuments.

Zwei Regeln sind entscheidend:

* Ein Zwischenstand enthält **keine finalen oder konsolidierten Inhalte** – diese werden erst in Phase 5 in das Repository überführt.
* Er vermeidet **Redundanzen** und konzentriert sich auf eine präzise Verdichtung des bisherigen Fortschritts.




## 5. Speicherorte & Versionierung

Übergaben und Abschlüsse erzeugen Ergebnisse, die **dauerhaft gesichert**, **auffindbar**, **versioniert** und **wiederverwendbar** sein müssen. Damit diese Ergebnisse nicht im Chat „verloren“ gehen, sondern korrekt in das Dokumentationssystem überführt werden, definiert dieser Abschnitt:

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

Übergaben erzeugen Inhalte, die dauerhaft erhalten bleiben müssen. Damit diese Ergebnisse nachvollziehbar, sauber versioniert und konsistent in die Dokumentation eingebettet sind, gelten die folgenden Leitlinien. Sie bilden gemeinsam den Standard für jede Form von Persistenz im Projekt.

### Veränderungen müssen commitbar sein

Jede bestätigte Übergabe führt zu mindestens einem Commit im Repository. Nichts bleibt ausschließlich im Chat – alle relevanten Ergebnisse werden schriftlich festgehalten und versioniert. So entsteht eine verlässliche Chronologie der Entwicklung.

### Commit-Messages folgen einem klaren Format

Damit die Commit-Historie verständlich bleibt, werden Commit-Messages nach einem einheitlichen Muster formuliert:

```
Add/update <datei>: <kurze Beschreibung>
```

Beispiele:

- `Add handover-and-closure.md: initial version`
- `Update process-macro.md: phase 3 consolidated`
- `Add persistence rules: new quality section`

Diese Standardisierung ist wichtig, damit sowohl Menschen als auch das LLM schnell erkennen, worum es im jeweiligen Commit geht.

### Metadaten müssen aktuell sein

Jedes Dokument beginnt mit einem Header (Titel, Kategorie, Version, Status, verwandte Dateien). Dieser Block ist Teil der Informationsarchitektur und muss bei jeder Änderung aktualisiert werden – beispielsweise durch Anheben der Version oder Ergänzen der Verweise.  So bleibt jedes Dokument eindeutig einzuordnen und korrekt verlinkt.

### Backlinks gehören ans Ende jeder Datei

Am Ende jeder Datei steht ein Abschnitt **„Weiterführende Dokumente“**. Dieser dient als Navigations- und Strukturanker und ist wesentlich für die methodische Kohärenz:

- Er ermöglicht dem LLM, Zusammenhänge zwischen Dokumenten zuverlässig zu erkennen.  
- Er verhindert, dass Dateien isoliert stehen oder Informationen doppelt entstehen.  
- Er erleichtert Menschen die Orientierung, indem verwandte Dokumente sichtbar verbunden bleiben.

Mindestens **2–4 Backlinks** sollten gesetzt werden, idealerweise innerhalb desselben Themenbereichs (z. B. Prozesse, Struktur, Qualität).

### Größere Arbeitspakete müssen separat erfasst und versioniert werden

Nicht jede Übergabe ist klein. Sobald mehrere Dateien betroffen sind oder ein Arbeitsschritt über Prozessphasen hinweg wirkt, gelten verschärfte Regeln.

Ein Arbeitspaket gilt als „größer“, wenn zum Beispiel:

- mehrere Dokumente gleichzeitig angepasst werden,
- konsolidierte Inhalte mehrere Prozessphasen betreffen,
- neue Dokumente entstehen, die die Gesamtstruktur beeinflussen,
- die Änderung schwer rückgängig zu machen wäre,
- ein klarer Meilenstein dokumentiert werden soll.

In solchen Fällen erfolgt der Umgang zweistufig:

#### 1. Ein neues Issue anlegen

Das Issue dokumentiert:

- Inhalt und Ziel des Arbeitspakets  
- alle betroffenen Dateien  
- die erforderlichen Schritte  
- die logische Zuordnung zu Commits  

So bleibt die Bearbeitung transparent und zuweisbar.

#### 2. Ein Mini-Release erstellen

Ein Mini-Release (z. B. `v0.3.1`) markiert den Zustand nach Abschluss des Arbeitspakets. Das ist wichtig, weil:

- größere Änderungen sauber versioniert sein müssen,
- spätere Arbeitsschritte darauf aufbauen können,
- der Projektverlauf klar nachvollziehbar bleibt,
- der Zustand jederzeit reproduzierbar ist.

**Kurz gesagt:**  
Größere Übergaben → eigenes Issue + Mini-Release → volle Nachvollziehbarkeit und Stabilität.





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

## 7 Zusammenfassung und Fazit

Der Handover- und Abschlussprozess bildet einen zentralen Baustein der gesamten Methodik. Er stellt sicher, dass Ergebnisse aus Chats nicht im Verlauf verloren gehen, sondern strukturiert dokumentiert, korrekt übergeben und stabil im Repository verankert werden. Durch einheitliche Regeln für Zwischenstände, klare Kriterien für den Abschluss eines Chats und nachvollziehbare Übergaben entsteht ein konsistenter Arbeitsfluss, der über mehrere Phasen hinweg tragfähig bleibt.

Standardisierte Formate, definierte Speicherorte und eindeutige Versionierungsregeln ermöglichen es sowohl Menschen als auch dem LLM, jederzeit sicher zwischen Dokumenten, Phasen und Aufgaben zu navigieren. Gleichzeitig schützen Backlinks, Commit-Standards und die konsequente Trennung zwischen Zwischenstand und finaler Persistenz vor Drift, Redundanzen und inkonsistenten Informationsflüssen.

Insgesamt stärkt dieser Prozess die Nachvollziehbarkeit, die Qualität und die Wiederverwendbarkeit der Arbeitsergebnisse. Er legt fest, wie Wissen übergeben, gespeichert und gepflegt wird – und schafft damit die Grundlage für eine langfristig stabile, methodisch saubere und kollaborative Zusammenarbeit zwischen Mensch und LLM.

## 8 Weiterführende Dokumente
- Makroprozess – Phase 6  
- Mikroprozess  
- Persistenzmechanismen  
- Informationsarchitektur  
