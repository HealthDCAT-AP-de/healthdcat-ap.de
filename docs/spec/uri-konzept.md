# URI-Konzept
**zuletzt geändert am 18.12.2024** 

Hier entsteht das URI-Konzept für HealthDCAT-AP.de.

# Konventionen und Empfehlungen für URIs

# Genutzte kontrollierte Vokabulare für HealthDCAT-AP.de

## EU Authority tables

|Name|URI|Beschreibung|Anwendung in HealthDCAT-AP.de|
|---|---|---|---|
|Access right|[http://publications.europa.eu/resource/authority/access-right](http://publications.europa.eu/resource/authority/access-right)|Die Tabelle der Zugriffsrechte ist ein kontrolliertes Vokabular, in dem die Zugriffsrechte oder -beschränkungen auf Ressourcen aufgeführt sind. Es ist für DCAT-Beschreibungen von Datensätzen vorgesehen, aber nicht darauf beschränkt.|`dct:accessRights`|
|Countries and territories|[http://publications.europa.eu/resource/authority/country](http://publications.europa.eu/resource/authority/country)| BeschrLänder und Gebiete ist ein kontrolliertes Vokabular, das Begriffe auflistet, die mit Namen von Ländern und Gebieten verbunden sind. Es ist ein Referenzdatenbestand, der unter die Politik der Europäischen Kommission zur Verwaltung von Referenzdaten fällt. Es enthält Codes und Namen von geografischen und geopolitischen Einheiten in allen EU-Amtssprachen und ist das Ergebnis einer Kombination mehrerer einschlägiger Standards, die geschaffen wurden, um den Anforderungen und Anwendungsfällen der Dienststellen der EU-Institutionen gerecht zu werden. Sein Hauptanwendungsbereich ist die Unterstützung dokumentarischer Metadatenaktivitäten.|`dct:spatial`|
|Data service type|[http://publications.europa.eu/resource/dataset/data-service-type](http://publications.europa.eu/resource/dataset/data-service-type)|Die Data Service Authority table ist ein kontrolliertes Vokabular mit möglichen Datendiensttypen, das speziell für das Projekt Linked Data Solutions (LDS) entwickelt wurde.|`healthdcatapde:dataServiceType`|
|Data theme|[http://publications.europa.eu/resource/dataset/access-right](http://publications.europa.eu/resource/authority/data-theme)| Die Data theme Authority table ist ein kontrolliertes Vokabular, das Konzepte auflistet, die mit den für die Klassifizierung von Datensätzen verwendeten Themen verbunden sind. Sein Hauptzweck ist die Unterstützung von Aktivitäten im Zusammenhang mit dem Anwendungsprofil des Data Catalog Vocabulary (DCAT-AP).  Die Konzepte wurden von der Arbeitsgruppe definiert, die für die Überarbeitung des DCAT-AP zuständig ist. Das Datenthema wird vom Amt für Veröffentlichungen der Europäischen Union verwaltet und auf der Website EU Vocabularies veröffentlicht.|`dcat:theme`|
|Dataset type|[https://publications.europa.eu/resource/authority/dataset-type](https://publications.europa.eu/resource/authority/dataset-type)|Dataset type ist ein kontrolliertes Vokabular, das die Arten von Datensätzen auflistet. Sein Hauptzweck ist die Unterstützung der Kategorisierung von Datensätzen auf dem offiziellen Portal für europäische Daten (data.europa.eu).|`dct:type`|
|Distribution status|[http://publications.europa.eu/resource/authority/distribution-status](http://publications.europa.eu/resource/authority/distribution-status)|Die Distribution status authority table ist ein kontrolliertes Vokabular, das zur Definition des Status von Verteilungen von Datensätzen verwendet wird, die mit dem DCAT-AP-Datenmodell beschrieben werden. Sie wurde entwickelt, um die Verwendung der von DCAT-AP vorgeschriebenen ADMS-Begriffe als kontrolliertes Vokabular zu ermöglichen. |`adms:status`|
|File type|[http://publications.europa.eu/resource/authority/file-type](http://publications.europa.eu/resource/authority/file-type)|File type ist ein kontrolliertes Vokabular, das verschiedene Arten von digitalen Dateien auflistet. Es wird vom Interinstitutionellen Ausschuss für Metadaten und Formate (IMFC) verwaltet, vom Publications Office der Europäischen Union gepflegt und auf der Website EU Vocabularies verbreitet. |`dct:format`|
|Language|[publications.europa.eu/resource/authority/language](publications.europa.eu/resource/authority/language)|Languages ist ein kontrolliertes Vokabular, das die Weltsprachen und Sprachvarietäten, einschließlich der Gebärdensprachen, auflistet. Sein Hauptzweck ist die Unterstützung von Aktivitäten im Zusammenhang mit dem Veröffentlichungsprozess. Der vollständige Satz von Sprachen enthält mehr als 8000 Sprachvarietäten, die jeweils durch einen Code gekennzeichnet sind, der dem ISO 639-3-Code entspricht. Die Konzepte sind an die internationale Norm ISO 639 angeglichen.|`dct:language`|
|Planned availability|[http://publications.europa.eu/resource/authority/planned-availability](http://publications.europa.eu/resource/authority/planned-availability)|Die Tabelle „Planned availability authority“ ist ein kontrolliertes Vokabular, das die geplante Verfügbarkeit der von DCAT-AP definierten Ressourcen angibt, nämlich Distribution, Datensatz und Datendienst. Die Liste wurde ursprünglich in den DCAT-AP-Standard aufgenommen um die Verfügbarkeit von DCAT-Distributionen zu beschreiben.|`dcatap:availability`|
|Target audience|[http://publications.europa.eu/resource/dataset/target-audience](http://publications.europa.eu/resource/dataset/target-audience)|Target audience ist ein kontrolliertes Vokabular, das die für allgemeine Veröffentlichungen verwendeten Zielgruppen auflistet. Es wird vom Publications Office der Europäischen Union verwaltet und auf der Website EU Vocabularies veröffentlicht.|`healthdcatapde:targetAudience`|


## Weitere kontrollierte Vokabulare

|Name|URI|Beschreibung|Anwendung in HealthDCAT-AP.de|
|---|---|---|---|
|DPV: Personal data| [https://w3c.github.io/dpv/2.0/pd/](https://w3c.github.io/dpv/2.0/pd/)|Die Erweiterung Personal Data (PD) bietet zusätzliche Konzepte zur Darstellung verschiedener Arten und Kategorien personenbezogener Daten für die Verwendung mit der Data Privacy Vocabulary (DPV)-Spezifikation. |`dpv:hasPersonalData`|
|DPV: Purposes |[https://w3c.github.io/dpv/2.0/dpv/#vocab-purposes](https://w3c.github.io/dpv/2.0/dpv/#vocab-purposes)|Die DPV-Purposes Taxonomie wird verwendet, um das Ziel oder den Grund darzustellen, der mit der Verarbeitung personenbezogener Daten und dem Einsatz von Technologien verbunden ist.|`dpv:hasPurpose`|



