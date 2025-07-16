---
title: Best Practices für die Migration von Adobe Analytics zu Adobe Customer Journey Analytics
description: Erfahren Sie mehr über die wichtigsten Schritte und Best Practices für die Migration von Adobe Analytics zu Customer Journey Analytics (CJA), einschließlich XDM-Schema-Design, Datenzuordnung und Einrichtung der Datenansicht.
solution: Analytics, Customer Journey Analytics
topic: Migration
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 3654
last-substantial-update: 2025-07-16T00:00:00Z
jira: KT-18535
source-git-commit: 90eb4a9d2cf445c58fde776092fb047f820fa207
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# Best Practices für die Migration von Adobe Analytics zu Adobe Customer Journey Analytics

Erfahren Sie mehr über die Migration von Adobe Analytics zu Customer Journey Analytics (CJA). Die von Nicolina Picone und Maurizio Corò vom Ultimate Success-Team von Adobe veranstaltete Veranstaltung bietet einen umfassenden Überblick über CJA, seine Funktionen und Best Practices für die Migration.

## Wichtige Diskussionsthemen

* Unterschiede zwischen Analytics und CJA
* Die Bedeutung starker Identitätskennungen, der Ausrichtung von Datenstrukturen und der Erstellung anpassbarer Datenansichten
* Behandelt Strategien für den Import historischer Daten, die Verwaltung der Marketing-Kanal-Attribution und die Nutzung der Flexibilität von CJA für maßgeschneiderte Berichte

>[!VIDEO](https://video.tv.adobe.com/v/3464911/?learn=on&enablevpops)

## Wichtige Erkenntnisse

* **Überblick über Customer Journey Analytics (CJA** CJA ist eine Weiterentwicklung von Adobe Analytics, die sich auf das vollständige Kunden-Journey über mehrere Touchpoints (z. B. Mobilgeräte, Web, CRM, Callcenter) statt auf Einzelereignisse konzentriert. Dies ermöglicht die Verarbeitung und Manipulation von Daten in Echtzeit.

* **Migrationsbereitschaft** Zu den wichtigsten Schritten bei der Migration von Adobe Analytics zu CJA gehören die Sicherstellung einer sicheren Identitätskennung (z. B. Personen-ID), die Ausrichtung von Variablen und Dimensionen und die Zuordnung von Daten zum XDM-Schema. Historische Daten können mit Validierungsschritten importiert werden.

* **Datenansichten und Flexibilität** CJA ermöglicht die Erstellung anpassbarer Datenansichten mit anpassbarer Sitzungsdauer, Segmentierungsfiltern und Attributionseinstellungen. Diese Flexibilität ermöglicht eine maßgeschneiderte Berichterstellung und Analyse.

* **Best Practices für die Migration historischer Daten** Validieren Sie CJA-Daten, indem Sie sie mit Adobe Analytics-Daten innerhalb eines akzeptablen Bereichs (z. B. 10 % Unterschied) vergleichen. Beginnen Sie mit einem kurzen Aufstockungsfenster (z. B. einen Monat) und skalieren Sie schrittweise.

* **Marketing-Kanal-Attribution** CJA bietet erweiterte Funktionen für die Attribution von Marketing-Kanälen, wodurch Einschränkungen wie die „erste Seite des Besuchs“ beseitigt werden und dynamischere Sitzungskonfigurationen ermöglicht werden.
