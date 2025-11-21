# Drift Management

## 1. Zweck und Einordnung

Ziel dieses Dokuments ist es, ein operationales Regelwerk zur Erkennung, Vermeidung und Korrektur von **semantischer Drift** in LLM-gestützten Projekten bereitzustellen.  
Drift bezeichnet jede Form der unbeabsichtigten Abweichung von zuvor definierten Begriffen, Strukturen, Rollen oder Kontexten.

Das Drift-Management ergänzt:
- die Persistenzmechanismen (dauerhafte Wissensspeicherung),
- die Qualitätssicherung,
- den Makro- und Mikroprozess der LLM-Zusammenarbeit.

Es stellt sicher, dass die Ergebnisse über längere Chat-Sequenzen hinweg **stabil**, **konsistent** und **reproduzierbar** bleiben.

## 2. Arten von Drift

### **2.1 Begriffsdrift**
Eine zuvor klar definierte Terminologie wird schrittweise verändert, verwässert oder inkonsistent verwendet.  
**Beispiel:** „Projektanweisung“ wird später als „Steuerprompt“ bezeichnet, obwohl die Begriffe unterschiedliche Bedeutung haben.

### **2.2 Strukturdrift**
Elemente verändern ihre Position, Reihenfolge oder logische Beziehung zueinander.  
**Beispiel:** Im Makroprozess entspricht Phase 4 nicht mehr der Konsolidierungsphase, sondern wird zur Persistenzphase umgedeutet.

### **2.3 Rollendrift**
Die Rollen des LLM oder von Personen im Projekt verlieren ihre Klarheit oder werden unbewusst überschrieben.  
**Beispiel:** „Reviewer“ liefert plötzlich operative Inhalte statt Qualitätsprüfung.

### **2.4 Kontextdrift**
Der inhaltliche Rahmen des Projekts verschiebt sich, weil Inhalte aus alten Chats unbeabsichtigt einfließen oder Auslassungen entstehen.

### **2.5 Ergänzende Formen**
- **Intent-Drift:** Die Zielsetzung der Aufgabe wird ungewollt verändert.  
- **Wissensdrift:** Inhalte aus dem Repository werden nicht mehr korrekt angewendet.

## 3. Ursachen von Drift

### **3.1 Modellinterne Faktoren**
- Wahrscheinlichkeitsbasierte Generierung
- Tendenz zur Generalisierung
- Überschreiben von Kontext bei langen Interaktionen

### **3.2 Externe Faktoren**
- Unpräzise oder sich wandelnde Benutzerprompts
- Wechsel zwischen Themen ohne explizite Kontextrekonstruktion

### **3.3 Prozess- und Dokumentationsfaktoren**
- Fehlende Persistenz
- Unklare Dokumentation
- Rollenwechsel ohne explizite Aktivierung

### **3.4 Interaktionsbezogene Faktoren**
- Fehlende Konsistenzprüfungen während der Arbeit
- Zu wenig Bezug auf stabilisierte Repository-Inhalte

## 4. Maßnahmenkatalog zur Drifterkennung

### **4.1 Frühindikatoren**
- Begriffe tauchen in neuer Bedeutung auf.
- Rollenbeschreibung wird nicht mehr eingehalten.
- Antworten widersprechen früheren Strukturen.
- Inhalte verlieren Präzision oder Detailtiefe.

### **4.2 Diagnose-Methoden**
- Vergleich der aktuellen Antwort mit Repository-Dokumenten
- Gegenprüfung zentraler Definitionen
- Cross-Check mit Glossar, Rollenbeschreibung, Makroprozess

### **4.3 Checklisten für schnelle Identifikation**
- Wird Terminologie konsistent verwendet?
- Stimmen Strukturen mit `process-macro.md` überein?
- Entspricht die Rollenaktivierung der Projektanweisung?
- Gibt es Brüche im Zielbild?

### **4.4 Automatisierbare Prüfungen**
- „Drift-Check am Chat-Start“
- „Quick Alignment Check“ bei Themenwechseln
- „Repository-Referenzierung“ bei allen kritischen Abschnitten

## 5. Regeln zur Driftvermeidung

### **5.1 Strukturregeln**
- Alle methodischen Inhalte müssen sich auf Makro- und Mikroprozess beziehen.
- Strukturänderungen nur nach expliziter Freigabe im Chat.

### **5.2 Begriffs- und Terminologieregeln**
- Glossar als verbindliche Quelle
- Neue Begriffe müssen explizit eingeführt werden
- Keine Synonyme für zentrale Begriffe (z. B. „Projektanweisung“)

### **5.3 Prompting-Regeln**
- Jede neue Arbeitseinheit beginnt mit einem Kontextabriss.
- LLM-Rollen müssen explizit aktiviert werden.
- Austausch von Themen nur nach „Kontext-Reset“.

### **5.4 Rollen- und Aufgabenklarheit**
- Jede LLM-Rolle arbeitet nur innerhalb ihres Mandats.
- Rollenwechsel sind zu markieren.

### **5.5 Dokumentationsregeln**
- Wichtige Ergebnisse müssen sofort ins Repository überführt werden.
- Entscheidungen sind nachvollziehbar zu dokumentieren.
- Persistenzmechanismen (siehe eigenes Dokument) gelten immer.

## 6. Routinen zur Konsistenzprüfung

### **6.1 Drift-Check beim Chat-Start**
Ein strukturierter Schnellcheck:
1. Ziel der aktuellen Arbeitseinheit wiederholen  
2. Projektanweisung referenzieren  
3. Relevante Dokumente laden  
4. Begriffe, Rollen, Strukturen bestätigen  
5. Abgleich mit letzter persistierter Version

### **6.2 Drift-Check während der Arbeit**
- Nach 5–8 Interaktionen kurzer Abgleich:
  - Terminologie konsistent?
  - Struktur unverändert?
  - Rollen eingehalten?

### **6.3 Drift-Check vor Persistenz (Makroprozess Phase 5)**
- Vollständigkeitsprüfung
- Konsistenz zu allen verwandten Dokumenten
- Explizite Rollenprüfung (Reviewer > Methodiker > Dokumentation)

### **6.4 Integration in den Mikroprozess**
- Drift-Check ist Bestandteil der Schleifenstruktur
- Kontrollpunkt vor „Deep Dive“
- Kontrollpunkt nach Variantenbildung

## 7. Korrekturmechanismen bei Drift

### **7.1 Sofortmaßnahmen**
- Drift benennen  
- Den betroffenen Abschnitt neu formulieren  
- Auf Repository-Inhalte referenzieren

### **7.2 Wiederherstellung des Projektkontextes**
- Re-Load der Projektanweisung
- Re-Load aller relevanten Dokumente
- Präzisierung der Zielsetzung

### **7.3 Rekalibrierung mit Repository-Inhalten**
- Korrekte Terminologie aus zentralen Dokumenten übernehmen
- Strukturen aus Makroprozess erneut verankern
- Rollen explizit reaktivieren

### **7.4 Reparatur-Workflow bei schwerwiegender Drift**
1. Drift benennen  
2. Ursache bestimmen  
3. Betroffene Stellen identifizieren  
4. Strukturelle Korrektur  
5. Persistenz aktualisieren  
6. Dokumentieren, was und warum korrigiert wurde  

### **7.5 Dokumentation der Korrekturen**
- Änderung im Dokument selbst
- Commit-Message mit Hinweis auf Drift-Korrektur
- Verweis auf betroffene Issues

## 8. Beispiel-Workflows

### **8.1 Drift-Check im operativen Chat-Ablauf**
1. User startet neuen Arbeitsblock → LLM bestätigt Problemrahmen  
2. LLM cross-checkt Terminologie aus Glossar  
3. Bei Abweichungen: Sofortkorrektur  
4. Ergebnis wird konsolidiert  

### **8.2 Drift-Korrektur im Mikroprozess**
- Bei Rollenabweichung  
- Bei Strukturveränderungen  
- Bei unklarer Zielrichtung  
→ Korrekturmechanismus aus Kapitel 7 anwenden

### **8.3 Drift-Prüfung im Makroprozess**
- Phase 1: Begriffe & Rollen prüfen  
- Phase 2: Strukturachsen gegen Drift sichern  
- Phase 3: iterativer Driftcheck  
- Phase 4: Widersprüche bereinigen  
- Phase 5: Persistenz gegen Drift stabilisieren  

### **8.4 Eskalationspfad bei persistenter Drift**
1. Drift nicht behebbar  
2. Kontext neu initialisieren  
3. Letztpersistierte Version verwenden  
4. Neu aufsetzen der Arbeitseinheit  

## 9. Integration in Makro- und Mikroprozess

### **Makroprozess**
- Phase 1: Baseline-Definition, zentrale Begriffe stabilisieren  
- Phase 2: Driftanfällige Begriffe identifizieren  
- Phase 3: operative Driftkontrolle  
- Phase 4: Widerspruchsprüfung  
- Phase 5: Persistenz als Drift-Schutz  
- Phase 8: Monitoring (Langzeitdrift)

### **Mikroprozess**
- Drift-Checks an zwei Stellen: Start & Pre-Persistenz  
- Rollenprüfung bei jedem Rollenwechsel  
- Strukturprüfung vor jedem Deep Dive  

## 10. Weiterführende Dokumente
- `persistence-mechanisms.md`  
- `process-macro.md`  
- `roles-llm.md`  
- `methodology-building-blocks.md`

