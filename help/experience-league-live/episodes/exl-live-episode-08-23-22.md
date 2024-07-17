---
title: Bitten Sie die Experten um nützliche Erweiterungen in Tags (Launch), das Web SDK zu überlasten.
description: Denken Sie an die Migration Ihrer Implementierung zum neuen Adobe Web SDK?  Wir werden einige unserer beliebtesten Erweiterungen in der Adobe-Tags-Bibliothek durchlaufen, die Ihnen dabei helfen, Ihre Datenerfassung auf die nächste Ebene zu bringen.
solution: Data Collection, Experience Platform
feature: Tags
kt: 10528
event-start-time: 2022-08-23 09:00-7
event-guests: Rudi Shumpert,Jeff Chasin,Eric Matisoff
exl-id: 5ef987f4-37f5-473f-b9f2-1598b7e655ba
duration: 3833
source-git-commit: 0b2f63198af8767f24783dbafd244c9398c24f33
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---

# Fragen Sie die Experten: Nützliche Erweiterungen in Tags (Launch), um das Web SDK zu überlasten.

Denken Sie an die Migration Ihrer Implementierung zum neuen Adobe Web SDK?  Wir werden einige unserer beliebtesten Erweiterungen in der Adobe-Tags-Bibliothek durchlaufen, die Ihnen dabei helfen, Ihre Datenerfassung auf die nächste Ebene zu bringen.

>[!VIDEO](https://video.tv.adobe.com/v/346610/?quality=12&learn=on)

## Fragen und Kommentare zur Sendung

### Data Element Assistant-Erweiterung von Evolytics

<br> 
**Frage:** Ist die Verwendung von Evolytics aus datensicherheitsbezogener Sicht sicher, da es sich um eine Drittanbietererweiterung handelt?

**Antwort:** Ja. Sie können den Erweiterungscode überprüfen, falls Sie möchten. Außerdem speichert er keines der Datumswerte, sondern führt nur eine Umwandlung durch.

<br> 

**Frage:** Erfasst diese Adobe ECID auch?

**Antwort:** Die Adobe ECID wird in dieser Erweiterung nicht erfasst. Diese Erweiterung ist für die Erstellung zusätzlicher anonymer Kennungen vorgesehen (unter anderem).

**Antwort:** Die Adobe ECID kann jedoch auf andere Weise erfasst werden. Wir werden dies über die ExL-Notizen und Twitter teilen, da wir keine Links im Chat hier freigeben können.

<br> 

**Frage:** Die Hash-Funktion bietet verschiedene Hash-Techniken wie SHA-256 und stellt öffentliche und private Schlüssel bereit?

**Antwort:** Ja! SHA-256 ist die Standardeinstellung

<br> 

### Allgemeine Fragen und Kommentare:

<br> 

**Frage:** Was klicken wir, um die Quelldateien für Erweiterungen herunterzuladen? Ist das im &quot;3-Punkt-Menü&quot;?

**Antwort:** Ja! Die 3 Punkte, dann Source herunterladen (aus der Katalogansicht)

<br> 

**Kommentar:** Eines der Dinge, die ich wirklich mit Erweiterungen durchsuche, ist der zeitsparende Aspekt dieser Erweiterungen. Viele von ihnen machen Dinge, die Sie *könnten* mit benutzerdefiniertem Code tun, aber mit einer Erweiterung müssen Sie diesen Code nicht schreiben.

**Antworten:** Rechts ein. Und es ist wiederholbar, ohne jedes Mal das Rad neu erschaffen zu müssen.

<br> 

**Frage:** Wie werden Analytics-Plug-ins unterstützt oder durch Web SDK-Implementierungen ersetzt?

**Antwort:** Viele Analytics-Plug-ins sind heutzutage aufgrund der zusätzlichen Flexibilität von Workspace und Adobe-Tags eigentlich nicht mehr erforderlich. Diese werden jedoch aktiv für die Verwendung durch das Web SDK migriert.

<br> 

**Frage:** Jegliche Entwicklung beim Activity Map-Tracking mit dem Web SDK?

**Antwort:** Ich freue mich, berichten zu können, dass Activity Map aktiv für die Unterstützung im Web SDK arbeitet.

<br> 

**Frage:** Können wir Zugriff auf das Adobe Edge-Netzwerk haben, um Ereignisse zu verwalten, bevor sie an die Endziele übertragen werden? Ich weiß, dass wir dies auch in Launch tun können, aber wäre es in Zukunft auch auf dem Server möglich?

**Antwort:** Ja! Dies ist über unsere Funktion zur Ereignisweiterleitung möglich, die Kunden über beliebige Real-Time CDP-Produkte (Real-Time CDP Connections, Prime oder Ultimate) erwerben können.

**Antwort:** RTCDP-Verbindungen (Ereignisweiterleitung) bieten die Möglichkeit, mehr Kontrolle zu haben, bevor Sie sie an Nicht-Adobe-Ziele senden.

**Antwort:** Sehen Sie sich einige unserer anderen ExL-Live-Videos an, um mehr darüber zu erfahren (z. B. [dieses ](exl-live-episode-06-23-22.md)).

<br> 

**Kommentar:** Schnellaufruf für eine meiner Lieblingserweiterungen: Es gibt eine Zuordnungstabelle-Erweiterung, in der Sie eine Tabelle für ein Datenelement lesen können, das &quot;Wenn dieser Wert dieser Wert ist, legen Sie ihn als diesen Wert fest.&quot;

**Antwort:** Die Flexibilität, die sie bieten, ist ziemlich beeindruckend. Beachten Sie auch, dass Unternehmen ihre eigenen privaten Erweiterungen erstellen können, wenn sie dies wünschen.

<br> 

**Frage:** Sie haben die individuellen Daten aus CRM-Systemen wie Stadt und Wetter angezeigt. Wo speichern wir also die individuelle Antwort?

**Antwort:** Antworten werden in jedem eindeutigen Ereignis gespeichert, das eine Regel in einer Ereignisweiterleitungseigenschaft Trigger, und nur in diesem bestimmten Ereignis verwendet.

<br> 

Fahren Sie mit der Diskussion über dieses Thema in der [Experience League Community-Diskussion](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-platform/experience-league-live-post-session-discussion-useful-extensions/m-p/542620#M240) fort.
<br> 

## Zusätzliche Experience League LIVE-Sitzungen aus dieser Datenerfassungsreihe

* [Experten fragen - Grundlagen des Web SDK](exl-live-episode-05-26-22.md)
* [Fragen Sie die Experten - RTCDP-Verbindungen](exl-live-episode-06-23-22.md)
* [Experten fragen - Datenspeicher und Datenvorbereitung](exl-live-episode-07-21-22.md)

