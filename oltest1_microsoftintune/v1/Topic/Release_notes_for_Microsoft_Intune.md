---
description: na
keywords: na
title: Release notes for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db9479b2-582d-4a1a-9fbc-fbfc6c680e6f
---
# Anmerkungen zu Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] ist eine integrierte, cloudbasierte Lösung für die Clientverwaltung, die Tools, Berichte und Upgradelizenzen für die aktuelle Windows-Version bietet und Ihre Computer schützt und auf dem neuesten Stand hält. Mithilfe von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] können Sie mobile Geräte im Netzwerk über Exchange ActiveSync oder direkt über [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwalten. Die folgenden Anmerkungen enthalten wichtige Informationen zu [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] sowie bekannte Probleme.

-   [Installation, Bereitstellung und Registrierung](../Topic/Release_notes_for_Microsoft_Intune.md#BKMK_WitRelnoteInstall)

-   [Warnungen](../Topic/Release_notes_for_Microsoft_Intune.md#BKMK_WitRelnoteAlerts)

## <a name="BKMK_WitRelnoteInstall"></a>Installation, Bereitstellung und Registrierung
Die folgenden Probleme können bei der Bereitstellung der Clientsoftware, der Vorbereitung des Clientgeräts für [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] oder bei der Registrierung des Geräts auftreten.

### Wenn Sie ein Windows 8.1-Gerät registrieren, das bei einem Proxyserver authentifiziert werden muss, tritt bei der Registrierung ohne Angabe eines Grunds ein Fehler auf
**Problem:** Wenn Sie ein [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)]-Gerät registrieren und das Gerät während der Registrierung bei einem Proxyserver authentifiziert werden muss, ist die Registrierung nicht möglich, wenn die Anmeldeinformationen für den Proxyserver nicht vom Gerät zwischengespeichert wurden. Wenn die Anmeldeinformationen für den Proxyserver nicht auf dem Gerät zwischengespeichert wurden, muss der Registrierungsvorgang angehalten werden, bis der Benutzer die Anmeldeinformationen eingibt. Während der Registrierung wird jedoch keine Aufforderung zur Eingabe der Anmeldeinformationen für den Proxyserver angezeigt. Das Resultat ist, dass der Registrierungsprozess nicht beim Proxyserver authentifiziert werden kann und dass keine Ursache für diesen Fehler angezeigt wird.

**Problemumgehung:** Konfigurieren und speichern Sie die Anmeldeinformationen für den Proxyserver vor der Registrierung auf allen [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)]-Geräten, die bei einem Netzwerk registriert werden müssen, für das ein authentifizierter Proxyserver erforderlich ist. So konfigurieren und speichern Sie die Anmeldeinformationen auf einem [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)]-Gerät

1.  Öffnen Sie auf dem [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)]-Gerät den **Internet Explorer**.

2.  Wenn Sie zur Eingabe der Anmeldeinformationen für den Proxyserver aufgefordert werden, geben Sie die entsprechenden Details ein, und wählen Sie die Option **Anmeldedaten speichern** aus.

3.  Registrieren Sie das Gerät.

### Die Registrierung von Windows Phone 8.1-Geräten in Microsoft Intune schlägt fehl, wenn die Geräteauthentifizierung in AD FS aktiviert ist
**Problem:** Wenn Sie ein Windows Phone 8.1-Gerät registrieren, tritt bei der Registrierung ein Fehler auf, wenn die optionale Einstellung für die Geräteauthentifizierung als Teil der globalen Authentifizierungsrichtlinie in den Active Directory-Verbunddiensten (AD FS) aktiviert ist.

**Problemumgehung:** Deaktivieren Sie die Geräteauthentifizierung auf dem AD FS-Server, indem Sie **Geräteauthentifizierung aktivieren** unter **Globale Authentifizierungsrichtlinie bearbeiten** deaktivieren. Weitere Informationen finden Sie unter [Konfigurieren von Authentifizierungsrichtlinien](http://technet.microsoft.com/library/dn486781.aspx).

### Mögliche Auswirkungen auf die Darstellung von Geräteeinstellungen durch das Konfigurieren der Einstellung „Nicht jugendfreie Inhalte im Medienstore zulassen“
**Problem:** Wenn die Einstellung **Nicht jugendfreie Inhalte im Medienstore zulassen** auf einem mobilen Gerät konfiguriert ist und bei einem iOS 5- oder iOS 6-Gerät angewendet wird, wird der Status aller Einstellungen bei diesem Gerät unter Umständen als **Konform** angezeigt.

**Problemumgehung:** Zum Anzeigen des korrekten Status der Geräteeinstellungen entfernen Sie die Einstellung **Nicht jugendfreie Inhalte im Medienstore zulassen** aus der Richtlinie und wenden sie dann erneut an.

### Wenn Sie Richtlinien oder Anwendungen für Microsoft Intune-Gruppen festlegen, werden diese nicht auf Geräte der Gruppe „Nicht gruppierte Geräte“ angewendet
**Problem:** Richtlinien und Anwendungen werden von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] gegenwärtig nicht richtig auf Geräte der Gruppe **Nicht gruppierte Geräte** angewendet. Dies gilt selbst dann, wenn die Richtlinie oder Anwendung für eine andere Gruppe als **Nicht gruppierte Geräte** festgelegt wird. Für dieses Problem werden keine Fehler angezeigt.

**Problemumgehung:** Entfernen Sie die Geräte aus der Gruppe **Nicht gruppierte Geräte**, und stellen Sie sicher, dass die Geräte weiterhin mindestens einer anderen Gruppe angehören, der Richtlinien und Anwendungen zugewiesen werden.

### Das Microsoft Intune App Wrapping Tool für Android besitzt keine eigene Deinstallationsfunktion.
**Problem:** Das **Microsoft Intune App Wrapping Tool für Android** besitzt keine eigene Funktion zum Deinstallieren des Tools.

**Problemumgehung:** Navigieren Sie zum Speicherort, in dem Sie das Tool installiert haben, und löschen Sie das Verzeichnis. Der Standardspeicherort für die Installation ist: **C:\Programme (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool**. Weitere Informationen zum App Wrapping Tool finden Sie unter [Vorbereiten von Android-Apps für die Verwaltung von mobilen Anwendungen](http://technet.microsoft.com/library/mt147413.aspx).

## <a name="BKMK_WitRelnoteAlerts"></a>Warnungen
Folgende Probleme mit Warnungen sind in dieser Version von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] bekannt:

### Bei Computern mit Windows 8 oder Windows 8.1 ist keine Remoteunterstützung verfügbar
**Problem:** In dieser Version ist die Remoteunterstützungsfunktion auf Computern mit Windows 8 oder Windows 8.1 nicht verfügbar.

**Problemumgehung:** Keine

### Warnbenachrichtigungen sind bei automatisch hinzugefügten Empfängern nicht funktionsfähig
**Problem:** Wenn ein Empfänger einer Warnbenachrichtigung automatisch hinzugefügt wird, erhält er möglicherweise nicht immer eine Benachrichtigung.

**Problemumgehung:** Fügen Sie Empfänger Warnbenachrichtigung manuell hinzu, um sicherzustellen, dass sie eine Warnungsbenachrichtigung erhalten.

## Siehe auch
[Technische Referenz für Microsoft Intune](../Topic/Technical_reference_for_Microsoft_Intune.md)

