---
title: Fragen an den Experten - Geschwindigkeit messen
description: Erfahren Sie, wie Sie die Geschwindigkeit mithilfe von  [!DNL Workfront]  messen und verfolgen können. Dieser Workshop wurde am 14. August 2019 aufgenommen.
doc-type: feature video
team: Technical Marketing
jira: KT-9912
last-substantial-update: 2023-08-15T00:00:00Z
exl-id: 83053de2-e386-4243-a9c8-a2ad9d51790f
duration: 4630
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '3962'
ht-degree: 0%

---

# Fragen an den Experten - Geschwindigkeit messen

Erfahren Sie, wie Sie die Geschwindigkeit mithilfe von [!DNL Workfront] messen und verfolgen können. Dieser Workshop wurde am 14. August 2019 aufgenommen.

>[!VIDEO](https://video.tv.adobe.com/v/341057/?quality=12)

## Benutzerdefinierte Felder, die in der Präsentation verwendet werden

Sparen Sie Zeit durch Kopieren und Einfügen der unten stehenden Berechnungen.

>[!NOTE]
>
>Die Syntax für benutzerdefinierte Feldberechnungen hat sich seit der Präsentation im Jahr 2019 geändert. Die in der Präsentation angegebenen Konzepte und anderen Anweisungen sind jedoch weiterhin korrekt.
>&#x200B;>**Die folgenden Berechnungen wurden aktualisiert, um die neuesten Syntaxregeln widerzuspiegeln.**

**Erstes Commit-Datum**

Format: Datum

Berechnung:

```
IF(ISBLANK({DE:First Commit Date}),{defaultBaseline}.{plannedCompletionDate},{DE:First Commit Date})
```

**Erste Dauer**

Format: Text

Berechnung:

```
IF(ISBLANK({DE:First Duration}),{defaultBaseline}.{durationMinutes},{DE:First Duration})
```

**Work-to-Commit-Ratio**

Format:Number

Berechnung:

```
ROUND(DIV({actualDurationMinutes},{DE:First Duration}),1)
```

**Work-to-Commit-Ratio-Status**

Format:Text

Berechnung:

```
IF({DE:Work-to-Commit Ratio}>2,"Terrible",IF({DE:Work-to-Commit Ratio}>1.6,"Poor",IF({DE:Work-to-Commit Ratio}>1.2,"Not Bad","Excellent")))
```

**Angepasste Geschwindigkeit**

Format:Number

Berechnung:

```
ROUND(DIV({actualDurationMinutes},{durationMinutes}),1)
```

**Angepasster Geschwindigkeitsstatus**

Format:Text

Berechnung:

```
IF({DE:Adjusted Velocity}>2,"Terrible",IF({DE:Adjusted Velocity}>1.6,"Poor",IF({DE:Adjusted Velocity}>1.2,"Not Bad","Excellent")))
```

## Fragen und Antworten

**Frage**

Hallo, vielen Dank für die Organisation dieses Webinars. Ich habe eine Frage zu Field in Workfront. In unserem System haben wir ein benutzerdefiniertes Feld namens „Status“ erstellt, das eine Kombination aus Status und Bedingung ist. Dieses Statusfeld enthält viele Statuen in tausend Projekten, was für unseren Tableau-Datenextrakt sehr wichtig ist. Jetzt möchten wir jedoch dieses Feld entfernen und stattdessen das native Feld Bedingung verwenden. Haben Sie eine Ahnung, wie ich dieses Feld umdrehen kann, ohne Daten zu verlieren? Alles, was ich mir jetzt vorstellen kann, ohne Daten zu verlieren, ist, es manuell von Projekt zu Projekt zu wechseln.

**Antwort**

In einer Situation wie dieser können Sie Filter und Massenbearbeitung verwenden, um den Aufwand für das Ausfüllen des Bedingungsfelds basierend auf Ihrem benutzerdefinierten Statusfeld halbautomatisch zu automatisieren.

Im Folgenden werden die Schritte beschrieben:

1. Bestimmen Sie, welche Statuswerte Sie Bedingungswerten zuordnen möchten. Angenommen, Sie haben den Statuswert „Spät“ und „Sehr spät“, die beide einem Bedingungswert „In Schwierigkeiten“ zugeordnet sind
1. Erstellen Sie einen Projektbericht, der alle Projekte mit dem Statuswert „spät“ und „Sehr spät“ ausgibt
1. Führen Sie den Bericht aus. Stellen Sie sicher, dass Sie alle Projekte anzeigen (siehe Optionen unten rechts im Bericht)
1. Klicken Sie in der Leiste mit den Spaltenüberschriften oben links im Bericht auf das Kontrollkästchen. Dadurch werden alle Projekte im Bericht ausgewählt
1. Klicken Sie auf die Schaltfläche Bearbeiten oberhalb der Berichtsliste
1. Setzen Sie den Bedingungstyp auf Manuell
1. Setzen Sie das Feld Bedingung auf In Schwierigkeiten
1. Klicken Sie auf Änderungen speichern


**Frage**

Wie wird „ausgezeichnet“, „nicht schlecht“ usw. definiert?

**Antwort**

Das war nur ein Beispiel, aber so habe ich es eingerichtet. Zuerst habe ich zwei Indizes berechnet:

bereinigte Geschwindigkeit

Die Formel hierfür lautet Tatsächliche Dauer/Geplante Dauer (die im Feld Dauer in einem Projekt gespeichert wird). Da sich die geplante Dauer des Projekts bei jeder Neuplanung ändern kann, entspricht die geplante Dauer der endgültigen Neuplanung.

Work-to-Commit-Ratio

Diese Formel ähnelt der angepassten Geschwindigkeit, mit der Ausnahme, dass wir anstelle des Werts Geplante Dauer aus dem endgültigen Neuplan die geplante Dauer verwenden möchten, die dem Kunden zuerst versprochen wurde. Wir gehen davon aus, dass die ursprüngliche Baseline diese Informationen enthält (und planen von nun an, unsere Projektmanager zu bitten, ihre Projekte so zu planen, dass wir genaue Daten erfassen können). Wir haben diesen Dauerwert von der ursprünglichen Grundlinie erfasst und ihn Erste Dauer genannt.

Durch Division der tatsächlichen Dauer durch die geplante Dauer oder die erste Dauer erhalten wir eine Zahl, die uns sagen kann, wie nahe wir dem Ziel gekommen sind. Wenn die geplante Dauer oder die erste Dauer der tatsächlichen Dauer entspricht, ist der Index 1. Wenn die tatsächliche Dauer größer ist, lautet die Antwort mehr als 1. Je größer die Zahl, desto schlechter haben wir unser Datum erfüllt.

In Anbetracht all dessen, was ich entschieden habe, Status sowohl für die angepasste Geschwindigkeit als auch für das Work-to-Commit-Verhältnis wie folgt zuzuweisen:

* 1.1 oder darunter nannte ich Excellent.
* 1.2 bis 1.5 Ich nannte Nicht schlecht.
* 1,6 bis 1,9 nannte ich arm.
* 2 oder größer nannte ich schrecklich.

**Frage**

Was muss der/die Arbeitende tun, um die Zeit zu verfolgen, die für die Durchführung der Projekte benötigt wird?

**Antwort**

Wir verfolgen nicht die tatsächlichen Stunden, die mit den Projekten hier verbracht wurden, sondern nur die Dauer. Wenn Sie jedoch Stunden verfolgen und die tatsächlichen Stunden über geplante Stunden zur Berechnung der Geschwindigkeit verwenden möchten, können Sie denselben Berichtstyp verwenden, indem Sie die geplanten Stunden mit den tatsächlichen Stunden vergleichen. Geplante Stunden sollten auch von der ursprünglichen Baseline erfasst werden.

**Frage**

Können Filter für Velocity bereitgestellt werden?

**Antwort**

Ich habe zwei Filterregeln für die Velocity-Berichte verwendet:

* Kategorien > ID > Gleich > API-Projektdaten (dies ist das benutzerdefinierte Formular, das alle berechneten Felder enthält). Ich möchte nur Projekte sehen, die dieses benutzerdefinierte Formular verwenden.)
* Projekt > Status > Gleich > Abgeschlossen (Ich möchte nur abgeschlossene Projekte sehen, da sie einen Wert für „Tatsächliche Dauer“ aufweisen, der angibt, wie lange es dauert, bis alles erledigt ist. Aktuelle Projekte liefern keine genaue Ist-Dauer für die Geschwindigkeitsberechnung)

Ich habe auch andere Filter hinzugefügt, um meinen Bericht klein genug zu halten, um ihn für das Webinar zu verwalten, aber in Ihrer Produktionsumgebung würden Sie wahrscheinlich alle Projekte mit dem benutzerdefinierten API-Formular in einem bestimmten Zeitraum sehen wollen. Sie können auch nach dem tatsächlichen Abschlussdatum des Projekts filtern.

**Frage**

Wenn Sie ein Projekt kopieren, werden dann dieselben Baselines in das neue Projekt übernommen?

**Antwort**

Nein, die Baselines sind nicht im kopierten Projekt enthalten

**Frage**

Können Sie mir bei einem Aufgabengenehmigungsprozess zeigen, wie ein Bericht erstellt wird, der ein Audit-Protokoll für jede Aufgabe in einem Projekt mit einem Zeit-/Datumsstempel für jede genehmigende Person bereitstellt?

**Antwort**

Erstellen Sie einen Aufgabenbericht. Klicken Sie auf der Registerkarte Spalten (Ansicht) auf Spalte hinzufügen . Geben Sie in das Feld „In dieser Spalte anzeigen:“ „genehmigen“ ein. Daraufhin werden die verschiedenen Genehmigungsfelder angezeigt, für die Berichte erstellt werden können. Ich würde vorschlagen, dass Sie zuerst eine Spalte für alles hinzufügen (mit Ausnahme von IDs), dann können Sie sehen, welche Informationen angezeigt werden.

Gehen Sie dann zur Registerkarte Filter und fügen Sie eine Filterregel für hinzu:

Aufgabe >> Ist Genehmigung >> gleich >> wahr. Dadurch werden nur Aufgaben angezeigt, an die eine Genehmigung angehängt ist.

Fügen Sie bei Bedarf zusätzliche Filter hinzu.

**Frage**

Ich möchte einen Testbericht erstellen. Eine Liste von Projekten, die zeigen, wie viele Korrekturabzüge sie haben und wie viele Versionen dieses Korrekturabzugs vorhanden sind.

**Antwort**

Erstellen Sie einen Dokumentbericht.

In der Standardansicht wird die Versionsnummer angezeigt. Sie sollten dies beibehalten, aber Sie können auch beliebige andere Spalten ändern.

Bericht nach Projektname gruppieren.

Bericht nach aktueller Version filtern:Proof Die ID ist nicht leer.

Dadurch erhalten Sie eine Liste aller Testsendungen in jedem Projekt. Er enthält für jeden Korrekturabzug eine Zeile und zeigt die Versionsnummer an (die der Gesamtzahl der Versionen entspricht).

**Frage**

Können Sie Velocity auf Aufgabenebene verwenden? Anstatt auf Projektebene?

**Antwort**

Ja, aber Sie müssen das benutzerdefinierte Projektformular kopieren und daraus ein benutzerdefiniertes Aufgabenformular erstellen. Anschließend müssen Sie die Berechnung im Feld Erstes Commit-Datum bearbeiten und den Verweis auf „Standardgrundlinie“ in „Standardgrundlinienaufgabe“ ändern. Tun Sie dasselbe für die erste Dauer. Anschließend können Sie das benutzerdefinierte Formular für die Aufgabe an alle Aufgaben anhängen, die Sie messen möchten. Sie müssen für diese Aufgabenberichte anstelle von Projektberichten erstellen. Sie müssen jedoch weiterhin sicherstellen, dass die ursprüngliche Projekt-Baseline als Standard-Baseline festgelegt ist. Alle Aufgabendaten werden in derselben Baseline mit den Projektdaten aufbewahrt.

**Frage**

Muss das erste Commit-Datum manuell vom Projektbesitzer festgelegt werden? Oder könnte es von existierenden Feldern ausgehen?

**Antwort**

Das erste Commit-Datum wird von der Standard-Baseline erfasst. Solange die standardmäßige Baseline die ursprüngliche Baseline ist, zeigt dies das geplante Abschlussdatum des Projekts zum Zeitpunkt an, als es zum ersten Mal auf den aktuellen Status gesetzt wurde.

**Frage**

Müssen berechnete Felder in benutzerdefinierten Formularen weiterhin regelmäßig aktualisiert werden? Oder wird das jetzt automatisch über Nacht (oder in einem anderen Trigger) geschehen?

**Antwort**

Berechnete Felder werden neu berechnet:

* Wenn ein Benutzer das Objekt bearbeitet
* Bei der Massenbearbeitung mit aktivierten benutzerdefinierten Ausdrücken neu berechnen
* Änderungen am Formular mit der ausgewählten Option „Vorherige Berechnungen aktualisieren“

**Frage**

Wenn die Geschwindigkeit die Dauer berücksichtigt, sollte der Prozentsatz der Fertigstellung in den Projektvoreinstellungen auf der Dauer basieren?

**Antwort**

Nein, die Option Projektvoreinstellungen bezieht sich nur auf die Berechnung des Prozentsatzes der Fertigstellung. Der Dauerwert selbst wird von dieser Einstellung nicht beeinflusst.

**Frage**

Was ist der Unterschied zwischen der ersten und der geplanten Laufzeit?

**Antwort**

Erste Dauer ist die Anzahl der Tage, die Sie dem Kunden ursprünglich für das Projekt zugesagt haben. Wir erhalten diese Zahl von der ursprünglichen Grundlinie, die aufgezeichnet wurde, als das Projekt von „Planung“ in „Aktuell“ geändert wurde.

Geplante Dauer ist die Anzahl der Tage vom Start Ihres Projekts bis zum geplanten Abschlussdatum. Anfangs sind diese beiden Zeiträume gleich, aber wenn das Projekt neu geplant wurde und sich das geplante Abschlussdatum ändert, hat sich auch die geplante Dauer geändert.

Der Wert der Velocity-Berichte beruht auf unserer Fähigkeit zu erkennen, wie stark sich die geplante Dauer gegenüber der ersten Dauer verändert hat. Wir können dies bis zu dem Zeitpunkt sehen, als wir mit der Aufzeichnung von Grundlinien begannen, als Projekte von Planung zu Aktuell wechselten.

**Frage**

Können Mitarbeiter nach Farbe so eingestellt werden, dass sie in allen Berichten gleich sind?

**Antwort**

Wenn Sie in einem Aufgabenbericht nach „Zugewiesen an“ > „Name“ gruppieren, können Sie bestimmten Benutzern auf der Registerkarte „Diagramm“ eine Farbe zuweisen. Wählen Sie einfach die Option Benutzerdefinierte Farben neben dem Feld Zugewiesen an >> Name auf der Registerkarte Diagramm und fügen Sie eine Farbe für jeden Worker hinzu.

**Frage**

Ich versuche festzustellen, ob es möglich ist, ein Dashboard mit einem Bereich zu erstellen, der auf einem benutzerdefinierten Formular auf Aufgabenebene betrachtet wird, um zu sehen, ob es vorhanden ist, und mit einem sekundären Bereich, wenn bestimmte Felder nicht leer sind. Ist das möglich?

**Antwort**

Mal sehen, ob ich deine Frage verstehe. Angenommen, ich habe ein benutzerdefiniertes Aufgabenformular namens „Tammy Form“ mit einem Feld darin namens „Tammy Field“.

Sie möchten einen Aufgabenbericht, der alle Aufgaben anzeigt, an die Tammy Form angehängt ist und in dem Tammy Field einen Wert hat.

Ja, das kannst du machen. In Ihrem Aufgabenbericht benötigen Sie lediglich einen Filter mit zwei Filterregeln:

Kategorien > ID > Gleiches Tammy-Formular

Aufgabe >> Tammy-Feld ist nicht leer

**Frage**

Gibt es eine Möglichkeit, einen Bericht zu erstellen, um nach einem bestimmten benannten Dokument in der Dokumentbibliothek zu suchen? Teil des Dashboards, den wir messen möchten, wenn bestimmte Dokumente vorhanden sind.

**Antwort**

Ja. Sie müssen einen Dokumentbericht erstellen. Es scheint, dass Sie bei jeder Ausführung des Berichts einen bestimmten Dokumentnamen angeben möchten. Wenn dies der Fall ist, würde ich empfehlen, zu Berichtsoptionen zu wechseln und Berichtsaufforderungen auszuwählen. Fügen Sie eine Eingabeaufforderung für Dokument >> Name hinzu.

**Frage**

Können Sie eine Farbe/einen Hexadezimalwert wählen, der nicht auf der Registerkarte „Diagramm“ aufgeführt ist, aber eine neue Farbe darstellt, die ein neuer Hexadezimalwert ist, z. B. eine neue Farbe aus den Markenfarben, um die Berichte anzupassen?

**Antwort**

Ja, Sie können einen beliebigen RGB-Code eingeben, den Sie möglicherweise finden konnten. Dies ist ein Standardcode, der die Menge an Rot, Grün und Blau in der Farbe angibt. Workfront akzeptiert jeden Hexadezimalwert von 000000 bis FFFFFF. Wenn Sie also den Code Ihrer Markenfarbe kennen, können Sie ihn verwenden.

**Frage**

Können Sie die Definition der Berichte im Dashboard (mit einer Beschreibung der Maßnahmen der einzelnen Berichte) erneut festlegen?

**Antwort**

Diagramm zum angepassten Geschwindigkeitsstatus

> Dies zeigt, wie gut wir beim Vergleich der tatsächlichen Projektdauer mit der geplanten Projektdauer die Projekte termingerecht abgeschlossen haben. Die geplante Laufzeit wurde angepasst, da das Projekt während seines Lebenszyklus neu geplant wurde.

Diagramm des Verhältnisses zwischen Arbeit und Commit

> Dies zeigt, wie gut wir beim Vergleich der tatsächlichen Projektdauer mit der ersten Projektdauer die Projekte termingerecht abgeschlossen haben. Die erste Dauer ist die ursprüngliche Zeit, die wir dem Kunden versprochen haben, bis zum Abschluss des Projekts. Die erste Dauer wurde aus dem Wert Dauer des Projekts berechnet, als es zum ersten Mal von „Planung“ in „Aktueller Status“ geändert wurde. Dies war die in der ursprünglichen Baseline aufgezeichnete Dauer.

Velocity Status List Report

> Dieser Bericht enthält alle berechneten benutzerdefinierten Felder und die signifikanten Daten für dieselben Projekte in den Diagrammen. Sie dient dazu, unsere Berechnungen zu überprüfen und auf Wunsch weitere Informationen zu erhalten.

**Frage**

Wie haben Sie die neuen Daten zur X-Achse hinzugefügt?

**Antwort**

Wenn Sie in einem Bericht nach Elementen gruppieren, können Sie ein Diagramm erstellen. Anschließend können Sie auf der Registerkarte Diagramm die X- oder Y-Achse festlegen.

**Frage**

Können Sie den Unterschied zwischen der ersten Dauer und der tatsächlichen Dauer überprüfen?

**Antwort**

Erste Dauer ist die Anzahl der Tage, die Sie dem Kunden ursprünglich für das Projekt zugesagt haben. Wir erhalten diese Zahl von der ursprünglichen Grundlinie, die aufgezeichnet wurde, als das Projekt von „Planung“ in „Aktuell“ geändert wurde.

Tatsächliche Dauer ist die Anzahl der Tage vom Start Ihres Projekts bis zum tatsächlichen Abschlussdatum.

**Frage**

Wie fließt die Projektgrundlinie in diesen Bericht ein?

**Antwort**

Die ursprüngliche Baseline des Projekts enthält das geplante Abschlussdatum und die geplante Dauer, die bestand, als das Projekt zum ersten Mal in den Status Aktuell geändert wurde. Wenn der Prozess das Projekt planen sollte, bevor es auf „aktuell“ gesetzt wird, entspricht dies dem Datum, zu dem Sie sich verpflichtet haben, das Projekt bis zum abzuschließen.

**Frage**

Gibt es eine Möglichkeit, das neue Formular massenhaft auf alte Projekte anzuwenden?

**Antwort**

Ja, Sie können mehrere Projekte aus einer Liste auswählen. In diesem Fall wird oben links in der Liste die Option „Bearbeiten“ angezeigt. Durch Klicken auf Bearbeiten bei der Auswahl mehrerer Objekte gelangen Sie in den so genannten „Bulk Edit“. Auf diese Weise können Sie ein benutzerdefiniertes Formular zu mehreren Projekten hinzufügen.

Um einer großen Anzahl von Projekten benutzerdefinierte Formulare hinzuzufügen, können Sie einen Bericht erstellen, den Sie so filtern, dass er nur die gewünschten Projekte enthält. Klicken Sie dann einfach auf das Kontrollkästchen über dem ersten Kontrollkästchen in der Liste, anstatt Projekte einzeln auszuwählen, und Sie wählen die gesamte Liste aus.

**Frage**

Ist es möglich, doppelte Einträge innerhalb der Gruppierung in einem Arbeitsauftragsbericht zu entfernen, aber nicht gruppierungsübergreifend?

**Antwort**

Die beste Möglichkeit, über Gruppierungen in Listenberichten nachzudenken, ist die folgende:

Zunächst steuern Sie mithilfe der Registerkarte Filter , welche Elemente in der Liste angezeigt werden. Es wird keine doppelten Einträge geben. Der Filter wird auf jedes Objekt angewendet. Wenn er den Filter durchläuft, wird er einmal in der Liste angezeigt, andernfalls überhaupt nicht.

Die nächste Gruppierung wird auf die gefilterte Liste angewendet. Eine Gruppierung identifiziert eine Sache bezüglich der Objekte in der Liste, z. B. den Namen des Portfolios, in dem sie sich befindet (Sie können nicht auf einer Liste von Dingen gruppieren, sondern nur auf einer einzigen Sache). Dann erscheinen alle Objekte mit demselben Wert in dieser Gruppierung, wie alle Projekte im selben Portfolio. Alle Projekte, für die kein Portfolio ausgewählt wurde, werden in der Gruppierung „Kein Wert“ angezeigt.

Daher können Objekte nicht in mehr als einer Gruppierung angezeigt werden. Und ob ein Objekt überhaupt in der Liste angezeigt wird, wird vollständig durch den Filter gesteuert (und ob die Person, die den Bericht ausführt, über die Rechte zum Anzeigen verfügt).

**Frage**

Würden Sie einen anderen Bericht zum Tracken der Geschwindigkeit empfehlen? Nur eine Empfehlung auf hoher Ebene ist großartig, da ich weiß, dass es nicht genug Zeit gibt, um sie im Detail durchzugehen.

**Antwort**

Wie bei jedem Bericht müssen Sie zunächst entscheiden, was Sie wissen möchten. Der nächste Schritt besteht darin, auf diese Informationen zuzugreifen, was in einigen Fällen bedeutet, dass Sie mit dem Tracking beginnen müssen.

Ein Grund, warum ich die tatsächliche Dauer mit zwei Arten von geplanter Dauer vergleiche, war, dass ich dachte, es gäbe interessante Einblicke in die Geschwindigkeit. Die Daten waren auch schon verfügbar, sodass ich nicht anfangen musste, sie zu verfolgen. Mit ein paar Berechnungen konnte ich die Daten in einer Form extrahieren, in der ich darüber berichten konnte.

Es empfiehlt sich jedoch, andere Informationen über Aufgaben oder Projekte zu verfolgen, über die berichtet werden soll.

Workfront verfügt über keine integrierten Geschwindigkeitsberichte. Daher würde ich Ihnen und Ihrem Team empfehlen, darüber zu diskutieren, was Sie wissen möchten, um die Geschwindigkeit zu bestimmen, und dann zu sehen, was Sie nachverfolgen müssen.

**Frage**

Können Sie etwas auf Spaltenebene berechnen? Anstatt ein berechnetes FELD aus einem benutzerdefinierten Formular aufzurufen?

**Antwort**

Es wäre möglich gewesen, einen Wert-Ausdruck im Textmodus zu verwenden, um diese Berechnungen durchzuführen. Wir hätten weder die erste Dauer noch das erste Commit-Datum erreichen können, aber wir mussten sie an einem Ort erfassen, an dem sie sich nicht ändern würden.

Was den Work-to-Commit-Ratio-Status und den angepassten Velocity-Status betrifft, so mussten dies benutzerdefinierte Felder sein, damit wir sie auf der Registerkarte „Diagramm“ verwenden konnten. Die Registerkarte Diagramm erkennt keine Textmodus-Gruppierungen. Sie müssen benutzerdefinierte Felder sein. Und da wir das Work-to-Commit-Verhältnis und die angepasste Geschwindigkeit brauchten, um diese Status zu berechnen, mussten sie auch benutzerdefinierte Felder sein. In diesem Fall mussten sie also alle benutzerdefinierte Felder sein, aber es ist immer gut, beide Möglichkeiten in Betracht zu ziehen und auszuwählen, was am besten funktioniert. Danke für die Frage!

**Frage**

Unsere Projekte ändern sich oft aufgrund von Verzögerungen oder Veränderungen des Kunden. Unser Bericht könnte alle als „schrecklich“ bezeichnen. Was ist eine Empfehlung zur Verfolgung von Änderungsgründen? Wir haben darüber nachgedacht, ein benutzerdefiniertes Formular auf Dokumentebene hinzuzufügen, das einen Änderungsgrund (entweder intern oder Client-Änderung) meldet, uns aber gefragt, was eine Best Practice ist.

**Antwort**

Es empfiehlt sich, ein Dropdown-Menü zu verwenden, um dies nachzuverfolgen. Fügen Sie so viele „Gründe“ hinzu, wie Sie sich vorstellen können, um damit zu beginnen, und fügen Sie dann eine „andere“ Option hinzu, um einen Grund zu erfassen, der nicht auf der Liste ist. Wenn dieser neue Grund häufig auftritt oder angezeigt wird, fügen Sie ihn zu Ihrer Dropdown-Liste hinzu. Sie können problemlos Berichte in einer Dropdown-Liste erstellen und in diesem Feld gruppieren (Sie können keine Gruppen nach Kontrollkästchen oder einem Dropdown-Menü mit Mehrfachauswahl erstellen).

Noch ein Kommentar dazu. Möglicherweise möchten Sie nicht alle Projekte in Ihre Velocity-Berichte aufnehmen. Wenn Sie Fehler beheben oder „gehen, wo noch niemand hingegangen ist“, gehen Sie wahrscheinlich nicht die gleiche Art von Verpflichtung zu einem Fertigstellungsdatum ein, wie wenn Sie ein Haus bauen, das Sie schon viele Male zuvor gebaut haben.

Konzentrieren Sie sich also bei der Geschwindigkeitsberichterstattung auf Bereiche, in denen sie Ihnen beim Erreichen Ihrer Ziele helfen kann.

**Frage**

Wenn ich die standardmäßige Baseline für ein Projekt auf „Original“ festgelegt und dann das aktuelle Projekt entfernt und wieder in die aktuelle Baseline eingefügt habe, ändert sich dann meine standardmäßige Baseline?

**Antwort**

Ja. Jedes Mal, wenn Sie den Status auf Aktuell ändern, erhalten Sie eine neue Grundlinie und es wird der neue Standard sein. Alle vorherigen Baselines sind jedoch weiterhin vorhanden und Sie können die ursprüngliche Baseline manuell wieder als Standard-Baseline festlegen.

**Frage**

Gibt es eine Möglichkeit, in einem Bericht festzulegen, welche Felder bearbeitet werden können? Kann ich Einschränkungen für bestimmte Felder festlegen?

**Antwort**

Sie können die Anzeige- und Bearbeitungsrechte für Felder in einem benutzerdefinierten Formular einschränken. Sie müssen die Felder in einen Abschnitt einbeziehen, und in den Abschnittseinstellungen können Sie die Rechte auswählen, die Benutzende benötigen, um Felder im Abschnitt anzeigen oder bearbeiten zu können.

**Frage**

Kann ein Bericht erstellt werden, der nach einem bestimmten benannten Dokument in der Dokumentbibliothek sucht?

**Antwort**

Ja. Sie müssen einen Dokumentbericht erstellen. Es scheint, dass Sie bei jeder Ausführung des Berichts einen bestimmten Dokumentnamen angeben möchten. Wenn dies der Fall ist, würde ich empfehlen, zu Berichtsoptionen zu wechseln und Berichtsaufforderungen auszuwählen. Fügen Sie eine Eingabeaufforderung für Dokument >> Name hinzu.

**Frage**

Warum sind Werte in Berichten als Spalten, aber nicht zur Auswahl oder Gruppierung verfügbar? Beispiel: Problem Source.

**Antwort**

Der Hauptgrund dafür, dass eine Spalte angezeigt werden kann, aber nicht für die Gruppierung verfügbar ist, könnte darin bestehen, dass sie eine Liste enthalten könnte, z. B. ein benutzerdefiniertes Kontrollkästchen oder Aufgabenzuweisungen. Gruppierung in einer Liste ist nicht zulässig.

**Frage**

Wie kann ich in einem Bericht (nach welchen Feldern) unterscheiden, wann die Eingabe der Std. erfolgt ist und wann die Std. tatsächlich ausgeführt wurden?

**Antwort**

Das Feld Eingabedatum für das Stundenobjekt bezieht sich auf das Datum, an dem die Stunden gearbeitet wurden. Dadurch unterscheidet sich das Eingabedatum von anderen Objekten, wobei es das Datum bedeutet, an dem das Objekt erstellt wurde. Obwohl es kein Erstellungsdatum für Stunden gibt, gibt es ein „Datum der letzten Aktualisierung“, bei dem es sich zunächst um das Erstellungsdatum und anschließend um ein beliebiges Datum handelt, an dem die Stunde danach bearbeitet wurde.

**Frage**

Wie können wir aus Sicht des Reportings auf Baseline-Daten zugreifen? Ich habe ein Projekt mit mehreren Baselines. Ich möchte sehen, wie die einzelnen Aufgaben in jeder Baseline geplant wurden. Gibt es eine Möglichkeit, einen Bericht zu erstellen, der den Projektplan für jede Baseline anzeigt?

**Antwort**

In einem Bericht werden die Felder angezeigt, die Sie für die Baseline sehen möchten, die derzeit als Standard festgelegt ist. Daher können Sie die Baseline ändern und Ihren Bericht aktualisieren, um Felder mit der neuen Baseline anzuzeigen.

Wenn Sie jedoch Informationen zu Ihren Aufgaben grafisch anzeigen möchten, können Sie dies mithilfe der Gantt-Diagramm-Funktion tun. Aktivieren Sie Gantt in einer Aufgabenliste (mithilfe des Gantt-Symbols oben rechts neben „Automatisch speichern„). Navigieren Sie dann zum Einstellungssymbol unten und rechts und klicken Sie darauf. Markieren Sie das Kästchen Grundlinie und es werden alle Grundlinien angezeigt. Sie können diese einzeln auswählen und die Änderungen in Ihren Aufgaben in der Gantt-Ansicht sehen.

**Frage**

Erstellen eines Berichts, um Änderungen seines Status für einen bestimmten Zeitraum zu ermitteln, z. B. im letzten Monat.

**Antwort**

Die Analytics-Funktion in Workfront bietet eine einfache Möglichkeit, historische Daten, einschließlich Statusänderungen, anzuzeigen.

Sie können jedoch auch Statusänderungsinformationen mithilfe eines Notizberichts abrufen. Sie können filtern, um Statusänderungen an Projekten anzuzeigen, wenn Sie das Feld Projektstatus verfolgen.

Gehen Sie also zunächst zu Einrichtung > Schnittstelle > Aktualisierungs-Feeds und stellen Sie sicher, dass der Projektstatus eines der integrierten Felder ist, die verfolgt werden. Wenn es das nicht ist, müssen Sie es hinzufügen.

Erstellen Sie nun einen Notizbericht und gehen Sie folgendermaßen vor:

Auf der Registerkarte Spalten (Ansicht) :

* Ersetzen Sie die Spalte „Notiztext“ durch „Audittext“. Dadurch werden Informationen darüber angezeigt, was sich durch den Status von und in geändert hat
* Lassen Sie die Spalten „Projekt: Name“ und „Eingabedatum“
* Klicken Sie auf die Spalte „Eingabedatum“ und aktivieren Sie dann im Bedienfeld „Spalteneinstellungen“ die Option „Nach dieser Spalte sortieren“. Wenn Sie die letzten Statusänderungen oben sehen möchten, sortieren Sie sie absteigend.

Auf der Registerkarte Gruppierungen :

* Nach Projekt gruppieren: Name

Erstellen Sie auf der Registerkarte Filter die folgenden Filterregeln:

* Hinweis > Prüfungstyp > Gleich > Statusänderung
* Fügen Sie zusätzliche Regeln hinzu, um nach dem Notiz-Eingabedatum zu filtern. Sie können dies lieber von Filtern auslassen und stattdessen eine Eingabeaufforderung verwenden
* Filtern Sie nach Projekt, Portfolio oder anderen Daten.

**Frage**

Können Sie als Planer Berichte für andere Benutzer abrufen?

**Antwort**

Ein Planer kann Berichte erstellen und sie für beliebige Benutzende freigeben, auch für Personen, die keine Benutzenden sind. Wechseln Sie beim Anzeigen des Berichts zu Berichtsaktionen > Freigabe und klicken Sie dann oben rechts im Feld Berichtszugriff auf das Zahnradsymbol. Wählen Sie „Für externe Benutzer öffentlich machen“ aus. Option. Sie können den angegebenen Link kopieren und an jeden senden. Der Bericht wird in Echtzeit im Browser angezeigt.
