---
title: Experten fragen - Best Practices zur Maximierung von Workfront Proof
description: Erfahren Sie, wie Sie Einstellungen konfigurieren, hervorragende Berichte aktivieren und allgemeine Fallstricke in Testversand vermeiden. Dieses Webinar wurde am 26. Februar 2020 aufgenommen.
doc-type: feature video
team: Technical Marketing
kt: 9916
exl-id: 7d3e437d-4a6e-44b8-9eff-eabb8284c391
duration: 5182
source-git-commit: 9a297cda953d4414131657f9ac84580aea0eabeb
workflow-type: tm+mt
source-wordcount: '5572'
ht-degree: 0%

---

# Experten fragen - Best Practices zur Maximierung von Workfront Proof

Erfahren Sie, wie Sie Einstellungen für Erfolg konfigurieren und auf Ansichten (und andere Tricks) zugreifen können, um eine hervorragende Berichterstellung zu ermöglichen, und wie Sie allgemeine Fallstricke in Testversand vermeiden können. Dieses Webinar wurde am 26. Februar 2020 aufgenommen.

>[!VIDEO](https://video.tv.adobe.com/v/341122/?quality=12)

## Fragen und Antworten

**Frage**

Um einem Empfänger die Möglichkeit zu geben, einen für ihn freigegebenen Testversand freizugeben, müssen Sie unter den Testversandeinstellungen die Option &quot;Anmeldung&quot; manuell aktivieren. Gibt es Pläne, dieses Kontrollkästchen standardmäßig automatisch zu aktivieren?

**Antwort**

Dieser kann von einem Administrator als Standard für einzelne Benutzer aktiviert/deaktiviert werden, indem Sie diesem Pfad folgen: PHQ-Anmeldung > Kontoeinstellungen > Benutzer > Klicken Sie auf den Link &quot;Benutzername&quot;> &quot;Standardmäßige Testeinstellungen&quot;.

**Frage**

Wenn Sie &quot;Neuer Testversand&quot;nicht auswählen und ein Dokument hochladen und der Benutzer auf &quot;automatisch Testversand erzeugen&quot;eingestellt ist. Können Sie diese Einstellungen ändern, nachdem die Dateien bereits hochgeladen wurden?

**Antwort**

Ja. Sie können alle Testversandeinstellungen anpassen, indem Sie den Testversand im Tab Dokumente auswählen und dann auf Details des Testversands klicken.

**Frage**

Gilt diese Präsentation für das eigenständige Werkzeug?

**Antwort**

Recommendations für Testrollen, E-Mail-Warnungen, Entscheidungsoptionen, Weiterleiten von E-Mails und Workflow-Vorlagengruppierung/Freigabe/Einstellungen sind für den eigenständigen Testversand relevant.

**Frage**

Wofür würden Sie eine Testversand-Vorlage verwenden?

**Antwort**

Wenn der Inhaltsüberprüfungsprozess Ihres Unternehmens häufig wiederholt oder Inhalt häufig von denselben Personen geprüft wird, können Sie Workflow-Vorlagen erstellen, die jene Validierer mit von Ihnen festgelegten Testversandrollen und Benachrichtigungseinstellungen enthalten.

**Frage**

Was ist eine Testversand-Workflow-Vorlage?

**Antwort**

Eine Testversand-Workflow-Vorlage ist eine Vorlage mit einem vorab festgelegten Testversand-Routing-Workflow, der auf Testsendungen angewendet werden kann. Sie ermöglichen die Standardisierung und Automatisierung von Testversandvalidierungsprozessen.

**Frage**

Wie können Sie eine Testversandvorlage erstellen?

**Antwort**

Als Administrator möchten Sie folgenden Pfad verwenden: PHQ-Anmeldung > Workflows > Neu > Neue Vorlage.

**Frage**

Ermöglicht die Funktion zur Vorlagenfreigabe die Freigabe für Gruppen und Teams oder nur für einzelne Benutzer?

**Antwort**

Derzeit können Sie keine Workflow-Vorlagen für Workfront-Gruppen, -Teams, -Rollen oder -Unternehmen freigeben. Sie können sie jedoch für Einzelanwender freigeben und für Testgruppen freigeben. Gehen Sie wie folgt vor, um eine Testgruppe zu erstellen: PHQ-Anmeldung > Gruppen > Neue Gruppe.

**Frage**

Gibt es beim Einreichen eines Testversands - unter &quot;Organisation&quot; - eine Möglichkeit, die Ordner zu bereinigen, die jeder Benutzer sieht, damit er nur die Ordner sieht, die für ihn relevant sind? Anstelle aller Ordner, die innerhalb des Unternehmenskontos erstellt wurden?

**Antwort**

Diese Frage bezieht sich auf Workfront Proof Standalone. In eigenständigen Workfront Proof können Sie private Ordner verwenden, um Ordner für bestimmte Benutzer auszublenden. Dies ermöglicht eine optimierte Liste von Ordnern, aus denen Sie wählen können. Beachten Sie, dass Sie auch die Typ-Ahead-Logik verwenden können, um den Ordner zu finden, dem Sie auch einen Testversand hinzufügen möchten.

**Frage**

Haben Überprüfer und Genehmiger die Möglichkeit, diese Benachrichtigungseinstellungen zu ändern?

**Antwort**

Administratoren in Workfront können die standardmäßigen E-Mail-Warnhinweiseinstellungen für Benutzer und Kontakte ändern. Testversand-Ersteller können dann die Benachrichtigungseinstellung beim Erstellen eines Testversands sowie bei vorhandenen Testsendungen ändern.

Empfänger von Testsendungen können ihre E-Mail-Warnung für bestimmte Testsendungen im Testversand-Viewer-Tool jederzeit ändern, indem sie im linken Menü das Einstellungssymbol auswählen.

**Frage**

Überschreiben die E-Mail-Warnungen die globalen Benachrichtigungen?

**Antwort**

Testversand-E-Mail-Warnhinweise sind völlig unabhängig von den globalen Benachrichtigungseinstellungen.

**Frage**

Wenn Überprüfer auf &quot;deaktiviert&quot;gesetzt sind, wie werden sie dann wissen, ob es einen neuen Testversand gibt, anhand dessen sie überprüfen können, ob sie einen früheren Testversand abgelehnt haben?

**Antwort**

E-Mail-Warnhinweise sind unabhängig von der neuen E-Mail-Testversand, der neuen Version, der E-Mail mit Risiko, der verspäteten E-Mail und der @Mentions-E-Mail. Wenn Sie als E-Mail-Warnung &quot;Deaktiviert&quot;wählen, deaktivieren Sie nur Benachrichtigungen zu Aktivitäten wie Kommentaren, Antworten und Entscheidungen zum Testversand (mit Ausnahme von @Mention-E-Mails aus Kommentaren).

**Frage**

Wird durch die Deaktivierung von E-Mails auf Unternehmensebene festgelegt? oder per Portfolio?

**Antwort**

Die Einstellung unter Einrichtung > E-Mail > Prüfung und Genehmigung , die den Versand von E-Mails aktiviert/deaktiviert, wenn Testversand-Empfänger Kommentare abgeben, ist Enterprise Wide (es handelt sich um eine globale Einstellung).

**Frage**

Ich habe einen &quot;Gastbenutzer&quot;-Benutzer, der zum Testversand hinzugefügt wurde und den Testversand nicht überprüfen kann. Und der Benutzer hat keinen Zugriff auf Workfront.

**Antwort**

Wenn der Gast auf den Testversand zugreifen kann, aber keine Kommentare/Entscheidungen trifft, überprüfen Sie seine Testrolle im Testversand. In diesem Fall wurden sie möglicherweise dem Testversand mit der Rolle &quot;Schreibgeschützt&quot;hinzugefügt. Wenn sie als Prüfer oder Prüfer und Genehmiger für den Testversand eingerichtet sind und dennoch keine Kommentare/Markierungen/Entscheidungen treffen können, senden Sie bitte ein Support-Ticket.

**Frage**

Benötigen Gastbenutzer eine Lizenz?

**Antwort**

Gastbenutzer benötigen keine Lizenz.

**Frage**

Ich sehe nicht das Entscheidungsfeld für den Testversand?

**Antwort**

Wenn das Feld für die Entscheidung eines Testversands nicht auf einem Testversand angezeigt wird, können Sie für den Testversand mit der Rolle Nur lesen oder Prüfer eingerichtet werden oder die Testphase, in der Sie sich im Testversand befinden, wurde noch nicht gestartet.

**Frage**

Können Sie die Einstellung unter WF > Setup klarstellen - wenn Sie die Möglichkeit haben, E-Mails für jeden Kommentar zu senden - werden diese auch dann gesendet, wenn die E-Mail in PHQ deaktiviert ist? und wer erhält die E-Mails?

**Antwort**

Die Option Workfront-Einrichtung > E-Mail > Benachrichtigung zu Überprüfung und Genehmigung ist unabhängig von den Optionen für E-Mail-Warnhinweise auf der Testversand-Ebene. Wenn diese Option aktiviert ist, erhält jeder, der an jedem Testversand teilnimmt, jedes Mal eine E-Mail, wenn jemand einen Kommentar abgibt.

**Frage**

Zuvor haben Sie für E-Mail-Warnungen außerhalb des Testversandeigentümers &quot;deaktiviert&quot;empfohlen. Werden die Empfänger dennoch per E-Mail benachrichtigt, dass ihnen in diesem Fall ein Testversand zugewiesen wurde?

**Antwort**

Ja. E-Mail-Warnungen (die auf &quot;Alle Aktivitäten&quot;, &quot;Deaktiviert&quot;, &quot;Entscheidungen&quot;usw. gesetzt werden können) sind unabhängig von E-Mails für den Nachweis von Benachrichtigungen (neuer Testversand, neue Version, Risikonachweis, verspäteter Testversand, @Erwähnungen).

**Frage**

Was ist, wenn Sie eine Instanz haben, in der jemand einem Testversand hinzugefügt wird und sie denken, dass sie dort nicht sein sollten? Würde das Entfernen von &quot;Nicht relevant&quot;ihnen keine Option zur Auswahl bieten?

**Antwort**

Dies ist eine gute Verwendung für die Option Nicht relevante Entscheidung . Sollte jedoch jemand nicht auf dem Testversand sein, empfehle ich ihm, @Erwähnung des Testversand-Eigentümers in einem Kommentar zum Testversand zu verwenden und die Entfernung zu beantragen. Wenn jemand, der eine Entscheidung über den Testversand treffen soll, die Entscheidung &quot;Nicht relevant&quot;trifft, wenn er die Entscheidung über &quot;Genehmigt&quot;oder &quot;Erforderlich&quot;trifft, kann dies die Funktionsweise des Workflows für diesen Testversand ändern.

**Frage**

Wo finde ich das Kontrollkästchen &quot;Anmeldung erforderlich&quot;für Gastbenutzer?

**Antwort**

Dies befindet sich beim Erstellen eines Testversands in den Testversandeinstellungen auf der Seite Testversand-Erstellung . Wenn der Testversand bereits erstellt wurde, können Sie auf diese Einstellung zugreifen, indem Sie den Testversand im Tab Dokumente auswählen und auf Details des Testversands > Einstellungen klicken. Beachten Sie, dass Sie die erforderlichen Testsendungen nur für Personen freigeben können, die über eine Testlizenz verfügen.

**Frage**

Kann sich jemand von einem Testversand entfernen, wenn er von einer anderen Person hinzugefügt wurde?

**Antwort**

Wenn die Person über Bearbeitungsrechte für den Testversand verfügt, zu dem sie hinzugefügt wurde, kann sie sich selbst entfernen. Personen mit Bearbeitungsrechten sind Workfront-Benutzer mit einer Proofing-Lizenz auf Administrator- oder Supervisorebene sowie Personen, die mit den Testversandrollen Autor oder Moderator zum Testversand hinzugefügt wurden. Jeder andere muss von einer Person mit Bearbeitungsrechten entfernt werden.

**Frage**

Warum sollte ich die Dokumentgenehmigung oder die Validierung des Testversands verwenden oder umgekehrt?

**Antwort**

Die Dokumentgenehmigung kann für ein Dokument verwendet werden, für das keine Kommentare und Markierungen erforderlich sind, die mit dem zu validierenden Dokument übereinstimmen. Ich möchte Sie beispielsweise nur bitten, sich dieses Dokument anzusehen und es entweder zu genehmigen oder abzulehnen. Der Testversand ermöglicht Kommentare und Markups innerhalb des Dokuments im Proof-Viewer-Tool. Sie müssen sich diesen Testversand ansehen, Kommentare hinzufügen, Markierungen hinzufügen und eine Entscheidung treffen. In Zukunft soll die Vereinheitlichung der beiden Funktionselemente geplant werden, da sie sich sehr ähnlich sind.

**Frage**

Wir sind Marketing-Experte und führen eine interne Testversandvalidierung durch und müssen diese dann extern an den Anfragenden senden. Wir gewähren keinen Zugang zu Anforderern für unsere Projekte. Wir wollen auch nicht, dass sie alle unsere Kommentare im internen Beweis sehen. Jetzt erstellen wir einen neuen sauberen Testversand, laden ihn herunter und senden ihn per E-Mail an ihn. Wir wollen sie mit Proof HQ holen, aber nicht sicher, wie sie das erreichen können, ohne ihnen auch Zugang zu unserem Projekt zu verschaffen. Welche Vorschläge?

**Antwort**

Ich empfehle die Verwendung von automatisierten Workflow-Vorlagen, die Ihnen die Verwendung von &quot;privaten Phasen&quot;ermöglichen. Mit privaten Phasen können Sie die Kommentare, Markierungen und Entscheidungen von Gastreviewern in anderen Phasen ausblenden. Dies würde es ermöglichen, dass Ihre interne Testversandprüfung vollständig von der externen Anfrage verborgen wird.

**Frage**

Wie kann man sich nach der Erstellung eines Testversands am besten selbst als Validierer und Validierer hinzufügen?

**Antwort**

Wenn Sie Workfront-Benutzer mit der Berechtigung &quot;Testversand für Administrator oder Supervisor&quot;sind, können Sie sich zu jedem Testversand hinzufügen, auf den Sie Zugriff haben. Andernfalls möchten Sie vom Testversand-Eigentümer (oder von einer anderen Person mit Bearbeitungsrechten für den Testversand) hinzugefügt werden.

**Frage**

Wir haben versucht, Benutzer in einem Testversand mit Tags zu versehen, erhalten jedoch keine E-Mail-Benachrichtigung. Gibt es in den Kontoeinstellungen etwas, um sicherzustellen, dass eine E-Mail gesendet wird?

**Antwort**

Ich empfehle, die Option E-Mail-Filter/Spam-Ordner zu überprüfen, um zu sehen, ob die Benachrichtigungen dorthin gegangen sind, und dann die erforderlichen Anpassungen innerhalb der E-Mail-Anwendung vorzunehmen, um diese E-Mails auf die Whitelist zu setzen. Sie können sich auch mit unserem Support-Team in dieser Frage in Verbindung setzen.

**Frage**

Sie können nur @ jemand, wenn sie einen Beweis Lizenz haben, richtig? Wie in war diese Person noch nie im Testversand und Sie möchten sie mit Tags versehen (@).

**Antwort**

Wenn Sie ein Gast oder ein Workfront-Benutzer mit einer Proofing-Lizenz für Manager sind, können Sie @Erwähnung eines jeden, der sich im Testversand befindet (unabhängig davon, ob dieser Benutzer über eine Lizenz verfügt oder nicht). Wenn Sie Workfront-Benutzer mit einer Testlizenz für Supervisor oder Administrator sind oder Inhaber eines Testversands sind, können Sie @Mention für jeden Benutzer in Ihrer Kontaktliste in der Testplattform verwenden.

**Frage**

Größtes Problem hier: E-Mail %2B-Adressierung (doppelte E-Mail-Adressen). Warum und wie geschieht das und wie kann es behoben werden?

**Antwort**

Dies kann vorkommen, wenn jemand mithilfe der falschen E-Mail-Adresse manuell jemanden zum Testversand hinzufügt. Wenn Ihnen dies gelingt, kann ein Administrator die falsche E-Mail-Adresse aus dem Testkonto entfernen, indem er den folgenden Pfad verwendet: PHQ-Anmeldung > Kontakte > Wählen Sie die falsche E-Mail-/Gastinstanz > Löschen. Wenn Sie Probleme damit haben, dass Benutzer mit doppelten E-Mail-Adressen hinzugefügt werden, wenden Sie sich an unser Supportteam.

**Frage**

Sobald eine Entscheidung getroffen wurde und Sie den Testversand wieder in die Produktion zurückversetzen müssen. Welche Art von Zugriff benötigen Sie für das Produktionsteam, damit es die Aktion des Kommentars verwenden kann, wenn der Testversand gesperrt ist?

**Antwort**

Wenn ein Testversand gesperrt ist, müssen Sie den Testversand entsperren, damit Benutzer Kommentare bearbeiten oder Antworten auf Kommentare senden können. Personen mit den folgenden Berechtigungen können den Testversand freigeben: Der Testversand-Inhaber, Workfront-Benutzer mit einem Proofing-Lizenzlevel Administrator oder Supervisor.

**Frage**

Was ist die beste Lösung für Teams, um Testsendungen zu erfahren, die sich bereits in einer Personenwarteschlange befinden?

**Antwort**

Sie können in Workfront einen Bericht über Testversandgenehmigungen erstellen. Anschließend können Sie Filter anwenden, die nur Testsendungen für bestimmte Benutzer anzeigen, für die noch eine Entscheidung erforderlich ist.

**Frage**

Gibt es eine Möglichkeit, Testsendungen mit den zugehörigen Genehmigungen in einen Ordner herunterzuladen?

**Antwort**

Sie können einen Bericht mit Druckzusammenfassung für Ihre Testsendungen aufrufen und herunterladen, der alle Kommentare, Antworten, Markups, Aktionen und Entscheidungen aller Versionen umfasst.

**Frage**

Wenn Benutzer Zugriff auf die Berichterstellung haben, erhalten sie dadurch auch Zugriff auf den Abschnitt auf der linken Seite (d.h. Workflows, Kontakte, Kontoeinstellungen usw.)?

**Antwort**

Dies hängt von ihrem Testversandniveau ab. Wenn sie mit der Manager- oder Supervisor-Lizenz eingerichtet sind, können sie auf Kontakte zugreifen, aber nicht auf Kontoeinstellungen und Workflows zugreifen. Wenn sie mit der Administratorlizenz eingerichtet sind, haben sie Zugriff auf Kontoeinstellungen und Workflows.

**Frage**

In meiner Organisation sendet der Projekt-Manager eine Genehmigungsanfrage an die Stakeholder zur Überprüfung/Stellungnahme. Sie haben erwähnt, dass wir keine Namen zu den Validierungsfeldern hinzufügen sollten. Wie können Sie als PM den kreativen Beweis an Interessengruppen weitergeben?

**Antwort**

Das Feld Genehmigung ist für Dokumentgenehmigungen vorgesehen, die Sie problemlos verwenden können, wenn Sie nur eine einfache Dokumentgenehmigung benötigen. Wenn Sie eine Testbestätigung (mit Kommentaren, Markierungen und einer Testbestätigungsentscheidung) wünschen, möchten Sie dem Testversand die Stakeholder mit der Testversandrolle von Reviewer &amp; Genehmiger hinzufügen.

**Frage**

Wie fügen Sie Personen zu neuen Rollen bei einem bereits erstellten Testversand hinzu?

**Antwort**

Um Testversand-Empfänger hinzuzufügen und die Rolle Testversand in einem vorhandenen Testversand auszuwählen, gehen Sie wie folgt vor: Wählen Sie den Testversand im Tab Dokumente aus und klicken Sie auf Details des Testversands. Wenn das Fenster mit den Details des Testversands geöffnet wird, klicken Sie auf die Schaltfläche Elipses oben rechts in der Bühne und wählen Sie &quot;Freigeben&quot;. Danach können Sie die Empfänger hinzufügen und ihre Rolle als Testversand sowie die E-Mail-Warnung auswählen.

**Frage**

Wenn wir Testversand-Managern/-erstellern Zugriff auf Proof HQ gewähren, können wir dann die Admin-Bereiche wie Workflows, Gruppen usw. blockieren?

**Antwort**

Ja, dies wird durch die Berechtigung zum Testversand von Benutzern bestimmt. Benutzer mit der Berechtigung &quot;Testversand&quot;von Manager oder Supervisor haben keinen Zugriff auf Kontoeinstellungen und Workflow-Vorlagen. Benutzer mit der Berechtigung &quot;Testversand&quot;des Administrators haben Zugriff auf Kontoeinstellungen und Workflow-Vorlagen. Alle Benutzer mit Zugriff können auf den Bereich Gruppen zugreifen.

**Frage**

Wie können Benutzer alle Testsendungen sehen, denen sie zugewiesen sind, ohne Testversandmanager zu sein?

**Antwort**

Wenn ein Benutzer alle Testsendungen sehen möchte, über die er noch entscheiden muss, kann er den Bereich Home oder My Updates in Workfront verwenden (je nach Zugriffsstufe). Sie können auch einen Bericht zur Bestätigung des Testversands erstellen und Filter anwenden, um nur Testsendungen anzuzeigen, bei denen der angemeldete Benutzer Reviewer und Genehmiger ist.

**Frage**

Hallo, können Sie die automatisierten Testsendungs-Workflows für Situationen nutzen, in denen es drei Entwurfs- und Feedback-Runden gibt und wie Sie berücksichtigen können, wann das Feedback zu spät bereitgestellt wird und wie dies am besten für jede Runde in Aufgaben in WF eingebunden werden kann (Feedback von Design- und Projektmanagern)?

**Antwort**

Sie können zwar viele verschiedene Ansätze für die Verwendung von Aufgaben zusammen mit Review und Genehmigung verwenden. Ein Ansatz, den ich gern verwende, ist die Aufgabe &quot;Proof Routing&quot;, und ich verwende den Testversand-Workflow, um die Benachrichtigungen an Empfänger zu verwalten (anstatt ihnen eine Aufgabe zuzuweisen). Sie können dann eine Aufgabe für &quot;Proof Routing Round 2&quot;und &quot;Proof Routing Round 3&quot;erstellen, die Ihnen dabei hilft, die Anzahl der Runden zu verfolgen. Sie können den Fortschritt der Testsendungen auch über das Testversand-Dashboard (PHQ-Anmeldung > Dashboard > Zu verwaltende Testsendungen) verfolgen. Diese Ansicht zeigt die Anzahl der von Ihnen verwalteten verspäteten Testsendungen (sowie Risikotests) an.

**Frage**

Wenn ein Testversand gelöscht wird, befindet sich eine Kopie dieses Testversands noch auf Ihren Servern?

**Antwort**

Ja. Wenn Sie einen Testversand löschen, der sich im Bereich Papierkorb des zugehörigen Testversands befindet, kann er bei Bedarf von dort wiederhergestellt werden und bleibt dort, bis der Papierkorb geleert ist.

**Frage**

Gibt es eine Möglichkeit, neue Entscheidungen auszulösen, wenn ein anderer Benutzer Änderungen ablehnt oder genehmigt. ie. Der Projektmanager muss eine neue Entscheidung treffen, auch wenn er sie bereits angeschaut und genehmigt hat. (zu versuchen, nicht zu machen, dass der Proj-Manager nicht auf die Korrektur warten muss, abhängig von ihrer Überprüfung)?

**Antwort**

Dies kann zwar nicht automatisiert werden, Sie können aber den Projektmanager mit der E-Mail-Warnung zu Entscheidungen einrichten. Auf diese Weise wird der Projektmanager über die getroffene Entscheidung informiert und kann dann zum Testversand zurückkehren, die von der Korrekturabteilung abgegebenen Kommentare überprüfen und dann bei Bedarf seine Entscheidung ändern.

**Frage**

Warum sehe ich beim Senden eines Updates im Abschnitt Testversand nur den Status SOC und nicht SOCD, wenn ich &quot;Zur Genehmigung anfordern&quot;aktivieren. Sollten wir dieses Kontrollkästchen vermeiden? Best Practice für das Senden einer Testversand-Aktualisierung.

**Antwort**

Bei Verwendung der Funktion &quot;Nach Genehmigung fragen&quot; arbeiten Sie mit der Funktion für die Dokumentgenehmigung, die von der Prüfung und der SOCD-Fortschrittsleiste unabhängig ist. Wenn Sie die Testversand-Rolle eines Testversand-Empfängers aktualisieren müssen, folgen Sie diesem Pfad: Wählen Sie im Tab Dokumente den Testversand aus und klicken Sie auf Details des Testversands. Wenn das Fenster mit den Testversanddetails geöffnet wird, wird die Empfängerliste angezeigt und die Option Testversand-Rolle (sowie E-Mail-Warnhinweis) kann entsprechend angepasst werden. Auf diese Weise können Sie (z. B.) die Rolle &quot;Testversand&quot;von &quot;Überprüfer&quot;in &quot;Prüfer und Genehmiger&quot;ändern.

**Frage**

Ist es möglich sicherzustellen, dass die validierungsverantwortlichen Benutzer keinen Zugriff auf frühere Versionen (und Kommentare) haben, wenn sie im selben Testversand-Dokument vorhanden sind? Muss ein neues Testversand-Dokument erstellt werden oder gibt es eine Möglichkeit, alle Versionen und Kommentare in einem Dokument zu speichern und den Zugriff auf Versionen zu bestimmen?

**Antwort**

In den Kontoeinstellungen des Testversands können Sie die Freigabe/den Sichtbarkeitszugriff auf Ihre Testsendungen steuern. Um diese Einstellung so zu aktualisieren, dass Testversand-Empfänger nur die von Ihnen angegebenen Testsendungen sehen (anstatt alle Versionen des Testversands anzuzeigen), gehen Sie wie folgt vor: PHQ-Anmeldung > Kontoeinstellungen > Einstellungen > Freigabe > Empfänger können alle Versionen anzeigen = Deaktiviert.

**Frage**

Können Sie den Testversand-Dashboard-Bildschirm als externe Seite zu einem WF-Dashboard hinzufügen? Wird das Dashboard Nicht-Administratoren angezeigt?

**Antwort**

Sie können das Testversand-Dashboard als externe Seite in einem Dashboard hinzufügen. Beachten Sie, dass dies nur für Benutzer mit einer Testlizenz sichtbar ist.

**Frage**

Die Dashboard- und Reporting-Funktionen in ProofHQ stehen nur Administratoren zur Verfügung, die Zugriff auf den Testversand haben, nicht wahr? Sind nicht allgemeine Planer ohne Administratorzugriff?

**Antwort**

Das ist richtig. Sie können jedoch einen Support-Fall mit Workfront einreichen, um alle Benutzer Ihrer Proofing-Lizenz um Zugriff auf das Testsystem zu bitten.

**Frage**

Hallo, eine Frage zur Flexibilität des Testversands: Wenn ein neuer Testversand-Version-Upload erforderlich ist, ohne den ursprünglichen Eigentümer zu sein, ist dies die Best Practice für ihn, einen Kollegen zum Workflow als Autor hinzuzufügen, und er wird &quot;Nicht relevant&quot;entscheiden? (Die Übertragung des Eigentums scheint nur für eine einzige Version zu funktionieren.)

**Antwort**

Dieser Anwendungsfall und dieser Workflow funktionieren wirklich. Eine andere Möglichkeit besteht darin, Benutzer, die möglicherweise neue Versionen in Testsendungen hochladen müssen, die nicht der Besitzer sind, mit dem Berechtigungsniveau Supervisor oder Administrator einzurichten. Diese Berechtigungsebene ermöglicht es ihnen, neue Versionen in Testsendungen hochzuladen, die sie nicht besitzen, ohne sie als Autor oder Moderator zum Testversand hinzufügen zu müssen (beides erfordert eine Entscheidung).

**Frage**

Wenn ich das verstehe, können Sie denselben Benutzer nicht in nachfolgenden Phasen eines automatisierten Workflows hinzufügen, was für uns problematisch ist. Ist dies etwas, das Sie ändern können, damit sich derselbe Benutzer in mehreren Phasen befinden kann?

**Antwort**

Sie können einen Testversand-Empfänger zwar nicht zu mehr als einer Testphase eines Testversands hinzufügen, aber sobald die Phase der Überprüfung, in der er sich befindet, aktiviert ist, befinden sie sich in den restlichen Phasen des Testversands dieser Version. Dies würde es ihnen ermöglichen, Kommentare weiter zu kommentieren und zu beantworten, auch wenn andere Phasen begonnen haben. Um sicherzustellen, dass dies funktioniert, müssen Sie sicherstellen, dass keine Bühnen gesperrt werden, wenn neue Bühnen beginnen.

**Frage**

Können Sie das Routing von Testsendungen zwischen Bühnen erklären? Wie kann man eine schließen und zur nächsten Stufe übergehen?

**Antwort**

Es gibt einige Optionen, die wir in automatisierten Workflow-Vorlagen zur Verfügung haben, mit denen wir von einer Phase zur nächsten wechseln können. Zu den Optionen, die Sie verwenden können, gehören &quot;Bei Erstellung eines Testversands&quot;, &quot;Wenn alle Entscheidungen in einer übergeordneten Phase genehmigt werden&quot;, &quot;Wenn alle Entscheidungen mit Änderungen in einer übergeordneten Phase genehmigt oder genehmigt werden&quot;, &quot;Wenn alle Entscheidungen in einer übergeordneten Phase getroffen werden&quot;sowie einige andere Optionen.

**Frage**

Können Sie einen Testversand aus einem Dokument entfernen, das automatisch erstellt wurde, aber kein Testversand sein soll?

**Antwort**

Wenn Sie die Einstellung &quot;Beim Hochladen von Dokumenten automatisch Testsendungen generieren&quot;aktiviert haben, können Sie keinen Testversand aus einem Dokument entfernen. Stattdessen sollten Sie dies über die Schaltfläche Neu hinzufügen > Dokumente erneut hochladen.

**Frage**

Kann ein Benutzer auf Stufe 3 des Testversands eine weitere Person als Review &amp; Genehmiger hinzufügen?

**Antwort**

Wenn der Benutzer über Bearbeitungsrechte für den Testversand verfügt, kann er dies tun. Benutzer mit Bearbeitungsrechten: Der Testversand-Inhaber, Testempfänger, der zum Testversand mit der Rolle Autor oder Moderator hinzugefügt wurde, Testlizenzanwender mit dem Berechtigungsnachweis Supervisor oder Administrator.

**Frage**

Wenn ein Benutzer als Autor bestimmt wurde, kann er eine neue Version des Testversands hochladen? Das wäre jemand anderes als der Testversand-Urheber.

**Antwort**

Testversandempfänger mit der Rolle &quot;Autor und Moderator&quot;können den Testsendungen, auf denen sie sich mit dieser Testversandrolle befinden, neue Versionen hinzufügen.

**Frage**

Externe Benutzer erhalten eine E-Mail pro Testversand zur Überprüfung. Dies kann für sie eine Herausforderung sein, den Status aller Testsendungen zu verfolgen, die sie im Spiel haben. Gibt es Optionen für Dashboards oder E-Mail-Statuslisten oder künftige Funktionen, mit denen externe Benutzer ihren Status bei mehreren Testsendungen verfolgen können?

**Antwort**

Es wird empfohlen, diese externen Benutzer mit einer kostenlosen Reviewer-Lizenz zu Workfront hinzuzufügen. Dadurch erhalten sie Zugriff auf die Seite Meine Aktualisierungen , die eine Liste aller noch ausstehenden Testsendungen enthält, über die sie eine Entscheidung treffen müssen.

**Frage**

Können Sie mehr über die Benachrichtigungen zu Entscheidungen erfahren? Erhalte ich nur Benachrichtigungen mit Testversandkommentaren von Validierungsverantwortlichen und Validierungsverantwortlichen oder erhalte ich die Kommentare von Validierungsverantwortlichen und wann bekomme ich diese?

**Antwort**

Benachrichtigungs-E-Mail-Warnungen zu Entscheidungen werden nur bei Testsendungen gesendet. Sie werden nicht gesendet, wenn Kommentare abgegeben werden. Wenn Sie jedoch eine Entscheidung -E-Mail erhalten, die anzeigt, dass ein Empfänger im Testversand die Entscheidung über erforderliche Änderungen getroffen hat, wissen Sie, dass dies ein guter Zeitpunkt ist, um die hinzugefügten Kommentare (die im Testversand enthalten sein werden) zu überprüfen.

**Frage**

Melden Sie sich bezüglich des Problems der Weiterleitung von E-Mails tatsächlich als Eigentümer der E-Mail an? Und würde das mit gesperrten Umgebungen passieren? Wird es mit einer SSO-Umgebung passieren?

**Antwort**

Dadurch werden Sie als die Person, die die E-Mail an Sie weitergeleitet hat, beim Testversand angemeldet. Die Verwendung von Anmeldung erforderlich für Testsendungen und SSO verhindert den Zugriff auf den Testversand als die Person, die Sie die E-Mail weitergeleitet hat.

**Frage**

Wo greife ich beim Testen auf das Dashboard und die Berichte zu?

**Antwort**

Wenn Sie rechts neben Ihrer Suchleiste in Workfront über ein Kontrollkästchen verfügen, bedeutet dies, dass Sie über ein integriertes Workfront- und Testkonto verfügen. Wenn Sie auf dieses Kontrollkästchen klicken, gelangen Sie zu Workfront Proof und der Startbildschirm wird zum Dashboard. Berichte können mit der Option Ansichten in Ihrem linken Bedienfeld erstellt werden.

**Frage**

Unter dem Abschnitt &quot;Rolle&quot;befinden sich 2 Häkchen am unteren Rand, die erwähnen, jemanden mit einer @mention usw. hinzuzufügen. In den Testversand-Einstellungen können Sie für jede Person Standardrollen festlegen, es gibt jedoch keine Option, diese Auswahlfelder automatisch zu aktivieren. Daher müssen Sie dies jedes Mal tun, wenn Sie einen Testversand erstellen. Wie können Sie dies zu einer Standardeinstellung für einen Benutzer machen?

**Antwort**

Es gibt derzeit keine Möglichkeit, dies zu einer Standardeinstellung für Testversand-Empfänger zu machen. Sie können diese jedoch als Standardeinstellungen für Empfänger in automatisierten Workflow-Vorlagen speichern.

**Frage**

Wie wechselt man zum Besitzer eines Testversands?

**Antwort**

Um den Besitzer eines Testversands zu wechseln, folgen Sie diesem Pfad: Wählen Sie im Tab Dokumente den Testversand aus und klicken Sie auf &quot;Testversanddetails&quot;. Der Tab Testversanddetails wird geöffnet. Wenn die Person, die Sie für den Testversand verantwortlich machen möchten, noch nicht im Testversand ist, können Sie sie als Empfänger hinzufügen, indem Sie in die Schaltfläche Eignung klicken und die Option Freigeben auswählen. Nachdem die Person zum Testversand hinzugefügt wurde (oder wenn sie bereits im Testversand ist), wählen Sie die entsprechende Elipses-Schaltfläche aus, um &quot;Inhaber&quot; zu wählen. Sie werden jetzt zum Besitzer des Testversands gemacht.

**Frage**

Was die neuen Versionen von Testsendungen angeht... die einzige Möglichkeit, dies zu tun, besteht darin, die Datei per Drag-and-Drop auf die vorhandene Datei zu ziehen. Ist das die richtige Methode?

**Antwort**

Es wird empfohlen, auf diese Weise neue Versionen zu erstellen: Wählen Sie den Testversand auf der Registerkarte Dokumente aus, klicken Sie dann auf die Schaltfläche Mehr und wählen Sie Neue Version > Testversand aus. Dadurch gelangen Sie zur Seite Neue Version , auf der der Workflow übertragen wird. Außerdem können Sie alle notwendigen Anpassungen vornehmen, bevor Sie die neue Version weiterleiten.

**Frage**

Können Sie Kommentare zu Testsendungen deaktivieren, um sie für einen Kunden freizugeben, damit er nicht das gesamte interne Feedback des Teams sieht? Damit Sie keinen neuen Testversand erstellen müssen.

**Antwort**

Ich empfehle die Verwendung von automatisierten Workflow-Vorlagen, die Ihnen die Verwendung von &quot;privaten Phasen&quot;ermöglichen. Mit privaten Phasen können Sie die Kommentare, Markierungen und Entscheidungen von Gastreviewern in anderen Phasen ausblenden. Dies würde es ermöglichen, dass Ihre interne Testversandprüfung vollständig von der externen Anfrage verborgen wird.

**Frage**

Fügt die Workfront Proof-Bühne nur hinzu, wenn automatisierte Workflows verwendet werden und jemand, der dem Workflow nicht hinzugefügt wurde, den Testversand öffnet?

**Antwort**

Die Phase &quot;Workfront Proof&quot;wird zu Testsendungen hinzugefügt, wenn ein Nicht-Empfänger auf den Testversand klickt. Sie wird auch angewendet, wenn ein Benutzer einen einfachen Workflow-Proof in einen automatisierten Workfront Proof konvertiert.

**Frage**

Können wir einen Testversand-Workflow einrichten, bei dem mehr als eine Entscheidung getroffen werden kann?

Wir versuchen, unserem internen Rechtsteam Berichte darüber bereitzustellen, wann externe Rechtsberater Prüfungen zu Testsendungen abgeschlossen hat (wie viele Tage im Durchschnitt dauert es, bis sie ihre Überprüfung abschließen, wer sie abschließt usw.).

Zunächst wurde eine neue Entscheidung zum Testversand-Workflow namens &quot;OC Review Complete&quot;hinzugefügt und es wurde angenommen, dass wir einen Bericht erstellen könnten, um diese zu verfolgen.

Das Problem besteht darin, dass nur eine Entscheidung über den Workflow getroffen werden kann.

**Antwort**

Es kann mehr als eine Entscheidung über einen Nachweis getroffen werden - es wird jedoch nur einen Gesamtstatus für einen Nachweis geben, der aus der Entscheidung des schlimmsten Fallszenarios über den Nachweis hervorgeht - oder aus der Entscheidung eines Primären Entscheidungsträgers.

Aufgrund Ihrer Berichterstellungsanforderungen empfehle ich Ihnen, alle Testversand-Benutzer über die gleichen Entscheidungsoptionen zu informieren (Genehmigt, Genehmigt mit Änderungen, Erforderlich) und dann die Berichte im Dashboard des Testversands (PHQ-Anmeldung > Berichte) zu verwenden und die Filteroption anzuwenden, um nach Empfängern zu filtern (die externen Rechtshilfeempfänger in den Filter aufzunehmen). So können Sie die durchschnittliche Umdrehungszeit für die Testsendungen sehen.

**Frage**

Warum ändern sich ALLE Rollen oder verschwinden, sobald eine neue Version auf einen vorhandenen Testversand gezogen und dort abgelegt wurde?

**Antwort**

Beim Ziehen und Ablegen eines Dokuments als neue Version haben Sie Recht, dass der Workflow aus der neuen Version entfernt wurde. Wenn Sie den Workflow von der vorherigen Version zur nächsten beibehalten möchten, wählen Sie den Testversand im Tab Dokumente aus und klicken Sie dann auf die Schaltfläche Mehr und wählen Sie Neue Version > Testversand aus. Dadurch gelangen Sie zur Seite Neue Version , auf der der Workflow übertragen wird. Außerdem können Sie alle notwendigen Anpassungen vornehmen, bevor Sie die neue Version weiterleiten.

**Frage**

Szenario - Testsendungen weiterleiten: Ein externer Kunde, der einen Testversand überprüft, sollte sich vor der Genehmigung des Testversands intern in seiner Organisation umkreisen lassen. Die anderen, die überprüfen werden nicht unbedingt im System, sodass es nicht @ in den Kommentaren funktioniert. Wie sollten sie die E-Mail am besten freigeben - leiten Sie die E-Mail weiter und weisen Sie dem Empfänger gegenüber darauf hin, dass Kommentare nicht als ihr Name erscheinen würden?

**Antwort**

Sie sollten die Funktion &quot;Abonnements testen&quot;verwenden. Diese Option kann in den Testversandeinstellungen aktiviert werden. Die Empfänger des Testversands können dann einen allgemeinen öffentlichen Link zum Testversand weiterleiten und Personen die Möglichkeit geben, sich für den Testversand anzumelden (im Wesentlichen selbst hinzufügen).

**Frage**

Was ist eine Best Practice für die Verwendung der Ordner in Dokumenten?

**Antwort**

Dies hängt von der Art des Projekts ab. Sie können jedoch einen Ordner für aktive Testsendungen in Betracht ziehen, der alle Testsendungen/Versionen enthält, die aktiv umgeleitet werden, sowie einen Ordner für genehmigte Testsendungen, der alle abgeschlossenen und validierten Testsendungen enthält. Sobald ein Testversand vollständig genehmigt wurde, verschieben Sie ihn aus dem Ordner &quot;Aktive Testsendungen&quot;in den Ordner &quot;Validierte Testsendungen&quot;.

**Frage**

Wenn ich drei Personen in einer Gruppe von Rezensionen habe, kann ich feststellen, dass ich von den 3 Genehmigungen benötige?

**Antwort**

Ja. Sie möchten die beiden Personen hinzufügen, die Sie als Prüfer und Genehmiger benötigen, und die dritte Person als Prüfer.

**Frage**

Wir möchten einen Testversand an einen externen Kunden (Nicht-Workfront-Benutzer) senden, um diesen zu prüfen und zu kommentieren. Wir möchten ihnen einen sauberen Beweis (d. h. einen, der keine internen Kommentare dazu enthält) zukommen lassen. Was sind die richtigen Schritte, um dies zu erreichen, um sicherzustellen, dass der externe Kunde den Testversand erhält (nur den Testversand, keinen Zugriff auf das Projekt selbst) und wie &quot;schicken&quot; die externen Kunden uns ihren ausgestellten Testversand zurück? Derzeit werden keine Testversandvorlagen/automatisierten Workflows verwendet.

**Antwort**

Es wird empfohlen, hierfür automatisierte Workflow-/automatisierte Workflow-Vorlagen zu verwenden, da Sie so die Funktion &quot;Private Stage&quot; verwenden können. Bei Verwendung der Funktion für die private Bühne können Sie die Kommentare/Entscheidungen und Empfänger bestimmter Phasen der Überprüfung für Personen in anderen Phasen verborgen halten. Beispielsweise könnten Sie eine interne Staging-Phase als private Staging und eine Client-Staging-Umgebung haben. Die Clients können nichts mit der internen Bühne zu tun haben, während Sie die Aktivität in der Client-Bühne sehen können.

**Frage**

Ist es möglich, bestimmte Benutzer (auch als Korrekturleser bezeichnet) in einem frühen Stadium zu halten, ohne dass sie in späteren Stadien angemeldet werden müssen?

**Antwort**

Sobald jemand in einer Phase einer Testversand-Version hinzugefügt wurde, bleibt er in den verbleibenden Phasen auf dieser Testversion. Sie haben die Möglichkeit, ihre Bühne zu sperren, wenn die nächste Phase beginnt (oder manuell), wodurch sie keine weiteren Kommentare abgeben können.

**Frage**

Wo können wir eine Liste aller Personen anzeigen, die einen Nachweis geprüft und/oder genehmigt haben, eines Tages und zu welcher Uhrzeit? Zu Prüfungszwecken usw. Gibt es auch einen Ort, an dem wir alle Prüfungen und Genehmigungen für alle Versionen eines Testversands sehen können?

**Antwort**

Um eine Liste der Aktivitäten anzuzeigen, z. B. wann Kommentare und Entscheidungen getroffen wurden, klicken Sie im Abschnitt &quot;Details des Testversands&quot;auf den Aktivitätsverlauf. Gehen Sie dazu wie folgt vor: Wählen Sie auf der Registerkarte Dokumente den Testversand aus > Klicken Sie auf Details des Testversands > Erweitern Sie den Abschnitt Aktivität . Wenn Sie diese Informationen auf Versionsebene sehen möchten, gehen Sie wie folgt vor: Wählen Sie den Testversand auf der Registerkarte Dokumente aus > Klicken Sie auf die Registerkarte Details > Unten im Bildschirm wird der Abschnitt Versionen angezeigt. Von hier aus können Sie auf die Details des Testversands auf der Versionsebene zugreifen.

**Frage**

Können Sie bitte ein wenig über private Bühnen beim Testen sprechen?

**Antwort**

Wenn eine Phase privat durchgeführt wird, sind Kommentare und Entscheidungen für Personen nicht sichtbar, die dieser Phase nicht hinzugefügt wurden oder keine Supervisoren-, Administratoren- oder Rechnungsadministratoren in dem Konto sind. Überprüfer, die einer privaten Bühne hinzugefügt werden, können auch nur die Bühne sehen, der sie auf dem Testversand und den Kommentaren in dieser Phase hinzugefügt wurden.
