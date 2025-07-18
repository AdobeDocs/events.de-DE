---
title: CDN- und WAF-Konfiguration in Adobe Experience Manager as a Cloud Service
description: Verbessern Sie die Leistung und Sicherheit von Adobe Experience Manager as a Cloud Service-Anwendungen mit anpassbaren CDN-Regeln, WAF-Schutz und der Konfigurations-Pipeline, wie sie von Adobe-Experten geteilt werden.
solution: Experience Manager as a Cloud Service
feature: Security
topic: Performance, Security
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 2211
last-substantial-update: 2024-11-26T00:00:00Z
jira: KT-16574
exl-id: a9f38e79-c707-443d-8b2f-e534ce4dd43d
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# CDN- und WAF-Konfiguration in Adobe Experience Manager as a Cloud Service

Erschließen Sie das volle Potenzial von Adobe Managed CDN mit anpassbaren CDN-Regeln, WAF-Schutz und der Konfigurations-Pipeline. Marius Petria, Sr. Computer Scientist bei Adobe, Quentin Vecchio, Software Development Engineer bei Adobe, und Florian Froese, Software Development Engineer bei Adobe, teilen Strategien zur Verbesserung der Leistung und Sicherheit von Adobe Experience Manager as a Cloud Service-Anwendungen.

>[!VIDEO](https://video.tv.adobe.com/v/3440611/?learn=on&enablevpops&captions=ger)

## Community-Diskussion

Setzen Sie das Gespräch in der Adobe Developers Live-Community [Diskussion](https://adobe.ly/3O0TyYa) fort.

## Wichtigste Punkte

* **Einführung neuer Konfigurationsfunktionen** Die Präsentation führt neue Konfigurationsfunktionen für das CDN in einem Cloud-Service ein, wobei der Schwerpunkt auf der Möglichkeit liegt, das CDN für verschiedene Anwendungsfälle zu konfigurieren.
* **CDN-Konfigurationsoptionen** Die neuen Optionen ermöglichen die Interaktion mit HTTP-Anfragen und -Antworten, z. B. das Hinzufügen/Entfernen von Kopfzeilen, das Umschreiben von Anfragepfaden, das Blockieren von Traffic, das Weiterleiten von Clients und den Proxy-Vorgang an verschiedene Ursprünge.
* **Sicherheitsverbesserungen** Die neuen Funktionen umfassen Traffic-Filterregeln zum Blockieren oder Protokollieren von Traffic basierend auf Anfragemustern und die Einführung von M WAF für erweiterten Schutz vor Web-Angriffen wie SQL-Injection und XSS.
* **Deklarative Konfiguration** Die Konfiguration erfolgt mithilfe von YAML-Dateien und wird über eine Konfigurations-Pipeline in Cloud Manager bereitgestellt, was einen schnellen und einfachen Prozess ermöglicht.
* **Anfrage- und Antworttransformationen** Die neuen Funktionen ermöglichen Anfragetransformationen, um URLs zu normalisieren und unnötige Abfrageparameter zu entfernen. Außerdem ermöglichen sie Antworttransformationen, um Header festzulegen, bevor Antworten an Clients gesendet werden.
* **Traffic-Filter und Ratenbegrenzung** Traffic-Filter können bestimmte IPs oder Länder blockieren und eine Ratenbegrenzung implementieren, um sich vor DDoS-Angriffen zu schützen. Die Ratenbegrenzung kann auf Grundlage verschiedener Kriterien wie Client-IP, Benutzeragent und Anfragepfad konfiguriert werden.
* **Überwachungs- und Analyse-Tools** Adobe bietet Tools wie Elasticsearch/Kibana- und Splunk-Dashboards zur Analyse von Traffic und Nutzung, die dabei helfen, potenzielle Sicherheitsbedrohungen zu identifizieren und zu minimieren.
* **Praktische Demo** Die Präsentation enthält eine Demo, in der gezeigt wird, wie CDN-Konfigurationen mithilfe von Cloud Manager bereitgestellt werden und wie Fehler behandelt und Konfigurationen mithilfe von AEM lokal validiert werden können.
