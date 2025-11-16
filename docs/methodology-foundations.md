# Foundations der Methodologie zur strukturierten Zusammenarbeit mit LLMs

## Version
- v0.1.0 – Erstfassung der Grundlagen
- v0.2.0 – Erweiterung um Persistenz als zentrale Voraussetzung

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
Ergebnisse lassen sich selten exakt reproduzieren. Variabilität ist erwünscht, aber bei komplexen Vorhaben hinderlich, wenn Präzision oder Nachvollziehbarkeit gefordert ist.

### 2.4 Fehlende Struktur in der Konversation  
Chats tendieren zu vermischten Ebenen, Brüchen in der Struktur, unklaren Arbeitsphasen und fehlenden Übergaben.

### 2.5 Wechsel zwischen Inhaltsebene und Metaebene  
Das Modell springt zwischen „Problemlösen“ und „die Methode erklären“. Ohne klare Trennung entsteht semantischer Drift.

### 2.6 Persistenzprobleme  
LLMs haben keine inhärente Persistenz. Erkenntnisse, Begriffe, Entscheidungen oder Strukturen aus früheren Chats werden nicht dauerhaft gespeichert.

### 2.7 Schwierigkeit, Zwischenergebnisse festzuhalten  
Chats sind kein Repository – sinnvolle Teilergebnisse verschwinden im Verlauf, wenn sie nicht gezielt extrahiert werden.

### 2.8 Multiple Rollen des LLMs  
LLMs können Methodiker, Architekt, Reviewer, Übersetzer, Systematiker, Autor etc. sein. Ohne Rollenklarheit entstehen Inkonsistenzen und ungewollte Rollenwechsel.

## 3. Persistenz als zentrale Voraussetzung

Persistenz ist eine fundamentale Voraussetzung für jede Methodologie zur Zusammenarbeit mit LLMs, da LLMs selbst *keine permanente Speicherung* besitzen. Alles, worüber Einigkeit erzielt wurde, muss unabhängig vom jeweiligen Chat **explizit gesichert und stabilisiert** werden.

Persistenz umfasst vier zentrale Kategorien:

### 3.1 Persistente Begriffe  
Definitionen, Terminologien, Modelle, Rollen, Konzepte – alles, was semantische Stabilität erfordert.

### 3.2 Persistente Strukturen  
Architekturen, Prozessmodelle, Arbeitsmodi, Datenstrukturen, Projektlogiken.

### 3.3 Persistente Ergebnisse  
Dokumente, Analysen, Zwischenstände, Entscheidungen, Artefakte.

### 3.4 Persistente Konventionen  
Formatvorgaben, Arbeitsregeln, Entscheidungsregeln, Strukturstandards.

Da das LLM keine dieser Elemente dauerhaft halten kann, benötigt die Methodik eine **externe Persistenzschicht**, bestehend aus:

- dem `docs/`-Verzeichnis (versionierte Dokumentation)
- dem Wiki (erweitertes Wissenssystem)
- Issues & Commits (formale Änderungshistorie)
- der Projektanweisung (interne, dauerhafte Steuerlogik)

Persistenz ist damit ein integraler Bestandteil des Gesamtsystems und muss in jedem Arbeitsschritt berücksichtigt werden. Ohne Persistenz entstehen Drift, Wiederholungsaufwand und Unzuverlässigkeit.

## 4. Anforderungen an eine belastbare Methodologie

Aus den Herausforderungen und der Persistenzanforderung ergeben sich klare methodische Anforderungen. Die Methodologie muss definieren, wie ein systematischer und kontrollierter Arbeitsprozess mit einem LLM entsteht.

### 4.1 WIE arbeitet man mit dem LLM?
- klare Rollen
- definierte Arbeitsmodi (Erarbeitung, Review, Meta, Strukturierung)
- Regeln für Ebenenwechsel
- stabile Gesprächsstruktur (Schritte, Phasen)

### 4.2 WIE werden Ergebnisse strukturiert?
- Abgrenzung Chat ↔ Repository
- definierte Dokumenttypen (README, Architektur, Entscheidungen, Glossare etc.)
- Regeln für Dokumentation im `docs/`-Verzeichnis und im Wiki
- sauberer Umgang mit Issues und Commits

### 4.3 WIE verhindert man semantischen Drift?
- stabile Begriffssysteme
- Projektanweisung als interne Steuerlogik
- regelmäßige Konsistenzchecks
- abgesicherte Versionierung im Repository
- klare Übergabeformate zwischen Chats

### 4.4 WIE werden Entscheidungen dokumentiert?
- Entscheidungspunkte erkennen
- formale Protokollierung (z. B. `decision-log.md`)
- Verbindung zu Issues und Commits herstellen
- versionierte, nachvollziehbare Änderungen

### 4.5 WIE erkennt man, wann ein Chat beendet werden muss?
- Kriterien für Chat-Ende (z. B. Ziel erreicht, Drift, Themenwechsel)
- Übergabeobjekte (z. B. strukturierte Zusammenfassung)
- Regeln für den Start neuer Chats

### 4.6 WIE iteriert man systematisch?
- inkrementelle Entwicklung
- kleinschrittige Konkretisierung
- Einordnung neuer Erkenntnisse in bestehende Strukturen
- Update-Prozess für Dokumente und Artefakte
- kontrollierte Anpassung der Projektanweisung (selten)

## 5. Bausteine für die spätere Methodik

Aus den Anforderungen lassen sich übergreifende methodische Bausteine ableiten. Diese bilden die spätere Struktur der gesamten Methodologie.

### 5.1 Steuerlogik (Projektanweisung)
- stabile, kurze Definition der Rollen
- Formatvorgaben
- Arbeitsprinzipien
- Konsistenzregeln

### 5.2 Externe Wissensbasis (GitHub)
- persistente Versionierung
- Dokumentation in Markdown
- Strukturierung nach Themen (`docs/`)
- Verbindung über Commits & Issues

### 5.3 Arbeitsprozesse
- definierte Makroprozesse (z. B. Phasenmodell)
- definierte Mikroprozesse (z. B. Schritte im Chat)
- klarer Umgang mit Iteration und Verbesserungszyklen

### 5.4 Chat-Design
- Strukturierung einzelner Chats
- Rollendefinitionen
- Aufteilung in Teilkontexte
- Übergabetemplates

### 5.5 Begriffs- und Strukturmanagement
- Glossare
- Modell- und Begriffsdefinitionen
- Regeln für die Weiterentwicklung von Begriffen

### 5.6 Decision & Drift Management
- Entscheidunglogbücher
- Konsistenzprüfungen
- Mechanismen zur frühen Drifterkennung

## 6. Zusammenspiel der Bausteine (Gesamtsystem)

Die Methodologie soll ein integriertes Gesamtsystem bilden, in dem:

1. **Projektanweisung** die dauerhafte Steuerlogik liefert  
2. **Chats** operative, iterative Arbeit leisten  
3. **GitHub** die externe Persistenzschicht bildet  
4. **Issues, Commits und Dokumentation** die Nachvollziehbarkeit garantieren  
5. **Arbeitsprozesse** den geregelten Ablauf sicherstellen  
6. **Persistenz** Drift minimiert und Struktur bewahrt  
7. **Rollenklarheit** die Arbeit mit dem LLM stabilisiert  

Das Gesamtsystem stellt sicher, dass Ergebnisse über Wochen, Monate oder Jahre hinweg **zielgerichtet**, **wiederholbar** und **nachvollziehbar** bleiben.

## 7. Ausblick auf Phase 1 – weitere Aufgaben

Aus diesem Dokument ergeben sich unmittelbar folgende Folge-Themen:

- Bausteine der Methodik präzisieren  
- Dokumenttypen & Speicherorte definieren  
- Ablaufmodell (Makroprozess) entwerfen  
- Mikroprozess für einzelne Chats definieren  
- Regeln zur Driftvermeidung ausarbeiten  
- Rollenmodell für das LLM entwickeln  

Diese Folgearbeiten bilden die nächsten Issues in Phase 1.

---

*Ende des Dokuments.*
