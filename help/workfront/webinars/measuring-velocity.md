---
title: Fragen an Experten - Messen der Geschwindigkeit
description: Erfahren Sie, wie Sie die Geschwindigkeit mit [!DNL Workfront] Berichterstellung. Diese Werkstatt wurde am 14. August 2019 aufgenommen.
doc-type: feature video
team: Technical Marketing
jira: KT-9912
last-substantial-update: 2023-08-15T00:00:00Z
exl-id: 83053de2-e386-4243-a9c8-a2ad9d51790f
duration: 4630
source-git-commit: 9a297cda953d4414131657f9ac84580aea0eabeb
workflow-type: tm+mt
source-wordcount: '3967'
ht-degree: 1%

---

# Fragen an Experten - Messen der Geschwindigkeit

Erfahren Sie, wie Sie die Geschwindigkeit mit [!DNL Workfront] Berichterstellung. Diese Werkstatt wurde am 14. August 2019 aufgenommen.

>[!VIDEO](https://video.tv.adobe.com/v/341057/?quality=12)

## Benutzerdefinierte Felder, die in der Präsentation verwendet werden

Sparen Sie Zeit, indem Sie die unten stehenden Berechnungen kopieren und einfügen.

>[!NOTE]
>
>Die Syntax für benutzerdefinierte Feldberechnungen hat sich seit der Präsentation im Jahr 2019 geändert. Die in der Präsentation enthaltenen Konzepte und Anleitungen sind jedoch immer noch korrekt.
>**Die folgenden Berechnungen wurden aktualisiert, um die neuesten Syntaxregeln widerzuspiegeln.**

**Erstes Veröffentlichungsdatum**

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

**Verhältnis zwischen Arbeit und Verpflichtung**

Format:Zahl

Berechnung:

```
ROUND(DIV({actualDurationMinutes},{DE:First Duration}),1)
```

**Status des Verhältnisses zwischen Arbeit und Selbstverpflichtung**

Format:Text

Berechnung:

```
IF({DE:Work-to-Commit Ratio}>2,"Terrible",IF({DE:Work-to-Commit Ratio}>1.6,"Poor",IF({DE:Work-to-Commit Ratio}>1.2,"Not Bad","Excellent")))
```

**Angepasste Geschwindigkeit**

Format:Zahl

Berechnung:

```
ROUND(DIV({actualDurationMinutes},{durationMinutes}),1)
```

**Angepasster Velocity-Status**

Format:Text

Berechnung:

```
IF({DE:Adjusted Velocity}>2,"Terrible",IF({DE:Adjusted Velocity}>1.6,"Poor",IF({DE:Adjusted Velocity}>1.2,"Not Bad","Excellent")))
```

## Fragen und Antworten

**Frage**

Hallo, vielen Dank für die Organisation dieses Webinars. Ich habe eine Frage zu Field in Workfront. In unserem System haben wir ein benutzerdefiniertes Feld namens &quot;State&quot;erstellt, das eine Kombination aus Status und Bedingung darstellt. Dieses Feld des Bundesstaates enthält viele Statuen in tausend Projekten, die für unseren Tableau-Datenextrakt sehr wichtig sind. Jetzt möchten wir dieses Feld jedoch beseitigen und stattdessen das native Feld Bedingungsfeld verwenden. Haben Sie eine Ahnung, wie ich dieses Feld umblättern kann, ohne Daten zu verlieren? Alles, was ich daran denken kann, es zu tun, ohne Daten zu verlieren, ist es, es manuell von Projekt zu Projekt zu wechseln.

**Antwort**

In einer solchen Situation können Sie die Filterung und Massenbearbeitung verwenden, um die Speicherung des Ausfüllens des Bedingungsfelds basierend auf Ihrem benutzerdefinierten Statusfeld zu halbieren.

Hierzu sind folgende Schritte notwendig:

1. Bestimmen Sie, welche Statuswerte Sie Bedingungswerten zuordnen möchten. Angenommen, Sie haben den Statuswert &quot;Late&quot;und &quot;Sehr spät&quot;, die beide dem Bedingungswert &quot;In Trouble&quot;zugeordnet sind.
1. Erstellen Sie einen Projektbericht, der alle Projekte mit dem Status &quot;Verspätet&quot;und &quot;Sehr spät&quot;anzeigt.
1. Führen Sie den Bericht aus. Stellen Sie sicher, dass alle Projekte angezeigt werden (siehe Optionen unten rechts im Bericht).
1. Aktivieren Sie das Kontrollkästchen oben links im Bericht in der Leiste mit Spaltenüberschriften. Dadurch werden alle Projekte im Bericht ausgewählt.
1. Klicken Sie auf die Schaltfläche Bearbeiten oberhalb der Berichtliste.
1. Setzen Sie den Bedingungstyp auf Manuell .
1. Setzen Sie das Bedingungsfeld auf In Trouble .
1. Klicken Sie auf Änderungen speichern


**Frage**

Wie wird Excellent, Not Bad usw. definiert?

**Antwort**

Das war nur ein Beispiel, aber so habe ich es eingerichtet. Zuerst berechnete ich zwei Indizes:

Angepasste Geschwindigkeit

Die Formel hierfür ist die tatsächliche Dauer/die geplante Dauer (die im Feld Dauer eines Projekts gespeichert wird). Da sich die geplante Projektdauer bei jeder Neuplanung des Projekts ändern kann, stellt die geplante Dauer den endgültigen Plan dar.

Verhältnis zwischen Arbeit und Verpflichtung

Diese Formel ähnelt der angepassten Velocity, mit dem Unterschied, dass wir anstelle des Wertes für die geplante Dauer aus dem endgültigen Plan die geplante Dauer verwenden möchten, die dem Kunden zuerst versprochen wurde. Wir gehen davon aus, dass die ursprüngliche Grundlinie diese Informationen enthält (und wir planen von jetzt an, unsere Projektmanager aufzufordern, ihre Projekte auf diese Weise zu planen, damit wir genaue Daten erfassen können). Wir haben diesen Dauerwert aus der ursprünglichen Grundlinie erfasst und ihn &quot;Erste Dauer&quot;genannt.

Indem wir die tatsächliche Dauer entweder durch die geplante Dauer oder die erste Dauer teilen, erhalten wir eine Zahl, die uns mitteilt, wie nah wir am Ziel waren. Wenn die geplante Dauer oder die erste Dauer der tatsächlichen Dauer entspricht, entspricht der Index 1. Wenn die tatsächliche Dauer größer ist, lautet die Antwort mehr als 1. Je größer die Zahl, desto schlechter taten wir bei der Erfüllung unseres Datums.

Also, angesichts all dessen, was ich beschlossen habe, Status für angepasste Velocity und das Verhältnis zwischen Arbeit und Verpflichtung wie folgt zuzuweisen:

* 1.1 oder darunter rief ich Excellent.
* 1.2 bis 1.5 Ich nannte Not Bad.
* 1.6 bis 1.9 Ich nannte Arme.
* 2 oder höher nannte ich Schrecklich.

**Frage**

Was muss der Arbeitnehmer tun, um die Zeit zu verfolgen, die für die Durchführung der Projekte benötigt wird?

**Antwort**

Wir verfolgen hier nicht die tatsächlichen Arbeitszeiten der Projekte, sondern verfolgen und vergleichen nur die Dauer. Wenn Sie jedoch Stunden verfolgen und tatsächliche Stunden über geplante Stunden verwenden möchten, um die Geschwindigkeit zu berechnen, können Sie diese Art von Bericht erstellen, indem Sie geplante Stunden mit tatsächlichen Stunden vergleichen. Sie möchten auch geplante Stunden von der Ausgangsbasis aus erfassen.

**Frage**

Können Sie für Velocity verwendete Filter bereitstellen?

**Antwort**

Ich habe zwei Filterregeln für die Velocity-Berichte verwendet:

* Kategorien >> ID >> Gleich > WPI-Projektdaten (dies ist das benutzerdefinierte Formular, das alle berechneten Felder enthält). Ich möchte nur Projekte sehen, die dieses benutzerdefinierte Formular verwenden.)
* Projekt > Status > Gleich > Abgeschlossen (ich möchte nur abgeschlossene Projekte sehen, da sie einen Wert für die tatsächliche Dauer haben, der angibt, wie lange es dauerte, bis alles fertig gestellt war. Laufende Projekte würden keine genaue tatsächliche Berechnungsdauer liefern.)

Ich habe auch andere Filter hinzugefügt, um meinen Bericht klein genug zu halten, um ihn für das Webinar zu verwalten. In Ihrer Produktionsumgebung möchten Sie jedoch wahrscheinlich alle Projekte mit dem benutzerdefinierten WPI-Formular in einem bestimmten Zeitraum sehen. Möglicherweise möchten Sie nach dem tatsächlichen Abschlussdatum des Projekts filtern.

**Frage**

Wenn Sie ein Projekt kopieren, enthält es dann dieselben Grundlinien für das neue Projekt?

**Antwort**

Nein, die Grundlinien sind nicht im kopierten Projekt enthalten

**Frage**

Können Sie mir für einen Aufgabengenehmigungsprozess zeigen, wie Sie einen Bericht erstellen, der für jede Aufgabe in einem Projekt einen Prüfpfad mit einem Zeitstempel/Datumsstempel für jeden Genehmiger bereitstellt?

**Antwort**

Erstellen Sie einen Aufgabenbericht. Klicken Sie auf der Registerkarte Spalten (Ansicht) auf Spalte hinzufügen . Geben Sie im Feld &quot;In dieser Spalte anzeigen:&quot;den Wert &quot;Genehmigen&quot;ein. Auf diese Weise werden die verschiedenen Validierungsfelder angezeigt, über die Berichte erstellt werden können. Ich schlage vor, dass Sie zunächst eine Spalte für alles hinzufügen (mit Ausnahme von IDs), dann können Sie sehen, welche Informationen angezeigt werden.

Gehen Sie dann zur Registerkarte Filter und fügen Sie eine Filterregel für Folgendes hinzu:

Aufgabe >> Ist Genehmigung >> Gleich >> Wahr. Dadurch werden nur Aufgaben angezeigt, für die eine Genehmigung angehängt ist.

Fügen Sie nach Bedarf weitere Filter hinzu.

**Frage**

Ich möchte einen Testversandbericht erstellen. Eine Liste von Projekten, die zeigen, wie viele Testsendungen sie haben und wie viele Versionen dieses Testversands es gibt.

**Antwort**

Erstellen Sie einen Dokumentbericht.

In der Standardansicht wird die Versionsnummer angezeigt. Sie möchten dies dort lassen, können aber auch andere Spalten ändern.

Gruppieren Sie den Bericht nach Projektname.

Filtern Sie den Bericht nach der aktuellen Version: Die Testversand-ID ist nicht leer.

Dadurch erhalten Sie eine Liste aller Testsendungen in jedem Projekt. Sie enthält für jeden Testversand eine Zeile und zeigt die Versionsnummer an (die mit der Gesamtanzahl der Versionen übereinstimmt).

**Frage**

Können Sie Geschwindigkeit auf Aufgabenebene verwenden? Statt auf Projektebene?

**Antwort**

Ja, Sie müssen jedoch das benutzerdefinierte Projekt-Formular kopieren und ein benutzerdefiniertes Aufgabenformular daraus erstellen. Dann müssen Sie die Berechnung im Feld Erstes Sendedatum bearbeiten und den Verweis auf &quot;Standardgrundlinie&quot;in &quot;Standardgrundaufgabe&quot;ändern. Wiederholen Sie den Vorgang für die erste Dauer. Danach können Sie das benutzerdefinierte Aufgabenformular an alle Aufgaben anhängen, die Sie messen möchten. Sie müssen dafür Aufgabenberichte anstelle von Projektberichten erstellen. Sie müssen jedoch weiterhin sicherstellen, dass die Grundlinie des Originalprojekts als Standardgrundlinie festgelegt ist. Alle Aufgabendaten werden mit den Projektdaten in derselben Grundlinie beibehalten.

**Frage**

Muss das erste Commit-Datum manuell vom Projekteigentümer festgelegt werden? Oder könnte sie aus vorhandenen Feldern abgerufen werden?

**Antwort**

Das erste Veröffentlichungsdatum wird von der Standardgrundlinie erfasst. Solange die Standardgrundlinie die ursprüngliche Basislinie ist, wird das geplante Abschlussdatum des Projekts zum Zeitpunkt der ersten Einstellung auf Aktueller Status angezeigt.

**Frage**

Berechnete Felder in benutzerdefinierten Formularen müssen weiterhin regelmäßig aktualisiert werden. Oder wird das automatisch über Nacht (oder an einem anderen Trigger) geschehen?

**Antwort**

Berechnete Felder werden neu berechnet:

* Wenn ein Benutzer das Objekt bearbeitet
* Bei Massenbearbeitung mit aktivierten benutzerdefinierten Ausdrücken neu berechnen
* Änderungen am Formular mit der ausgewählten Option &quot;Vorherige Berechnungen aktualisieren&quot;

**Frage**

Sollte die Geschwindigkeit die Dauer in Betracht ziehen, sollte die Option &quot;Prozent abgeschlossen&quot;in der Projekterspräferenz auf der Dauer basieren?

**Antwort**

Nein, die Option Projektvoreinstellungen bezieht sich nur darauf, wie Prozent abgeschlossen berechnet wird. Der Wert &quot;Dauer&quot;selbst ist von dieser Einstellung nicht betroffen.

**Frage**

Was ist der Unterschied zwischen der Dauer des ersten und des Plans?

**Antwort**

Die erste Dauer ist die Anzahl der Tage, die Sie dem Kunden ursprünglich versprochen haben, dass das Projekt dauern würde. Wir erhalten diese Zahl von der ursprünglichen Grundlinie, die aufgezeichnet wurde, als das Projekt von Planung zu Aktuell geändert wurde.

Die geplante Dauer ist die Anzahl der Tage vom Beginn Ihres Projekts bis zum geplanten Abschlussdatum. Diese beiden Zeiträume sind zunächst identisch, aber wenn das Projekt jemals neu geplant und das geplante Abschlussdatum geändert wurde, so änderte sich auch die geplante Dauer.

Der Wert der Velocity-Berichte rührt daher, dass wir sehen können, wie stark sich die geplante Dauer von der ersten Dauer geändert hat. Das können wir schon beim ersten Aufzeichnen von Grundlinien sehen, als sich Projekte von Planung auf Aktuell änderten.

**Frage**

Können Sie festlegen, dass Mitarbeiter farblich gekennzeichnet sind, sodass sie in allen Berichten gleich sind?

**Antwort**

Wenn Sie in einem Aufgabenbericht eine Gruppe nach Zugeordnetem > Namen erstellen, können Sie bestimmten Benutzern auf der Registerkarte Diagramm eine Farbe zuweisen. Wählen Sie einfach die Option Benutzerdefinierte Farben neben dem Feld Zugeordneter Benutzer >> Name auf der Registerkarte Diagramm und fügen Sie für jeden Worker eine Farbe hinzu.

**Frage**

Ich versuche festzustellen, ob es möglich ist, ein Dashboard mit einem Bereich zu erstellen, der ein benutzerdefiniertes Formular auf Aufgabenebene betrachtet, um zu sehen, ob es vorhanden ist, und sekundär, wenn bestimmte Felder nicht leer sind. Ist das möglich?

**Antwort**

Mal sehen, ob ich deine Frage verstehe. Angenommen, ich habe ein benutzerdefiniertes Aufgabenformular namens Tammy Form mit einem Feld namens Tammy Field.

Sie möchten einen Aufgabenbericht erstellen, in dem alle Aufgaben angezeigt werden, die mit Tammy Form verbunden sind und in denen Tammy Field einen gewissen Wert hat.

Ja, das kannst du machen. Sie benötigen lediglich einen Filter in Ihrem Aufgabenbericht mit zwei Filterregeln:

Kategorien >> ID Gleich Tammy-Formular

Aufgabe >> Tammy-Feld ist nicht leer

**Frage**

Gibt es eine Möglichkeit, einen Bericht zu erstellen, um in der Dokumentbibliothek nach einem bestimmten benannten Dokument zu suchen? Teil des Dashboards, das wir messen möchten, ob bestimmte Dokumente existieren.

**Antwort**

Ja. Sie müssen einen Dokumentbericht erstellen. Es scheint, dass Sie bei jeder Ausführung des Berichts einen bestimmten Dokumentnamen angeben möchten. Sollte dies der Fall sein, empfehle ich, die Berichtsoptionen aufzurufen und Berichtaufforderungen auszuwählen. Fügen Sie eine Eingabeaufforderung für Dokument >> Name hinzu.

**Frage**

Können Sie einen Farbe-/Hexadezimalwert wählen, der nicht auf der Registerkarte &quot;Diagramm&quot;aufgeführt ist, aber es handelt sich um eine neue Farbe, die ein neuer Hexadezimalwert ist. Beispielsweise eine neue Farbe aus meinen Markenfarben, damit ich die Berichte anpassen kann?

**Antwort**

Ja, Sie können jeden RGB-Code eingeben, den Sie möglicherweise gefunden haben. Dies ist ein Standardcode, der angibt, wie viel Rot, Grün und Blau in der Farbe enthalten sind. Workfront akzeptiert jeden Hexadezimalwert von 00000 bis FFFF. Wenn Sie also den Code Ihrer Markenfarbe kennen, können Sie ihn verwenden.

**Frage**

Können Sie die Definition der Berichte im Dashboard neu angeben (geben Sie eine Beschreibung der Messungen in den einzelnen Berichten an)?

**Antwort**

Angepasstes Velocity-Statusdiagramm

> Dies zeigt, wie gut wir beim rechtzeitigen Abschluss von Projekten beim Vergleich der tatsächlichen Dauer des Projekts mit der geplanten Dauer vorgegangen sind. Die geplante Dauer wurde angepasst, da das Projekt während seines Lebenszyklus neu geplant wurde.

Statusdiagramm für das Verhältnis zwischen Arbeit und Befehl

> Dies zeigt, wie gut wir beim rechtzeitigen Abschluss von Projekten beim Vergleich der tatsächlichen Projektdauer mit der ersten Projektdauer abgeschnitten haben. Die erste Dauer ist die ursprüngliche Zeit, die wir dem Kunden versprochen haben, dass das Projekt abgeschlossen sein würde. Die erste Dauer wurde aus dem Wert für die Dauer des Projekts berechnet, als es zum ersten Mal von Planung in Aktueller Status geändert wurde. Dies war die Dauer, die in der Ausgangslinie verzeichnet wurde.

Velocity-Statuslistenbericht

> Dieser Bericht enthält alle berechneten benutzerdefinierten Felder und die wichtigen Daten für dieselben Projekte in den Diagrammen. Ihr Zweck ist es, uns zu erlauben, unsere Berechnungen zu überprüfen und bei Bedarf weitere Details zu erhalten.

**Frage**

Wie wurden die neuen Daten zur X-Achse hinzugefügt?

**Antwort**

Wenn Sie in einem Bericht nach irgendetwas gruppieren, können Sie ein Diagramm erstellen. Anschließend können Sie die X- oder Y-Achse auf der Registerkarte Diagramm festlegen.

**Frage**

Können Sie die Differenz zwischen der ersten und der tatsächlichen Dauer übergehen?

**Antwort**

Die erste Dauer ist die Anzahl der Tage, die Sie dem Kunden ursprünglich versprochen haben, dass das Projekt dauern würde. Wir erhalten diese Zahl von der ursprünglichen Grundlinie, die aufgezeichnet wurde, als das Projekt von Planung zu Aktuell geändert wurde.

Die tatsächliche Dauer ist die Anzahl der Tage vom Projektstart bis zum tatsächlichen Abschlussdatum.

**Frage**

Wie werden die Projektgrundlagen in diesen Bericht einbezogen?

**Antwort**

Die ursprüngliche Grundlinie des Projekts enthält das geplante Abschlussdatum und die geplante Dauer, die beim ersten Wechsel des Projekts in den Status Aktuell bestanden. Wenn Ihr Prozess das Projekt planen sollte, bevor Sie es auf &quot;Aktuell&quot;festlegen, dann würde dies das Datum darstellen, bis zu dem Sie das Projekt abgeschlossen haben.

**Frage**

Gibt es eine Möglichkeit, das neue Formular auf alte Projekte anzuwenden?

**Antwort**

Ja, Sie können mehrere Projekte aus einer Liste auswählen. In diesem Fall wird oben links in der Liste die Option &quot;Bearbeiten&quot;angezeigt. Wenn Sie auf Bearbeiten klicken, wenn mehrere Objekte ausgewählt sind, gelangen Sie in das so genannte &quot;Massenbearbeitung&quot;. Auf diese Weise können Sie ein benutzerdefiniertes Formular zu mehreren Projekten hinzufügen.

Eine Verknüpfung zum Hinzufügen benutzerdefinierter Formulare zu einer großen Anzahl von Projekten besteht darin, einen Bericht zu erstellen, den Sie filtern, um nur die gewünschten Projekte einzuschließen. Anstatt die Projekte einzeln auszuwählen, aktivieren Sie einfach das Kontrollkästchen oberhalb des ersten Kontrollkästchens in der Liste und wählen Sie die gesamte Liste aus.

**Frage**

Ist es möglich, doppelte Einträge aus der Gruppierung in einem Zuweisungsbericht zu entfernen, aber nicht aus Gruppierungen?

**Antwort**

Die beste Möglichkeit, über Gruppierungen in Listenberichten nachzudenken, ist:

Zuerst steuern Sie auf der Registerkarte Filter , welche Elemente in der Liste angezeigt werden. Es gibt keine doppelten Einträge. Der Filter wird auf jedes Objekt angewendet. Wenn er den Filter durchläuft, wird er einmal in der Liste angezeigt, wenn er nicht erscheint.

Die nächste Gruppierung wird auf die gefilterte Liste angewendet. Eine Gruppierung identifiziert eine Sache mit den Objekten in der Liste, wie den Namen des Portfolios, in dem sie sich befindet (Sie können keine Liste von Dingen gruppieren, sondern nur eine einzige Sache). Dann werden alle Objekte mit demselben Wert in dieser Gruppierung angezeigt, wie alle Projekte im selben Portfolio. Alle Projekte, für die kein Portfolio ausgewählt wurde, werden in der Gruppe &quot;Kein Wert&quot;angezeigt.

Daher können Objekte nicht in mehr als einer Gruppierung angezeigt werden. Und ob ein Objekt überhaupt in der Liste angezeigt wird, wird vollständig vom Filter gesteuert (und wenn die Person, die den Bericht ausführt, über die Berechtigung zum Anzeigen verfügt).

**Frage**

Würden Sie einen anderen Bericht empfehlen, um Velocity zu verfolgen? Nur eine Empfehlung auf hoher Ebene ist großartig, weil ich weiß, dass es nicht genug Zeit gibt, um im Detail zu gehen.

**Antwort**

Wie bei jedem Bericht müssen Sie zuerst entscheiden, was Sie wissen möchten. Der nächste Schritt besteht darin, auf diese Informationen zuzugreifen, was in einigen Fällen bedeutet, dass Sie mit dem Tracking beginnen müssen.

Ein Grund, warum ich mich entschloss, die tatsächliche Dauer mit zwei Arten von geplanter Dauer zu vergleichen, war, dass ich dachte, dass sie interessante Einblicke über Geschwindigkeit liefern würde. Die Daten waren auch bereits verfügbar, sodass ich nicht anfangen musste, sie zu verfolgen. Mit ein paar Berechnungen konnte ich die Daten in einem Formular extrahieren, über das ich berichten könnte.

Sie können aber auch andere Informationen über Aufgaben oder Projekte nachverfolgen, über die Sie Berichte erstellen können.

Workfront verfügt über keine integrierten Velocity-Berichte. Daher empfehle ich Ihnen und Ihrem Team-Brainstorm, was Sie wissen möchten, um die Geschwindigkeit zu ermitteln und dann zu sehen, was Sie verfolgen müssen.

**Frage**

Können Sie irgendetwas auf SPALTENebene berechnen? Statt ein berechnetes FELD aus einem benutzerdefinierten Formular aufzurufen?

**Antwort**

Es wäre möglich gewesen, einen Werteausdruck im Textmodus zu verwenden, um diese Berechnungen durchzuführen. Wir hätten aber nicht die erste Dauer oder das erste Datum der Zusage tun können, wir mussten sie an einem Ort erfassen, an dem sie sich nicht ändern würden.

Was den Status der Arbeitsleistung-Selbstverpflichtung und den angepassten Velocity-Status anbelangt, so mussten diese benutzerdefinierten Felder sein, damit wir sie auf der Registerkarte Diagramm verwenden können. Auf der Registerkarte Diagramm werden Textmodusgruppierungen nicht erkannt. Es müssen benutzerdefinierte Felder angegeben werden. Und da wir das Verhältnis von Arbeit zu Selbstverpflichtung und die angepasste Velocity brauchten, um diese Status zu berechnen, mussten wir sie auch als benutzerdefinierte Felder verwenden. In diesem Fall mussten sie alle benutzerdefinierte Felder sein, aber es ist immer gut, beide Möglichkeiten in Betracht zu ziehen und zu wählen, was am besten funktioniert. Danke für die Frage!

**Frage**

Unsere Projekte ändern sich häufig aufgrund von Verzögerungen bei den Kunden oder Veränderungen im gesamten Projekt. Unser Bericht könnte alle als &quot;schrecklich&quot; bezeichnen. Was ist eine Empfehlung, um Gründe für Veränderungen zu verfolgen? Es wurde überlegt, ein benutzerdefiniertes Formular auf Dokumentebene hinzuzufügen, das Gründe für eine Änderung angibt (entweder interne oder Client-Änderung), sich jedoch zu fragen, was eine Best Practice ist.

**Antwort**

Die Best Practice besteht darin, dies mithilfe eines Dropdown-Menüs zu verfolgen. Fügen Sie so viele &quot;Gründe&quot;hinzu, wie Sie sich vorstellen können, und fügen Sie dann eine &quot;andere&quot;Option hinzu, um einen Grund zu erfassen, der nicht auf der Liste steht. Wenn dieser neue Grund aussieht oder häufig vorkommt, fügen Sie ihn Ihrem Dropdown-Menü hinzu. Sie können problemlos über Dinge in einer Dropdown-Liste berichten und sich auf dieses Feld gruppieren (Sie können keine Gruppen auf Kontrollkästchen oder eine Dropdown-Liste mit Mehrfachauswahl erstellen).

Noch eine Bemerkung dazu. Möglicherweise möchten Sie nicht alle Projekte in Ihre Velocity-Berichte aufnehmen. Wenn Sie Fehler beheben oder &quot;dorthin gehen, wo niemand zuvor hingegangen ist&quot;, machen Sie wahrscheinlich nicht die gleiche Verpflichtung zu einem Abschlussdatum, als ob Sie ein Haus bauen würden, das Sie schon viele Male gebaut haben.

Stellen Sie also sicher, dass Sie Ihre Velocity-Berichte auf Orte konzentrieren, an denen sie Ihnen bei der Erreichung Ihrer Ziele helfen können.

**Frage**

Wenn ich die Standardgrundlinie für ein Projekt auf &quot;Original&quot;setze und das Projekt dann aus dem aktuellen Stand nehme und wieder auf den aktuellen Stand stelle, ändert dies dann meine Standardgrundlinie?

**Antwort**

Ja. Jedes Mal, wenn Sie den Status auf Aktuell ändern, erhalten Sie eine neue Grundlinie und es wird die neue Standardeinstellung sein. Alle vorherigen Grundlinien sind jedoch weiterhin vorhanden und Sie können die ursprüngliche Grundlinie manuell so festlegen, dass sie wieder die Standardgrundlinie ist.

**Frage**

Gibt es eine Möglichkeit, in einem Bericht festzulegen, welche Felder bearbeitbar sind? Kann ich Einschränkungen für bestimmte Felder festlegen?

**Antwort**

Sie können die Anzeige- und Bearbeitungsrechte für Felder in einem benutzerdefinierten Formular einschränken. Sie müssen die Felder in einen Abschnitt einbeziehen. In den Abschnittseinstellungen können Sie die Rechte auswählen, die Benutzer benötigen, um Felder im Abschnitt anzeigen oder bearbeiten zu können.

**Frage**

Können Sie einen Bericht erstellen, der nach einem bestimmten benannten Dokument in der Dokumentbibliothek sucht?

**Antwort**

Ja. Sie müssen einen Dokumentbericht erstellen. Es scheint, dass Sie bei jeder Ausführung des Berichts einen bestimmten Dokumentnamen angeben möchten. Sollte dies der Fall sein, empfehle ich, die Berichtsoptionen aufzurufen und Berichtaufforderungen auszuwählen. Fügen Sie eine Eingabeaufforderung für Dokument >> Name hinzu.

**Frage**

Warum sind in Berichten Werte als Spalte verfügbar, können aber nicht ausgewählt oder gruppiert werden? Beispiel: Problemquelle.

**Antwort**

Der Hauptgrund, aus dem eine Spalte möglicherweise angezeigt, aber nicht gruppiert werden kann, besteht darin, dass sie eine Liste enthalten könnte, z. B. ein benutzerdefiniertes Kontrollkästchen oder Aufgabenzuweisungen. Eine Gruppierung auf einer Liste ist nicht zulässig.

**Frage**

Wie kann ich in einem Bericht (nach welchen Feldern) unterscheiden, wann der Eintrag seiner erfolgte und wann die Stunde tatsächlich ausgeführt wurde?

**Antwort**

Das Feld Datum der Einsendung für das Objekt Stunde bezieht sich auf das Datum, an dem die Stunden bearbeitet wurden. Dadurch unterscheidet sich das Entrypdatum von anderen Objekten, wobei es das Datum der Erstellung des Objekts bezeichnet. Auch wenn es kein Erstellungsdatum für Stunden gibt, gibt es ein &quot;Letztes Aktualisierungsdatum&quot;, das anfänglich das Erstellungsdatum ist und danach jedes Datum, an dem die Stunde bearbeitet wurde.

**Frage**

Wie können wir aus Sicht der Berichterstellung auf Baseline-Daten zugreifen? Ich habe ein Projekt mit mehreren Grundlinien. Ich möchte sehen, wie einzelne Aufgaben in den einzelnen Grundlinien geplant wurden. Gibt es eine Möglichkeit, einen Bericht zu schreiben, der den Projektplan für jede Grundlinie anzeigt?

**Antwort**

Ein Bericht zeigt alle Felder an, die Sie für die aktuell als Standard festgelegte Grundlinie sehen möchten. So können Sie die Grundlinie ändern und Ihren Bericht aktualisieren, um Felder mit der neuen Grundlinie anzuzeigen.

Wenn Sie jedoch Informationen über Ihre Aufgaben grafisch anzeigen möchten, können Sie dies mit der Gantt-Diagrammfunktion tun. Aktivieren Sie Gantt in einer Aufgabenliste (mithilfe des Gantt-Symbols oben rechts neben Autosave), klicken Sie dann auf das Symbol Einstellungen , das sich direkt darunter befindet, rechts und klicken Sie darauf. Markieren Sie das Feld Grundlinie . Daraufhin werden alle Grundlinien angezeigt. Sie können diese einzeln auswählen und die Änderungen in Ihren Aufgaben in der Gantt-Ansicht anzeigen.

**Frage**

So erstellen Sie einen Bericht, um die Statusänderungen für einen bestimmten Zeitraum zu ermitteln, z. B. im letzten Monat.

**Antwort**

Die Analytics-Funktion in Workfront bietet eine hervorragende Möglichkeit, historische Daten, einschließlich Statusänderungen, anzuzeigen.

Sie können jedoch auch Statusänderungsinformationen mit einem Hinweis -Bericht erhalten. Sie können filtern, um Statusänderungen an Projekten anzuzeigen, wenn Sie das Feld Projektstatus verfolgen.

Gehen Sie also zuerst zu Einrichtung > Schnittstelle > Feeds aktualisieren und stellen Sie sicher, dass der Projektstatus eines der integrierten Felder ist, die verfolgt werden. Wenn es nicht ist, müssen Sie es hinzufügen.

Erstellen Sie nun einen Hinweis -Bericht und gehen Sie wie folgt vor:

Auf der Registerkarte Spalten (Ansicht):

* Ersetzen Sie die Spalte &quot;Hinweistext&quot;für &quot;Audit-Text&quot;. Dadurch werden Informationen zu den Statusänderungen angezeigt, von und zu
* Behalten Sie die Spalten &quot;Projekt: Name&quot;und &quot;Datum der Eingabe&quot;bei.
* Klicken Sie auf die Spalte &quot;Eingangsdatum&quot;und aktivieren Sie dann im Bereich &quot;Spalteneinstellungen&quot;die Option &quot;Nach dieser Spalte sortieren&quot;. Wenn Sie die neuesten Statusänderungen am oberen Bildschirmrand sehen möchten, werden sie in absteigender Reihenfolge sortiert.

Im Tab Gruppierungen :

* Gruppe nach Projekt: Name

Erstellen Sie auf der Registerkarte Filter die folgenden Filterregeln:

* Hinweis > Audit-Typ > Gleich > Statusänderung
* fügen Sie zusätzliche Regeln hinzu, um nach dem Eintragsdatum der Notiz zu filtern. Möglicherweise möchten Sie dies aus Filtern ausschließen und stattdessen eine Berichtsaufforderung verwenden
* Filtern Sie nach Bedarf nach Projekt-, Portfolio- oder anderen Daten.

**Frage**

Als Planer können Sie Berichte für andere Benutzer abrufen?

**Antwort**

Ein Planer kann Berichte erstellen und für beliebige Benutzer freigeben, auch für Personen, die keine Benutzer sind. Gehen Sie beim Anzeigen des Berichts zu Berichtaktionen > Freigabe und klicken Sie dann auf das Zahnradsymbol oben rechts im Feld Zugriff auf Bericht . Wählen Sie &quot;Veröffentlichen Sie diese für externe Benutzer&quot;. -Option. Sie können den bereitgestellten Link kopieren und an jeden senden. Der Bericht wird in Echtzeit im Browser angezeigt.
