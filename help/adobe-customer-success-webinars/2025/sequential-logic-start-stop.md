---
title: Beherrschen der sequenziellen Logik in Adobe Analytics und Customer Journey Analytics - Startet und Stoppt
description: Beherrschen Sie die sequenzielle Logik in Adobe Analytics mit erweiterter Segmentierung, Umfangskontrollen und abgeleiteten Feldern, um Kundenverhaltensmuster zu erkennen und die Datengenauigkeit zu verbessern.
solution: Analytics, Customer Journey Analytics
role: Developer
level: Intermediate
doc-type: Event
duration: 3370
last-substantial-update: 2025-05-08T00:00:00Z
jira: KT-18017
source-git-commit: cfc7b54ae4360779ca2c41f88fc08089bae99165
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---


# Meistern der sequenziellen Logik in Adobe Analytics und Customer Journey Analytics: Startet und stoppt

In dieser Sitzung erkunden wir, wie Sequenzen mit dem THEN-Operator in Adobe Analytics (AA) und Customer Journey Analytics (CJA) konfiguriert werden. Erfahren Sie, wie Sie präzise Aktivitätsuntergruppen abrufen können, indem Sie die Checkpoints NUR NACH/NUR VOR SEQUENZ mit AUSSCHLIESSEN kombinieren.

## Diskussionspunkte

* Schneller Überblick über eigenständige sequenzielle Logikoperatoren und das visuelle Framework.
* Beschreiben Sie, wie sich „AUSSCHLIESSEN“ auf die Ergebnisse von Sequenzen auswirkt, indem SIE „NUR NACH/VOR SEQUENZ“ verwenden.
* Präsentieren Sie Anwendungsfälle und Demos, die zeigen, wie Sie die Methoden für Ihr Unternehmen übernehmen können.

>[!VIDEO](https://video.tv.adobe.com/v/3458040/?learn=on&enablevpops)

## Highlights


1. Sequenzielle Logik und Segmentierung in Analytics

   * Die Sitzung konzentrierte sich auf fortschrittliche Techniken zur Anwendung der sequenziellen Logik in der Analyse und betonte die Bedeutung des Verständnisses von Start- und Stopppunkten in Datensequenzen, um Kundenverhalten effektiv zu analysieren.
   * Sequenzielle Operatoren wurden als Tools zur Identifizierung von Mustern wie „Web-Treffer gefolgt von E-Mail-Treffer“ oder „Antragseinsendung gefolgt von nachfolgenden Sitzungen“ diskutiert.
   * Es wurde die gierige Natur der Segmentlogik hervorgehoben, wodurch erklärt wurde, wie sie den größtmöglichen Datensatz zurückgibt, es sei denn, dies wird durch zusätzliche Bedingungen eingeschränkt.
   * Techniken zur Definition des Umfangs, wie „nur vor“ und „nur nach“ Sequenzen, wurden eingeführt, um Untergruppen von Daten basierend auf bestimmten geschäftlichen Fragen zu untersuchen.
   * Die Verwendung von Checkpoints, Näherungsbedingungen und Ausschlusskriterien wurde erläutert, um die Datenanalyse zu verfeinern und komplexe geschäftliche Fragen zu beantworten.

2. Umgang mit mehreren interessanten Punkten in der Datenanalyse

   * Andy hat Szenarien besprochen, in denen Kundinnen und Kunden mehrere Anträge eingereicht haben, und die Notwendigkeit, das Verhalten nach jeder Übermittlung zu analysieren, anstatt nur die erste.
   * Es wurden Probleme wie sich überschneidende Antragseinreichungen und die Festlegung, ob die ursprünglichen Interessenpunkte einbezogen oder ausgeschlossen werden sollten, behandelt.
   * Es wurde betont, wie wichtig es ist, Annahmen zu klären und die Logik für den Umgang mit mehreren Vorkommen einer Sequenz zu verfeinern, um eine genaue Analyse des Kundenverhaltens über seinen gesamten Lebenszyklus hinweg sicherzustellen.

3. Erweiterte Techniken zum Stoppen des Datenabgleichs

   * In der Sitzung wurden Methoden eingeführt, um den Datenabgleich an bestimmten Checkpoints mithilfe von Ausschlusskriterien zu stoppen, sodass Analysten Daten zwischen definierten Start- und Stopppunkten untersuchen können.
   * Beispiele waren die Analyse des Verhaltens zwischen „Web-Treffer gefolgt von Mobile-App-Interaktion“ und dem Stoppen bei „E-Mail-Interaktion“.
   * Die Verwendung von „innerhalb“- und „nachher“-Bedingungen wurde erklärt, um strengere Näherungsregeln durchzusetzen und unbeabsichtigte Ergebnisse aus gieriger Logik zu vermeiden.
   * Andy zeigte, wie diese Techniken angewendet werden können, um Kundenverhalten in Bezug auf bestimmte Ereignisse wie Antragseinreichungen zu untersuchen.

4. Validieren und Verfeinern der Datenanalyselogik

   * Andy betonte, wie wichtig die Validierung von Annahmen und die Testlogik sei, um genaue Ergebnisse zu gewährleisten, da Fehler bei der Segmenterstellung oder bei den Datenannahmen häufig vorkommen.
   * Beispiele für unerwartete Ergebnisse aufgrund einer gierigen Logik wurden geteilt, was die Notwendigkeit strenger Bedingungen wie „innerhalb eines Ereignisses“ oder „innerhalb einer Sitzung“ hervorhob.
   * Validierungs-Benchmarks, z. B. kleine Datensätze mit bekannten Merkmalen, wurden empfohlen, um Analysemethoden zu testen und zu verfeinern.

5. Anwendung der sequenziellen Logik auf reale Anwendungsfälle

   * Andy gab Beispiele für reale Anwendungsfälle, wie die Analyse des Kundenverhaltens nach Antragseinreichungen oder die Identifizierung gängiger Aktionen nach Käufen oder negativen Bewertungen.
   * In der Sitzung wurde gezeigt, wie sequenzielle Logik auf Studienmuster wie „erste Sitzung nach Anwendung“ oder „zweite Sitzung nach Anwendung“ über mehrere Vorkommnisse hinweg angewendet werden kann.
   * Die Bedeutung der Skalierung der Analyse auf breitere Datensätze bei gleichzeitiger Wahrung der Genauigkeit wurde mit Beispielen kaskadierender Effekte in Daten auf Sitzungsebene erörtert.

6. Verwenden abgeleiteter Felder für flexible Analysen

   * Andy führte das Konzept der Verwendung abgeleiteter Felder in Adobe Customer Journey Analytics (CJA) ein, um Interessensmomente dynamisch zu definieren, sodass weniger Filter für jede Analyse bearbeitet werden müssen.
   * Abgeleitete Felder ermöglichen es Analysten, Filter relativ zu einem einzelnen Feld zu erstellen, was schnelle Anpassungen ermöglicht, um verschiedene Interessenpunkte zu untersuchen, z. B. produktspezifische Anwendungen oder andere Kundenereignisse.

7. Praktische Anwendungen und Zukunftspläne

   * Andy hat Pläne für die nächste Webinar-Session vorgestellt, in der es um Vorlagen, Kurzdarstellungen und praktische Anwendungen der besprochenen Konzepte gehen wird, weg von Schulungen und umsetzbaren Anwendungsfällen.
   * Die Sitzung endete mit einem Aufruf zur Rückmeldung über eine Umfrage, um das Interesse an zukünftigen Themen zu ermitteln und die Abstimmung mit den Zielen der Teilnehmer sicherzustellen.
   * Andy hob die Mikro-Engagements des Ultimate Success-Teams hervor und bot zielgerichtete Coachings an, um Unternehmen dabei zu helfen, diese Konzepte auf ihre spezifischen Anwendungsfälle anzuwenden.

8. Austausch von Material und Folgemaßnahmen

   * Andy bestätigte, dass Webinar-Materialien, einschließlich Aufzeichnungen und Blog-Posts, mit den Teilnehmern geteilt werden, um eine dokumentierte Form des Sitzungsinhalts bereitzustellen.
   * Die Teilnehmer wurden ermutigt, sich an ihre TAMs oder CSMs zu wenden, um weitere Hilfe zu erhalten und Ultimate Success-Lizenzen für personalisierte Coaching-Sitzungen zu erkunden.
