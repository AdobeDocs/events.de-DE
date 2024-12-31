---
title: Schnelle Entwicklungsumgebungen für Adobe Experience Manager
description: Erleichterung der schnellen Entwicklung und Bereitstellung in Cloud-Umgebungen mit der neuen Adobe-SDK, wodurch die Bereitstellungszeit erheblich verkürzt wird und schnelle Updates, Live-Protokolle und erweiterte Konfigurationsoptionen unterstützt werden, wie in DevOps Life 2024 erläutert.
feature: Developer Tools
topic: Development
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 2427
last-substantial-update: 2024-11-27T00:00:00Z
jira: KT-16570
exl-id: 330d8be1-14a0-488a-aae0-ee90e1f7621e
source-git-commit: baacc97f717d27581d0ef28384e2f680dbef854e
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Schnelle Entwicklungsumgebungen für Adobe Experience Manager

Erfahren Sie mehr über Best Practices für schnelle Entwicklungsumgebungen (RDEs) und die aktualisierte Entwicklerkonsole. Natalia Angulo Herrera, Software Development Engineer bei Adobe, und Remo Liechti, Software Development Engineer bei Adobe, behandeln die Migrationsherausforderungen, die AIO CLI-Einrichtung, Bereitstellung, Tests, Protokollierung und Konfigurationsverwaltung für einen reibungsloseren Adobe Experience Manager-Workflow.

>[!VIDEO](https://video.tv.adobe.com/v/3440397/?learn=on&enablevpops)


## Community-Diskussion

Setzen Sie das Gespräch in der Adobe Developers Live-Community [Diskussion](https://adobe.ly/3UJluDo) fort.

## Wichtige Erkenntnisse

* **Einführung in DevOps Life 2024** Die Session wird von Natalia und Remo von Adobe gehostet, wobei der Schwerpunkt auf schnellen Entwicklungsumgebungen liegt.
* **Problembeschreibung** Die Herausforderung, dass lokale Entwicklungsumgebungen lokal gut funktionieren, aber bei der Bereitstellung in der Cloud fehlschlagen.
* **Lösung** Erstellung einer neuen SDK in der Cloud, um eine schnelle Entwicklung und Bereitstellung zu ermöglichen und die Zeit von 30 Minuten auf Sekunden oder einige Minuten zu reduzieren.
* **Bereitstellungsprozess** Die neue Umgebung ermöglicht schnelle Aktualisierungen und Validierungen über ein neues API- und CLI-Plug-in und ermöglicht so schnelleres Feedback und eine schnellere Bereitstellung.
* **Infrastrukturunterschiede** Die Cloud-Umgebung verwendet eine einzige Autoren- und Veröffentlichungsinstanz ohne hohe Verfügbarkeit und verwendet keine MongoDB.
* **Einrichtung und Verwendung** Entwickler können über die Cloud-Schnittstelle eine schnelle Entwicklungsumgebung einrichten, wobei npm und Adobe IO CLI für die Installation und Konfiguration verwendet werden.
* **Basic Commands** Zu den wichtigsten Befehlen gehören io und —help, io login, io status, io install, io history, io delete und io reset.
* **Protokollierung und Debugging** Die neue Umgebung unterstützt Live-Protokolle und das Ändern von Protokollebenen ohne erneute Bereitstellung mithilfe von Befehlen wie io am- oder d-Protokollen.
* **Erweiterte Themen** Unterstützung für Frontend-Pakete und Konfigurations-Pipelines, die eine schnelle Bereitstellung und Iteration ermöglichen.
* **Kommende Funktionen** plant die Einführung der Snapshot-Funktion für einfacheres Zurücksetzen der Umgebung und automatische Aktualisierungen ohne Inhaltsverlust.
* **Fragen und Antworten und Feedback** Die Sitzung ermutigt die Teilnehmer, dem Discord-Kanal beizutreten, um Live-Interaktionen und Feedback mit dem Entwicklungsteam zu erhalten.
