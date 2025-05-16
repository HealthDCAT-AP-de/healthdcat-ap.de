# HealthDCAT-AP.de Spezifikation

###### Aktuelle Version
###### Voraussichtliches Veröffentlichungsdatum 
###### Letzte Änderung  
###### Beteiligte 
###### Feedback
##### Pflegekonzept HealthDCAT-AP.de
##### Konventionenhandbuch HealthDCAT-AP.de
##### URI-Konzept HealthDCAT-AP.de

## Zusammenfassung 

HealthDCAT-AP.de ist ein im Rahmen der Post-COVID-Challenge anlässlich der Gründung des Dateninstitutes des Bundes entwickelter Datenkatalog-Standard für Daten im Gesundheitsbereich. 

Hintergrund ist die Erforschung des Post-COVID-Syndroms, also Beschwerden, die mindestens zwölf Wochen oder länger nach der akuten COVID-Infektion vorliegen. Dies ist von hoher gesellschaftlicher Relevanz. Analog zu ME/CFS (Myalgische Enzephalomyelitis/Chronisches Fatigue-Syndrom) ist die Forschung durch heterogene und zugleich oft diffuse Symptome erschwert. Das Fehlen gepflegter Datensätze und insbesondere gepflegter Metadatensätze, die eine Verknüpfung zwischen den einzelnen Datensätzen und somit auch Verknüpfungen zwischen Risikofaktoren und Symptomen erlauben, stellte bisher ein weiteres Hindernis für die Auswertung der Daten dar. Da die Daten aus verschiedenen medizinischen Fachbereichen und weiteren Quellen kommen, unterstützt der für die Datenkatalog-Spezifikation gewählte technologische Ansatz (Semantic Web) insbesondere die Nutzung der FAIR-Prinzipien (Findable, Accessible, Interoperable, Re-usable).

Als international zu bewertende Fragestellung müssen Konzepte zur Adressierung der oben beschriebenen Problemlage ebenso international gedacht werden. Für den europäischen Datenraum sind mit dem Konzept des European Data Spaces und dessen fachliche Ausprägung im Gesundheitsbereich (Health), also dem  European Health Data Space (EHDS), der Verordnung für ein interoperables Europa wichtige gesetzliche Grundlagen gelegt worden, die auch auf die harmonisierungsbedürfte Ebene der [semantischen Interoperabilität](https://www.it-planungsrat.de/fileadmin/beschluesse/2024/Information2024_16_AL_PG_Semantische_Interoperabilit%C3%A4t__Anlage_1.pdf) einzahlt.

Zwar existieren bereits sektorspezifische Datenformate und -konzepte wie HL7/FHIR, Thesauri, Taxonomien, Ontologien, Applikationsprofile und auch vereinzelt Wissensgraphen; ein auf den Gesundheitssektor angepasster Datenkatalog-Standard, der die für einen übergreifenden Datenraum benötigten Funktionen unterstützt, ist jedoch bisher noch nicht vorhanden.

Im Rahmen des Vorhabens HealthDCAT-AP.de wurde aufgrund dessen eine Spezifikation aus einem EU-Datenmodell abgeleitet. Das Vorhaben HealthDCAT-AP.de berücksichtigt dabei das EU Pilotprojekt HealthData@EU und das dort entwickelte Datenmodell HealthDCAT-AP sowie die darunter vom Generaldirektorat Informatik (DG Digital Services) entwickelte Spezifikation DCAT-AP. Dieses wird mittelfristig mithilfe von Instanzdaten zu einem Wissensgraphen weiterentwickelt. 

HealthDCAT-AP.de wurde im Rahmen der Kooperation der ]init[ AG und des WIG2-Instituts im Rahmen der Challenge für das Dateninstitut im 2. Halbjahr 2024 entwickelt, und in Workshops Bedarfsträgern und weiteren Stakeholdern aus der Fachlichkeit [vorgestellt](https://www.youtube.com/@HealthDCAT-AP).  

## Inhaltsverzeichnis
[1. Kontext](#1-kontext)

[2. Zugrundeliegende Datenmodelle und Spezifikationen](#2-zugrundeliegende-datenmodelle-und-spezifikationen)

[3. Überblick über HealthDCAT-AP.de](#3-überblick-über-healthdcat-apde)

[4. Klassen](#4-klassen) 

[5. Kontrollierte Vokabulare](#5-kontrollierte-vokabulare)

[6. Glossar](#6-glossar) 

[7. Changelog](#7-changelog) 

## 1. Kontext
### 1.1 Post-COVID Challenge
Das in dieser Spezifikation beschriebene Datenmodell wurde im Rahmen der Post-COVID-Challenge entwickelt, die vom Bundesministerium des Innern und für Heimat (BMI) zusammen mit dem Bundesministerium für Wirtschaft und Klimaschutz (BMWK) initiiert wurde. 
Ziel der Challenge ist die Erstellung eines sektorübergreifenden, offenen und frei verfügbaren Datenmodells zur Unterstützung der Post-COVID-Forschung. Das Modell soll dazu beitragen, Informationen auffindbar, zugänglich und auswertbar zu machen. Dadurch soll es erleichtert werden, die gesellschaftlich hochrelevante Krankheit besser zu verstehen. Insbesondere durch die einheitlichere Bereitstellung und Verknüpfung von Metadaten zu existierenden Daten in z.B. Studien soll die Datenlage zu Post-COVID verbessert werden.
Das hier vorgestellte Metadatenmodell ist ein Resultat der Stufen 1 und 2 dieser Challenge und stellt wesentliche Vorarbeit für die Schaffung eines nationalen Gesundheitsmetadatenprofils dar.

### 1.2 Init AG
Das Unternehmen ]init[ AG für digitale Kommunikation zählt zu den Marktführern für innovative Lösungen in den Bereichen E-Government, E-Democracy und E-Business. Über 1.400 Mitarbeiter:innen an den Standorten Berlin, Mainz, München, Köln, Hamburg und Leipzig konzipieren und realisieren unter dem Motto "Services for the eSociety" auf Basis moderner Informations- und Kommunikationstechnologien maßgeschneiderte Lösungen für nationale wie internationale Regierungen und
Verwaltungen, NGOs sowie weitere gesellschaftliche Akteure. Als Vision hat sich ]init[ zum Ziel gesetzt, den gesellschaftlichen Akteuren und Organisationen eine Führungsrolle in der modernen Gesellschaft zu ermöglichen. Dabei gestaltet ]init[ durch innovative Lösungen den Veränderungsprozess von Organisationen und steigert so ihre Wertschöpfung nachhaltig. ]init[ versteht sich dabei als Innovator auf Basis ausgewiesener fachlicher und technologischer Expertise, vielfältigen Referenzen sowie der individuellen Kompetenzen unserer Mitarbeiter:innen.

### 3.3 WIG2 Institut
Das WIG2 Institut ist eine unabhängige und neutrale Forschungseinrichtung, die evidenzbasierte Antworten auf komplexe Fragestellungen im Gesundheitswesen liefert.
Seit der Gründung des WIG2 Instituts im Jahr 2014 begleitet es aktiv gesundheitspolitische Themen und systemische Fragestellungen wie die Evaluation integrierter, innovativer Versorgungsmodelle oder die Entwicklung des Morbi-RSA als Kerninstrument des deutschen Gesundheitssystems. Darüber hinaus nimmt es das Gesundheitswesen über verschiedene Schwerpunktthemen in den Blick. Diese Schwerpunktthemen beinhalten unter anderem Gesundheitspolitisches Handeln sowie Regionale Versorgungsstrukturen. 


## 2. Zugrundeliegende Datenmodelle und Spezifikationen
In diesem Abschnitt werden die HealthDCAT-AP.de zugrundeliegenden Datenmodelle und -spezifikationen beschrieben.

### 2.1 Verwendete Datenmodelle

#### 2.1.1 Dublin Core
Dublin Core ist ein grundlegender Metadatenstandard, der nach einer in Dublin, Ohio stattfindenden Konferenz im Jahr 1995 entwickelt wurde, um digitale Ressourcen und deren Metadaten zu beschreiben. Der Standard besteht aus 15 Kernelementen, die eine einfache, aber flexible Struktur für die Dokumentation von Informationen bieten, einschließlich Titel, Autor, Datum und Beschreibung. Dublin Core ist weit verbreitet und wird vor allem in digitalen Bibliotheken, Archiven, wissenschaftlichen Publikationen und auf Webseiten verwendet, um Ressourcen auffindbar und zugänglich zu machen. Die Elemente von Dublin Core sind sowohl für einfache Anwendungen als auch für komplexere, semantische Anforderungen anpassbar. Als universelles Basisvokabular bietet Dublin Core eine Grundlage, auf der viele spezifische Profile und Erweiterungen aufbauen, um den unterschiedlichen Anforderungen und Kontexten gerecht zu werden.

#### 2.1.2 DCAT
DCAT ist ein grundlegendes Vokabular, das von der W3C entwickelt wurde, um Datenkataloge, Datensätze und deren Verfügbarkeiten (Distributions) in einem maschinenlesbaren Format zu standardisieren. Es bildet eine wichtige Grundlage für die Interoperabilität und das Linked Data-Prinzip in offenen Datenportalen. DCAT definiert zentrale Entitäten wie Catalog, Dataset, Distribution und DataService sowie deren Eigenschaften.
Ziel von DCAT ist es, Datensätze auffindbar, zugänglich und interoperabel zu machen, unabhängig von der Plattform. Als Basisvokabular bietet DCAT die strukturellen Elemente, auf denen spezifische Profile, wie DCAT-AP, aufbauen können.
]

#### 2.1.3 DCAT-AP
DCAT-AP ist ein auf DCAT aufbauendes Anwendungsprofil, das von der Europäischen Kommission im Rahmen der ISA²-Initiative entwickelt wurde. Es erweitert DCAT um Eigenschaften zur Abdeckung spezifischer Anforderungen und verwendete kontrollierte [Vokabulare des Amtes für amtliche Veröffentlichungen der EU](https://op.europa.eu/de/web/eu-vocabularies), die den Austausch von Metadaten zwischen europäischen Datenportalen erleichtern.
Es definiert verbindliche, empfohlene und optionale Eigenschaften, wie etwa Aussagen zum publisher, zur Lizenz oder zur thematischen Einordnung, und sorgt somit dank der funktionalen Vorgaben nicht nur für eine Harmonisierung des Frontends in den Open Data Portalen der Mitgliedstaaten der EU. Es sorgt auch durch eine Harmonisierung der Metadatenstrukturen im Backend für eine gesteigerte Auffindbarkeit und einfachere Nachnutzung. 
Der Einsatz von DCAT-AP ermöglicht es also, Metadaten in einem einheitlichen Format bereitzustellen und durch den Einsatz von Linked Data-Technologien maschinenlesbar zu machen. Dies durch die Art der Ausgestaltung nach dem "Open World Paradigma" und der Verwendung bereits verbreiteter Vokabulare und Microformate (siehe Dublin Core) sogar für Systeme, denen die Struktur des Metadatenprofils im Voraus nicht bekannt ist. DCAT-AP wurde speziell auf den europäischen Kontext zugeschnitten und dient als Grundlage für nationale und sektorspezifische Erweiterungen, wie DCAT-AP.de.

#### 2.1.4 DCAT-AP.de
DCAT-AP.de ist die deutsche Ableitung des europäischen DCAT-AP-Standards. Es wurde entwickelt, um den Standardisierungsbedarf "offener Verwaltungsdaten" in Deutschland sicherzustellen. DCAT-AP.de berücksichtigt die spezifischen Anforderungen deutscher Datenportale und Behörden sowie nationale rechtliche Rahmenbedingungen. Es ist indirekt gesetzlich verankert durch a) eGovGesetzdie Pflichte Offene Daten an das GovData Portal anzu
Es erweitert DCAT-AP um zusätzliche kontrollierte Vokabulare und Attribute, die für den deutschen Kontext relevant sind, z. B. spezifische Lizenzangaben und Sprachinformationen. DCAT-AP.de wird von deutschen Behörden und Open-Data-Plattformen verwendet, um den Austausch und die Wiederverwendbarkeit von Verwaltungsdaten zu optimieren. Zugleich bleibt es dabei vollständig kompatibel mit DCAT-AP und dem zugrunde liegenden W3C-DCAT-Standard.

#### 2.1.5 HealthDCAT-AP
HealthDCAT-AP ist ein spezialisiertes Anwendungsprofil des DCAT-AP, das entwickelt wurde, um Metadaten für Gesundheitsdatensätze im Rahmen des Europäischen Gesundheitsdatenraums (EHDS) zu standardisieren. Es erweitert DCAT-AP um spezifische Klassen und Eigenschaften, die spezifische Anforderungen von Gesundheitsdaten abdecken sollen, einschließlich der Aspekte Datenschutz und Sicherheit. Durch die Anpassung an die EHDS-Verordnung fördert HealthDCAT-AP die Interoperabilität und erleichtert den grenzüberschreitenden Austausch von Gesundheitsdaten innerhalb der EU. Es baut auf den Prinzipien von DCAT und DCAT-AP auf und integriert zusätzliche Mechanismen, um die Auffindbarkeit und Zugänglichkeit von elektronischen Gesundheitsdaten zu verbessern.

#### 2.1.6 Croissant
Die auf dem schema.org-Vokabular aufbauende Croissant-Spezifikation liegt seit März 2024 in Version 1.0 vor. Herausgeber ist das MLCommons-Konsortium. Es wurde entwickelt, um die Nutzung von Datensätzen in maschinellen Lernmodellen zu vereinfachen. Sie bietet ein Vokabular für Datensatzattribute und standardisiert die Art und Weise, wie Daten in verschiedenen maschinellen Lern-Frameworks wie PyTorch, TensorFlow oder JAX geladen werden. Durch die Vereinheitlichung der Beschreibung und Semantik von ML-Datensätzen erleichtert die Croissant-Spezifikation Forschern und Praktikern das Erkunden, Verstehen und Nutzen einer breiten Palette von Datensätzen. Sie baut auf bestehenden Standards auf und zielt darauf ab, die Interoperabilität und Wiederverwendbarkeit von Daten im Bereich des maschinellen Lernens zu verbessern

#### 2.1.7 Data Privacy Vocabulary
Das Data Privacy Vocabulary (DPV) ist ein standardisiertes Vokabular der W3C, das Datenschutzinformationen maschinenlesbar beschreibt und standardisiert. Es dient der Interoperabilität und dem Verständnis von Datenschutzanforderungen in verschiedenen Systemen. DPV definiert zentrale Entitäten wie z.B. DataSubject, DataController, Processing, Purpose und DataRecipient sowie deren Eigenschaften.
Ziel des DPV ist es, Datenschutzaspekte transparent zu dokumentieren und die Einhaltung von Vorschriften wie der DSGVO zu unterstützen. Als flexibles Vokabular bildet es die Grundlage für spezifische Datenschutzprofile und Erweiterungen, die unterschiedliche rechtliche Anforderungen und Implementierungen abbilden.

#### 2.1.8 Data Quality Vocabulary
Das Data Quality Vocabulary (DQV) ist ein standardisiertes Vokabular der W3C, das dazu dient, die Qualität von Daten in einem maschinenlesbaren Format zu beschreiben. Es definiert zentrale Entitäten wie z.B. DataQualityMetric, DataQualityDimension, DataQualityAssessment und DataQualityRequirement sowie deren Eigenschaften.
Ziel des DQV ist es, die Qualität von Daten systematisch zu erfassen und zu kommunizieren, um eine bessere Nutzung und Entscheidungsfindung zu ermöglichen. Als flexibles Vokabular bildet es die Basis für die Entwicklung spezifischer Qualitätsprofile und Standards, die in verschiedenen Kontexten und für unterschiedliche Anwendungsfälle genutzt werden können.

## 2.2 Verwendete Spezifikationen
| **Namespace** | **URI des Namespace** | **Name der Spezifikation** |
|---------|-----------------|-----------------|
| adms | http://www.w3.org/ns/adms# | Asset Description Metadata Schema |
| cr | http://mlcommons.org/croissant/1.0 | Croissant Format Specification | 
| dcat | http://www.w3.org/ns/dcat# | Data Catalog Vocabulary | 
| dcatap | http://data.europa.eu/r5r/ | DCAT Application profile for data portals in Europe (DCAT-AP) | 
| dcatde | http://dcat-ap.de/def/dcatde/ | German Adaptation of DCAT-AP | 
| dcterms | http://purl.org/dc/terms/ | DCMI (Dublin Core Metadata Initiative) Metadata Terms | 
| foaf | http://xmlns.com/foaf/0.1/ | FOAF (Friend of a friend) Vocabulary | 
| geodcatap | https://semiceu.github.io/GeoDCAT-AP/releases/3.0.0/ | Etension of the DCAT application profile describing geospatial datasets, dataset series, and services |
| healthdcatap | https://healthdcat-ap.github.io/ | Health-related extension of the DCAT application profile | 
| healthdcatapde | N/A | German Adaptation of HealthDCAT-AP | 
| locn | http://www.w3.org/ns/locn# | ISA Programme Location Core Vocabulary | 
| odrl | http://www.w3.org/ns/odrl/2/ | Open Digital Rights Language | 
| rdfs | http://www.w3.org/2000/01/rdf-schema# | RDF (Resource Description Framework) Vocabulary Description Language 1.0: RDF Schema | 
| schema | http://schema.org/ | Vocabulary for structured data on the Internet | 
| skos | http://www.w3.org/2004/02/skos/core# | SKOS Simple Knowledge Organization System – Reference | 
| spdx | http://spdx.org/rdf/terms# | Software Package Data Exchange | 
| time | http://www.w3.org/2006/time# | OWL-Time is an OWL-2 DL ontology of temporal concepts, for describing the temporal properties of resources | 
| vcard | http://www.w3.org/2006/vcard/ns# | File format standard for electronic business cards | 
| xsd | http://www.w3.org/2001/XMLSchema# | XML Schema Part 2: Datatypes Second Edition | 


## 3. Überblick über HealthDCAT-AP.de 
Als ein Austauschstandard für Gesundheitsdaten im Rahmen der Post-COVID Forschung ist der Hauptanwendungsfall von DCAT-AP.de der Austausch von Metadaten zwischen verschiedenen Akteuren des Gesundheitssektors. Dabei wird in den meisten Fällen ein Datensatz (`dcat:Dataset`) mit verschiedenen Ausprägungen (`dcat:Distribution`) aus einem Datenkatalog (`dcat:Catalog`) in der Forschung genutzt. Dieser Datensatz wiederum ist mit einer Person oder Organisation (`foaf:Agent`) assoziert. Um die Lesbarkeit und Anbindung an KI-Lösungen zu verbessern wird hierbei auch die Klasse `cr:FileObject`vergeben. 
Diese und alle weiteren ergänzenden Klassen sind unter Punkt 5 näher erläutert. 

Zum besseren visuellen Verständnis wurde ebenso ein UML Diagramm erstellt. 

![Preview:_Healthdcatapde-extended_draft](https://github.com/HealthDCAT-AP-de/healthdcat-ap.de/blob/main/model/preview_healthdcatapde_extended_draft.svg?raw=True)

## 4. Klassen

### 4.1. Verpflichtende Klassen 
Diese Klassen sind für die korrekte Verwendung des Modells verpflichtend notwendig. Sie sind notwendig um die Interoperbilität zwischen verschiedenen Datensätzen zu gewährleisten. Zugleich wurde sich hierbei auf eine möglichst geringe Anzahl an Klassen beschränkt, um die Hürden für die Verwendung des Modells gering zu halten. Ergänzend dazu sind daher unter 5.2 daher auch empfohlene Klassen aufgelistet, die zusätzliche Informationen beinhalten und den Nutzen des Datenmodells erweitern. 

[`dcat:Catalog`](#512-klasse-dcatcatalog) 

[`dcat:Dataset`](#513-klasse-dcatdataset) 

[`cr:FileObject`](#514-klasse-crfileobject) 

[`dcat:Distribution`](#515-klasse-dcatdistribution) 

[`foaf:Agent`](#516-klasse-foafagent) 

[`skos:Concept`](#517-klasse-skosconcept) 

#### 4.1.1 Klasse: dcat:Resource 
> | *URI der Klasse* | [`dcat:Resource`](https://www.w3.org/ns/dcat#Resource) |
> |:-----------------|:----------------------------------------------------|
> | Beschreibung     | Ressource, die von einem einzelnen Akteur veröffentlicht oder kuratiert wurde. Diese Klasse wird in HealthDCAT-AP.de nicht direkt verwendet, jedoch ihre Subklassen. |
> | Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-3/#Class:Resource |

#### 4.1.2 Klasse: dcat:Catalog
> | *URI der Klasse* | [`dcat:Catalog`](http://www.w3.org/ns/dcat#Catalog) |
> |:-----------------|:----------------------------------------------------|
> | Beschreibung     | Eine Sammlung oder Quelle, welche die beschriebenen Datensätze, Datenservices oder Kataloge zur Verfügung stellt. |
> | Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-3/#Class:Catalog |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dcatap:applicableLegislation`](https://semiceu.github.io/DCAT-AP/r5r/releases/3.0.0/#applicableLegislation) | `rdfs:Resource` | `1..*` | Verpflichtend | Diese Eigenschaft gibt die rechtlichen Grundlagen für die im Katalog enthaltenen Daten an. |
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine Beschreibung des Kataloges als Freitext. |
| [`dct:title`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft bezeichnet den einem Katalog zugewiesenen Titel. |
| [dct:publisher](http://purl.org/dc/terms/publisher) | `foaf:Agent` | `1` | Verpflichtend | Diese Eigenschaft bezieht sich auf die Stelle oder Person, die verantwortlich für Bereitstellung des Kataloges ist. |
| [`dct:issued`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#issued) | `rdfs:Literal` | `0..1` | Empfohlen |  Diese Eigenschaft enthält das Datum der Herausgabe/Emission (z.B. in Form einer Veröffentlichung) des Kataloges. |
| [`dct:language`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#language) | `dct:LinguisticSystem` | `*` | Empfohlen |  Diese Eigenschaft bezieht sich auf die Sprache, die in den textuellen Beschreibungen der dem Katalog zugehörigen Ressourcen Verwendung findet (z.B. Titel, Beschreibungen usw.). |
| [`dct:license`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#LicenseDocument) | `dct:LicenseDocument` | `0..1` | Empfohlen |  Diese Eigenschaft bezieht sich auf die Lizenz, mit welcher der Katalog verwendet oder wiederverwendet werden kann. |
| [`dct:modified`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#modified) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft erfasst das Datum der letzten Aktualisierung bzw. Modifikation des Kataloges. |
| [`foaf:homepage`](http://xmlns.com/foaf/spec/#term_homepage) | `foaf:Document` | `0..1` | Empfohlen | Diese Eigenschaft verweist auf eine Homepage, welche die zentrale Homepage des Kataloges ist. |
| [dcat:dataset](https://www.w3.org/ns/dcat#dataset) | `dcat:Dataset` | `*` | Empfohlen |  	Diese Eigenschaft verknüpft den Katalog mit einem Datensatz, welcher somit Teil des Kataloges wird. |
| [`dct:rights`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#RightsStatement) | `dct:RightsStatement` | `0..1` | Optional | Diese Eigenschaft verweist auf eine juristische Darlegung, welche die mit dem Katalog assoziierten Nutzungsbestimmungen spezifiziert. |
| [dcat:service](https://www.w3.org/ns/dcat#service) | `dcat:DataService` | `*` | Empfohlen |  Diese Eigenschaft verknüpft den Katalog mit einem Datenservice, welcher somit Teil des Kataloges wird. |
| [dct:spatial](http://purl.org/dc/terms/spatial) | `dct:Location` | `*` | Empfohlen |  	Diese Eigenschaft bezieht sich auf einen vom Katalog abgedeckten geographischen Bereich.  |
| [dcat:record](https://www.w3.org/ns/dcat#record) | `dcat:CatalogRecord` | `*` | Empfohlen |  Diese Eigenschaft bezieht sich auf den Katalogeintrag, welcher Teil des Kataloges ist. |
| [dcat:themeTaxonomy](http://www.w3.org/ns/dcat#themeTaxonomy) | `skos:ConceptScheme` | `*` | Empfohlen |  Diese Eigenschaft verweist auf das eingesetzte Schema zur Klassifizierung der dem Katalog zugewiesenen DCAT-Ressourcen in Form von Kategorien. |
| [dct:hasPart](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#hasPart) | `dcat:Catalog` | `*` | Optional | Diese Eigenschaft verweist auf einen in Beziehung stehenden Unterkatalog, der Teil des beschriebenen Kataloges ist. |
| [dct:isPartOf](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#isPartOf) | `dcat:Catalog` | `*` | Optional |  Diese Eigenschaft verweist auf einen in Beziehung stehenden Hauptkatalog, in welchem der beschriebene Katalog physikalisch oder logisch eingebunden ist. | 
| [dcat:catalog](https://www.w3.org/ns/dcat#catalog) | `dcat:Catalog` | `*` | Optional |  	Diese Eigenschaft verweist auf einen Katalog, dessen Inhalt im Kontext dieses Katalogs von Interesse ist. |
| [dct:creator](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#creator) | `foaf:Agent` | `*` | Optional |  Diese Eigenschaft verweist auf Stellen oder Personen, die den Katalog erstellt hat.|
| [dct:temporal](http://purl.org/dc/terms/temporal) | `dct:PeriodOfTime` | `*` | Optional |  Diese Eigenschaft verweist auf ein Zeitintervall, welches durch Start- und Endzeitpunkt bezeichnet bzw. definiert ist. |


#### 4.1.3 Klasse: dcat:Dataset
>| *URI der Klasse* | [`dcat:Dataset`](http://www.w3.org/ns/dcat#Dataset) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     |  	Eine logische Entität, welche die veröffentlichten Informationen repräsentiert. |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-3/#Class:Dataset |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dcatap:applicableLegislation`](https://semiceu.github.io/DCAT-AP/r5r/releases/3.0.0/#applicableLegislation) | `rdfs:Resource` | `1..*` | Verpflichtend |  	Die Rechtsvorschriften, die die Erstellung oder Verwaltung des Datensatzes vorschreiben. |
| [`dct:accessRights`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#accessRights) | `dct:RightsStatement` | `1` | Verpflichtend | Diese Eigenschaft verweist auf Informationen, die darlegen, ob der Datensatz öffentlich zugänglich ist, Zugriffseinschränkungen existieren oder er nicht-öffentlich ist. |
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine Beschreibung des Datensatzes als Freitext. |
| [`dct:identifier`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#identifier) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält die Haupt-ID des Datensatzes im Kontext des jeweiligen Kataloges (z.B. die URI-Adresse oder eine andere eindeutige ID). |
| [`dct:provenance`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#provenance) | `dct:ProvenanceStatement` | `1..*` | Verpflichtend | Diese Eigenschaft umfasst eine Angabe zur Entwicklungsgeschichte des Datensatzes, insbesondere in wessen Besitz oder Obhut die Ressource sich bislang befunden hat, soweit die Wechsel signifikanten Einfluss auf die Authentizität, Integrität und Interpretierbarkeit dieser Ressource hat.. |
| [`dct:title`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft bezeichnet den einem Datenservice zugewiesenen Titel. Sie kann für parallele Sprachversionen wiederholt werden. |
| [`dpv:hasPersonalData`](https://w3c.github.io/dpv/2.0/dpv/#hasPersonalData) | `dpv:personalData` | `1..*` | Verpflichtend | Diese Eigenschaft zeigt an, dass ein Datensatz personenbezogene Daten enthält. |
| [`healthdcatap:numberOfRecords`](https://healthdcat-ap.github.io/#healthdcatapnumberofrecords) | `xsd:nonNegativeInteger` | `1` | Verpflichtend | Diese Eigenschaft gibt die Anzahl der Datensätze im Datensatz an. |
| [`healthdcatap:numberOfUniqueIndividuals`](https://healthdcat-ap.github.io/#healthdcatapnumberofuniqueindividuals) | `xsd:nonNegativeInteger` | `1` | Verpflichtend | Diese Eigenschaft gibt die Anzahl der Einzelpersonen im Datensatz an. |
| [`healthdcatap:populationCoverage`](https://healthdcat-ap.github.io/#healthdcatappopulationcoverage) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft gibt eine Definition der im Datensatz abgedeckten Population in natürlicher Sprache an. |
| [dcat:theme](http://www.w3.org/ns/dcat#theme) | `skos:Concept` | `1..*` | Verpflichtend |  Diese Eigenschaft bezieht sich auf die dem Datensatz zugewiesenen Kategorien. Mit einem Datensatz können mehrere Kategorien assoziiert sein. |
| [dct:type](http://purl.org/dc/terms/type) | `skos:Concept` | `1` | Verpflichtend | Diese Eigenschaft bezieht sich auf den Typ des Datensatzes. |
| [healthdcatap:healthCategory](https://healthdcat-ap.github.io/#healthdcataphealthCategory) | `skos:Concept` | `1..*` | Verpflichtend | Diese Eigenschaft verweist auf die Gesundheitskategorie, zu der dieser Datensatz gehört.|
| [dct:publisher](http://purl.org/dc/terms/publisher) | `foaf:Agent` | `1` | Verpflichtend |  Diese Eigenschaft verweist auf die Stelle oder Person, die für Bereitstellung des Datensatzes verantwortlich ist. |
| [dct:spatial](http://purl.org/dc/terms/spatial) | `dct:Location` | `1..*` | Verpflichtend | Ein räumlicher Bereich oder ein bezeichneter Ort. |
| [healthdcatap:hdab](https://healthdcat-ap.github.io/#healthdcataphdab) | `foaf:Agent` | `1` | Verpflichtend | Diese Eigenschaft verweist auf die Stelle für den Zugang zu den Gesundheitsdaten, die den entsprechenden Zugang dazu im jeweiligen Staat unterstützt. |
| [`healthdcatap:maxTypicalAge`](https://healthdcat-ap.github.io/#healthdcatapmaxTypicalAge) | `xsd:nonNegativeInteger` | `0..1` | Empfohlen | Diese Eigenschaft gibt das maximale Alter an, das im Datensatz enthalten ist. |
| [`healthdcatap:minTypicalAge`](https://healthdcat-ap.github.io/#healthdcatapminTypicalAge) | `xsd:nonNegativeInteger` | `0..1` | Empfohlen | Diese Eigenschaft gibt den Minimalwert des Alters an, das im Datensatz enthalten ist. |
| [`dcat:contactPoint`](https://www.w3.org/ns/dcat#contactPoint) | `vcard:Kind` | `*` | Empfohlen | Diese Eigenschaft gibt relevante Kontaktinformationen für den Datensatz an.|
| [`dcat:keyword`](https://www.w3.org/ns/dcat#keyword) | `rdfs:Literal` | `*` | Empfohlen | Diese Eigenschaft enthält Schlagwörter oder Tags, die den Datensatz beschreiben. |
| [`dpv:hasLegalBasis`](https://w3c.github.io/dpv/2.0/dpv/#hasLegalBasis) | `rdfs:Resource` | `*` | Empfohlen | Diese Eigenschaft gibt die rechtliche Grundlage an, auf der die Verarbeitung personenbezogener Daten basiert. |
| [`dpv:hasPurpose`](https://w3c.github.io/dpv/2.0/dpv/#hasPurpose) | `rdfs:Resource` | `*` | Empfohlen | Diese Eigenschaft gibt den Zweck der Verarbeitung personenbezogener Daten an. |
| [`dqv:hasQualityAnnotation`](https://www.w3.org/TR/vocab-dqv/#dqv:hasQualityAnnotation) | `dqv:QualityAnnotaion` | `*` | Empfohlen | Diese Eigenschaft verbindet einen Datensatz mit einer anderen Ressource (z. B. einem Dokument), welches die Qualität des Datensatzes beschreibt. |
| [`healthdcatap:publisherNote`](https://healthdcat-ap.github.io/#healthdcatappublishernote) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft enthält eine Kurzbeschreibung des Herausgebers des Datensatzes und seiner Aktivitäten. |
| [healthdcatap:healthTheme](https://healthdcat-ap.github.io/#healthdcataphealththeme) | `skos:Concept` | `*` | Empfohlen | Diese Eigenschaft verweist auf eine Kategorie des Datensatzes oder ein Tag zur Beschreibung des Datensatzes. |
| [healthdcatap:hasCodeValues](https://healthdcat-ap.github.io/#healthdcataphasCodeValues) | `skos:Concept` | `*` | Empfohlen | Diese Eigenschaft verweist auf Gesundheitsklassifikationen und ihre Codes, die mit dem Datensatz verbunden sind.  |
| [healthdcatap:publisherType](https://healthdcat-ap.github.io/#healthdcatappublishertype) | `skos:Concept` | `0..1` | Empfohlen | Diese Eigenschaft verweist auf eine Art von Organisation, die den Datensatz zur Verfügung stellt.  |
| [cr:recordSet]("https://docs.mlcommons.org/croissant/docs/croissant-spec.html#recordset") | `cr:RecordSet` | `*` | Empfohlen | Diese Eigenschaft verweist auf eine Menge von strukturierten Datensätzen aus einer oder mehreren Datenquellen. |
| [healthdcatap:analytics](https://healthdcat-ap.github.io/#Dataset.analytics) | `dcat:Distribution` | `*` | Empfohlen | Diese Eigenschaft verweist auf eine analytische Verteilung des Datensatzes.  |
| [cr:distribution](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#distribution) | `cr:FileObject` | `1..*` | Empfohlen | Diese Eigenschaft verweist auf die grundlegende Einheit innerhalb des Croissant Metadatendstandards, welche die einzelnen Daten innerhalb eines Datensets beschreibt. |
| [adms:sample](http://www.w3.org/ns/adms#sample) | `dcat:Distribution` | `*` | Empfohlen | Diese Eigenschaft verweist auf eine Beispieldistribution des Datensatzes. |
| [dcat:distribution](http://www.w3.org/ns/dcat#distribution) | `dcat:Distribution` | `*` | Empfohlen | Diese Eigenschaft verknüpft den Datensatz mit einer verfügbaren Distribution. |
| [dct:temporal](http://purl.org/dc/terms/temporal) | `dct:PeriodOfTime` | `*` | Empfohlen | Diese Eigenschaft verweist auf ein Zeitintervall, welches durch Start- und Endzeitpunkt bezeichnet bzw. definiert ist. |
| [`adms:versionNotes`](https://www.w3.org/TR/vocab-adms/#adms-versionnotes) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft enthält eine Beschreibung der Änderungen im Datensatz im Vergleich zu einer vorherigen Version. |
| [`dcat:landingPage`](https://www.w3.org/ns/dcat#landingPage) | `foaf:Document` | `*` | Optional | Diese Eigenschaft enthält eine Webseite die Zugang auf den Datensatz verschafft.|
| [`dcat:spatialResolutionInMeters`](https://www.w3.org/ns/dcat#spatialResolutionInMeters) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft enthält einen Minimalwert der räumlichen Trennung in Metern.|
| [`dcat:temporalResolution`](https://www.w3.org/ns/dcat#temporalResolution) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf die minimal auflösbare Zeitspanne im Datensatz .|
| [`dcatde:geocodingDescription`](https://www.dcat-ap.de/def/dcatde/2.0/spec/#datensatz-beschreibung-abdeckung) | `rdfs:Resource` | `*` | Optional | Diese Eigenschaft bezieht sich auf eine geopolitische Abdeckung des Datensatzes, etwa durch Kennzeichnung der Verwaltungsebene Bund, Bundesland, Kreis oder Kommune.|
| [`dcatde:politicalGeocodingLevelURI`](https://www.dcat-ap.de/def/dcatde/2.0/spec/#datensatz-ebene-geopolitischen-abdeckung) | `rdfs:Resource` | `*` | Optional | Diese Eigenschaft beschreibt die Geopolitische Abdeckung des Datensatzes, etwa durch Kennzeichnung der Verwaltungsebene Bund, Bundesland, Kreis oder Kommune, in Form einer dcat-ap.de URI. |
| [`dcatde:politicalGeocodingURI`](https://www.dcat-ap.de/def/dcatde/2.0/spec/#datensatz-geopolitischen-abdeckung) | `rdfs:Resource` | `*` | Optional | Diese Eigenschaft verknüpft einen Datensatz mit dem von ihm abgedeckten administrativen Gebiet der Bundesrepublik Deutschland, etwa ein konkretes Bundesland, eine Kommune oder ein Landkreis, repräsentiert durch eine URI.|
| [`dct:accrualPeriodicity`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#accrualPeriodicity) | `dct:Frequency` | `0..1` | Optional | Diese Eigenschaft beschreibt Richtlinie zur Aufnahme von Elementen in einen Datensatz. |
| [`dct:alternative`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/terms/alternative/)  | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft beschreibt einen alternativen Namen oder ein Akronym für einen Datensatz |
| [`dct:conformsTo`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#conformsTo) | `dct:Standard` | `*` | Optional | Diese Eigenschaft verweist auf einen etablierten Standard auf den referenziert wird.|
| [`dcat:inSeries`](https://www.w3.org/ns/dcat#inSeries) | `dcat:Dataseries` | `*` | Optional | Diese Eigenschaft verweist auf die Datensatzserie zu der der Datensatz gehört. |
| [`dct:isReferencedBy`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#isReferencedBy) | `rdfs:Resource` | `*` | Optional | Diese Eigenschaft verweist auf eine Ressource die auf den Datensatz verweist, ihn zitiert oder anderweitig auf ihn hinweist. |
| [`dct:issued`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#issued) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft verweist auf das Veröffentlichungsdatum des Datensatzes.  |
| [`dct:language`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#language) | `dct:LinguisticSystem ` | `*` | Optional | Die Eigenschaft verweist auf die Sprache des Datensatzes. |
| [`dct:modified`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#modified) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft verweist auf die Angabe des Datums (Format: YYYY-MM-DD HH-MM-SS) an dem der Datensatz zuletzt angepasst wurde.|
| [`dct:relation`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#relation) | `rdfs:Resource` | `*` | Optional | Diese Eigenschaft verweist auf eine verwandte Ressource. |
| [`foaf:page`](http://xmlns.com/foaf/spec/) | `foaf:document` | `*` | Optional | Diese Eigenschaft verweist auf eine Seite oder ein Dokument über diesen Datensatz. |
| [`dcat:version`](https://www.w3.org/ns/dcat#version) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft enthält eine Versionsnummer oder anderweitige Versionskennzeichnung des Datensatzes.|
| [`prov:wasGeneratedBy`](https://www.w3.org/TR/prov-o/#wasGeneratedBy) | `prov:Activity` | `*` | Optional | Diese Eigenschaft verweist auf einen Hinweis wie oder mit was der Datensatz technisch erzeugt wurde.|
| [`healthdcatap:hasCodingSystem`](https://healthdcat-ap.github.io/#healthdcataphasCodingSystem) | `dct:Standard` | `*` | Optional | Diese Eigenschaft verweist auf verwendete Codingsysteme wie z.B. ICD-10-CM, DGRs, SNOMED=CT. |
| [`healthdcatapde:targetAudience`]() | `skos:Concept` | `*` | Optional | Diese Eigenschaft verweist auf die Zielgruppe eines Datensatzes. |
| [dct:creator](http://purl.org/dc/terms/creator) | `foaf:Agent` | `*` | Optional |  	Diese Eigenschaft verweist auf Stellen oder Personen, die die Daten erstellt haben. Die Autorenschaft umfasst für gewöhnlich das Recht am geistigen Eigentum. |
| [dct:contributor](http://purl.org/dc/terms/contributor) | `foaf:Agent` | `*` | Optional |  Diese Eigenschaft verweist auf Stellen oder Personen, die die Daten bearbeitet haben (z.B. durch Formatierung derselben). |
| [geodcatap:originator](http://data.europa.eu/930/Originator) | `foaf:Agent` | `*` | Optional | Diese Eigenschaft verweist auf den ursprünglichen Ersteller oder Urheber eines geospatialen Datensatzes.  | 
| [geodcatap:custodian](http://data.europa.eu/930/Custodian) | `foaf:Agent` | `*` | Optional | Diese Eigenschaft verweist auf die verwaltende Person oder Organisation eines geospatialen Datensatzes. |
| [healthdcatap:retentionPeriod](https://healthdcat-ap.github.io/#healthdcatapretentionperiod) | `dct:PeriodOfTime` | `0..1` | Optional | Diese Eigenschaft verweist auf einen Zeitraum, in dem der Datensatz für die Sekundärnutzung zur Verfügung steht. |
| [adms:identifier](http://purl.org/dc/terms/identifier) | `adms:Identifier` | `*` | Optional |  Diese Eigenschaft verweist auf sekundäre IDs des Datensatzes. |
| [dcat:qualifiedRelation](http://www.w3.org/ns/dcat#qualifiedRelation) | `dcat:Relationship` | `*` | Optional |  Link zu einer Beschreibung (in Form der Klasse `dcat:Relationship`) einer Beziehung zu einer anderen Ressource. |
| [prov:qualifiedAttribution](https://www.w3.org/TR/prov-o/#qualifiedAttribution) | `prov:Attribution` | `*` | Optional |  Verbindet den Datensatz über die Klasse prov:Attribution mit einem Agenten, der in beschriebener Weise Verantwortung für ihn trägt. |
| [dct:source](http://purl.org/dc/terms/source) | `dcat:Dataset` | `*` | Optional |  Diese Eigenschaft bezieht sich auf einen verwandten Datensatz, von dem der beschriebene Datensatz abgeleitet ist. |
| [dct:hasVersion](http://purl.org/dc/terms/hasVersion) | `dcat:Dataset` | `*` | Optional |  Diese Eigenschaft bezieht sich auf einen verwandten Datensatz in Form einer weiteren/nachfolgenden Version, Edition oder Adaption des beschriebenen Datensatzes. |
| [dct:isVersionOf](http://purl.org/dc/terms/isVersion) | `dcat:Dataset` | `*` | Optional |  Diese Eigenschaft bezieht sich auf einen verwandten Datensatz, der vom beschriebenen Datensatz eine vorherige Version, Edition oder Adaption ist. |


#### 4.1.4 Klasse: foaf:Agent
>| *URI der Klasse* | [`foaf:Agent`](http://xmlns.com/foaf/spec/#term_Agent) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Eine Stelle oder Person, welche mit Katalogen und Datensätzen in unterschiedlichen Rollenausprägungen assoziiert ist. |
>| Weiterführende Dokumentationen | http://xmlns.com/foaf/spec/#term_Agent |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`foaf:name`]("http://xmlns.com/foaf/spec/#term_name") | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft verweist auf den Namen der Stelle, Person oder Organisation. |
| [dct:type](http://purl.org/dc/terms/type) | `skos:Concept` | `0..1` | Optional |  Diese Eigenschaft bezieht sich auf den Typ der verantwortlichen Stelle, Person oder Organisation, die die Ressource bereitstellt. |


#### 4.1.5 Klasse: skos:Concept 
>| *URI der Klasse* | [`skos:Concept`](https://www.w3.org/TR/skos-reference/#concepts) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | EIn grundlegendes Konzept oder Objekt innerhalb des Modells. |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/skos-reference/#concepts |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`skos:prefLabel`](https://www.w3.org/TR/skos-reference/#labels) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft verweist auf den Titel des Konzepts. |
| [skos:inScheme]( http://www.w3.org/2004/02/skos/core#inScheme) | `skos:ConceptScheme` | `*` | Optional | Diese Eigenschaft verweist auf eine Sammlung von Konzepten/ Begrifflichkeiten von denen dieses `skos:Concept`Teil ist. |


### 4.2 Empfohlene Klassen 
Folgende Klassen werden für die Verwendung des Modells empfohlen. Sie haben einen hohen Mehrwert für das Datenmodell, sind jedoch nicht verpflichtend da die dafür benötigten Informationen für die entsprechenden Klassen in der Praxis eventuell nicht immer vorhanden sind. Sie als nicht verpflichtend aufzulisten erhöht die Flexibilität des Modells und erlaubt die Inklusion weiterer Datensätze, welche die für diese Klassen benötigten Informationen nicht oder nur teilweise aufweisen. 

[`cr:RecordSet`](#521-klasse-crrecordset) 

[`cr:Field`](#522-klasse-crfield)

[`dct:PeriodOfTime`](#523-klasse-dctperiodoftime)

[`dct:LicenceType`](#524-klasse-dctlicencetype) |

#### 4.2.1 Klasse: cr:RecordSet
>| *URI der Klasse* | [`cr:RecordSet`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#recordset) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     |  	Eine Menge von strukturierten Datensätzen aus einer oder mehreren Datenquellen. |
>| Weiterführende Dokumentationen | https://docs.mlcommons.org/croissant/docs/croissant-spec.html |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine Beschreibung für die einzelne Datei, die im RecordSet enthalten ist. |
| [`cr:key`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#key) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft beschreibt ein oder mehrere Felder, deren Werte jeden Datensatz im RecordSet eindeutig identifizieren |
| [cr:field](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#field) | `cr:Field` | `1..*` | Verpflichtend | Diese Eigenschaft verweist auf ein Feld innerhalb eines Datensatzes verweisen, welches dieses `cr:RecordSet` enthält. |
| [`cr:data`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#data) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft beschreibt einen oder mehrere Datensätze, die die Daten des RecordSet bilden. |
| [`sc:examples`]() | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft verweist auf einen oder mehrere Datensätze, die als Beispielinhalt des RecordSet bereitgestellt werden, oder ein Verweis auf eine Datenquelle, die Beispiele enthält. |


#### 4.2.2 Klasse cr:Field
>| *URI der Klasse* | [`cr:Field`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#field) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     |  	Ein Feld innerhalb eines Datensatzes. Es kann auch die Spalte in Tabelle oder innerhalb einer verschachtelte Datenstruktur darstellen. |
>| Weiterführende Dokumentationen | https://docs.mlcommons.org/croissant/docs/croissant-spec.html |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`cr:dataType`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#datatype) | `rdfs:Literal` | `1..*]` | Verpflichtend | Diese Eigenschaft verweist auf den Datentyp des Feldes, identifiziert durch den URI der entsprechenden Klasse. Es kann entweder ein atomarer Typ oder ein semantischer Typ sein. |
| [`cr:source`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#source) | `rdfs:Literal` | `1..*]` | Verpflichtend | Diese Eigenschaft verweist auf eine Datenquelle für ein cr:Field. |
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine Beschreibung für die einzelne Datei, die in cr:Field enthalten ist. |
| [`cr:references`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#references) | `rdfs:Literal` | `*` | Empfohlen | Diese Eigenschaft verweist auf andere cr:Field Elemente in einem anderen cr:RecordSet. |
| [cr:subField](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#subfield) | `cr:Field` | `*` | Optional | Diese Eigenschaft verweist auf ein Feld innerhalb eines anderen Feldes. |
| [cr:parentField](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#parentfield) | `cr:Field` | `*` | Optional | Diese Eigenschaft verweist auf ein `cr:Field` welches bereits im jeweiligen `cr:Recordset`enthalten ist. |


#### 4.2.3 Klasse: dct:PeriodOfTime 
>| *URI der Klasse* | [`dct:PeriodOfTime`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#PeriodOfTime) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Ein Zeitintervall, welches durch Start- und Endzeitpunkt bezeichnet bzw. definiert ist. |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-3/#Class:Period_of_Time |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dcat:endDate`](https://www.w3.org/ns/dcat#endDate) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft beschreibt das Ende eines Zeitintervalls. |
| [`dcat:startDate`](https://www.w3.org/ns/dcat#startDate) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft beschreibt den Start eines Zeitintervalls. |
| [`time:hasBeginning`](https://www.w3.org/TR/owl-time/#time:hasBeginning) | `time:Instant` | `0..1` | Optional | Diese Eigenschaft beschreibt den Anfang einer Periode oder eines Zeitintervalls. |
| [`time:hasEnd`](https://www.w3.org/TR/owl-time/#time:hasEnd) | `time:Instant` | `0..1` | Optional | Diese Eigenschaft beschreibt das Ende einer Periode oder eines Zeitintervalls.|


#### 4.2.4 Klasse: dct:LicenceType
>| *URI der Klasse* | [`dct:LicenceType`](http://purl.org/dc/terms/LicenseDocument) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Ein rechtlich verbindliches Dokument, welches die Verwendung einer Ressource offiziell erlaubt. |
>| Weiterführende Dokumentationen | https://www.dublincore.org/specifications/dublin-core/dcmi-terms/2012-06-14/#terms-LicenseDocument |
>> **Beziehungen zu anderen Klassen innerhalb des Modells** 

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [dct:type](http://purl.org/dc/terms/type) | `skos:Concept` | `*` | Empfohlen |  	Diese Eigenschaft bezieht sich auf den Typ einer Lizenz. |


#### 4.2.5 Klasse: cr:FileObject
>| *URI der Klasse* | [`cr:FileObject`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#fileobject) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     |  	Die grundlegende Einheit innerhalb des Croissant Metadatendstandards, welche die einzelnen Daten innerhalb eines Datensets beschreibt. |
>| Weiterführende Dokumentationen | https://docs.mlcommons.org/croissant/docs/croissant-spec.html |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine Beschreibung für die einzelne Datei, die im dcat:Dataset enthalten ist. |
| [`sc:name `](https://schema.org/name) | `rdfs:Literal` | `1` | Verpflichtend | Diese Eigenschaft enthält den Namen der Datei. |
| [`sc:contentSize`](https://schema.org/contentSize) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft beschreibt die Dateigröße in (Mega/Kilo/...) Bytes. |
| [`sc:contentURL`](https://schema.org/contentUrl) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft beinhaltet den Link zur eigentlichen Datei eines Datensatzes. |
| [`sc:encodingFormat `](https://schema.org/encodingFormat) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft beinhaltet das Format zur Datei als Mime-Type. |
| [`sc:sameAs`](https://schema.org/sameAs) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft verweist auf eine URL (oder "local name") eines FileObjects mit demselben Inhalt, aber in einem anderen Format. |
| [`sc:sha256`](https://schema.org/sha256) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft verweist auf den Prüfwert für den Dateiinhalt. |
| [cr:containedIn](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#containedIn) | `cr:FileObject` | `0..*` | Optional | Diese Eigenschaft verweist auf ein anderes `FileObject` das diese Einheit beinhaltet.  |


#### 4.2.6 Klasse: dcat:Distribution
>| *URI der Klasse* | [`dcat:Distribution`](https://www.w3.org/ns/dcat#distribution) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Eine physische Verkörperung oder Repräsentanz des Datensatzes in einem spezifischen Format. |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-3/#Class:Distribution |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dcat:byteSize`](https://www.w3.org/ns/dcat#byteSize) | `rdfs:Literal` | `1` | Verpflichtend | Diese Eigenschaft enthält die Größe der Distribution in Bytes. |
| [`dcat:accessURL`](https://www.w3.org/ns/dcat#accessURL) | `rdfs:Resource` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine URL-Adresse, die Zugriff auf die Distribution eines Datensatzes ermöglicht. |
| [`dcatap:applicableLegislation`](https://semiceu.github.io/DCAT-AP/r5r/releases/3.0.0/#applicableLegislation) | `rdfs:Resource` | `1..*` | Verpflichtend | Diese Eigenschaft gibt die rechtlichen Grundlagen für die Distribution  an. |
| [`dct:format`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#format) | `dct:MediaType` | `1` | Verpflichtend | Diese Eigenschaft verweist auf das Datenformat der Distribution. |
| [`dct:rights`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#RightsStatement) | `dct:RightsStatement` | `1` | Verpflichtend | Diese Eigenschaft verweist auf eine juristische Darlegung, welche die mit der Distribution assoziierten Nutzungsbestimmungen spezifiziert. |
| [`dct:license`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#LicenseDocument) | `dct:LicenseDocument` | `0..1` | Empfohlen | Diese Eigenschaft bezieht sich auf die Lizenz, unter welcher die Distribution zur Verfügung gestellt wird. |
| [`dcat:compressFormat`](https://www.w3.org/ns/dcat#mediaType) | `dct:MediaType` | `0..1]` | Optional | Diese Eigenschaft bezieht sich auf das Dateiformat, in dem die Daten der Distribution in komprimierter Form, z.B. um die Größe zu reduzieren, zum Download angeboten werden. |
| [`dcat:downloadURL`](https://www.w3.org/ns/dcat#downloadURL) | `rdfs:Resource` | `*` | Optional | Diese Eigenschaft enthält eine URL-Adresse, welche einen direkten Zugriff/Link auf die herunterladbare Datei im beschriebenen Format liefert. |
| [`dcat:mediaType`](https://www.w3.org/ns/dcat#mediaType) | `dct:MediaType` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf den Medientyp der Distribution. |
| [`dcat:packageFormat`](https://www.w3.org/ns/dcat#mediaType) | `dct:MediaType` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf das Dateiformat, in dem die Daten der Distribution zusammengeschnürt zum Download angeboten werden. Zum Beispiel, um den Download zu erleichtern. |
| [`dct:conformsTo`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#conformsTo) | `dct:Standard` | `*` | Optional | Diese Eigenschaft beschreibt einen etablierten Standard, mit dem die Distribution übereinstimmt. |
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft enthält eine Freitextbeschreibung der Distribution. |
| [`dct:issued`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#issued) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft verweist auf das Veröffentlichungsdatum der Distribution.  |
| [`dct:language`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#language) | `dct:LinguisticSystem ` | `*` | Optional | Die Eigenschaft verweist auf die Sprache der Distribution. |
| [`dct:modified`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#modified) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft verweist auf die Angabe des Datums (Format: YYYY-MM-DD HH-MM-SS) an dem die Distribution zuletzt angepasst wurde.|
| [`dct:title`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft bezeichnet den einer Distribution zugewiesenen Titel.  |
| [`foaf:page`](http://xmlns.com/foaf/spec/) | `foaf:document` | `*` | Optional | Diese Eigenschaft verweist auf eine Seite oder ein Dokument über die Distribution.|
| [`odrl:hasPolicy`](http://www.w3.org/ns/odrl/2/hasPolicy) | `hasPolicy` | `0..1` | Optional | Diese Eigenschaft verweist auf ein Regelwerk, das die Rechte die mit dieser Distribution assoziiert werden unter Verwendung des ODRL Vokabulars beschreibt. |
| [dcat:accessService](http://www.w3.org/ns/dcat#accessService) | `dcat:DataService` | `*` | Optional | Diese Eigenschaft verweist auf den Datenservice, der Zugang zur Distribution ermöglicht. |
| [spdx:checksum](http://spdx.org/rdf/terms#checksum) | `spdx:Checksum` | `0..1` | Optional |  	Diese Eigenschaft  Mechanismusverweist auf einen Mechanismus, mit dem sichergestellt werden kann, dass die Inhalte der Distribution sich nicht verändert haben |
| [adms:status](http://www.w3.org/ns/adms#status) | `skos:Concept` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf den Status bzw. Reifegrad der Distribution. |
| [dcatap:availability](http://data.europa.eu/r5r/availability) | `skos:Concept` | `0..1` | Optional |  Verfügbarkeit der Distribution eines Datensatzes, als Auswahl aus einer festen Liste von Werten via DCAT-AP URIs. |


### 4.3 Optionale Klassen 
Im Rahmen des HealthDCAT-AP.de Modells sind die folgenden Klassen optional. Sie können somit verwendet werden und haben einen Mehrwert, jedoch ist ein Datensatz ohne diese Informationen ebenso verwendbar und innerhalb des Modells korrekt. 

[`dcat:DataService`](#531-klasse-dcatdataservice)

[`dct:Location`](#532-klasse-dctlocation)

[`adms:Identifier`](#534-klasse-admsidentifier)

[`spdx:Checksum`](#535-klasse-spdxchecksum)

[`dcat:CatalogRecord`](#536-klasse-dcatcatalogrecord)

[`dcat:Relationship`](#537-klasse-dcatrelationship) 

[`prov:Attribution`](#538-klasse-provattribution) 

[`skos:ConceptScheme`](#539-klasse-skosconceptscheme) 

#### 4.3.1 Klasse: dcat:DataService
>| *URI der Klasse* | [`dcat:DataService`](https://www.w3.org/ns/dcat#DataService) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Ein Datenservice ermöglicht den Zugang zu einem oder mehreren Datensätzen oder stellt Datenverarbeitungsverfahren zur Verfügung. |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-3/#Class:Data_Service |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dcat:endpointURL`](https://www.w3.org/ns/dcat#endpointURL) | `rdfs:Resource` | `1..*` | Verpflichtend | Die URL unter der API-Endpunkt eines Datenservices erreichbar ist. |
| [`dct:title`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title) | `rdfs:Literal`  | `1..*` | Verpflichtend | Diese Eigenschaft bezeichnet den einem Datenservice zugewiesenen Titel. |
| [`dcatap:applicableLegislation`](https://semiceu.github.io/DCAT-AP/r5r/releases/3.0.0/#applicableLegislation) | `rdfs:Resource` | `1..*` | Verpflichtend | Diese Eigenschaft gibt die rechtlichen Grundlagen für die im Datenservice enthaltenen Daten an. |
| [`dcat:contactPoint`]("https://www.w3.org/ns/dcat#contactPoint") | `vcard:Kind` | `*` | Empfohlen | Diese Eigenschaft umfasst Kontaktinformationen, welche für das Zusenden von Kommentaren zum jeweiligen Datensatzservice verwendet werden können. |
| [`dcat:endpointDescription`]("https://www.w3.org/ns/dcat#endpointDescription") | `rdfs:Resource` | `*` | Empfohlen | Die Beschreibung der Services, die unter den angebenen Endpunkten erreicht werden können. |
| [`dcat:keyword`]("https://www.w3.org/ns/dcat#keyword") | `rdfs:Literal` | `*` | Empfohlen | "Diese Eigenschaft enthält ein Schlagwort oder Schlüsselbegriff zur Beschreibung des Datenservices." |
| [`dcat:theme`](https://www.w3.org/ns/dcat#theme) | `dct:subject` | `*` | Empfohlen | Diese Eigenschaft bezieht sich auf die dem Datenservice zugewiesenen Kategorien. | <a name="eigenschaft-dcat-theme"></a>
| [`dct:conformsTo`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#conformsTo) | `dct:Standard` | `*` | Empfohlen | Diese Eigenschaft verweist auf ein etabliertes Schema, zu dem der Datenservice konform ist. |
| [dcat:servesDataset](http://www.w3.org/ns/dcat#servesdataset) | `dcat:Dataset` | `*` | Empfohlen |  Diese Eigenschaft verweist auf einen Datensatz, der vom Datenservice ausgeliefert werden kann. |
| [dct:publisher](http://purl.org/dc/terms/publisher) | `foaf:Agent` | `*` | Empfohlen |  	Diese Eigenschaft verweist auf die Stelle oder Person, die für Bereitstellung des Datenservices verantwortlich ist. |
| [dcatap:availability]((http://data.europa.eu/r5r/availability)) | `skos:Concept` | `0..1` | Empfohlen |  Diese Eigenschaft verweist auf eine geplante Verfügbarkeit des Datenservices als Auswahl aus einer festen Liste von Werten via DCAT-AP URIs. |
| [`dcat:landingPage`](https://www.w3.org/ns/dcat#landingPage) | `foaf:Document` | `*` | Optional |  	Diese Eigenschaft verweist auf eine Webseite, welche Zugriff auf den Datenservice und/oder weitere Informationen ermöglicht. |
| [`dct:accessRights`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#accessRights) | `dct:RightsStatement` | `0..1` | Optional |  Diese Eigenschaft verweist auf Informationen, die darlegen, ob der Datenservice öffentlich zugänglich ist, Zugriffseinschränkungen existieren oder er nicht-öffentlich ist. |
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft enthält eine Beschreibung des Datenservices als Freitext. |
| [`dct:format`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#format) | `dct:MediaType` | `*` | Optional | Die Datenformate, die beim Abruf der dcat:endpointURL zurückgegeben werden können. |
| [`dct:license`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#license) | `dct:LicenseDocument` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf die Lizenz, mit welcher der Datenservice verwendet oder wiederverwendet werden kann.|
| [`healthdcatapde:dataServiceType`]() | `skos:Concept` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf eine Option der Service Type Liste. |


#### 4.3.2 Klasse: dct:Location
>| *URI der Klasse* | [`dct:Location`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/terms/Location/) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Ein räumlicher Bereich oder ein bezeichneter Ort. Er kann durch ein kontrolliertes Vokabular oder mit geographischen Koordinaten repräsentiert werden. |
>| Weiterführende Dokumentationen | https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#Location |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dcat:bbox`](https://www.w3.org/ns/dcat#bbox) | `rdfs:Resource` | `0..1` | Empfohlen | Diese Eigenschaft beschreibt die Bounding Box eines Ortes, |
| [`dcat:centroid`](https://www.w3.org/ns/dcat#centroid) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft beschreibt den geografischen Mittelpunkt eines Ortes. |
| [`locn:geometry`](https://www.w3.org/ns/legacy_locn#geometry) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft beschreibt die Geometrie eines Ortes. |


#### 4.3.4 Klasse: adms:Identifier
>| *URI der Klasse* | [`adms:Identifier`](https://www.w3.org/ns/legacy_adms#Identifier) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Die Klasse "Identifier" besteht je nach spezifischen Kontext aus einem String, welcher - die ID ist,  - eine optionale ID für das ID-Schema ist, - eine optionale ID für die Version des ID-Schemas ist oder - eine optionale ID für die das ID-Schema pflegende verantwortliche Stelle ist. |
>| Weiterführende Dokumentationen | https://www.w3.org/ns/legacy_adms#Identifiern |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`skos:notation`](https://www.w3.org/2009/08/skos-reference/skos.html#notation) | `rdfs:Literal` | `1` | Verpflichtend | Diese Eigenschaft enthält einen datentypreferenzierten ID-String im Kontext des ID-Schemas. |


#### 4.3.5 Klasse: spdx:Checksum 
>| *URI der Klasse* | [`spdx:Checksum`](https://spdx.org/rdf/terms/#checksum) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Ein Wert, der es ermöglicht, die Inhalte einer Datei zu verifizieren (für korrekt zu erklären). Diese Klasse ermöglicht es, die Ergebnisse einer Vielzahl von Prüfsummen- und Kryptoalgorithmen zu repräsentieren. |
>| Weiterführende Dokumentationen | https://spdx.org/rdf/terms/#checksum |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`spdx:algorithm`](https://spdx.org/rdf/terms/#algorithm) | `rdfs:Resource` | `1` | Verpflichtend |  Diese Eigenschaft identifiziert den verwendeten Algorithmus zur Erzeugung der Prüfsumme.|
| [`spdx:checksumValue`](https://spdx.org/rdf/terms/#checksumValue) | `rdfs:Literal` | `1` | Verpflichtend | Diese Eigenschaft identifiziert die Prüfsumme als Ergebnis des verwendeten Algorithmus. |


#### 4.3.6 Klasse: dcat:CatalogRecord
>| *URI der Klasse* | [`dcat:CatalogRecord`](https://www.w3.org/ns/dcat#CatalogRecord) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Die Beschreibung des Eintrags in einem Katalog. |
>| Weiterführende Dokumentationen | https://www.dcat-ap.de/def/dcatde/3.0/spec/#klasse-katalogeintrag |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dct:modified`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#modified) | `rdfs:Literal` | `1` | Verpflichtend | Diese Eigenschaft erfasst das Datum der letzten Aktualisierung bzw. Modifikation des Katalogeintrags. |
| [foaf:primaryTopic](http://xmlns.com/foaf/spec/) | `dcat:Resource` | `1` | Verpflichtend | Diese Eigenschaft verknüpft den Katalogeintrag mit einer `dcat:Resource`. |
| [`dct:conformsTo`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#conformsTo) | `rdfs:Resource` | `0..1` | Empfohlen | Diese Eigenschaft bezieht sich auf das Application Profile zu dem die Metadaten im Katalog konform sind. |
| [`dct:issued`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#issued) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft enthält das Datum, an dem die Beschreibung der Ressource aufgenommen wurde. |
| [adms:status](http://www.w3.org/ns/adms#status) | `skos:Concept` | `0..1` | Empfohlen | Diese Eigenschaft bezieht sich auf den Typ der letzten Revision des Datensatzeintrags im Katalog. |
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft enthält eine Freitextbeschreibung des Katalogeintrags. |
| [`dct:language`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#language) | `dct:LinguisticSystem` | `*` | Optional | Diese Eigenschaft bezieht sich auf die Sprache der Metadatenbeschreibung für die zum Katalogeintrag gehörenden Eigenschaften (z.B. Titel, Beschreibungen usw.). |
| [`dct:title`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft bezeichnet den Titel eines Katalogeintrags. |
| [dct:source](http://purl.org/dc/terms/source) | `dcat:CatalogRecord` | `0..1` | Optional | Diese Eigenschaft verweist auf die ursprünglichen Metadaten, mit Hilfe derer die Metadaten des Katalogeintrags erstellt wurden. |


#### 4.3.7 Klasse: dcat:Relationship
>| *URI der Klasse* | [`dcat:Relationship`](http://www.w3.org/ns/dcat#Relationship) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Eine Klasse, um eine Beziehung zwischen mehreren DCAT Ressourcen genauer zu beschreiben. |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-2/#Class:Relationship |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dcat:hadRole`](https://www.w3.org/ns/dcat#hadRole) | `dcat:Role` | `1..*` | Verpflichtend | Diese Eigenschaft verweist auf die Funktion einer Ressource in Beziehung zu einer anderen Ressource. |
| [`dct:relation`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#relation) | `rdfs:Resource` | `1..*` | Verpflichtend | Diese Eigenschaft verweist auf die Ressourcen, die miteinander in einer Beziehung stehen. |


#### 4.3.8 Klasse: prov:Attribution
>| *URI der Klasse* | [`prov:Attribution`](http://www.w3.org/ns/prov#Attribution) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Diese Klasse verkn�ft eine Ressource mit Agenten und beschreibt, welche Rolle die Agenten im Bezug auf die Ressource eingenommen haben. Sie ist insbesondere dann relevant, wenn keine Eigenschaften wie `dcatde:originator`, `dct:creator` oder `dct:publisher` existieren, um die Rolle zu beschreiben. |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/prov-o/#Attribution |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dcat:hadRole`](https://www.w3.org/ns/dcat#hadRole) | `dcat:Role` | `1..*` | Verpflichtend | Beschreibt die Funktion, die Agenten in Bezug auf eine Ressource hatten. |
| [`prov:agent`](https://www.w3.org/ns/prov#agent) | `prov:Agent` | `1..*` | Verpflichtend | Die Eigenschaft referenziert auf einen prov:Agent, der eine Ressource beeinflusst hat.|


#### 4.3.9 Klasse: skos:ConceptScheme
>| *URI der Klasse* | [`skos:ConceptScheme`](http://www.w3.org/2004/02/skos/core#ConceptScheme) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Eine Sammlung von Konzepten/Begrifflichkeiten (z.B. in Form eines kontrollierten Vokabulars) durch welche die Kategorie definiert ist. |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-2/#Class:Concept_Scheme |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dct:title`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft bezeichnet den einer Sammlung zugewiesenen Titel. |


## 5. Kontrollierte Vokabulare
Im Rahmen von HealthDCAT-AP.de wurden mehrere kontrollierte Vokabulare berücksichtigt. Die folgende Auflistung beinhaltet alle inkludierten kontrollierten Vokabulare. Ebenfalls wird aufgeführt, mit welcher Verbindlichkeit das jeweilige Vokabular genutzt werden muss, sofern die entsprechende Eigenschaft verwendet wird. Die Verwendung dieser Wertelisten erhöht das bereits hohe Maß an Interoperabilität und Standisierung von HealthDCAT-AP.de erneut.
Für die Auswahl der hier verwendeten Wertelisten wurden ähnliche Anforderungen wie sie auch z.B. DCAT-AP.de verwendet berücksichtigt. Dazu gehöhrt unter Anderem dass die entsprechende Werteliste angemessen dokumentiert und von einer vertrauenswürdigen Orghanisation wie z.B. der Europäischen Union stammt. 


#### 5.1 EU Vokabular "Data theme"
>| *Betroffene Eigenschaft* | `dcat:theme` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Data theme" ist ein kontrolliertes Vokabular, das Konzepte auflistet, die für die Klassifizierung von Datensätzen verwendet werden.  |
>| Verbindlichkeit | Empfohlen |
>| Verwendung in KLassen | `dcat:DataService`  |
>| Basis URI | http://publications.europa.eu/resource/authority/data-theme |
>| Weiterführende Dokumentationen | https://op.europa.eu/de/web/eu-vocabularies/concept-scheme/-/resource?uri=http://publications.europa.eu/resource/authority/data-theme |

#### 5.2 Countries and territories
>| *Betroffene Eigenschaft* | `dcat:Location` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Countries" ist ein kontrolliertes Vokabular, welches verschiedene Länder und Territorien auflistet.  |
>| Verbindlichkeit | Verpflichtend |
>| Verwendung in KLassen | `dcat:DataService` |
>| Basis URI | http://publications.europa.eu/resource/authority/country/ |
>| Weiterführende Dokumentationen | https://op.europa.eu/de/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/country |

#### 5.3 Language
>| *Betroffene Eigenschaft* | `dct:language` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Language" ist ein kontrolliertes Vokabular, das Sprachen auflistet, unter anderem auch Zeichensprachen.  |
>| Verbindlichkeit | Optional |
>| Verwendung in KLassen | `dcat:DataSet`; `dcat:Distribution` |
>| Basis URI | http://publications.europa.eu/resource/dataset/language |
>| Weiterführende Dokumentationen | https://op.europa.eu/de/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/language |

#### 5.4 Purpose
>| *Betroffene Eigenschaft* | `dpv:hasPurpose` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Die Taxonomie "Purposes" des Data Privacy Vocabulary listet verschiedene Gründe für die Verwendung von Daten auf.  |
>| Verbindlichkeit | Empfohlen |
>| Verwendung in KLassen | `dcat:DataSet` |
>| Basis URI | https://w3c.github.io/dpv/2.0/dpv/#vocab-purposes |
>| Weiterführende Dokumentationen | https://w3c.github.io/dpv/2.0/dpv/modules/purposes.html |

#### 5.5 Access rights
>| *Betroffene Eigenschaft* | `dct:accessRights` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Access Rights" ist ein kontrolliertes Vokabular, das verschiedene Formen der Zugriffsrechte und -beschränkungen für einen Datensatz auflistet wie z.B. "Public" und "Non-Public".  |
>| Verbindlichkeit | Verbindlich für `dcat:DataSet` ; Optional für `dcat:DataService` |
>| Verwendung in KLassen | `dcat:DataSet` ; `dcat:DataService` |
>| Basis URI |  http://publications.europa.eu/resource/dataset/access-right |
>| Weiterführende Dokumentationen | https://op.europa.eu/de/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/access-right |

#### 5.6 File type
>| *Betroffene Eigenschaft* | `dct:format` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Access Rights" ist ein kontrolliertes Vokabular, das verschiedene Formen der Zugriffsrechte und -beschränkungen für einen Datensatz auflistet wie z.B. "Public" und "Non-Public".  |
>| Verbindlichkeit | Optional für `dcat:DataService` ; Verbindlich für `dcat:Distribution` |
>| Verwendung in KLassen | `dcat:DataService` ; `dcat:Distribution` |
>| Basis URI |  http://publications.europa.eu/resource/dataset/file-type |
>| Weiterführende Dokumentationen | https://op.europa.eu/de/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/file-type |

#### 5.7 Data service type
>| *Betroffene Eigenschaft* | `healthdcatapde:dataServiceType` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Data service type" ist ein kontrolliertes Vokabular, das verschiedene Formen wie auf einen Datensatz zugegriffen werden kann wie z.B. mithilfe einer API oder eines SPARQL Endpoint umfasst.  |
>| Verbindlichkeit | Optional |
>| Verwendung in KLassen | `dcat:DataService` |
>| Basis URI |  http://publications.europa.eu/resource/authority/data-service-type |
>| Weiterführende Dokumentationen | https://op.europa.eu/en/web/eu-vocabularies/concept-scheme/-/resource?uri=http://publications.europa.eu/resource/authority/data-service-type |

#### 5.8 Planned availability 
>| *Betroffene Eigenschaft* | `dcatap:availability` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Planned availability" ist ein kontrolliertes Vokabular, das verschiedene Formen der Verfügbarkeit eines Datensatzes beschreibt.  |
>| Verbindlichkeit | Empfohlen für `dcat:DataService` ; Optional für `dcat:Distribution` |
>| Verwendung in KLassen | `dcat:DataService` ; `dcat:Distribution` |
>| Basis URI |      http://publications.europa.eu/resource/dataset/planned-availability |
>| Weiterführende Dokumentationen | https://op.europa.eu/de/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/planned-availability |

#### 5.9 Target Audience 
>| *Betroffene Eigenschaft* | `healthdcatapde:targetAudience` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Data service type" ist ein kontrolliertes Vokabular, das die verschiedenen möglichen Zielgruppen eines Datensatzes beschreibt wie z.B. Forschende.  |
>| Verbindlichkeit | Optional |
>| Verwendung in KLassen | `dcat:DataSet` |
>| Basis URI | http://publications.europa.eu/resource/dataset/target-audience |
>| Weiterführende Dokumentationen | https://op.europa.eu/de/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/target-audience |

#### 5.10 Dataset type
>| *Betroffene Eigenschaft* | `dct:type` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Dataset type" ist ein kontrolliertes Vokabular, das Begriffe zur Einordnung des Datensatzes umfasst wie z.B. ob es ein Glossar, Geodaten etc. sind.  |
>| Verbindlichkeit | Verbindlich |
>| Verwendung in KLassen | `dcat:DataSet` |
>| Basis URI | http://publications.europa.eu/resource/authority/dataset-type |
>| Weiterführende Dokumentationen | https://op.europa.eu/de/web/eu-vocabularies/concept-scheme/-/resource?uri=http://publications.europa.eu/resource/authority/dataset-type |

#### 5.11 Distribution status 
>| *Betroffene Eigenschaft* | `adms:status` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Das Vokabular "Distribution status" ist ein kontrolliertes Vokabular, das Begrifflichkeiten zur Einordnung des Status des Datensatzes beinhaltet wie z.B. ob er veraltet oder noch im Aufbau ist.  |
>| Verbindlichkeit | Optional |
>| Verwendung in KLassen | `dcat:Distribution` |
>| Basis URI | http://publications.europa.eu/resource/dataset/distribution-status |
>| Weiterführende Dokumentationen | https://op.europa.eu/de/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/distribution-status|

#### 5.12 Personal Data 
>| *Betroffene Eigenschaft* | `dpv:hasPersonalData` |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Die Erweiterung "Personal Data" des Data Privacy Vocabulary beinhaltet eine verschiedene Kategorien um persönliche Daten innerhalb eines Datensatzes einzuordnen, wie z.B. Staatsbürgerschaft oder Blutgruppe. |
>| Verbindlichkeit | Verbindlich |
>| Verwendung in KLassen | `dcat:DataSet` |
>| Basis URI | -- |
>| Weiterführende Dokumentationen | https://w3c.github.io/dpv/2.0/pd/ |


## 6. Glossar
>| *Begriff*  | *Definition/ Erklärung* |
>|:-----------------|:----------------------------------------------------|
>| ADMS | [Asset Description Metadata Schema](http://www.w3.org/ns/adms#) |
>| Datenportal | Web-basiertes System, welches einen Datenkatalog beinhaltet |
>| Datensatz (Dataset) | Sinnvolle Sammlung von zusammenhängenden Daten, die von einer einzelnen Quelle veröffentlicht oder kuratiert wird und in einem oder mehreren Formaten erreichbar ist oder als Download zur Verfügung steht |
>| DCAT | W3C Data Catalog, ein RDF-Vokabular |
>| DCAT-AP | ISA² Data Catalogue Application Profile des W3C Data Catalog DCAT |
>| DCAT-AP.de | Deutsche Adaption des „ISA² Data Catalogue Application Profile“ |
>| DCT | [DCMI Metadata Terms](https://purl.org/dc/terms/) |
>| Distribution | Logisches Konzept von Metadaten zu einer Ressource die physisch/real erreichbar ist bzw. als Download zur Verfügung steht |
>| Dublin Core | Metadatenvokabular zur Beschreibung von Dokumenten und anderen Objekten im Internet |
>| EU | Europäische Union |
>| FOAF | [Friends of a Friend Vocabulary](http://xmlns.com/foaf/spec/) |
>| Interoperabilität | Fähigkeit zur Zusammenarbeit von verschiedenen Systemen, Techniken oder Organisationen. |
>| Literal | Eine Zeichenfolge, die zur direkten Darstellung der Werte von Basistypen (z. B. Ganzzahlen, Gleitkommazahlen, Datumsangaben, Zeichenketten) definiert bzw. zulässig ist. |
>| Metadaten | Daten, die Informationen über Merkmale anderer Daten enthalten, aber nicht diese Daten selbst sind. |
>| RDF | [Resource Description Framework](https://www.w3.org/RDF/) |
>| RDF/XML | Notation von RDF in XML |
>| RDFS | [RDF Schema](https://www.w3.org/TR/rdf-schema/) |
>| SKOS | [Simple Knowledge Organization System](https://www.w3.org/2009/08/skos-reference/skos.html) |
>| SPDX | [Software Package Data Exchange](https://spdx.org/rdf/terms/) |
>| UML | Unified Modeling Language (vereinheitlichte Modellierungssprache) |
>| URI | Uniform Ressource Identifier, besteht aus einer Zeichenfolge, die zur Identifizierung einer abstrakten oder physischen Ressource dient. |
>| URL | Uniform Ressource Locator |
>| W3C | World Wide Web Consortium |


## 7. Changelog
V0.5 auf V0.6:
Anpassungen in der Einleitung
Austausch Begriff "Standard" mit Spezifikation




