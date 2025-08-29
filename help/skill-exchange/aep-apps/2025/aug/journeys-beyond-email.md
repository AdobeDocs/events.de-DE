---
title: Adobe Journey jenseits von E-Mails lösen
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer Multi-Channel-Journey entwerfen und testen können, indem Sie Testprofile, Ereignisdaten und reale Szenarien für eine optimale Interaktion verwenden.
feature: Email, Direct Mail, Journeys
role: User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 0
last-substantial-update: 2025-08-28T00:00:00Z
jira: KT-18850
source-git-commit: a633bfda2c2067c6eb34a8743665993dbceea660
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# Adobe Journey jenseits von E-Mails lösen

In dieser Sitzung wird anhand eines konkreten Beispiels die Lösung realer Probleme in Adobe Journey Optimizer untersucht. Es zeigt Strategien für die Erstellung von Multi-Touchpoint-Journey für E-Mail, Voice und Briefpost auf, um kohärente Kundenerlebnisse zu schaffen. Die Teilnehmer erhalten umsetzbare Einblicke und Ansätze aus der Sicht eines Produkteigentümers, um Journey zu optimieren.

## Wichtige Schlussfolgerungen

* Schlüsseln Sie reale Probleme mithilfe spezifischer Cross-Channel-Journey-Mappings auf.
* Für jedes Problem gibt es mehrere gültige Lösungen - Flexibilität ist der Schlüssel.

>[!VIDEO](https://video.tv.adobe.com/v/3471331/?learn=on&enablevpops)

## Anwenden von realen Journey-Szenarien

* **Wiederkehrender Zahlungsrückgang** Wenn die monatliche Zahlung eines Spenders fehlschlägt, können Sie eine kanalübergreifende Antwort erstellen, um das Problem zu beheben und Beziehungen Trigger.
* **Kanalauswahl** Verwenden Sie zuerst E-Mail, dann Briefpost oder Anrufe, wenn die E-Mail unzustellbar ist oder nicht verarbeitet wird.
* **Personalization** Passen Sie Nachrichten basierend auf Spenderdaten an, z. B. Details zum Kindersponsoring, um die Kommunikation relevant zu machen.
* **Skalierbarkeit** Entwerfen Sie Journey, um die Teambeteiligung zu minimieren und zukünftige Updates zu vereinfachen.

## Entwerfen von Multi-Channel-Journey in Schritten

* **Ereignis identifizieren** Beginnen Sie mit der Erkennung eines wiederkehrenden Kreditkartenrückgangs. Hier wird die Journey Trigger.
* **Daten an AEP senden** Erstellen Sie in Adobe Experience Platform ein Batch-Ereignis vom Typ „Ablehnen“ in einem benutzerdefinierten Datensatz.
* **Journey aufschlüsseln** Erstellen Sie drei Microjourneys: E-Mail-Benachrichtigung, Briefpost und ausgehende Anrufe. Jede Version verwendet andere Daten und Timings.
* **Kommunikation personalisieren** Verwenden Sie Ereignisdaten für E-Mails, Profildaten für Druck und Anrufe. Planen Sie im Voraus, damit für jeden Kanal die richtigen Daten verfügbar sind.
* **Überwachen von Antworten** Passen Sie die Journey basierend auf Kundenaktionen (z. B. E-Mail-Öffnungen, Klicks oder Zahlungsauflösung) an, um die nächsten Schritte zu entscheiden.