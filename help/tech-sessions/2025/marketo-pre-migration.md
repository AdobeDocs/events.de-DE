---
title: Marketo-Migration zur Adobe Admin Console - (vor der Migration)
description: Adobe migriert Marketo Engage zur besseren Benutzerverwaltung auf die Admin Console. Erfahren Sie mehr über automatische und Self-Migration-Typen, Voraussetzungen, Änderungen nach der Migration, Best Practices, häufige Fehler und Support. Rufen Sie die Sitzungsaufzeichnung auf der Experience League-Website von Adobe auf.
solution: Marketo Engage
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 2280
last-substantial-update: 2025-03-14T00:00:00Z
jira: KT-17483
exl-id: 9c3da83f-9e02-4a2e-9784-10213facf056
source-git-commit: 088615f28aa91dfd4ba119c11c4c9f8a89441d84
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Marketo-Migration zur Adobe Admin Console - Vor der Migration

Seien Sie dabei, wenn Sie Adobe-Experten für eine nahtlose Marketo-Migration begeistern!

In diesem informativen Webinar können Sie sich mit dem Customer Experience &amp; Identity-Team von Adobe schon vor der Marketo-Migration vertraut machen. Wir führen Sie durch die wichtigsten Schritte, Best Practices und gemeinsamen Herausforderungen, um einen reibungslosen Übergang zur Adobe Admin Console zu gewährleisten.

Was Sie lernen werden,

* Eine Schritt-für-Schritt-Roadmap für Ihren Vormigrationsprozess
* Best Practices zur Vereinfachung der Umstellung und Vermeidung von Fallstricken
* Expertenantworten auf gemeinsame Migrationsbelange

Unabhängig davon, ob Sie gerade erst mit der Migration beginnen oder sich auf die letzten Schritte vorbereiten, bietet Ihnen diese Sitzung das Wissen und die Tools, um den Prozess mit Zuversicht zu navigieren. Verpassen Sie nicht die Gelegenheit, vorwärts zu kommen und Ihre Marketo-Migration nahtlos durchzuführen!

>[!VIDEO](https://video.tv.adobe.com/v/3449712/?learn=on&enablevpops)

## Wichtige Erkenntnisse

### Zweck der Migration und Übersicht

Adobe migriert Marketo Engage auf Admin Console, um alle Produkte in einem Hub zu konsolidieren und so die Benutzerverwaltung und den Zugriff zu verbessern.  Die Admin Console dient als zentraler Knotenpunkt für die Verwaltung von Adobe-Produkten, Benutzerrollen, Berechtigungen und Support-Zugriff. Die URLs für den Zugriff auf Marketo Engage werden in die Experience Cloud-Plattform von Adobe geändert.

### Migrationstypen

* **Automatische Migration** Für Organisationen mit weniger als 75 Benutzern und ohne SSL-Einrichtung. Adobe übernimmt die Migration.
* **Selbstmigration** Für Organisationen mit SSL-Einrichtung. Administratoren verwalten den Migrationsprozess mithilfe der Migrationskonsole.

### Voraussetzungen für die Migration

* Systemadministratoren müssen die Einverständnis-E-Mail ausfüllen.
* SSL muss in der Admin Console eingerichtet werden (nicht in der Marketo-Instanz).

### Änderungen nach der Migration

* Benutzende melden sich mit Adobe ID oder einer Federated ID (SSL) an.
* Administratorrollen und -berechtigungen bestimmen die Zugriffsebenen in der Admin Console.

### Best Practices

* Überprüfen Sie die Benutzer-E-Mails und lösen Sie gesperrte Konten vor der Migration auf.
* Stellen Sie sicher, dass korrekte Administratorrollen zugewiesen sind.
* Deaktivieren Sie Anzeigenblocker oder verwenden Sie den Inkognito-Modus, um Anmeldeprobleme zu vermeiden.

### Häufige Fehler

* Falsche Administratorberechtigungen können den Zugriff einschränken.
* Browser-Erweiterungen und Anzeigenblocker können den Zugriff beeinträchtigen.
* IP-Whitelists werden noch nicht von Admin Console unterstützt, werden jedoch derzeit entwickelt.

### Auswirkungen auf die Funktionalität

* Automatisierte E-Mails, API-Benutzer und Munchkin-Codes sind von der Migration nicht betroffen.
* Die Migration wirkt sich hauptsächlich auf die Benutzerauthentifizierung und -verwaltung aus.

### Support

* Benutzende, bei denen Probleme auftreten, sollten einen Support-Fall bei der Adobe-Kundenunterstützung eröffnen.
* Schließen Sie die IMS-Organisations-ID in Support-Fällen ein, um eine schnellere Lösung zu erzielen.
