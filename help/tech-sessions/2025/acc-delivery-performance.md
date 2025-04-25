---
title: Adobe Campaign Classic-Bereitstellungsleistung - Fehlerbehebung
description: In dieser Sitzung wurden wichtige Strategien zur Verbesserung der E-Mail- und SMS-Versandleistung mit Adobe Campaign behandelt. Sie löste häufig auftretende Probleme wie Bereitstellungsverzögerungen, geringen Durchsatz und langsame Transaktionen und bietet Lösungen wie Batch-Optimierung, SQL-Protokollierung und Server-Leistungsüberwachung. Zu den Best Practices für die Zustellbarkeit gehörten die ordnungsgemäße E-Mail-Authentifizierung (SPF, DKIM, DMARC), die Überwachung auf schwarzen Listen und Spam-Prüfungen. Um die Leistung zu verbessern, haben Experten saubere Workflows, Einschränkungsregeln und das Vermeiden von freigegebenen Containern empfohlen. Tipps zum SMS-Versand mit Fokus auf die ordnungsgemäße Einrichtung externer Konten und Protokollanalyse. Die Sitzung konzentrierte sich auch auf die Tracking-Validierung, die Datenbankwartung mithilfe von aufgeblähten Berichten und die Anwendung von Druck-/Ermüdungsregeln zur Steigerung der Interaktion. Eine Sitzungsaufzeichnung wird per E-Mail freigegeben und auf der Adobe Experience Site veröffentlicht.
version: Classic v7
solution: Campaign Classic v7
product: Adobe Campaign
feature: SMS, Deliverability, Troubleshooting
role: User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 2257
last-substantial-update: 2025-04-25T00:00:00Z
jira: KT-17869
source-git-commit: 373605f79b3122382e221252232a26535ff3109b
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---


# Technische Sitzungen: Adobe Campaign Classic-Bereitstellungsleistung - Fehlerbehebung

In dieser Sitzung untersuchen wir häufige Probleme, die bei der Bereitstellung einer optimalen Leistung mit Adobe Campaign Classic (ACC) auftreten können, und stellen umsetzbare Strategien zur Fehlerbehebung und Problembehebung bereit. Die Teilnehmer lernen, wie Leistungsengpässe identifiziert, Inkonsistenzen in der Versandvorbereitung/Konfiguration behoben und Best Practices implementiert werden, um eine reibungslose Kommunikation zu gewährleisten. Von der Versandoptimierung bis zur Überwindung technischer Schwierigkeiten: Dieses Webinar vermittelt den Teilnehmern das Wissen und die Tools, die zur Steigerung der Effizienz ihrer ACC-Kampagnen, zur Optimierung der Ergebnisse und zur Bereitstellung hochwertiger Kundenerlebnisse erforderlich sind.

>[!VIDEO](https://video.tv.adobe.com/v/3457826/?learn=on&enablevpops)

## Wichtige Erkenntnisse

**Herausforderungen und Lösungen beim Versand**

* Häufige Probleme sind Versandverzögerungen, Vorbereitungsfehler, blockierte Sendungen, niedrige Erfolgsraten, geringer Durchsatz, geringe Interaktion und Langsamkeit beim Versand von Transaktionen.
* Die Lösungen umfassen die Optimierung des Versand-Batching, die Überwachung der Server-Leistung, die Aktivierung der SQL-Abfrageprotokollierung, die Überprüfung von Auditprotokollen und die Sicherstellung einer ordnungsgemäßen Konfiguration der MTA- und IP-Affinitäten.

**Best Practices für die Zustellbarkeit**

* Stellen Sie eine ordnungsgemäße E-Mail-Authentifizierung sicher (SPF, DKIM, DMARC).
* Status der schwarzen Liste überwachen und Spam-auslösende Inhalte vermeiden.
* Spam-Prüfungen verwenden, um Spam-Punktzahlen vor dem Senden von E-Mails zu bewerten.

**Optimieren der Versandleistung**

* Verwenden Sie saubere Zielgruppen-Workflows und beschränken Sie Personalisierungsfelder.
* Implementieren Sie Einschränkungsregeln, Batch-Verarbeitung und Topologieregeln für Ausschlüsse und Filter.
* Vermeiden Sie die Freigabe von Containern über mehrere Kanäle hinweg, um Engpässe zu vermeiden.

**Fehlerbehebung bei Problemen mit dem SMS-Versand**

* Stellen Sie sicher, dass externe Konten eindeutig konfiguriert sind und SMS-Prozesse ausgeführt werden.
* Überprüfen Sie die SMS-Protokolle auf Fehler und überprüfen Sie die regulären Ausdrücke in den SMP-Einstellungen.
* Wenden Sie sich bei Konfigurationsproblemen an den Dienstleister.

**Langsamer Versand durch Transaktionen**

* Überwachen Sie interne und gesamte Verarbeitungszeiten.
* Stellen Sie sicher, dass die Versandgröße innerhalb der Beschränkungen liegt (60 GB für Batch, 30 GB für Ereignis).
* Überprüfen Sie Typologieregeln und Personalisierungseinstellungen.

**Tracking und Interaktion**

* Validieren von Tracking-Workflows und Server-Protokollen.
* Testen Sie benutzerdefinierte Tracking-Formeln in niedrigeren Umgebungen vor der Produktion.
* Stellen Sie sicher, dass die Tracking-Server ausgeführt werden.

**Datenbankwartung**

* Verwenden Sie aufgeblähte Berichte, um Tabellen mit hoher Aufblähung zu identifizieren und ein DB-Vakuum zu rechtfertigen.

**Allgemeine Empfehlungen**

* Verwenden Sie Druck- und Ermüdungsregeln, um unnötige E-Mails zu begrenzen.
* Segmentieren Sie große Sendungen in kleinere Batches, um die Leistung zu optimieren.