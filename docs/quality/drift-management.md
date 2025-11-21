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

## 5. Regeln zur Drift-Vermeidung

Drift zu vermeiden ist wesentlich effektiver als sie im Nachhinein zu korrigieren. Die folgenden Regeln bilden das präventive Fundament des Drift-Managements und greifen an den Stellen an, an denen Drift typischerweise entsteht: bei der Struktur, der Terminologie, den Prompts, den Rollen und der Dokumentation. Durch konsequente Anwendung dieser Regeln bleibt das Projekt über viele Iterationen hinweg stabil und konsistent, unabhängig davon, wie lange oder komplex die Zusammenarbeit mit dem LLM wird.

### 5.1 Strukturregeln

Die Struktur eines Projekts ist einer der wichtigsten Ankerpunkte gegen Drift. Wenn die definierte Prozess- oder Dokumentstruktur nicht konsequent eingehalten wird, beginnt das Modell sehr schnell, alternative Strukturen zu entwickeln, da es aus Trainingsdaten gelernt hat, Texte kreativ und hilfreich umzugestalten.

#### Was bedeutet das konkret?

* Strukturen dürfen niemals "nebenbei" verändert werden.
* Änderungen an Dokumenten, Kapiteln oder Tabellen müssen **bewusst**, **explizit** und **dokumentiert** erfolgen.
* Das Modell muss wissen, welche Struktur *fix* ist und welche Stellen veränderbar sind.

#### Beispiel

Im Makroprozess sind die sechs Kernphasen eindeutig definiert. Wenn das LLM während einer tiefen Erarbeitung beginnt vorzuschlagen:

> „Vielleicht sollten wir zwischen Phase 3 und 4 eine zusätzliche Phase für Feinspezifikation einfügen?“

Dann ist dies **nicht** als „kreativer Vorschlag“ zu sehen, sondern als beginnende **Strukturdrift**, denn Strukturänderungen gehören nicht in eine operative Phase, sondern in ein eigenes Issue und Review.

### 5.2 Terminologieregeln

Terminologie ist das Rückgrat der Konsistenz, und driftfreie Begriffe sind entscheidend für ein gemeinsames Verständnis zwischen Mensch und Modell. LLMs tendieren dazu, Synonyme zu nutzen, Varianten einzuführen oder Begriffe semantisch zu erweitern — selbst wenn die ursprünglichen Begriffe präzise definiert wurden.

#### Regelprinzipien

* Kernbegriffe werden ausschließlich in der definierten Form verwendet.
* Keine Synonyme für definierte Begriffe.
* Neues Vokabular wird nur dann eingeführt, wenn:

  1. es inhaltlich notwendig ist,
  2. im Chat explizit begründet wird,
  3. und anschließend im Glossar persistiert wird.

#### Beispiel

Begriff laut Glossar:
**„Rollenmodell des LLM“**.

Wenn das Modell später schreibt: „… in unserem *Akteursmodell* unterscheidet das LLM zwischen Reviewer und Methodiker…“, dann entsteht Begriffsdrift, weil „Akteur“ inhaltlich etwas anderes meint. Dieses Problem hätte der **Mini-Glossar-Check** sofort erkannt.

### 5.3 Prompting-Regeln

Die Art und Weise, wie Prompts formuliert werden, hat direkten Einfluss darauf, wie stabil oder drift-anfällig ein Projekt wird. Drift entsteht oft durch unklare oder vage Prompts, die das LLM zu freier Interpretation verleiten.

#### Zentraler Grundsatz

**Jede Arbeitseinheit beginnt mit einer strukturierten Reinitialisierung.**

Das umfasst:

* den Kontext (Was machen wir?)
* die aktuelle Aufgabe (Was ist der nächste Schritt?)
* die Rolle (Wie soll das LLM handeln?)
* die relevanten Dokumente (Worauf stützen wir uns?)

Wechselst du hingegen ohne Vorwarnung zu einem neuen Thema oder lässt wesentliche Kontextanteile weg, interpretiert das Modell mehr als es sollte — Drift entsteht automatisch.

#### Beispiel

Unpräziser Prompt:

> „Kannst du das Kapitel besser formulieren?“

Dies lässt offen:

* welche Rolle aktiv ist,
* welche Struktur beibehalten werden soll,
* ob die Terminologie konsistent bleiben muss,
* ob es um sprachliche Optimierung vs. strukturelle Anpassung geht.

Mit Prompting-Regeln wird daraus:

> „Arbeite als *Reviewer*.
> Überarbeite **ausschließlich** die sprachliche Klarheit des folgenden Abschnitts,
> **ohne Struktur**, Begriffe oder Rollen zu verändern.“

Auf diese Weise besteht kein Drift-Risiko.

### 5.4 Rollen- und Verantwortlichkeitsregeln

Rollen sind ein starker Schutzmechanismus gegen Drift. Wenn Rollen präzise eingesetzt und sauber aktiviert werden, bleibt das Modell im definierten Modus und versucht nicht, Aufgaben anderer Rollen zu übernehmen oder neue Rollen auszudenken.

#### Regeln

* Rollenwechsel müssen immer explizit erfolgen.
* Rollen dürfen nicht implizit vermischt werden.
* Jede Rolle hat eine klar begrenzte Befugnis.
* Keine „automatischen“ Rollenentscheidungen durch das Modell.

#### Beispiel

Du arbeitest gerade mit dem LLM als „Methodiker“ an einem Prozessabschnitt. Dann sagst du:

> „Kannst du das anschließend kurz prüfen?“

Das Modell weiß in diesem fall nicht, ob du nun die Rolle des „Reviewers“ aktivieren willst. Es könnte selbstständig den Rollenwechsel vornehmen und beginnen, Inhalte zu bewerten, statt sie zu verbessern.

Die korrekte Variante lautet:

> „Aktiviere Rolle *Reviewer*. Prüfe ausschließlich Konsistenz, ohne den Inhalt umzuschreiben.“

### 5.5 Dokumentations- und Persistenzregeln

Viele Formen von Drift entstehen nicht im Chat, sondern dazwischen — wenn neue Inhalte nicht zeitnah persistiert werden. Je länger Chat-Entwürfe „ungesichert“ bleiben, desto höher das Risiko, dass sie in späteren Phasen wieder verloren gehen oder mit alten Versionen kollidieren.

#### Regeln

* Jede relevante Änderung muss **zeitnah** in das Repository übertragen werden.
* Zwischenstände dürfen nicht über zu viele Chat-Iterationen hinweg allein im Chat verbleiben.
* Persistenz erfolgt *immer* vor Kontextwechseln.
* Entscheidungsgrundlagen müssen dokumentiert werden, nicht nur Ergebnisse.

#### Beispiel

Du überarbeitest im Chat eine große Tabelle zu Drift-Arten. Die neue Fassung bleibt zunächst nur im Chat. Zwei Tage später startest du eine neue Chat-Einheit zum gleichen Thema und referenzierst dein Repository. Das Modell nimmt automatisch die **alte Version** als Grundlage, weil keine persistierte Aktualisierung existiert.

→ Jetzt hast du zwei Versionen im Projekt — idealer Nährboden für Drift.

Mit Persistenzregel:

> „Die aktualisierte Tabelle wurde soeben in `docs/quality/drift-management.md` persistiert.“

Es bleibt alles stabil.

### Kurzfazit zu den Regeln

Drift entsteht überall dort, wo Struktur, Sprache, Rollen oder Dokumentationsstand nicht eindeutig kontrolliert werden. Die Regeln zur Drift-Vermeidung sorgen dafür, dass das LLM **weniger interpretieren** und **mehr reproduzieren** muss — ein zentraler Erfolgsfaktor für langfristige Projekte.


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

