---
title: Fragen Sie den Experten - Qualität und Interaktion messen
description: Erfahren Sie, wie Sie Berichte erstellen, die Fragen zur Qualität und Interaktion beantworten. Dieses Webinar wurde am 13. November 2019 aufgezeichnet.
doc-type: feature video
team: Technical Marketing
kt: 9914
exl-id: 76a8e418-71c7-414a-9938-e64e4e73c184
duration: 3980
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 0%

---

# Fragen Sie den Experten - Qualität und Interaktion messen

Erfahren Sie, wie Sie Berichte erstellen, die Fragen zur Qualität und Interaktion beantworten. Dieses Webinar wurde am 13. November 2019 aufgezeichnet.

>[!VIDEO](https://video.tv.adobe.com/v/341120/?quality=12)

## Fragen und Antworten

**Frage**

Es gibt einige Felder, die nach gefiltert werden können, aber nicht verfügbar sind, wenn Sie versuchen, nach ihnen zu gruppieren. Arbeiten Sie an konsistenten Optionen für sie?

**Antwort**

Mit den Reporting-Tools können Sie nicht nach einem dynamischen Feld gruppieren oder nach einem Feld, bei dem mehrere Auswahlmöglichkeiten gleichzeitig ausgewählt sein können, z. B. einem Kontrollkästchen. Sie können nur Felder mit einem einzigen Wert gruppieren, auch wenn diese möglicherweise viele Auswahlmöglichkeiten haben.

Sie können nach Kontrollkästchen filtern und sie anzeigen, Sie können sie nur nicht gruppieren.

**Frage**

Kann ich bei der Iteration zu Aufgabengebieten die primäre fett darstellen?

**Antwort**

In der Iteration können wir das primäre Aufgabengebiet identifizieren. Wir müssen dies in einem Werteausdruck tun, aber HTML-Codes werden in einem Werteausdruck nicht erkannt. Also müssen wir uns einen anderen Weg einfallen lassen, um zu erkennen, dass die Rolle die primäre ist. Ich habe &quot;**&quot; vor und nach dem Namen der primären Rolle in diesem Code eingefügt. Probieren Sie es aus und sehen Sie, wie es Ihnen gefällt:

```
displayname=All Job Roles 
listdelimiter=<p> 
listmethod=nested(userRoles).lists 
textmode=true
type=iterate 
valueexpression=IF({user}.{roleID}={role}.{ID},CONCAT("**",{role}.{name},"**"),{role}. {name})
valueformat=HTML
```

Dadurch erhalten Sie eine Liste wie die folgende:

```
Support Engineer 
QA Engineer 
**Designer**
```

Dabei ist Designer die primäre Rolle für diesen Benutzer.

**Frage**

Hallo! Ich stelle einen Workflow für unsere Redaktion zusammen, der verfolgt, wo sich ein Artikel in seinem Lebenszyklus befindet (anfängliches Schreiben —> Abteilung(en) Reviews —> endgültige Bearbeitungen —> Veröffentlichen). Sie möchten leicht erkennen, in welchem Meilenstein oder Aufgabe sie sich derzeit befindet. Das Feedback, das ich erhalte, ist die standardmäßige Meilenstein -Ansicht (mit der roten oder grünen Schattierung) ist zu „beschäftigt und komplex“. Gibt es eine Möglichkeit, einfach den „Projektnamen“ und den „aktuellen Meilenstein“ in einer Tabelle oder einem Raster anzuzeigen?

**Antwort**

Ja. Sie können einen Aufgabenbericht erstellen, der die aktuell bearbeiteten Meilensteinaufgaben und die zugehörige Aufgabe ausgibt. Dies ist in einer Tabelle oder in einem Listenbericht möglich.

**Frage**

Können wir Korrekturabzugsinformationen mit Projektinformationen in einem Bericht kombinieren?

**Antwort**

Wenn Sie einen Bericht zur Korrekturabzugsgenehmigung erstellt haben, können Projektinformationen im Textmodus in Spalten übernommen werden. Wenn Sie beispielsweise auf den Projektnamen in einer Spalte verweisen möchten, können Sie Folgendes verwenden:

```
displayname=Project Name
textmode=true 
valuefield=documentVersion:document:project:name 
valueformat=HTML
```

**Frage**

Ich hätte auch gerne mehr Informationen über die Berichterstattung über Korrekturabzugsdaten, da sie sich auf das Projekt beziehen. Beispiel: ein Projektbericht, der Korrekturabzugsentscheidungen und Kommentare enthält.

**Antwort**

Um Projektinformationen und Testversandinformationen in einem einzigen Bericht zu referenzieren, sollten Sie einen Testversandgenehmigungsbericht erstellen. Derzeit können Kommentare aus einem Korrekturabzug nicht in diesen Bericht übernommen werden. Jede Entscheidung der genehmigenden Person für Korrekturabzüge kann jedoch in ihrem eigenen Zeileneintrag in der Spalte Entscheidung der genehmigenden Person gefunden werden.

**Frage**

Ich verwende sharecol oft, um den Status einer einzelnen Seite zu erstellen (viele Spalten). Wenn ich jedoch nach dem Erstellen eines Berichts oben auf der Seite eine Spalte hinzufügen möchte, ist es sehr zeitaufwendig, zurückzugehen und Änderungen vorzunehmen. Haben Sie Tipps oder Tricks, um diese Art von Änderung vorzunehmen?

**Antwort**

Wenn Sie darüber sprechen, eine Spalte an den Anfang einer Liste von Spalten im Textmodus zu setzen, müssen Sie Ihre Spalten nur manuell neu nummerieren.

Wenn Sie den Bericht jedoch bereits erstellt haben, wobei die erste Spalte einige freigegebene Spalten enthält, und Sie eine weitere freigegebene Spalte oben in der Liste platzieren möchten, ist dies einfacher.

Fügen Sie im Berichtseditor einfach einige neue Spalten hinzu und ziehen Sie sie ganz links in den Bildschirm Spalten (Ansicht). Sehen Sie sich danach die linke Spalte an, und Sie werden feststellen, dass die Spaltennummern im Textmodus alle inkrementiert wurden. Ziehen Sie so viele leere Spalten wie nötig hierher. Achten Sie darauf, etwas in diese leeren Spalten zu setzen, bevor Sie es speichern, da sie sonst entfernt werden.

**Frage**

Hallo - Was den endgültigen Fehlerbericht angeht - wie können die Berichte für mehrere Projekte erstellt werden - wenn Fehler für mehrere Projekte auftreten??

**Antwort**

Sie können nach Portfolio oder Projekt filtern, je nachdem, wie Sie Ihre Arbeit organisiert haben.

Sie können auch nach Anforderungswarteschlangen filtern. Möglicherweise möchten Sie Anfrage-Warteschlangen für jedes Projekt einrichten, in dem Sie Kunden-Benutzer als Prüfer erstellen können, die sich anmelden und Tickets direkt an die Anfrage-Warteschlangen senden können, die Sie für sie freigegeben haben.

**Frage**

Die ersten Berichte basieren auf Projekten/Projektnamen, kann dies auch für Aufgaben getan werden, und wenn ja, was die beste Möglichkeit, sie zu gruppieren, da möglicherweise der Aufgabenname häufiger anders wäre als nicht…danke!

**Antwort**

Alle diese Berichte können entweder als Aufgaben-, Problem- oder Projektberichte erstellt werden, je nachdem, wie Sie die Dinge verfolgen.

Eine gängige Möglichkeit, Aufgaben zu gruppieren, besteht darin, sie zuerst nach ihrem Projektnamen und dann nach dem Aufgabennamen innerhalb jedes Projekts zu gruppieren. Auf diese Weise können Sie, wenn Sie zwei Aufgaben mit demselben Namen haben, leicht erkennen, in welchem Projekt sie sich befinden.

**Frage**

Ich möchte wissen, welche Korrekturabzüge noch ausstehen, an welche Aufgabe und welches Projekt sie gebunden sind, wann sie weitergeleitet wurden, wann sie fällig sind und wer Moderator und genehmigende Person ist.

**Antwort**

Offene Korrekturabzüge können in einem Bericht zu Korrekturabzugsgenehmigungen nach Entscheidung warten > Gleich > True gefiltert werden. Es gibt eine Spalte für genehmigende Person, die Ihnen mitteilt, wer noch keine Entscheidung getroffen hat.

Sie können mithilfe des Textmodus auf die Aufgabe oder das Projekt verweisen, an die bzw. das der Korrekturabzug gebunden ist (siehe Beispiele unten).

```
displayname=Task Name
textmode=true 
valuefield=documentVersion:document:task:name 
valueformat=HTML
```

```
displayname=Project Name
textmode=true 
valuefield=documentVersion:document:project:name
valueformat=HTML
```

Für das Routing-Datum, das Fälligkeitsdatum und den Moderator können diese Felder derzeit nicht in einen Workfront-Bericht übernommen werden. Daher müssen Sie direkt in den Korrekturabzug klicken, um diese Informationen anzuzeigen.

**Frage**

Können Sie ein benutzerdefiniertes Formular einrichten, das nach Abschluss der Anforderung automatisch an den Anfragenden gesendet wird? Wie eine Umfrage zur „Kundenzufriedenheit“?

**Antwort**

Hier ist eine Sache, die Sie tun können, um Ihre Bedürfnisse zu erfüllen. Sie können eine Erinnerungsnachricht an ein Problem anhängen, sodass eine E-Mail an „Eingegeben von“ gesendet wird, nachdem ein tatsächliches Abschlussdatum eingegeben wurde. Die „Eingegeben von“ ist die Person, die das Problem erstellt hat.

Sie würden die Erinnerungsnachricht wie im Webinar für „Erinnerung zum Ausfüllen des Nachbearbeitungs-Reviews (AAR)“ erstellen, mit der Ausnahme, dass es sich um eine Problemerinnerung handelt. Wahrscheinlich möchten Sie auch eine E-Mail-Vorlage dafür erstellen, um einen Link zur Umfrage bereitzustellen. Sie müssen die Erinnerungsbenachrichtigung manuell auf jedes Problem anwenden (oder die Massenbearbeitung verwenden).

Eine Integration wäre besser, da sie die manuellen Schritte automatisieren könnte, aber die Erinnerungsbenachrichtigung kann sofort erfolgen.

**Frage**

Ich habe einen Bericht erstellt, der Projekte nach Vorlagentyp zeigt. Ich kann den Projektbesitzer auflisten, aber nicht die Personen, die einem Projekt zugewiesen sind.

**Antwort**

Wenn Sie das Projekt-Team (Registerkarte „Personal„) in eine Spalte in Ihrem Projektbericht ziehen möchten, müssen Sie dies über den Textmodus erstellen. Der Textmodus sieht wie folgt aus:

```
displayname=Staffing 
listdelimiter=<p> 
listmethod=nested(projectUsers).lists 
textmode=true
type=iterate 
valuefield=user:name 
valueformat=HTML
```

## Textmodus-Code für den AAR-Interaktionsbericht

```
column.0.displayname=Task Details
column.0.value=<b>Project Name:</b>&nbsp;
column.0.valueformat=HTML
column.0.sharecol=true
column.1.valuefield=project:name
column.1.valueformat=HTML
column.1.sharecol=true
column.2.value=<br>
column.2.valueformat=HTML
column.2.sharecol=true
column.3.value=<b>Task Name:</b>&nbsp;
column.3.valueformat=HTML
column.3.sharecol=true
column.4.valuefield=name
column.4.valueformat=HTML
column.4.sharecol=true
column.5.value=<br>
column.5.valueformat=HTML
column.5.sharecol=true
column.6.value=<b>Task Owner:</b>&nbsp;
column.6.valueformat=HTML
column.6.sharecol=true
column.7.valuefield=assignedTo:name
column.7.valueformat=HTML
column.7.sharecol=true
column.8.value=<br>
column.8.valueformat=HTML
column.8.sharecol=true
column.9.value=<b>Actual Completion Date:</b>&nbsp;
column.9.valueformat=HTML
column.9.sharecol=true
column.10.valuefield=actualCompletionDate
column.10.valueformat=HTML
column.11.displayname=Name of Reviewer
column.11.linkedname=Name of Reviewer
column.11.namekey=view.relatedcolumn
column.11.namekeyargkey.0=Name of Reviewer
column.11.namekeyargkey.1=name
column.11.querysort=DE:Name of Reviewer:name
column.11.valuefield=Name of Reviewer:name
column.11.valueformat=customReferenceObjectAsString
column.12.displayname=AAR 1
column.12.description=In your view, does the work match stakeholders’ expectations? Did we achieve the intended results?
column.12.value=<b>AAR 1 Score:</b>&nbsp;
column.12.valueformat=HTML
column.12.sharecol=true
column.13.valuefield=AAR 1 - In your view, does the work match stakeholders’ expectations? Did we achieve the intended results?
column.13.valueformat=customDataLabelsAsString
column.13.sharecol=true
column.14.value=<br>
column.14.valueformat=HTML
column.14.sharecol=true
column.15.value=<br><b>AAR 1 User Comment:</b>&nbsp;
column.15.valueformat=HTML
column.15.sharecol=true
column.16.valuefield=AAR 1 User Comment
column.16.valueformat=customDataLabelsAsString
column.17.linkedname=direct
column.17.namekey=AAR 1 Reviewer Comment
column.17.querysort=DE:AAR 1 Reviewer Comment
column.17.valuefield=AAR 1 Reviewer Comment
column.17.valueformat=customDataLabelsAsString
column.18.linkedname=direct
column.18.displayname=AAR 1 Needs Attn
column.18.querysort=DE:AAR 1 Needs Attention
column.18.valuefield=AAR 1 Needs Attention
column.18.valueformat=customDataLabelsAsString
column.19.linkedname=direct
column.19.displayname=AAR 1 Needs Attn Notes
column.19.querysort=DE:AAR 1 Needs Attention Notes
column.19.valuefield=AAR 1 Needs Attention Notes
column.19.valueformat=customDataLabelsAsString
column.20.displayname=AAR 2
column.20.description=Do You Believe This Work Will Make an Impact?
column.20.value=<b>AAR 2 Score:</b>&nbsp;
column.20.valueformat=HTML
column.20.sharecol=true
column.21.valuefield=AAR 2 - Do You Believe This Work Will Make an Impact?
column.21.valueformat=customDataLabelsAsString
column.21.sharecol=true
column.22.value=<br>
column.22.valueformat=HTML
column.22.sharecol=true
column.23.value=<br><b>AAR 2 User Comment:</b>&nbsp;
column.23.valueformat=HTML
column.23.sharecol=true
column.24.valuefield=AAR 2 User Comment
column.24.valueformat=customDataLabelsAsString
column.25.linkedname=direct
column.25.namekey=AAR 2 Reviewer Comment
column.25.querysort=DE:AAR 2 Reviewer Comment
column.25.valuefield=AAR 2 Reviewer Comment
column.25.valueformat=customDataLabelsAsString
column.26.linkedname=direct
column.26.displayname=AAR 2 Needs Attn
column.26.querysort=DE:AAR 2 Needs Attention
column.26.valuefield=AAR 2 Needs Attention
column.26.valueformat=customDataLabelsAsString
column.27.linkedname=direct
column.27.displayname=AAR 2 Needs Attn Notes
column.27.querysort=DE:AAR 2 Needs Attention Notes
column.27.valuefield=AAR 2 Needs Attention Notes
column.27.valueformat=customDataLabelsAsString
column.28.displayname=AAR 3
column.28.description=Are you proud of the work you did on this?
column.28.value=<b>AAR 3 Score:</b>&nbsp;
column.28.valueformat=HTML
column.28.sharecol=true
column.29.valuefield=AAR 3 - Are you proud of the work you did on this?
column.29.valueformat=customDataLabelsAsString
column.29.sharecol=true
column.30.value=<br>
column.30.valueformat=HTML
column.30.sharecol=true
column.31.value=<br><b>AAR 3 User Comment:</b>&nbsp;
column.31.valueformat=HTML
column.31.sharecol=true
column.32.valuefield=AAR 3 User Comment
column.32.valueformat=customDataLabelsAsString
column.33.linkedname=direct
column.33.namekey=AAR 3 Reviewer Comment
column.33.querysort=DE:AAR 3 Reviewer Comment
column.33.valuefield=AAR 3 Reviewer Comment
column.33.valueformat=customDataLabelsAsString
column.34.linkedname=direct
column.34.displayname=AAR 3 Needs Attn
column.34.querysort=DE:AAR 3 Needs Attention
column.34.valuefield=AAR 3 Needs Attention
column.34.valueformat=customDataLabelsAsString
column.35.linkedname=direct
column.35.displayname=AAR 3 Needs Attn Notes
column.35.querysort=DE:AAR 3 Needs Attention Notes
column.35.valuefield=AAR 3 Needs Attention Notes
column.35.valueformat=customDataLabelsAsString
column.36.displayname=Done
column.36.valuefield=Review Complete
column.36.valueformat=customDataLabelsAsString
```
