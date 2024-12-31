---
title: Ausführbare Kampagnen - Erfahren Sie, wie ausführbare Dateien die Effizienz und Wirkung steigern können.
description: Seien Sie dabei, wenn Chris Willis, Courtny Edwards-Jones und Jane Musatova in diesem Adobe Champion Deep Dive erfahren, wie ausführbare Kampagnen in Marketo Prozesse optimieren, die Datengenauigkeit gewährleisten und komplexe Workflows automatisieren können - mit praktischen Beispielen und einem Fokus auf die Minimierung von Fehlern und Rückständen.
role: Developer, User
level: Intermediate, Experienced
doc-type: Event
duration: 3778
last-substantial-update: 2024-03-07T00:00:00Z
jira: KT-15098
thumbnail: 3427704.jpeg
exl-id: cfea1a1a-2d29-4cf6-b633-aa2a2523114e
source-git-commit: 8da73b657295864a3bf6c64598b2fbd664a2379d
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Ausführbare Kampagnen - Erfahren Sie, wie ausführbare Dateien die Effizienz und Wirkung steigern können.

>[!VIDEO](https://video.tv.adobe.com/v/3427704/?learn=on)

**Moderiert von** Chris Willis
**Redner** Courtny Edwards-Jones und Jane Musatova

## Übersicht

In dieser Ausgabe des Adobe Champion Deep Dive besprechen wir die Verwendung von ausführbaren Kampagnen in Marketo und liefern Beispiele dafür, wie sie zur Optimierung von Prozessen und zur Gewährleistung der Datengenauigkeit verwendet werden können. Ausführbare Kampagnen sind eine Art intelligente Kampagne, die Flüsse synchron ausführt und Abhängigkeiten zwischen verschiedenen Schritten zulässt. Sie können verwendet werden, um fehlgeschlagene Prozesse wie die Datenstandardisierung oder die Lead-Qualifizierung automatisch zu wiederholen, bevor mit dem nächsten Schritt fortgefahren wird. Das Dokument behandelt auch die Verwendung übergeordneter Kampagnen und verschachtelter ausführbarer Dateien sowie die Einschränkungen ausführbarer Kampagnen, z. B. die Unfähigkeit, Webhooks oder Warteschritte zu verwenden.

## Welchen Zweck haben ausführbare Kampagnen?

Ausführbare Kampagnen dienen der Optimierung und Automatisierung komplexer Workflows in Marketo. Mit ausführbaren Kampagnen können Sie eine Sequenz von Aktionen definieren, die abgeschlossen werden müssen, bevor Sie mit dem nächsten Schritt in einer Kampagne fortfahren. Dadurch wird sichergestellt, dass jede Aktion vollständig ausgeführt wird, bevor der Vorgang fortgesetzt wird, wodurch das Risiko von Fehlern oder unvollständigen Prozessen reduziert wird. Ausführbare Kampagnen können verwendet werden, um fehlgeschlagene Prozesse erneut auszuführen, Daten zu standardisieren und anzureichern, Leads zu qualifizieren, interessante Momente zu erfassen und vieles mehr. Sie bieten eine effizientere und organisiertere Möglichkeit, Marketing-Vorgänge zu verwalten und zu automatisieren.

## Was ist eine ausführbare Kampagne und wie funktioniert sie?

Eine ausführbare Kampagne ist eine Art intelligente Kampagne in Marketo, die die sequenzielle Ausführung mehrerer Flüsse innerhalb einer Kampagne ermöglicht. Sie soll sicherstellen, dass jeder Fluss vollständig ausgeführt wird, bevor der nächste beginnt. Dies unterscheidet sich von einer Anfragekampagne, bei der Flüsse asynchron ausgeführt werden und mehrere Flüsse parallel ausgeführt werden können.

Um eine ausführbare Kampagne zu erstellen, aktivieren Sie beim Erstellen der Kampagne das Kontrollkästchen „Ausführbar“. Nach der Erstellung können Sie der Kampagne Flussschritte hinzufügen, z. B. das Ändern von Datenwerten, das Senden von E-Mails oder das Aktualisieren des Programmstatus. Es gibt jedoch einige Einschränkungen bei ausführbaren Kampagnen. Sie können keine Trigger, Webhooks oder Warteschritte innerhalb einer ausführbaren Kampagne verwenden.

Ausführbare Kampagnen sind für Prozesse nützlich, die voneinander abhängig sind, bei denen ein Fluss abgeschlossen sein muss, bevor der nächste beginnen kann. Sie können dabei helfen, betriebliche Prozesse zu optimieren, die Datenverarbeitung zu vereinfachen und das Risiko von Fehlern oder Rückständen zu minimieren. Durch die Verwendung ausführbarer Kampagnen können Sie sicherstellen, dass jeder Schritt in einem Prozess abgeschlossen ist, bevor Sie mit dem nächsten fortfahren, wodurch die Effizienz und Genauigkeit Ihrer Marketing-Vorgänge verbessert wird.