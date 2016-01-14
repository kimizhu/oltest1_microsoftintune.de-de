---
description: na
keywords: na
title: Get ready to enroll devices in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44fd4af0-f9b0-493a-b590-7825139d9d40
---
# Vorbereiten der Registrierung von Ger&#228;ten in Microsoft Intune
![](../Image/Nav_Icons/WIT_Tile_W_Overview.png)![](../Image/Nav_Icons/WIT_Tile_W_GetStarted.png)![](../Image/Nav_Icons/WIT_Tile_W_EnrollDevicesHighlight.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageDevices.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageApps.png)![](../Image/Nav_Icons/WIT_Tile_W_ProtectResources.png)![](../Image/Nav_Icons/WIT_Tile_W_RetireData.png)![](../Image/Nav_Icons/WIT_Tile_W_TechnicalReference.png)![](../Image/Nav_Icons/WIT_Tile_W_Troubleshooting.png)
![](../Image/Nav_Icons/WIT_Banner_EnrollDevices.png)

Damit Mitarbeiter auf mobilen Geräten (einschließlich Android, iOS und Windows Phone) Unternehmensressourcen verwenden können, müssen Sie die Geräteregistrierung aktivieren. Dies ist der Vorgang, der die Verwaltung der Geräte ermöglicht. Dazu müssen Sie zunächst [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] als Autorität für die Verwaltung mobiler Geräte festlegen und für das Betriebssystem des Geräts die Registrierung aktivieren. Computer unter Windows 8.1 und Windows 10 können wahlweise als mobile Geräte oder mithilfe der [Intune-Clientsoftware](http://technet.microsoft.com/library/dn646959.aspx) verwaltet werden.

## Aktivieren der Registrierung mobiler Geräte
Zum Aktivieren der MDM-Registrierung müssen Sie die *Autorität für die Verwaltung mobiler Geräte* festlegen. Die Autorität für die Verwaltung mobiler Geräte definiert den Verwaltungsdienst mit der Berechtigung zum Verwalten einer Gruppe von Geräten.  Optionen für die Autorität für die Verwaltung mobiler Geräte sind [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], Configuration Manager mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] oder Office 365 MDM-Lösungen.  Office 365 und Intune können zusammen verwendet werden, um mobile Geräte zu verwalten. Wenn System Center Configuration Manager als Verwaltungsautorität festgelegt ist, kann kein anderer Dienst für die Verwaltung mobiler Geräte verwendet werden. Legen Sie als Einstieg [Intune als Autorität für die Verwaltung mobiler Geräte fest](https://technet.microsoft.com/library/mt346013.aspx).

Sie müssen dann die Registrierung für die Betriebssysteme aktivieren, die Ihre Organisation unterstützen möchte. Bestimmte mobile Betriebssysteme (z. B. Windows und iOS) erfordern eine Vertrauensstellung zwischen den Geräten und [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], um die Verwaltung zu ermöglichen.

-   [Einrichten der Android-Verwaltung mit Microsoft Intune](../Topic/Set_up_Android_management_with_Microsoft_Intune.md)

-   [Einrichten der iOS-Verwaltung mit Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) - Einschließlich [unternehmenseigener iOS-Geräte](https://technet.microsoft.com/library/dn408185.aspx#BKMK_DEP)

-   [Einrichten der Windows Phone-Verwaltung mit Microsoft Intune](../Topic/Set_up_Windows_Phone_management_with_Microsoft_Intune.md)

-   [Einrichten der Windows-Geräteverwaltung mit Microsoft Intune](../Topic/Set_up_Windows_device_management_with_Microsoft_Intune.md)

## Verwalten mehrerer Geräte mit dem Konto für den Geräteregistrierungs-Manager
Mit Intune können Organisationen eine Vielzahl mobiler Geräte mit einem einzelnen Benutzerkonto verwalten. Das Konto *Geräteregistrierungs-Manager* ist ein spezielles Intune-Konto mit Berechtigung zum Registrieren von mehr als fünf Geräten. Weitere Informationen finden Sie unter [Registrieren von firmeneigenen Geräten mit dem Geräteregistrierungs-Manager in Microsoft Intune](../Topic/Enroll_corporate-owned_devices_with_the_Device_Enrollment_Manager_in_Microsoft_Intune.md).

## MDM mit Intune und Exchange ActiveSync
Damit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] mobile Geräte direkt verwalten kann, müssen Benutzer Geräte in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] registrieren. Bei mobilen Geräten, die nicht von Benutzern registriert wurden, können Sie die Verwaltung mit Exchange ActiveSync unter Verwendung von Exchange Connector aktivieren. Exchange-Geräte können sowohl auf lokalen Servern als auch mit einem über Microsoft Office 365 in der Cloud gehosteten Exchange verwaltet werden. Mit dem Exchange Connector stellen Sie eine Verbindung mit Ihrer Exchange-Bereitstellung her und können mobile Geräte über die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole verwalten. Informationen finden Sie unter [Verwaltung mobiler Geräte mit Exchange ActiveSync und Microsoft Intune](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md).

## Siehe auch
[Dokumentation zu Microsoft Intune](../Topic/Documentation_for_Microsoft_Intune.md)

