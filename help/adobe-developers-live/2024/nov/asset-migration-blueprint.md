---
title: Assets-Migrationsplan
description: Erfahren Sie anhand der Erkenntnisse von Achim Koch, wie Sie ein veraltetes DAM zu Adobe Experience Manager Assets migrieren. Sie decken Stakeholder-Analysen, Ressourcenplanung, Datenumwandlung und Best Practices wie die Verwendung von CSV-Dateien für die Datenverarbeitung ab.
feature: Migration
topic: Migration
solution: Experience Manager, Experience Manager Assets
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 1690
last-substantial-update: 2024-11-26T00:00:00Z
jira: KT-16576
exl-id: f588055b-05c7-44df-be67-799a0e3ee1ed
source-git-commit: 946d7cd484e8c5d4358d4099b3518705cab8d4a3
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Assets-Migrationsplan

Kommen Sie zu Achim Koch, Principal Technical Architect bei Adobe, um zu erfahren, wie man ein veraltetes DAM zu Adobe Experience Manager Assets migriert. Gewinnen Sie Einblicke in die Analyse von Stakeholdern, Ressourcenplanung, Datenumwandlung und Best Practices wie die Verwendung von CSV-Dateien für die Datenverarbeitung. Erstellen Sie eine Roadmap für Ihre eigenen Adobe Experience Manager-Migrationsprojekte.

>[!VIDEO](https://video.tv.adobe.com/v/3440448/?learn=on&enablevpops&captions=ger)

## Community-Diskussion

Setzen Sie das Gespräch in der Adobe Developers Live-Community [Diskussion](https://adobe.ly/4hKHpnF) fort.

## Wichtige Erkenntnisse

* **Kein vorkonfiguriertes Tool für die Migration** Aufgrund der Vielfalt an Produkten und benutzerdefinierten Lösungen gibt es kein einzelnes Tool, das von verschiedenen Altsystemen zu Adobe Experience Manager (AEM) migrieren kann.

* **Fünf Phasen der Migration**

   * Projektplanung
   * Implementierungsplanung
   * AEM-Implementierung
   * Implementierung des Migrationsskripts
   * Migrationsausführung

* **Stakeholder-**: Die Identifizierung und Einbeziehung von Stakeholdern wie Sponsoren, Geschäftsanwendern, IT-Systemadministratoren und Legacy-Systemunterstützung ist von entscheidender Bedeutung.

* **Ressourcen- und Zeitleistenplanung** Stellen Sie sicher, dass Ressourcen verfügbar sind, und planen Sie rund um Feiertage, Spitzenzeiten und Off-Limit-Fenster.

* **Technische Planung** Dazu gehören Anforderungsanalyse, Datenumwandlung und Infrastrukturplanung.

* **Iterativer Prozess** Die Migration umfasst mehrere Iterationen der Skriptausführung, Analyse, Feedback und Anpassung.

* **Verwendung von CSV-**: CSV-Dateien werden aufgrund ihrer Benutzerfreundlichkeit und Lesbarkeit während des Migrationsprozesses bevorzugt.

* **Scripting Language** Node.js wird wegen seiner Unterstützung von CSV, AWS und HTTP und als gute Gelegenheit, JavaScript zu lernen, empfohlen.

* **Qualität und Wiederholbarkeit** Stellen Sie eine hochwertige Datenmigration sicher, behalten Sie Originaldaten und CSV-Dateien als Referenz bei und machen Sie den Prozess wiederholbar.

* **Content-Freeze** Deklarieren Sie während der Migration ein Content-Freeze, um zu verhindern, dass neue Daten hinzugefügt werden, nachdem der Snapshot erstellt wurde.

* **Tools und Tipps** Verwenden Sie Tools wie VS-Code mit der Rainbow-CSV-Erweiterung und berücksichtigen Sie die Bytereihenfolgemarkierung (BOM) für UTF-8-Textdateien.

* **Geschäftsgenehmigung** Reservieren Sie Zeit für das Testen und Einholen der offiziellen Geschäftsgenehmigung nach der Migration, um das Einfrieren von Inhalten aufzuheben.
