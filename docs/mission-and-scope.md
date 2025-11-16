# Entwicklung einer Methode zur strukturierten Zusammenarbeit mit LLMs in komplexen Projekten

## 1. Hintergrund und Motivation

Komplexe Sachverhalte – zum Beispiel die schrittweise Entwicklung einer WebApp, die Konzeption eines Frameworks oder die Ausarbeitung von Compliance-Tools – werden zunehmend gemeinsam mit Large Language Models (LLMs) wie ChatGPT bearbeitet.

In der Praxis zeigt sich dabei ein wiederkehrendes Problem:

- Erkenntnisse aus früheren Chat-Phasen gehen verloren.
- Formulierungen und Konzepte „verwässern“ über die Zeit.
- Der Kontext verschiebt sich (Kontextdrift).
- Entscheidungen sind später nur schwer nachzuvollziehen.
- Die Zusammenarbeit wirkt zufällig statt geplant.

Dieses Vorhaben soll eine methodische Grundlage schaffen, um solche komplexen Arbeiten **gezielt, strukturiert und reproduzierbar** mit einem LLM durchführen zu können.

## 2. Problemstellung

Ohne klare Methode entstehen bei umfangreichen Chat-Verläufen typischerweise folgende Probleme:

- **Kontextverlust:** Wichtige Definitionen, Annahmen und Entscheidungen werden im Verlauf übersehen oder vom Modell nicht mehr berücksichtigt.
- **Inkonsistenzen:** Begriffe, Architekturen oder Rollen werden im Laufe des Projekts unterschiedlich verwendet.
- **Wissensdrift:** Das LLM reagiert anders als zu Beginn, weil die relevanten Vorgaben nicht stabil verankert sind.
- **Fehlende Dokumentation:** Gute Teilergebnisse bleiben im Chat „vergraben“ und sind schwer wiederzufinden oder weiterzuverwenden.
- **Nicht reproduzierbare Ergebnisse:** Es ist schwer oder unmöglich, einen früheren Stand wiederherzustellen oder ein Vorgehen nachzuvollziehen.

Gerade bei größeren Vorhaben – z. B. der Entwicklung einer Software – ist dieses Verhalten hinderlich und erzeugt unnötige Reibungsverluste.

## 3. Ziel des Vorhabens

Ziel des Projekts **„cher-llm-methodology“** ist es, eine **klare, wiederverwendbare Methodik** zu entwickeln, mit der:

- komplexe Themen über viele Chat-Sitzungen hinweg konsistent bearbeitet werden können,
- gewonnene Erkenntnisse und Ergebnisse **nicht verwässern**, sondern gezielt gesichert werden,
- das LLM sich an zentrale Vorgaben „erinnern“ kann (über Projektanweisungen und externe Doku),
- der Arbeitsprozess mit dem LLM **zielorientiert und stringent** bleibt,
- und die Zusammenarbeit Schritt für Schritt verbessert werden kann.

Die Methode soll sowohl allgemein nutzbar sein als auch an konkreten Beispielen demonstriert werden.

## 4. Anforderungen an die Zusammenarbeit mit dem LLM

Aus der bisherigen Erfahrung und den Überlegungen in diesem Projekt ergeben sich folgende Anforderungen:

1. **Einsatz von Projekten im LLM (z. B. ChatGPT-Projekte)**  
   - Es muss möglich sein, einen stabilen „Rahmen“ zu definieren (Projektanweisung), der über viele Chats hinweg gilt.
   - Diese Projektanweisung soll kurz, präzise und langfristig stabil sein.

2. **Trennung von Steuerlogik und ausführlicher Dokumentation**  
   - Die Projektanweisung enthält nur das Wichtigste (Rollen, Ziele, Arbeitsweise).
   - Ausführliche Inhalte (Methoden, Beispiele, Checklisten) werden in **Markdown-Dokumenten** im GitHub-Repository gepflegt.

3. **Externe, versionierbare Wissensbasis**  
   - Erkenntnisse und Zwischenergebnisse werden regelmäßig aus dem Chat heraus in Markdown-Dateien übernommen.
   - GitHub dient als zentrale, versionierte Wissensbasis (z. B. `docs/`-Verzeichnis, Wiki).

4. **Iteratives Vorgehen**  
   - Ziel ist nicht Perfektion im ersten Schritt, sondern eine schrittweise Verfeinerung.
   - Neue Erkenntnisse führen zu kontrollierten Anpassungen der Dokumentation und – seltener – der Projektanweisung.

5. **Transparente Nachvollziehbarkeit**  
   - Wichtige Entscheidungen, Definitionen und Modelle sollen in der Dokumentation nachvollziehbar sein.
   - Die Verbindung zwischen Chat-Ergebnissen und Repository-Inhalten soll erkennbar sein (z. B. über Issues, Commits, Referenzen).

## 5. Abgrenzung

Dieses Vorhaben konzentriert sich auf:

- die **Methode** der Zusammenarbeit mit LLMs,
- die **Organisation** von Chats, Projekten und Dokumentation,
- und die **Strukturierung** von Erkenntnissen und Ergebnissen.

Es geht **nicht** primär um:

- die technische Implementierung einzelner Projekte,
- die Bewertung bestimmter LLM-Modelle,
- oder die rechtliche/ethische Einordnung von KI an sich.

Diese Themen können später angebunden werden, stehen aber nicht im Zentrum dieses ersten Schrittes.

---

*Version: v0.1 – Erstfassung des Projektvorhabens*
