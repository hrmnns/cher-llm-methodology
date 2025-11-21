# Dokumentationsübersicht – cher-llm-methodology

Dieses Verzeichnis enthält die interne Projektdokumentation der Methodik.  
Die Struktur folgt der definierten Informationsarchitektur aus  
[meta/information-architecture.md](meta/information-architecture.md).

## Foundations  
Grundlagen, Kontext und vorbereitende Arbeiten.

- [mission-and-scope.md](foundations/mission-and-scope.md)
- [chatgpt-projects.md](foundations/chatgpt-projects.md)
- [preparation-summary.md](foundations/preparation-summary.md)
- [methodology-foundations.md](foundations/methodology-foundations.md)

## Prozesse  
Makro- und Mikroprozesse der strukturierten Zusammenarbeit mit dem LLM.

- [process-macro.md](processes/process-macro.md)
- [process-micro-chat.md](processes/process-micro-chat.md)
- [handover-and-closure.md](processes/handover-and-closure.md)

## Struktur & Rollen  
Bausteine, Begriffe, Rollen und grundlegende Strukturprinzipien der Methodik.

- [methodology-building-blocks.md](structure/methodology-building-blocks.md)
- [roles-llm.md](structure/roles-llm.md)
- [document-types-and-storage.md](structure/document-types-and-storage.md)

## Qualitätssicherung  
Mechanismen zur Sicherstellung von Konsistenz, Persistenz und Driftkontrolle.

- [persistence-mechanisms.md](quality/persistence-mechanisms.md)
- [drift-management.md](quality/drift-management.md)

## Meta  
Governance, Standards und Regeln für Pflege & Weiterentwicklung.

- [decision-log-method.md](meta/decision-log-method.md)
- [document-metadata-standard.md](meta/document-metadata-standard.md)
- [maintenance-rules.md](meta/maintenance-rules.md)
- [information-architecture.md](meta/information-architecture.md)

# Pflege- und Aktualisierungsregeln

Bitte bei jeder Änderung folgende Schritte beachten:

1. **Dokument in dieser Übersicht aktualisieren**  
   - korrekte Kategorie wählen  
   - alphabetische Ordnung innerhalb der Kategorie empfohlen  
   - Statussymbole optional (✔ fertig, 🚧 in Arbeit, ⏳ geplant)

2. **Backlink-Abschnitt am Ende jedes Dokuments pflegen**  
   Beispiel:
   ```md
   ## Weiterführende Dokumente
   - process-macro.md
   - roles-llm.md
   ```
   (Backlinks immer thematisch sinnvoll setzen.)

3. **Strukturänderungen zuerst hier dokumentieren**,  
   danach im Repository in der tatsächlichen Verzeichnisstruktur umsetzen.

4. **docs/** = Arbeits- & Entwicklungsstand  
   **Wiki** = stabile Endversionen (keine Entwürfe, keine Work-in-Progress)

---

*Version: v0.2 – aktualisiert nach Ergänzung des Rollenmodells (`roles-llm.md`)*
