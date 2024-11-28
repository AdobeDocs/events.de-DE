---
title: Assets-MigrationsBlueprint
description: Erfahren Sie, wie Sie ein Legacy-DAM mit Einblicken von Achim Koch in Adobe Experience Manager Assets migrieren können. Diese Einblicke umfassen die Analyse von Interessenträgern, die Ressourcenplanung, die Datenumwandlung und Best Practices wie die Verwendung von CSV-Dateien für die Datenverarbeitung.
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

# Assets-MigrationsBlueprint

Schließen Sie sich Achim Koch, Technischer Hauptarchitekte bei der Adobe an, um zu erfahren, wie Sie ein veraltetes DAM nach Adobe Experience Manager Assets migrieren können. Erhalten Sie Einblicke in die Analyse von Stakeholdern, Ressourcenplanung, Datenumwandlung und Best Practices wie die Verwendung von CSV-Dateien für die Datenverarbeitung. Erstellen Sie eine Roadmap für Ihre eigenen Adobe Experience Manager-Migrationsprojekte.

>[!VIDEO](https://video.tv.adobe.com/v/3440403/?learn=on&enablevpops)

## Community-Diskussion

Fahren Sie mit der Unterhaltung in der Adobe Developers Live Community [diskussion](https://adobe.ly/4hKHpnF) fort.

## Wichtige Schritte

* **Kein natives Migrationswerkzeug** Es gibt kein einzelnes Tool, das aufgrund der Vielfalt von Produkten und benutzerdefinierten Lösungen von verschiedenen älteren Systemen zu Adobe Experience Manager (AEM) migriert werden kann.

* **Fünf Migrationsphasen**

   * Projektplanung
   * Implementierungspläne
   * AEM Implementierung
   * Implementierung des Migrationsskripts
   * Migrationsausführung

* **Einbeziehung der Interessenträger** Es ist von entscheidender Bedeutung, Interessengruppen wie Sponsoren, Geschäftsbenutzer, IT-Systemadministratoren und Unterstützung älterer Systeme zu identifizieren und einzubinden.

* **Ressourcen- und Timeline-Planung** Stellen Sie sicher, dass Ressourcen zur Verfügung stehen und planen Sie sie um Feiertage, maximale Geschäftszeiten und Off-Limit-Fenster.

* **Technische Planung** Dies umfasst die Anforderungsanalyse, Datenumwandlung und Infrastrukturplanung.

* **Iterativer Prozess** Die Migration umfasst mehrere Iterationen der Skriptausführung, Analyse, Feedback und Anpassung.

* Die Verwendung von CSV-Dateien **CSV-Dateien wird empfohlen, um sie während des Migrationsprozesses benutzerfreundlich und lesbar zu machen.**

* **Skriptsprache** Node.js wird empfohlen, um CSV, AWS und HTTP zu unterstützen und JavaScript zu lernen.

* **Qualität und Wiederholbarkeit** Stellen Sie eine hochwertige Datenmigration sicher, behalten Sie Originaldaten und CSV-Dateien zur Referenz bei und machen Sie den Prozess wiederholbar.

* **Content Freeze** Deklarieren Sie während der Migration einen Inhaltsfrieren, um zu verhindern, dass neue Daten hinzugefügt werden, nachdem der Schnappschuss erstellt wurde.

* **Tools und Tipps** Verwenden Sie Tools wie VS Code mit der Rainbow CSV-Erweiterung und berücksichtigen Sie die BOM (Byte Order Marker) für UTF-8-Textdateien.

* **Genehmigung für Unternehmen** Reservieren Sie Zeit für Tests und den Erhalt der offiziellen Genehmigung für das Unternehmen nach der Migration, um das Einfrieren des Inhalts zu erhöhen.
