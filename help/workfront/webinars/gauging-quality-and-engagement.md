---
title: Fragen Sie den Experten - Qualität des Testversands und Interaktion
description: Erfahren Sie, wie Sie Berichte erstellen, die Fragen zur Qualität und Interaktion beantworten. Dieses Webinar wurde am 13. November 2019 aufgenommen.
activity: use
doc-type: feature video
team: Technical Marketing
kt: 9914
exl-id: 50dbcdf4-2e5d-420b-975e-1e3e683356fd
source-git-commit: ca06e5a8b1602a7bcfb83a43f529680a5a96bacf
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 1%

---

# Fragen Sie den Experten - Qualität des Testversands und Interaktion

Erfahren Sie, wie Sie Berichte erstellen, die Fragen zur Qualität und Interaktion beantworten. Dieses Webinar wurde am 13. November 2019 aufgenommen.

>[!VIDEO](https://video.tv.adobe.com/v/341120/?quality=12)

## Fragen und Antworten

**Frage**

Es gibt einige Felder, nach denen gefiltert werden kann, die jedoch nicht verfügbar sind, wenn Sie versuchen, sie zu gruppieren. Arbeiten Sie daran, diese Optionen konsistent zu machen?

**Antwort**

Die Reporting-Tools ermöglichen es Ihnen nicht, eine Gruppierung nach einem dynamischen Feld oder einem Feld vorzunehmen, bei dem mehrere Auswahlmöglichkeiten gleichzeitig ausgewählt sein können (z. B. ein Kontrollkästchen). Sie können nur Felder gruppieren, die einen einzigen Wert haben, auch wenn sie viele Möglichkeiten haben.

Sie können nach Checkboxes filtern und sie anzeigen, Sie können sie einfach nicht gruppieren.

**Frage**

Kann ich im Beispiel der Iteration zu Stellenrollen das primär fett anzeigen?

**Antwort**

In der Iteration können wir die Rolle des Hauptauftrags identifizieren. Wir müssen dies in einem Werteausdruck tun, aber HTML-Codes werden in einem Werteausdruck nicht erkannt. Wir müssen also eine andere Möglichkeit finden, die Rolle als die primäre Rolle zu identifizieren. Ich setzte &quot;**&quot;vor und nach dem primären Rollennamen in diesen Code. Probieren Sie es aus, um zu sehen, wie es Ihnen gefällt:

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

Hallo! Ich stelle einen Workflow für unser Redaktionsteam zusammen, der verfolgt, wo sich ein Artikel im Lebenszyklus befindet (anfängliches Schreiben > Bewertungen der Abteilungen > endgültige Bearbeitungen > Veröffentlichen). Sie möchten einfach sehen, zu welchem Meilenstein oder welchen Aufgaben er sich derzeit befindet. Das Feedback, das ich erhalte, ist die standardmäßige Meilensteinansicht (mit roter oder grüner Schattierung) zu &quot;beschäftigt und komplex&quot;. Gibt es eine Möglichkeit, einfach &quot;Projektname&quot;und &quot;Aktueller Meilenstein&quot;in einer Tabelle oder einem Raster anzuzeigen?

**Antwort**

Ja. Sie können einen Aufgabenbericht erstellen, der die derzeit bearbeiteten Meilensteinaufgaben und die damit verbundenen Aufgaben anzeigt. Dies können Sie in einer Tabelle oder in einem Listenbericht tun.

**Frage**

Können in einem Bericht Testsendungen mit Projektinformationen kombiniert werden?

**Antwort**

Wenn Sie einen Bericht zur Testbestätigung erstellt haben, können Projektinformationen mithilfe des Textmodus in Spalten eingefügt werden. Wenn Sie beispielsweise den Projektnamen in einer Spalte referenzieren möchten, können Sie Folgendes verwenden:

```
displayname=Project Name
textmode=true 
valuefield=documentVersion:document:project:name 
valueformat=HTML
```

**Frage**

Ich möchte auch mehr Informationen über die Berichterstattung über die Testversanddaten im Zusammenhang mit dem Projekt erhalten. Beispiel: ein Projektbericht, der eine Testbestätigungsentscheidung und Kommentare enthält.

**Antwort**

Um Projektinformationen und Testversandinformationen in einem einzigen Bericht zu referenzieren, sollten Sie einen Validierungsbericht erstellen. Derzeit können keine Kommentare aus einem Testversand in diesen Bericht aufgenommen werden. Jede Entscheidung für einen Testversand-Validierer kann jedoch in der Spalte Entscheidung für den Genehmiger in einem eigenen Zeileneintrag gefunden werden.

**Frage**

Ich verwende sharecol oft, um den Status einer einzelnen Seite zu erstellen (viele Spalten). Wenn ich nach der Erstellung eines Berichts jedoch eine Spalte am Seitenanfang hinzufügen möchte, ist es sehr zeitaufwendig, zurückzukehren und zu ändern. Haben Sie Tipps oder Tricks, diese Art von Änderung vorzunehmen?

**Antwort**

Wenn Sie davon sprechen, eine Spalte ganz oben in der Liste der Textmodus-Spalten zu platzieren, müssen Sie Ihre Spalten nur manuell neu nummerieren.

Wenn Sie den Bericht jedoch bereits erstellt haben, wobei die erste Spalte einige gemeinsame Spalten enthält, und Sie eine weitere gemeinsame Spalte ganz oben auf der Liste platzieren möchten, ist dies einfacher.

Fügen Sie im Berichtseditor einfach einige neue Spalten hinzu und ziehen Sie sie ganz links in den Bildschirm Spalten (Ansicht). Nachdem Sie dies getan haben, sehen Sie, was früher die linke Spalte war, und Sie werden feststellen, dass die Spaltenzahlen im Textmodus inkrementiert wurden. Ziehen Sie so viele leere Spalten dorthin, wie Sie benötigen. Stellen Sie sicher, dass Sie etwas in diese leeren Spalten einfügen, bevor Sie es speichern, sonst werden sie entfernt.

**Frage**

Hallo - im Hinblick auf den letzten Fehlerbericht - wie können die Berichte für mehrere Projekte erstellt werden - wenn Fehler für mehrere Projekte eingehen?

**Antwort**

Sie können nach Portfolio oder Projekt filtern, je nachdem, wie Sie Ihre Arbeit organisiert haben.

Sie können auch nach Anforderungswarteschlangen filtern. Möglicherweise möchten Sie Anforderungswarteschlangen für jedes Projekt einrichten, in denen Sie Kundenbenutzer als Validierer erstellen können, die sich anmelden und Tickets direkt an die Anforderungswarteschlangen senden können, die Sie für sie freigegeben haben.

**Frage**

Die ersten Berichte basieren auf Projekten/Projektnamen, können dies auch für Aufgaben durchgeführt werden und wenn ja, wie man sie am besten gruppiert, da der Aufgabenname möglicherweise öfter als nicht anders lautete..Danke!

**Antwort**

Alle diese Berichte können je nach Art der Verfolgung entweder als Aufgaben-, Problem- oder Projektberichte erstellt werden.

Eine gängige Möglichkeit, Aufgaben zu gruppieren, besteht darin, sie zunächst nach ihrem Projektnamen und dann nach dem Aufgabennamen in jedem Projekt zu gruppieren. Auf diese Weise ist es einfach zu sehen, in welchem Projekt sie sich befinden, wenn Sie zwei Aufgaben mit demselben Namen haben.

**Frage**

Ich möchte wissen, mit welchen Testsendungen, mit welchen Aufgaben und Projekten sie verbunden sind, wann sie weitergeleitet wurden, wann sie fällig sind und wer Moderator und Genehmiger ist.

**Antwort**

Ausstehende Testsendungen können innerhalb eines Validierungsberichts nach Warten auf Entscheidung > Entspricht > Wahr gefiltert werden. Es gibt eine Spalte für Genehmiger, die Ihnen mitteilt, wer noch keine Entscheidung getroffen hat.

Sie können auf die Aufgabe oder das Projekt verweisen, an das der Testversand mithilfe des Textmodus gebunden ist (siehe Beispiele unten).

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

Was das Routing-Datum, das Fälligkeitsdatum und den Moderator anbelangt, so können diese Felder derzeit nicht in einen Workfront-Bericht übertragen werden. Daher müssen Sie direkt in den Testversand klicken, um diese Informationen anzuzeigen.

**Frage**

Können Sie ein benutzerdefiniertes Formular einrichten, das automatisch an einen Anfragenden gesendet wird, nachdem dessen Anfrage abgeschlossen wurde? Wie eine Umfrage zur Kundenzufriedenheit?

**Antwort**

Hier ist eine Sache, die Sie tun können, um Ihre Bedürfnisse zu erfüllen. Sie können eine Erinnerungsbenachrichtigung an ein Problem anhängen, das eine E-Mail an die &quot;Eingestiegen von&quot;sendet, nachdem ein tatsächliches Abschlussdatum eingegeben wurde. Die Person &quot;Eingestiegen von&quot;ist die Person, die das Problem erstellt hat.

Sie würden die Erinnerungsbenachrichtigung wie im Webinar für &quot;Erinnerung zum Ausfüllen der AAR-Datei für &quot;Nach Aktionsüberprüfung&quot; erstellen, mit der Ausnahme, dass dies eine Problemerinnerung wäre. Sie möchten wahrscheinlich eine E-Mail-Vorlage für diese erstellen und einen Link zur Umfrage bereitstellen. Sie müssen die Erinnerungsbenachrichtigung manuell auf jedes Problem anwenden (oder die Massenbearbeitung verwenden).

Eine Integration wäre besser, da sie die manuellen Schritte automatisieren könnte, aber die Erinnerungsbenachrichtigung kann sofort durchgeführt werden.

**Frage**

Ich habe einen Bericht erstellt, der Projekte nach Vorlagentyp anzeigt. Ich kann den Projekteigentümer auflisten, aber nicht die Personen, die einem Projekt zugewiesen sind.

**Antwort**

Wenn Sie im Projektteam (Registerkarte &quot;Staffelung&quot;) eine Spalte in Ihrem Projektbericht abrufen möchten, müssen Sie dies über den Textmodus erstellen. Der Textmodus sieht wie folgt aus:

```
displayname=Staffing 
listdelimiter=<p> 
listmethod=nested(projectUsers).lists 
textmode=true
type=iterate 
valuefield=user:name 
valueformat=HTML
```

## Textmoduscode für den AAR-Interaktionsbericht

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
