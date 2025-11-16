# Foundations der Methodologie zur strukturierten Zusammenarbeit mit LLMs

## Version
v0.1.0 – Erstfassung der Grundlagen

---

## 1. Zweck dieses Dokuments

Dieses Dokument beschreibt die grundlegenden Ausgangsbedingungen, Herausforderungen und Anforderungen, die berücksichtigt werden müssen, um eine belastbare Methodologie für die Zusammenarbeit mit Large Language Models (LLMs) in komplexen Projekten zu entwickeln.

Es bildet das Fundament für alle weiteren Schritte in Phase 1.

## 2. Ausgangspunkt: Warum Zusammenarbeit mit LLMs komplex ist

Die praktische Arbeit mit LLMs in umfangreichen Projekten zeigt klar, dass ohne methodische Begleitung typische Probleme auftreten. Diese Herausforderungen definieren den Problemraum, den die Methodologie adressieren muss.

### 2.1 Kontextdrift  
LLMs verlieren über mehrere Chats hinweg Kohärenz. Frühere Definitionen, Entscheidungen oder Regeln werden nicht dauerhaft berücksichtigt.

### 2.2 Inkonsistente Begriffsverwendung  
Begriffe, Rollen, Architekturen oder Strukturvorgaben verändern sich im Verlauf, wenn sie nicht explizit stabilisiert werden.

### 2.3 Fehlende Wiederholbarkeit  
Ergebnisse lassen sich selten exakt reproduzieren. Variabilität ist erwünscht, aber in komplexen Vorhaben hinderlich, wenn Präzision oder Nachvollziehbarkeit gefordert ist.

### 2.4 Fehlende Struktur in der Konversation  
Chats tendieren zu vermischten Ebenen, Brüche in der Struktur, unklaren Arbeitsphasen und fehlenden Übergaben.

### 2.5 Wechsel zwischen Inhaltsebene und Metaebene  
Das Modell springt zwischen „Problemlösen“ und „die Methode erklären“. Ohne klare Trennung entsteht semantischer Drift.

### 2.6 Persistenz- und Versionsprobleme  
LLMs speichern Wissen nicht dauerhaft; Chatverläufe sind ephemer. Ohne externe Versionierung gehen Erkenntnisse verloren oder verwässern.

### 2.7 Schwierigkeit, Zwischenergebnisse festzuhalten  
Chats sind kein Repository – sinnvolle Teilergebnisse verschwinden im Verlauf, wenn sie nicht gezielt extrahiert werden.

### 2.8 Multiple Rollen des LLMs  
LLMs können Methodiker, Architekt, Reviewer, Übersetzer, Systematiker, Autor etc. sein. Ohne Rollenklarheit entstehen Inkonsistenzen und Rollenwechsel „zwischen den Zeilen“.

## 3. Anforderungen an eine belastbare Methodologie

Aus den Herausforderungen ergeben sich klare Anforderungen. Die Methodologie muss definieren, wie ein systematischer und kontrollierter Arbeitsprozess entsteht.

### 3.1 WIE arbeitet man mit dem LLM?
- klare Rollen für das Modell  
- definierte Arbeitsmodi (Erarbeitung, Review, Meta, Strukturierung)  
- Regeln für Ebenenwechsel  
- stabile Gesprächsstruktur (Schritte, Phasen)

### 3.2 WIE werden Ergebnisse strukturiert?
- Abgrenzung Chat ↔ Repository
- definierte Dokumenttypen (README, Architektur, Entscheidungen, Glossare etc.)
- Regeln für Dokumentation im `docs/`-Verzeichnis und im Wiki
- sauberer Umgang mit Issues und Commits

### 3.3 WIE verhindert man semantischen Drift?
- stabile Begriffsdefinitionen
- Projektanweisung als dauerhafte Steuerlogik
- regelmäßige Konsistenzchecks
- abgesicherte Versionierung im Repository
- klare Übergabeformate zwischen Chats

### 3.4 WIE werden Entscheidungen dokumentiert?
- Entscheidungspunkte erkennen
- formale Protokollierung (z. B. `decision-log.md`)
- Verbindung zu Issues/Commits herstellen
- versionierte, nachvollziehbare Änderungen

### 3.5 WIE erkennt man, wann ein Chat beendet werden muss?
- Kriterien für Chat-Ende (z. B. Ziel erreicht, Drift, Themenwechsel)
- Übergabeobjekte (z. B. strukturierte Zusammenfassung)
- Startregeln für neue Chats

### 3.6 WIE iteriert man systematisch?
- inkrementelle Entwicklung
- kleinschrittige Konkretisierung
- Einordnung neuer Erkenntnisse in bestehende Strukturen
- Update-Prozess für Dokumente und Artefakte
- kontrollierte Anpassung der Projektanweisung (selten)

## 4. Bausteine für die spätere Methodik

Aus den Anforderungen lassen sich übergreifende methodische Bausteine ableiten. Diese bilden die spätere Struktur der gesamten Methodologie.

### 4.1 Steuerlogik (Projektanweisung)
- stabile, kurze Definition der Rollen
- Formatvorgaben
- Arbeitsprinzipien
- Konsistenzregeln

### 4.2 Externe Wissensbasis (GitHub)
- persistente Versionierung
- Dokumentation in Markdown
- Strukturierung nach Themen (z. B. `docs/`)
- Verbindung über Commits & Issues

### 4.3 Arbeitsprozesse
- definierte Makroprozesse (z. B. Phasenmodell)
- definierte Mikroprozesse (z. B. Schritte im Chat)
- klarer Umgang mit Iteration und Verbesserungszyklen

### 4.4 Chat-Design
- Strukturierung der Chats
- Rollendefinitionen
- Aufteilung in Teilkontexte
- Übergabetemplates

### 4.5 Begriffs- und Strukturmanagement
- Glossare
- Modell- und Begriffsdefinitionen
- Regeln für die Weiterentwicklung von Begriffen

### 4.6 Decision & Drift Management
- Entscheidunglogbücher
- Konsistenzprüfungen
- Mechanismen, um Drift früh zu erkennen

## 5. Zusammenspiel der Bausteine (Gesamtsystem)

Die Methodologie soll ein integriertes Gesamtsystem bilden, in dem:

1. **Projektanweisung** die Steuerlogik liefert.  
2. **Chats** operative Arbeit leisten (iterativ, fokussiert).  
3. **GitHub-Dokumentation** das persistent gesicherte Wissen bildet.  
4. **Issues, Commits und Dokumentation** die Nachvollziehbarkeit garantieren.  
5. **Arbeitsprozesse** sicherstellen, dass alles geordnet abläuft.  
6. **Regeln gegen Drift** Konsistenz wahren.  
7. **Rollenklarheit** die Arbeit mit LLMs stabilisiert.  

Das Gesamtsystem stellt sicher, dass Ergebnisse über Wochen, Monate oder Jahre hinweg **zielgerichtet**, **wiederholbar** und **nachvollziehbar** bleiben.

## 6. Ausblick auf Phase 1 – weitere Aufgaben

Aus diesem Dokument ergeben sich unmittelbar folgende Folge-Themen:

### ✓ Bausteine der Methodik präzisieren  
Was genau gehört in jeden Baustein? Wie definiert man deren Schnittstellen?

### ✓ Dokumenttypen & Speicherorte definieren  
Was gehört ins `docs/`-Verzeichnis, was ins Wiki, was in Issues?

### ✓ Ablaufmodell (Makroprozess) entwerfen  
Wie läuft ein Projekt mit LLM ab (Phasen, Übergaben, Routinen)?

### ✓ Mikroprozess für einzelne Chats definieren  
Wie strukturiert man einen Chat? Welche Schritte sind zwingend?

### ✓ Regeln zur Driftvermeidung ausarbeiten  
Wie stabilisiert man Begriffe und Entscheidungen?

### ✓ Rollenmodell für das LLM  
Welche Rollen gibt es? Wann werden sie aktiviert?

Diese Folgearbeiten bilden die nächsten Issues in Phase 1.

---

*Ende des Dokuments.*
