---
title: Fragen Sie die Fachleute - Nützliche Erweiterungen in Tags (Launch), um die Web-SDK aufzuladen.
description: Denken Sie über eine Migration Ihrer Implementierung auf die neue Adobe Web SDK nach?  Wir werden einige unserer beliebtesten Erweiterungen in der Adobe-Tags-Bibliothek durchgehen, die Ihnen dabei helfen, Ihre Datenerfassung auf die nächste Ebene zu bringen.
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

# Fragen Sie die Fachleute: Nützliche Erweiterungen in Tags (Launch), um die Web-SDK aufzuladen

Denken Sie über eine Migration Ihrer Implementierung auf die neue Adobe Web SDK nach?  Wir werden einige unserer beliebtesten Erweiterungen in der Adobe-Tags-Bibliothek durchgehen, die Ihnen dabei helfen, Ihre Datenerfassung auf die nächste Ebene zu bringen.

>[!VIDEO](https://video.tv.adobe.com/v/346610/?quality=12&learn=on)

## Fragen und Kommentare aus der Messe

### Erweiterung „Datenelement-Assistent“ von Evolytics

<br> 
**Frage** Ist die Verwendung von Evolytics aus Sicht der Datensicherheit sicher, da es sich um eine Erweiterung von Drittanbietern handelt?

**Antwort:** Ja. Sie können den Erweiterungs-Code überprüfen, wenn Sie möchten, auch speichert er keines der Daten, sondern führt lediglich eine Transformation durch.

<br> 

**Frage:** erfasst dies auch Adobe-ECID?

**Antwort:** Die Adobe-ECID wird in dieser Erweiterung nicht erfasst. Diese Erweiterung dient u. a. zum Erstellen zusätzlicher anonymer Kennungen.

**Antwort:** Die Adobe-ECID kann jedoch auf andere Weise erfasst werden. Wir teilen dies über die ExL-Notizen und die Twitter mit, da wir Links im Chat hier nicht teilen können.

<br> 

**Frage:** Die Hash-Funktion bietet verschiedene Hash-Techniken wie SHA-256 und bietet öffentliche und private Schlüssel?

**Antwort:** Jep! SHA-256 ist die Standardeinstellung

<br> 

### Allgemeine Fragen und Anmerkungen:

<br> 

**Frage:** Was klicken wir, um die Quelldateien für Erweiterungen herunterzuladen? Steht das im „3-Punkte-Menü“?

**Antwort:** Ja! Die 3 Punkte und dann Source herunterladen (aus der Katalogansicht)

<br> 

**Kommentar** Eines der Dinge, die ich wirklich mit Erweiterungen grabe, ist der zeitsparende Aspekt. Viele von ihnen tun Dinge, *Sie* mit benutzerdefiniertem Code tun könnten, aber mit einer Erweiterung müssen Sie diesen Code nicht schreiben.

**Antwort:** direkt. Und es lässt sich wiederholen, ohne dass das Rad jedes Mal neu aufgebaut werden muss.

<br> 

**Frage:** Wie werden Analytics-Plug-ins unterstützt oder durch Web SDK-Implementierungen ersetzt?

**Antwort:** Viele Analytics-Plugins sind heutzutage aufgrund der zusätzlichen Flexibilität von Workspace- und Adobe-Tags eigentlich unnötig. Wenn dies nicht der Fall ist, werden diese aktiv für die Verwendung durch die Web-SDK migriert.

<br> 

**Frage** Gibt es Entwicklungen beim Activity Map-Tracking mit Web SDK?

**Antwort:** Ich freue mich, berichten zu können, dass auch in Web SDK aktiv an Activity Map gearbeitet wird, um Unterstützung zu erhalten

<br> 

**Frage:** Wären wir in der Lage, Zugriff auf das Adobe Edge-Netzwerk zu haben, um Ereignisse zu verwalten, bevor wir sie an die Endziele übertragen? Ich verstehe, dass wir dies auch in Launch tun können, aber wäre es in Zukunft möglich, dies auch auf dem Server zu tun?

**Antwort:** Ja! Dies ist über unsere Ereignisweiterleitungsfunktion möglich, die Kunden über jedes unserer Real-Time CDP-Produkte (Real-Time CDP Connections, Prime oder Ultimate) erwerben können.

**Antwort:** RTCDP Connections (Ereignisweiterleitung) bietet die Möglichkeit, mehr Kontrolle zu haben, bevor Sie sie an Ziele senden, die nicht mit Adobe verbunden sind.

**Antwort:** Sehen Sie sich einige unserer anderen ExL Live-Videos an, um mehr darüber zu erfahren (wie [dieses](exl-live-episode-06-23-22.md)).

<br> 

**Kommentar:** Kurzaufruf für eine meiner Lieblingserweiterungen: Es gibt eine Zuordnungstabellenerweiterung, in der Sie eine Tabelle für ein Datenelement lesen können, das „wenn dieser Wert dieser ist, dann setzen Sie ihn als dieser.“

**Antwort:** Die Flexibilität, die sie bieten, ist ziemlich beeindruckend. Beachten Sie außerdem, dass Unternehmen auch eigene private Erweiterungen erstellen können, falls sie dies möchten.

<br> 

**Frage** Sie haben die einzelnen CRM-Daten wie Stadt und Wetter gezeigt. Wo speichern wir also die einzelnen Antworten?

**Antwort:** Antworten werden in jedem eindeutigen Ereignis gespeichert, das eine Regel innerhalb einer Ereignisweiterleitungs-Eigenschaft Trigger hat und nur in diesem bestimmten Ereignis verwendet wird.

<br> 

Setzen Sie die Diskussion zu diesem Thema in der [Experience League-Community-Diskussion ](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-platform/experience-league-live-post-session-discussion-useful-extensions/m-p/542620?profile.language=de#M240).
<br> 

## Zusätzliche Experience League LIVE-Sitzungen aus dieser Datenerfassungsreihe

* [Fragen an Experten - Die Grundlagen von Web SDK](exl-live-episode-05-26-22.md)
* [Fragen an Experten - RTCDP Connections](exl-live-episode-06-23-22.md)
* [Fragen an Experten - Datenströme und Datenvorbereitung](exl-live-episode-07-21-22.md)

