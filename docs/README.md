# Dokumentationsübersicht – cher-llm-methodology

Dieses Verzeichnis enthält die interne Projektdokumentation der Methodik. Die Struktur folgt der definierten Informationsarchitektur aus `information-architecture.md` (#8).

## Foundations
Grundlagen und Kontext des Projekts.

- [mission-and-scope.md](foundations/mission-and-scope.md)
- [chatgpt-projects.md](foundations/chatgpt-projects.md)
- [preparation-summary.md](foundations/preparation-summary.md)
- [methodology-foundations.md](foundations/methodology-foundations.md)

## Prozesse
Makro- und Mikroprozesse der Zusammenarbeit mit dem LLM.

- [process-macro.md](processes/process-macro.md)
- [process-micro-chat.md](processes/process-micro-chat.md)
- [handover-and-closure.md](processes/handover-and-closure.md)

## Struktur & Rollen
Bausteine, Begriffe und Rollen der Methodik.

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

1. **Dokument in dieser Übersicht eintragen oder aktualisieren**  
   - korrekte Kategorie  
   - alphabetische Ordnung **innerhalb** der Kategorie empfohlen  
   - Statussymbole optional

2. **Backlink-Abschnitt am Ende jedes Dokuments**  
   ```md
   ## Weiterführende Dokumente
   – (werden im Verlauf ergänzt)
   ```

3. **Strukturänderungen zuerst hier pflegen**, dann im Repository umsetzen.

4. **docs/** = Arbeits- & Entwicklungsstand  
   **Wiki** = stabile Endversionen (keine Entwürfe)

---

*Version: v0.1 – Vollständige initiale Struktur umgesetzt*
