---
title: CDN- und WAF-Konfiguration in Adobe Experience Manager as a Cloud Service
description: Verbessern Sie die Leistung und Sicherheit von Adobe Experience Manager as a Cloud Service-Anwendungen mit anpassbaren CDN-Regeln, WAF-Schutz und der Config Pipeline, wie von Adobe-Experten gemeinsam genutzt.
feature: Security
topic: Performance, Security
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 2211
last-substantial-update: 2024-11-26T00:00:00Z
jira: KT-16574
exl-id: a9f38e79-c707-443d-8b2f-e534ce4dd43d
source-git-commit: 946d7cd484e8c5d4358d4099b3518705cab8d4a3
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# CDN- und WAF-Konfiguration in Adobe Experience Manager as a Cloud Service

Das gesamte Potenzial von Adobe verwaltetem CDN mit anpassbaren CDN-Regeln, WAF-Schutz und der Config Pipeline wird freigeschaltet. Marius Petria, Sr. Computer Scientist bei Adobe, Quentin Vecchio, Software Development Engineer bei Adobe, und Florian Froese, Software Development Engineer bei Adobe, teilen Strategien zur Verbesserung der Leistung und Sicherheit von Adobe Experience Manager as a Cloud Service-Anwendungen.

>[!VIDEO](https://video.tv.adobe.com/v/3440401/?learn=on&enablevpops)

## Community-Diskussion

Fahren Sie mit der Unterhaltung in der Adobe Developers Live Community [diskussion](https://adobe.ly/3O0TyYa) fort.

## Wichtigste Punkte

* **Einführung neuer Konfigurationsfunktionen** Mit der Präsentation werden neue Konfigurationsfunktionen für das CDN in einem Cloud-Service eingeführt, wobei der Schwerpunkt auf der Möglichkeit liegt, das CDN für verschiedene Anwendungsfälle zu konfigurieren.
* **CDN-Konfigurationsoptionen** Die neuen Optionen ermöglichen die Interaktion mit HTTP-Anforderungen und -Antworten, z. B. Hinzufügen/Entfernen von Kopfzeilen, Umschreiben von Anfragepfaden, Blockieren von Traffic, Umleiten von Clients und Proxing zu unterschiedlichen Quellen.
* **Verbesserungen der Sicherheit** Zu den neuen Funktionen gehören Traffic-Filterregeln zum Blockieren oder Protokollieren von Traffic auf der Grundlage von Anforderungsmustern sowie die Einführung von M WAF für erweiterten Schutz vor Web-Angriffen wie SQL-Injection und XSS.
* **Deklarative Konfiguration** Die Konfiguration erfolgt mithilfe von YAML-Dateien und wird über eine Konfigurations-Pipeline in Cloud Manager bereitgestellt, wodurch sie schnell und unkompliziert ausgeführt wird.
* **Anforderungs- und Antwortumwandlungen** Die neuen Funktionen ermöglichen Anforderungsumwandlungen zum Normalisieren von URLs und zum Entfernen unnötiger Abfrageparameter und Antworttransformationen, um Kopfzeilen festzulegen, bevor Antworten an Clients gesendet werden.
* **Traffic-Filter und Ratenbegrenzung** Traffic-Filter können bestimmte IPs oder Länder blockieren und Ratenbegrenzungen implementieren, um den Schutz vor DDoS-Angriffen zu gewährleisten. Die Ratenbegrenzung kann anhand verschiedener Kriterien wie Client-IP, Benutzeragent und Anfragepfad konfiguriert werden.
* **Monitoring- und Analyse-Tools** Adobe bietet Tools wie Elasticsearch/Kibana- und Splunk-Dashboards, um Traffic und Nutzung zu analysieren und so potenzielle Sicherheitsbedrohungen zu identifizieren und zu minimieren.
* **Praktische Demo** Die Präsentation enthält eine Demo, in der gezeigt wird, wie CDN-Konfigurationen mit Cloud Manager bereitgestellt werden und wie Fehler behandelt und Konfigurationen lokal mithilfe von AEM validiert werden.
