# HealthDCAT-AP.de Spezifikation Entwurf
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

Hintergrund ist die Erforschung des Post-COVID-Syndroms, also Beschwerden, die mindestens zwölf Wochen oder länger nach der akuten COVID-Infektion vorliegen. Dies ist von hoher gesellschaftlicher Relevanz. Analog zu ME/CFS (Myalgische Enzephalomyelitis/Chronisches Fatigue-Syndrom) ist die Forschung durch heterogene und zugleich oft diffuse Symptome erschwert. Das Fehlen gepflegter Datensätze und insbesondere gepflegter Metadatensätze, die eine Verknüpfung zwischen den einzelnen Datensätzen und somit auch Verknüpfungen zwischen Risikofaktoren und Symptomen erlauben, stellte bisher ein weiteres Hindernis für die Auswertung der Daten dar. Da die Daten aus verschiedenen medizinischen Fachbereichen und weiteren Quellen kommen, unterstützt der Semantic-Web-Ansatz dieses Datenkatalog-Standards insbesondere die Nutzung der FAIR-Prinzipien (Findable, Accessible, Interoperable, Re-usable).

Als international zu bewertende Fragestellung müssen Konzepte zur Adressierung der oben beschriebenen Problemlage ebenso international gedacht werden. Für den europäischen Datenraum sind mit dem European (Health) Data Space (EHDS), dem Data Act, dem AI-Act sowie dem Interoperable Europe Act wichtige gesetzliche Grundlagen für die (semantische) Interoperabilität gelegt worden.

Zwar existieren bereits sektorspezifische Datenformate und -konzepte wie HL7 FHIR, Thesauri, Taxonomien, Ontologien, Applikationsprofile und auch vereinzelt Wissensgraphen; ein auf den Gesundheitssektor angepasster Datenkatalog-Standard, der die für einen übergreifenden Datenraum benötigten Funktionen unterstützt, ist jedoch bisher noch nicht vorhanden gewesen.

Im Rahmen des Vorhabens HealthDCAT-AP.de wurde aufgrund dessen dieser Standard mit dem Ansatz des Semantic Web erarbeitet. Das Vorhaben HealthDCAT-AP.de berücksichtigt dabei das Pilotprojekt HealthData@EU und das dort entwickelte Datenmodell HealthDCAT-AP. Dieses wird mittelfristig mithilfe von Instanzdaten zu einem Wissensgraphen weiterentwickelt. 

HealthDCAT-AP.de wurde mithilfe einer Kooperation der ]init[ AG und des WIG2-Instituts entwickelt. 

## Inhaltsverzeichnis

## 1. Einleitung

## 2. Kontext
#### 2.1 PostCovid Challenge
Das in dieser Spezifikation beschriebene Datenmodell wurde im Rahmen der PostCovid-Challenge entwickelt, die vom Bundesministerium des Innern und für Heimat (BMI) initiiert wurde. Ziel der Challenge war die Erstellung eines sektorübergreifenden, offenen und frei verfügbaren Datenmodells zur Unterstützung der Post-COVID-Forschung. Dieses Modell soll dazu beitragen, die gesellschaftlich hochrelevante Krankheit besser zu verstehen, insbesondere durch die Verknüpfung und Bereitstellung bislang fehlender Daten. Die Ergebnisse sollen langfristig aktuelle und kontextreiche Informationen für die Forschung liefern.
Das hier vorgestellte HealthDCAT-AP.de Modell ist ein Resultat dieser Challenge.


#### 2.2 Init AG
Die ]init[ AG für digitale Kommunikation zählt zu den Marktführern für innovative Lösungen in den Bereichen E-Government, E-Democracy und E-Business. Über 1.400 Mitarbeiter:innen an den Standorten Berlin, Mainz, München, Köln, Hamburg und Leipzig konzipieren und realisieren unter dem Motto "Services for the eSociety" auf Basis moderner Informations- und Kommunikationstechnologien maßgeschneiderte Lösungen für nationale wie internationale Regierungen und
Verwaltungen, NGOs sowie weitere gesellschaftliche Akteure. Als Vision hat sich ]init[ zum Ziel gesetzt, den gesellschaftlichen Akteuren und Organisationen eine Führungsrolle in der modernen Gesellschaft zu ermöglichen. Dabei gestaltet ]init[ durch innovative Lösungen den Veränderungsprozess von Organisationen und steigert so ihre Wertschöpfung nachhaltig. ]init[ versteht sich dabei als Innovator auf Basis ausgewiesener fachlicher und technologischer Expertise, vielfältigen Referenzen sowie der individuellen Kompetenzen unserer Mitarbeiter:innen.

#### 2.3 WIG2 Institut
Das WIG2 Institut ist eine unabhängige und neutrale Forschungseinrichtung, die evidenzbasierte Antworten auf komplexe Fragestellungen im Gesundheitswesen liefert.
Seit der Gründung des WIG2 Instituts im Jahr 2014 begleitet es aktiv gesundheitspolitische Themen und systemische Fragestellungen wie die Evaluation integrierter, innovativer Versorgungsmodelle oder die Entwicklung des Morbi-RSA als Kerninstrument des deutschen Gesundheitssystems. Darüber hinaus nimmt es das Gesundheitswesen über verschiedene Schwerpunktthemen in den Blick. Diese Schwerpunktthemen beinhalten unter anderem Gesundheitspolitisches Handeln sowie Regionale Versorgungsstrukturen. 


## 3. Zugrundeliegende Spezifikationen
In diesem Abschnitt werden die HealthDCAT-AP.de zugrundeliegenden Datenmodelle und -spezifikationen beschrieben.

#### 3.1 Dublin Core
Dublin Core ist ein grundlegender Metadatenstandard, der entwickelt wurde, um digitale Ressourcen und deren Metadaten zu beschreiben. Der Standard besteht aus 15 Kernelementen, die eine einfache, aber flexible Struktur für die Dokumentation von Informationen bieten, einschließlich Titel, Autor, Datum und Beschreibung. Dublin Core ist weit verbreitet und wird vor allem in digitalen Bibliotheken, Archiven, wissenschaftlichen Publikationen und auf Webseiten verwendet, um Ressourcen auffindbar und zugänglich zu machen. Die Elemente von Dublin Core sind sowohl für einfache Anwendungen als auch für komplexere, semantische Anforderungen anpassbar. Als universelles Basisvokabular bietet Dublin Core eine Grundlage, auf der viele spezifische Profile und Erweiterungen aufbauen, um den unterschiedlichen Anforderungen und Kontexten gerecht zu werden.

#### 3.2 DCAT
DCAT ist ein grundlegendes Vokabular, das von der W3C entwickelt wurde, um Datenkataloge, Datensätze und deren Verfügbarkeiten (Distributions) in einem maschinenlesbaren Format zu standardisieren. Es bildet eine wichtige Grundlage für die Interoperabilität und das Linked Data-Prinzip in offenen Datenportalen. DCAT definiert zentrale Entitäten wie Catalog, Dataset, Distribution und DataService sowie deren Eigenschaften.
Ziel von DCAT ist es, Datensätze auffindbar, zugänglich und interoperabel zu machen, unabhängig von der Plattform. Als Basisvokabular bietet DCAT die strukturellen Elemente, auf denen spezifische Profile, wie DCAT-AP, aufbauen können.

#### 3.3 DCAT-AP
DCAT-AP ist ein auf DCAT aufbauendes Anwendungsprofil, das von der Europäischen Kommission im Rahmen der ISA²-Initiative entwickelt wurde. Es erweitert DCAT um spezifische Anforderungen und kontrollierte Vokabulare, die den Austausch von Metadaten zwischen europäischen Datenportalen erleichtern.
Zusätzlich definiert es verbindliche und optionale Eigenschaften, wie publisher, license und theme, um eine höhere Standardisierung und Auffindbarkeit zu gewährleisten. DCAT-AP ermöglicht es, Metadaten in einem einheitlichen Format bereitzustellen und durch den Einsatz von Linked Data-Technologien maschinenlesbar zu machen. Es ist speziell auf den europäischen Kontext zugeschnitten und dient als Grundlage für nationale und sektorspezifische Erweiterungen, wie DCAT-AP.de.

#### 3.4 DCAT-AP.de
DCAT-AP.de ist die deutsche Anpassung des europäischen DCAT-AP-Standards. Es wurde entwickelt, um die Interoperabilität und Standardisierung offener Verwaltungsdaten in Deutschland sicherzustellen. DCAT-AP.de berücksichtigt die spezifischen Anforderungen deutscher Datenportale und Behörden sowie nationale rechtliche Rahmenbedingungen.
Es erweitert DCAT-AP um zusätzliche kontrollierte Vokabulare und Attribute, die für den deutschen Kontext relevant sind, z. B. spezifische Lizenzangaben und Sprachinformationen. DCAT-AP.de wird von deutschen Behörden und Open-Data-Plattformen verwendet, um den Austausch und die Wiederverwendbarkeit von Verwaltungsdaten zu optimieren. Zugleich bleibt es dabei vollständig kompatibel mit DCAT-AP und dem zugrunde liegenden W3C-DCAT-Standard.

#### 3.5 HealthDCAT-AP
HealthDCAT-AP ist ein spezialisiertes Anwendungsprofil des DCAT-AP, das entwickelt wurde, um Metadaten für Gesundheitsdatensätze im Rahmen des Europäischen Gesundheitsdatenraums (EHDS) zu standardisieren. Es erweitert DCAT-AP um spezifische Klassen und Eigenschaften, die den einzigartigen Anforderungen von Gesundheitsdaten gerecht werden, einschließlich Datenschutz und Sicherheit. Durch die Anpassung an die EHDS-Verordnung fördert HealthDCAT-AP die Interoperabilität und erleichtert den grenzüberschreitenden Austausch von Gesundheitsdaten innerhalb der EU. Es baut auf den Prinzipien von DCAT und DCAT-AP auf und integriert zusätzliche Mechanismen, um die Auffindbarkeit und Zugänglichkeit von elektronischen Gesundheitsdaten zu verbessern.

#### 3.6 Croissant
Die auf dem schema.org-Vokabular aufbauende Croissant-Spezifikation liegt seit März 2024 in Version 1.0 vor. Herausgeber ist das MLCommons-Konsortium. Es wurde entwickelt, um die Nutzung von Datensätzen in maschinellen Lernmodellen zu vereinfachen. Sie bietet ein Vokabular für Datensatzattribute und standardisiert die Art und Weise, wie Daten in verschiedenen maschinellen Lern-Frameworks wie PyTorch, TensorFlow oder JAX geladen werden. Durch die Vereinheitlichung der Beschreibung und Semantik von ML-Datensätzen erleichtert die Croissant-Spezifikation Forschern und Praktikern das Erkunden, Verstehen und Nutzen einer breiten Palette von Datensätzen. Sie baut auf bestehenden Standards auf und zielt darauf ab, die Interoperabilität und Wiederverwendbarkeit von Daten im Bereich des maschinellen Lernens zu verbessern

#### 3.7 Data Privacy Vocabulary
Das Data Privacy Vocabulary (DPV) ist ein standardisiertes Vokabular der W3C, das Datenschutzinformationen maschinenlesbar beschreibt und standardisiert. Es dient der Interoperabilität und dem Verständnis von Datenschutzanforderungen in verschiedenen Systemen. DPV definiert zentrale Entitäten wie z.B. DataSubject, DataController, Processing, Purpose und DataRecipient sowie deren Eigenschaften.
Ziel des DPV ist es, Datenschutzaspekte transparent zu dokumentieren und die Einhaltung von Vorschriften wie der DSGVO zu unterstützen. Als flexibles Vokabular bildet es die Grundlage für spezifische Datenschutzprofile und Erweiterungen, die unterschiedliche rechtliche Anforderungen und Implementierungen abbilden.

#### 3.8 Data Quality Vocabulary
Das Data Quality Vocabulary (DQV) ist ein standardisiertes Vokabular der W3C, das dazu dient, die Qualität von Daten in einem maschinenlesbaren Format zu beschreiben. Es definiert zentrale Entitäten wie z.B. DataQualityMetric, DataQualityDimension, DataQualityAssessment und DataQualityRequirement sowie deren Eigenschaften.
Ziel des DQV ist es, die Qualität von Daten systematisch zu erfassen und zu kommunizieren, um eine bessere Nutzung und Entscheidungsfindung zu ermöglichen. Als flexibles Vokabular bildet es die Basis für die Entwicklung spezifischer Qualitätsprofile und Standards, die in verschiedenen Kontexten und für unterschiedliche Anwendungsfälle genutzt werden können.

## 4. Überblick über HealthDCAT-AP.de 

## 5. Terminologie und Definitionen

### 5.1. Verpflichtende Klassen 

#### 5.1.1 Klasse: dcat:Resource 


#### 5.1.2 Klasse: dcat:Catalog
> | *URI der Klasse* | [`dcat:Catalog`](http://www.w3.org/ns/dcat#Catalog) |
> |:-----------------|:----------------------------------------------------|
> | Beschreibung     | Eine Sammlung oder Quelle, welche die beschriebenen Datensätze, Datenservices oder Kataloge zur Verfügung stellt. |
> |  eingebunden über | - |
> | Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-3/#Class:Catalog |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dcatap:applicableLegislation`](https://semiceu.github.io/DCAT-AP/r5r/releases/3.0.0/#applicableLegislation) | `rdfs:Resource` | `1..*` | Verpflichtend | Diese Eigenschaft gibt die rechtlichen Grundlagen für die im Katalog enthaltenen Daten an. |
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine Beschreibung des Kataloges als Freitext. |
| [`dct:title`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft bezeichnet den einem Katalog zugewiesenen Titel. |
| [`dct:issued`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#issued) | `rdfs:Literal` | `0..1` | Empfohlen |  Diese Eigenschaft enthält das Datum der Herausgabe/Emission (z.B. in Form einer Veröffentlichung) des Kataloges. |
| [`dct:language`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#language) | `dct:LinguisticSystem` | `*` | Empfohlen |  Diese Eigenschaft bezieht sich auf die Sprache, die in den textuellen Beschreibungen der dem Katalog zugehörigen Ressourcen Verwendung findet (z.B. Titel, Beschreibungen usw.). |
| [`dct:license`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#LicenseDocument) | `dct:LicenseDocument` | `0..1` | Empfohlen |  Diese Eigenschaft bezieht sich auf die Lizenz, mit welcher der Katalog verwendet oder wiederverwendet werden kann. |
| [`dct:modified`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#modified) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft erfasst das Datum der letzten Aktualisierung bzw. Modifikation des Kataloges. |
| [`foaf:homepage`](http://xmlns.com/foaf/spec/#term_homepage) | `foaf:Document` | `0..1` | Empfohlen | Diese Eigenschaft verweist auf eine Homepage, welche die zentrale Homepage des Kataloges ist. |
| [`dct:rights`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#RightsStatement) | `dct:RightsStatement` | `0..1` | Optional | Diese Eigenschaft verweist auf eine juristische Darlegung, welche die mit dem Katalog assoziierten Nutzungsbestimmungen spezifiziert. |

#### 5.1.3 Klasse: dcat:Dataset
>| *URI der Klasse* | [`dcat:Dataset`](http://www.w3.org/ns/dcat#Dataset) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     |  	Eine logische Entität, welche die veröffentlichten Informationen repräsentiert. |
>| eingebunden über | - |
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
| [`healthdcatap:maxTypicalAge`](https://healthdcat-ap.github.io/#healthdcatapmaxTypicalAge) | `xsd:nonNegativeInteger` | `0..1` | Empfohlen | Diese Eigenschaft gibt das maximale Alter an, das im Datensatz enthalten ist. |
| [`healthdcatap:minTypicalAge`](https://healthdcat-ap.github.io/#healthdcatapminTypicalAge) | `xsd:nonNegativeInteger` | `0..1` | Empfohlen | Diese Eigenschaft gibt den Minimalwert des Alters an, das im Datensatz enthalten ist. |
| [`dcat:contactPoint`](https://www.w3.org/ns/dcat#contactPoint) | `vcard:Kind` | `*` | Empfohlen | Diese Eigenschaft gibt relevante Kontaktinformationen für den Datensatz an.|
| [`dcat:keyword`](https://www.w3.org/ns/dcat#keyword) | `rdfs:Literal` | `*` | Empfohlen | Diese Eigenschaft enthält Schlagwörter oder Tags, die den Datensatz beschreiben. |
| [`dpv:hasLegalBasis`](https://w3c.github.io/dpv/2.0/dpv/#hasLegalBasis) | `rdfs:Resource` | `*` | Empfohlen | Diese Eigenschaft gibt die rechtliche Grundlage an, auf der die Verarbeitung personenbezogener Daten basiert. |
| [`dpv:hasPurpose`](https://w3c.github.io/dpv/2.0/dpv/#hasPurpose) | `rdfs:Resource` | `*` | Empfohlen | Diese Eigenschaft gibt den Zweck der Verarbeitung personenbezogener Daten an. |
| [`dqv:hasQualityAnnotation`](https://www.w3.org/TR/vocab-dqv/#dqv:hasQualityAnnotation) | `dqv:QualityAnnotaion` | `*` | Empfohlen | Diese Eigenschaft verbindet einen Datensatz mit einer anderen Ressource (z. B. einem Dokument), welches die Qualität des Datensatzes beschreibt. |
| [`healthdcatap:publisherNote`](https://healthdcat-ap.github.io/#healthdcatappublishernote) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft enthält eine Kurzbeschreibung des Herausgebers des Datensatzes und seiner Aktivitäten. |
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

#### 5.1.4 Klasse: cr:FileObject
>| *URI der Klasse* | [`cr:FileObject`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#fileobject) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     |  	Die grundlegende Einheit innerhalb des Croissant Metadatendstandards, welche die einzelnen Daten innerhalb eines Datensets beschreibt. |
>| eingebunden über | PLATZHALTER |
>| Weiterführende Dokumentationen | https://docs.mlcommons.org/croissant/docs/croissant-spec.html |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine Beschreibung für die einzelne Datei, die im dcat:Dataset enthalten ist. |
| [`sc:name `](https://schema.org/name) | `rdfs:Literal` | `1` | Verpflichtend | Diese Eigenschaft enthält den Namen der Datei. |
| [`sc:contentSize `](https://schema.org/contentSize) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft beschreibt die Dateigröße in (Mega/Kilo/...) Bytes. |
| [`sc:contentURL `](https://schema.org/contentUrl) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft beinhaltet den Link zur eigentlichen Datei eines Datensatzes. |
| [`sc:encodingFormat `](https://schema.org/encodingFormat) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft beinhaltet das Format zur Datei als Mime-Type. |
| [`sc:sameAs `](https://schema.org/sameAs) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft verweist auf eine URL (oder "local name") eines FileObjects mit demselben Inhalt, aber in einem anderen Format. |
| [`sc:sha256 `](https://schema.org/sha256) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft verweist auf den Prüfwert für den Dateiinhalt. |

#### 5.1.5 Klasse: dcat:Distribution
>| *URI der Klasse* | [`dcat:Distribution`](https://www.w3.org/ns/dcat#distribution) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Eine physische Verkörperung oder Repräsentanz des Datensatzes in einem spezifischen Format. |
>| eingebunden über | - |
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
| [`dcat:downloadURL](https://www.w3.org/ns/dcat#downloadURL) | `rdfs:Resource` | `*` | Optional | Diese Eigenschaft enthält eine URL-Adresse, welche einen direkten Zugriff/Link auf die herunterladbare Datei im beschriebenen Format liefert. |
| [`dcat:mediaType`](https://www.w3.org/ns/dcat#mediaType) | `dct:MediaType` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf den Medientyp der Distribution. |
| [`dcat:packageFormat`](https://www.w3.org/ns/dcat#mediaType) | `dct:MediaType` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf das Dateiformat, in dem die Daten der Distribution zusammengeschnürt zum Download angeboten werden. Zum Beispiel, um den Download zu erleichtern. |
| [`dct:conformsTo](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#conformsTo) | `dct:Standard` | `*` | Optional | Diese Eigenschaft beschreibt einen etablierten Standard, mit dem die Distribution übereinstimmt. |
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft enthält eine Freitextbeschreibung der Distribution. |
| [`dct:issued`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#issued) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft verweist auf das Veröffentlichungsdatum der Distribution.  |
| [`dct:language`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#language) | `dct:LinguisticSystem ` | `*` | Optional | Die Eigenschaft verweist auf die Sprache der Distribution. |
| [`dct:modified`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#modified) | `rdfs:Literal` | `0..1` | Optional | Diese Eigenschaft verweist auf die Angabe des Datums (Format: YYYY-MM-DD HH-MM-SS) an dem die Distribution zuletzt angepasst wurde.|
| [`dct:title`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft bezeichnet den einer Distribution zugewiesenen Titel.  |
| [`foaf:page`](http://xmlns.com/foaf/spec/) | `foaf:document` | `*` | Optional | Diese Eigenschaft verweist auf eine Seite oder ein Dokument über die Distribution.|
| [`odrl:hasPolicy`](http://www.w3.org/ns/odrl/2/hasPolicy) | `hasPolicy` | `0..1` | Optional | Diese Eigenschaft verweist auf ein Regelwerk, das die Rechte die mit dieser Distribution assoziiert werden unter Verwendung des ODRL Vokabulars beschreibt. |

#### 5.1.6 Klasse: foaf:Agent
>| *URI der Klasse* | [`foaf:Agent`](http://xmlns.com/foaf/spec/#term_Agent) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     |  	Eine Stelle, Person oder Organisation. |
>| eingebunden über | - |
>| Weiterführende Dokumentationen | http://xmlns.com/foaf/spec/#term_Agent |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [foaf:name]("http://xmlns.com/foaf/spec/#term_name") | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft beschreibt den Namen der Stelle, Person oder Organisation. |

#### 5.1.7 Klasse: skos:Concept 
>| *URI der Klasse* | [`skos:Concept`](https://www.w3.org/TR/skos-reference/#concepts) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | - |
>| eingebunden über | - |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/skos-reference/#concepts |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [skos:prefLabel](https://www.w3.org/TR/skos-reference/#labels) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft verweist auf den Titel des Konzepts. |


### 5.2 Empfohlene Klassen 

#### 5.2.1 Klasse: cr:RecordSet
>| *URI der Klasse* | [`cr:RecordSet`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#recordset) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     |  	Eine Menge von strukturierten Datensätzen aus einer oder mehreren Datenquellen. |
>| eingebunden über | - |
>| Weiterführende Dokumentationen | https://docs.mlcommons.org/croissant/docs/croissant-spec.html |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine Beschreibung für die einzelne Datei, die im RecordSet enthalten ist. |
| [`cr:key`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#key) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft beschreibt ein oder mehrere Felder, deren Werte jeden Datensatz im RecordSet eindeutig identifizieren |
| [`cr:data`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#data) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft beschreibt einen oder mehrere Datensätze, die die Daten des RecordSet bilden. |
| [`sc:examples`]() | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft verweist auf einen oder mehrere Datensätze, die als Beispielinhalt des RecordSet bereitgestellt werden, oder ein Verweis auf eine Datenquelle, die Beispiele enthält. |

#### 5.2.2 Klasse cr:Field
>| *URI der Klasse* | [`cr:Field`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#field) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     |  	Ein Feld innerhalb eines Datensatzes. Es kann aber auch die Spalte in Tabelle oder innerhalb einer verschachtelte Datenstruktur darstellen. |
>| eingebunden über | - |
>| Weiterführende Dokumentationen | https://docs.mlcommons.org/croissant/docs/croissant-spec.html |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [`cr:dataType`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#datatype) | `rdfs:Literal` | `1..*]` | Verpflichtend | Diese Eigenschaft verweist auf den Datentyp des Feldes, identifiziert durch den URI der entsprechenden Klasse. Es kann entweder ein atomarer Typ oder ein semantischer Typ sein. |
| [`cr:source`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#source) | `rdfs:Literal` | `1..*]` | Verpflichtend | Diese Eigenschaft verweist auf eine Datenquelle für ein cr:Field. |
| [`dct:description`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `1..*` | Verpflichtend | Diese Eigenschaft enthält eine Beschreibung für die einzelne Datei, die in cr:Field enthalten ist. |
| [`cr:references`](https://docs.mlcommons.org/croissant/docs/croissant-spec.html#references) | `rdfs:Literal` | `*` | Empfohlen | Diese Eigenschaft verweist auf andere cr:Field Elemente in einem anderen cr:RecordSet. |

#### 5.2.3 Klasse: dct:PeriodOfTime 
>| *URI der Klasse* | [`dct:PeriodOfTime`](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#PeriodOfTime) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Ein Zeitintervall, welches durch Start- und Endzeitpunkt bezeichnet bzw. definiert ist. |
>| eingebunden über | - |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-3/#Class:Period_of_Time |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [dcat:endDate](https://www.w3.org/ns/dcat#endDate) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft beschreibt das Ende eines Zeitintervalls. |
| [dcat:startDate](https://www.w3.org/ns/dcat#startDate) | `rdfs:Literal` | `0..1` | Empfohlen | Diese Eigenschaft beschreibt den Start eines Zeitintervalls. |
| [time:hasBeginning](https://www.w3.org/TR/owl-time/#time:hasBeginning) | `time:Instant` | `0..1` | Optional | Diese Eigenschaft beschreibt den Anfang einer Periode oder eines Zeitintervalls. |
| [time:hasEnd](https://www.w3.org/TR/owl-time/#time:hasEnd) | `time:Instant` | `0..1` | Optional | Diese Eigenschaft beschreibt das Ende einer Periode oder eines Zeitintervalls.|

#### 5.2.4 Klasse: dct:LicenceType


### 5.3 Optionale Klassen 

#### 5.3.1 Klasse: dcat:DataService
>| *URI der Klasse* | [`dcat:DataService`](https://www.w3.org/ns/dcat#DataService) |
>|:-----------------|:----------------------------------------------------|
>| Beschreibung     | Ein Datenservice ermöglicht den Zugang zu einem oder mehreren Datensätzen oder stellt Datenverarbeitungsverfahren zur Verfügung. |
>| eingebunden über | - |
>| Weiterführende Dokumentationen | https://www.w3.org/TR/vocab-dcat-3/#Class:Data_Service |

| **Attribut** | **Wertebereich** | **Kardinalität** | **Verbindlichkeit** | **Beschreibung** |
|--------------|---------|-----------------|--------------------|------------------|
| [dcat:endpointURL](https://www.w3.org/ns/dcat#endpointURL) | `rdfs:Resource` | `1..*` | Verpflichtend | Die URL unter der API-Endpunkt eines Datenservices erreichbar ist. |
| [dct:title](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title) | `rdfs:Literal`  | `1..*` | Verpflichtend | Diese Eigenschaft bezeichnet den einem Datenservice zugewiesenen Titel. |
| [`dcatap:applicableLegislation`](https://semiceu.github.io/DCAT-AP/r5r/releases/3.0.0/#applicableLegislation) | `rdfs:Resource` | `1..*` | Verpflichtend | Diese Eigenschaft gibt die rechtlichen Grundlagen für die im Datenservice enthaltenen Daten an. |
| [dcat:contactPoint]("https://www.w3.org/ns/dcat#contactPoint") | `vcard:Kind` | `*` | Empfohlen | Diese Eigenschaft umfasst Kontaktinformationen, welche für das Zusenden von Kommentaren zum jeweiligen Datensatzservice verwendet werden können. |
| [dcat:endpointDescription]("https://www.w3.org/ns/dcat#endpointDescription") | `rdfs:Resource` | `*` | Empfohlen | Die Beschreibung der Services, die unter den angebenen Endpunkten erreicht werden können. |
| [dcat:keyword]("https://www.w3.org/ns/dcat#keyword") | `rdfs:Literal` | `*` | Empfohlen | "Diese Eigenschaft enthält ein Schlagwort oder Schlüsselbegriff zur Beschreibung des Datenservices." |
| [dcat:theme](https://www.w3.org/ns/dcat#theme) | `dct:subject` | `*` | Empfohlen | Diese Eigenschaft bezieht sich auf die dem Datenservice zugewiesenen Kategorien. |
| [dct:conformsTo](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#conformsTo) | `dct:Standard` | `*` | Empfohlen | Diese Eigenschaft verweist auf ein etabliertes Schema, zu dem der Datenservice konform ist. |
| [dcat:landingPage](https://www.w3.org/ns/dcat#landingPage) | `foaf:Document` | `*` | Optional |  	Diese Eigenschaft verweist auf eine Webseite, welche Zugriff auf den Datenservice und/oder weitere Informationen ermöglicht. |
| [dct:accessRights](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#accessRights) | `dct:RightsStatement` | `0..1` | Optional |  Diese Eigenschaft verweist auf Informationen, die darlegen, ob der Datenservice öffentlich zugänglich ist, Zugriffseinschränkungen existieren oder er nicht-öffentlich ist. |
| [dct:description](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description) | `rdfs:Literal` | `*` | Optional | Diese Eigenschaft enthält eine Beschreibung des Datenservices als Freitext. |
| [dct:format](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#format) | `dct:MediaType` | `*` | Optional | Die Datenformate, die beim Abruf der dcat:endpointURL zurückgegeben werden können. |
| [dct:license](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#license) | `dct:LicenseDocument` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf die Lizenz, mit welcher der Datenservice verwendet oder wiederverwendet werden kann.|
| [healthdcatapde:dataServiceType]() | `skos:Concept` | `0..1` | Optional | Diese Eigenschaft bezieht sich auf eine Option der Service Type Liste. |

#### 5.3.2 Klasse: dct:Location

#### 5.3,4 Klasse: adms:Identifier

#### 5.3.5 Klasse: spdx:Checksum 

#### 5.3.6 Klasse: dcat:CatalogRecord

#### 5.3.7 Klasse: dcat:Relationship

#### 5.3.8 Klasse: prov:Attribution

#### 5.3.9 Klasse: skos:ConceptScheme


## 6. Kontrollierte Vokabulare

## 7. Glossar

## 8. Changelog





