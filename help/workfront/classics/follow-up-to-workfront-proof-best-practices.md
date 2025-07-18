---
title: Fragen an Experten - Follow-up zu Best Practices für Workfront Proof
description: Erfahren Sie, warum Sie automatisierte Workflow-Vorlagen verwenden sollten, wie Sie sie erstellen und wie Sie die Testversandeinstellungen anpassen können, um den Datenschutz sicherzustellen. Dieses Webinar wurde am 4. März 2020 aufgezeichnet.
doc-type: feature video
team: Technical Marketing
kt: 9917
exl-id: 2b2f6522-2fd9-4d5e-9bc3-903c1d5e4e3b
duration: 4083
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '1649'
ht-degree: 0%

---

# Fragen an Experten - Follow-up zu Best Practices für Workfront Proof

Erfahren Sie, warum Sie automatisierte Workflow-Vorlagen verwenden sollten, wie Sie sie erstellen und wie Sie die Testversandeinstellungen anpassen können, um den Datenschutz sicherzustellen. Dieses Webinar wurde am 4. März 2020 aufgezeichnet.

>[!VIDEO](https://video.tv.adobe.com/v/341123/?quality=12)

## Fragen und Antworten

**Frage**

Es scheint, dass unsere Instanz beim Hochladen von Dokumenten automatisch Korrekturabzüge generiert. Gibt es eine Möglichkeit, diese Funktion zu aktivieren/deaktivieren?

**Antwort**

Ja, diese Einstellung kann in Ihrem persönlichen Profil deaktiviert werden. Wenn Sie auf Meine Einstellungen > Voreinstellungen klicken, gibt es ein Kontrollkästchen für „Beim Hochladen von Dokumenten automatisch Korrekturabzüge generieren“, das aktiviert oder deaktiviert werden kann.

**Frage**

Können Sie Workflows erstellen, die leere Phasen enthalten, damit Sie nach dem Anhängen Einzelpersonen ausfüllen können, damit mehrere Teams einen Fluss verwenden können?

**Antwort**

Ja, automatisierte Workflow-Vorlagen können leere Phasen enthalten, sodass je nach Team, das sie verwendet, verschiedene Benutzer hinzugefügt werden können.

**Frage**

In unserem Anwendungsfall lädt der Designer das Dokument hoch, aber der Account Manager generiert den Korrekturabzug und richtet den Genehmigungsfluss ein. Wenn eine neue Version benötigt wird, fügt Designer die Version nur als Dokument hinzu und der Prozess beginnt von vorne. Gibt es eine Möglichkeit, den Korrekturabzugsfluss weiterhin vom Account Manager und die Versionierung vom Designer verwalten zu lassen, ohne den Fluss bei jeder Erstellung des neuen Korrekturabzugs erstellen zu müssen?

**Antwort**

Wenn Sie die Designer mit einer Zugriffsebene „Arbeit“ oder „Plan“ in Workfront einrichten, erhalten diese eine Proofing-Lizenz. Wenn ihre Proofing-Lizenz auf „Supervisor“ oder „Administrator“ festgelegt ist, können neue Versionen von Korrekturabzügen erstellt werden, ohne dass der Account Manager die neue Version konvertieren und einen Workflow anwenden muss. Die neue Version übernimmt nur den Workflow aus der vorherigen Version (und kann zu diesem Zeitpunkt auch geändert oder geändert werden).

**Frage**

Was wird für „E-Mail-Warnhinweise“ empfohlen? Entscheidungen oder alle Warnhinweise?

**Antwort**

Ich empfehle, dass die Erstellerin bzw. der Besitzer des Korrekturabzugs für ihren E-Mail-Warnhinweis auf „Entscheidungen“ eingestellt ist. Ich empfehle allen anderen Testversand-Empfängern für ihren E-Mail-Warnhinweis die Einstellung „Deaktiviert“ (obwohl der E-Mail-Warnhinweis auf „Deaktiviert“ eingestellt ist, erhalten sie dennoch Benachrichtigungen zu neuen Korrekturabzügen, neuer Version, verspätetem Korrekturabzug und @Mention E-Mail). Dadurch wird sichergestellt, dass die E-Mail-Warnhinweise zielgerichtet eingerichtet werden und die E-Mail-Adresse auf ein Minimum beschränkt bleibt.

**Frage**

Sind Sie in der Lage, den Verantwortlichen für den Korrekturabzug zu ändern, der benachrichtigt wird, wenn die Entscheidungen getroffen werden? Wir haben versucht, das Proofing-Tool zu verwenden, konnten jedoch nicht den Dokumentbesitzer in der Person ändern, die das Originaldokument hochgeladen hat. Beispiel: Ein Marketing-Manager hat das Originaldokument hochgeladen, aber es war ein Marketing-Spezialist, der letztendlich für das Abrufen von Entscheidungen und das Vornehmen von Änderungen verantwortlich war.

**Antwort**

Um den/die Verantwortliche(n) des Korrekturabzugs zu ändern, müssen Sie diesem Pfad folgen: Dokumente > Wählen Sie den Korrekturabzug aus > Klicken Sie im Fenster mit den Korrekturabzugsdetails auf „Korrekturabzugsdetails“ > Suchen Sie den Empfänger, der/die Sie zum Verantwortlichen für den Korrekturabzug machen möchten > Klicken Sie auf die Schaltfläche mit den Auslassungspunkten für diesen Empfänger und wählen Sie „Verantwortlichen erstellen“ aus.

**Frage**

Gibt es eine Nachverfolgung der Anzahl der Rezensionsrunden, die stattgefunden haben?

**Antwort**

In der Regel entsprechen Revisionsrunden der Anzahl der Korrekturabzugsversionen.

**Frage**

Kann sich eine Person in mehr als einem Stadium befinden? Mit anderen Worten, wenn wir einen Manager in einem frühen Überprüfungszyklus haben, der die abschließende Überprüfung in einer späteren Phase hat, wie würden wir das einrichten?

**Antwort**

Sie können einen Testversand-Empfänger zwar nicht zu mehr als einem Überprüfungsschritt zu einem Testversand hinzufügen, aber sobald der Überprüfungsschritt, in dem er sich befindet, aktiviert wurde, befindet er sich auf dem Testversand für die verbleibende Version. Auf diese Weise könnten sie weiterhin Kommentare abgeben und auf Kommentare antworten, auch wenn andere Phasen bereits begonnen haben. Um sicherzustellen, dass dies funktioniert, müssen Sie sicherstellen, dass Sie beim Starten des neuen Schritts keine Stadien haben.

**Frage**

Können vorhandene Workflows bearbeitet werden?

**Antwort**

Ja, Sie können zu Workfront Proof navigieren und dann im Menü links Workflows auswählen. Dort können Sie Stadien bearbeiten, Benutzer hinzufügen, Benutzer entfernen, Stadien hinzufügen usw.

**Frage**

Hat der Genehmigungs-Workflow für ein Dokument im Korrekturabzug einen bestimmten Vorteil gegenüber der Aufgabe? Wir haben sie für die Aufgabe zur Dokument-/Kunstentwicklung eingerichtet. Wenn das Kunstwerk also in einem beliebigen Schritt des Genehmigungsprozesses abgelehnt wird, wird die Aufgabe wieder aktiviert, damit der zugewiesene Designer es überarbeiten kann. So müssen wir nicht an zwei Orten arbeiten. Aber vielleicht vermisse ich etwas Wichtiges über diesen Weg.

**Antwort**

Im Falle des Proofings verwalten Sie den Genehmigungsprozess mithilfe der Workflow-Engine für Korrekturabzüge. Auf diese Weise können Sie das Tool für die partizipative Überprüfung von Korrekturabzügen verwenden, um Feedback, Kommentare, Markierungen, Entscheidungen und Phasen zu sammeln. Sie haben die Möglichkeit, mehrere Workflow-Trigger zu verwenden, um den Korrekturabzug weiterzuleiten, und können Einstellungen verwenden, die nur für Korrekturabzugsschritte gelten, z. B. Sperren, private Phasen und Primäre Entscheidungsträger. Sie haben außerdem die Möglichkeit, eindeutige Korrekturabzug-Rollen und eindeutige E-Mail-Benachrichtigungen zu Korrekturabzügen zuzuweisen. Darüber hinaus haben Sie die Möglichkeit, so unterschiedliche Inhalte wie statische, Video- und interaktive Korrekturabzüge (etwa 150 verschiedene Dateitypen) zu überprüfen.

**Frage**

Wer kann die Bühne auf eine private Bühne stellen? Nur Administratoren?

**Antwort**

Die Erstellung der Vorlage liegt in der Verantwortung des Administrators, aber jeder Benutzer, der einen Korrekturabzug erstellen kann, kann die Phase privat machen.

**Frage**

Ist die Frist in der E-Mail-Benachrichtigung enthalten?

**Antwort**

Ja, wenn Sie eine Frist auf einen Korrekturabzug anwenden, wird dieser in der E-Mail-Benachrichtigung angezeigt.

**Frage**

Können Sie eine Vorlage für eine Korrekturabzugsgruppe freigeben?

**Antwort**

Sie können jedoch auch feststellen, dass sie nur für Mitglieder der Gruppe freigegeben werden, die Korrekturabzugslizenzen besitzen. Sie können Vorlagen nicht für Workfront-Benutzende oder Gäste freigeben, die keine Korrekturabzugslizenzen besitzen.

**Frage**

Wie wird ein Korrekturabzug an den Besitzer des Korrekturabzugs weitergeleitet, wenn er abgelehnt wird?

**Antwort**

Der/die Testversand-Verantwortliche bleibt während aller Testversandphasen im Testversand. Wenn der Korrekturabzug abgelehnt wird, muss der Korrekturabzug selbst nicht an den Besitzer zurückgeleitet werden. Stattdessen wird der Verantwortliche des Korrekturabzugs per E-Mail über die getroffene Entscheidung benachrichtigt, die Kommentare überprüft und mit einer neuen Version begonnen.

**Frage**

Wie kann ich das Dokument „Download“ im Korrekturabzug deaktivieren/ausblenden?

**Antwort**

Wenn Sie einen neuen Korrekturabzug hinzufügen, scrollen Sie nach unten, bis Sie zu den Korrekturabzugseinstellungen gelangen. Dort wird ein Kontrollkästchen für „Original-Datei herunterladen“ angezeigt, das Sie aktivieren oder deaktivieren können?

**Frage**

Wie wirkt sich diese Datenschutzeinstellung in den Kontoeinstellungen auf Proofing-Benutzende aus, die speziell den automatisierten Vergleich verwenden (Seite an Seite mit automatischem Vergleich) - Verhindert die Standardeinstellung auf DEAKTIVIERT, dass der Prüfer zwei Versionen vergleicht?

**Antwort**

Für die Freigabeeinstellung „Empfänger können alle Versionen anzeigen“ - wenn sie auf „Deaktiviert“ gesetzt ist und der Empfänger nicht in Version 1, sondern in Version 2 war, kann er die Versionen 1 und 2 nicht vergleichen. Beachten Sie, dass Workfront-Benutzende mit der Berechtigungsstufe „Supervisor“ oder „Administrator“ alle Versionen unabhängig von der Einstellung sehen können.

**Frage**

Können mehrere Personen eine neue Version hochladen? Beispielsweise lädt ein Werbetexter Version 1 hoch und dann haben wir den Korrekturabzug in Schritt 1 . Sie sehen eine Änderung, die vorgenommen werden muss, kann die Upload-Version 2?

**Antwort**

Empfängerinnen und Empfänger von Korrekturabzügen können neue Versionen von Korrekturabzügen erstellen, wenn sie die folgenden Kriterien erfüllen: 1) Sie sind Inhaber des Korrekturabzugs - oder 2) sie sind für den Korrekturabzug mit der Rolle „Autor“ oder „Moderator“ eingerichtet - oder 3) sie sind mit der Berechtigungsstufe für Korrekturabzüge von Supervisor oder Administrator eingerichtet.

**Frage**

Wie werden mehrere Korrekturabzüge (z. B. A, B und C) mit dem automatisierten Workflow. Fängst du wieder an?

**Antwort**

Sie können eine automatisierte Workflow-Vorlage auf mehrere Korrekturabzüge zum Zeitpunkt der Erstellung der ersten Version der Korrekturabzüge anwenden. Gehen Sie dazu folgendermaßen vor: Dokumente > Neu hinzufügen > Korrekturabzug. Wählen Sie auf der Seite Neuer Korrekturabzug mehrere Dateien aus, die hochgeladen werden sollen, wenden Sie die automatisierte Workflow-Vorlage an und erstellen Sie die Korrekturabzüge.

**Frage**

Kann ein Korrekturabzug mit Kommentaren in eine PDF exportiert werden?

**Antwort**

Sie können eine Druckzusammenfassung eines Korrekturabzugs in eine PDF-Datei exportieren. Dies enthält alle Kommentare, Markierungen, Antworten und Entscheidungen.

**Frage**

Wo kann ich die Korrekturabzugseinstellungen sehen?

**Antwort**

Um die Korrekturabzugseinstellungen für einen vorhandenen Korrekturabzug anzuzeigen, folgen Sie diesem Pfad: Registerkarte „Dokumente“ > Wählen Sie den Korrekturabzug aus > Klicken Sie auf „Korrekturabzugsdetails“ > Erweitern Sie im sich öffnenden Fenster „Korrekturabzugsdetails“ den Bereich „Einstellungen“.

**Frage**

Kann man jemanden auf der privaten Bühne markieren?

**Antwort**

Wenn Sie ein Testversand-Empfänger in der privaten Phase sind, können Sie jeden in dieser privaten Phase taggen. Wenn Sie sich nicht in der privaten Phase befinden, können Sie niemanden in der privaten Phase taggen.

**Frage**

Können Sie eine Phase nach der Aktivierung deaktivieren?

**Antwort**

Sie können eine aktive Phase nicht deaktivieren. Sie können die Phase jedoch „sperren“, was Personen innerhalb der Phase daran hindert, Kommentare und Entscheidungen zu treffen.

**Frage**

Was passiert hinter den Kulissen, wenn 1 oder mehr Prüfer in einer Phase sagen, dass Änderungen erforderlich sind? Wer wird zum Hochladen einer neuen Version benachrichtigt?

**Antwort**

Dies hängt von der Einstellung „E-Mail-Warnhinweis“ des Korrekturabzugs-Erstellers und/oder der Testversand-Empfänger ab. Ich empfehle, dass Ersteller/Inhaber von Korrekturabzügen mit dem E-Mail-Warnhinweis „Entscheidungen“ eingestellt werden, sodass sie jedes Mal per E-Mail benachrichtigt werden, wenn eine Entscheidung über den Korrekturabzug getroffen wird.
