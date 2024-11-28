---
title: Best Practices für die Leistungsbereitstellung
description: Optimieren Sie die Medienbereitstellung und -leistung mit Dynamic Media, indem Sie adaptives Streaming, benutzerdefinierte Videoprofile, Best Practices für SEO, Bildoptimierung, Masseninhaltsmanagement, Viewer-Vorgaben, Cache-Invalidierung und intelligente Bildbearbeitung nutzen.
feature: Dynamic Media, Video, SEO Optimization, Smart Imaging, Viewer Presets, Best Practices
topic: Content Management
solution: Experience Manager, Experience Manager Assets
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 1596
last-substantial-update: 2024-11-26T00:00:00Z
jira: KT-16572
exl-id: a1920020-b9ce-43be-8f9e-e52aac68da7b
source-git-commit: 946d7cd484e8c5d4358d4099b3518705cab8d4a3
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Best Practices für die Leistungsbereitstellung

Treten Sie Riya Midha, Produkt-Manager bei der Adobe bei, um die Best Practices für die Einrichtung von Adobe Experience Manager Assets Dynamic Media zu erkunden. Erfahren Sie, wie Sie die Asset-Bereitstellung optimieren, das Video-Streaming verbessern, Viewer konfigurieren und die Leistung messen und verbessern können.

>[!VIDEO](https://video.tv.adobe.com/v/3440399/?learn=on&enablevpops)

## Community-Diskussion

Fahren Sie mit der Unterhaltung in der Adobe Developers Live Community [diskussion](https://adobe.ly/3YGedpb) fort.

## Wichtige Schritte

* **Dynamic Media-Funktionen** Dynamic Media ermöglicht die schnelle und flexible Bereitstellung hochwertiger, personalisierter Medien auf allen Geräten, die Verarbeitung von jährlich mehr als 9 Billionen Medienlieferungen und ein tägliches Spitzenvolumen von bis zu 69 Milliarden Assets.
* **Adaptives Streaming** Die Verwendung von adaptivem Streaming für die Videobereitstellung reduziert die Pufferung erheblich. Ein Test zeigte eine Verringerung der Pufferanzahl von 50 auf 5 bei einem 60-Sekunden-Video mit einer eingeschränkten Bandbreite von 5 MBit/s.
* **Videoprofile** Das Erstellen benutzerdefinierter Videoprofile mit unterschiedlichen Qualitätskodierungen gewährleistet eine optimale Videoleistung unter verschiedenen Netzwerkbedingungen.
* **Best Practices für SEO**
   * Verwenden Sie Regelsätze zum Erstellen beschreibender URLs für ein besseres SEO.
   * Fügen Sie Bildern alternative Text- und Titelattribute hinzu.
   * Nutzen Sie intelligente Bildbearbeitung und die neuesten Bildformate wie WebP für bessere Suchrankings.
* **Bildoptimierung**
   * Verwenden Sie Skalierungsparameter, um die Bildauflösung basierend auf der Bildschirmgröße anzupassen.
   * Vermeiden Sie die Verwendung von 100 %-Qualität für Bilder. Verwenden Sie stattdessen einen Bereich von 80-90 %, um die Dateigröße zu reduzieren, ohne dass ein deutlicher Qualitätsverlust auftritt.
   * Wenden Sie Scharfzeichnungsparameter an, um die Textklarheit in Bildern zu verbessern.
* **Massen-Content-Management**
   * Trennen Sie Inhalte für die Bereitstellung dynamischer Medien von anderen Inhalten.
   * Verwenden Sie eine selektive Synchronisierung, um die Verarbeitungszeiten zu optimieren und die Markteinführungszeit zu verkürzen.
* **Viewer-Vorgaben** Passen Sie das Erscheinungsbild und Verhalten des Viewers mithilfe von Viewer-Vorgaben ohne Codeänderungen an. Beispiele sind das Bearbeiten von Wiedergabe-/Pause-Schaltflächen, das Aktivieren von automatischer Wiedergabe und Schleife sowie das Hinzufügen von Bildüberlagerungen.
* **Cache-Invalidierung** Verwenden Sie die Cache-Invalidierung, um sofort Änderungen widerzuspiegeln, die an bereits veröffentlichten Assets vorgenommen wurden. Dabei wird die standardmäßige 10-Stunden-TTL umgangen.
* **Überwachung und Debugging** Verwenden Sie Tools wie das AEM-Desktop-Programm und die Seite &quot;Query Debugger&quot;, um Verarbeitungsaufträge zu verfolgen und nicht verarbeitete Assets zu identifizieren.
* **Intelligente Bildbearbeitung** Intelligente Bildbearbeitung ist standardmäßig für alle Domänen aktiviert, was die Größe von Bilddateien verringert und die Ladezeiten verbessert.
