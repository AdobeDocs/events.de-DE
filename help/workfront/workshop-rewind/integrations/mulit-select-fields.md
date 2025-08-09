---
title: Einfaches Navigieren in der Workfront-API und durch Fusion-Änderungen für Mehrfachauswahlfelder
description: Erfahren Sie mehr über bevorstehende Adobe Workfront-API- und Fusion-Änderungen, einschließlich Updates für mehrere Auswahlfelder, Ereignisabonnement-Versionierung und Strategien zur Verhinderung umwälzender Änderungen.
feature: Workfront API, Workfront Fusion, Workfront Integrations and Apps
topic: Integrations
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 3172
last-substantial-update: 2025-08-08T00:00:00Z
jira: KT-18631
source-git-commit: 6225f36c5d26ecca5ebc2aca24a2d592a3279570
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---


# Einfaches Navigieren in der Workfront-API und durch Fusion-Änderungen für Mehrfachauswahlfelder

Dieser Workshop wurde am 25. Juni 2025 aufgezeichnet und beinhaltete Andy Hess, der die bevorstehenden Änderungen an der Workfront-API und Fusion teilte.

>[!VIDEO](https://video.tv.adobe.com/v/3469978/?learn=on&enablevpops)

## Ressourcen

Neben der On-Demand-Aufzeichnung haben wir auch das Dia-Deck und weitere Ressourcen hinzugefügt:
* [Slide Deck PDF](https://workfront-experience.s3.us-west-2.amazonaws.com/Training/Guides/Customer+Success+at+Scale/Navigating+the+API+and+Fusion+Changes+for+Multi-Select+Fields+with+Ease+062425.pdf)
* Ein Event, das in Zusammenarbeit mit dem Adobe Software Development Team gehostet wird, wurde Anfang Mai zu den Änderungen an den Ereignisabonnements durchgeführt, wenn Sie mehr zu diesem spezifischen Bereich erfahren möchten, [[Ereignisnachbereitung] Beibehalten Ihrer Fusion-Szenarien während des Upgrades auf Event Subscriptions V2](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/m-p/754182?profile.language=de#M4041)

## Wichtige Erkenntnisse und Ressourcen

* Änderungen an den Workfront-API-Mehrfachauswahlfeldern sind in Version 21 (Oktober 2025) geplant, um ein konsistentes JSON-Array-Format anstelle von gemischten String-/Array-Antworten sicherzustellen
* Die Versionierung von Ereignisabonnements wird eingeführt - Version 2 gibt immer Felder mit Mehrfachauswahl als Arrays zurück, während Version 1 das aktuelle inkonsistente Verhalten beibehält
* Für neue Ereignisabonnements wird standardmäßig automatisch Version 2 verwendet. Alle Abonnements werden automatisch Mitte Januar 2026 auf Version 2 aktualisiert
* Eine neue Workfront-Connector-Version wird im Laufe dieses Jahres mit einem manuellen Upgrade-Prozess veröffentlicht, um die Modulzuordnung beizubehalten und laufenden Änderungen vorzubeugen
* Der Fusion AI-Assistent ist derzeit verfügbar, erfordert jedoch eine unterzeichnete KI-Vereinbarung und eine ordnungsgemäße Lizenzeinrichtung. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben oder mehr erfahren möchten. [ Informationen zur Verwendung von KI in Fusion](https://experienceleague.adobe.com/de/docs/workfront-fusion/using/manage-scenarios/fusion-ai-assistant)
* [Derzeit verfügbare Workfront Fusion-Vorlagen](https://experienceleague.adobe.com/de/docs/workfront-fusion/using/create-and-manage-templates/currently-available-fusion-templates)
* [Call for Fusion-Vorlagen](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/call-for-fusion-template-ideas/m-p/732085?profile.language=de#M3686)- Wenn Sie Vorschläge für neue Fusion-Vorlagen haben, fügen Sie diese hier hinzu! Hier holt das Team Ideen hervor  

Wenn Sie weitere Fragen haben, beantworten Sie bitte diesen [Experience League Community Post](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-navigating-the-workfront-api-and-fusion-changes/td-p/761253?profile.language=de)! 

Wir hoffen, Sie bei zukünftigen Customer Success-Workshops begrüßen zu dürfen!  Sehen Sie sich unbedingt die [Workfront Events](https://experienceleague.adobe.com/events/?lang=de&filters=Workfront) auf Experience League an, um die vollständige Liste zu erhalten und sich zu registrieren.