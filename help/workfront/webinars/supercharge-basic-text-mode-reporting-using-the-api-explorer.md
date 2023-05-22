---
title: Fragen Sie den Experten - Berichterstellung für den grundlegenden Textmodus mit Supercharge über den API Explorer.
description: Erfahren Sie mehr über den API-Explorer, seine Verwendung und die Verbesserung Ihrer Berichte mithilfe des grundlegenden Textmodus. Dieses Webinar wurde am 22. Januar 2020 aufgenommen.
activity: use
doc-type: feature video
team: Technical Marketing
kt: 9918
source-git-commit: edd0bdb28a9b3d065a64a95af6a216b747577c77
workflow-type: tm+mt
source-wordcount: '1658'
ht-degree: 2%

---

# Fragen Sie den Experten - Berichterstellung für den grundlegenden Textmodus mit Supercharge über den API Explorer.

Erfahren Sie mehr über den API-Explorer, seine Verwendung und die Verbesserung Ihrer Berichte mithilfe des grundlegenden Textmodus. Dieses Webinar wurde am 22. Januar 2020 aufgenommen.

>[!VIDEO](https://video.tv.adobe.com/v/341124/?quality=12)

## Weitere Ressourcen

![Eine Grafik mit Beispielen für Code-Regeln im Textmodus](assets/text-mode-chart.png)


**Spalte &quot;Alle Auftragsrollen&quot;**

```
description="Primary =" indicates the user's primary job role
displayname=All Job Roles
listdelimiter=<p>
listmethod=nested(userRoles).lists
textmode=true
type=iterate
valueexpression=IF({user}.{roleID}={role}.{ID},CONCAT("Primary = ",{role}.{name}),{role}.{name})
valueformat=HTML
```

**Textmodus für die Spalte &quot;Alle Teams&quot;**

```
displayname=All Teams
listdelimiter=<p>
listmethod=nested(teams).lists
textmode=true
type=iterate
valueexpression={name}
valueformat=HTML
```

**Textmodus für die Spalte &quot;Alle Gruppen&quot;**

```
displayname=All Groups
listdelimiter=<p>
listmethod=nested(userGroups).lists
textmode=true
type=iterate
valuefield=group:name
valueformat=HTML
```

**Textmodus für die Spalte &quot;Direkte Berichte&quot;**

```
displayname=Direct Reports
listdelimiter=<p>
listmethod=nested(directReports).lists
textmode=true
type=iterate
valueexpression={name}
valueformat=HTML
```

## Fragen und Antworten

**Frage**

Ist es möglich, im Textmodus eine beliebige Sammlung in einem Bericht zu verwenden?

**Antwort**

Ja, Sie können ein beliebiges Objekt im Sammlungsbereich verwenden. Sie werden erforschen und sehen wollen, worauf Sie Zugriff haben. Nicht alle haben Zugriff auf das Benutzerobjekt und das Vorgangsrollenobjekt, wie wir es mit dem Benutzerrollen-Objekt im API-Explorer gesehen haben.

**Frage**

Können Sie die bedingte Verwendung verschiedener Sammlungen in derselben Spalte (Projekt- und Aufgabenaktualisierungen) besprechen?

**Antwort**

Wenn Sie sich im Iterationsbereich befinden und dort das Wertefeld oder den Werteausdruck sehen, greift dies auf eines der Elemente in Ihrer Sammlungsliste zu. Mithilfe des Wertefelds können wir den Namen dieser Auftragsrolle abrufen, z. B. oder alles, was sich in diesem Element in der Liste befindet. Wenn Sie sich in einer Aufgabe befinden, kann ein Aufgabenobjekt auf das Projekt verweisen, in dem es sich befindet.

**Frage**

Können Sie besprechen, ob die Sammlung von Aufgabenaktualisierungen nur in einem Aufgabenbericht möglich ist?

**Antwort**

Wenn Sie einen Problembericht erstellen, können Sie Aufgabeninformationen anzeigen, wenn das Problem in Bezug auf die Aufgabe gemeldet wurde. Außerdem können Sie diese Informationen aus der Sammlung sehen. Außer in diesen Situationen müssen Sie sich in einem Aufgabenbericht befinden, um Aufgabenerfassungsdaten anzuzeigen.

**Frage**

Können Sie das Textformat ([!DNL CSS]) Beispiele?

**Antwort**

Workfront unterstützt nicht [!DNL CSS] im Textmodus.

**Frage**

Was ist die beste und/oder schnellste Methode, einen benutzerdefinierten Feldnamen zu finden - für Textmodusberichte? Ich habe die HTML-Bearbeitungsoption im Browser ODER verwendet, indem ich ein Feld in einem Bericht hinzugefügt habe und in den Textmodus wechselte, um es zu erfassen.. merkwürdig, wie andere dies durchführen.

**Antwort**

Ich finde es am schnellsten, das Feld in der Benutzeroberfläche auszuwählen, dann in den Textmodus zu wechseln und den Feldnamen zu kopieren. Dadurch wird sichergestellt, dass ich die richtige Schreibweise für das Feld erhalte.

**Frage**

Wie kann ich den Textmodus verwenden, um Mitglieder eines Teams in einem Bericht zu identifizieren? Wir verwenden derzeit Teamzuweisungen in Workflows zur Aufgabenvalidierung und möchten die Teammitglieder in der aktuellen Validierungsphase in einer Spalte auflisten, die der Funktionsweise des Felds Genehmiger und Status ähnelt.

**Antwort**

Um auf die Team-Mitglieder zu verweisen, die der aktuellen Validierungsphase zugeordnet sind, müssen Sie auf eine Sammlung einer referenzierten Kollektion verweisen, die derzeit über die Textmodusfunktionen von Workfront nicht möglich ist. Die Spalte, die Ihr Unternehmen derzeit verwendet und die das mit der Genehmigung verbundene Team anzeigt, ist Ihre beste Option.

**Frage**

Müssen Feld- und Objektname Groß-/Kleinschreibung (z. B. Rolle vs. Rolle)?

**Antwort**

Wenn Sie Objekte im Textmodus referenzieren, sollten Sie sie genau so schreiben, wie in der rechten Spalte des API Explorer angezeigt wird. Wenn Sie beispielsweise einen Projektnamen aus einem Aufgabenbericht referenzieren möchten, würde Ihr Wertefeld wie folgt aussehen:

```
valuefield=project:name
```

Im Fall von Problemen werden diese jedoch im API Explorer als opTasks bezeichnet. Wenn Sie also einen Stunden-Bericht ausführen und eine Spalte für den Problemnamen hinzufügen möchten, würde das Wertefeld wie folgt aussehen:

```
valuefield=opTask:name
```

**Frage**

Ich möchte einen Bericht erstellen, der für jedes Projekt zeigt, an welchen aktiven Aufgaben derzeit gearbeitet wird. Wie würde ich das am besten machen? Ich denke, es wäre ein Aufgabenbericht, dem auch Spalten mit Projektinformationen hinzugefügt werden?

**Antwort**

Das ist richtig. Ein Aufgabenbericht wäre dafür am besten. Sie müssen &quot;Aktive Aufgaben&quot;definieren. Wenn Sie Vorgänger verwenden, wären dies Aufgaben, die bereit sind. Sie können also nach &quot;Bereit = True&quot;filtern. Dies würde alle Aufgaben einbringen, die startbereit sind. Dann empfehle ich Ihnen, eine Gruppierung nach Projektname durchzuführen, sodass Ihre Aufgaben alle gruppiert sind und Sie auf einen Blick sehen können, welche Aufgaben zu welchem Projekt gehören.

**Frage**

Gibt es eine Möglichkeit, Berichte zu erstellen, die Daten berechnen - zum Beispiel % der Projekte, die bestimmte Kriterien erfüllen?

**Antwort**

Die beste Möglichkeit, einen Bericht zu erstellen, um Daten darzustellen oder zu berechnen (z. B. in %), besteht darin, Gruppierungen auf Ihren Bericht anzuwenden und dann eine Grafik anzuwenden. Wenn Sie dem Bericht ein Tortendiagramm hinzufügen möchten, können die Tortenscheiben in Werten oder Prozentwerten dargestellt werden.

**Frage**

Können Sie den Textmodus verwenden, um die Mitglieder eines Teams zu identifizieren, die der aktuellen Phase der Aufgabenvalidierung ähnlich der Spalte Genehmiger und Status zugewiesen sind?

**Antwort**

Im Textmodus müssen Sie dem Bericht &quot;Aufgabe&quot;eine Kollektionsspalte hinzufügen, die Folgendes enthält:

```
displayname=Current Approval Stage Approvers 
listdelimiter=<p> 
listmethod=nested(currentApprovalStep.stepApprovers).lists 
textmode=true
type=iterate 
valuefield=user:name 
valueformat=HTML
```

**Frage**

Können Sie filtern, wo alle Gruppen eine bestimmte Gruppe enthalten?

**Antwort**

Wenn Sie die Elemente in Ihrem Bericht filtern möchten, tun Sie dies im Filter -Tab Ihres Berichts. Wenn Sie also nur Benutzer sehen möchten, bei denen eine ihrer Gruppen &quot;Buchhaltung&quot;lautete, würden Sie eine Filterregel hinzufügen, die Folgendes sagt:

```
Other Groups>ID>Equal>Accounting
```

**Frage**

Gibt es eine Möglichkeit, einen Bericht zu erstellen, der die tatsächliche Dauer einer Kombination von Aufgaben bestimmt?

**Antwort**

Sie müssen Ihren Bericht so filtern, dass nur die gewünschte Aufgabenkombination einbezogen wird. Dann müssten Sie eine Spalte &quot;Tatsächliche Dauer&quot;in Ihre Ansicht einfügen und sie anhand der Summe in den Spalteneinstellungen zusammenfassen. Schließlich müssten Sie Ihren Bericht auf irgendeine Weise gruppieren. Wenn Sie den Bericht ausführen, zeigt die Gruppierungsleiste die Gesamtdauer an, die in den Zeilen, die gruppiert werden, tatsächlich vergangen ist.

**Frage**

Gibt es eine Möglichkeit, Aufgaben, die unter ein übergeordnetes Element fallen, abzuziehen, um die Dauer für die restlichen Aufgaben unter einem übergeordneten Element zu bestimmen?

**Antwort**

Die Dauer einer übergeordneten Aufgabe wird berechnet, indem das Startdatum der frühesten Startaufgabe vom Enddatum der letzten Endaufgabe unter dieser übergeordneten Aufgabe abgezogen wird. In einem Bericht wissen Sie nur über jede einzelne Aufgabe, die in Betracht gezogen wird, ob sie angezeigt werden soll oder nicht. Die Report Engine kann nicht an Informationen aus einer Aufgabe festhalten und sie bei der Untersuchung einer anderen Aufgabe verwenden. Die einzige Möglichkeit, das zu erreichen, was Sie verlangen, besteht darin, eine Aufgabe aus der Liste der Projektaufgaben zu entfernen und zu beobachten, wie die Dauer der übergeordneten Aufgabe neu berechnet wird.

**Frage**

Bei bedingten Gruppierungen ist ein benutzerdefiniertes Formular (z. B. &quot;Westliche Staaten&quot;, &quot;Zentralstaaten&quot;, &quot;Oststaaten&quot;) zur Dekodierung der einzelnen Gruppen eine gängige Technik, die gut mit dieser Anmerkung funktioniert. Wann empfiehlt es sich, berechnete Gruppierungen oder berechnete Parameter zu verwenden?

**Antwort**

Berechnete Gruppierungen (auch als Wertausdruck in einer Gruppierung bezeichnet) sind eine praktische Methode, um ein Ergebnis zu erhalten, das in Ihrer Gruppierungsleiste angezeigt wird. Dies kann auch mithilfe eines berechneten benutzerdefinierten Felds erfolgen. Für jeden Ansatz gibt es Vor- und Nachteile:

* Werteausdrücke werden jedes Mal berechnet, wenn Ihre Browser-Seite aktualisiert wird. Dies kann besser sein als berechnete benutzerdefinierte Felder, die neu berechnet werden, wenn das Objekt, an das sie angehängt sind, bearbeitet wird, wenn die berechneten Felder in einer Massenbearbeitung neu berechnet werden oder wenn das benutzerdefinierte Formular bearbeitet und die Option &quot;Vorherige Berechnungen aktualisieren&quot;aktiviert wird.
* Werteausdrücke können jedoch nicht in Grafiken, bedingter Formatierung oder Filtern verwendet werden. Dazu müssen Sie berechnete benutzerdefinierte Felder verwenden.

**Frage**

Gibt es keine Möglichkeit, den Anzeigenamen der Gruppierung von &quot;Kein Wert&quot;zu etwas anderem zu ändern, das wir für Berichtszwecke aufrufen? Mit anderen Worten, es wird immer &quot;Kein Wert&quot;?

**Antwort**

Es gibt eine Möglichkeit, &quot;Kein Wert&quot;durch etwas Anderes zu ersetzen. Angenommen, Sie haben einen Projektbericht nach Portfolio gruppiert. Alle Projekte, die keinem Portfolio zugewiesen sind, werden in einer Gruppierung mit dem Titel aufgeführt:

```
Portfolio: Name: No Value
```

Um dies zu ändern, bearbeiten Sie die Gruppierung im Textmodus und ersetzen Sie die folgende Zeile:

```
group.0.valuefield=portfolio:name
```

mit dieser Zeile:

```
group.0.valueexpression=IF(ISBLANK({portfolio}.{name}),"Not in any Portfolio",{portfolio}.{name})
```

Die Gruppierung hat jetzt folgenden Titel:

```
Portfolio: Name: Not in any Portfolio
```

**Frage**

Gibt es einen Parameter zur Verfolgung unvollständiger Zuweisungen, d. h.:

1. Aufgaben mit einer einzelnen Zuweisung, denen keine Person zugewiesen wurde, oder
1. Aufgaben mit mehreren Zuweisungen, denen mindestens eine nicht zugewiesene Person für die angeforderten Rollen zugewiesen ist

**Antwort**

Dies lässt sich durch die Verwendung eines Zuweisungsberichts und Filterung nach

```
Assigned To ID > Is Blank and Role ID > Is Not Blank
```

Dadurch werden alle Aufgaben oder Probleme berücksichtigt, die einer Rolle, aber nicht notwendigerweise einem bestimmten Benutzer zugewiesen wurden. Sie müssen die Spalten für den Namen Aufgabe und Problem hinzufügen, um zu sehen, zu welchem Objekt die Zuweisung gehört, und wenn sie nach Projektname gruppiert sind, sollte dies helfen, das Objekt organisiert zu halten.

**Frage**

Chuck, ich vergesse, aber erinnern Sie sich an die Eigenschaft im Textmodus, die dann als QuickInfo gerendert wird, wenn Sie den Mauszeiger bewegen?

**Antwort**

description= ermöglicht die Anzeige einer QuickInfo, wenn Sie den Mauszeiger über die Spaltenüberschrift bewegen.

**Frage**

Kann ich einen Bericht zu einem Kontrollkästchen erstellen, das mehrere Auswahlmöglichkeiten erlaubt, aber nur die erste Auswahl in den Bericht zieht?

**Antwort**

Ja. Die im Kontrollkästchen ausgewählten Optionen enthalten alle eine Zeichenfolge, wobei jede Auswahl durch ein Komma getrennt ist. Verwenden Sie den Suchausdruck, um die Position des ersten Kommas im Kontrollkästchen-Feld zu finden, und verwenden Sie dann diesen Index mit dem LINKEN Ausdruck, um so viele Zeichen am Anfang der Liste anzuzeigen. Hier ist der Code:

```
valueexpression=IF(SEARCH(",",{DE:Checkbox Field},0)>0,LEFT({DE:Checkbox Field},SEARCH(",",{DE:Checkbox Field},0)),{DE:Checkbox Field})
```

Wenn Sie in Ihrem Kontrollkästchen ein Komma in einem Auswahlnamen verwenden, wird nur der Teil dieser Auswahl bis zum ersten Komma angezeigt.
