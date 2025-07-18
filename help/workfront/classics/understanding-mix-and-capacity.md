---
title: Fragen an den Experten - Mix und Kapazität verstehen
description: Erfahren Sie, wie Sie den Mix und die Kapazität in Ihrem Unternehmen messen. Dieses Webinar wurde am 2. Oktober 2019 aufgezeichnet.
doc-type: feature video
team: Technical Marketing
kt: 9913
exl-id: 49cce53f-457b-4973-a0d9-1b5ce2272884
duration: 4239
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '2229'
ht-degree: 0%

---

# Fragen an den Experten - Mix und Kapazität verstehen

Erfahren Sie, wie Sie den Mix und die Kapazität in Ihrem Unternehmen messen. Dieses Webinar wurde am 2. Oktober 2019 aufgezeichnet.

>[!VIDEO](https://video.tv.adobe.com/v/341119/?quality=12)

## Fragen und Antworten

**Frage**

Wie setzt man %s auf ein Säulendiagramm?

**Antwort**

Die im Mixbericht aufgelisteten %-Werte waren vorhanden, weil wir auf der Registerkarte „Diagramm“ „Spalten gruppieren“ und „Auf 100 % gestapelt“ ausgewählt haben. Wenn wir „Gestapelt“ wählen, werden die geplanten Stundensummen und nicht der Prozentsatz angezeigt.

**Frage**

Wenn die Arbeitslast Ihrer Abteilung/Organisation eine Mischung aus Projekten/Aufgaben und Problemen/Anfragen ist, wie können Sie empfehlen, eine allgemeine Überprüfung (in einem Workfront-Bericht) einer API durchzuführen.

**Antwort**

Projekte, Aufgaben und Probleme müssen jeweils eigene Berichte mit eigenen benutzerdefinierten Formularen haben. Sie können jedoch jeweils dasselbe Feld Arbeitstyp verwenden. Möglicherweise möchten Sie die drei Berichte in einem Dashboard anzeigen.

**Frage**

Müssen wir Aufgaben in großen Mengen bearbeiten, um sie operationell oder strategisch zu machen?

**Antwort**

Die von uns vorgeschlagene Technik besteht darin, einen Bericht zu erstellen, der Ihnen eine Liste der Aufgaben liefert, die einsatzbereit sind. Sobald Sie wissen, dass Sie alle Aufgaben gleichzeitig auswählen können, führen Sie eine Massenbearbeitung durch, fügen Sie dann das benutzerdefinierte Formular mit Arbeitstyp an und legen Sie den Arbeitstyp für alle Aufgaben auf „Operativ“ fest. Gehen Sie ebenso vor, um eine Liste strategischer Aufgaben zu erstellen, sie massenweise zu bearbeiten und das benutzerdefinierte Formular hinzuzufügen usw.

Im Webinar werden einige Ideen für benutzerdefinierte Eingabeaufforderungen erwähnt, die Ihnen beim Abrufen einer Liste helfen können, z. B. das Suchen nach bestimmten Wörtern im Aufgabennamen, beim Projektbesitzer, beim Portfolio oder bei den zugewiesenen Benutzern. Das sind nur Ideen. Sie sollten einen Bericht erstellen, der in Ihrer Situation am besten funktioniert.

**Frage**

Wenn ich 4 Kategorien in meinem Mix habe, kann ich dann für jede ein Ziel erstellen und dann einen Bericht über den Delta-Faktor zwischen Prognose vs. Plan vs. Ist erstellen? (4 Kategorien: Kampagne, Geschäftsbereich, Web und Produkt). Wir haben die Kategorien auf Projektebene in benutzerdefinierten Formularen/Feldern. Ziel wäre die Erstellung einer vierteljährlichen Prognose (Budget/Prognose), auf die die geplanten Stunden und letztendlich die tatsächlichen Stunden folgen.

**Antwort**

Wenn Sie alle Kategorien in einem benutzerdefinierten Feld haben (nennen wir es vorerst Arbeitstyp ), erstellen Sie einfach zuerst eine Projektberichtsgruppierung nach „Geplante Stunden“ und dann nach „Arbeitstyp“. Filtern Sie Ihren Projektbericht, um Projekte in Planning innerhalb der gewünschten Datumsbereiche anzuzeigen. Verwenden Sie ein Diagramm mit gruppierten Spalten oder Balken, die zu 100 % gestapelt sind, wenn Prozentsätze angezeigt werden sollen. Dies könnte Ihr Prognosebericht sein.

Sie können den Bericht kopieren und bearbeiten, um einen Bericht auf der Grundlage der aktuellen Projekte zu erstellen und den Mix weiterhin auf der Grundlage der geplanten Stunden anzuzeigen.

Sie können den Bericht erneut kopieren, in „Nach tatsächlichen Stunden anstatt nach geplanten Stunden gruppieren“ ändern und nur abgeschlossene Projekte innerhalb der gewünschten Datumsbereiche anzeigen. Dies zeigt die prozentuale Mischung auf der Basis der tatsächlichen Stunden.

**Frage**

Funktioniert dies, wenn Sie mehrere Kategorie-IDs für ein Projekt oder eine Aufgabe haben?

**Antwort**

Ja, wenn Sie mehrere IDs haben, müssen diese wie folgt durch eine Registerkarte getrennt werden:

```
EXISTS:1:$$EXISTSMOD=NOTEXISTS
EXISTS:1:$$OBJCODE=OBJCAT
EXISTS:1:categoryID=5d76d82600e7926bb51eeb1e0886810e 5d54288d01034619f2eb2c74f6472f18
EXISTS:1:objID=FIELD:ID
```

Die beste Möglichkeit, sie durch ein Tabulatorzeichen zu trennen, besteht darin, zuerst Ihre Liste der Kategorien im Builder zu erstellen. Fügen Sie mehrere benutzerdefinierte Formularnamen ein. Wenn Sie in den Textmodus wechseln, werden sie als IDs angezeigt, die durch Registerkarten getrennt sind.

Die verschiedenen IDs werden als ORs behandelt. Wenn also eine dieser IDs mit der Aufgabe verknüpft ist, wird sie nicht im Bericht angezeigt.

**Frage**

Wird in dem Bericht „ANDed“ angezeigt oder ist dies „ORed“?

**Antwort**

Die einzelnen benutzerdefinierten Eingabeaufforderungen lauten „ANDed“. Wenn Sie also PAM als Projektbesitzer und Bill als der Aufgabe zugewiesen angeben, sehen Sie nur Aufgaben, die Bill zugewiesen sind und in Projekten enthalten sind, in denen PAM der Projektbesitzer ist.

**Frage**

Warum kann man nur nach bestimmten Spalten sortieren? Das heißt, Sie können nicht nach Arbeitsaufträgen sortieren.

**Antwort**

„Arbeitsaufträge“ ist eine Liste, und Sie können in einer Liste von Elementen nicht sortieren oder gruppieren. Sie können nur einzelne Elemente sortieren oder gruppieren.

Um den Punkt zu veranschaulichen, stellen Sie sich eine Liste solcher Zuweisungen für eine Aufgabe vor:

```
Jane
Bill
Dan
```

Und eine Liste mit Zuweisungen wie dieser für eine andere Aufgabe:

```
Bill
Jane
Helen
```

Welche Aufgabe soll zuerst in einer Sortierung angezeigt werden? Man könnte auch „Sortieren nach dem Vornamen in der Liste“ sagen, aber das ist nicht unbedingt nützlich, da man die Reihenfolge nicht kontrollieren kann. Workfront vermeidet das Problem, indem es die Sortierung nach Listen überhaupt nicht zulässt.

Was ist mit Gruppierung nach Liste? Wenn wir nach einer Liste von Namen gruppieren könnten, würden Sie alle Aufgaben, die Jane, Bill, Dan zugewiesen sind, gruppiert und alle Aufgaben, die Jane, Dan, Bill (dieselbe Liste, aber in einer anderen Reihenfolge) zugewiesen sind, in einer anderen Gruppierung finden. Auch hier vermeidet Workfront das Problem, indem es die Gruppierung nach Listen nicht zulässt.

**Frage**

Werden die geplanten Stunden für strategische Aufgaben und die tatsächlichen Stunden für operative Aufgaben verwendet?

**Antwort**

Nein. In unserem Beispiel verwenden wir Geplante Stunden, um den für strategische und operative Aufgaben geplanten Aufwand anzuzeigen. So können wir sie leicht vergleichen, ob in der Vergangenheit, in der Gegenwart oder in der Zukunft. Sie können auch tatsächliche Stunden verwenden, um strategische und operative Aufgaben zu vergleichen, jedoch nur für Aufgaben in der Vergangenheit, da tatsächliche Stunden die Stunden sind, die Personen als die Zeit angegeben haben, die sie tatsächlich mit der Arbeit an den Aufgaben verbracht haben.

**Frage**

Wie sind im Ressourcenplaner Aufgaben zu erfassen, die in der Vergangenheit geplant, aber nicht abgeschlossen wurden? Die geplanten Stunden scheinen nicht vorwärts zu rollen und werden daher in zukünftigen Wochen nicht als Aufgaben/Stunden angezeigt, die Ressourcen benötigen.

**Antwort**

Es gibt keine „automatische“ Vorverlegung nicht abgeschlossener Arbeiten. In diesem Fall müssen Sie Ihr Projekt neu planen. Möglicherweise sind die Ressourcen, die Sie einer bestimmten Aufgabe ursprünglich zugewiesen hatten, im neuen Zeitrahmen nicht verfügbar, sodass der Projektmanager sich dies ansehen und entscheiden muss, wie er die Neuplanung am besten vornimmt. Dies kann bedeuten, dass die Beteiligten einbezogen und Genehmigungen für die Änderungen im Plan eingeholt werden müssen.

**Frage**

Würden Sie empfehlen, den FTE anzupassen, anstatt 2 Stunden pro Tag für die Überprüfung von E-Mails und Unterbrechungen einzugeben?

**Antwort**

Ja, wenn Sie den FTE auf .75 setzen, sodass ein Benutzer im Ressourcenplaner 6 Stunden pro Tag als verfügbar angezeigt wird. Das wird ihre tägliche Verfügbarkeit sein. Wenn Sie möchten, dass sie in verschiedenen Zeiträumen je nach Datum als nicht verfügbar angezeigt werden, z. B. am letzten Tag eines jeden Quartals, dann ist ein Overhead-Projekt der richtige Weg, um dies zu tun.

Einige Personen bevorzugen Overhead-Projekte, weil sie diese selbst erstellen und nach Bedarf ändern können, während sie möglicherweise nicht das Recht haben, ihr eigenes FTE zu bearbeiten.

**Frage**

Sind die Daten für das Dashboard „Team-Kapazität“ für alle verfügbar, für die Sie den Bericht freigeben, unabhängig davon, welche Berechtigungen sie für die Arbeit haben?

**Antwort**

Wenn ein(e) Benutzende(r) nicht berechtigt ist, das Objekt anzuzeigen, wird es nicht im Bericht/Dashboard angezeigt. Wenn Sie jedoch möchten, dass alle Benutzer dieselben Ergebnisse sehen, können Sie zu Berichtsaktionen > Bearbeiten > Berichtseinstellungen gehen und in Ihrem Namen in das Feld „Diesen Bericht ausführen mit Zugriffsrechten von“ eingeben. Dadurch können die in diesem Bericht freigegebenen Benutzer die genauen Ergebnisse sehen, die Sie sehen. Dadurch erhalten sie keinen zusätzlichen Zugriff auf das Ergebnis selbst, sodass einige Ergebnisse möglicherweise angeklickt werden können oder nicht.

**Frage**

Wie kann ein Bericht erstellt werden, der alle einem Projekt zugewiesenen Mitarbeiter insgesamt (nicht auf Aufgabenebene) ausgibt?

**Antwort**

Sie können in einem Projektbericht eine Spalte erstellen, die alle Benutzer anzeigt, die auf der Registerkarte „Personal“ (Projektteam) aufgelistet sind. Sie werden den folgenden Textmodus verwenden:

```
displayname=Project Team
listdelimiter=<p>
listmethod=nested(projectUsers).lists
textmode=true
type=iterate
valuefield=user:name
valueformat=HTML
```

**Frage**

Ich möchte einen Bericht/ein Dashboard, der/das die Arbeitsweise meines Teams enthält. Insbesondere folgende Szenarien: - Projekte in meinem Besitz / Für mich erstellte Projekte / Aufgaben, die ich anderen zugewiesen habe / Aufgaben, die mir zugewiesen wurden

**Antwort**

Projekte in meinem Besitz

Es gibt einen integrierten Bericht mit dem Namen „Aktuelle Projekte“, der alle aktuellen Projekte anzeigt. Sie können dieses Projekt bearbeiten und eine Filterregel hinzufügen:Project > Eigentümer-ID > Gleich > $$USER.IDT und dann den Bericht speichern und in „Projekte in meinem Besitz“ umbenennen.

Für mich erstellte Projekte

Es gibt einen integrierten Bericht mit dem Namen „Meine Projekte“, der Ihnen alle aktuellen Projekte zeigt, an denen Sie dem Projektteam angehören (d. h. Sie sind Verantwortlicher, Sponsor oder einer Aufgabe zugewiesen). Sie sind sich nicht sicher, ob Sie dies wünschen, aber es gibt keine andere Möglichkeit herauszufinden, ob jemand ein Projekt für Sie erstellt hat, außer Sie zum Projektbesitzer oder Sponsor zu machen oder Sie einer Aufgabe zuzuweisen.

Aufgaben, die ich anderen zugewiesen habe

Erstellen Sie einen Aufgabenbericht mit beliebigen Filtern, wechseln Sie dann zur Registerkarte Filter und klicken Sie auf Zum Textmodus wechseln . Fügen Sie diesen Code zu dem hinzu, was bereits vorhanden ist:

```
EXISTS:1:$$OBJCODE=ASSGN
EXISTS:1:taskID=FIELD:ID
EXISTS:1:assignedByID=$$USER.ID
```

Dadurch werden alle Aufgaben angezeigt, bei denen der angemeldete Benutzer mindestens einem der aktuellen Bearbeiter zugewiesen hat. Wenn Verantwortliche von mehreren Personen zugewiesen wurden, wird nur der Name der ersten Person, die die Person zugewiesen hat, auf der Landingpage der Aufgabe als „Angefordert von“ angezeigt. Wenn Sie alle zugewiesenen Personen und Personen anzeigen möchten, die sie zugewiesen haben, können Sie Ihrer Ansicht eine Spalte hinzufügen, in den Textmodus wechseln und alles, was dort vorhanden ist, durch diese ersetzen:

```
displayname=All Assignees and Requesters
listdelimiter=<p>
listmethod=nested(assignments).lists
textmode=true
type=iterate
valueexpression=CONCAT("Assigned To: ",{assignedTo}.{name},"; Requested By: ",{assignedBy}.{name})
valueformat=HTML
```

Mir zugewiesene Aufgaben

Es gibt einen integrierten Bericht mit dem Namen „Meine Aufgaben“, der Ihnen alle unvollständigen Aufgaben in aktuellen Projekten zeigt, in denen Sie der Aufgabenbesitzer sind. Ich schlage vor, dass Sie den Filter ändern, um Ihnen alle Aufgaben anzuzeigen, bei denen Sie einer der potenziell vielen zugewiesenen Benutzer sind, nicht nur der Aufgabenbesitzer. Entfernen Sie dazu die Filterregel

```
Task > Assigned To ID > Equal > $$USER.ID 
```

und durch ersetzt

```
Assignment Users > ID > Equal > $$USER.ID
```

**Frage**

Gibt es eine Möglichkeit, Beschriftungen in Diagrammen anzupassen? Ich habe festgestellt, dass, wenn ich ein Diagramm erstellt habe, um den Projektstatus widerzuspiegeln, der Name der Hauptgruppe letztendlich in der Beschriftung enthalten ist.

**Antwort**

Beschriftungen in Diagrammen verwenden den Feldnamen des Elements, nach dem Sie gruppieren. Die einzige Möglichkeit, die Beschriftungen zu ändern, besteht also darin, ein berechnetes benutzerdefiniertes Feld mit einem beliebigen Namen zu verwenden. Fügen Sie im Abschnitt Berechnung des Felds den Feldnamen des nativen Felds ein, nach dem Sie gruppieren möchten.

**Frage**

Wie können Sie die Berichtsbalken für Chucks Team-Arbeitsaufträge farblich kennzeichnen? D.h. Bernstein für hinten, Rot für spät &amp; Grün für pünktlich? Können Sie auch die Reihenfolge ändern, sodass sie logischer ist, d. h. rot/bernsteinfarben/grün oder umgekehrt?

**Antwort**

Um die im Bericht verwendeten Farben für die Optionen des Fortschrittsstatus zu ändern, bearbeiten Sie den Bericht und klicken Sie auf die Registerkarte Diagramm . Suchen Sie nach der Dropdown-Liste „Benutzerdefinierte Farben >&quot;. Er wird neben dem Feld „Linke Achse (Y)“ oder dem Feld „Daten gruppieren nach“ angezeigt, je nachdem, ob Sie Spalten oder Balken gruppieren möchten oder nicht. In dieser Dropdown-Liste können Sie Farben auswählen. Wenn Sie auf die Zahlen unten rechts in den Farboptionen klicken, können Sie Ihre Farbe aus einer größeren Palette auswählen.

Leider lässt sich die Reihenfolge dieser Felder nicht ändern.

**Frage**

Können Sie ein Diagramm erstellen, das auf die Anzahl der Projekte verweist, denen ein Worker eine Aufgabe zugewiesen wird?

**Antwort**

Ja, so geht&#39;s:

* Erstellen eines Projektberichts
* Wenn der betreffende Benutzer der angemeldete Benutzer ist, sollte der Filter diese Zeile enthalten:

```
   Project Users > ID > Equal >$$USER.ID 
```

* Wenn nicht, setzen Sie den Benutzernamen an die Stelle von [!DNL $$USER.ID]. Dadurch werden alle Projekte angezeigt, denen diese Person eine Aufgabe zugewiesen wurde oder deren Eigentümer oder Sponsor sie ist. Wenn Sie nur Projekte anzeigen möchten, denen Aufgaben zugewiesen sind, sollten Sie diese beiden zusätzlichen Filterregeln hinzufügen:

```
   Project > Owner ID > Not Equal > $$USERID
   Project > Sponsor ID > Not Equal > $$USERID
```

* Erstellen Sie mindestens eine Gruppierung, damit Sie ein Diagramm erstellen können. Gruppieren Sie alles, wie die Firma. Klicken Sie dann auf die Registerkarte Diagramm und wählen Sie ein Diagramm aus. „Datensatzanzahl“ ist der Standard für eine Achse. Dies ist die Anzahl der Projekte, denen der Benutzer einen Arbeitsauftrag zugewiesen hat.

Wenn einem Benutzer ein Arbeitsauftrag für ein Projekt erteilt wird (der einer Aufgabe oder einem Projektbesitzer oder Projektsponsor zugewiesen ist), wird diese Person zum Projektteam hinzugefügt und kann auf der Registerkarte „Personal“ unter der Unterregisterkarte „Personen“ angezeigt werden. Wenn ein(e) Benutzende(r) vom Status als Projektbesitzer, Sponsor oder mit Aufgabenzuweisungen entfernt wird, ist sein Name noch im Projektteam. Sie muss manuell entfernt werden, wenn Sie sie entfernen möchten. Beachten Sie, dass sich dies auf die Genauigkeit Ihrer Berichtsergebnisse auswirken kann. Um jemanden aus dem Projektteam zu entfernen, gehen Sie zu Personal > Personen, wählen Sie die Person(en) aus und klicken Sie dann auf die Schaltfläche Entfernen , die über der Liste angezeigt wird.

**Frage**

Wie kann man die absteigende Reihenfolge einer Spalte im Textmodus (in einer Gruppierung) ändern?

**Antwort**

Sie können beim Erstellen eines Berichts auf der Registerkarte „Spalten (Ansicht)“ die meisten Spalten sortieren. Dadurch wird Ihr gesamter Listenbericht sortiert, wenn Sie keine Gruppierungen haben. Wenn Sie Gruppierungen haben, wird innerhalb jeder Gruppierung nach dieser Auswahl sortiert.

**Frage**

Wie kann ich eine Spalte erstellen, in der die Team-Mitglieder identifiziert werden, die einer Genehmigungsphase zugewiesen sind?

**Antwort**

Wenn Sie einen Aufgaben- oder Problem-/Anfragebericht ausführen, ist in der Report Builder eine Spalte mit dem Namen „Genehmiger und Status“ verfügbar, über die diese Informationen abgerufen werden.
