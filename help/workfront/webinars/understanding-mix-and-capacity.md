---
title: Fragen an Experten - Mischung und Kapazität verstehen
description: Erfahren Sie, wie Sie Mix und Kapazität in Ihrem Unternehmen messen können. Dieses Webinar wurde am 2. Oktober 2019 aufgenommen.
activity: use
doc-type: feature video
team: Technical Marketing
kt: 9913
exl-id: 5993c6c3-0583-4d1c-94aa-2e64a699e7f1
source-git-commit: ca06e5a8b1602a7bcfb83a43f529680a5a96bacf
workflow-type: tm+mt
source-wordcount: '2224'
ht-degree: 1%

---

# Fragen an Experten - Mischung und Kapazität verstehen

Erfahren Sie, wie Sie Mix und Kapazität in Ihrem Unternehmen messen können. Dieses Webinar wurde am 2. Oktober 2019 aufgenommen.

>[!VIDEO](https://video.tv.adobe.com/v/341119/?quality=12)

## Fragen und Antworten

**Frage**

Wie setzt man %s in ein Spaltendiagramm?

**Antwort**

Die im Mix-Bericht aufgelisteten Prozentwerte waren vorhanden, da wir auf der Registerkarte &quot;Diagramm&quot;die Option &quot;Gruppenspalten&quot;und die Option &quot;Auf 100 % gestapelt&quot;ausgewählt haben. Wenn wir &quot;Gestapelt&quot;wählen, werden die geplanten Stundensummen und nicht der Prozentsatz angezeigt.

**Frage**

Wie empfehlen Sie eine allgemeine Überprüfung (in einem Workfront-Bericht) einer WPI, wenn die Arbeitslast Ihrer Abteilung/Organisationen aus einer Mischung aus Projekten/Aufgaben und Problemen/Anforderungen besteht?

**Antwort**

Projekte, Aufgaben und Probleme müssen jeweils über eigene Berichte mit eigenen benutzerdefinierten Formularen verfügen. Sie können jedoch jeweils dasselbe Feld &quot;Arbeitstyp&quot;verwenden. Sie können die drei Berichte in einem Dashboard anzeigen lassen.

**Frage**

Müssen Aufgaben in großen Mengen bearbeitet werden, um sie operationell oder strategisch zu gestalten?

**Antwort**

Die Technik, die wir vorschlagen, besteht darin, einen Bericht zu erstellen, der es Ihnen ermöglicht, eine Liste von Aufgaben zu erhalten, die funktionsfähig sind. Sobald Sie alle Aufgaben gleichzeitig auswählen können, bearbeiten Sie sie stapelweise, fügen Sie das benutzerdefinierte Formular mit Arbeitstyp hinzu und legen Sie den Arbeitstyp für alle Aufgaben gleichzeitig auf &quot;Operativ&quot;fest. Auf die gleiche Weise werden Sie eine Liste strategischer Aufgaben sammeln, diese stapelweise bearbeiten und das benutzerdefinierte Formular hinzufügen usw.

Im Webinar werden einige Ideen für benutzerdefinierte Eingabeaufforderungen erwähnt, die Ihnen dabei helfen können, eine Liste zu erhalten, z. B. das Suchen nach bestimmten Wörtern im Aufgabennamen, dem Projekteigentümer, dem Portfolio oder den zugewiesenen Benutzern. Das sind nur Ideen. Sie sollten einen Bericht erstellen, der in Ihrer Situation am besten funktioniert.

**Frage**

Wenn ich vier Kategorien in meinem Mix habe, kann ich dann für jeden ein Ziel erstellen und dann über die Unterschiede zwischen Prognose vs. Plan vs. tatsächlichen Werten berichten? (4 Kategorien: Campaign, Business Unit, Web und Produkt). Die Kategorien befinden sich auf Projektebene in benutzerdefinierten Formularen/Feldern. Ziel wäre die Erstellung einer vierteljährlichen Prognose (Budget/Prognose) und die anschließende Verfolgung der geplanten und letztlich tatsächlichen Stunden.

**Antwort**

Wenn Sie alle Kategorien in einem benutzerdefinierten Feld haben (nennen wir es vorerst &quot;Arbeitstyp&quot;), erstellen Sie einfach einen Projektbericht, der zuerst nach geplanten Stunden und danach nach Arbeitstyp gruppiert. Filtern Sie Ihren Projektbericht, um Projekte in der Planung innerhalb der gewünschten Datumsbereiche anzuzeigen. Verwenden Sie ein Diagramm mit gruppierten Spalten oder Balken, die auf 100 % gestapelt sind, wenn Sie Prozentsätze anzeigen möchten. Dies könnte Ihr Prognosebericht sein.

Sie können den Bericht kopieren und bearbeiten, um einen Bericht zu erstellen, der auf aktuellen Projekten basiert, und dennoch die Mischung basierend auf geplanten Stunden anzeigen.

Sie können den Bericht erneut kopieren, ihn in eine Gruppe nach tatsächlichen Stunden anstelle von geplanten Stunden ändern und nur abgeschlossene Projekte innerhalb der gewünschten Datumsbereiche anzeigen. Dies würde den prozentualen Mix basierend auf den tatsächlichen Stunden zeigen.

**Frage**

Funktioniert das, wenn Sie mehrere Kategorie-IDs für ein Projekt oder eine Aufgabe haben?

**Antwort**

Ja, wenn Sie mehrere IDs haben, müssen diese durch eine Registerkarte getrennt werden, wie hier gezeigt:

```
EXISTS:1:$$EXISTSMOD=NOTEXISTS
EXISTS:1:$$OBJCODE=OBJCAT
EXISTS:1:categoryID=5d76d82600e7926bb51eeb1e0886810e 5d54288d01034619f2eb2c74f6472f18
EXISTS:1:objID=FIELD:ID
```

Die beste Möglichkeit, sie durch Tabulatorzeichen zu trennen, besteht darin, zuerst Ihre Liste von Kategorien im Builder zu erstellen. Geben Sie mehrere benutzerdefinierte Formularnamen ein. Wenn Sie in den Textmodus wechseln, werden diese als durch Tabulatoren getrennte IDs angezeigt.

Die verschiedenen IDs werden als ORs behandelt. Wenn also eine von ihnen an die Aufgabe angehängt ist, wird sie nicht im Bericht angezeigt.

**Frage**

Werden im Bericht &quot;ANDed&quot;oder &quot;ORed&quot;angezeigt?

**Antwort**

Die einzelnen benutzerdefinierten Eingabeaufforderungen lauten &quot;ANDed&quot;. Wenn Sie also Pam als Projekteigentümer und Bill als der Aufgabe zugewiesen angeben, sehen Sie nur Aufgaben, die Bill zugewiesen sind und sich in Projekten befinden, in denen Pam Projektinhaber ist.

**Frage**

Warum können Sie nur nach bestimmten Spalten sortieren? Sie können also nicht nach Zuweisungen sortieren.

**Antwort**

&quot;Zuweisungen&quot;ist eine Liste und Sie können keine Elemente in einer Liste sortieren oder gruppieren. Sie können nur ein einzelnes Element sortieren oder gruppieren.

Um diesen Punkt zu veranschaulichen, stellen Sie sich eine Liste von Zuweisungen wie diese für eine Aufgabe vor:

```
Jane
Bill
Dan
```

Eine Liste von Zuweisungen wie diese für eine andere Aufgabe:

```
Bill
Jane
Helen
```

Welche Aufgabe sollte in einer Art zuerst angezeigt werden? Sie könnten &quot;nach dem Vornamen in der Liste sortieren&quot;sagen, aber dies ist nicht unbedingt nützlich, da Sie die Reihenfolge nicht steuern können. Workfront vermeidet das Problem, indem es Ihnen überhaupt nicht gestattet, Listen nach Listen zu sortieren.

Wie sieht es mit der Gruppierung nach Liste aus? Wenn wir nach einer Liste von Namen gruppieren könnten, würden Sie alle Aufgaben, die Jane, Bill, Dan zugewiesen sind, gruppieren und alle Aufgaben, die Jane, Dan, Bill (gleiche Liste, aber in einer anderen Reihenfolge) zugewiesen sind, in einer anderen Gruppierung finden. Auch hier vermeidet Workfront das Problem, indem es keine Gruppierung nach Listen zulässt.

**Frage**

Werden geplante Stunden für strategische Aufgaben und tatsächliche Betriebsstunden verwendet?

**Antwort**

Nein. In unserem Beispiel verwenden wir geplante Stunden, um den geplanten Aufwand für sowohl strategische als auch operative Aufgaben zu zeigen. Dadurch können wir sie leicht vergleichen, ob in der Vergangenheit, in der Gegenwart oder in der Zukunft. Sie können auch die tatsächlichen Stunden verwenden, um strategische und operative Aufgaben zu vergleichen, aber nur für Aufgaben in der Vergangenheit, da die tatsächlichen Stunden die Stunden sind, die die Menschen als die Zeit gemeldet haben, die sie tatsächlich mit den Aufgaben verbracht haben.

**Frage**

Wie werden im Ressourcenplaner Aufgaben berücksichtigt, die in der Vergangenheit geplant, aber noch nicht abgeschlossen wurden? Die geplanten Stunden scheinen sich nicht weiterzuentwickeln und werden daher in zukünftigen Wochen nicht als Aufgaben/Stunden angezeigt, die Ressourcen benötigen.

**Antwort**

Es gibt keine &quot;automatische&quot;Weiterleitung nicht abgeschlossener Arbeiten. In diesem Fall müssen Sie Ihr Projekt neu planen. Vielleicht sind die Ressourcen, die Sie einer bestimmten Aufgabe ursprünglich zugewiesen hatten, im neuen Zeitrahmen nicht verfügbar, daher muss sich der Projektmanager damit beschäftigen und entscheiden, wie die Neuplanung am besten durchgeführt werden kann. Dies kann bedeuten, dass Interessenträger einbezogen und Genehmigungen für die Änderungen des Plans erhalten werden.

**Frage**

Wäre es empfehlenswert, die VZÄ nicht anzupassen, anstatt 2 Stunden pro Tag zur Überprüfung von E-Mails und Pausen einzugeben?

**Antwort**

Ja, wenn Sie die FTE auf 0,75 festlegen, wird einem Benutzer im Ressourcenplaner 6 Stunden pro Tag angezeigt. Das wird ihre Verfügbarkeit jeden Tag sein. Wenn Sie sie je nach Datum für verschiedene Zeiträume anzeigen möchten, z. B. wenn sie am letzten Tag eines jeden Quartals nicht verfügbar sind, ist dies durch ein Overhead-Projekt möglich.

Manche Leute bevorzugen Gemeinkosten-Projekte, weil sie sie für sich selbst erstellen und sie bei Bedarf ändern können, während sie möglicherweise nicht über die Rechte verfügen, ihre eigene FTE zu bearbeiten.

**Frage**

Stehen die Daten für das Dashboard zur Teamkapazität jedem zur Verfügung, für den Sie den Bericht freigeben, unabhängig von den Berechtigungen, die er für die Arbeit hat?

**Antwort**

Wenn ein Benutzer nicht über die Berechtigung zum Anzeigen des Objekts verfügt, ist es im Bericht/Dashboard nicht sichtbar. Wenn Sie jedoch möchten, dass alle die gleichen Ergebnisse sehen, können Sie &quot;Berichtaktionen&quot;> &quot;Bearbeiten&quot;> &quot;Berichtseinstellungen&quot;aufrufen und in das Feld &quot;Diesen Bericht mit Zugriffsrechten ausführen&quot;eingeben. Dadurch können die Benutzer, die für diesen Bericht freigegeben sind, die genauen Ergebnisse sehen, die Ihnen angezeigt werden. Sie erhalten keinen zusätzlichen Zugriff auf das Ergebnis selbst, sodass einige Ergebnisse angeklickt werden können oder nicht.

**Frage**

Wie können wir einen Bericht erstellen, der alle Mitarbeiter anzeigt, die einem Projekt insgesamt zugewiesen sind (nicht auf Aufgabenebene)?

**Antwort**

Sie können eine Spalte in einem Projektbericht erstellen, die alle Benutzer anzeigt, die auf der Registerkarte &quot;Staffing&quot;(Projektteam) aufgelistet sind. Sie sollten den folgenden Textmodus verwenden:

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

Ich möchte einen Bericht/ein Dashboard haben, der bzw. das die Funktionsweise meines Teams beinhaltet. Insbesondere die folgenden Szenarien: - Projekte, deren Inhaber ich bin/Projekte, die für mich erstellt wurden/Aufgaben, die ich anderen zugewiesen habe/Aufgaben, die mir zugewiesen sind

**Antwort**

Projekte, die ich besitze

Es gibt einen integrierten Bericht mit dem Namen &quot;Aktuelle Projekte&quot;, der alle aktuellen Projekte anzeigt. Sie können dieses Projekt bearbeiten und eine Filterregel hinzufügen: Projekt > Eigentümer-ID > Gleich > $$USER.IDTspeichern und den Bericht in &quot;Projekte, die ich besitze&quot;umbenennen.

Für mich erstellte Projekte

Es gibt einen integrierten Bericht mit dem Namen &quot;Meine Projekte&quot;, in dem alle aktuellen Projekte angezeigt werden, in denen Sie im Projektteam sind (d. h. Sie sind Inhaber, Sponsor oder der Aufgabe zugewiesen). Nicht sicher, ob dies das ist, was Sie verlangen, aber es gibt keine andere Möglichkeit zu wissen, ob jemand ein Projekt für Sie erstellt hat, außer Sie zum Projekteigentümer, Sponsor oder Zuweisung zu einer Aufgabe zu machen.

Aufgaben, die ich anderen zugewiesen habe

Erstellen Sie einen Aufgabenbericht mit den gewünschten Filtern. Gehen Sie dann zur Registerkarte Filter und klicken Sie auf In Textmodus wechseln . Fügen Sie diesen Code zu dem bereits vorhandenen hinzu:

```
EXISTS:1:$$OBJCODE=ASSGN
EXISTS:1:taskID=FIELD:ID
EXISTS:1:assignedByID=$$USER.ID
```

Auf diese Weise werden alle Aufgaben angezeigt, denen der angemeldete Benutzer mindestens einen der aktuellen Verantwortlichen zugewiesen hat. Wenn die Zuweisung von mehreren Benutzern erfolgt ist, wird nur der Name der ersten Person, der die Person zugewiesen hat, auf der Aufgabenlandeseite als &quot;Anfordert von&quot;angezeigt. Wenn Sie alle zugewiesenen Personen sehen möchten und die ihnen jeweils eine Spalte zugewiesen haben, können Sie eine Spalte zu Ihrer Ansicht hinzufügen, wechseln Sie in den Textmodus und ersetzen Sie das vorhandene Element durch Folgendes:

```
displayname=All Assignees and Requesters
listdelimiter=<p>
listmethod=nested(assignments).lists
textmode=true
type=iterate
valueexpression=CONCAT("Assigned To: ",{assignedTo}.{name},"; Requested By: ",{assignedBy}.{name})
valueformat=HTML
```

Aufgaben, die mir zugewiesen sind

Es gibt einen integrierten Bericht mit dem Namen &quot;My Tasks&quot;, der alle unvollständigen Aufgaben für aktuelle Projekte anzeigt, in denen Sie der Aufgabenbesitzer sind. Ich schlage vor, dass Sie den Filter so ändern, dass alle Aufgaben angezeigt werden, denen Sie eine der potenziell vielen zugewiesenen Benutzer sind, nicht nur der Aufgabenbesitzer. Entfernen Sie dazu die Filterregel

```
Task > Assigned To ID > Equal > $$USER.ID 
```

und ersetzt sie durch

```
Assignment Users > ID > Equal > $$USER.ID
```

**Frage**

Gibt es eine Möglichkeit, Beschriftungen in Diagrammen anzupassen? Ich habe festgestellt, dass bei der Erstellung eines Diagramms, das den Projektstatus widerspiegelt, der Name der Startseite schließlich in die Beschriftung aufgenommen wird.

**Antwort**

Beschriftungen in Diagrammen verwenden den Feldnamen der Gruppe. Die einzige Möglichkeit, die Beschriftungen zu ändern, besteht darin, ein berechnetes benutzerdefiniertes Feld mit dem gewünschten Namen zu verwenden. Geben Sie im Berechnungsabschnitt des Felds den Feldnamen des nativen Felds ein, nach dem Sie eine Gruppe bilden möchten.

**Frage**

Wie können Sie den Code der Berichtbalken auf Chuck&#39;s Team Assignements farblich markieren? Ich bin z.B. gelb für hinten, rot für spät und grün für pünktlich? Können Sie die Reihenfolge auch logischer ändern, d. h. rot/gelb/grün oder umgekehrt?

**Antwort**

Um die Farben zu ändern, die im Bericht für die Fortschrittsstatus-Optionen verwendet werden, bearbeiten Sie den Bericht und klicken Sie auf die Registerkarte Diagramm . Suchen Sie nach der Dropdown-Liste &quot;Benutzerdefinierte Farben >&quot;. Sie wird neben dem Feld &quot;Linke (Y) Achse&quot;oder dem Feld &quot;Gruppieren von Daten nach&quot;angezeigt, je nachdem, ob Sie Spalten oder Balken gruppieren möchten oder nicht. In dieser Dropdown-Liste können Sie Farben auswählen. Wenn Sie auf die Zahlen unten rechts der Farboptionen klicken, können Sie Ihre Farbe aus einer größeren Palette auswählen.

Leider lässt sich die Reihenfolge nicht ändern.

**Frage**

Können Sie ein Diagramm erstellen, in dem auf die Anzahl der Projekte verwiesen wird, denen einem Worker eine Aufgabe zugewiesen wurde?

**Antwort**

Ja, wie folgt:

* Erstellen eines Projektberichts
* Wenn der fragliche Benutzer der angemeldete Benutzer ist, sollte der Filter die folgende Zeile enthalten:

```
   Project Users > ID > Equal >$$USER.ID 
```

* Wenn nicht, setzen Sie den Benutzernamen anstelle von [!DNL $$USER.ID]. Dadurch werden alle Projekte angezeigt, bei denen diese Person mit einer Aufgabe betraut ist oder der Eigentümer oder Sponsor ist. Wenn Sie nur Projekte sehen möchten, denen Aufgaben zugewiesen sind, sollten Sie diese beiden zusätzlichen Filterregeln hinzufügen:

```
   Project > Owner ID > Not Equal > $$USERID
   Project > Sponsor ID > Not Equal > $$USERID
```

* Erstellen Sie mindestens eine Gruppierung, um ein Diagramm zu erstellen. Gruppieren Sie zu allem, zum Beispiel zu Unternehmen. Klicken Sie dann auf die Registerkarte Diagramm und wählen Sie ein Diagramm aus. &quot;Datensatzanzahl&quot;ist die Standardeinstellung für eine Achse. Dies ist die Anzahl der Projekte, in denen der Benutzer eine Zuweisung hat.

Wenn einem Benutzer eine Zuweisung zu einem Projekt zugewiesen wird (das einer Aufgabe, einem Projekteigentümer oder einem Projektsponsor zugewiesen ist), wird diese Person zum Projektteam hinzugefügt und kann auf der Registerkarte &quot;Staffing&quot;auf der Unterregisterkarte &quot;Personen&quot;angezeigt werden. Wenn ein Benutzer nicht mehr der Projekteigentümer, Sponsor oder eine Aufgabenzuweisung ist, liegt sein Name weiterhin im Projektteam. Sie muss manuell entfernt werden, wenn sie entfernt werden soll. Beachten Sie, dass dies die Genauigkeit Ihrer Berichtsergebnisse beeinträchtigen könnte. Um eine Person aus dem Projektteam zu entfernen, gehen Sie zu Personal > Personen , wählen Sie die Person(en) aus und klicken Sie dann auf die Schaltfläche Entfernen , die über der Liste angezeigt wird.

**Frage**

Wie kann die absteigende Reihenfolge einer Spalte im Textmodus (in einer Gruppierung) geändert werden?

**Antwort**

Sie können die meisten Spalten auf der Registerkarte Spalten (Ansicht) beim Erstellen eines Berichts sortieren. Wenn keine Gruppierungen vorhanden sind, wird der gesamte Listenbericht sortiert. Wenn Sie Gruppierungen haben, werden diese in jeder Gruppierung nach der gewünschten Auswahl sortiert.

**Frage**

Wie kann ich eine Spalte erstellen, die Teammitglieder identifiziert, die einer Genehmigungsphase zugewiesen sind?

**Antwort**

Wenn Sie einen Bericht &quot;Aufgabe&quot;oder &quot;Problem/Anfrage&quot;ausführen, ist im Report Builder eine Spalte namens &quot;Genehmiger und Status&quot;verfügbar, die diese Informationen abruft.
