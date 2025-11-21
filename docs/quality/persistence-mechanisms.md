# Persistenzmechanismen für die LLM-Zusammenarbeit
*(Version v0.1 – vollständige Erstfassung)*

## 1. Zweck des Dokuments
Persistenzmechanismen stellen sicher, dass Begriffe, Strukturen, Ergebnisse und Konventionen in der LLM-Zusammenarbeit **dauerhaft stabil**, **nachvollziehbar** und **wiederverwendbar** bleiben.

Dieses Dokument beschreibt:
- welche Inhalte dauerhaft gesichert werden müssen,
- wie Chat-Ergebnisse korrekt in die Dokumentation überführt werden,
- welche Rollen dabei beteiligt sind,
- und wie Versionierung, Änderungsmanagement und Konsistenzsicherung funktionieren.

Persistenz ist ein zentrales Element von **Phase 5 (Persistenz) des Makroprozesses**.  
Sie bildet die Grundlage dafür, dass die Methode nachhaltig funktioniert — unabhängig von Chat-Verläufen.

## 2. Grundlagen der Persistenz
Persistenz bedeutet im Kontext der LLM-Zusammenarbeit:

> “Wissen, das für das Projekt wesentlich ist, wird außerhalb der Chats so dokumentiert, dass es **dauerhaft**, **versioniert** und **konsistent** verfügbar bleibt.”

Dabei gilt die zentrale Trennung:

- **Chat** = Ort der Erarbeitung (temporär)  
- **Repository** = Single Source of Truth (dauerhaft)

Persistenz ist notwendig, weil:
- ChatGPT-Kontexte enden oder driften können,
- Inhalte in Chats de facto nicht versionierbar sind,
- Entscheidungen später nachvollziehbar sein müssen,
- mehrere Menschen mit dem LLM arbeiten können.

## 3. Persistenzarten

### 3.1 Begriffe (Terminologie, Glossar)
- saubere Definitionen für verwendete Begriffe  
- klare sprachliche Eindeutigkeit  
- zentrale Ablage im Glossar oder in den jeweiligen Dokumenten  
- Vermeidung synonymen Nebengebrauchs

### 3.2 Strukturen (Prozesse, Rollen, Architektur)
- definierte Modelle und Abläufe  
- stabile Gliederungen  
- Prozessphasen (Makro-, Mikroprozesse)  
- Rollenmodelle und Verantwortlichkeiten

### 3.3 Ergebnisse (Dokumente, Artefakte, Modelle)
- Prozessdokumente  
- Tabellen, Diagramme  
- Templates  
- Methodische Modelle  
- Beispiele  

### 3.4 Konventionen (Formatregeln, Arbeitsweisen)
- Formatierungsvorgaben  
- Rollenlogik  
- Regeln für Iterationen  
- Kommunikationsprinzipien  

### 3.5 Beziehungen zwischen Persistenzarten
Persistenzarten bauen logisch aufeinander auf:

1. **Begriffe** → Grundlage  
2. **Strukturen** → Rahmensystem  
3. **Ergebnisse** → operative Artefakte  
4. **Konventionen** → verbindliche Regeln  

Jede Änderung auf einer unteren Ebene hat potenziell Auswirkungen auf obere Ebenen (z. B. Glossar → Prozessbeschreibung).

## 4. Prinzipien stabiler Persistenz

Die Persistenz folgt einer Reihe grundlegender Prinzipien, die sicherstellen, dass Inhalte langfristig stabil und nachvollziehbar bleiben:

- **Klarheit:** Inhalte müssen präzise formuliert sein und dürfen keine offenen Fragen oder Mehrdeutigkeiten enthalten.
- **Eindeutigkeit:** Alle Begriffe, Modelle und Strukturen müssen eindeutig definiert und voneinander abgegrenzt sein.
- **Versionierbarkeit:** Jede Änderung an Dokumenten muss über Git festgehalten werden. Persistierte Inhalte benötigen klar erkennbare Versionsstände.
- **Änderungsstabilität:** Persistiert werden nur gereifte, belastbare Inhalte. Explorative Ergebnisse aus Chats werden erst nach Konsolidierung übernommen.
- **Nachvollziehbarkeit:** Persistente Dokumente müssen verständlich sein, ohne den Chat-Verlauf nachlesen zu müssen. Entscheidungen und Varianten sollen dokumentiert werden.

## 5. Regeln zur Überführung von Chat-Ergebnissen ins Repository

### 5.1 Entscheidungsbaum: Wohin gehört welches Ergebnis?
| Art des Ergebnisses | Zielort |
|---------------------|---------|
| Methodische Inhalte, Prozesse, Modelle | `docs/` |
| Finalisierte, für Anwender bestimmte Inhalte | Wiki |
| Aufgaben, offene Punkte, ToDos | Issues |
| Entscheidungen, Alternativen, Varianten | decision-log |
| Kleinere Änderungen oder Fixes | Commit-Messages |

### 5.2 Wann kommen Inhalte ins Repository?
Ein Chat-Ergebnis wird persistiert, wenn:

- es **stabil** genug ist,  
- es **Teil der Methode** werden soll,  
- es **keine offene Prüffrage** mehr enthält,  
- es **reproduzierbar** sein muss,  
- es **in folgenden Chats referenziert** werden soll.

### 5.3 Wann werden Inhalte *nicht* übernommen?
- wenn das Ergebnis noch zu vage oder vorläufig ist,
- wenn Alternativen noch diskutiert werden,
- wenn der Chat ein exploratives Stadium hat,
- wenn der Inhalt redundant oder widersprüchlich ist.

### 5.4 Mindestanforderungen für Übernahme
Ein persistenzfähiger Inhalt muss:

- klar strukturiert sein,  
- sprachlich sauber sein,  
- keine offenen Fragen enthalten,  
- konsistent zu bestehenden Dokumenten sein,  
- eindeutig versionierbar sein.

## 6. Versionierte Dokumentationsmechanismen

### 6.1 Versionsstände in Markdown-Dateien
Jedes Dokument enthält:
- Versionsnummer  
- Status  
- Metadatenblock  

Versionierung erfolgt ähnlich wie bei Software:

- **Major** = große methodische Änderungen  
- **Minor** = Ergänzungen neuer Abschnitte  
- **Patch** = kleine Korrekturen  

### 6.2 Commit-Muster & Konventionen
Empfohlene Commit-Struktur:

```
<Scope>: <Kurze Erklärung>

Beispiel:
quality: Add persistence mechanisms v0.1
docs: Update macro process table formatting
structure: Fix terminology for method roles
```

### 6.3 Release-Konventionen (optional)
Bei größeren Meilensteinen:
- Release Notes  
- Tagging (z. B. v0.2)  
- Hinweis auf releasetechnische Änderungen  

### 6.4 Änderungsprotokolle / Changelogs
Für tiefergehende Änderungen:
- `CHANGELOG.md` im Repo  
- klare, strukturierte Änderungsbeschreibung  

### 6.5 Umgang mit Major/Mid/Minor-Änderungen
- Major nur nach Abstimmung  
- Minor bei Ergänzungen  
- Patch bei Korrekturen  

## 7. Rolle der zentralen Dokumentationsartefakte

### 7.1 README-Dateien
- Orientierungspunkte für Verzeichnisse  
- vermitteln Struktur, nicht Inhalt  
- enthalten Links, nicht komplette Dokumentation  

### 7.2 Wiki
- Endfassung für Nutzer  
- hochstabile Inhalte  
- keine Entwürfe oder Varianten  

### 7.3 decision-log
- Dokumentationsort für Entscheidungen  
- enthält Alternativen, Gründe, Auswirkungen  
- dient als methodische Revisionsquelle  

### 7.4 Issues
- Planungsinstrument  
- Ort für offene Punkte  
- dienen der Navigation für Chat-Ergebnisse  
- verknüpfen Chat → Repo  

### 7.5 Commits
- kleinste Einheit der Persistenz  
- dokumentieren jede Veränderung  
- erzeugen Revisionssicherheit  

## 8. Verfahren für Stabilisierung & Änderungsmanagement

### 8.1 Änderungsprozess (Change Cycle)
1. Identifikation einer möglichen Änderung  
2. Diskussion im Chat (Exploration)  
3. Ableitung eines konsolidierten Vorschlags  
4. Persistenz in `docs/`  
5. Commit + ggf. Decision-Log  
6. Abschluss oder Issue für Feintuning

### 8.2 Wann ist eine Änderung zulässig?
- wenn sie nachvollziehbar notwendig ist  
- wenn sie konsistent zu bestehenden Strukturen ist  
- wenn sie dokumentiert wird  

### 8.3 Wann braucht es ein neues Issue?
- bei größeren Änderungen  
- bei Erweiterungen eines Dokuments  
- wenn mehrere Dateien betroffen sind  

### 8.4 Umgang mit Breaking Changes
Breaking Changes müssen:
- klar dokumentiert werden  
- mit Begründung versehen sein  
- im Changelog landen  
- ggf. zu einer neuen Major-Version führen  

### 8.5 Übergabe in Wiki-Stabilität
Ein Dokument wandert ins Wiki, wenn:
- es final ist,  
- keine strukturellen Änderungen mehr zu erwarten sind,  
- es für Endnutzer gedacht ist.

## 9. Konsistenzprüfungen als Routine

### 9.1 Arten von Konsistenzprüfungen
- **begriffsbezogen**  
- **strukturell**  
- **dokumentarisch**  
- **prozessual**  

### 9.2 Regelmäßige Prüfzyklen
- alle wichtigen Dokumente mind. einmal pro Release prüfen  
- vor jeder Persistenzphase (Phase 5)  
- bei größeren Strukturänderungen  

### 9.3 Werkzeuge für Konsistenz
- interne Checklisten  
- Vergleich alter und neuer Dokumentversionen  
- Issues für festgestellte Abweichungen  

### 9.4 Dokumentation der Konsistenzprüfungen
- kurze Commit-Nachrichten  
- Issues für größere Abweichungen  
- Einträge im decision-log bei relevanten Änderungen  

## 10. Zusammenfassung
Persistenzmechanismen gewährleisten:

- dauerhaft stabile Begriffe,  
- konsistente Strukturen,  
- versionierte Ergebnisse,  
- saubere Konventionen,  
- klare Entscheidungswege,  
- nachvollziehbare Entwicklung.

Sie sind damit ein zentraler Baustein der Methodik und integraler Bestandteil des Makroprozesses.

## 11. Weiterführende Dokumente
- `drift-management.md`  
- `process-macro.md`  
- `document-types-and-storage.md`  
