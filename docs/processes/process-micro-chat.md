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

In dieser Phase findet die eigentliche inhaltliche Arbeit statt.
Der strukturierte Arbeitszyklus sorgt dafür, dass der Chat nicht unkontrolliert verläuft, sondern in klar abgegrenzten Schritten, Iterationen und Ebenenwechseln geführt wird.
Ziel ist es, innerhalb des definierten Rahmens systematisch Ergebnisse zu erarbeiten, zu prüfen und schrittweise zu verfeinern.

### Einstieg / Trigger

Die Phase beginnt, sobald der Start-Prompt vollständig formuliert und bestätigt ist.
Das LLM hat Rollen und Modus verstanden, der Mensch hat Ziel und Fokus definiert – damit kann der operative Teil beginnen.

### Schritte in der Phase

1. **Fokus klären**
   Zu Beginn eines Arbeitszyklus präzisiert der Prompt-Autor, worauf sich der nächste Schritt konzentrieren soll. Das kann ein Abschnitt, Unterthema, eine Frage oder ein Teilziel sein.

2. **Auftrag formulieren**
   Der Prompt-Autor erzeugt einen klaren Prompt, der beschreibt, was das LLM tun soll: Ideen entwickeln, strukturieren, textuell ausarbeiten, bewerten, vergleichen etc. Der Auftrag ist kurz, präzise und entspricht dem aktuellen Modus.

3. **Ergebnis prüfen und rückkoppeln**
   Das LLM liefert ein Ergebnis, das der Prompt-Autor prüft: auf Qualität, Passung, Logik, Vollständigkeit und Konsistenz mit dem Ziel des Chats. Anschließend erfolgt Feedback oder Nachschärfung.

4. **Iterationen durchführen**
   Der Prompt-Autor entscheidet nach jeder Rückkopplung, ob:
   – ein weiterer Zyklus zur Verfeinerung nötig ist,
   – ein Ebenenwechsel sinnvoll ist,
   – das Ergebnis stabil genug ist, um den Abschnitt abzuschließen.

5. **Ebenenwechsel explizit machen**
   Wenn von Struktur- auf Inhaltebene, oder von Grob- zu Feindetail gewechselt wird, sagt der Prompt-Autor das ausdrücklich an. Dies verhindert Vermischungen und sorgt für Klarheit im Arbeitsstil.

6. **Zwischenergebnisse markieren**
   Sobald ein Ergebnis stabil erscheint, wird es benannt (z. B. „Zwischenergebnis A“), dokumentiert und als Grundlage für weitere Schritte verwendet.

### Was der Prompt-Autor in dieser Phase tun muss (Kernverantwortungen)

* Den Arbeitsfokus bewusst steuern, statt ihn dem LLM zu überlassen.
* Aufträge in Form kurzer, klarer Prompts formulieren („Bitte strukturiere…“, „Bitte überprüfe…“).
* Ergebnisse kritisch prüfen und gezielt nachschärfen.
* Disziplin bei Ebenenwechseln halten (nie Inhalte, Struktur und Formulierungen gleichzeitig bearbeiten).
* Relevante Zwischenergebnisse rechtzeitig sichern und benennen.
* Themen driftenden Tendenzen sofort korrigieren („Zurück zum Fokus…“).
* Den Arbeitsprozess aktiv moderieren – er ist nicht selbstlaufend.

### Worauf der Prompt-Autor besonders achten muss (Critical Points):

* **Zu breite Arbeitsaufträge vermeiden.**\
  Breite Prompts führen dazu, dass das LLM versucht, „alles auf einmal“ zu lösen. Beispiel:\
  *Ungünstig:* „Bitte schreibe Phase B komplett aus.“\
  *Gut:* „Bitte entwirf drei Varianten für die Unterstruktur von Phase B.“

* **Jeder Zyklus braucht einen klaren Fokus.**\
  Ohne klaren Schwerpunkt verzettelt sich der Chat. Beispiel:\
  *Gut:* „Fokus nur auf die Definition des Ziels der Phase.“\
  *Ungünstig:* „Mach Phase B besser.“

* **Ebenen nicht vermischen.**\
  Struktur, Inhalt und Formulierungen dürfen nicht gleichzeitig bearbeitet werden. Beispiel:\
  *Klar:* „Wir bleiben auf Strukturebene. Formulierungen später.“\
  *Unklar:* „Struktur okay — kannst du es direkt schön ausschreiben?“

* **Iterationen nicht überspringen.**\
  Der erste Entwurf ist oft unpräzise; ein zweiter oder dritter Durchlauf bringt Qualität.  Beispiel:\
  *Vorgehen:* Struktur → Feedback → Verfeinerung → Bestätigung.

* **Feedback muss konkret sein.**\
  LLMs können mit vagen Rückmeldungen wenig anfangen. Beispiel:\
  *Klar:* „Bitte Punkt 4 kürzer formulieren und Beispiel ergänzen.“\
  *Vage:* „Das passt noch nicht so.“

* **Der Prompt-Autor steuert den Arbeitsprozess.**\
  Das LLM schlägt vor — der Mensch trifft Entscheidungen und gestaltet den Ablauf.  Beispiel:\
  *Aktiv:* „Bitte zurück zum Fokus. Wir sind noch bei der Struktur, nicht der Formulierung.“\
  *Passiv:* Das LLM arbeiten lassen und hoffen, dass es „sich schon richtig einpendelt“.

* **Rechtzeitig Ergebnisse sichern.**\
  Wenn Zwischenergebnisse nicht klar markiert werden, verschwinden sie im Chatverlauf. Beispiel:\
  *Gut:* „Dieses Ergebnis nennen wir ‚Zwischenergebnis B.2 – stabil‘.“\
  *Risiko:* Unmarkierte Entwürfe werden später überlagert und sind nicht mehr eindeutig auffindbar.


### Ergebnisse und Artefakte

* Klar benannte Zwischenergebnisse, die den aktuellen Arbeitsstand transparent machen und als stabile Bezugspunkte dienen.
* Iterativ verfeinerte Inhalte oder Strukturen, die nachvollziehbar aus den einzelnen Arbeitszyklen hervorgegangen sind.
* Deutlich markierte Ebenenwechsel, sodass erkennbar bleibt, wann von Struktur- zu Inhaltsebene oder von Grob- zu Feindetail gewechselt wurde.
* Teilergebnisse, die ausreichend stabil und qualitätsgesichert sind, um später direkt in Repository-Dokumente übernommen zu werden.
* Entscheidungsnotizen oder Klärungen, die den Entstehungsprozess dokumentieren und spätere Nachvollziehbarkeit erleichtern.
* Eine logisch aufgebaute Folge von Arbeitsschritten, die zeigt, wie der Chat zum jeweiligen Ergebnis geführt hat und welche Argumente oder Varianten berücksichtigt wurden.

### Beispiel für einen typischen Arbeitszyklus

* Der Prompt-Autor legt den Fokus fest, zum Beispiel: „Bitte konzentriere dich ausschließlich auf die Unterstruktur von Phase B.“
* Anschließend formuliert er den Auftrag: „Erstelle drei präzise strukturierte Varianten, jeweils in klar getrennten Blöcken.“
* Das LLM liefert die Varianten; der Prompt-Autor prüft sie daraufhin, welche am besten zum Ziel des Chats passt.
* Er gibt gezieltes Feedback, etwa: „Variante 2 ist vielversprechend, aber bitte den Teil zu den Iterationen klarer herausarbeiten.“
* Eine weitere Iteration folgt, in der die Variante verbessert und präzisiert wird.
* Sobald das Ergebnis stabil und klar ist, markiert der Prompt-Autor es als Zwischenergebnis: „Diese Fassung nennen wir ‚Strukturvariante B.1 – stabil‘.“

## Phase C – Ergebnissicherung

### Ziel der Phase

Die Ergebnissicherung stellt sicher, dass wesentliche Resultate des Chats klar identifiziert, benannt und dokumentiert werden. Sie verhindert, dass gute Ergebnisse im Verlauf des Chats überlagert oder unauffindbar werden, und legt die Grundlage für eine saubere Übergabe ins Repository.

Das Ziel der Phase ist es, stabile, eindeutig benannte Ergebnisse zu erzeugen, die direkt weiterverwendet werden können.

### Einstieg / Trigger

Diese Phase beginnt immer dann, wenn:

* ein inhaltliches oder strukturelles Ergebnis stabil genug erscheint,
* ein Arbeitsabschnitt abgeschlossen wurde,
* ein Zwischenergebnis explizit als Grundlage für spätere Schritte dienen soll,
* oder der Prompt-Autor sicherstellen möchte, dass ein bestimmter Stand nicht verloren geht.

Die Ergebnissicherung ist keine einmalige Aktion, sondern läuft parallel und bedarfsgesteuert innerhalb der Phase B.

### Schritte in der Phase

1. **Stabile Ergebnisse identifizieren**\
   Der Prompt-Autor entscheidet, welche Inhalte oder Strukturen als „ausreichend stabil“ gelten, um sie zu sichern.

2. **Klare Benennung vergeben**\
   Ergebnisse erhalten einen eindeutigen Namen, zum Beispiel:\
   „Zwischenergebnis C.1 – Strukturentwurf“,\
   „Ergebnisblock – finaler Abschnitt der Phase B“.

3. **Ergebnis in einem sauber abgegrenzten Block festhalten**\
   Das LLM liefert das Ergebnis klar getrennt vom restlichen Text, ohne Meta-Diskussion.\
   Der Prompt-Autor prüft, ob der Block vollständig und sauber abgegrenzt ist.

4. **Version oder Status markieren**\
   Der Prompt-Autor kennzeichnet das Ergebnis, zum Beispiel:\
   „stabil“, „final“, „für Repo geeignet“, „Entwurf v0.2“.

5. **Kontext kurz ergänzen (falls nötig)**\
   Wenn es für die spätere Übergabe relevant ist, wird kurz erklärt, wie der Block entstanden ist oder wozu er dient.

6. **Bestätigung des Ergebnisses**\
   Der Prompt-Autor entscheidet explizit, dass der Block final oder stabil genug ist, um für Phase D bereit zu sein.

### Was der Prompt-Autor in dieser Phase tun muss (Kernverantwortungen)

* Stabilität des Ergebnisses einschätzen und bewusst entscheiden, ob es sichertauglich ist.
* Ergebnisse klar benennen, damit sie später auffindbar und referenzierbar sind.
* Verantwortlich prüfen, ob der Ergebnisblock logisch stimmig, vollständig und passend zum Chat-Ziel ist.
* Darauf achten, dass Ergebnisblöcke sauber getrennt von Diskussionen und Begleittexten stehen.
* Klarstellen, ob ein Ergebnis „stabil“ oder „final“ ist.
* Sicherstellen, dass alles, was später ins Repository gehört, in dieser Phase sauber markiert wird.

### Worauf der Prompt-Autor besonders achten muss (Critical Points)

* **Ergebnisse niemals ungekennzeichnet im Chat stehen lassen.**\
  Unmarkierte Ergebnisse verschwinden später im Verlauf und sind schwer reproduzierbar. Beispiel:\
  Ungünstig: „Das sieht gut aus.“\
  Gut: „Bitte markiere diesen Block als ‚Zwischenergebnis C.2 – stabil‘.“

* **Ergebnisblöcke müssen sauber abgegrenzt werden.**\
  Wenn Diskussion und Ergebnis vermischt sind, wird die spätere Übernahme erschwert. Beispiel:\
  Gut: Ein separater Block nur mit Inhalt, keine Meta-Kommentare.

* **Jedes Ergebnis braucht einen Namen.**\
  Benennungen verhindern Verwechslungen und erleichtern Bezüge in späteren Chats.\
  Beispiel: „Finaler Entwurf Phase B – Version 0.3“.

* **Stabil ≠ final.**\
  Ein stabiles Ergebnis kann Grundlage für Weiterarbeit sein, ist aber noch nicht repository-ready.

* **Nur geprüfte Ergebnisse sichern.**\
  Es ist Aufgabe des Prompt-Autors, Resultate vor der Sicherung zu prüfen. Niemals unkontrolliert übernehmen.

* **Dokumentation vermeiden, die zu ausführlich ist.**\
  Sicherung heißt Klarheit, nicht ausufernde Historie. Ergebnisblöcke kurz, präzise und eindeutig halten.

### Ergebnisse und Artefakte

* klar benannte und sauber abgegrenzte Ergebnisblöcke
* definierte Versionen oder Statusangaben (z. B. „stabil“, „final“)
* Zwischenergebnisse, die als Grundlage für spätere Bearbeitung dienen
* konsistente und nachvollziehbare Dokumentationspunkte innerhalb des Chats
* Ergebnisblöcke, die für Phase D (Übergabe ins Repository) vorbereitet sind
* eindeutige Referenzen, die eine spätere Wiederverwendung sicherstellen

### Beispiel für eine Ergebnissicherung

* Der Prompt-Autor erkennt, dass ein Strukturentwurf aus Phase B nun stabil ist.
* Er bittet das LLM: „Bitte stelle diesen Strukturentwurf als sauberen, separaten Ergebnisblock bereit.“
* Das LLM liefert den Block; der Prompt-Autor prüft und ergänzt einen Status wie „Zwischenergebnis C.3 – stabil“.
* Der Block wird bestätigt und später in Phase D für das Repository genutzt.

### Ergebnisse und Artefakte

* Eindeutig benannte Ergebnisblöcke, die den Stand eines Arbeitsabschnitts klar widerspiegeln und jederzeit wiedergefunden werden können.
* Knappe Statuskennzeichnungen wie „stabil“, „final“ oder „Entwurf v0.2“, die transparent machen, wie weit das Ergebnis gereift ist.
* Zwischenergebnisse, die als verlässliche Basis für spätere Schritte oder nächste Chats verwendet werden können.
* Klar abgegrenzte Inhalte, die vom Begleittext getrennt sind und sich dadurch leichter für das Repository übernehmen lassen.
* Dokumentierte Entscheidungen oder Klärungen, die zeigen, warum ein bestimmter Entwurf gewählt oder verworfen wurde.
* Eine nachvollziehbare Abfolge von Ergebnispunkten, die deutlich macht, wie der Chat Schritt für Schritt zum Endstand gelangt ist.

### Beispiel für eine Ergebnissicherung

* Der Prompt-Autor erkennt, dass ein Strukturentwurf aus der vorherigen Iteration nun ausreichend ausgereift ist, um ihn zu sichern.
* Er formuliert den Auftrag: „Bitte stelle den Strukturentwurf noch einmal als sauberen, getrennten Ergebnisblock bereit.“
* Das LLM liefert den Block; der Prompt-Autor prüft ihn und ergänzt eine klare Bezeichnung wie „Zwischenergebnis C.3 – stabil“.
* Anschließend bestätigt er, dass dieser Stand als Grundlage für die weitere Arbeit oder für die spätere Übergabe ins Repository dienen soll.




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
