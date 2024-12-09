---
title: Optimieren der Inhaltsbereitstellung - Entsperren der Leistung von Edge Services
description: ATM Edge Delivery Services (EDS) verbessert ATM Funktionen durch zusammenstellbare Dienste, schnelle Entwicklungszyklen und hohe Lightthouse-Werte, unterstützt dokumentbasierte und WYSIWYG-Bearbeitung, Server-lose Architektur, schnelle Site-Erstellung und umfangreiche Anpassungsoptionen.
solution: Experience Manager, Experience Manager as a Cloud Service
feature: Edge Delivery Services
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3589
last-substantial-update: 2024-12-06T00:00:00Z
jira: KT-16631
source-git-commit: 47ae42d06ed311e60ebce194e0683bb95e8e5b69
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Optimieren der Inhaltsbereitstellung: Entsperren der Leistung von Edge Services

In dieser Sitzung werden wir einen Überblick über Edge Delivery Services (EDS) und deren Architektur geben. Wir werden uns mit der Integration von EDS in dokumentbasiertes Authoring und AEM-basiertes Authoring über den universellen Editor beschäftigen. In einer Live-Demo wird EDS in Aktion vorgestellt, gefolgt von Ressourcen für die weitere Erforschung und einer Q&amp;A-Sitzung.

>[!VIDEO](https://video.tv.adobe.com/v/3440938/?learn=on&enablevpops)

## Wichtige Schritte

### Einführung in das EDS

* EDS ist ein Set zusammenstellbarer Dienste, die die Fähigkeiten von ATM verbessern sollen. &#x200B;
* Ziel ist es, außergewöhnliche Erlebnisse bereitzustellen, die Interaktionen und Konversionen mit schnellen Entwicklungszyklen und einem 100-%-Lightthouse-Ergebnis fördern. &#x200B;

### Authoring-Optionen

* **Dokumentenbasiertes Authoring** Verwendet vertraute Tools wie Microsoft Word- oder Google-Dokumente für die Inhaltserstellung und ermöglicht so die schnelle Inhaltserstellung ohne umfangreiche Schulungen. &#x200B;
* **Universal Editor** Stellt eine WYSIWYG-Oberfläche bereit, die herkömmlichen ATM-Sites ähnelt und eine detailliertere und visuellere Inhaltserstellung ermöglicht. &#x200B;

### Architektur

* EDS ist in das Amazon Cloud Service-Framework integriert. &#x200B;
* Es unterstützt eine Server-lose Implementierung und kann ohne eine herkömmliche Autoren- oder Herausgeberinstanz funktionieren. &#x200B;
* Es können zwei Ebenen der Zwischenspeicherung implementiert werden: auf der Ebene der Kundeninfrastruktur und auf der Ebene des EDS. &#x200B;

### Content-Management

* Für das dokumentbasierte Authoring sind ein GitHub-Konto, Google Drive oder Microsoft SharePoint, ein Sidekick-Plug-in und ein Tool zur Codesynchronisierung erforderlich. &#x200B;
* Für EDS mit IAM-Authoring sind ein GitHub-Konto, eine IAM as a Cloud Service-Lizenz und ein Tool zur Code-Synchronisierung erforderlich.

### Entwicklung und Implementierung

* Die Erstellung einer Website mit EDS erfolgt schnell und dauert oft weniger als einen Tag. &#x200B;
* Die lokale Entwicklung kann mithilfe des Befehls aem-up durchgeführt werden, um eine lokale Version der Website zu erstellen.
* Änderungen können zu Testzwecken an Funktionsverzweigungen übertragen werden, bevor sie in die Hauptverzweigung zusammengeführt werden. &#x200B;

### Anpassen und Erweiterbarkeit

* Benutzerdefinierte Komponenten können mit einfachem CSS und JavaScript erstellt werden. &#x200B;
* Die Architektur ermöglicht Integrationen von Drittanbietern und benutzerdefinierte Authoring-Quellen.

### Best Practices

* Es wird empfohlen, Vanilla JavaScript und CSS zu verwenden, um hohe Leuchtturmwerte zu erzielen.
* Jede Einführung von Bibliotheken wie React sollte sorgfältig geprüft und getestet werden, um eine Leistungsbeeinträchtigung zu vermeiden.

### Support und Dokumentation

* Es steht eine umfassende Dokumentation zur Verfügung, die Benutzer durch den Einrichtungs- und Anpassungsprozess führt. &#x200B;
* Benutzer sollten sich für alle ungelösten Probleme an den Adobe-Support wenden. &#x200B;