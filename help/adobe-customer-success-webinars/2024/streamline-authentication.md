---
title: Streamline-Authentifizierung - Migration von Dienstkonto (JWT) zu OAuth Server-zu-Server-Anmeldedaten
description: Das Adobe-Webinar unter der Leitung der Außendiensttechniker Jeff Homequest und Marco Lara konzentrierte sich auf die Migration vom Dienstkonto JWT zu OAuth-Server-zu-Server-Anmeldedaten. Es hob den Termin für die Einstellung von Januar 2025, Migrationsschritte, Vorteile von OAuth und besondere Aspekte für AEM hervor, mit umfassender Unterstützung und Dokumentation für den Prozess.
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3292
last-substantial-update: 2024-12-06T00:00:00Z
jira: KT-16629
source-git-commit: 47ae42d06ed311e60ebce194e0683bb95e8e5b69
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Streamline-Authentifizierung: Migration von Dienstkonto (JWT) zu OAuth Server-zu-Server-Anmeldedaten

Dieses Webinar führt die Teilnehmer durch die Migration von den veralteten JWT-Anmeldedaten (Service Account) zu den neuen OAuth Server-zu-Server-Anmeldedaten. Da die JWT-Anmeldeinformationen (Service Account) nach dem 27. Januar 2025 nicht mehr funktionieren, ist es für Entwickler und Organisationen von entscheidender Bedeutung, den Migrationsprozess zu verstehen, um potenzielle Dienstunterbrechungen zu vermeiden. Im Webinar werden auch die Vorteile von OAuth Server-zu-Server-Anmeldedaten und die Sicherstellung einer Migration ohne Ausfallzeiten hervorgehoben.

>[!VIDEO](https://video.tv.adobe.com/v/3440936/?learn=on&enablevpops)

## Wichtige Schritte

* **Aufzeichnung und Folien des Treffens** Das Treffen wurde aufgezeichnet, und am Ende ist ein Link zur Aufzeichnung verfügbar.
* **Einführung der Redner** Jeff Homequest und Marco Lara, beide Senior Feldingenieure bei der Adobe, führten das Webinar.
* **Webinar Focus** Das Webinar konzentrierte sich auf die Migration von JWT-Dienstkonto zu OAuth-Server-zu-Server-Anmeldedaten.
* **Veraltungsfrist** Adobe stellt die JWT-Anmeldeinformationen ein und muss bis Ende Januar 2025 migriert werden.
* **Target-Zielgruppe** Das Webinar zielte auf Anwendungsentwickler, technische Leads und Integrationsarchitekten mithilfe von JWT-Anmeldeinformationen in Adobe-Anwendungen ab.
* **Migrationsschritte** Das Webinar enthält eine schrittweise Migrationsanleitung und eine Demo.
* **Fragen und Antworten zur Sitzung** Fragen wurden während des gesamten Meetings gestellt, wobei am Ende eine spezielle Frage und Antwort-Sitzung stattfand.
* **Vorteile von OAuth** OAuth vereinfachen die Entwicklung, verbessern die Sicherheit und optimieren die Wartung im Vergleich zu JWT.
* **Timeline für die Migration**
   * 1. Mai 2023 - Ankündigung der künftigen Einstellung der Unterstützung.
   * 2. Juni 2024 - Letztes Datum zum Erstellen neuer Anmeldedaten für Dienstkonten.
   * 27. Januar 2025 - Lebenszyklusende für Dienstkonten und APIs, die sie verwenden, werden nicht mehr funktionieren.
* **&#x200B; Besondere Überlegungen für AEM** Im Webinar wurde untersucht, wie die Migration AEM Cloud- und On-Premise-Kunden beeinflusst, einschließlich spezifischer Autorisierungsmuster und -konfigurationen.
* **Automatisch generierte Integrationen** Automatisch generierte Integrationen werden von Adobe vor Ablauf der Frist automatisch migriert.
* **Support und Dokumentation** Adobe bietet umfassende Dokumentation und Unterstützung für den Migrationsprozess. Kunden können sich an Adobe-Mitarbeiter oder professionelle Dienstleistungen wenden, um Hilfe zu erhalten.
* **Testen und Validieren** Es wird empfohlen, Integrationen nach der Migration und vor dem Löschen alter JWT-Anmeldeinformationen gründlich zu testen.
* **Benutzerdefinierte Integrationen** Kunden mit benutzerdefinierten Integrationen sollten die Migration so bald wie möglich identifizieren und planen, insbesondere wenn Drittanbieter beteiligt sind.