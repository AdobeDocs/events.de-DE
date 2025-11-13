---
title: Wichtige Tipps und Best Practices für die AEM Lucene-Suche
description: Verbessern Sie die digitale Interaktion mit erweiterten AEM-Suchwerkzeugen wie Filtern, Facetten, automatischen Vorschlägen, NGram und Rechtschreibprüfung. Lernen Sie aus echten Demos.
solution: Experience Manager
feature: Search
role: Admin, Developer
level: Intermediate, Experienced
doc-type: Event
duration: 3630
last-substantial-update: 2025-11-13T00:00:00Z
jira: KT-19550
source-git-commit: 84c9a126769fa94b0197d12ca594137e13edc510
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---


# Wichtige Tipps und Best Practices für die AEM Lucene-Suche

Erfahren Sie, wie Sie Ihre digitale Präsenz verbessern und die Kundeninteraktion mit den neuesten Suchfunktionen verbessern können, einschließlich Filtern, Facetten, automatischen Vorschlägen, NGram und Rechtschreibprüfung. Lernen Sie aus echten Demos und erhalten Sie Einblicke in die Optimierung Ihrer Suchfunktionen mit AEM und Lucene. Dieses Webinar bietet Ihnen die Möglichkeit, Ihr Sucherlebnis zu verbessern und in der digitalen Landschaft einen Vorsprung zu erzielen.

>[!VIDEO](https://video.tv.adobe.com/v/3476410/?learn=on&enablevpops)

## Ermöglichen einer leistungsstarken Suche in Adobe Experience Manager

Adobe Experience Manager (AEM) nutzt die Lucene-Suche, um schnelle und relevante Ergebnisse für Inhalte, Assets und Metadaten bereitzustellen. In dieser Sitzung wird untersucht, wie Lucene-Indizes funktionieren, wie sie konfiguriert werden und welche Best Practices zur Maximierung der Suchleistung vorliegen.

* **Lucene Search is Everywhere** ermöglicht die Suche in AEM-Autoren-, -Publisher- und -Portalen sowie die Verarbeitung von automatischen Vorschlägen, Filtern, Facetten und Paginierung.
* **Indexdefinitionen steigern die Leistung** Die Anpassung von Oak-Indexdefinitionen ist für eine effiziente, zielgerichtete Suche von entscheidender Bedeutung.
* **Best Practices sind wichtig** Kopieren Sie vorhandene Indexdefinitionen, beschränken Sie indizierte Eigenschaften und verwenden Sie die richtigen Flags für Volltext- und Eigenschaftensuchen.
* **Erweiterte Funktionen erweitern UX**-Facetten, automatische Vorschläge, Rechtschreibprüfung, Verstärken und Nachahmen können für umfassendere Sucherlebnisse aktiviert werden.

Wenn Sie diese Prinzipien verstehen, können Sie in AEM stabile, hochwertige Suchfunktionen sicherstellen, die sowohl technische als auch geschäftliche Ziele unterstützen.

## Lucene-Index-Bausteine

AEM Lucene-Indexdefinitionen bilden die Grundlage für die Suchleistung und -genauigkeit. Zu den wichtigsten Komponenten gehören:

* **Type** Gibt die Indexart an (Lucene, Eigenschaft usw.).
* **Knotentyp-Einschränkung** Targeting bestimmter Inhaltstypen (z. B. dam:Asset, cq:Page)
* **Pfadbeschränkung** Begrenzt die Indizierung auf definierte Repository-Pfade, um die Effizienz zu steigern.
* **Aggregierte Regeln** Steuert Tiefe und Umfang indizierter Inhalte und stellt sicher, dass relevante Eigenschaften durchsuchbar sind.
* **Indexregeln** Kernkonfiguration; legt Flags wie nodeScopeIndex (breite Volltextsuche) und Analysiert (Tokenisierung/Normalisierung) fest.

Eine sorgfältige Konfiguration dieser Elemente stellt sicher, dass Suchabfragen schnell, relevant und ressourceneffizient sind.

## Suchleistung optimieren

Für eine effektive Suchoptimierung in AEM Lucene müssen die strategische Konfiguration und die Best Practices eingehalten werden:

* **Mit vorhandenen Indizes beginnen** Standarddefinitionen immer kopieren und ändern und nie von Grund auf neu erstellen.
* **Indizierte Eigenschaften begrenzen** Schließen Sie nur die erforderlichen Eigenschaften ein, um Indizes schlank und leistungsfähig zu halten.
* **Verwenden Sie Kennzeichnungen mit Bedacht:
   * **nodeScopeIndex** true für eine breite Volltextsuche
   * **analyzed** true für Tokenisierung auf Eigenschaftsebene
   * **evaluatePathRestriction** true für pfadbasierte Abfragen
* **Eigenschaftenindizierung** Bevorzugte Eigenschaftsbeschränkung sucht nach der besten Leistung; verwenden Sie Volltext nur, wenn erforderlich.
* **Sortierung und Facetten** Aktivieren Sie „propertyIndex“ und „Reihenfolge“ für die Sortierung. Legen Sie „facet** für die zahlenbasierte Filterung auf „true“ fest.

Die Anwendung dieser Strategien führt zu schnelleren Abfragen, reduzierter Ressourcennutzung und relevanteren Ergebnissen.

