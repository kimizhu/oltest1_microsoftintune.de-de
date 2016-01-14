---
description: na
keywords: na
title: Manage Windows PCs with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b8d22fe-c318-4796-b760-44f1ccf34312
---
# Verwalten von Windows-PCs mit Microsoft Intune
Zusätzlich zur Verwaltung mobiler Geräte können Sie [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] auch zur Verwaltung von Computern verwenden, auf denen unterstützte Betriebssysteme ausgeführt werden, indem Sie die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Computerclientsoftware einsetzen. Die [Hardware- und Softwarevoraussetzungen](https://technet.microsoft.com/library/dn646975.aspx) zur Ausführung des Computerclients sind minimal – im Grunde wird jedes System unterstützt, auf dem Windows Vista oder eine höhere Version ausgeführt werden kann.  Die Clientsoftware lässt sich auch problemlos auf Computern innerhalb einer (beliebigen) oder außerhalb einer Domäne installieren.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwalten Computer mithilfe von Richtlinien, ähnlich wie die Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) der Windows Server Active Directory-Domänendienste (Active Directory Domain Services, AD DS). Wenn Sie Computer in einer Active Directory-Domäne mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwalten, müssen Sie [sicherstellen, dass Intune-Richtlinien nicht zu Konflikten mit GPOs führen](https://technet.microsoft.com/library/dn646986.aspx), die für Ihre Organisation eingerichtet sind.

> [!NOTE]
> Microsoft Intune bietet als eigenständiger Dienst die folgenden Features zum Verwalten von Computern. Geräte, auf denen Windows 8.1 ausgeführt wird, können unter Verwendung des Intune-Clients verwaltet oder als mobile Geräte registriert werden. Die folgenden Informationen gelten für Computer, auf denen der Intune-Client ausgeführt wird. Weitere Informationen über die Verwaltungsfunktionen für mobile Geräte finden Sie unter [Verwaltungsfunktionen für mobile Geräte in Microsoft Intune](https://technet.microsoft.com/library/dn600287(TechNet.10).aspx).

## Installieren des Intune-Computerclients
Der erste Schritt bei der Verwaltung von Computern mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] besteht darin, den Client zu installieren. Die Clientsoftware kann installiert werden, wenn ein Computer durch den [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienst mit einer der folgenden Methoden für die Verwaltung registriert wurde:

-   Sie können [die Microsoft Intune-Clientsoftware manuell bereitstellen](https://technet.microsoft.com/library/dn646969.aspx#BKMK_Manual). Bei dieser Art der Bereitstellung lädt ein Administrator die Intune-Clientsoftware herunter und installiert sie manuell auf jedem PC.

    Für den Download der Intune-Clientsoftware öffnen Sie die Intune-Verwaltungskonsole und laden im Bereich "Clientsoftwaredownload" das Clientsoftwarepaket herunter. Nach der Installation der Clientsoftware installiert Intune automatisch zusätzliche Software, die ggf. zur Verwaltung des Computers erforderlich ist.

-   Sie können die gleichen Dateien, die Sie für die manuelle Installation des Intune-Clients herunterladen, auch zur [Bereitstellung des Clients auf Computern in einer Domäne mithilfe von Active Directory-GPOs verwenden](https://technet.microsoft.com/library/dn646969.aspx).

-   [Benutzer können all ihre Computer über das Intune-Unternehmensportal selbst registrieren](https://technet.microsoft.com/library/dn646969.aspx). Jeder registrierte Computer wird automatisch mit dem Benutzerkonto verknüpft, das zum Installieren der Intune-Clientsoftware verwendet wurde.

-   Sie können die Intune-Clientsoftware auch im Rahmen einer [Betriebssystembereitstellung](https://technet.microsoft.com/library/dn646969.aspx) auf Computern bereitstellen.

## Computerverwaltung mit dem Intune-Computerclient
Nach der Installation des Intune-Clients stellt die Clientsoftware verschiedene Funktionen für die Computerverwaltung bereit, einschließlich der folgenden: [Anwendungsverwaltung](https://technet.microsoft.com/library/dn646961.aspx), Endpoint Protection, Hardware- und Softwarebestand, Softwareupdates sowie Berichterstellung zu Complianceeinstellungen.

Verschiedene vom Computerclient bereitgestellte Aufgaben der Computerverwaltung werden mithilfe von Intune-Richtlinien wie z. B. den folgenden verwaltet:

-   Konfigurieren von [Windows Firewall-Einstellungen](https://technet.microsoft.com/library/mt346040.aspx) auf verwalteten Computern.

-   Konfigurieren von [Softwareupdateeinstellungen](https://technet.microsoft.com/library/dn646968.aspx) für verwaltete Computer zum Suchen und Herunterladen von erforderlichen Softwareupdatees.

-   Schützen der verwalteten Computer vor potenziellen Bedrohungen und Schadsoftwareprogrammen durch [Echtzeitüberwachung und Endpoint Protection](https://technet.microsoft.com/library/dn646970.aspx).

Zusätzlich zu den Aktionen, die der Intune-Client-Agent lokal auf einzelnen Computern ausführt, können Sie die Intune-Verwaltungskonsole auch für andere [allgemeine Computerverwaltungsaufgaben](https://technet.microsoft.com/library/dn646989.aspx) auf Computern verwenden, auf denen der Client installiert ist:

-   Anzeigen von Informationen zum Hardware- und Softwarebestand auf verwalteten Computern

-   Remoteneustart eines Computers

-   Abkoppeln eines Computers zum Deinstallieren der Clientsoftware und Entfernen aus der Intune-Verwaltung

-   Verknüpfen von Benutzern mit bestimmten verwalteten Computern

-   Reagieren auf Remoteunterstützungsanforderungen

Der Intune-Client-Agent wird in der Regel im Hintergrund ausgeführt – Benutzerinteraktionen oder Maßnahmen zur Fehlerbehebung sind nur selten erforderlich. Sollten Sie jedoch Hilfe bei der Behebung von Problemen mit der Computerverwaltung benötigen, stehen verschiedene [Ressourcen zur Lösung zur Verfügung](https://technet.microsoft.com/library/dn646987.aspx).

## Siehe auch
[Konfigurieren und Verwalten von Geräten mit Microsoft Intune](../Topic/Configure_and_manage_devices_with_Microsoft_Intune.md)

