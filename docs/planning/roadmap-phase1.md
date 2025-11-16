# Roadmap für Phase 1 – Bearbeitungsreihenfolge der Methodologie

## Version
v0.1 – Strukturierte Bearbeitungsreihenfolge für Phase 1 (Ideensammlung)

## 1. Zweck dieses Dokuments

Dieses Dokument beschreibt die empfohlene Reihenfolge der Bearbeitung aller Kern-Issues der Phase 1 des Projekts *cher-llm-methodology*.  
Die Reihenfolge ist so gewählt, dass Abhängigkeiten berücksichtigt und methodische Grundlagen zuerst geschaffen werden.

## 2. Gesamtübersicht der Bearbeitungsreihenfolge

Die Roadmap folgt zwei Prinzipien:

1. **Von grob → fein**: Zuerst das große Ganze, dann Details.  
2. **Von Grundlagen → Ableitungen**: Erst Strukturen, dann Mechanismen, dann Templates.

## 3. Schrittweiser Ablauf

### **Schritt 1 – Makroprozess definieren (Issue #11)** 
Ziel: Gesamtphasen der LLM-Zusammenarbeit definieren.  
Begründung: Der Makroprozess gibt den strukturellen Rahmen vor, an dem sich alle weiteren Elemente orientieren.
Link: https://github.com/hrmnns/cher-llm-methodology/blob/main/docs/processes/process-macro.md (Version 1.0)

### **Schritt 2 – Mikroprozess definieren (Issue #12)**  
Ziel: Struktur für jeden einzelnen Chat entwickeln.  
Begründung: Der Mikroprozess ist die operative Grundeinheit und baut direkt auf dem Makroprozess auf.

### **Schritt 3 – Methodische Bausteine präzisieren (Issue #9)**  
Ziel: Alle Bausteine (Steuerlogik, Prozesse, Persistenz, Rollen, Drift usw.) einzeln und systematisch definieren.  
Begründung: Erst nach Makro- und Mikroprozess ist klar, welche Bausteine benötigt werden und wie sie zusammenspielen.

### **Schritt 4 – Rollenmodell des LLM definieren (Issue #15)**  
Ziel: Klare Definition der Rollen, die das LLM einnimmt (Methodiker, Reviewer etc.).  
Begründung: Rollen ergeben sich aus den Prozessen – daher erst nach deren Definition.

### **Schritt 5 – Dokumenttypen & Speicherorte definieren (Issue #10)**  
Ziel: Regeln festlegen, welche Inhalte in `docs/`, Wiki, Issues oder decision-logs landen.  
Begründung: Die Struktur hängt direkt von Prozessen und Bausteinen ab und bildet die Grundlage für Persistenz.

### **Schritt 6 – Persistenz-Mechanismen ausarbeiten (Issue #13)**  
Ziel: Mechanismen festlegen, um Begriffe, Strukturen und Ergebnisse dauerhaft stabil zu halten.  
Begründung: Persistenz ist erst definierbar, wenn Dokumenttypen und Speicherorte klar sind.

### **Schritt 7 – Drift Management entwickeln (Issue #14)**  
Ziel: Maßnahmen zur Erkennung und Korrektur semantischen Drifts entwickeln.  
Begründung: Drift-Management setzt Persistenz, Prozesse und Rollen voraus.

### **Schritt 8 – Übergabe- und Abschlussformate definieren (Issue #16)**  
Ziel: Templates und Regeln für Chat-Ende, Übergaben und Chat-Neustarts.  
Begründung: Übergaben hängen von Prozessen, Rollen, Persistenz und Drift-Mechanismen ab – daher zuletzt.

## 4. Kompakte tabellarische Übersicht

| Schritt | Thema | Abhängigkeiten | Ergebnis |
|--------|--------|----------------|----------|
| 1 | Makroprozess | – | `process-macro.md` |
| 2 | Mikroprozess | Makroprozess | `process-micro-chat.md` |
| 3 | Methodische Bausteine | Makro + Mikro | `methodology-building-blocks.md` |
| 4 | Rollenmodell | Prozesse + Bausteine | `roles-llm.md` |
| 5 | Dokumenttypen & Speicherorte | Prozesse + Bausteine | `document-types-and-storage.md` |
| 6 | Persistenz | Dokumenttypen | `persistence-mechanisms.md` |
| 7 | Drift Management | Persistenz + Prozesse | `drift-management.md` |
| 8 | Übergaben | Alle vorherigen | `handover-and-closure.md` |

## 5. Zusammenfassung

Diese Roadmap minimiert Inkonsistenzen und vermeidet Doppelarbeit, da:

- Grundstrukturen zuerst gelegt werden,  
- alle abhängigen Dokumente logisch später folgen,  
- und jedes Dokument auf einem stabilen Fundament steht.

Damit ist eine saubere, nachvollziehbare Phase-1-Umsetzung gewährleistet.

*Ende des Dokuments.*
