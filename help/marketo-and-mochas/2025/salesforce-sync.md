---
title: Marketo und Mokkas - Salesforce Sync
description: Beherrschen Sie die Marketo-Salesforce-Synchronisierung mit fachkundiger Anleitung zu Berechtigungen, Außendienstsichtbarkeit, Administratorzusammenarbeit und Best Practices, um eine reibungslose, optimierte Integration sicherzustellen.
feature: Salesforce Integration
topic: Integrations
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 3547
last-substantial-update: 2025-08-07T00:00:00Z
jira: KT-18706
source-git-commit: bc5752512fb1bc50cefe0180c308574e821888a2
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---


# Marketo und Mokkas: Salesforce Sync

Marketo verfügt nur über sehr wenige native Integrationen, aber Salesforce ist die leistungsfähigste von allen. Da rund 90 % der Marketo-Kundinnen und -Kunden auch Salesforce verwenden, berät Adobe Kundinnen und Kunden in Bezug auf die Theorie, Diagnose und Optimierung der Synchronisierung zwischen beiden. Die Marketo-Synchronisierung mit SFDC basiert größtenteils auf den Berechtigungen in SFDC, die dem Marketo-Synchronisierungsbenutzer erteilt werden. Dies kann für Kunden schwierig sein, da mehrere Administratoren oder verschiedene Teams Silos in der Kommunikation rund um Aktualisierungen im System erstellen.

Dieses Webinar behandelt folgende Themen im Zusammenhang mit der Synchronisierung von Marketo &lt;-> SFDC:

・ Erläuterung der Sicht der Vögel auf die Funktionsweise der Synchronisierung
・ Ausblenden von Feldern und Objekten aus dem Marketo Sync-Benutzer in SFDC
・ Kommunikation mit dem SFDC-Administrator
・ Effektive Zusammenarbeit mit dem Marketo Support
・ Zu vermeidende Aspekte beim Synchronisieren von Marketo mit SFDC

>[!VIDEO](https://video.tv.adobe.com/v/3470624/?learn=on&enablevpops)

## Best Practices für die Verwendung von Salesforce Sync

Um Salesforce Sync effektiv mit Marketo zu verwenden, befolgen Sie die folgenden Best Practices, die Schritt für Schritt in einfachen Begriffen erklärt werden:

1. **Grundlegendes zum Synchronisierungsprozess**

   Die Synchronisierung verbindet Marketo und Salesforce, sodass Daten zwischen den beiden Systemen fließen können. Stellen Sie sich den &quot;Marketo Sync User“ als Brücke zwischen den beiden Plattformen vor. Dieser Benutzer ist berechtigt, bestimmte Daten zu lesen und zu schreiben:

   * **Schreibzugriff** Leads und Kontakte (Marketo kann diese in Salesforce aktualisieren).
   * **Lesezugriff** Konten, Opportunities, benutzerdefinierte Objekte und Aktivitäten (Marketo kann diese anzeigen, aber nicht ändern).

   Wenn sich Daten in Salesforce oder Marketo ändern, aktualisiert die Synchronisierung das andere System alle fünf Minuten. Sie können jedoch dringende Aktualisierungen mithilfe von Flussschritten wie „Mit SFDC synchronisieren“ priorisieren.

1. **Felder bereinigen**

   Nur aktiv verwendete Synchronisierungsfelder. Beispiel:

   * Wenn Sie alte Felder wie „COVID-19-Hinweise“ haben, die nicht mehr relevant sind, entfernen Sie diese aus der Synchronisierung. Dadurch wird der Durcheinander reduziert und der Prozess beschleunigt.
   * Vermeiden Sie das Synchronisieren von Formelfeldern (z. B. „Lead-Alter in Tagen„), da sie keine Zeitstempel aktualisieren, was zu Problemen führen kann.

1. **Vermeiden von Rückständen**

   Ein Rückstand tritt auf, wenn zu viele Daten auf die Synchronisierung warten. So vermeiden Sie dies:

   * Unnötige Updates begrenzen: Wenn sich beispielsweise ein Kontowert leicht ändert (z. B. von 60 auf 61), kann er Trigger-Updates für alle zugehörigen Kontakte vornehmen. Gruppieren Sie stattdessen Scores in Bereichen (z. B. 0-25, 26-50), um Aktualisierungen zu reduzieren.
   * Batch-Kampagnen: Verwenden Sie Batch-Kampagnen anstelle von Trigger-Kampagnen, um Daten effizienter zu verarbeiten.

1. **Fehler verwalten**

   Fehler können auftreten, wenn Marketo versucht, ein Feld in Salesforce zu aktualisieren, aber nicht über die entsprechenden Berechtigungen verfügt. Fehlerbehebung:

   * Melden Sie sich bei Salesforce als Marketo-Synchronisierungsbenutzer an und führen Sie dieselbe Aktion aus. Dies hilft bei der Identifizierung von Berechtigungsproblemen oder ungültigen Daten.
   * Richten Sie in Marketo wiederkehrende Kampagnen ein, um häufige Fehler zu beheben, z. B. die Standardisierung von Landes-/Länderwerten (z. B. „CA“ zu „California„).

1. **Benutzerdefinierte Synchronisierungsfilter verwenden**

   Mithilfe benutzerdefinierter Filter können Sie steuern, welche Datensätze zwischen Salesforce und Marketo synchronisiert werden. Erstellen Sie beispielsweise ein Feld namens „Nicht mit Marketo synchronisieren“. Wenn dieses Feld für einen Datensatz mit „true“ markiert ist, wird es nicht mit Marketo synchronisiert. Dies ist nützlich, um ungültige E-Mail-Adressen oder veraltete Kontakte auszuschließen.

1. **Aufgabenerstellung begrenzen**

   In: Elm Salesforce. Konzentrieren Sie sich auf aussagekräftige Aktivitäten wie „ausgefülltes Formular“ oder „geklickter Link in E-Mail“.

1. **Zusammenarbeit mit Ihrem Salesforce-Administrator**

   Da die Synchronisierung beide Systeme umfasst, arbeiten Sie eng mit Ihrem Salesforce-Administrator zusammen, um:

   * Verwalten Sie die Berechtigungen für den Marketo-Synchronisierungsbenutzer.
   * Bereinigen Sie unnötige Felder in Salesforce.
   * Beheben Sie Synchronisierungsprobleme gemeinsam.

1. **Überwachen der Synchronisierungsleistung**

   Überprüfen Sie regelmäßig den Synchronisierungsstatus im Administratorbereich von Marketo:

   Achten Sie auf Spitzen in den Dashboards „Synchronisierungsrückstand - Trend“ oder „Synchronisierungsdurchsatz“. Diese zeigen Verzögerungen oder übermäßige Aktualisierungen an.
Wenn Sie Probleme bemerken, untersuchen Sie, welche Felder oder Datensätze das Problem verursachen.

1. **Benutzerdefinierte Objekte mit Bedacht verwenden**

   Benutzerdefinierte Objekte sind spezielle Datenstrukturen, die zusätzliche Informationen (z. B. Produktdetails) speichern können. Synchronisieren Sie nur benutzerdefinierte Objekte, die für Ihre Kampagnen erforderlich sind, um zu vermeiden, dass Ihre Datenbank aufgebläht wird.

1. **Planen Sie die Skalierbarkeit**

   Berücksichtigen Sie bei der Einrichtung der Synchronisierung langfristig:

   * Pflegen Sie ein Datenwörterbuch, um zu verfolgen, welche Felder synchronisiert werden und warum.
   * Vermeiden Sie das Synchronisieren unnötiger Felder oder Datensätze, um das System effizient zu halten.

Wenn Sie diese Schritte ausführen, können Sie eine reibungslose und effiziente Integration zwischen Marketo und Salesforce sicherstellen, Fehler minimieren und den Wert Ihrer Daten maximieren.
