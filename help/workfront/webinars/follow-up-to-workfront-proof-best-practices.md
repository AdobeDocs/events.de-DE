---
title: Experten fragen - Best Practices für Workfront Proof im Nachgang
description: Erfahren Sie, warum Sie automatisierte Workflow-Vorlagen verwenden sollten, wie Sie diese erstellen und wie Sie die Testversandeinstellungen anpassen, um den Datenschutz zu gewährleisten. Dieses Webinar wurde am 4. März 2020 aufgenommen.
doc-type: feature video
team: Technical Marketing
kt: 9917
exl-id: 2b2f6522-2fd9-4d5e-9bc3-903c1d5e4e3b
duration: 4083
source-git-commit: 9a297cda953d4414131657f9ac84580aea0eabeb
workflow-type: tm+mt
source-wordcount: '1649'
ht-degree: 0%

---

# Experten fragen - Best Practices für Workfront Proof im Nachgang

Erfahren Sie, warum Sie automatisierte Workflow-Vorlagen verwenden sollten, wie Sie diese erstellen und wie Sie die Testversandeinstellungen anpassen, um den Datenschutz zu gewährleisten. Dieses Webinar wurde am 4. März 2020 aufgenommen.

>[!VIDEO](https://video.tv.adobe.com/v/341123/?quality=12)

## Fragen und Antworten

**Frage**

Es scheint, dass unsere Instanz beim Hochladen von Dokumenten automatisch Testsendungen generiert. Gibt es eine Möglichkeit, diese Funktion zu aktivieren/deaktivieren?

**Antwort**

Ja, diese Einstellung kann in Ihrem persönlichen Profil deaktiviert werden. Wenn Sie unter Einstellungen > Voreinstellungen auf klicken, wird das Kontrollkästchen &quot;Beim Hochladen von Dokumenten automatisch Testsendungen generieren&quot;aktiviert, das aktiviert oder deaktiviert werden kann.

**Frage**

Können Sie einen Workflow mit leeren Bühnen erstellen, damit Sie einzelne Elemente ausfüllen können, nachdem Sie ihn angehängt haben, damit mehrere Teams einen Fluss verwenden können?

**Antwort**

Ja, automatisierte Workflow-Vorlagen können leere Phasen aufweisen, sodass je nach verwendetem Team verschiedene Benutzer hinzugefügt werden können.

**Frage**

In unserem Anwendungsfall lädt der Designer das Dokument hoch, doch der Kundenbetreuer generiert den Testversand und richtet den Validierungsfluss ein. Wenn eine neue Version benötigt wird, fügt der Designer die Version nur als Dokument hinzu und der Prozess beginnt von vorn. Gibt es eine Möglichkeit, den Testversand weiterhin vom Kundenbetreuer verwalten zu lassen und den Designer die Versionierung zu verwalten, ohne den Ablauf jedes Mal erstellen zu müssen, wenn Sie den neuen Testversand generieren?

**Antwort**

Wenn Sie die Designer mit einer Zugriffsebene für Workfront einrichten, erhalten die Benutzer eine Testlizenz. Wenn ihre Testversandlizenz auf &quot;Supervisor&quot;oder &quot;Administrator&quot;festgelegt ist, können sie neue Versionen von Testsendungen erstellen, ohne den Kundenbetreuer dazu zu bewegen, die neue Version zu konvertieren und einen Workflow anzuwenden. Die neue Version übernimmt lediglich den Workflow aus der vorherigen Version (und kann jetzt auch geändert oder geändert werden).

**Frage**

Was wird für &quot;E-Mail-Warnungen&quot;empfohlen? Entscheidungen oder alle Ausschreibungen?

**Antwort**

Ich empfehle dem Testversand-Ersteller/-eigentümer für die E-Mail-Warnung &quot;Entscheidungen&quot;. Ich empfehle allen anderen Testversand-Empfängern für ihren E-Mail-Warnhinweis den Wert &quot;Deaktiviert&quot;(obwohl der E-Mail-Warnhinweis auf &quot;Deaktiviert&quot;gesetzt ist, erhalten sie trotzdem Benachrichtigungen zu Neuem Testversand, Neuer Version, verspätetem Testversand und @Erwähnung-E-Mail). Durch diese Konfiguration wird sichergestellt, dass die E-Mail-Warnungen auf ein Minimum begrenzt werden und E-Mails erhalten bleiben.

**Frage**

Können Sie den Eigentümer des Testversands ändern, der bei der Entscheidungsfindung benachrichtigt wird? Wir versuchten, das Testodierungs-Tool zu verwenden, konnten jedoch den Dokumenteigentümer nicht von der Person ändern, die das Originaldokument hochgeladen hat. Beispiel: Ein Marketing-Manager hat das Originaldokument hochgeladen, aber es war ein Marketing-Spezialist, der letztendlich für die Entscheidungsfindung und die Durchführung von Änderungen verantwortlich war.

**Antwort**

Um den Testversand-Besitzer zu ändern, gehen Sie wie folgt vor: Dokumente > Testversand auswählen > Klicken Sie auf &quot;Testversand-Details&quot; > Suchen Sie im Fenster der Testversanddetails den Empfänger, den Sie zum Testversand-Inhaber machen möchten. Klicken Sie auf die Schaltfläche Testversand und wählen Sie &quot;Inhaber&quot;.

**Frage**

Gibt es eine Verfolgung der Anzahl der Runden von Überprüfungen?

**Antwort**

In der Regel entsprechen die Revisionsrunden der Anzahl der Testversandversionen.

**Frage**

Kann eine Person in mehr als einer Bühne sein? Mit anderen Worten, wenn wir einen Manager in einem frühen Prüfungszyklus haben, der eine abschließende Überprüfung in einem späteren Stadium durchführt, wie würden wir das einrichten?

**Antwort**

Sie können einen Testversand-Empfänger zwar nicht zu mehr als einer Testphase eines Testversands hinzufügen, aber sobald die Phase der Überprüfung, in der er sich befindet, aktiviert ist, befinden sie sich in den restlichen Phasen des Testversands dieser Version. Dies würde es ihnen ermöglichen, Kommentare weiter zu kommentieren und zu beantworten, auch wenn andere Phasen begonnen haben. Um sicherzustellen, dass dies funktioniert, müssen Sie sicherstellen, dass keine Bühnen gesperrt werden, wenn die neue Phase beginnt.

**Frage**

Können Sie bestehende Workflows bearbeiten?

**Antwort**

Ja, Sie möchten zu Workfront Proof navigieren und dann im Menü auf der linken Seite die Option Workflows auswählen. Dort können Sie Bühnen bearbeiten, Benutzer hinzufügen, Benutzer entfernen, Bühnen hinzufügen usw.

**Frage**

Hat der Genehmigungs-Workflow eines Dokuments für den Testversand einen besonderen Vorteil gegenüber der Aufgabe? Wir haben es so eingerichtet, dass es in der Aufgabe zur Dokument-/Kunstentwicklung enthalten ist. Wenn das Kunstwerk in einem beliebigen Stadium des Genehmigungsprozesses abgelehnt wird, wird die Aufgabe erneut ausgeführt, damit der zugewiesene Designer sie überarbeitet. So müssen wir nicht an zwei Orten arbeiten. Aber vielleicht vermisse ich etwas Wichtiges, wenn ich diesen Weg gehe.

**Antwort**

Im Falle eines Testversands verwalten Sie den Validierungsprozess mithilfe der Testversand-Workflow-Engine. Auf diese Weise können Sie mithilfe des kollaborativen Testversand-Überprüfungstools Feedback, Kommentare, Markups, Entscheidungen und Bühnen sammeln. Sie können mehrere Workflow-Trigger verwenden, um den Testversand zu leiten, und Einstellungen verwenden, die für Testsendungen spezifisch sind, z. B. Sperren, Privatstadien und Primäre Entscheidungsträger. Sie können auch eindeutige Testversandrollen und eindeutige E-Mail-Benachrichtigungen zuweisen. Darüber hinaus haben Sie die Möglichkeit, so unterschiedliche Inhalte wie statische, Video- und interaktive Testsendungen (rund 150 verschiedene Dateitypen) zu überprüfen.

**Frage**

Wer kann die Bühne auf eine private Bühne stellen? Nur Administratoren?

**Antwort**

Die Erstellung der Vorlage obliegt dem Administrator. Jeder Benutzer, der einen Testversand erstellen kann, kann die Bühne jedoch privat gestalten.

**Frage**

Ist der Termin in der E-Mail-Benachrichtigung enthalten?

**Antwort**

Ja, wenn Sie einen Testversand terminieren, wird dies in der E-Mail-Benachrichtigung angezeigt.

**Frage**

Können Sie eine Vorlage für eine Proof-Gruppe freigeben?

**Antwort**

Sie können jedoch feststellen, dass sie nur für Mitglieder der Gruppe freigegeben wird, die über Testlizenzen verfügen. Sie können Vorlagen nicht für Workfront-Benutzer oder -Gäste freigeben, die keine Testversandlizenzen besitzen.

**Frage**

Wie wird ein Testversand an den Testversandinhaber umgeleitet, wenn er abgelehnt wird?

**Antwort**

Der Testversand-Besitzer bleibt in allen Testsendungen auf dem Testversand. Wird der Testversand abgelehnt, muss der Testversand nicht an den Eigentümer zurückgesendet werden. Stattdessen wird der Testversand-Besitzer per E-Mail über die getroffene Entscheidung informiert, die Kommentare überprüfen und mit einer neuen Version beginnen.

**Frage**

Wie kann ich das &#39;Download&#39;-Dokument in Testversand deaktivieren/ausblenden?

**Antwort**

Wenn Sie einen neuen Testversand hinzufügen, sollten Sie nach unten scrollen, bis Sie zu Testversandeinstellungen gelangen. Dort sehen Sie ein Kontrollkästchen für &quot;Original-Datei herunterladen&quot;, das Sie auswählen oder deaktivieren können.

**Frage**

Wie wirkt sich diese Datenschutzeinstellung in den Kontoeinstellungen auf die Testversand-Benutzer aus, die den automatisierten Vergleich (Seite für Seite mit automatischem Vergleich) verwenden? Verhindert die Einstellung der Standardeinstellung auf DISabled den Vergleich zweier Versionen durch Prüfer?

**Antwort**

Für die Freigabeeinstellung &quot;Empfänger können alle Versionen anzeigen&quot;ist es nicht möglich, Version 1 und Version 2 zu vergleichen, wenn der Empfänger auf &quot;Deaktiviert&quot;gesetzt ist und nicht Version 1, sondern Version 2 verwendet hat. Beachten Sie, dass Workfront-Benutzer mit der Berechtigungsstufe &quot;Testversand für Supervisor&quot;oder &quot;Administrator&quot;alle Versionen unabhängig von der Einstellung sehen können.

**Frage**

Können wir mehrere Personen eine neue Version hochladen? zum Beispiel lädt ein Kopierer Version 1 hoch und dann haben wir das Angebot in Schritt 1. Sie sehen eine Änderung, die vorgenommen werden muss, oder die Upload-Version 2?

**Antwort**

Testversand-Empfänger können neue Testsendungen erstellen lassen, wenn sie die folgenden Kriterien erfüllen: 1) Sie sind Inhaber des Testversands - oder 2) Sie werden mit der Testversandrolle Autor oder Moderator auf dem Testversand eingerichtet - oder 3) Sie werden mit dem Berechtigungsnachweis oder Administrator eingerichtet.

**Frage**

Wie werden mehrere Testsendungen durchgeführt (z. B. A, B und C) mit dem automatisierten Workflow. Fangen Sie wieder an?

**Antwort**

Sie können eine automatisierte Workflow-Vorlage zum Zeitpunkt der Erstellung der Testsendungen auf mehrere Testsendungen anwenden. Gehen Sie dazu wie folgt vor: Dokumente > Neu hinzufügen > Testversand. Wählen Sie auf der Seite &quot;Neuer Testversand&quot;mehrere hochzuladende Dateien aus, wenden Sie die automatisierte Workflow-Vorlage an und erstellen Sie die Testsendungen.

**Frage**

Kann ein Testversand mit Kommentaren in eine PDF exportiert werden?

**Antwort**

Sie können eine Druckzusammenfassung auf einem Testversand in eine PDF-Datei exportieren. Diese enthält alle Kommentare, Markups, Antworten und Entscheidungen.

**Frage**

Wo kann ich die Testversandeinstellungen sehen?

**Antwort**

Um die Testversandeinstellungen für einen vorhandenen Testversand anzuzeigen, gehen Sie wie folgt vor: Registerkarte Dokumente > Testversand > Klicken Sie auf &quot;Testversanddetails&quot; > Über das sich öffnende Fenster mit den Testversanddetails können Sie den Bereich &quot;Einstellungen&quot;erweitern.

**Frage**

Können Sie jemanden auf der privaten Bühne taggen?

**Antwort**

Wenn Sie Testversand-Empfänger in der privaten Bühne sind, können Sie jede Person in dieser privaten Bühne mit Tags versehen. Wenn Sie sich nicht in der privaten Bühne befinden, können Sie niemanden aus der privaten Bühne mit Tags versehen.

**Frage**

Können Sie eine Phase nach der Aktivierung deaktivieren?

**Antwort**

Sie können eine aktive Bühne nicht deaktivieren. Sie können die Bühne jedoch &quot;sperren&quot;, wodurch Personen auf der Bühne daran gehindert werden, Kommentare und Entscheidungen zu treffen.

**Frage**

Was passiert hinter den Kulissen, wenn mindestens ein Prüfer in einer Phase Änderungen für erforderlich hält? Wer wird benachrichtigt, eine neue Version hochzuladen?

**Antwort**

Dies hängt von der Einstellung &quot;E-Mail-Warnung&quot; des Testversands und/oder des Testversands ab. Es wird empfohlen, Testversand-Ersteller/-besitzer mit der E-Mail-Warnung &quot;Entscheidungen&quot;zu versehen, damit sie per E-Mail benachrichtigt werden, wenn über den Testversand entschieden wird.
