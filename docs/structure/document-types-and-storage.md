# Document Types and Storage  
Dieses Dokument definiert alle im Projekt *cher-llm-methodology* verwendeten Dokumenttypen, ihren Zweck, Speicherort, Formatvorgaben sowie Regeln für Versionierung und Aktualisierung. Es dient als verbindlicher Referenzrahmen der Dokumentationsarchitektur.

# 1. Zweck des Dokuments
Eine klare Struktur der Dokumenttypen ist notwendig, um:
- Wissensdrift zu verhindern  
- Redundanzen zu vermeiden  
- die Persistenz der Ergebnisse sicherzustellen  
- konsistente Navigation zu ermöglichen  
- den Übergang vom Arbeitsstand zur finalen Dokumentation zu steuern  

Dieses Dokument operationalisiert die Informationsarchitektur und definiert alle Dokumentarten präzise.

# 2. Überblick über alle Dokumenttypen
Das Projekt nutzt neun klar abgegrenzte Dokumenttypen:

1. **Projektanweisung** – Steuerlogik des LLM  
2. **README.md** – Einstiegspunkt des Projekts  
3. **Markdown-Dokumente (`docs/`)** – zentrale Wissensbasis  
4. **Wiki-Seiten** – stabile Endfassung  
5. **Issues** – Aufgabensteuerung  
6. **Decision Logs** – Entscheidungsdokumentation  
7. **Roadmaps / Planungsdokumente**  
8. **ChatGPT-Projektdateien**  
9. **Kontextmaterial (optional)**

Jeder Typ erfüllt einen klar definierten Zweck im Gesamtprozess.

# 3. Zweck, Inhalt & Verantwortlichkeiten der Dokumenttypen

## 3.1 Projektanweisung
**Zweck:** Definiert das Verhalten des LLM über viele Chats hinweg.  
**Inhalt:** Rollen, Formatregeln, Do/Don't, Iterationsprinzip.  
**Verantwortung:** Methodiker.  
**Änderungen:** selten, nur wohldosiert.  
**Risiko bei Fehlpflege:** Modell driftet → Inkonsequente Ergebnisse.

## 3.2 README.md (Projektwurzel)
**Zweck:** Orientierung, Einstieg, Strukturüberblick.  
**Inhalt:** Projektziel, Struktur, Links, Hinweise auf Arbeitsweise.  
**Verantwortung:** Methodiker & Dokumentationsverantwortliche.  
**Reifegrad:** stabil, aber bei Strukturänderungen zu aktualisieren.

## 3.3 Markdown-Dateien im `docs/`-Verzeichnis
Dies sind die **Arbeits- und Wissensdokumente**.

### Ordnerstruktur:
- `foundations/` – Grundlagen, Motivation  
- `processes/` – Makro- & Mikroprozesse  
- `structure/` – Rollen, Bausteine, Dokumenttypen  
- `quality/` – Persistenz, Drift-Management  
- `meta/` – Entscheidungsläufe, interne Entwicklungen  

**Zweck:** zentrale Wissensbasis, versioniert, iterativ.  
**Verantwortlich:** Methodiker, Reviewer, Dokumentationsverantwortliche.  
**Hinweis:** Inhalte gelangen später ins Wiki → Endfassung.

## 3.4 Wiki-Seiten
**Zweck:** öffentliche, finale Darstellung der Methode.  
**Inhalt:** klare, anwenderorientierte Darstellung der endgültigen Ergebnisse.  
**Reifegrad:** hoch – keine Entwürfe.  
**Verantwortlich:** Methodiker.  
**Regel:** Nur Inhalte der Phasen 5/6 (Persistenz & Abschluss).

## 3.5 Issues
**Zweck:** Aufgabensteuerung.  
**Inhalt:** Beschreibung, Kontext, Definition of Done, Verlinkung zu Docs.  
**Verantwortlich:** Projektleitung & Methodiker.  
**Struktur:** Standardisiertes Template.  
**Regel:** Jedes Dokument entsteht über ein Issue.

## 3.6 Decision Logs
**Zweck:** Nachvollziehbare Dokumentation aller relevanten Entscheidungen.  
**Inhalt:** Problem, Optionen, Entscheidung, Begründung, Datum.  
**Regel:** Niemals rückwirkend ändern, nur ergänzen.  
**Nutzen:** Revisionssicherheit & Konsistenz bei späteren Änderungen.

## 3.7 Roadmaps / Planungsdokumente
**Zweck:** Orientierung in mittel- und langfristigen Entwicklungen.  
**Inhalt:** Phasen, Priorisierung, offene Arbeitspakete.  
**Verantwortung:** Projektverantwortliche.  
**Regel:** Änderungen nur über Issues.

## 3.8 ChatGPT-Projektdateien
**Zweck:** Steuerung der Chat-Umgebung (z. B. Projektanweisung).  
**Speicherort:** ChatGPT-Projekt selbst.  
**Regel:** Nur stabile Inhalte, niemals WIP.

## 3.9 Kontextmaterial
**Zweck:** ergänzendes Material (z. B. Skizzen, Notizen).  
**Regel:** optional; gehört nicht zur offiziellen Doku.  

# 4. Speicherort je Dokumenttyp

| Dokumenttyp | Speicherort | Zweck |
|-------------|-------------|--------|
| Projektanweisung | ChatGPT-Projekt | stabile Steuerlogik |
| README.md | Repo-Wurzel | Orientierung |
| Foundations | `docs/foundations/` | Grundlagen |
| Prozesse | `docs/processes/` | Phasen & Abläufe |
| Struktur | `docs/structure/` | Rollen, Bausteine |
| Qualität | `docs/quality/` | Validität & Konsistenz |
| Decision Logs | `docs/meta/` | Entscheidungsbasis |
| Roadmaps | `docs/planning/` | Planung |
| Wiki | GitHub Wiki | Endfassung |

# 5. Formatvorgaben

## 5.1 Markdown-Regeln
- UTF‑8  
- klare Überschriften: H1–H3  
- Tabellen bevorzugt für strukturierte Inhalte  
- keine HTML-Formatierung außer wenn zwingend nötig  
- keine dekorativen Elemente

## 5.2 Metadatenblock
Jede Datei im `docs/`:

```md
---
title: …
category: …
version: …
status: …
related: [a.md, b.md]
---
```

## 5.3 Verlinkungen
- relative Links  
- Backlinks am Dokumentende  
- kein Link auf trunkierte URLs

## 5.4 Dateinamen
- lowercase  
- keine Umlaute  
- keine Leerzeichen  
- keine Versionsnummern im Namen  

# 6. Beispielinhalte je Dokumenttyp

## Beispiel: Prozessdokument (Auszug)
```md
# Phase 3 – Operative Bearbeitung
Ziel: Inhalte iterativ gemeinsam mit dem LLM erarbeiten.
```

## Beispiel: Decision Log (Auszug)
```md
## Entscheidung 2025-01-12
**Problem:** Zwei Varianten der Phasenstruktur.  
**Entscheidung:** Variante A (8 Phasen).  
**Begründung:** höhere Klarheit & Pilotierbarkeit.
```

## Beispiel: Issue
```md
### Aufgabe
Erstelle das Dokument „roles-llm.md“.

### Definition of Done
- Rollenliste vollständig
- Zuständigkeiten beschrieben
```

# 7. Regeln für Aktualisierung & Versionierung

## 7.1 Aktualisierungsanlässe
- neue Erkenntnisse  
- strukturelle Änderungen  
- Konsolidierung (Phase 4)  
- Persistenz (Phase 5)  

## 7.2 Versionierung
- Version im Metadatenblock erhöhen  
- Commit-Messages nach konventionellem Muster  
- Dokumentiert durch entsprechende Issues  

## 7.3 Übergang docs → Wiki
Nur wenn:
- konsolidiert  
- freigegeben  
- final formuliert  

## 7.4 Breaking Changes
- zwingend ins Decision Log  
- klarer Hinweis im Commit  

# 8. Matrix „Was gehört wohin?“
| Inhalt | Typ | Speicherort | Format | Reifegrad | Verantwortlich | Aktualisierung |
|--------|------|-------------|--------|-----------|----------------|----------------|
| Grundlagen | foundations | docs/foundations | md | mittel–hoch | Methodiker | bei Änderungen |
| Phasen | processes | docs/processes | md | mittel–hoch | Methodiker | iterativ |
| Rollen | structure | docs/structure | md | mittel | Methodiker | bei Bedarf |
| Dokumenttypen | structure | docs/structure | md | hoch | Methodiker | selten |
| Drift-Management | quality | docs/quality | md | mittel–hoch | Methodiker | regelmäßig |
| Persistenz | quality | docs/quality | md | mittel–hoch | Methodiker | regelmäßig |
| Entscheidungen | decision-log | docs/meta | md | mittel | Methodiker | fortlaufend |
| Planung | roadmap | docs/planning | md | variabel | Projektleitung | bei Repriorisierung |
| Endfassung | wiki | GitHub Wiki | md | hoch | Methodiker | nach Phase 6 |

# 9. Zusammenfassung
Dieses Dokument bildet die verbindliche Grundlage für:
- klare Zuordnung von Inhalten  
- strukturierte Ablage  
- konsistente Versionierung  
- eine stabile Wissensbasis  
- den Übergang von Arbeitsständen zu finalen, reifen Dokumenten  

Es ist zentraler Bestandteil des methodischen Fundaments der gesamten LLM-Methodologie.

# 10. Weiterführende Dokumente
- information-architecture.md  
- persistence-mechanisms.md  
- decision-log-method.md  
