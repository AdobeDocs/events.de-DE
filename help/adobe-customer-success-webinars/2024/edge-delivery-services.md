---
title: Optimierung der Inhaltsbereitstellung - Erschließen der Leistungsfähigkeit von Edge Services
description: ATM Edge Delivery Services (EDS) erweitert die ATM-Funktionen durch zusammenstellbare Services, schnelle Entwicklungszyklen und hohe Punktzahlen. Unterstützt werden das dokumentbasierte und WYSIWYG-Authoring, Server-lose Architektur, die schnelle Site-Erstellung und umfangreiche Anpassungsoptionen.
solution: Experience Manager, Experience Manager as a Cloud Service
feature: Edge Delivery Services
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3589
last-substantial-update: 2024-12-06T00:00:00Z
jira: KT-16631
exl-id: 2057e491-9ec3-4bfe-b85a-6b74d70822bf
source-git-commit: 1387be704e6b6dc1a7446e409da7da81403fdc3c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Optimierung der Inhaltsbereitstellung: Die Leistungsfähigkeit von Edge Services nutzen

In dieser Sitzung geben wir einen Überblick über Edge Delivery Services (EDS) und seine Architektur. Wir werden uns damit befassen, wie EDS mit der dokumentbasierten und AEM-basierten Inhaltserstellung über den universellen Editor integriert wird. In einer Live-Demo wird EDS in Aktion gezeigt, gefolgt von Ressourcen für weitere Untersuchungen und einer Fragerunde.

>[!VIDEO](https://video.tv.adobe.com/v/3440938/?learn=on&enablevpops)

## Wichtige Erkenntnisse

### Einführung in EDS

* EDS ist eine Reihe zusammenstellbarer Services, die die Funktionen von ATM verbessern sollen. &#x200B;
* Ziel ist es, außergewöhnliche Erlebnisse zu bieten, die Interaktion und Konversionen mit schnellen Entwicklungszyklen und einem 100 %-Lighthouse-Wert fördern. &#x200B;

### Authoring-Optionen

* **Dokumentenbasiertes Authoring** Verwendet vertraute Tools wie Microsoft Word oder Google Docs für die Inhaltserstellung, was eine schnelle Inhaltserstellung ohne umfangreiche Schulung ermöglicht. &#x200B;
* **Universeller Editor** Bietet eine WYSIWYG-Schnittstelle, die herkömmlichen ATM-Sites ähnelt und eine detailliertere und visuellere Inhaltserstellung ermöglicht. &#x200B;

### Architektur

* EDS ist in das Amazon Cloud Service-Framework integriert. &#x200B;
* Es unterstützt eine Server-lose Implementierung und kann ohne eine herkömmliche Autoren- oder Veröffentlichungsinstanz ausgeführt werden. &#x200B;
* Es können zwei Ebenen der Zwischenspeicherung implementiert werden: auf der Ebene der Kundeninfrastruktur und auf der Ebene des EDS. &#x200B;

### Content-Management

* Für das dokumentbasierte Authoring sind ein GitHub-Konto, Google Drive oder Microsoft SharePoint, ein Sidekick-Plug-in und ein Tool zur Codesynchronisierung erforderlich. &#x200B;
* EDS mit IAM-Authoring erfordert ein GitHub-Konto, eine Lizenz für IAM as a Cloud Service und ein Code-Synchronisierungs-Tool.

### Entwicklung und Bereitstellung

* Der Prozess der Erstellung einer Website mit EDS ist schnell, dauert oft weniger als einen Tag. &#x200B;
* Die lokale Entwicklung kann mit dem AEM-Befehl up durchgeführt werden, um eine lokale Version der Website zu erstellen.
* Änderungen können an Funktionsverzweigungen zum Testen übertragen werden, bevor sie in die Hauptverzweigung zusammengeführt werden. &#x200B;

### Anpassung und Erweiterbarkeit

* Benutzerdefinierte Komponenten können mit einfachen CSS- und JavaScript-Elementen erstellt werden. &#x200B;
* Die Architektur ermöglicht Drittanbieterintegrationen und benutzerdefinierte Authoring-Quellen.

### Best Practices

* Es wird empfohlen, Vanilla JavaScript und CSS zu verwenden, um hohe Lighthouse-Werte zu erzielen.
* Jede Einführung von Bibliotheken wie React sollte sorgfältig geprüft und getestet werden, um eine Beeinträchtigung der Leistung zu vermeiden.

### Support und Dokumentation

* Eine umfassende Dokumentation steht zur Verfügung, um Benutzende durch den Einrichtungs- und Anpassungsprozess zu führen. &#x200B;
* Benutzende sollten sich bei ungelösten Problemen an den Adobe-Support wenden. &#x200B;
