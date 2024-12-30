---
title: Optimieren der Authentifizierung - Migration vom Dienstkonto (JWT) zu OAuth-Server-zu-Server-Anmeldeinformationen
description: Das von den leitenden Außendiensttechnikern Jeff Homequest und Marco Lara geleitete Adobe-Webinar konzentrierte sich auf die Migration vom Dienstkonto-JWT zu OAuth-Server-zu-Server-Anmeldeinformationen, wobei die Frist für die Einstellung im Januar 2025, die Migrationsschritte, die Vorteile von OAuth und besondere Überlegungen für AEM mit umfassender Unterstützung und Dokumentation für den Prozess hervorgehoben wurden.
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3292
last-substantial-update: 2024-12-06T00:00:00Z
jira: KT-16629
exl-id: 97e2a2de-1cb4-4f2f-8c9b-47ee40227625
source-git-commit: 1387be704e6b6dc1a7446e409da7da81403fdc3c
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Optimieren der Authentifizierung: Migration vom Dienstkonto (JWT) zu OAuth-Server-zu-Server-Anmeldeinformationen

Dieses Webinar führt Teilnehmende durch die Migration von den veralteten JWT-Anmeldedaten (Service Account) zu den neuen OAuth-Server-zu-Server-Anmeldedaten. Da die Anmeldeinformationen für das Service-Konto (JWT) nach dem 27. Januar 2025 nicht mehr funktionieren, ist es für Entwickler und Organisationen wichtig, den Migrationsprozess zu verstehen, um potenzielle Service-Unterbrechungen zu vermeiden. In diesem Webinar werden auch die Vorteile von OAuth Server-zu-Server-Anmeldeinformationen und die Gewährleistung einer Migration ohne Ausfallzeiten erläutert.

>[!VIDEO](https://video.tv.adobe.com/v/3440936/?learn=on&enablevpops)

## Wichtige Erkenntnisse

* **Besprechungsaufzeichnung und Folien** Das Meeting wurde aufgezeichnet, und am Ende wird ein Link zur Aufzeichnung verfügbar sein.
* **Vorstellung der Redner** Jeff Homequest und Marco Lara, beide Senior Field Engineers beim Adobe, leiteten das Webinar.
* **Webinar-**: Das Webinar konzentrierte sich auf die Migration vom JWT des Service-Kontos zu OAuth-Server-zu-Server-Anmeldeinformationen.
* **Deprecation Deadline** JWT-Anmeldeinformationen werden von Adobe nicht mehr unterstützt und müssen bis Ende Januar 2025 migriert werden.
* **Target-Zielgruppe** Das Webinar richtete sich an Anwendungsentwickler, technische Leiter und Integrationsarchitekten, die JWT-Anmeldeinformationen in Adobe-Anwendungen verwenden.
* **Migrationsschritte** Das Webinar umfasste eine schrittweise Migrationshandbuch und eine Demo.
* **Fragen und Antworten** Fragen wurden während des gesamten Meetings gestellt und am Ende wurde eine dedizierte Frage- und Antwortsitzung hinzugefügt.
* **Vorteile von OAuth** OAuth vereinfacht im Vergleich zu JWT die Entwicklung, erhöht die Sicherheit und optimiert die Wartung.
* **Zeitplan für die Migration**
   * 1. Mai 2023 - Ankündigung der zukünftigen Einstellung.
   * 2. Juni 2024 - Letztes Datum für die Erstellung neuer Anmeldedaten für Service-Konten.
   * 27. Januar 2025 - Das Ende der Lebensdauer von Service-Konten und APIs, die sie verwenden, funktionieren nicht mehr.
* **&#x200B;Besondere Hinweise für AEM** Im Webinar wurde erörtert, wie sich die Migration auf AEM-Cloud- und On-Premise-Kunden auswirkt, einschließlich spezifischer Autorisierungsmuster und -konfigurationen.
* **Automatisch generierte Integrationen** Automatisch generierte Integrationen werden vor Ablauf der Frist automatisch per Adobe migriert.
* **Support und Dokumentation** Adobe bietet umfangreiche Dokumentationen und Unterstützung für den Migrationsprozess. Kunden können sich an Adobe-Mitarbeiter oder professionelle Services wenden, um Unterstützung zu erhalten.
* **Testen und Validierung** Es wird empfohlen, Integrationen nach der Migration und vor dem Löschen alter JWT-Anmeldeinformationen gründlich zu testen.
* **Benutzerdefinierte Integrationen** Kunden mit benutzerdefinierten Integrationen sollten die Migration so schnell wie möglich identifizieren und planen, insbesondere wenn Drittanbieter beteiligt sind.
