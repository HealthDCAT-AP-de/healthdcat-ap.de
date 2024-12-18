[Zurück zum Inhaltsverzeichnis](https://healthdcat-ap-de.github.io/healthdcat-ap.de/report_stage_2.html)

# 5 Weiterentwicklung des Datenmodells

Im Abschlussbericht für Stufe 1 der Challenge ist die Funktionsweise des Datenmodells und des Resource Description Frameworks (RDF) beschrieben. In diesem Resource Description Framework werden Informationen und Ressourcen über Prädikate miteinander verknüpft, so dass sogenannte semantische Tripel bestehend aus Subjekt, Prädikat und Objekt entstehen[^53].

Das in diesem Vorhaben entwickelte Datenmodell bildet die logische Grundlage eines Metadatenstandards in der Post-COVID-Forschung; es bildet ab, welche Klassen mit welchen Attributen versehen sind, insbesondere deren Verpflichtungsgrade und Kardinalitäten (Pflicht, Empfohlen, Optional). Es legt weiterhin benannte Beziehungen zu anderen Klassen fest, die wiederum Verpflichtungsgrade haben können. Metadatensätze als Instanzen des Modells sind semantische Tripel, deren Subjekte, Prädikate und Objekte Instanzen der Klassen, Attribute und Beziehungen des Modells sind. Wenn das Modell beispielsweise verpflichtend die Angabe einer Beziehung zwischen zwei Klassen vorschreibt, so enthält der Metadatensatz diese Beziehung zwischen zwei Instanzen der Klassen in Form eines semantischen Tripels.

Im Sinne der Interoperabilität wurde das Datenmodell basierend auf den Anwendungsprofilen und RDF-Vokabularen DCAT, DCAT-AP, HealthDCAT-AP, Croissant, Data Privacy Vocabulary (DPV) sowie Data Quality Vocabulary (DQV) entwickelt. Kurze Beschreibungen der Anwendungsprofile beziehungsweise Vokabulare finden sich im Bericht von Stufe 1[^54]. Anpassungen dieser Vokabulare und Anwendungsprofile bedingen daher Änderungen des hier vorgestellten Modells. In diesem Sinne handelt es sich somit um eine ökosystemorientierte Entwicklung, die im folgenden Unterkapitel dargestellt wird. Der entsprechende Betrieb und die Nachnutzung des Datenmodells werden im darauffolgenden Unterkapitel behandelt. Das dritte Unterkapitel gibt dann einen konkreten Einblick in die inhaltlichen Änderungen, die in Stufe 2 durchgeführt wurden.

Der aktuelle Stand des Datenmodells kann dem UML-Diagramm entnommen werden, das sich auf dem GitHub des Vorhabens befindet. Dort sind sowohl die UML-Serialisierung als auch eine Grafik-Datei verfügbar[^55].

[nächstes Kapitel](https://healthdcat-ap-de.github.io/healthdcat-ap.de/report_stage_2/5_Weiterentwicklung_des_Datenmodells/5.1_Standardentwicklung_im_Oekosystem.html)

[^53]: vgl. Bericht für Stufe 1: https://healthdcat-ap-de.github.io/healthdcat-ap.de/report_stage_1/2_Ausrichtung_ des_Datenmodells_an_den_Anforderungen_der_Forschung/2.5_Initialversion_Datenmodell/2.5.1_Konzept_fuer_ein_offenes_semantisches_Metadatenmodell.html
[^54]: vgl. Bericht für Stufe 1: https://healthdcat-ap-de.github.io/healthdcat-ap.de/report_stage_1/2_Ausrichtung_ des_Datenmodells_an_den_Anforderungen_der_Forschung/2.5_Initialversion_Datenmodell/2.5.2_Europaeische_und_internationale_RDF-Standards.html
[^55]: vgl. healthdcat-ap.de/model at main · HealthDCAT-AP-de/healthdcat-ap.de
