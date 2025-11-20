# Methodology Building Blocks (Ausführliche Version – Style C)

Dieses Dokument enthält **ausführliche, tiefgehende Beschreibungen** aller Bausteine der Methodologie.  
Jeder Baustein umfasst:
- Zweck (mit Abgrenzungen)  
- Inhalte (detailliert, inkl. Beispielen)  
- Schnittstellen (konkret erklärt)  
- typische Artefakte (einsatznah)  
- Verantwortlichkeit (LLM/Nutzer)  
- typische Fehlerquellen  
- Praxis-Hinweise  
- Mini-Checkliste  

# 1. Steuerlogik (Projektanweisung)

## Zweck
Die Steuerlogik definiert die **dauerhaften Regeln**, unter denen die LLM-Zusammenarbeit stattfindet.  
Sie wirkt wie ein *methodisches Betriebssystem*: stabil, klar, immer aktiv.

### Was gehört dazu?
- Rollen (LLM als Methodiker, Reviewer, Strukturgeber)
- Formatvorgaben (Markdown, Tabellen, Gliederungen)
- Arbeitsweise (iterativ, präzise, keine Ausschweifungen)
- Rückfragenregeln
- Konsistenzprinzipien

### Was gehört NICHT dazu?
- fachliche Inhalte  
- Projektentscheidungen  
- längere Dokumentationstexte

### Beispiel
„Immer Markdown, klare Struktur, keine Ausschweifungen, Rückfragen bei Unklarheiten.“

## Inhalte (detailliert)
- Output-Standards  
- Rollenaktivierung  
- Kommunikationsstil  
- Toleranzgrenzen für Abweichungen  
- Definition von Qualität (Klarheit, Struktur, Anschlussfähigkeit)

## Schnittstellen
- **Mikroprozesse:** Die Steuerlogik definiert, wie Chat-Schritte aussehen.  
- **Drift-Management:** Steuerlogik = Referenz, an der Drift gemessen wird.  
- **Persistenz:** Definiert, was als „persistierbarer Output“ gilt.

## Typische Artefakte
- Projektanweisung  
- Verhaltensregeln  
- Rollenprofile  

## Verantwortlichkeit
- **Nutzer:** erstellt, ändert  
- **LLM:** befolgt, meldet Abweichungen  

## Typische Fehler
- zu viele Regeln  
- instabile Projektanweisung  
- Vermischen von Steuerlogik und Inhaltsdokumenten

## Praxis-Hinweise
- nur selten anpassen  
- maximal 0,5–1 Seite Inhalt  
- klar, knapp, präzise

## Checkliste
- Ist die Steuerlogik kurz?  
- Klar formuliert?  
- Frei von fachlichen Inhalten?  

# 2. Externe Wissensbasis (Repository)

## Zweck
Das Repository ist der **dauerhafte Wissensspeicher** des gesamten Projekts.  
Es verhindert Wissensverlust und dient als Referenz für alle Chats.

## Inhalte (detailliert)
- Dokumentationsstruktur  
- Inhaltsverzeichnis  
- versionierte Markdown-Dateien  
- Prozessdefinitionen  
- Entscheidungen & Logs

## Schnittstellen
- **Persistenz:** Welche Ergebnisse müssen wohin?  
- **Makroprozesse:** Jede Phase erzeugt Repo-Dokumente.  
- **Drift-Management:** Repo-Inhalte sind der stabile „Anker“.

## Typische Artefakte
- `docs/` Ordner  
- Strukturübersicht  
- Roadmaps  
- Prozess-Dokumente  

## Verantwortlichkeit
- **Nutzer:** pflegt  
- **LLM:** nutzt als Wissensquelle

## Fehlerquellen
- „Chat-Wissen“ nicht ins Repo überführen  
- unklare Dateinamen  
- fehlende Verlinkungen

## Praxis-Hinweise
- immer mit `docs/README.md` arbeiten  
- konsistente Dateistruktur halten

## Checkliste
- Ist jedes Ergebnis im Repo persistiert?  
- Existieren doppelte Inhalte?  

# 3. Makroprozesse

## Zweck
Beschreiben den **langfristigen, übergeordneten Ablauf** (Phasen 1–8) für komplexe Vorhaben.

## Inhalte (detailliert)
- Ziele jeder Phase  
- Inputs/Outputs  
- Rollen  
- Übergabekriterien  
- Beispielhafte Durchläufe

## Schnittstellen
- **Mikroprozesse:** Makro = Orientierung, Mikro = operative Arbeit  
- **Persistenz:** Phase 4–6 spezifizieren Überführung  
- **Übergaben:** formelle Anschlussfähigkeit

## Typische Artefakte
- `process-macro.md`  
- Phasenmodelle  
- Swimlane-Diagramme  

## Verantwortlichkeit
- **Nutzer & LLM gemeinsam**

## Fehlerquellen
- Phasen vermischt oder übersprungen  
- fehlende Übergabeformate  
- zu viel Detail in Makroprozessen

## Praxis-Hinweise
- Makroprozess ist *stabil*, selten ändern  
- Der wichtigste Referenzpunkt für alle Beteiligten

## Checkliste
- Sind alle Phasen klar abgegrenzt?  
- Hat jede Phase definierte Outputs?  

# 4. Mikroprozesse

## Zweck
Definieren die **operative Ablaufsteuerung innerhalb eines Chats**.

## Inhalte (detailliert)
- Analyse-Phase  
- Klärungsphase  
- Erzeugungsphase  
- Review-Phase  
- Iterationsschleifen  
- Rollenorientierung  

## Schnittstellen
- **Makroprozesse:** Mikro füllt Makro mit Leben  
- **Chat-Design:** spezifische Prompt-Struktur  
- **Drift-Management:** Mikro ist der Ort zur Drift-Prüfung

## Typische Artefakte
- Mikroprozess-Schema  
- Ablaufdiagramme  
- Prompt-Sequenzen  

## Verantwortlichkeit
- **Nutzer:** führt Prozess  
- **LLM:** strukturiert Antworten entsprechend  

## Fehlerquellen
- Sprung ohne Klärungsphase  
- zu früh in die Erzeugung  
- fehlende Review-Schritte

## Praxis-Hinweise
- Mikroprozesse sind *das Herzstück* für Qualität  
- immer in kleinen Iterationen denken

## Checkliste
- Wurde jeder Schritt explizit durchlaufen?  
- Wurden Rückfragen geklärt?  

# 5. Chat-Design

## Zweck
Strukturiert die **einzelnen Chat-Nachrichten und die Art der Kommunikation**.

## Inhalte (detailliert)
- Prompt-Struktur  
- Rollenansprache  
- Sequenzierung  
- Formatregeln  
- Kontrollfragen  
- strukturelle Hinweissignale  

## Schnittstellen
- **Mikroprozess:** Chat-Design steuert die operativen Schritte  
- **Drift-Management:** Gute Prompts verhindern Drift  
- **Rollen:** Rollen müssen über Prompts aktiviert werden

## Artefakte
- Prompt-Templates  
- Design-Guides  
- Formulierungsbausteine  

## Verantwortlichkeit
- **Nutzer:** entwirft Prompts  
- **LLM:** interpretiert und strukturiert sie

## Fehlerquellen
- unscharfe Prompts  
- zu viele Themen auf einmal  
- fehlende Rollenaktivierung

## Praxis-Hinweise
- Ein guter Prompt = klare Rolle + Format + Zweck  
- Immer explizit sein  

## Checkliste
- Ist Rolle klar?  
- Format definiert?  
- Ziel explizit benannt?  

# 6. Begriffs- und Strukturmanagement

## Zweck
Sorgt für **stabile Sprache und konsistente Strukturachsen**.

## Inhalte (detailliert)
- Glossar  
- Namenskonventionen  
- Strukturmodelle  
- Domain-spezifische Terminologie  
- Hierarchien (Prozess, Rollen, Artefakte)

## Schnittstellen
- **Makroprozesse:** konsistente Sprache  
- **Mikroprozesse:** Verwendung des Glossars  
- **Drift-Management:** Begriffsabweichungen erkennen

## Artefakte
- glossary.md  
- Begriffsmatrizen  
- Strukturübersichten  

## Verantwortlichkeit
- **Nutzer:** entscheidet  
- **LLM:** verwendet

## Fehlerquellen
- Begriffe ändern sich unbewusst  
- widersprüchliche Formulierungen  
- fehlende zentrale Übersicht

## Praxis-Hinweise
- Glossar ist lebendes Dokument  
- immer auf Begriffsklarheit prüfen

## Checkliste
- Ist jeder Begriff eindeutig?  
- Wird er konsistent genutzt?  

# 7. Drift-Management

## Zweck
Erkennt und verhindert **Kontextdrift**, **Logikdrift** und **Strukturdrift**.

## Inhalte (detailliert)
- Driftarten (semantisch, logisch, strukturell)
- Drift-Indikatoren  
- Prüfmechanismen  
- „Reset“-Mechanismen  
- Drift-Protokolle

## Schnittstellen
- **Chat-Design:** Prompts als Schutzmechanismus  
- **Persistenz:** regelmäßiger Reset auf Repo-Wissen  
- **Begriffsmanagement:** Wortwahlprüfung

## Artefakte
- Drift-Checklisten  
- Reviewfragen  
- Wiederverankerungsprompts  

## Verantwortlichkeit
- **LLM:** meldet Drift  
- **Nutzer:** korrigiert

## Fehlerquellen
- zu seltene Drift-Checks  
- unpräzise Sprache  
- zu lange Chats ohne Zusammenfassung

## Praxis-Hinweise
- Jede Iteration endet mit Mini-Drift-Check  
- Bei Unsicherheit: Zusammenfassung anfordern

## Checkliste
- Hat sich die Terminologie verschoben?  
- Sind Aussagen widersprüchlich?  

# 8. Persistenz-Mechanismen

## Zweck
Überführung von Chat-Ergebnissen in versionierte, langlebige Repository-Dokumente.

## Inhalte (detailliert)
- Commit-Standards  
- Naming-Regeln  
- Persistenz-Trigger (wann persistieren?)  
- Überführungsprozesse  
- Aggregation mehrerer Iterationen

## Schnittstellen
- **Makroprozesse:** definieren Zeitpunkte  
- **Repository:** Zielsystem  
- **Übergaben:** formelle Endpunkte

## Artefakte
- Markdown-Dokumente  
- Commit-Messages  
- Releases  

## Verantwortlichkeit
- **Nutzer:** persistiert  
- **LLM:** bereitet Inhalte strukturiert vor

## Fehlerquellen
- zu seltenes Persistieren  
- unklare oder unvollständige Überführung  
- fehlende Commit-Standards

## Praxis-Hinweise
- Nach Abschluss jeder Phase persistieren  
- Commit-Messages klar & technisch halten

## Checkliste
- Wurde alles Wesentliche überführt?  
- Sind alte Versionen nachvollziehbar?  

# 9. Rollen des LLM

## Zweck
Definiert **methodische Rollen**, die der LLM einnehmen kann.

## Inhalte (detailliert)
- LLM-Methodiker: Struktur & Vorgehen  
- Reviewer: Konsistenz- und Qualitätsprüfung  
- Strukturgeber: Gliederung, Ordnung  
- Schreibassistent: Textproduktion  

## Schnittstellen
- **Mikroprozesse:** Rollen werden situativ aktiviert  
- **Chat-Design:** Prompts steuern Rollen

## Artefakte
- Rollenbeschreibungen  
- Aktivierungs-Prompts  

## Verantwortlichkeit
- **Nutzer:** aktiviert Rollen  
- **LLM:** führt aus  

## Fehlerquellen
- Rollen nicht explizit aktiviert  
- falsche Rollenkombinationen  
- vermischte Rollen

## Praxis-Hinweise
- Immer mit „Als LLM-Methodiker…“ beginnen  
- Rollen ideal kombinieren

## Checkliste
- Ist die Rolle klar aktiviert?  
- Passt sie zu dem Schritt des Mikroprozesses?  

# 10. Übergaben & Abschlussformate

## Zweck
Sichert eindeutige Zwischen- und Endstände für Qualität, Nachvollziehbarkeit und Weiterverwendung.

## Inhalte (detailliert)
- Übergabekriterien  
- Input/Output-Definitionen  
- finale Dokumente  
- Abschlussberichte  
- Issue-Abschlüsse  

## Schnittstellen
- **Makroprozesse:** Übergabepunkte  
- **Persistenz:** finalisierte Inhalte  
- **Repository:** dauerhafte Ablage

## Artefakte
- Übergabedokumente  
- Abschlussberichte  
- Release Notes  

## Verantwortlichkeit
- **Nutzer:** finalisiert  
- **LLM:** strukturiert vor  

## Fehlerquellen
- fehlende Übergabedokumente  
- unklare Outputs  
- unklare Verantwortlichkeit

## Praxis-Hinweise
- Übergabe muss immer schriftlich vorliegen  
- Issue-Abschlusskommentar = Pflicht  

## Checkliste
- Gibt es ein Abschlussdokument?  
- Sind Outputs eindeutig und vollständig?

# Gesamtzusammenhang

Alle Bausteine sind **ineinander verzahnt** und bilden ein kohärentes System:  

- **Steuerlogik** gibt den methodischen Rahmen  
- **Repository** verankert Wissen dauerhaft  
- **Makro- & Mikroprozesse** strukturieren Arbeit  
- **Chat-Design** steuert die Kommunikation  
- **Begriffsmanagement** sichert Einheitlichkeit  
- **Drift-Management** hält Stabilität  
- **Persistenz** speichert Ergebnisse  
- **Rollen** operationalisieren das LLM  
- **Übergaben** schließen Arbeitspakete ab  

Das Zusammenspiel ermöglicht **reproduzierbare, nachvollziehbare und qualitativ hochwertige LLM-Zusammenarbeit**.

