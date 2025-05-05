---
title: Best Practices für einen leistungsstarken Versand
description: Optimieren Sie die Medienbereitstellung und -leistung mit Dynamic Media durch die Nutzung von adaptivem Streaming, benutzerdefinierten Videoprofilen, Best Practices für SEO, Bildoptimierung, Masseninhalts-Management, Viewer-Vorgaben, Cache-Invalidierung und intelligenter Bildbearbeitung.
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

# Best Practices für einen leistungsstarken Versand

Seien Sie dabei, wenn Riya Midha, Sr. Product Manager bei Adobe, die Best Practices für die Einrichtung von Adobe Experience Manager Assets Dynamic Media erkundet. Erfahren Sie, wie Sie die Asset-Bereitstellung optimieren, Video-Streaming verbessern, Viewer konfigurieren und die Leistung messen und verbessern können.

>[!VIDEO](https://video.tv.adobe.com/v/3440426/?learn=on&enablevpops&captions=ger)

## Community-Diskussion

Setzen Sie das Gespräch in der Adobe Developers Live-Community [Diskussion](https://adobe.ly/3YGedpb) fort.

## Wichtige Erkenntnisse

* **Dynamic Media-Funktionen** Dynamic Media ermöglicht die schnelle und flexible Bereitstellung hochwertiger, personalisierter Medien auf allen Geräten, die mehr als 9 Billionen Mediensendungen pro Jahr und tägliche Spitzenmengen von bis zu 69 Milliarden Assets verarbeiten.
* **Adaptives Streaming** Die Verwendung von adaptivem Streaming für die Videobereitstellung reduziert die Pufferung erheblich. Ein Test zeigte eine Verringerung der Pufferanzahl von 50 auf 5 in einem 60-Sekunden-Video mit einer eingeschränkten Bandbreite von 5 Mbit/s.
* **Videoprofile** Das Erstellen benutzerdefinierter Videoprofile mit verschiedenen Kodierungen sorgt für eine optimale Videoleistung bei unterschiedlichen Netzwerkbedingungen.
* **Best Practices für SEO**
   * Verwenden Sie Regelsätze, um beschreibende URLs für eine bessere SEO zu erstellen.
   * Hinzufügen von Alternativtext und Titelattributen zu Bildern.
   * Nutzen Sie die intelligente Bildbearbeitung und die neuesten Bildformate wie WebP für bessere Such-Ranglisten.
* **Bildoptimierung**
   * Skalierungsparameter verwenden, um die Bildauflösung an die Bildschirmgröße anzupassen.
   * Vermeiden Sie die Verwendung einer 100%igen Bildqualität. Verwenden Sie stattdessen einen Bereich von 80 bis 90 %, um die Dateigröße ohne merklichen Qualitätsverlust zu reduzieren.
   * Wenden Sie Scharfzeichnungsparameter an, um die Textklarheit in Bildern zu verbessern.
* **Masseninhalts-Management**
   * Trennung von Inhalten, die für die Bereitstellung von Dynamic Media vorgesehen sind, von anderen Inhalten.
   * Verwenden Sie selektive Synchronisierung, um die Verarbeitungszeiten zu optimieren und die Markteinführungszeit zu verbessern.
* **Viewer-Vorgaben** Passen Sie das Erscheinungsbild und Verhalten des Viewers mithilfe von Viewer-Vorgaben ohne Code-Änderungen an. Beispiele sind das Bearbeiten von Wiedergabe-/Pause-Schaltflächen, das Aktivieren der automatischen Wiedergabe und Schleife und das Hinzufügen von Bildüberlagerungen.
* **Cache-Invalidierung** Verwenden Sie die Cache-Invalidierung, um Änderungen an bereits veröffentlichten Assets sofort widerzuspiegeln, und umgehen Sie die standardmäßige 10-Stunden-TTL.
* **Überwachung und Debugging** Verwenden Sie Tools wie das AEM-Desktop-Programm und die Seite „Abfrage-Debugger“, um Verarbeitungsaufträge zu verfolgen und nicht verarbeitete Assets zu identifizieren.
* **Intelligente Bildbearbeitung** Die intelligente Bildbearbeitung ist standardmäßig auf allen Domains aktiviert, wodurch die Größe der Bilddateien verringert und die Ladezeiten verbessert werden.
