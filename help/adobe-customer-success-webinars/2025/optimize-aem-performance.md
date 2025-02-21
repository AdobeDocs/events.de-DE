---
title: Optimieren der AEM-Leistung - Caching-Strategien und -Techniken
description: In der Sitzung wurden Strategien und Techniken für das Caching, Caching-Mechanismen und -Ebenen, die Verarbeitung dynamischer Inhalte, das Debugging von Caching-Problemen und die Synchronisierung der Cache-Invalidierung zwischen dem Dispatcher und dem CDN behandelt.
topic: Performance
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3764
last-substantial-update: 2025-02-21T00:00:00Z
jira: KT-17373
source-git-commit: e7bf8b79ad4920b303fc3afbdfb4adee60614c88
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# Optimieren der AEM-Leistung: Caching-Strategien und -Techniken

In dieser Sitzung untersuchen wir verschiedene Caching-Mechanismen - wie Seiten-, Asset- und Dispatcher-Caching - sowie die Implementierung des Caching auf CDN-Ebene, um die Inhaltsbereitstellung zu optimieren und Ladezeiten zu reduzieren. In der Diskussion werden Best Practices für jede Caching-Ebene, die Behebung gängiger Probleme und die Nutzung von CDN-Funktionen für maximale Effizienz behandelt.

## Wichtige Diskussionspunkte

* Einführung in das Caching
* Arten der Zwischenspeicherung, Best Practices für die Zwischenspeicherung, Cache-Invalidierung und -Aktualisierung
* Debugverfahren

>[!VIDEO](https://video.tv.adobe.com/v/3444452/?learn=on&enablevpops)

## Wichtige Erkenntnisse

* **Caching-Strategien und -Techniken** Die Sitzung konzentrierte sich auf verschiedene Caching-Strategien und -Techniken zur Leistungsoptimierung, einschließlich des Caching auf verschiedenen Ebenen wie Browser, CDN und Dispatcher.

* **Caching-Mechanismen und -Ebenen** In der Diskussion wurden verschiedene Caching-Mechanismen und -Ebenen behandelt, einschließlich Browser-Caching, CDN-Caching und Dispatcher-Caching, und es wurde erörtert, wie sie konfiguriert und verwaltet werden können.

* **Dynamic Content Handling** Es wurden Techniken zum Umgang mit dynamischen Inhalten auf einer Seite besprochen, einschließlich der Verwendung von Sling Dynamic Include (SDI) und Edge Side Includes (ESI), um sicherzustellen, dass dynamische Inhalte nicht zwischengespeichert werden, während statische Inhalte zwischengespeichert werden.

* **Debugging von Caching** Es wurden verschiedene Techniken zum Debugging von Caching-Problemen auf verschiedenen Ebenen (Browser, CDN, Dispatcher) erläutert, einschließlich der Verwendung von Kopfzeilen, Protokollen und bestimmten Konfigurationen zur Identifizierung und Lösung von Caching-Problemen.

* **Synchronisation der Cache-**: In der Sitzung wurde die Herausforderung behandelt, die Cache-Invalidierung zwischen dem Dispatcher und dem CDN zu synchronisieren. Es wurde empfohlen, kürzere Werte für das maximale Alter und CDN-Bereinigungs-APIs zu verwenden, um sicherzustellen, dass beide Caches bei der Seitenaktivierung gleichzeitig ungültig gemacht werden.