---
title: Adobe Pass - neue REST-API v2
description: In dieser Sitzung wird die neue REST-API v2 von Adobe vorgestellt und die Anwender werden durch den Migrationsprozess geführt.
role: Developer
level: Beginner, Intermediate, Experienced
doc-type: Technical Video
duration: 3230
last-substantial-update: 2025-04-07T00:00:00Z
jira: KT-17685
hidefromtoc: true
source-git-commit: 1082d67d49901e151115255b585799a5f57bda4a
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---


# Adobe Pass - neue REST-API v2

In dieser Sitzung wird die neue REST-API v2 von Adobe vorgestellt und die Anwender werden durch den Migrationsprozess geführt.

>[!VIDEO](https://video.tv.adobe.com/v/3457461/?learn=on&enablevpops)

## Wichtige Highlights

* **Überblick und Vorteile**

   * Die REST-API v2 wurde für eine moderne, flexible und skalierbare Authentifizierung entwickelt, die auf anspruchsvolle Ereignisse und Szenarien mit mehreren Geräten ausgerichtet ist.
   * Zu den wichtigsten Verbesserungen gehören die verbesserte Verschlüsselung, Sitzungskonsistenz, geräteübergreifendes SSO und erweiterte Fehlerinformationen für ein schnelleres Debugging.

* **Migrationsschritte**

   * Benutzer müssen neue registrierte Anwendungen mit REST API v2-Bereichen erstellen.
   * Vorhandene Konfigurationen wie Gerätekennung und MVPD-Zuordnungen können wiederverwendet werden.
   * Die Migration umfasst Phasen wie Registrierung, Konfiguration, Authentifizierung, Vorabautorisierung und Autorisierung.

* **Funktionale Verbesserungen**

   * Die einheitliche RESTful-API ersetzt Access Neighbor-SDKs und vereinfacht die Implementierung über Plattformen hinweg.
   * Unterstützung mehrerer Authentifizierungsprofile innerhalb derselben Sitzung und nahtlose geräteübergreifende Übergänge.
   * Die Flüsse der Vorabautorisierung und Autorisierung bleiben für den Inhaltszugriff obligatorisch.

* **Planung**

   * Die REST-API v1 erhält bis Dezember 2025 keine Updates mehr und wird bis Ende 2026 vollständig eingestellt.
   * Die Benutzer sollten die Migration rechtzeitig vor diesen Fristen abschließen.

* **Ressourcen und Support**

   * Dokumentation, Cookbooks und häufig gestellte Fragen sind auf Adobe Experience League verfügbar.
   * Adobe bietet Sandbox-Umgebungen, Zendesk-Tickets und Migrationstreffen zur Unterstützung an.

* **Highlights mit Fragen und Antworten**

   * Die REST-API v2 erfordert eine erneute Authentifizierung, da sie nicht mit v1 abwärtskompatibel ist.
   * Die Vorabautorisierung dient Benutzeroberflächenzwecken, während für Medien-Token eine Autorisierung erforderlich ist.
   * SSO wird über ein neues Adobe-Service-Token unterstützt.

