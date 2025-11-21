# Drift Management (Überarbeitete und erweiterte Fassung)

## 1. Zweck und Einordnung

Dieses Dokument beschreibt ein praktisches, alltagstaugliches Drift-Management für LLM-gestützte Projekte. „Drift“ bezeichnet jede ungewollte Veränderung von Begriffen, Strukturen, Rollen oder Kontexten, die dazu führt, dass das LLM schrittweise von der ursprünglichen Problemdefinition abweicht. Je länger ein Projekt läuft und je mehr Chats stattfinden, desto größer ist das Risiko, dass Inhalte verwässern oder sich in feinen, aber entscheidenden Details verändern.

Drift-Management verfolgt daher drei Kernziele:

1. **Früh erkennen**, wenn sich Abweichungen anbahnen.  
2. **Aktiv verhindern**, dass Abweichungen unkontrolliert wachsen.  
3. **Gezielt korrigieren**, um den Projektzustand stabil zu halten.

Es ergänzt die Persistenzmechanismen, sorgt für methodische Stabilität und ist integraler Bestandteil des Makroprozesses.

## 2. Arten von Drift

### 2.1 Begriffsdrift
Begriffe verlieren ihre definierte Bedeutung oder werden plötzlich in anderer Bedeutung verwendet.

**Beispiel:**  
„Methodologie-Baustein“ wird im Verlauf zu „Modul“, „Element“ oder „Arbeitskomponente“, obwohl im Glossar klar definiert ist, was ein Baustein ist und wie er sich abgrenzt.

### 2.2 Strukturdrift
Die Gliederung eines Dokuments oder eines Prozesses verändert sich unmerklich über Zeit.

**Beispiel:**  
Der Makroprozess umfasst sechs Kernphasen. Im Verlauf beginnt das LLM, Phase 3 in zwei Teilphasen zu zerlegen – ohne Beschluss.

### 2.3 Rollendrift
Rollen verlieren eindeutige Verantwortlichkeiten. Das LLM übernimmt Aufgaben anderer Rollen oder wechselt „inoffiziell“.

**Beispiel:**  
Der „Reviewer“ beginnt plötzlich, operative Inhalte zu erzeugen, obwohl seine Rolle auf die Qualitätsprüfung beschränkt ist.

### 2.4 Kontextdrift
Der thematische Rahmen verschiebt sich – oft unbewusst.

**Beispiel:**  
Das Projekt behandelt die Entwicklung einer LLM-Methodologie. Nach mehreren Chats antwortet das LLM plötzlich aus einer allgemeinen KI-Perspektive und vergisst, dass es sich um eine projektspezifische Methodik handelt.

### 2.5 Ergänzende Formen
- **Intent-Drift:** Die Zielsetzung verändert sich („Wir wollten eigentlich X, aber jetzt reden wir über Y“).
- **Wissensdrift:** Repository-Informationen werden zunehmend unpräzise wiedergegeben.
- **Dokumenten-Drift:** Inhalte verschiedener Dokumente werden vermischt oder überlagert.



## 3. Ursachen von Drift

Drift entsteht im Verlauf eines LLM-gestützten Projekts meist nicht durch einen einzelnen Fehler, sondern durch ein Zusammenspiel verschiedener Faktoren. Dazu gehören modellinterne Mechanismen, prozessuale Schwachstellen, unklare Nutzerinteraktionen, Kontextverlust und Lücken in der Dokumentation. Wenn diese Ursachen zusammenwirken, verändern sich Begriffe, Strukturen, Rollen und sogar die Zielsetzung eines Projekts oft schleichend, sodass Abweichungen erst spät sichtbar werden. Das folgende Kapitel erläutert diese Ursachen im Detail und illustriert sie mit realistischen Beispielen aus typischen LLM-Arbeitsprozessen.

### 3.1 Modellinterne Ursachen

Large Language Models arbeiten probabilistisch. Jede erzeugte Antwort ist das Ergebnis einer Wahrscheinlichkeitsverteilung möglicher Fortsetzungen, nicht eines stabil gespeicherten Wissenszustands. Dadurch entstehen natürliche Variationen: Ein Begriff kann in einer späteren Antwort anders formuliert werden, eine Struktur geringfügig verändert oder eine Rolle anders interpretiert werden. Diese kleinen Abweichungen fallen zu Beginn oft kaum auf, können sich aber mit jeder weiteren Interaktion verstärken. Besonders in langen Chats, in denen der frühere Kontext teilweise aus dem Fenster fällt oder nur noch abgeschwächt gewichtet wird, tendieren Modelle dazu, auf allgemeine Muster zurückzugreifen und ursprünglich präzise Definitionen behutsam zu verallgemeinern.

Ein typisches Beispiel ist die Veränderung von Prozessstrukturen. Wenn der Makroprozess eines Projekts sechs klar definierte Phasen umfasst, kann das Modell nach vielen Iterationen beginnen, zusätzliche „Zwischenschritte“ vorzuschlagen. Diese wirken aus Sicht des Modells plausibel, stehen aber im Widerspruch zur offiziellen Definition. Dadurch entsteht Strukturdrift, obwohl das Modell korrekt und „hilfreich“ antworten wollte.

### 3.2 Prozessbezogene Ursachen

Drift entsteht häufig dort, wo methodische Ankerpunkte fehlen. Ohne regelmäßige Drift-Checks, explizite Rollenaktivierung oder konsequente Bezugnahme auf die persistierte Dokumentation verliert das LLM nach und nach den strukturellen Rahmen, der zu Beginn eines Projekts klar definiert war. Besonders in intensiven Arbeitsphasen, in denen viele Iterationen nacheinander stattfinden, verändert sich die Gesprächsdynamik – und das Modell beginnt, auf interne Heuristiken zurückzugreifen, statt sich strikt an die externen Vorgaben zu halten.

Ein Beispiel dafür ist die allmähliche Veränderung von Begriffen innerhalb eines Kapitels. Wenn man etwa über 12 Nachrichten hinweg Varianten eines Abschnitts erarbeitet, aber keinen Abgleich mit dem Glossar oder der Definition der verwendeten Begriffe vornimmt, kann das Modell beginnen, alternative Formulierungen einzusetzen. Aus „Methodologie-Baustein“ wird dann vielleicht „Konzeptbaustein“. Diese kleine Variation ist für das Modell vollkommen logisch, widerspricht aber der festgelegten Begriffswelt und erzeugt schleichende Begriffsdrift. Der Mikroprozess sieht deshalb regelmäßige Drift-Checks vor, um genau diese Dynamik zu kontrollieren.

### 3.3 Nutzerinteraktionen als Ursache

Sehr häufig geht Drift vom Benutzer selbst aus, ohne dass dieser es beabsichtigt. Schon eine kleine Veränderung in der Formulierung eines Prompts kann dazu führen, dass das Modell einen neuen Bedeutungsrahmen übernimmt. Wenn ein Begriff plötzlich in einer anderen Form verwendet wird oder eine Frage anders gestellt wird als zuvor, interpretiert das Modell dies als gewollte Bedeutungsverschiebung – und passt seine zukünftigen Antworten entsprechend an. Auch das versehentliche Weglassen der Rollenaktivierung führt häufig dazu, dass das Modell den impliziten Rollenkontext rekonstruiert und dabei ungewollt in einen anderen Modus gerät.

Ein klassisches Beispiel findet sich in der Verwendung von Synonymen. Wenn man im Verlauf eines Projekts statt des definierten Begriffs „Rollenmodell“ plötzlich von einem „Akteursmodell“ spricht, entsteht für das Modell kein Widerspruch. Stattdessen verknüpft es beide Begriffe miteinander und behandelt sie in späteren Antworten als nahezu austauschbar. So entsteht Begriffsdrift, die sich nur schwer wieder vollständig rückgängig machen lässt, wenn sie einmal fest im Gespräch verankert ist.

### 3.4 Kontext- und Speicherprobleme

Ein weiteres wichtiges Driftphänomen ergibt sich aus dem Kontextfenster von LLMs. Je länger ein Chat wird, desto mehr früherer Kontext verliert an Relevanz oder fällt ganz heraus. Dadurch werden präzise Definitionen aus frühen Arbeitsphasen unter Umständen von späteren, vereinfachten Heuristiken überlagert. Das Modell orientiert sich dann eher an typischen Mustern seiner Trainingsdaten als an den spezifischen Projektvorgaben.

Dies zeigt sich zum Beispiel, wenn man nach sehr langen Arbeitssequenzen wieder zu einem früheren Dokument zurückkehrt. Obwohl zu Beginn genau definiert wurde, dass „Drift“ aus vier Kernarten besteht, können später Antworten entstehen, in denen plötzlich von „Fehlerarten“ gesprochen wird oder neue Driftarten ohne Absprache eingeführt werden. Diese Abweichungen sind nicht Ausdruck eines falschen Verständnisses, sondern das Ergebnis eines natürlichen Kontextverlusts über viele Iterationen hinweg.

### 3.5 Dokumentations- und Persistenzlücken

Drift entsteht nicht nur im Chat, sondern oft auch zwischen Chat und Repository. Wenn eine neue Version eines Dokuments im Chat entsteht, aber nicht zeitnah in das Repository übertragen wird, entstehen zwei parallele Wahrheiten: eine im Chat, eine im Repository. Sobald eine neue Arbeitseinheit gestartet wird und das Modell wieder mit der persistierten Version arbeitet, kommt es zu Divergenzen. Das LLM versucht dann, beide Stände zu „vereinigen“, was fast zwangsläufig zu Drift führt.

Ein typisches Beispiel ist die Überarbeitung einer Tabelle. Wird eine neue Version im Chat erarbeitet, aber nicht abgespeichert, und später wieder auf das Repository verwiesen, nutzt das Modell erneut die alte Version. Dies führt zu unerwarteten Vermischungen aus neuer und alter Logik – ein klassischer Auslöser für Wissensdrift und strukturelle Inkonsistenzen.

### 3.6 Rollenbezogene Ursachen

Rollen stellen einen methodischen Rahmen dar, der die Zusammenarbeit strukturiert. Wird dieser Rahmen jedoch nicht konsequent genutzt oder wird ein Rollenwechsel nicht explizit benannt, beginnt das Modell nach eigenem Ermessen zu entscheiden, welche Rolle gerade angemessen wäre. Dies führt schnell zu Rollendrift, die wiederum oft der Ausgangspunkt für weitere Driftformen ist, beispielsweise strukturelle Abweichungen oder unklare Zielverlagerungen.

Ein anschauliches Beispiel entsteht, wenn während der Überarbeitung eines Dokuments plötzlich der Prompt „Kannst du das für mich verbessern?“ gegeben wird, ohne die Rolle des Modells zu benennen. Das Modell kann diese Aufforderung als kreative, als redaktionelle oder als analytische Aufgabe interpretieren. Je nachdem, welche interne Heuristik greift, könnte das Modell plötzlich beginnen, Abschnitte umzustrukturieren oder Inhalte zu verdichten – obwohl eigentlich nur ein sprachliches Finetuning gewünscht war. Die Drift entsteht also nicht aus Unachtsamkeit des Modells, sondern aus einem nicht präzise definierten Rollenrahmen.

### 3.7 Zusammenfassung: Ursachen von Drift

Drift entsteht in LLM-gestützten Projekten nicht durch einen einzigen Fehler, sondern durch das Zusammenspiel mehrerer Faktoren. Das Modell selbst erzeugt durch seine probabilistische Arbeitsweise natürliche Variationen, die sich in langen Chats schrittweise verstärken können. Wenn der Arbeitsprozess zudem nicht konsequent strukturiert ist – etwa durch fehlende Drift-Checks oder unklare Rollenaktivierungen – verliert das LLM mit der Zeit den definierten Rahmen aus den Augen.

Auch der Mensch trägt häufig unbewusst zur Drift bei: Eine kleine Änderung in der Formulierung eines Prompts, die Nutzung von Synonymen oder ein unklarer Rollenwechsel kann das Modell dazu bringen, neue Begriffe oder Strukturen einzuführen, die so nie geplant waren. Mit zunehmender Chatlänge entsteht zudem Kontextverlust: Frühere Definitionen werden schwächer gewichtet oder fallen aus dem Kontextfenster, sodass das Modell auf seine generischen Muster zurückgreift.

Verstärkt wird Drift schließlich durch Dokumentations- und Persistenzlücken. Wenn neue Inhalte im Chat entstehen, aber nicht zeitnah ins Repository übertragen werden, entwickeln sich Chat-Stand und Repository-Version auseinander. Das Modell versucht später, beide Versionen zu verbinden, was zwangsläufig zu Inkonsistenzen führt. Unklare oder nicht aktivierte Rollen verschärfen dieses Problem weiter, weil das Modell seine Rolle heuristisch interpretiert und dadurch schnell zusätzliche Abweichungen entstehen.

Insgesamt ist Drift also ein natürlicher, aber kontrollierbarer Effekt, der aus der Dynamik zwischen Modellverhalten, Prozessen, Nutzeraktionen und Dokumentationsstand entsteht. Effektives Drift-Management beginnt daher mit dem Verständnis dieser Ursachen und sorgt dafür, dass sie durch klare Regeln, stabile Prozesse und regelmäßige Konsistenzprüfungen gar nicht erst wirksam werden.

## 4. Maßnahmenkatalog zur Drifterkennung

### 4.1 Frühindikatoren
Typische Frühzeichen, die ernst genommen werden sollten:

- Das LLM schlägt andere Begriffe vor, obwohl bereits definierte existieren.
- Rollen werden ohne Aktivierung gewechselt.
- Die Struktur weicht leicht ab (z. B. andere Überschriften).
- Antworten wirken weniger präzise oder stärker verallgemeinert.

### 4.2 Diagnosetechniken

**Glossar-Check:**  
Kurz prüfen, ob zentrale Begriffe noch exakt so verwendet werden wie definiert.

**Strukturabgleich:**  
Die aktuelle Antwort wird mit den korrespondierenden Repository-Dokumenten verglichen.

**Mini-Regressionstest:**  
Das LLM wird gebeten, die wichtigsten Regeln oder Begriffe kurz wiederzugeben.

### 4.3 Checkliste zur Drifterkennung
1. Stimmen die Begriffe mit dem Glossar überein?  
2. Entspricht die Struktur dem Makroprozess?  
3. Werden Rollen korrekt aktiviert und angewendet?  
4. Weicht die Antwort stilistisch oder inhaltlich von früheren Mustern ab?

### 4.4 Automatisierbare Methoden
- Kurzabfrage: „Welche zentralen Begriffe gelten hier?“  
- Kontextrekonstruktion: „Was ist der Zustand der Arbeitseinheit?“  
- Strukturvalidierung: „Bitte fasse die definierte Phasenstruktur zusammen.“

## 5. Regeln zur Driftvermeidung

### 5.1 Strukturregeln
- Prozessstrukturen dürfen nur nach expliziter Freigabe geändert werden.
- Dokumente müssen mit identischen Abschnittslogiken geführt werden.

### 5.2 Terminologieregeln
- Keine Synonyme für zentrale Begriffe.  
- Neue Begriffe nur nach expliziter Definition.

### 5.3 Prompting-Regeln
- Jede Arbeitseinheit beginnt mit einem eindeutigen Kontextabriss.  
- Rollen müssen explizit aktiviert werden.  
- Themenwechsel müssen angekündigt werden.

### 5.4 Dokumentationsregeln
- Ergebnisse zeitnah persistieren.  
- Änderungen müssen nachvollziehbar formuliert werden.  
- Redundante Inhalte vermeiden oder zentralisieren.

## 6. Routinen zur Konsistenzprüfung

### 6.1 Drift-Check beim Chat-Start

Ein effektiver Start-Check umfasst:

1. Ziel der Arbeitseinheit wiederholen  
2. Relevante Dokumente referenzieren  
3. Begriffe bestätigen  
4. Rollen aktivieren  
5. Offene Punkte prüfen  

**Beispiel:**  
„Wir starten mit der nächsten Iteration. Bitte bestätige die gültigen Begriffe für Drift und erläutere kurz den aktuellen Stand.“

### 6.2 Drift-Check während der Arbeit

Nach etwa 5–8 Nachrichten:

- Sind die Rollen noch korrekt?  
- Wurde der Zielrahmen eingehalten?  
- Stimmt die Struktur der Antwort?  

**Beispiel:**  
„Bitte bestätige, ob wir weiterhin entlang der definierten Drift-Arten arbeiten.“

### 6.3 Drift-Check vor Persistenz

Ein verpflichtender Schritt vor jeder Ablage:

- Terminologie gegen Glossar abgleichen  
- Struktur gegen Makroprozess prüfen  
- Offene Fragen markieren  

### 6.4 Integration in den Mikroprozess

Der Mikroprozess enthält zwei feste Driftpunkte:

- **Drift-Check vor der Iteration** – Stabilisierung vor dem Arbeiten  
- **Drift-Check nach dem Entwurf** – Prüfung vor Persistenz

## 7. Korrekturmechanismen bei Drift

### 7.1 Sofortmaßnahmen

- Drift explizit benennen  
- Klarstellung der betroffenen Stelle  
- Neuer Bezug zu Repository-Inhalten  

### 7.2 Wiederherstellung des Projektkontextes

- Projektanweisung neu laden  
- Glossar erneut referenzieren  
- Zielsetzung korrigieren  

**Beispiel:**  
„Wir haben eine leichte Strukturdrift. Bitte stelle die Phasennummerierung gemäß Makroprozess wieder her.“

### 7.3 Rekalibrierung

- Abgleich mit der zuletzt persistierten Version  
- Neuformulierung fehlerhafter Passagen  
- Klarere Strukturierung zur Stabilisierung

### 7.4 Reparatur-Workflow

1. Drift identifizieren  
2. Ursache benennen  
3. Alle betroffenen Stellen markieren  
4. Konsistente Neuformulierung  
5. Reviewer-Prüfung  
6. Persistenz und Commit  

## 8. Beispiel-Workflows

### 8.1 Drift-Check im operativen Ablauf

**Ablaufbeispiel:**

1. User startet neue Aufgabe  
2. LLM bestätigt Glossar + Struktur  
3. Kleine Abweichung wird bemerkt  
4. LLM korrigiert Terminologie  
5. Arbeit beginnt erst danach  

### 8.2 Drift-Korrektur im Mikroprozess

**Beispiel:**

Ein Dokument wird überarbeitet und das LLM schlägt plötzlich neue Rollen vor.  
Vorgehen:

- Rollendrift benennen  
- bestehende Rollen nachladen  
- Antwort neu erzeugen  
- Reviewer prüfen lassen  
- Persistieren  

### 8.3 Drift-Prüfung im Makroprozess

Phasenspezifische Driftpunkte:

- **Phase 1:** Begriffe stabilisieren  
- **Phase 2:** Strukturachsen fixieren  
- **Phase 3:** Iterative Driftkontrolle  
- **Phase 4:** Widerspruchsbereinigung  
- **Phase 5:** Drift-Schutz durch Persistenz  

## 9. Integration in Makro- und Mikroprozess

Drift-Management ist ein Querschnittsprinzip.  
Es sorgt dafür, dass die Methode stabil bleibt – unabhängig davon, wie lange ein Projekt dauert.

### Im Makroprozess
- schützt Phase 1 vor unklaren Definitionen,  
- stabilisiert Phase 3 gegen operative Drift,  
- sichert Phase 5 als endgültigen Drift-Schutz.

### Im Mikroprozess
- Driftchecks fixieren den Rahmen jeder Iteration,  
- Rollenwechsel werden kontrolliert,  
- Strukturabweichungen werden früh erkannt.

## 10. Visualisierungen

Die folgenden Diagramme stellen die zentralen Mechanismen des Drift-Managements visuell dar. Sie können direkt in PlantUML gerendert oder in GitHub mit einem geeigneten Plugin angezeigt werden.

### 10.1 Übersicht der Drift-Arten und ihrer Beziehungen

Dieses Diagramm zeigt, wie die verschiedenen Drift-Typen (Begriffs-, Struktur-, Rollen-, Kontextdrift) mit den drei zentralen Maßnahmenbereichen Erkennen, Vermeiden und Korrigieren zusammenhängen. Zudem wird dargestellt, an welchen Stellen Makroprozess, Mikroprozess und die stabilisierenden Repository-Dokumente die Drift-Kontrolle unterstützen.

![Drift Management](./data/drift-management.png)

## 10.2 Drift-Workflow (Schritt-für-Schritt)

Dieses Diagramm visualisiert den kompletten Ablauf bei der Behandlung von Drift: Vom ersten Hinweis über Diagnose und Klassifikation bis hin zu Korrektur, Validierung und Persistenz. Es dient insbesondere als operativer Leitfaden für Nutzer, Reviewer und Methodiker.

![Drift Workflow](./data/drift-workflow.png)

## 11. Weiterführende Dokumente
- persistence-mechanisms.md  
- process-macro.md  
- roles-llm.md  
- methodology-building-blocks.md  

