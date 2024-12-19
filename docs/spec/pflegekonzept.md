# Pflegekonzept
**zuletzt geändert am 19.12.2024**

# 1 Einführung

Dieses Dokument beschreibt Kontext und Prozesse zur kontinuierlichen Pflege des Datenmodells HealthDCAT-AP.de. Es handelt sich um die deutsche Version des Datenmodells für den Europäischen Gesundheitsdatenraum (EHDS). Dieses Modell wird im Rahmen der Post-COVID-Challenge des Dateninstituts entwickelt.

Das Dokument befindet sich gegenwärtig im Aufbau.

Erste Informationen zum Pflegekonzept können dem einschlägigen Kapitel aus dem [Bericht für Stufe 2](https://healthdcat-ap-de.github.io/healthdcat-ap.de/report_stage_2/4_Fortschreiben_der_Konzepte/4.2_Pflegekonzept.html) entnommen werden.

> Wie im [Bericht zum Abschluss der ersten Stufe](https://healthdcat-ap-de.github.io/healthdcat-ap.de/report_stage_1/2_Ausrichtung_des_Datenmodells_an_den_Anforderungen_der_Forschung/2.6_Konzept_HealthDCAT-AP.de/2.6.4_Nachnutzung_von_DCAT-AP.de_Artefakten.html) geschrieben, nutzt HealthDCAT-AP.de Artefakte von DCAT-AP.de nach. Entsprechend orientiert sich das Pflegekonzept für HealthDCAT-AP.de am [Pflegehandbuch von DCAT-AP.de](https://www.it-planungsrat.de/fileadmin/beschluesse/2018/Beschluss2018-30_TOP12_Anlage1_DCAD_AP.pdf).


# 2 Das Anwendungsprofil HealthDCAT-AP.de


## 2.1 Überblick über das Anwendungsprofil

Das Anwendungsprofil inkludiert in der jeweiligen Version folgende Dokumente und Artefakte:

1. HealthDCAT-AP.de Spezifikation
2. HealthDCAT-AP.de Konventionenhandbuch
3. UML-Modell

Im weiteren Sinne gehören ebenfalls folgende Dokumente und Artefakte zum Anwendungsprofil:

- URI-Konzept
- Pflegehandbuch


## 2.2 Abhängigkeiten von anderen Standards

HealthDCAT-AP.de nutzt eine Reihe von Basismodellen und Vokabularen nach. Entsprechende Abhängigkeiten sind bei der Pflege des Anwendungsprofils zu beachten.
- DCMI Metadata (dct)
- Asset Description Metadata Schema (adms)
- W3C Data Catalog Vocabulary (dcat)
- ISA Data Catalog Vocabulary Application Profile (DCAT-AP)
- GeoDCAT
- HealthDCAT-AP
- DCAT-AP.de
- Data Privacy Vocabulary (dpv)
- Data Quality Vocabulary (dqv)
- ISA Core Location Vocabulary (locn)
- Friend of a Friend (foaf)
- SPDX
- Schema.org
- Croissant (cr)
- VCARD
- Open Digital Rights Language (odrl)
- Web Ontology Language
- Simple Knowledge Organization System (skos)
- XML Schema Definition


# 3 Umfeld

## 3.1 Nutzer des Standards

## 3.2 Gremien mit Auswirkung die Ausgestaltung des Standards

# 4 Prozesse und Aufgaben im Rahmen der Pflege von HealthDCAT-AP.de

## 4.1 Grundbetrieb

Im Grundbetrieb des Anwendungsprofils ist sichergestellt, dass erstens die aktuelle Version des Datenmodells öffentlich zugänglich ist. Zweitens haben Nutzer über eine Kommunikationsplattform zudem die Möglichkeit, die Weiterentwicklung des Anwendungsprofils mitzugestalten und erhalten sowie drittens Beratungsunterstützung.

Wie es bei existierenden Standards gängige Praxis ist, werden die erste und zweite Funktionen des Grundbetriebs durch die Pflege einer GitHub-Seite durch die Pflegestelle von HealthDCAT-AP.de sichergestellt. Über diese Seite sind die in Punkt 2.1 genannten Dokumente und Artefakte in der aktuellsten Version verfügbar. Zudem haben allen Interessierten über die GitHub-Seite die Möglichkeit, Prüf- oder Änderungsaufforderungen in Form von Issues einzureichen. 

Die dritte Funktion des Grundbetriebs ist im aktuellen Entwicklungsstadium von HealthDCAT-AP.de noch nicht vollständig ausgeprägt. Derzeit steht es allen Interessierten offen, das Team von HealthDCAT-AP.de über das [Funktionspostfach](mailto:pf-healthdcat-ap@init.de) zu kontaktieren.

## 4.2 Änderungsmanagement

Um das Anwendungsprofil fortlaufend mit den Anforderungen der Post-COVID-Forschung und der Gesundheitsakteure in Einklang zu bringen, ist ein permanentes Änderungsmanagement erforderlich. Grundsätzlich gibt es drei Konstellationen, aus denen sich Änderungsaufforderungen an das Anwendungsprofil ergeben, namentlich:[^1]
-  Die Weiterentwicklung eines der Basismodelle, insbesondere HealthDCAT-AP
-  Änderungsbedarfe nach Praxistests sowie durch Community-Feedback
-  Sich wandelnde gesetzliche Rahmenbedingungen

Hieraus entstehende Änderungsaufforderungen werden zur offenen Diskussion als Issue im GitHub des Anwendungsprofils veröffentlicht. Falls Interessenten ihre Anliegen nicht direkt als Issue einreichen, kann dies durch die Pflegestelle des Standards erfolgen. Das Änderungsmanagement sieht nun vor, dass Änderungsaufforderungen zyklisch durch ein Change Advisory Board bewertet und priorisiert werden. Vom Gremium akzeptierte Änderungen werden anschließend im Änderungsplan vorgesehen, bevor sie umgesetzt und qualitätsgesichert werden.

In Anlehnung an DCAT-AP.de können Änderungsanträge von HealthDCAT-AP.de folgende Status durchlaufen:[^2]
- erfasst – Antrag wurde vom Antragssteller ausgefüllt
- bewertet - Antrag wurde von der Pflegestelle formal geprüft und bewertet
- geplant – Antrag ist zur Umsetzung eingeplant
- genehmigt – Umsetzung ist genehmigt für eine konkrete Version
- in Umsetzung – Antrag wird gerade umgesetzt
- geprüft – Umsetzung wurde von der Pflegestelle gegengeprüf

## 4.3 Releasemanagement

# 5 HealthDCAT-AP.de Pflegestelle

[^1]: vgl. [Abschlussbericht der zweiten Stufe](https://healthdcat-ap-de.github.io/healthdcat-ap.de/report_stage_2/5_Weiterentwicklung_des_Datenmodells/5.3_Inhaltliche_Vorstellung_zentraler_Aenderungen.html)

[^2]: vgl. [Pflegehandbuch DCAT-AP.de, S. 24](https://www.it-planungsrat.de/fileadmin/beschluesse/2018/Beschluss2018-30_TOP12_Anlage1_DCAD_AP.pdf)