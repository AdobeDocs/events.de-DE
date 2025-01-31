---
title: AEM GEMs - Erste Schritte mit Adobe-verwaltetem CDN
description: Erfahren Sie, wie Sie das von Adobe verwaltete CDN in AEM Cloud Service konfigurieren, um die Leistung und Sicherheit mit neuen CDN-Konfigurationsfunktionen zu verbessern.
role: Developer, User
level: Intermediate
doc-type: Event
duration: 3438
last-substantial-update: 2025-01-30T00:00:00Z
jira: KT-17227
source-git-commit: 1cfa9cdb0e973e6d088b1faeaa63539b0a7fba36
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---


# AEM GEMs - Erste Schritte mit Adobe-verwaltetem CDN

Erfahren Sie mehr über das von Adobe verwaltete CDN in AEM Cloud Service und dessen Konfiguration. Erkunden Sie gemeinsam mit uns die neuen CDN-Konfigurationsfunktionen, mit denen Sie sowohl die Leistung als auch die Sicherheit Ihrer AEM as a Cloud Service-Programme verbessern können. In dieser Sitzung werden Sie Folgendes entdecken:

* Was ist das Adobe-CDN?
* Relevante Topologien für AEMaaCS und Edge Delivery Services
* Typische Anwendungsfälle, die mit CDN-Regeln implementiert werden können
* Verwenden von RDEs zum schnellen Testen und Bereitstellen von CDN-Konfigurationen

>[!VIDEO](https://video.tv.adobe.com/v/3443168/?learn=on&enablevpops)

*Aufgenommen am 22. Januar 2025*

Haben Sie eine Frage, vielleicht einen Kommentar?  Beteiligen Sie sich an der Diskussion in den [Experience League Communities](https://adobe.ly/4haufPK)!

## Wichtige Erkenntnisse

### Wichtigste Funktionen von Adobe Managed CDN

* **Benutzerdefinierte Domains und Zertifikate:** für das Hosten benutzerdefinierter Domains und Zertifikate zum Herstellen sicherer Verbindungen erforderlich.
* **Caching** Die Bereitstellung von HTTP-Antworten aus dem Cache ist deutlich schneller (unter 10 Millisekunden) als der Abruf aus der Quelle (Hunderte von Millisekunden).
* **Standardmäßiges und benutzerdefiniertes CDN** Adobe bietet ein vorkonfiguriertes verwaltetes CDN, Benutzende können jedoch auch ihr eigenes CDN mitbringen.

### Konfigurationsoptionen

* **Anforderungstransformationen** Ändern von Kopfzeilen, Neuschreiben von Pfaden, Blockieren von Traffic und Umleitungsanfragen.
* **Traffic-Filter** Blockieren oder Zulassen von Traffic basierend auf bestimmten Regeln.
* **Authentifizierung** Unterstützung für Edge-Schlüssel, Punch-Schlüssel und Standardauthentifizierung.
* **Origin-Selektoren** Proxy-Anfragen an verschiedene Ursprünge basierend auf definierten Regeln.
* **Antworttransformationen** Ändern Sie Antwortkopfzeilen und -status.

### Bereitstellung und Anpassung

* **Konfigurations-Pipeline** Bereitstellen von YAML-Dateien zum Konfigurieren von CDN-Regeln.
* **Traffic-Schutz** Verwenden Sie Traffic-Filterregeln, um Traffic basierend auf Mustern zu blockieren, zu protokollieren und zu warnen.
* **Ratenbegrenzung** Protect gegen DDoS-Angriffe durch Begrenzung der Anzahl der Anfragen pro IP.

### Tools und Analyse

* **Elasticsearch-Kibana** Stapel, Nutzung und Traffic mit bereitgestellten Dashboards analysieren.
* **Protokollweiterleitung** Leiten Sie Protokolle zur Analyse an eine Splunk-Instanz weiter.

### Demo-Highlights

* **Konfigurationen bereitstellen** Demonstration der Bereitstellung von Traffic-Filterregeln und Umleitungen.
* **Authentifizierung und Ursprungsauswahl** Es wurde gezeigt, wie die einfache Authentifizierung und der Proxy-Traffic für verschiedene Ursprünge eingerichtet werden.

### Best Practices

* **Schnelle Antworten** Stellen Sie schnelle Antworten von den Ursprüngen sicher, um Sicherheitslücken zu vermeiden.
* **Gute Zwischenspeicherung** Nutzen Sie die Zwischenspeicherung, um Traffic effizient zu verarbeiten.
* **Verwenden von Dashboards** Analysieren des Traffics und der Nutzung, um geeignete Ratenbeschränkungen festzulegen.
* **Kombinieren Sie Strategien** Verwenden Sie verschiedene Ratenbegrenzungsstrategien für einen besseren Schutz.
* **Warnhinweise festlegen** Werde benachrichtigt, wenn die Site angegriffen wird.
* **Testregeln** Beginnen Sie mit der Protokollierung von Aktionen, bevor Sie sie blockieren, um sicherzustellen, dass die Regeln erwartungsgemäß funktionieren.

### Kontakt und Feedback

* **Feedback und Anwendungsfälle** Wenden Sie sich an das Team, um erweiterte Anwendungsfälle und Feedback zu erhalten.
* **Future Sessions** Nehmen Sie an Umfragen teil, um Themen für zukünftige Sitzungen vorzuschlagen.