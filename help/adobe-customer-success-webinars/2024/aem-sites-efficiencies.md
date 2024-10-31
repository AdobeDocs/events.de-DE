---
title: AEM Sites-Effizienz - Leistungsoptimierung, Konfiguration und Fehlerbehebung
description: 'Grundlagen zur Fehlerbehebung bei Adobe Experience Manager (AEM) Sites. Unabhängig davon, ob Sie Leistungsprobleme haben oder sich mit komplexen Konfigurationen befassen, bietet diese Sitzung praktische Fertigkeiten zur Pflege und Optimierung Ihrer AEM. Wir werden Live-Demos über Folien priorisieren und praktische Erfahrung bei der Bewältigung von Herausforderungen in der realen Welt bieten​Wichtige Diskussionspunkte: Virtual-Host-Konfiguration und Domänenzuordnung - Leistungsprobleme - Autorisierung, Identifizierung, Benutzerberechtigungen'
solution: Experience Manager
version: Cloud Service
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3452
last-substantial-update: 2024-10-30T00:00:00Z
jira: KT-16353
source-git-commit: 3f245f71cd4db5097b5a9e712114112451d899e4
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---


# AEM Sites-Effizienz: Leistungsoptimierung, Konfiguration und Fehlerbehebung

In diesem Webinar werden wir uns mit den Grundlagen der Fehlerbehebung bei Adobe Experience Manager (AEM) Sites befassen. Unabhängig davon, ob Sie Leistungsprobleme haben oder sich mit komplexen Konfigurationen befassen, bietet diese Sitzung praktische Fertigkeiten zur Pflege und Optimierung Ihrer AEM. Wir werden Live-Demos über Folien priorisieren und praktische Erfahrung bei der Bewältigung von Herausforderungen in der realen Welt bieten&#x200B;

>[!VIDEO](https://video.tv.adobe.com/v/3435114/?learn=on)

## Wichtigste Punkte

Das Webinar konzentrierte sich auf die Effizienz der AMP-Site, einschließlich Leistungsoptimierung, Konfiguration und Fehlerbehebung.

### Dispatcher-Konfiguration

* Bedeutung des Dispatchers bei der Bereitstellung leistungsfähiger Websites.
* Wichtige Aspekte der Dispatcher-Konfiguration: Konfiguration des virtuellen Hosts, Domänenzuordnung mit Cachestruktur sowie regelmäßige Berichte und Umleitungen.

### Rights Management

* Best Practices: Wenden Sie Berechtigungen auf Gruppen an, vermeiden Sie Abweisungsanweisungen und vermeiden Sie ÜberEngineering.
* Verwendung des Netcentric ACL-Tools zur Verwaltung von Rechten über eine Yaml-Datei, um eine einfache Bereitstellung und Rückverfolgbarkeit zu gewährleisten.

### Leistungsprobleme

* Wichtig ist, Deltas bei Synchronisierungsvorgängen zu identifizieren, um vollständige Cache-Leerungen zu vermeiden.
* Vermeiden Sie große Seitenvorgänge während der Geschäftszeiten.
* Vereinfachung der Workflows auf die erforderlichen Schritte.
* Seien Sie vorsichtig mit Systemprozessen von Drittanbietern auf Autorensystemen, insbesondere mit Tools wie ImageMagick.
* Vermeiden Sie synchronisierte Anforderungen an Drittanbietersysteme, die die Last nicht verarbeiten können.
* Verwalten Sie umfangreiche benutzerdefinierte Komponenten, um Leistungseinbußen zu vermeiden.
* Überwachen Sie Sitzungen mit langer Laufzeit, um zu verhindern, dass keine Segmentausnahmen gefunden werden.