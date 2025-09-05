---
title: Technische Sitzungen - Adobe Campaign-Subdomain- und SSL-Verwaltung im Control Panel
description: Erfahren Sie, wie Sie Subdomains im Control Panel von Adobe Campaign delegieren und konfigurieren, SSL-Zertifikate einrichten und die Konfiguration überwachen, um eine sichere E-Mail-Zustellbarkeit zu gewährleisten.
solution: Campaign
feature: Subdomains and Certificates
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 3409
last-substantial-update: 2025-09-05T00:00:00Z
jira: KT-18866
source-git-commit: 18ce421793d97372198151afc92b24f3bed053a8
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Technische Sitzungen: Adobe Campaign-Subdomain- und SSL-Verwaltung im Control Panel

In dieser Sitzung untersuchen wir die Konzepte der Subdomain-Delegierung und -Konfiguration in Adobe Campaign, einschließlich der Installation von SSL-Zertifikaten zur Sicherung von Subdomains.

Erfahren Sie, was eine Subdomain ist, welche Zwecke sie hat und welche Delegierungsmethoden Adobe ihre effektive Verwendung ermöglichen. In der Sitzung werden auch die Prinzipien zum Schützen einer Subdomain durch SSL-Zertifikate und Best Practices für die Pflege einer sicheren Umgebung behandelt.

Wir bieten eine schrittweise Anleitung zur Konfiguration von Subdomains mithilfe des Self-Service Control Panels, in der potenzielle Hindernisse und deren Bewältigung hervorgehoben werden. Die Teilnehmer erwerben praktische Kenntnisse, um eine reibungslose Einrichtung und sichere Verwaltung ihrer Subdomains zu gewährleisten.

Unabhängig davon, ob Sie Administrator, Entwickler oder Plattformbesitzer sind, erhalten Sie in dieser Sitzung die Fähigkeiten, Subdomains in Adobe Campaign sicher zu konfigurieren und zu schützen.

>[!VIDEO](https://video.tv.adobe.com/v/3471391/?learn=on&enablevpops)

## Beherrschen der Subdomain-Verwaltung in Adobe Campaign

Entfesseln Sie die Grundlagen der Zuweisung, Konfiguration und Sicherheit von Subdomains für die E-Mail-Kommunikation in Adobe Campaign:

* **Subdomain-Delegierung** Wählen Sie zwischen vollständiger oder CNAME-Delegierung, um zu steuern, wie Adobe Ihre DNS- und E-Mail-Zustellbarkeit verwaltet.
* **DNS- und SSL-Setup** Die ordnungsgemäße Konfiguration von MX-, SPF-, DKIM-, DMARC- und SSL-Zertifikaten ist für einen sicheren, seriösen E-Mail-Versand von entscheidender Bedeutung.
* **Control Panel** Verwenden Sie das Self-Service-Tool von Adobe, um die Einrichtung von Subdomains zu optimieren, Einträge zu überwachen und SSL-Zertifikate zu verwalten.
* **Häufige Fehler** Vermeiden Sie Verzögerungen und Fehler, indem Sie sich mit Audit-Zeitplänen, Datensatzanforderungen und Schritten zur Fehlerbehebung vertraut machen.

Durch die Beherrschung dieser Prozesse sind Ihre Kampagnen sicher, lieferbar und wahren den Ruf Ihrer Marke.

## Delegationsmethoden: ** vs. CNAME

* **Vollständige Delegierung** Adobe verwaltet alle DNS-Einträge für die Subdomain und gewährleistet so optimale Zustellbarkeit und Sicherheit. Empfohlen für die meisten Benutzer.
* **CNAME-Delegierung** Der Kunde und Adobe teilen sich DNS-Verantwortlichkeiten. Der Kunde erstellt CNAME-Einträge, die auf von Adobe verwaltete Ressourcen verweisen.
* **Die wichtigsten Unterschiede:
* **Vollständig** Adobe verfügt über die volle Berechtigung; weniger Kundenwartung.
* **CNAME** Gemeinsame Verantwortung; mehr manuelle Schritte für den Kunden.
* **Tipp** Delegieren Sie niemals Ihre Stamm-Domain - nur Subdomains -, um zu vermeiden, dass Sie die Kontrolle über Ihre Haupt-Domain verlieren.
