---
title: Die Architektur der Analyse - Ansätze für Ihr Customer Journey Analytics-Datenmodell
description: Erfahren Sie, wie Sie CJA-Datenmodelle mit Ereignishierarchien, Attribution und KPIs strukturieren, um tiefere Journey-Einblicke für Kunden zu erschließen.
feature: Attribution
role: User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 0
last-substantial-update: 2025-09-04T00:00:00Z
jira: KT-18813
source-git-commit: 124b52203b98a80dd9202dab1b0dbe575475a52b
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Die Architektur der Analyse: So gehen Sie Ihr Customer Journey Analytics-Datenmodell an

Ein wichtiger Aspekt beim Erstellen eines CJA-Datenmodells ist das Verständnis der hierarchischen Beziehung zwischen verschiedenen Touchpoints und Interaktionen. Dies bildet die Grundlage für aussagekräftige Analysen und Erkenntnisse.

Zu den wichtigsten Aspekten gehören:

* Identifizieren und Zuordnen von Kundeninteraktionspunkten über alle Kanäle hinweg
* Klare Ereignishierarchien und -beziehungen etablieren
* Definieren konsistenter Attributionsmodelle
* Erstellen standardisierter Metriken und KPIs

Durch die korrekte Strukturierung dieser Elemente können Unternehmen die vollständige Kunden-Journey besser verfolgen und analysieren, was zu umsetzbareren Einblicken und verbesserten Entscheidungsfunktionen führt.

>[!VIDEO](https://video.tv.adobe.com/v/3471111/?learn=on&enablevpops)

## Entsperren der Datenmodellierung für leistungsstarke Analysen

Erfahren Sie, wie eine effektive Datenarchitektur in Adobe Experience Platform (AEP) und Customer Journey Analytics (CJA) zu umsetzbaren Einblicken und Berichten führt.

* **Der Schemaentwurf ist wichtig** Die Auswahl zwischen flachen Schemata, Arrays und Arrays von Objekten wirkt sich direkt auf die Analysefunktionen und die Berichtsflexibilität aus.
* **Transformationsprozess** Die in AEP aufgenommenen Daten müssen sorgfältig strukturiert sein, um eine nahtlose Transformation und Benutzerfreundlichkeit in CJA sicherzustellen.
* **Container-Hierarchie** Das Verständnis der Ereignis-, Sitzungs- und Personenebenen ist für die Analyse auf mehreren Ebenen und das genaue Reporting von entscheidender Bedeutung.
* **Praktische Strategien** Vorabplanung, Schema-Governance und die Nutzung von Plattformfunktionen sind der Schlüssel zu skalierbaren, zukunftssicheren Implementierungen.

Durch die Beherrschung dieser Konzepte können Teams ihre Analyse-Workflows optimieren und tiefere geschäftliche Einblicke erschließen.

## Schematypen und ihre Anwendungsfälle

* **Flache Schemata** Optimiert für unkomplizierte Eins-zu-eins-Datenbeziehungen. Ideal für grundlegende Ereignisverfolgung und einfache Metriken/Dimensionen.
* **Arrays** Nützlich für Listen verwandter Elemente (z. B. Produktkategorien, Inhalts-Tags). Jedes Array-Element wird zu einer individuellen Dimension für die Analyse.
* **Objekt-Arrays** Für komplexe Anwendungsfälle wie Produktkäufe, bei denen jedes Objekt seine eigenen Eigenschaften und Beziehungen beibehält. Ermöglicht eine detaillierte Analyse auf Objektebene.
* **Mit Bedacht wählen** Wählen Sie das einfachste Schema aus, das Ihren Anforderungen entspricht, aber nutzen Sie Arrays und Objekte für erweiterte Szenarien, in denen Beziehungen beibehalten werden müssen.