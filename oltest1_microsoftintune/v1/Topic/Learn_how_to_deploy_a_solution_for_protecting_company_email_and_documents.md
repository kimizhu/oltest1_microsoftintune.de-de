---
description: na
keywords: na
title: Learn how to deploy a solution for protecting company email and documents
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2e10af43-3138-45c0-b2f7-14a1d2bfb237
---
# Erfahren Sie, wie Sie eine L&#246;sung f&#252;r den Schutz von gesch&#228;ftlichen E-Mails und Dokumenten bereitstellen.
Unternehmen ermöglichen ihren Mitarbeitern in zunehmendem Maß, ihre Produktivität durch den Zugriff auf E-Mails, Dokumente und Unternehmensressourcen über mobile Geräte zu erhöhen. Allerdings stellt die Menge der vertraulichen Daten, die in geschäftlichen E-Mails und Dokumenten gespeichert sind, ein hohes Sicherheitsrisiko für Unternehmen dar.

Dieses Handbuch ist für IT-Spezialisten bestimmt, die nach der besten Lösung für Ihr Unternehmen suchen und mithilfe einer der nachfolgend beschriebenen Konfigurationen einen bedingten Zugriff durchsetzen möchten. Dadurch ermöglichen Sie den Mitarbeitern weiterhin die Nutzung mobiler Geräte für den Zugriff auf geschäftliche E-Mails und schützen gleichzeitig die Unternehmensdaten.

> [!TIP]
> Eine herunterladbare Version des gesamten Themenbereichs finden Sie in der [TechNet-Bibliothek](https://gallery.technet.microsoft.com/Deploying-Enterprise-16499404).

## Einführung
Der Schutz von Unternehmensdaten ist äußerst wichtig und wird zunehmend zum Problem, da immer mehr Mitarbeiter ihre mobilen Geräte für den Zugriff auf Unternehmensressourcen (einschließlich E-Mails- und E-Mail-Anlagen) verwenden. Als IT-Administrator möchten Sie sicherstellen, dass die Unternehmensdaten selbst dann geschützt sind, wenn sich die mobilen Geräte nicht am physischen Unternehmensstandort befinden.

Microsoft Enterprise Mobility Suite (EMS) löst dieses Problem und sorgt auf vier Ebenen – Identität, Gerät, Anwendung und Daten – für einen umfassenden Schutz geschäftlicher E-Mails und Dokumente . Neben anderen Funktionen stellt EMS sicher, dass Mitarbeiter nur von Geräten auf geschäftliche E-Mails zugreifen können, die mit Microsoft Intune verwaltet werden und mit den IT-Richtlinien kompatibel sind.

Der Schutz von Unternehmens-E-Mail umfasst zwei Hauptziele:

-   **Zugriff auf geschäftliche E-Mails nur von kompatiblen Geräten**: Ein wichtiger Schritt zum Schutz von Unternehmensdaten besteht im Beschränken des Zugriffs für Geräte, die kein sicheres Kennwort verwenden, für die ein Jailbreak durchgeführt wurde oder die nicht verschlüsselt sind.  Mit Microsoft Intune können Sie Bedingungen festlegen, die Ihre Benutzer für den Zugriff auf die Unternehmensressourcen erfüllen müssen. Dies wird als bedingter Zugriff bezeichnet.

-   **Schützen des Inhalts von E-Mails und E-Mail-Anlagen:** Der bedingte Zugriff gewährleistet zwar, dass nur kompatible Geräte auf E-Mails zugreifen können, doch steht der Schutz der Inhalte in E-Mails und E-Mail-Anlagen immer noch infrage.  Der Inhalt kann kopiert, verschoben, an einem anderen Speicherort gespeichert oder mit einem anderen Benutzer gemeinsam verwendet werden.  EMS löst dieses Problem mithilfe von Verwaltungsrichtlinien für mobile Anwendungen.

    Verwaltete Apps sind Anwendungen, auf die Verwaltungsrichtlinien für mobile Apps angewendet werden, die sie mit den Sicherheitsanforderungen Ihres Unternehmens kompatibel machen. Mit diesen Apps haben Sie die direkte Kontrolle hinsichtlich der Bereitstellung, der laufenden Verwaltung (wie Bestand oder Updates) sowie der selektiven Löschung der Apps und der zugehörigen Daten. Außerdem ermöglicht Intune Ihnen über eine Reihe von MAM-Richtlinien (Verwaltung mobiler Anwendungen) das Ändern der Funktionalität von Apps und das Beschränken der gemeinsamen Nutzung von Daten. Weitere Informationen zur Funktionsweise dieser Lösung einschließlich Details zur Architektur finden Sie unter [Schützen von geschäftlichen E-Mails und Dokumenten](https://technet.microsoft.com/en-us/library/mt574220.aspx).

    > [!NOTE]
    > Sie können ein E-Mail-Profil erstellen und bereitstellen und anschließend eine Compliance-Richtlinie festlegen, die vorschreibt, dass E-Mail-Profile von Intune verwaltet werden müssen (empfohlen). Dies gibt Ihnen die Möglichkeit, E-Mails von deaktivierten Geräten zu entfernen und dadurch sicherzustellen, dass auf iOS-Plattformen Anlagen nur in Anwendungen geöffnet werden können, die von Intune verwaltet werden. Weitere Informationen finden Sie unter [Schritt 5: Erstellen von Kompatibilitätsrichtlinien und Bereitstellung für die Benutzer](../Topic/Use_conditional_access_with_Intune_and_Configuration_Manager.md#Step_5).

### <a name="Step_5"></a>In diesem Artikel beschriebene Lösungen
Dieser Abschnitt enthält eine allgemeine Übersicht über jede Lösung – Implementierung von Configuration Manager zusammen mit Intune, nur Intune, Verwaltung mobiler Anwendungen (MAM) und Azure Rights Management Service (Azure RMS).

-   Verwalten des Zugriffs auf E-Mails über einen bedingten Zugriff

    Sie können Configuration Manager und Intune miteinander kombinieren oder nur Intune, zusammen mit Exchange Online oder Exchange Server im Unternehmen, verwenden, um standortunabhängig auf allen Arten von PCs und mobilen Geräten einen bedingten Zugriff durchzusetzen und zu verwalten. Durch das Erzwingen des bedingten Zugriffs in dieser Art von Umgebung geben Sie dem Benutzer die Möglichkeit, produktiver zu arbeiten, und sorgen gleichzeitig für den Schutz der Unternehmensdaten.

-   Schützen von E-Mail-Anlagen und Daten mithilfe der MAM-Lösung

    In Intune können Sie Richtlinien für die Verwaltung mobiler Anwendungen (MAM) erzwingen und auf diese Weise die Funktionalität der Apps ändern, die Sie in Ihrem Unternehmen bereitstellen. Sie können z. B. Ausschneide-, Kopier- und Einfügevorgänge innerhalb einer verwalteten App einschränken oder eine App so konfigurieren, dass alle Weblinks innerhalb des Managed Browser geöffnet werden. Dadurch wird sichergestellt, dass diese Apps mit den Unternehmensrichtlinien für Compliance und Sicherheit kompatibel sind.

-   Azure Rights Management Service für Richtlinien zur Vermeidung von Datenverlusten

    Azure Rights Management Service (Azure RMS) verwendet zur Sicherung von Dateien und E-Mails auf mehreren Geräten (z. B. Telefon, Tablet und PC) Richtlinien für die Verschlüsselung, Identifizierung und Autorisierung. Informationen können sowohl in Ihrem Unternehmen als auch außerhalb geschützt werden, da der Schutz der Daten erhalten bleibt, auch wenn sie das Firmengelände verlassen.

### Bewerten der gewünschten Implementierung
Die Vielzahl der Design- und Konfigurationsoptionen, die es für die Verwaltung mobiler Apps gibt, macht es schwierig, die Kombination zu ermitteln, die sich am besten für die Anforderungen Ihres Unternehmens eignet. Das Handbuch [Entwurfsüberlegungen für die Verwaltung mobiler Geräte](https://technet.microsoft.com/en-us/library/mt143180.aspx) verdeutlicht die Designanforderungen für die Verwaltung mobiler Geräte und enthält eine Reihe von Schritten und Aufgaben, mit denen Sie eine Lösung entwerfen können, die den geschäftlichen und technologischen Anforderungen Ihres Unternehmens am besten entspricht.

### Allgemeiner Ablauf für den Endbenutzer
Nach dem Implementieren der Lösung können die Endbenutzer nur von verwalteten **und** kompatiblen Geräten auf geschäftliche E-Mails zugreifen. Sobald sie von ihren Geräten auf die E-Mails zugreifen können, werden die Unternehmensdaten geschützt und innerhalb des App-Ökosystems gespeichert. Sie sind nur für die vorgesehenen Benutzer verfügbar. Der Zugriff kann jederzeit widerrufen werden, wenn das Gerät nicht mehr kompatibel ist.

Besonders die in Intune für den bedingten Zugriff festgelegten Richtlinien stellen sicher, dass Geräte nur dann auf E-Mails zugreifen können, wenn sie mit den von Ihnen festgelegten Compliance-Richtlinien kompatibel sind. Aktionen wie Kopieren und Einfügen oder das Speichern bei privaten Cloudspeicherdiensten können mithilfe von Verwaltungsrichtlinien für mobile Apps eingeschränkt werden. Mithilfe des Azure Rights Managements Service kann gewährleistet werden, dass sensible E-Mail-Daten und weitergeleitete Anlagen nur von den bestimmungsgemäßen Empfängern gelesen werden können. Der Ablauf für den Endbenutzer ist unter [Endbenutzererfahrung bei bedingtem Zugriff](../Topic/End-user_experience_of_conditional_access.md) im Detail beschrieben.

## Siehe auch
[Verwenden des bedingten Zugriffs zwischen Intune und Configuration Manager](../Topic/Use_conditional_access_with_Intune_and_Configuration_Manager.md)
[Endbenutzererfahrung bei bedingtem Zugriff](../Topic/End-user_experience_of_conditional_access.md)

