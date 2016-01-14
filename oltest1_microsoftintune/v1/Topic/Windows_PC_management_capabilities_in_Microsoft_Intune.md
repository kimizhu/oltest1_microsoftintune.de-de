---
description: na
keywords: na
title: Windows PC management capabilities in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 77fa5c66-a87c-47df-964c-800eea509b33
---
# Funktionen f&#252;r die Windows-PC-Verwaltung in Microsoft Intune
Sie können [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zum Verwalten von Windows-PCs verenden, auf denen der Intune-Client installiert ist. Über die PC-Verwaltung können Sie Apps und Software sowie Softwareupdates auf Ihren verwalteten PCs bereitstellen, Endpoint Protection und die Windows-Firewall verwalten und vieles mehr.  Im Folgenden finden Sie eine Liste der unterstützten Konfigurationen und Funktionen.

## <a name="BKMK_ClientReqs"></a>Anforderungen für die PC-Verwaltung
**Betriebssysteme**: 
Sie können den [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Client auf PCs installieren, auf denen die folgenden Betriebssysteme ausgeführt werden (sowohl x86 als auch x64):

-   **Windows Vista**: Business, Enterprise oder Ultimate Edition.

-   **Windows 7**: Professional, Enterprise oder Ultimate Edition (ohne Service Pack oder mit SP1).

-   **Windows 8**: Professional oder Enterprise Edition.

-   **Windows 8.1**: Professional oder Enterprise Edition.

-   **Windows 10**: Professional oder Enterprise Edition.

**Hardware**:
Im Folgenden sind die Hardwaremindestanforderungen zum Installieren des [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Clients aufgeführt:

|Anforderungen|Weitere Informationen|
|-----------------|-------------------------|
|Netzwerk|Für den Client ist ein PC mit Internetzugriff erforderlich.|
|Prozessor und Arbeitsspeicher|Weitere Informationen entnehmen Sie den Prozessor- und Arbeitsspeicheranforderungen des PC-Betriebssystems.|
|Speicherplatz|200 MB verfügbarer Speicherplatz vor der Installation der Clientsoftware|
**Software**: 
Im Folgenden sind die Softwareanforderungen zum Installieren des [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Clients aufgeführt:

|Anforderungen|Weitere Informationen|
|-----------------|-------------------------|
|Administratorrechte|Das Konto, mit dem die Clientsoftware installiert wird, muss über lokale Administratorrechte auf dem PC verfügen.|
|Windows Installer 3.1|Auf dem PC wird Windows Installer 3.1 oder höher benötigt.<br /><br />So zeigen Sie die Windows Installer-Version auf einem PC an:<br /><br />-   Klicken Sie auf dem PC mit der rechten Maustaste auf **%windir%\System32\msiexec.exe**, und klicken Sie dann auf **Eigenschaften**.<br /><br />Sie können die neueste Version von Windows Installer von der Microsoft Developer Network-Website unter [Windows Installer Redistributables (Weitervertreibbare Komponenten für Windows Installer)](http://go.microsoft.com/fwlink/?LinkID=234258) herunterladen.|
|Entfernen nicht kompatibler Clientsoftware|Bevor Sie die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Clientsoftware installieren, müssen Sie die folgende Clientsoftware auf dem PC deinstallieren:<br /><br />-   Beliebige Version von [!INCLUDE[cm5short](../Token/cm5short_md.md)]<br />-   Beliebige Version von [!INCLUDE[sccmshortname](../Token/sccmshortname_md.md)]<br />-   Beliebige Version von Systems Management Server (SMS)|

## <a name="WIT_Cap"></a>Intune-Funktionen für die Windows-PC-Verwaltung

-   **Verwalten von Softwareupdates**: Sie können PCs auf dem aktuellen Stand halten und festlegen, wann Updates angewendet werden sollen.

-   **Windows-Firewall-Richtlinie**: Hiermit können Sie sicherstellen, dass die Windows-Firewall auf keinem von Ihrem Unternehmen verwendeten PC inaktiv oder nicht ordnungsgemäß konfiguriert ist.

-   **Schutz vor Schadsoftware**: [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] umfasst Endpoint Protection, um Ihre PCs vor Schadsoftware zu schützen.

-   **Remoteunterstützung**: Mithilfe von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] können Benutzer Kontakt mit IT-Supportmitarbeitern aufnehmen, die ihnen über eine in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] integrierte Remotedesktopfunktion Unterstützung bieten können.

-   **Softwarelizenzverwaltung**.  Überwachen Sie, wie viele Lizenzen verfügbar sind und wie viele Lizenzen verwendet werden.

## Siehe auch
[Einführung in Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)
[Verwalten von Windows-PCs mit Microsoft Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

