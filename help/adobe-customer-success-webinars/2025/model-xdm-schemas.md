---
title: Best Practices und Erkenntnisse für die Modellierung von XDM-Schemata
description: Stammdatenmodellierung in AEP mit XDM-Schemata, Identitätsverwaltung und Best Practices für skalierbare Personalisierung und Segmentierung in Echtzeit.
solution: Experience Platform
topic: Personalization
role: Developer
level: Intermediate
doc-type: Event
duration: 3488
last-substantial-update: 2025-05-08T00:00:00Z
jira: KT-18019
exl-id: 3327dc51-b5e4-49bd-884a-4defea8664eb
source-git-commit: ef1eacd73c5a4fb9cdfee730d40606ec65bab2a7
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Best Practices und Erkenntnisse für die Modellierung von XDM-Schemata

In dieser Sitzung erfahren Sie mehr über die wichtigsten Best Practices und Tastaturbefehle zum Erstellen skalierbarer, hochwertiger Adobe Experience-Datenmodelle (XDM), die mit Adobe Experience Platform-Standards übereinstimmen. Gewinnen Sie Einblicke in die effektive Zuordnung von Kundenerlebnis- und Anwendungsfalldaten zu XDM, um eine nahtlose Integration über Adobe und externe Tools hinweg zu ermöglichen.

## Diskussionspunkte

* Definieren und Organisieren von XDM-Komponenten, um skalierbare und flexible Datenmodelle sicherzustellen
* Häufige Herausforderungen beim Design, der Weiterentwicklung und der Wartung von XDM

>[!VIDEO](https://video.tv.adobe.com/v/3458042/?learn=on&enablevpops)

## Wichtige Erkenntnisse

**Datenmodellierung in Adobe Experience Platform (AEP)**

Das XDM-Schema ist die Grundlage für die Datenmodellierung in AEP und ermöglicht die Integration und Freigabe von Daten über verschiedene Systeme hinweg. Sie definiert die Struktur und Bedeutung von Daten wie Profilattribute und ereignisbasierte Aktionen.

**Identity Management**

Eine ordnungsgemäße Identitätsverwaltung ist von entscheidender Bedeutung, um Probleme wie den Profilzusammenbruch zu vermeiden. Das Hashing sensibler Daten wie E-Mails und die Verwendung eindeutiger Kennungen können helfen, die Datenintegrität aufrechtzuerhalten. Identitätszuordnungen werden für die Echtzeit-Segmentierung und Personalisierung empfohlen.

**Best Practices für das Schema-Design**

Halten Sie Schemata einfach und konzentrieren Sie sich auf Marketing-Anwendungsfälle. Vermeiden Sie das Überladen von Schemata mit unnötigen Attributen. Verwenden Sie standardisierte Feldergruppen und minimieren Sie Anpassungen für Skalierbarkeit und Zukunftssicherheit.

**Ereignis- vs. Profilattribute**

Entscheiden Sie, ob Daten basierend auf Marketing-Zielen als Profilattribute oder Ereignisse modelliert werden sollen. Profilattribute eignen sich für die Zielgruppenbestimmung in Echtzeit, während Ereignisse historische Einblicke für die zeitbasierte Segmentierung bieten.

**Umgang mit ausgeblendeten Profilen und Skalierbarkeit**

Reduzierte Profile können nur durch die Adobe-Unterstützung behoben werden, aber Regeln für Identitätsdiagramme können zukünftige Reduzierungen verhindern. Für die Neustrukturierung vorhandener Schemata wird empfohlen, die erforderlichen Daten zu extrahieren und neu mit einem sauberen Schema zu beginnen.
