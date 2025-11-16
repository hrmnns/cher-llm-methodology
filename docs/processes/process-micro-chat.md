# Mikroprozess „Chat-basierte Zusammenarbeit mit LLM“

Dieser Mikroprozess beschreibt den Ablauf eines einzelnen Chats im Rahmen der Arbeit mit dem Repository `cher-llm-methodology`. Ziel ist es, Chats strukturiert, konsistent und reproduzierbar zu gestalten. Er definiert Phasen, Rollen, Ergebnisformate und Regeln für die Übergabe der Chat-Ergebnisse ins Repository. Der Mikroprozess wird in jedem fachlich relevanten Projekt-Chat angewendet.

## Executive Summary

<!-- Kurzfassung des Mikroprozesses in 5–10 Bullet Points -->

- [ ] Zweck des Mikroprozesses „Chat“
- [ ] Typischer Ablauf in Kurzform (Ablaufformel)
- [ ] Zentrale Phasen und ihre Ziele
- [ ] Wichtige Ergebnisarten und Artefakte
- [ ] Regeln für Übergabe ins Repository
- [ ] Checkliste für Chat-Abschluss
- [ ] Verweis auf Templates (Start-Block, Abschluss-Block)

---

## Inhaltsverzeichnis

<!-- automatisches oder manuelles TOC, je nach Renderumgebung -->

<!-- omit in toc -->
- [Mikroprozess „Chat-basierte Zusammenarbeit mit LLM\"](#mikroprozess-chat-basierte-zusammenarbeit-mit-llm)
- [Executive Summary](#executive-summary)
- [Inhaltsverzeichnis](#inhaltsverzeichnis)
- [Phase A – Chat-Start](#phase-a--chat-start)
- [Phase B – Strukturierter Arbeitszyklus](#phase-b--strukturierter-arbeitszyklus)
- [Phase C – Ergebnissicherung](#phase-c--ergebnissicherung)
- [Phase D – Übergabe ins Repository](#phase-d--übergabe-ins-repository)
- [Phase E – Chat-Abschluss](#phase-e--chat-abschluss)
- [Übergeordnete Zusammenhänge](#übergeordnete-zusammenhänge)
- [Zusammenfassung und Fazit](#zusammenfassung-und-fazit)

## Phase A – Chat-Start

### Ziel der Phase

Die Startphase stellt sicher, dass jeder projektbezogene Chat mit einem klar definierten Start-Prompt beginnt.
Sie schafft Orientierung über Ziel, Rollen, Modus und Kontext und bildet damit die Grundlage für eine qualitativ hochwertige und reproduzierbare Prompt-basierte Zusammenarbeit. Das zentrale Ergebnis dieser Phase ist ein vollständig ausgefüllter Start-Prompt-Block, der den Chat strukturiert eröffnet.

### Einstieg / Trigger

Diese Phase beginnt immer dann, wenn ein neuer fachlicher Chat im Rahmen der Methodik eröffnet wird. Sie ist unabhängig vom Thema, aber zwingend erforderlich für:

- neue Themen
- Themenwechsel oder Detailvertiefungen
- Fortsetzung nach Pausen
- Chats zur Bearbeitung oder Klärung eines Issues
- Chats zur Erstellung, Überarbeitung oder Analyse eines Dokuments

### Schritte in der Phase

1. **Kontextaufnahme**\
Zu Beginn wird in wenigen Sätzen klargestellt, warum dieser Chat gestartet wird, welcher vorherige Stand existiert und auf welche Dokumente oder Issues sich der Chat bezieht. Ziel ist eine gemeinsame, knappe Ausgangsbasis.

2. **Zieldefinition**\
Anschließend wird präzise beschrieben, was in diesem Chat erreicht werden soll. Das Ziel soll klar überprüfbar und in einer Sitzung erreichbar sein. Optional können auch Themen benannt werden, die bewusst ausgeklammert werden.

3. **Rollenklärung**\
Der Prompt-Autor legt fest, welche Rolle das LLM übernimmt (z. B. Reviewer, Methodiker oder Co-Autor) und welche Rolle er selbst innehat. Diese Rollen geben dem Chat eine erkennbare Struktur und bestimmen die Arbeitslogik.

4. **Modusfestlegung**\
Nun wird der Arbeitsmodus definiert: etwa Exploration, Strukturierung, Ausarbeitung, Planung, Review oder Produktion. Der Modus legt fest, wie das LLM antworten und wie der Chat insgesamt geführt werden soll.

5. **Benennen relevanter Artefakte und Bezüge**\
Es wird transparent gemacht, auf welche vorhandenen Materialien der Chat aufsetzt, zum Beispiel auf bestimmte Markdown-Dateien, Issues oder Ergebnisse vorangegangener Chats. So entsteht ein konsistenter Informationsstand.

6. **Formulierung des Start-Prompt-Blocks**\
Abschließend fasst der Prompt-Autor alle vorherigen Punkte in einem strukturierten Start-Prompt zusammen. Dieser Block ist der verbindliche Einstieg in die operative Arbeit und muss vor Beginn der nächsten Phase vollständig vorliegen.

### Was der Prompt-Autor in dieser Phase tun muss (Kernverantwortungen)

Die Verantwortung für einen klaren und produktiven Start liegt vollständig beim Menschen.
Er muss sich um folgende Punkte kümmern:

- den Anlass kurz, präzise und fokussiert formulieren
- ein konkretes Ziel definieren, das in einer Sitzung erreichbar ist
- die Rollen bewusst festlegen, damit das LLM zielgerichtet arbeiten kann
- den Arbeitsmodus auswählen (und explizit aussprechen)
- die relevanten Artefakte und Bezüge nennen
- einen sauberen, vollständigen Start-Prompt formulieren
- diesen Start-Prompt vor Beginn der Arbeit nochmal überprüfen („Prompt-Check“)

Worauf der Prompt-Autor besonders achten muss (Critical Points):

* **Ein Chat = ein Ziel.**\
Wenn mehrere Ziele gleichzeitig verfolgt werden, verliert der Chat Fokus und Effizienz. Ein eindeutiges Ziel verhindert Abschweifungen und erleichtert es, am Ende eindeutig festzustellen, ob der Chat erfolgreich war.

* **Der Start-Prompt ist das zentrale Steuerinstrument.**\
Er definiert die Rolle des LLM, den Rahmen der Zusammenarbeit und die Erwartungen an das Ergebnis. Ein unklarer Prompt führt zwangsläufig zu unklaren Antworten, Missverständnissen oder unnötigen Iterationen.

* **Der Prompt darf nicht zu breit oder mehrdeutig sein.**\
Breite oder schwammige Formulierungen machen es dem LLM schwer, zielgerichtet zu arbeiten. Je präziser und enger gefasst der Prompt ist, desto konsistenter und reproduzierbarer wird die Zusammenarbeit.

* **Der Kontext sollte auf maximal 5–7 Sätze begrenzt bleiben.**\
Zu viel Kontext verwässert das Ziel und belastet den Chat mit unnötigen Informationen. Das LLM arbeitet am besten, wenn es einen kompakten, klar priorisierten Kontext erhält, der den Kern des Themas erfasst.

* **Rollen und Arbeitsmodus müssen explizit genannt werden.**\
Das LLM kann nicht erraten, welche Rolle es spielen soll. Ohne klar definierte Rollen (z. B. Reviewer vs. Co-Autor) und einen festgelegten Modus (z. B. Strukturierung vs. Ausarbeitung) variiert das Antwortverhalten, was den Prozess inkonsistent macht.

* **Der Rahmen des Chats wird nur vom Menschen gesetzt.**\
Das LLM folgt. Wenn der Prompt-Autor die Kontrolle nicht bewusst übernimmt, verlagert sich die Steuerung unbewusst zum LLM — und das führt häufig zu thematischen Driftbewegungen oder zu tiefen Detailgängen, die nicht beabsichtigt waren.

* **Die Startphase ist erst abgeschlossen, wenn der vollständige Start-Prompt bestätigt ist.**\
Ein unfertiger oder nur halb formulierter Start führt fast immer zu Fehlinterpretationen. Die klare Bestätigung („Der Start-Prompt steht. Wir beginnen.“) markiert den Übergang in den strukturierten Arbeitsmodus.

### Ergebnisse und Artefakte

* Ein vollständig formulierter Start-Prompt, der den Chat eindeutig eröffnet und den Rahmen klar festlegt.
* Klar definierte Rollen, sodass die Zusammenarbeit zwischen Prompt-Autor und LLM von Beginn an eindeutig strukturiert ist.
* Ein festgelegter Arbeitsmodus, der bestimmt, wie das LLM agiert und welche Art von Antworten zu erwarten sind.
* Benannte und für beide Seiten transparente Artefakte bzw. Referenzen, auf denen der Chat aufbaut.
* Eine präzise Zieldefinition, die als Leitlinie für den weiteren Verlauf dient.
* Ein klarer Startpunkt für die nächste Phase, sodass der Übergang in den strukturierten Arbeitszyklus ohne Reibungsverluste erfolgen kann.

### Template: Start-Prompt-Block

```md
Anlass / Kontext:
…

Ziel dieses Chats:
…

Rollen:
– LLM: …
– Prompt-Autor: …

Arbeitsmodus:
…

Relevante Artefakte / Bezüge:
– …

Explizite Fokusgrenzen (optional):
– …
```

Beispiel eines vollständig formulierten Start-Prompt-Blocks:

```md
Anlass / Kontext:
Beginn der Ausarbeitung des Mikroprozesses „Chat“. Das Gerüst in der Datei „process-micro-chat.md“ ist bereits erstellt.

Ziel dieses Chats:
Phase A vollständig ausformulieren und in eine versionierbare, repository-fähige Form bringen.

Rollen:
– LLM: Methodiker, Reviewer und Co-Autor
– Prompt-Autor: Product Owner und Entscheider

Arbeitsmodus:
Strukturierung und Ausarbeitung

Relevante Artefakte / Bezüge:
– Dokumentgerüst „process-micro-chat.md“
– Issue #12
– Makroprozess-Dokument „process-macro.md“

Explizite Fokusgrenzen (optional):
Dieser Chat umfasst ausschließlich Phase A.
```




## Phase B – Strukturierter Arbeitszyklus

### Ziel der Phase
<!-- Ziel der iterativen Zusammenarbeit inhaltlich -->

### Einstieg / Trigger
<!-- Übergang vom Start in die operative Arbeit -->

### Schritte in der Phase
<!-- Fokus klären, Auftrag formulieren, Ergebnis reviewen, Iterationen, Ebenenwechsel -->

### Ergebnisse / Artefakte
<!-- Zwischenstände, benannte Versionen, markierte „finale“ Blöcke -->

### Beispiel
<!-- Kurzer Beispiel-Ausschnitt eines typischen Iterationszyklus -->

## Phase C – Ergebnissicherung

### Ziel der Phase
<!-- Sicherung der wesentlichen Ergebnisse im Chat selbst -->

### Einstieg / Trigger
<!-- z. B. wenn ein Zwischenergebnis stabil ist -->

### Schritte in der Phase
<!-- Zusammenfassen, benennen, kennzeichnen (z. B. „final“ / „ready for repo“) -->

### Ergebnisse / Artefakte
<!-- klar markierte Ergebnisblöcke, Zusammenfassungen -->

### Beispiel
<!-- Beispiel für einen als final gekennzeichneten Block -->

## Phase D – Übergabe ins Repository

### Ziel der Phase
<!-- Sicherstellen, dass relevante Ergebnisse ins Repo überführt werden -->

### Einstieg / Trigger
<!-- Wenn Inhalte stabil und als „repo-relevant“ identifiziert sind -->

### Schritte in der Phase
<!-- Wo kommt was hin? (docs/, Issues, ggf. Wiki), wie werden Verweise gesetzt -->

### Ergebnisse / Artefakte
<!-- aktualisierte Dateien, neue Issues, Verlinkungen -->

### Beispiel
<!-- Beispiel für eine Übernahme in eine .md-Datei und ein Issue -->

## Phase E – Chat-Abschluss

### Ziel der Phase
<!-- Klarer, bewusster Abschluss eines Chats -->

### Einstieg / Trigger
<!-- Wenn das Chat-Ziel (weitgehend) erreicht ist -->

### Schritte in der Phase
<!-- Abschluss-Checkliste durchgehen, Abschluss-Block erstellen, nächste Schritte definieren -->

### Ergebnisse / Artefakte
<!-- Ausgefüllter Abschluss-Block, benannte nächste Schritte -->

### Beispiel
<!-- Konkreter Abschluss-Block zu einem Chat -->

## Übergeordnete Zusammenhänge

### Rollenmodell im Mikroprozess „Chat“

<!-- Beschreibung der Rollen (z. B. LLM als Methodiker/Strukturgeber/Reviewer, Nutzer als Product Owner/Entscheider etc.) -->

### Visualisierung des Mikroprozesses

<!-- Verweis auf ein oder mehrere Diagramme (z. B. PlantUML Activity Diagram, Swimlane LLM/Mensch) -->

### Beziehung zum Makroprozess und weiteren Bausteinen

<!-- 
- Bezug zu `process-macro.md`
- Bezug zu `chatgpt-projects.md`, `mission-and-scope.md`
- Konsistenz der Begriffe (Phase, Iteration, Ebene, Artefakt)
-->

## Zusammenfassung und Fazit

<!--
- Was leistet der Mikroprozess „Chat“?
- Beitrag zu Qualität, Konsistenz, Reproduzierbarkeit
- Wann gilt der Prozess als erfolgreich angewendet?
- Weiterentwicklung der Methodik
-->

---

##Versionierung
Version: v1.0
Status: Erste vollständige und geprüfte Fassung 
Datum: 2025-11-16

## Weiterführende Dokumente
– (werden im Verlauf ergänzt)
