---
title: AEM Sites-Effizienz - Leistungsoptimierung, Konfiguration und Fehlerbehebung
description: In dieser Sitzung werden wesentliche Kenntnisse zur Fehlerbehebung für Adobe Experience Manager (AEM) Sites behandelt, wobei der Schwerpunkt auf praktischen, praktischen Lösungen für Leistungsprobleme, komplexen Konfigurationen und Benutzerberechtigungen liegt.
solution: Experience Manager
version: Cloud Service
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3452
last-substantial-update: 2024-10-30T00:00:00Z
jira: KT-16353
exl-id: 55f7c1d8-7c2c-4392-894a-2aa9b3cc0e4a
source-git-commit: ef652eb09c33f11d69ec66f70013cd3e53537a95
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# AEM Sites-Effizienz: Leistungsoptimierung, Konfiguration und Fehlerbehebung

In diesem Webinar gehen wir auf die Grundlagen zur Fehlerbehebung bei Adobe Experience Manager (AEM) Sites ein. Unabhängig davon, ob Sie Leistungsprobleme haben oder komplexe Konfigurationen haben, bietet diese Sitzung praktische Fähigkeiten zur Pflege und Optimierung Ihrer AEM-Umgebung. Wir haben bei Live-Demos Priorität vor Folien und bieten praktische Erfahrung bei der Bewältigung realer Herausforderungen&#x200B;

>[!VIDEO](https://video.tv.adobe.com/v/3435114/?learn=on)

## Wichtigste Punkte

Das Webinar konzentrierte sich auf die Effizienz der AMP-Site, einschließlich Leistungsoptimierung, Konfiguration und Fehlerbehebung.

### Dispatcher-Konfiguration

* Bedeutung des Dispatchers bei der Bereitstellung leistungsfähiger Websites.
* Schlüsselaspekte der Dispatcher-Konfiguration: Konfiguration virtueller Hosts, Domain-Zuordnung mit Cache-Struktur und regelmäßiges Reporting und Weiterleitungen.

### Rights Management

* Best Practices: Wenden Sie Rechte auf Gruppen an, vermeiden Sie Ablehnungsanweisungen und übertriebenes Engineering.
* Verwendung des Netcentric ACL-Tools zur Verwaltung von Rechten über eine YAML-Datei, um eine einfache Bereitstellung und Rückverfolgbarkeit sicherzustellen.

### Leistungsprobleme

* Wichtigkeit der Identifizierung von Deltas bei Synchronisierungsvorgängen, um vollständige Cache-Leerungen zu vermeiden.
* Vermeiden Sie große Seitenvorgänge während der Geschäftszeiten.
* Vereinfachen Sie Workflows auf die erforderlichen Schritte.
* Seien Sie vorsichtig mit Systemprozessen von Drittanbietern auf Autorensystemen, insbesondere mit Tools wie ImageMagick.
* Vermeiden Sie synchronisierte Anfragen an Drittanbietersysteme, die die Last nicht bewältigen können.
* Verwalten Sie umfangreiche benutzerdefinierte Komponenten, um Leistungseinbußen zu vermeiden.
* Überwachen Sie nach langwierigen Sitzungen, um zu verhindern, dass Ausnahmen für Segmente nicht gefunden werden.
