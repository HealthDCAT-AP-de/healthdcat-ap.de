# Pflegekonzept
Teil von Stufe 1 war die Erprobung eines Software-Stacks, der insbesondere die Weiterentwicklung und Zugänglichkeit des Modells in den nächsten Phasen sicherstellen soll. Grundsätzlich ist hierbei ein Open-Source-Ansatz zu bevorzugen. Es stellt eine Herausforderung dar, dass eine Full-Stack-Open-Source-Lösung nicht in der in Stufe 1 zur Verfügung stehenden Zeit einzurichten und nutzbar ist. Tools wie beispielsweise VocBench dienen primär der Pflege eines zugrundeliegenden Vokabulares. Der vollumfängliche mögliche Funktionsumfang wie etwa das Visualisieren von Instanzdaten und deren Validierung gegen das Modell werden somit in Stufe 2 erprobt und dokumentiert. Grundsätzlich sei jedoch an dieser Stelle erwähnt, dass der Ansatz des Vorhabens technologieneutral ist und somit ein Vendor Lock-In kein Risiko darstellt.
Das Pflegekonzept sieht vor diesem Hintergrund folgenden Ansatz vor:

Zum einen erfolgt die offene, technologieneutrale Veröffentlichung auf der Git-Repository-Plattform GitHub. Zum anderen wird das proprietäre Visualisierungs- und Abfragetool Stardog genutzt. Stardog hat sich auf das Wissensmanagement in geschlossenen Systemen fokussiert (beispielsweise für das unternehmensinterne Wissensmanagement), ermöglicht aber einen vergleichsweisen intuitiven und niedrigschwelligen Einstieg in die Visualisierung und Abfrage graphbasierter Datenbanken. Für eine ausführlichere Erläuterung der Funktionalitäten sei auf den Abschnitt 7 verwiesen.
Für die langfristige Pflege des Metadatenstandards ist es empfehlenswert, sich an bestehenden Konventionen und Praktiken zu orientieren. Als Ausgestaltung des europäischen Vorhabens HealthDCAT-AP, das sich wiederum in den Rahmen der vielfältigen europäischen DCAT-Applikationsprofile eingliedert, wird somit eine Veröffentlichung auf GitHub unter der Lizenz Creative Commons 4.0 int. Namensnennung „]init[ AG und WIG2 im Auftrag des BMI und BMWK“ (CC BY 4.0 int) erfolgen. Über GitHub erfolgt ebenfalls das Release- und Changemanagement, ggf. in Kombination mit Stakeholder-Workshops, die aufgezeichnet und im Nachgang veröffentlicht werden. Stakeholder können Änderungsanträge (Change Requests) am Standard als GitHub Issues stellen.

Zunehmend nutzt das BMI die Plattform OpenCode für Öffentlichkeitsbeteiligungen, beispielhaft für den Konsultationsprozess zu ausgewählten Architekturdokumenten zum National-Once-Only-Technical-System (NOOTS).[^57]

Aufgrund aktuell fehlenden Supports bei OpenCode, der kommunalen Verankerung des Betreibers (Anstalt öffentlichen Rechts in Stuttgart) und aufgrund des Bedarfs nach Sichtbarkeit im internationalen Raum wird für Stufe 1 und Stufe 2 GitHub statt OpenCode zur Veröffentlichung genutzt. Die Eignung von OpenCode wird in Stufe 2 erneut geprüft.

Der Betreiber wird die Änderungsanträge einem Expertengremium ausgewählter Stakeholder unterbreiten, in dem über die Umsetzung der Anträge beschlossen wird. Gegebenenfalls parallel hierzu wird ein Arbeitskreis nach dem Vorbild der DCAT-AP Working Groups etabliert, in dem die Betreiber mit Stakeholdern fachliche und technische Fragestellungen diskutieren und bearbeiten. Das Vorgehen dazu zum Aufsetzen des Beteiligungsverfahren ist in beschrieben.

Änderungsbedarfe werden in Anlehnung an DCAT-AP in drei Kategorien unterteilt, die jeweils unterschiedliche Release-Zyklen nach sich ziehen und unterschiedliche Auswirkungen auf die Implementierung des Metadatenstandards aufweisen:
* Fehlerbehebungen (bug fixes)   halbjährlicher Zyklus falls erforderlich, keine Auswirkung auf die Implementierung - der Arbeitskreis wird mindestens zwei Wochen vor der Neuveröffentlichung informiert, sodass Einwände erhoben werden können;
* geringfügige semantische Änderungen (minor semantic changes)   jährlicher Zyklus, keine zwingende Auswirkung auf die Implementierung - dem Arbeitskreis stehen sechs Wochen für eine Beurteilung zur Verfügung, und
* erhebliche semantische Änderungen (major semantic changes)   alle zwei Jahre, keine Abwärtskompatibilität möglich - diese Änderungen müssen innerhalb eines mindestens drei Monate währenden Zeitrahmens durch den Arbeitskreis diskutiert und mindestens einen Monat öffentlich zugänglich bewertet werden.

Mit jedem Release werden alle veröffentlichten Dateien erneut zur Verfügung gestellt. Dies sind im Wesentlichen:
* das Modell als UML-Datei, ggf. ergänzt durch SHACL-Constraints zur Validierung;
* Spezifikation bzw. Usage Notes als normative Tabellen;
* der Graph als RDF-Dokument und
* ab dem Folgerelease ein Change und Decision Log als Markdown-Datei.

Die Pflege betrifft zum einen das Modell, auf dem der Graph basiert, zum anderen den Wissensgraphen selbst. Bei der Pflege des Modells muss eine enge Abstimmung mit dem europäischen Vorhaben HealthDCAT-AP erfolgen, um etwaige Weiterentwicklungen verzögerungsfrei aufnehmen zu können. Dies ist für die Anschlussfähigkeit des Standards und damit die Interoperabilität erforderlich. Es wird sich daher an den Releasebedarf und die Change Requests des europäischen Vorhabens angekoppelt.
Der Wissensgraph selbst wird fortlaufend weiterentwickelt und bietet die Möglichkeit, die Metadaten konkreter Datensätze zu beschreiben und zu verknüpfen. In diesen Themenbereich fällt ab Stufe 2 ebenfalls die Entwicklung geeigneter SPARQL-Abfragen.

[^57]: NOOTS (opencode.de)
