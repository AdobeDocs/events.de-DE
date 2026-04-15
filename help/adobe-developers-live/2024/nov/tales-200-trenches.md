---
title: Geschichten aus 200 Gräben
description: Stellen Sie den Erfolg von Web-Projekten sicher, indem Sie der Leistung Priorität einräumen, Google PageSpeed Insights verwenden, Schlüsselmetriken wie LCP und TBT optimieren, Ressourcen effizient verwalten und Best Practices für die Entwicklung und Bildoptimierung befolgen.
solution: Experience Manager, Experience Manager Sites
feature: Edge Delivery Services
topic: Integrations, Performance, Development
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 1321
last-substantial-update: 2024-11-27T00:00:00Z
jira: KT-16541
exl-id: 1104048d-4074-49aa-a0bc-0065fa2df505
source-git-commit: 460acb3fd1e9b29075cefa07e8d6947d2a61a314
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---

# Geschichten aus 200 Gräben

Kiran Murugulla, Senior Engineer bei Adobe, und Varun Mitra, Architekt für Adobe Experience Manager Cloud, teilen mit Ihnen die wichtigsten Erfahrungen aus über 200 abgeschlossenen Edge Delivery Services-Projekten. Entdecken Sie die Geheimnisse hinter der Bereitstellung schneller, leistungsstarker Erlebnisse mit außergewöhnlichem Core Web Vitals.


>[!VIDEO](https://video.tv.adobe.com/v/3439424/?learn=on&enablevpops)

## Community-Diskussion

Setzen Sie das Gespräch in der Adobe Developers Live-Community [Diskussion](https://adobe.ly/4fwWvvi) fort.

## Wichtige Schlussfolgerungen

* **Performance ist kritisch** Leistung, insbesondere die Geschwindigkeit von Web-Seiten, wird als Schlüsselfaktor für erfolgreiche Web-Projekte hervorgehoben. Ein primäres Ziel ist es, Leistungswerte von 100 sicherzustellen.
* **Entwicklungspraktiken**
   * Verwenden Sie Google PageSpeed Insights für kontinuierliche Tests während der Entwicklung.
   * Starten Sie Projekte mit Textbaustein-Code, der bereits 100 Punkte erreicht, um die hohe Leistung aufrechtzuerhalten.
   * Stellen Sie vor dem Zusammenführen sicher, dass Pull-Anforderungen (PRs) Leistungsstandards erfüllen.
* **Schlüsselmetriken** Konzentrieren Sie sich auf die Optimierung des LCP (Largest Contentful Paint) und der TBT (Total Blocking Time), da sie sich erheblich auf die Leistungswerte auswirken.
* **Ressourcenverwaltung**
   * Schließen Sie erforderliche Ressourcen wie Schriftarten und Skripte von Drittanbietern in die Projektquelle ein.
   * Verwenden Sie Schriftartenfallbacks, um Ladezeiten zu verbessern.
   * Verzögertes Laden nicht erforderlicher Skripte zur Verbesserung der anfänglichen Ladeleistung.
* **Bildoptimierung** Priorisieren Sie das Laden von Bildern, die sich im sichtbaren Bereich befinden, und verwenden Sie für wichtige Bilder Abrufeinstellungen mit hoher Priorität.
* **Fallstudien**
   * ***CNN.com*** Optimierte Abfrageindizes und verzögertes Laden von Google-Anzeigen, um die Leistung zu verbessern.
   * ***Herbert Homes*** Verwendete die Intersection Observer-API zum Laden von Daten beim Scrollen, um die Leistung und das Benutzererlebnis zu verbessern.
* **Best Practices**
   * Beginnen Sie mit Textbausteincode und verwenden Sie gut strukturiertes Markup.
   * Verwenden Sie erweiterte CSS-Selektoren und minimieren Sie die Manipulation von JavaScript.
   * Fokus auf mobile First-Entwicklung.
   * Stellen Sie sicher, dass die Inhaltsstrukturierung für Autoren intuitiv ist.
* **Tools** Verwenden Sie Tools wie Google Sheets und DSA, um Site-Leistungsbewertungen im Zeitverlauf zu verfolgen.
