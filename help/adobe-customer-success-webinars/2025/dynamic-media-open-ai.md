---
title: Meistern von Dynamic Media mit Open API
description: Machen Sie sich mit den wichtigsten Unterschieden zwischen herkömmlichem Dynamic Media und dem Open-API-Modell vertraut und erfahren Sie, wie Sie Dynamic Media Ultimate mit Open API erfolgreich umstellen und implementieren können.
solution: Experience Manager as a Cloud Service, Experience Manager Assets
feature-set: Experience Manager Assets
feature: SDK/API
topic: Development, Content Management
role: Admin, Developer, User
level: Beginner, Intermediate
doc-type: Event
duration: 2757
last-substantial-update: 2025-08-08T00:00:00Z
jira: KT-18702
source-git-commit: ef1eacd73c5a4fb9cdfee730d40606ec65bab2a7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 3%

---


# Meistern von Dynamic Media mit Open API

Dieses Webinar richtet sich an Fachleute, die mit Dynamic Media vertraut sind und „Dynamic Media Ultimate&quot; [ Open API ](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dm-prime-ultimate) und implementieren möchten.  Wir werden die allgemeinen Funktionen von Dynamic Media Ultimate mit Open API untersuchen und mit denen von herkömmlichem Dynamic Media vergleichen. Unser Ziel ist es, ein umfassendes Verständnis der Unterschiede zwischen diesen beiden Ansätzen zu liefern, sodass sich mit Dynamic Media vertraute Teilnehmer einfach an das Open-API-Modell anpassen können.

>[!VIDEO](https://video.tv.adobe.com/v/3470620/?learn=on&enablevpops)

## Vergleich der wichtigsten Funktionen

| Funktion | Dynamic Media | Dynamic Media mit OpenAPI |
|-----------------------------|------------------------|----------------------------|
| *Verfügbarkeit* | On-Premise, AMS, Cloud | Nur Cloud |
| *Modifiers* | Rich-Set verfügbar | Begrenzt, aber steigend |
| *Zugangssteuerung* | Für alle Benutzer offen | Eingeschränkt nach Rollen |
| *CDN TTL* | ~10 Stunden | ~10 Minuten |
| *Durchsetzung von Genehmigungen* | Automatisch veröffentlicht | Erfordert Genehmigung |
| *SEO-freundlich* | Ja | Ja |

## Integrationsszenarien

Diese Integrationsszenarien zeigen die Flexibilität und Skalierbarkeit von Dynamic Media mit OpenAPI für unterschiedliche Unternehmensanforderungen.

* **AEM Sites-Integration** Dynamic Media mit OpenAPI unterstützt die nahtlose Integration mit AEM Sites, sodass Assets direkt aus der Bereitstellungsebene abgerufen werden können, ohne dass Duplikate auftreten.
* **CMS von Drittanbietern** Ermöglicht die Integration in Plattformen wie Salesforce und Drupal mithilfe von APIs oder Micro-Front-End-Anwendungen.
* **API-gesteuerter Zugriff** Bietet APIs zum Suchen, Abrufen und Bereitstellen optimierter Ausgabedarstellungen von Assets.
* **Optimierung der Versandstufe** Assets werden über Fastly bereitgestellt, wodurch eine schnellere und effizientere Bereitstellung gewährleistet ist.