---
title: Dispatcher-Konfigurationen in Adobe Experience Manager as a Cloud Service
description: Erfahren Sie mehr über die Best Practices für Caching, Sicherheit und Leistung von AEM Dispatcher, um die Skalierbarkeit und Effizienz von AEM as a Cloud Service zu maximieren.
solution: Experience Manager as a Cloud Service
version: Experience Manager as a Cloud Service
feature: Dispatcher
role: Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 4200
last-substantial-update: 2025-05-07T00:00:00Z
jira: KT-17903
source-git-commit: cfc7b54ae4360779ca2c41f88fc08089bae99165
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---


# Technische Sitzungen: Dispatcher-Konfigurationen in Adobe Experience Manager as a Cloud Service

**Adobe Experience Manager (AEM) as a Cloud Service** bietet Skalierbarkeit, Flexibilität und verbesserte Leistung für moderne Digital-Experience-Plattformen. Kernstück dieser Architektur ist die **AEM Dispatcher**, eine wichtige Komponente für Caching, Sicherheit und Anfragenverwaltung. Wenn die Dispatcher ordnungsgemäß konfiguriert ist, beschleunigt sie die Bereitstellung von Inhalten, schützt Backend-Systeme und steigert die Gesamtleistung der Site.

In dieser Übersicht werden die wichtigsten Einstellungen von Dispatcher beschrieben, einschließlich Caching-Strategien, Zugriffskontrollmechanismen und Anforderungsfilterung. Außerdem werden Best Practices für die Aufrechterhaltung einer sicheren und leistungsstarken AEM-Bereitstellung in der Cloud beschrieben. Unabhängig davon, ob Sie Entwickler, Architekten oder geschäftliche Entscheidungsträger sind, ist ein solides Verständnis von Dispatcher-Konfigurationen entscheidend, um das volle Potenzial von AEM as a Cloud Service zu erschließen.

>[!VIDEO](https://video.tv.adobe.com/v/3457891/?learn=on&enablevpops)

## Wichtige Schlussfolgerungen

* **Dispatcher SDK zur Validierung** Die AEM Dispatcher SDK ist ein leistungsstarkes Tool für die statische Konfigurationsanalyse. Es ermöglicht eine schnelle Validierung von Konfigurationen, prüft auf Unveränderlichkeit und identifiziert Fehler, was im Vergleich zu vollständigen Pipeline-Bereitstellungen viel Zeit spart.

* **Schnelle Entwicklungsumgebung (RDE)** RDE bietet eine interaktive Laufzeitumgebung zum Testen und Debuggen von Konfigurationen, die über die statische Analyse hinausgehen. Dies ermöglicht eine schnellere Validierung und Fehlerbehebung und verringert den Zeitaufwand für die Bereitstellung und das Testen.

* **Erweiterte Netzwerke mit Mod-Proxy** Erweiterte Netzwerkkonfigurationen wie VPN und dedizierte Ausgangs-IPs können mit Cloud Manager eingerichtet werden. Das mod-Proxy-Modul ermöglicht die Abladung von Transaktionen von AEM an externe Services, wodurch die Leistung optimiert und die Belastung der JVM verringert wird.

* **Best Practices für Dispatcher-Konfigurationen** Zu den wichtigsten Empfehlungen gehören die Verwendung relativer Pfade, eindeutiger x-vhost-Header, ordnungsgemäßer Client-Header und die Nutzung von Cache-Control-Headern zur effektiven Verwaltung des Caching. Auf diese Weise lassen sich Pipeline-Fehler vermeiden und die Debugging-Effizienz verbessern.

* **Web-Stufen-Pipeline für die Bereitstellung** Die Web-Stufen-Pipeline ist ein Dienstprogramm für die Bereitstellung isolierter Dispatcher-Konfigurationen. Es umfasst zusätzliche Tests wie die Cache-Invalidierung, um sicherzustellen, dass Inhaltsaktualisierungen in Produktionsumgebungen sofort und korrekt widergespiegelt werden.