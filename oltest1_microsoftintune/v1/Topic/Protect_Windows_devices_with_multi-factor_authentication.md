---
description: na
keywords: na
title: Protect Windows devices with multi-factor authentication
search: na
ms.date: na
ms.prod: configuration-manager
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9b4f197d-bc10-4bee-91c9-19bcc8287d36
---
# Sch&#252;tzen von Windows-Ger&#228;ten mit mehrstufiger Authentifizierung in Microsoft Intune
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] integriert die mehrstufige Authentifizierung (MFA), damit Sie Ihre Unternehmensressourcen besser sichern können, indem für Benutzer zu ihrem Benutzernamen und Kennwort eine zusätzliche Verifizierung erforderlich ist. (z. B. zum Verwenden eines Telefonanrufs oder einer Textnachricht)[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] unterstützt die Verwendung von MFA während der Registrierung von Windows 8.1 (oder höher)-, Windows Phone 8.1 oder Windows 10-Mobile-Geräten. Die MFA-Anforderung kann auf Benutzer- oder Gruppenebene auf dem ADFS-Server zugewiesen werden. Verfügt Ihre Organisation über eine lokale IT-Infrastruktur, die eine Active Directory-Domäne mit Konfiguration von Active Directory-Verbunddiensten (ADFS) umfasst, können Sie die MFA auf dem Verbundserver konfigurieren und anschließend in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] registrieren. Wenn Sie die MFA auf dem Verbundserver konfigurieren, sie aber nicht für die Registrierung in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] aktivieren, müssen Benutzer die MFA bei jedem Zugriff auf Unternehmensressourcen durchführen.

Sie können auch die MFA für Azure Active Directory (AAD) verwenden, damit Benutzer sie bei jedem Zugriff auf Unternehmensressourcen durchführen müssen. Diese Anforderung kann individuell für einzelne Benutzer aktiviert werden. AAD-MFA ist ein Clouddienst, der keine lokale IT-Infrastruktur erfordert. Informationen zum Einrichten der AAD-MFA finden Sie unter [Hinzufügen von Multi-Factor Authentication in Azure Active Directory](http://technet.microsoft.com/library/dn249466.aspx).

## <a name="Reqs_MFA"></a>Lokale Infrastrukturanforderungen für ADFS-MFA
Um die mehrstufige Authentifizierung einzurichten, benötigen Sie Folgendes:

-   **Active Directory-Domäne, mit der der ADFS-Server verbunden ist.**

-   **Active Directory Federation Services (ADFS)-Server, konfiguriert für MFA.** Einen Server mit Windows Server 2012 R2, eingerichtet als ADFS-Server. Weitere Informationen finden Sie unter [Verwenden der mehrstufigen Authentifizierung mit Windows Server 2012 R2 AD FS](http://msdn.microsoft.com/library/azure/dn807157.aspx).

Alle oben aufgeführten Server müssen die Systemanforderungen unter [Systemanforderungen und Installationsinformationen für Windows Server 2012 R2](http://technet.microsoft.com/library/dn303418.aspx) erfüllen.

## Anfordern von ADFS-MFA bei der Registrierung von Windows-Geräten
Informationen zum Aktivieren der MFA in ADFS finden Sie unter [Verwalten von Risiken mit zusätzlicher mehrstufiger Authentifizierung für sensible Anwendungen](http://technet.microsoft.com/library/dn280949.aspx).

#### So fordern Sie die MFA-Registrierung in der Intune-Verwaltungskonsole an

1.  Klicken Sie in der Intune-Verwaltungskonsole auf **Admin** &gt; **Verwaltung mobiler Geräte** &gt; **Mehrstufige Authentifizierung**.

2.  Aktivieren Sie MFA in Ihrem Azure AD-Mandanten oder in Ihrer lokalen Umgebung, bevor Sie MFA für die Intune-Registrierung von Windows-Geräten anfordern. Wenn Sie dies nicht tun, erhalten Benutzer eine Fehlermeldung, wenn sie versuchen, ihre Windows-Geräte zu registrieren.

    > [!IMPORTANT]
    > Wenn Sie nicht zuerst MFA in Ihrem Azure AD-Mandanten aktivieren, bevor sie für die Intune-Registrierung angefordert wird, und wenn automatische MDM-Registrierung während des Einbindens in Azure AD konfiguriert ist, erhalten Benutzer eine Fehlermeldung, wenn sie versuchen ihre Windows-Geräte in Azure AD einzubinden.

3.  Klicken Sie auf **Mehrstufige Authentifizierung konfigurieren**, und klicken Sie dann auf **Mehrstufige Authentifizierung aktivieren**.

## Siehe auch
[Schützen von Daten und Geräten mit Microsoft Intune](../Topic/Protect_data_and_devices_with_Microsoft_Intune.md)

