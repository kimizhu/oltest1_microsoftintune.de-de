---
description: na
keywords: na
title: Troubleshoot client setup in Microsoft Intune
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e46d292b-1d16-46db-a87f-d53eefa4d22a
---
# Behandlung von Problemen bei der Clienteinrichtung in Microsoft Intune

## Behandlung von Problemen bei der Clienteinrichtung
Die folgenden Abschnitte enthalten Informationen zu gängigen Problemen bei der Clienteinrichtung.

### Vorgehensweise bei Clientinstallationsfehlern

-   Wenn in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] für den Computer keine Warnungen zur Softwarebereitstellung angezeigt werden, überprüfen Sie Internetverbindung und Proxykonfiguration des Computers und stellen Sie sicher, dass der Computer mit der Dienst-URL [https://manage.microsoft.com](https://manage.microsoft.com) kommunizieren kann. Wiederholen Sie anschließend die Installation der Clientsoftware.

-   Sie können eine E-Mail-Nachricht an ausgewählte Empfänger versenden lassen, wenn eine Fehlerwarnung bei der Bereitstellung von Clientsoftware auftritt. Konfigurieren Sie dazu eine Benachrichtigungsregel im Arbeitsbereich **Admin**. Weitere Informationen finden Sie unter [Benachrichtigungen durch Microsoft Intune-Warnungen](../Topic/Get_notified_by_Microsoft_Intune_alerts.md).

-   [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] zeigt die kritische Warnung **Fehler bei der Bereitstellung der Clientsoftware** an, wenn die Bereitstellung der Clientsoftware fehlschlägt. Diese Warnung wird auf den Seiten **Systemübersicht** und **Warnungen** in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] angezeigt. Überprüfen Sie die Warnungen auf die folgende Weise:

##### So suchen Sie in den Warnungen nach Hinweisen auf fehlerhafte Installationen

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Warnungen** &gt; **Übersicht**.

2.  Auf der Seite **Warnungsübersicht** finden Sie die folgenden Informationen:

    -   die drei wichtigsten Warnungen, sortierbar nach Datum, Kategorie oder Schweregrad

    -   die Gesamtzahl der aktiven Warnungen

3.  Klicken Sie auf **Alle Warnungen**, um die folgenden Informationen auf der Seite **Warnungen** anzuzeigen. Kritische Warnungen werden zuerst angezeigt:

    -   **Name**: Dies ist der Name des Warnungstyps, von dem die Warnung generiert wurde.

    -   **Quelle**: Dies ist ein Link zur Quelle der Warnung.  Wenn der Anzeigeschwellenwert des Warnungstyps auf **Alle** festgelegt ist, wird über diesen Link ein einzelnes betroffenes Gerät angezeigt.  Wenn der Anzeigeschwellenwert des Warnungstyps auf einen Wert festgelegt ist, wird über diesen Link eine Liste aller Geräte angezeigt, die von dieser Warnung betroffen sind.

    -   **Zuletzt aktualisiert**: Hier wird angegeben, wann die Warnung zuletzt geändert wurde. Wenn eine Warnung geschlossen ist, wird hier die Uhrzeit angezeigt, zu der die Warnung geschlossen wurde.

    -   **Schweregrad**: Gibt den Schweregrad der Warnung an

### <a name="BKMK_Whattodo"></a>Vorgehensweise, wenn sich der Client nicht in der Microsoft Intune-Administratorkonsole deinstallieren lässt

##### So entfernen Sie die Clientsoftware unter Verwendung des Microsoft Intune-Befehlszeilentools

1.  Öffnen Sie eine Eingabeaufforderung im Administratormodus.

2.  Navigieren Sie zum Ordner *%programfiles%\Microsoft\OnlineManagement\Common*

3.  Führen Sie den folgenden Befehl aus: **ProvisioningUtil.exe /UninstallAgents /MicrosoftIntune**.

### Fehlercodes bei der Clientinstallation
In der folgenden Tabelle werden Fehlercodes erläutert, die in **Warnungen** angezeigt werden, wenn die Installation der Clientsoftware fehlschlägt. Gleichzeitig werden Vorschläge zur Behebung der Probleme vorgestellt, für die die Fehlercodes stehen.

|Fehlercode|Mögliches Problem|Lösungsvorschlag|
|--------------|---------------------|--------------------|
|**0x80CF0437**|Die Uhr des Clientcomputers ist nicht auf die richtige Uhrzeit eingestellt.|Stellen Sie sicher, dass die Uhr und die Zeitzone des Clientcomputers richtig eingestellt sind.|
|**0x80240438**, **0x80CF0438**, **0x80CF401B**|Verbindung mit [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Dienst nicht möglich. Überprüfen Sie die Proxy-Einstellungen des Clients.|Überprüfen Sie, ob die Proxykonfiguration des Clientcomputers von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] unterstützt wird, und ob der Clientcomputer Zugang zum Internet hat. Weitere Informationen zu den unterstützten Proxykonfigurationen finden Sie unter [Schützen von Windows-PCs mit Endpoint Protection für Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).|
|**0x80CF402C**|Verbindung mit [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Dienst nicht möglich. Überprüfen Sie die Netzwerkverbindungen.|Überprüfen Sie, ob der Computer über eine Netzwerkverbindung verfügt. Stellen Sie sicher, dass das Netzwerkkabel verbunden bzw. das Funknetzwerk aktiv ist.|
|**0x80240438, 0x80CF0438**|Proxyeinstellungen in Internet Explorer und im lokalen System sind nicht konfiguriert.|Überprüfen Sie die Proxyeinstellungen des Clients, und vergewissern Sie sich, dass die Proxykonfiguration des Clientcomputers von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] unterstützt wird und der Clientcomputer mit dem Internet verbunden ist. Weitere Informationen zu den unterstützten Proxykonfigurationen finden Sie unter [Schützen von Windows-PCs mit Endpoint Protection für Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).|
|**0x80043001**|Das Registrierungspaket ist nicht mehr aktuell.|Laden Sie das aktuellste Clientsoftwarepaket vom Arbeitsbereich **Admin** herunter, und installieren Sie es. Weitere Informationen finden Sie im Thema [Installieren des Windows-PC-Clients mit Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).|
|**0x80043004**|Das Abonnement ist nicht vorhanden oder wurde deaktiviert.|Prüfen Sie, ob Ihr Konto und Ihr Abonnement für [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] noch aktiv sind. Melden Sie sich zum Anzeigen Ihrer Kontoeinstellungen bei Ihrem Konto im [Microsoft Intune-Kontenportal](http://go.microsoft.com/fwlink/?LinkId=247978) an.|
|**0x80043002**|Das Konto befindet sich im Wartungsmodus.|Wenn sich das Konto im Wartungsmodus befindet, können Sie keine neuen Clientcomputer registrieren. Melden Sie sich zum Anzeigen Ihrer Kontoeinstellungen bei Ihrem Konto im [Microsoft Intune-Kontenportal](http://go.microsoft.com/fwlink/?LinkId=247978) an.|
|**0x80043003**|Das Konto wurde gelöscht.|Prüfen Sie, ob Ihr Konto und Ihr Abonnement für [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] noch aktiv sind. Melden Sie sich zum Anzeigen Ihrer Kontoeinstellungen bei Ihrem Konto im [Microsoft Intune-Kontenportal](http://go.microsoft.com/fwlink/?LinkId=247978) an.|
|**0x80043005**|Der Clientcomputer wurde abgekoppelt.|Warten Sie einige Stunden, entfernen Sie ältere Versionen der Clientsoftware von dem Computer, und versuchen Sie dann erneut, die Clientsoftware auf dem Computer zu installieren. Weitere Anweisungen finden Sie unter [What to do if the client will not uninstall from the Microsoft Intune administrator console](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md#BKMK_Whattodo).|
|**0x80043006**|Die maximal zulässige Anzahl von Arbeitsplätzen für das Konto wurde erreicht.|Ihr Unternehmen muss zusätzliche Arbeitsplätze erwerben, bevor Sie weitere Clientcomputer bei dem Dienst registrieren können.|
|**0x80043007**|Zertifikatsdatei wurde im Ordner des Installationsprogramms nicht gefunden.|Extrahieren Sie alle Dateien, bevor Sie die Installation starten. Die extrahierten Dateien dürfen nicht umbenannt oder verschoben werden: Alle Dateien müssen im selben Ordner vorhanden sein, da die Installation sonst fehlschlägt. Weitere Informationen finden Sie unter [Installieren des Windows-PC-Clients mit Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).|
|**0x8024D015**, **0x00240005**, **0x80070BC2**, **0x80070BC9**, **0x80CFD015**|Die Software kann nicht installiert werden, weil ein Neustart des Clientcomputers aussteht.|Starten Sie den Computer neu, und wiederholen Sie dann die Installation der Clientsoftware.|
|**0x80070032**|Eine oder mehrere Voraussetzungen, die für die Installation der Clientsoftware erforderlich sind, wurden auf dem Clientcomputer nicht gefunden.|Stellen Sie sicher, dass alle erforderlichen Updates auf dem Clientcomputer installiert sind, und versuchen Sie dann erneut, die Clientsoftware zu installieren. Weitere Informationen zu den Voraussetzungen für die Installation der Clientsoftware finden Sie unter [Anforderungen an die Netzwerkinfrastruktur für Microsoft Intune](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md).|
|**0x80043008**|Der Dienst „Updates für Microsoft Online Management“ konnte nicht gestartet werden.|Wenden Sie sich an den [Support](http://go.microsoft.com/fwlink/?LinkID=246606).|
|**0x80043009**|Der Clientcomputer ist bereits für den Dienst registriert.|Sie müssen den Clientcomputer abkoppeln, bevor sie ihn erneut für den Dienst registrieren können. Weitere Anweisungen finden Sie unter [What to do if the client will not uninstall from the Microsoft Intune administrator console](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md#BKMK_Whattodo).|
|**0x8004300B**|Das Installationspaket für die Clientsoftware kann nicht ausgeführt werden, da die Windows-Version auf dem Client nicht unterstützt wird.|Die auf dem Client ausgeführte Windows-Version wird von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] nicht unterstützt. Eine Liste der unterstützten Betriebssysteme finden Sie unter [Anforderungen an die Netzwerkinfrastruktur für Microsoft Intune](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md).|
|**0xAB2**|Fehler beim Zugriff auf die VBScript-Laufzeit für die benutzerdefinierte Aktion.|Dieser Fehler wird von einer benutzerdefinierten Aktion verursacht, die auf DLLs (Dynamic-Link Libraries) aufbaut. Um den DLL-Fehler zu ermitteln, benötigen Sie möglicherweise die Tools, die im Artikel 198038 der [Microsoft Support-KB: Hilfreiche Tools bei Problemen mit der Paketerstellung und Weitergabe](http://go.microsoft.com/fwlink/?LinkID=234255) erläutert werden.|
|**0x8004300f**|Die Software kann nicht installiert werden, da der System Center Configuration Manager-Client bereits installiert ist.|Entfernen Sie den Configuration Manager-Client, und wiederholen Sie dann die Installation der Clientsoftware.|
|**0x80043010**|Die Software kann nicht installiert werden, da der OMADM-Client (Open Mobile Alliance Device Management) bereits installiert ist.|Heben Sie die Registrierung des OMADM-Clients auf, und wiederholen Sie dann die Installation der Clientsoftware.|
Treten weiterhin Installationsprobleme auf, wenden Sie sich an den [Support](http://go.microsoft.com/fwlink/?LinkID=246606). Halten Sie das Registrierungsprotokoll des Clientcomputers (dieses befindet sich unter %*programfiles*%\Microsoft\OnlineManagement\Logs\Enrollment.log und %*userprofile*%\AppData\Local\Microsoft\OnlineManagement\Logs\Enrollement.log) und das Windows Update-Protokoll (%*windir*%\windowsupdate.log) für die Supportmitarbeiter bereit.

