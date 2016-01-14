---
description: na
keywords: na
title: Mobile device management with Exchange ActiveSync and Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb9618d2-dc90-48be-b921-8044b7e693ac
---
# Verwaltung mobiler Ger&#228;te mit Exchange ActiveSync und Microsoft Intune
Damit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] mobile Geräte direkt verwalten kann, müssen Benutzer Geräte in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] registrieren. Bei mobilen Geräten, die nicht von Benutzern registriert wurden, können Sie die Verwaltung mit Exchange ActiveSync unter Verwendung von Exchange Connector aktivieren. Exchange-Geräte können sowohl auf lokalen Servern als auch mit einem über Microsoft Office 365 in der Cloud gehosteten Exchange verwaltet werden. Sie stellen eine Verbindung mit Ihrer Exchange-Bereitstellung über Exchange Connector her und können mobile Geräte über die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole verwalten. Dort stehen Ihnen folgende Funktionen zur Verfügung:

-   Bereitstellung von Richtlinien für Benutzergruppen zum besseren Schutz der auf mobilen Geräten gespeicherten Unternehmensdaten (z. B. Kennwort, Verschlüsselung und Anlagen)

-   Festlegung von Regeln für den Zugriff auf mobile Geräte nach Gerätefamilie und Gerätemodell, um zu bestimmen, welche mobilen Geräte auf Exchange ActiveSync zugreifen können

-   Registrieren und Umbenennen von Geräten und Aufheben von deren Registrierung

-   Zurücksetzen mobiler Geräte mit der Option zum Zurücksetzen des mobilen Geräts (z. B. bei verlorenen oder gestohlenen Geräten)

Dieses Thema enthält die folgenden Abschnitte:

-   [Konfigurieren von Microsoft Intune On-Premises Connector für lokales oder gehostetes Exchange](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_EX_OP): Verwenden Sie diesen Abschnitt, um Ihre lokale Infrastruktur mit lokalem oder gehostetem Exchange zu konfigurieren.

-   [Konfigurieren von Intune Service to Service Connector für gehostetes Exchange](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_S_S)

-   [Überprüfen der Exchange-Verbindung](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_val_ex)

-   [Zurücksetzen mobiler Geräte, die mit Exchange verwaltet werden](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_EXCap)

-   [Richtlinie für mobile Geräte, die mit Exchange verwaltet werden](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_pol)

-   [Exchange-Zugriffsregeln für mobile Geräte](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_acc)

## <a name="bkmk_EX_OP"></a>Konfigurieren von Microsoft Intune On-Premises Connector für lokales oder gehostetes Exchange
Verwenden Sie diesen Abschnitt, um Ihre lokale Infrastruktur mit lokalem oder gehostetem Exchange zu konfigurieren.

### Anforderungen
Zur Vorbereitung einer Verbindung von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] mit Exchange Server müssen die folgenden Anforderungen erfüllt sein. Sie haben diese Anforderungen möglicherweise bereits beim Einrichten von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] erfüllt.

|Anforderungen|Weitere Informationen|
|-----------------|-------------------------|
|Festlegen der Autorität für die Verwaltung mobiler Geräte für [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|[Festlegen von Microsoft Intune als Autorität für die Verwaltung mobiler Geräte](../Topic/Set_mobile_device_management_authority_and_configure_Microsoft_Intune.md)|
|Sicherstellen, dass die Hardwareanforderungen für On-Premises Connector erfüllt sind|[Anforderungen für On-Premises Connector](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_ExchanceConnectorReqs)|
|Konfigurieren eines Benutzerkontos mit der Berechtigung zum Ausführen der designierten Liste von Windows PowerShell-Cmdlets|PowerShell-Cmdlets für On-Premises Exchange Connector (siehe unten)|

### <a name="bkmk_PS_onprem"></a>PowerShell-Cmdlets für On-Premises Exchange Connector
Sie müssen in Active Directory ein Benutzerkonto erstellen, das von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Exchange Connector verwendet wird. Das Konto muss über die Berechtigung zum Ausführen der folgenden erforderlichen Windows PowerShell-Exchange-Cmdlets verfügen:

-   Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings

-   Get-CasMailbox, Set-CasMailbox

-   Get-ActiveSyncMailboxPolicy, Set-ActiveSyncMailboxPolicy, New-ActiveSyncMailboxPolicy, Remove-ActiveSyncMailboxPolicy

-   Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule

-   Get-ActiveSyncDeviceStatistics

-   Get-ActiveSyncDevice

-   Get-ExchangeServer

-   Get-ActiveSyncDeviceClass

-   Get-Recipient

-   Clear-ActiveSyncDevice, Remove-ActiveSyncDevice

-   Set-ADServerSettings

-   Get-Command

### Laden Sie Microsoft Intune Exchange Connector herunter, und installieren und konfigurieren Sie das Tool.
Zum Einrichten einer Verbindung, über die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] mit dem Exchange-Server kommunizieren kann, auf dem die Postfächer der mobilen Geräte gehostet werden, müssen Sie das Tool für den lokalen Connector über die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Administratorkonsole herunterladen und konfigurieren.

##### So laden Sie das Softwareinstallationspaket für den lokalen Connector herunter

1.  Öffnen Sie die [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2.  Klicken Sie im Bereich für die Arbeitsbereichsverknüpfungen auf **Verwaltung**.

3.  Blenden Sie im Navigationsbereich **Microsoft Exchange** unter **Verwaltung mobiler Geräte** ein, und klicken Sie dann auf **Exchange-Verbindung einrichten**.

4.  Klicken Sie auf der Seite **Exchange-Verbindung einrichten** auf **Lokalen Connector herunterladen**.

5.  Die Software für den lokalen Connector ist in einem komprimierten Ordner (ZIP-Archiv) enthalten, der geöffnet oder gespeichert werden kann. Klicken Sie im Dialogfeld **Dateidownload** auf **Speichern**, um den komprimierten Ordner an einem sicheren Speicherort zu speichern.

> [!IMPORTANT]
> Sie dürfen die extrahierten Dateien weder umbenennen noch verschieben, da sonst die Installation der Software für den lokalen Connector fehlschlägt.

Führen Sie die folgenden Schritte aus, um [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] On-Premises Connector zu installieren.

> [!IMPORTANT]
> Der lokale Connector kann nur einmal pro [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Abonnement und nur auf einem Computer installiert werden. Wenn Sie versuchen, den lokalen Connector ein zweites Mal zu installieren, wird die erste Exchange-Verbindung ersetzt.

##### So installieren Sie den lokalen Connector

1.  Extrahieren Sie die Dateien in **Exchange_Connector_Setup.zip** an einem sicheren Ort.

2.  Nachdem die Dateien extrahiert wurden, doppelklicken Sie auf **Exchange_Connector_Setup.exe**, um den lokalen Connector zu installieren.

    > [!IMPORTANT]
    > Wenn der Speicherort nicht sicher ist, sollten Sie die Zertifikatdatei **WindowsIntune.accountcert** nach der Installation des lokalen Connectors unbedingt löschen.

> [!NOTE]
> Sie können nur eine Exchange-Verbindung pro [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konto einrichten. Wenn Sie versuchen, eine weitere Verbindung zu konfigurieren, wird die ursprüngliche Verbindung durch die neue ersetzt.

##### Lokalen Exchange-Connector konfigurieren

1.  Wählen Sie im Feld **Exchange-Server** Ihren Exchange-Serverumgebungstyp für Exchange unter Microsoft Office 365 aus. Zur Auswahl stehen **Lokaler Exchange-Server** und **Gehosteter Exchange-Server**.

2.  Geben Sie bei einem lokalen Exchange-Server entweder den Servernamen oder den vollqualifizierten Domänennamen des Exchange-Servers an, auf dem die Clientzugriffs-Serverrolle gehostet wird.

3.  Bei einem gehosteten Exchange-Server in Microsoft Office 365 geben Sie die Adresse des Exchange-Servers an.  So ermitteln Sie die URL des gehosteten Exchange-Servers:

    1.  Öffnen Sie die Outlook Web-App für Office 365.

    2.  Klicken Sie auf das Symbol „?“ oben links, und wählen Sie **Info** aus.

    3.  Suchen Sie den Wert **Externer POP-Server**.

4.  Geben Sie bei einem dedizierten, gehosteten Exchange-Server entweder den Servernamen oder den vollqualifizierten Domänennamen des dedizierten Exchange-Servers an, auf dem die Clientzugriffs-Serverrolle gehostet wird.

5.  Klicken Sie auf **Proxyserver**, um die Proxyservereinstellungen für Ihren gehosteten Exchange-Server anzugeben.

    1.  Wählen Sie **Beim Synchronisieren von Informationen für mobile Geräte einen Proxyserver verwenden** aus.

    2.  Geben Sie den **Proxyservernamen** und die für den Zugriff auf den Server zu verwendende **Portnummer** ein.

    3.  Ist für den Zugriff auf den Proxyserver die Angabe von Benutzeranmeldeinformationen erforderlich, wählen Sie **Mithilfe von Anmeldeinformationen eine Verbindung mit dem Proxyserver herstellen** aus, und geben Sie **Domäne\Benutzer** und das **Kennwort** ein.

    4.  Klicken Sie auf **OK**.

6.  Geben Sie die für die Verbindung zu Ihrem Exchange-Server erforderlichen Anmeldeinformationen an.

7.  Geben Sie die zum Senden von Benachrichtigungen an das Exchange-Postfach des Benutzers erforderlichen administrativen Anmeldeinformationen ein. Diese Benachrichtigungen sind über bedingte Zugriffsrichtlinien mit Intune konfigurierbar. Weitere Informationen zu diesen Richtlinien finden Sie unter [Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md).

    Stellen Sie sicher, dass die AutoErmittlungs- und Exchange-Webdienste auf dem Exchange-Clientzugriffsserver konfiguriert sind. Weitere Informationen dazu finden Sie unter [Clientzugriffsserver](https://technet.microsoft.com/library/dd298114.aspx).

8.  Geben Sie im Feld **Kennwort** das Kennwort für dieses Konto an, damit von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] auf Exchange Server zugegriffen werden kann.

9. Klicken Sie auf **Verbinden**.

    Die Einrichtung der Verbindung kann einige Minuten dauern.

    Bei der Konfiguration werden von [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] Ihre Proxyeinstellungen gespeichert, um den Zugriff auf das Internet zu ermöglichen. Wenn sich Ihre Proxyeinstellungen ändern, müssen Sie [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] neu konfigurieren, damit für [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] die aktualisierten Proxyeinstellungen verwendet werden.

Nach Einrichtung der Verbindung durch [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] werden mobile Geräte, die mit in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwalten Benutzern verbunden sind, automatisch synchronisiert und der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] hinzugefügt. Diese Synchronisation kann einige Zeit in Anspruch nehmen.

Wechseln Sie zur Anzeige des Status der Verbindung und des letzten erfolgreichen Synchronisationsversuchs in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] zum Arbeitsbereich **Verwaltung**, und klicken Sie dann unter **Verwaltung mobiler Geräte** auf **Exchange**.

> [!NOTE]
> Wenn Sie den lokalen Connector installiert haben und zu einem späteren Zeitpunkt die Exchange-Verbindung löschen, müssen Sie den lokalen Connector von dem Computer löschen, auf dem er installiert wurde.

## <a name="bkmk_S_S"></a>Konfigurieren von Intune Service to Service Connector für gehostetes Exchange
Verwenden Sie diesen Abschnitt, um [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] und gehostetes Exchange ohne lokale Infrastruktur zu verbinden.

### Anforderungen
Zur Vorbereitung einer Verbindung von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] mit Exchange Server müssen die folgenden Anforderungen erfüllt sein.

|Anforderungen|Weitere Informationen|
|-----------------|-------------------------|
|Festlegen der Autorität für die Verwaltung mobiler Geräte für [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|[Vorbereiten der Registrierung von Geräten in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)|
|Sicherstellen, dass die Hardwareanforderungen für On-Premises Connector erfüllt sind|[Anforderungen an Service to Service Connector](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_ServiceConnectorReqs)|
|Konfigurieren eines Benutzerkontos mit der Berechtigung zum Ausführen der designierten Liste von Windows PowerShell-Cmdlets|PowerShell-Cmdlets für Service to Service Connector (siehe unten)|

### <a name="Bkmk_PS_STS"></a>PowerShell-Cmdlets für Service to Service Connector
Sie müssen in Exchange Online ein Benutzerkonto erstellen, das von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Exchange Connector verwendet wird. Das Konto muss über die Berechtigung zum Ausführen der erforderlichen Windows PowerShell-Exchange-Cmdlets verfügen, die unten aufgeführt sind.

-   Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings

-   Get-MobileDeviceMailboxPolicy, Set-MobileDeviceMailboxPolicy, New-MobileDeviceMailboxPolicy, Remove-MobileDeviceMailboxPolicy

-   Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule

-   Get-MobileDeviceStatistics

-   Get-MobileDevice

-   Get-ActiveSyncDeviceClass

-   Get-Recipient

-   Clear-MobileDevice, Remove-MobileDevice

### Dienst für Service Connector einrichten

1.  Öffnen Sie die [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2.  Klicken Sie im Bereich für die Arbeitsbereichsverknüpfungen auf **Verwaltung**.

3.  Blenden Sie im Navigationsbereich **Microsoft Exchange** unter **Verwaltung mobiler Geräte** ein, und klicken Sie dann auf **Exchange-Verbindung einrichten**.

4.  Klicken Sie auf der Seite **Exchange-Verbindung einrichten** auf **Dienst für Service Connector einrichten**.

Der Dienst für Service Connector wird automatisch konfiguriert und mit Ihrer gehosteten Exchange-Umgebung synchronisiert.

## <a name="bkmk_val_ex"></a>Überprüfen der Exchange-Verbindung

-   Nachdem Sie [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] erfolgreich konfiguriert haben, klicken Sie in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] auf den Arbeitsbereich **Verwaltung**, klicken Sie unter **Verwaltung mobiler Geräte** auf **Microsoft Exchange**, und überprüfen Sie die unter **Exchange-Verbindungsinformationen** angezeigten Details.

-   Sie können auch die Uhrzeit und das Datum des letzten erfolgreichen Synchronisationsversuchs überprüfen.

## <a name="bkmk_EXCap"></a>Zurücksetzen mobiler Geräte, die mit Exchange verwaltet werden
In der folgenden Tabelle werden die Funktionen zum Abkoppeln/Zurücksetzen über Exchange ActiveSync beschrieben.

|Typ des Zurücksetzens|Windows 8.1 und Windows RT 8.1|Windows RT|Windows Phone 8|iOS|Android|
|-------------------------|----------------------------------|--------------|-------------------|-------|-----------|
|Vollständiges Zurücksetzen|E-Mail-Konto und zwischengespeicherte E-Mails werden entfernt.|E-Mail-Konto und zwischengespeicherte E-Mails werden entfernt.|Zurück auf Werkseinstellungen|Zurück auf Werkseinstellungen|Zurück auf Werkseinstellungen|
|Selektives Zurücksetzen/E-Mail|E-Mail-Konto wird entfernt|E-Mail-Konto wird entfernt|Nicht unterstützt.|Nicht unterstützt.|Nicht unterstützt.|
|Selektives Zurücksetzen/Richtlinien|Die Durchsetzung von Richtlinien wird entfernt, es werden jedoch keine Einstellungen geändert.|Die Durchsetzung von Richtlinien wird entfernt, es werden jedoch keine Einstellungen geändert.|Die Durchsetzung von Richtlinien wird entfernt, es werden jedoch keine Einstellungen geändert.|Die Durchsetzung von Richtlinien wird entfernt, es werden jedoch keine Einstellungen geändert.|Die Durchsetzung von Richtlinien wird entfernt, es werden jedoch keine Einstellungen geändert.|

## <a name="bkmk_pol"></a>Richtlinie für mobile Geräte, die mit Exchange verwaltet werden
Richtlinieneinstellungen können über die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole angewendet werden, siehe [Verwalten von Einstellungen und Features auf Ihren Geräten mit Microsoft Intune-Richtlinien](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md). Eine detaillierte Liste der Exchange ActiveSync-Richtlinieneinstellungen und -Funktionen, die von bestimmten mobilen Geräten unterstützt werden, finden Sie unter [Exchange ActiveSync Client Comparison Table (Vergleichstabelle der Exchange ActiveSync-Clients)](http://go.microsoft.com/fwlink/?LinkId=247270).

> [!NOTE]
> Beim Herstellen einer Verbindung zwischen [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] und einer Microsoft Exchange-Umgebung wird bei allen Benutzern, die über [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltet werden, die EAS-Richtlinie auf die aktuelle Standardrichtlinie auf dem Microsoft Exchange-Server zurückgesetzt, wenn keine spezifische Richtlinie in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] definiert ist.

## <a name="bkmk_acc"></a>Exchange-Zugriffsregeln für mobile Geräte
Mit den Exchange-Zugriffsregeln für mobile Geräte wird der Zugriff mobiler Geräte auf Exchange gesteuert. Diese Einstellung gilt für alle mobilen Geräte, auch solche, die nicht in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] registriert sind. Sie können zunächst eine **Standardregel** definieren, die für alle mobilen Geräte gilt, auf welche keine benutzerdefinierten Regeln angewendet werden. Die folgende Tabelle enthält die Zugriffsebenen, die von Exchange ActiveSync verwaltet werden:

|Zugriffsebene|Beschreibung|
|-----------------|----------------|
|**Zugriff auf Exchange für alle mobilen Geräte zulassen, sofern nicht durch eine benutzerdefinierte Regel anders festgelegt**|Mit der Zugriffsebene „Zulassen“ kann ein mobiles Gerät über Exchange ActiveSync synchronisiert werden, und es kann eine Verbindung mit dem Exchange-Server herstellen, um E-Mails abzurufen und Kalenderinformationen, Kontakte, Aufgaben und Notizen zu bearbeiten. Diese Synchronisierung wird nur beendet, wenn das Gerät nicht mehr der von Ihnen konfigurierten **Sicherheitsrichtlinie für mobiles Gerät** von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] entspricht oder der Benutzer oder das spezifische mobile Gerät vom Exchange-Administrator blockiert wird.|
|**Zugriff auf Exchange für alle mobilen Geräte blockieren, sofern nicht durch eine benutzerdefinierte Regel anders festgelegt**|Ein mobiles Gerät, das aufgrund einer von Ihnen konfigurierten Gerätezugriffseinstellung blockiert wird, erhält keinen Zugriff auf den Exchange-Server und empfängt den Fehler „HTTP 403 Verboten“. Der Benutzer erhält eine E-Mail-Nachricht vom Exchange-Server, in der er darüber informiert wird, dass das mobile Gerät nicht mehr auf sein Postfach zugreifen kann. Der Benutzer kann dann auf seinem blockierten mobilen Gerät keine E-Mail-Nachrichten mehr lesen. Sie können dieser Nachricht über die Aufgabe **Nachricht an Benutzer festlegen** angepassten Text hinzufügen, um den Benutzern, deren Geräte blockiert wurden, Anweisungen mitzuteilen.|
|**Alle mobilen Geräte unter Quarantäne stellen und später für jedes mobile Gerät im Einzelfall entscheiden, sofern nicht durch eine benutzerdefinierte Regel anders festgelegt**|Wenn ein mobiles Gerät unter Quarantäne gestellt wird, kann es weiterhin eine Verbindung zum Exchange-Server herstellen. Ihm wird jedoch nur ein beschränkter Zugriff auf die Daten gewährt. Der Benutzer des Geräts kann seinen eigenen Ordnern mit dem Kalender, Kontakten, Aufgaben und Notizen Inhalt hinzufügen, aber das Gerät kann keine Inhalte aus dem Postfach des Benutzers abrufen. Der Benutzer erhält nur eine E-Mail-Nachricht, in der er darüber informiert wird, dass das mobile Gerät unter Quarantäne gestellt wurde. Diese Nachricht wird vom Gerät empfangen und ist auch im Postfach des Benutzers vorhanden. Sie können dieser Nachricht über die Aufgabe **Nachricht an Benutzer festlegen** angepassten Text hinzufügen, um den Benutzern, deren Geräte unter Quarantäne gestellt wurden, Anweisungen mitzuteilen.|
Eine Zugriffsmethode enthält eine **Standardregel** und **Benutzerdefinierte Regeln** und gilt für alle mobilen Geräte, die mit Exchange verbunden sind. Die folgende Tabelle enthält einige Beispiele für Zugriffsmethoden.

|Zugriffsmethode|Beschreibung|
|-------------------|----------------|
|Liste „Zulassen“|Mit der Liste „Zulassen“ können Sie einer Liste bekannter Geräte Zugriff gewähren und den Zugriff für alle anderen Geräte blockieren. Hierzu müssen Sie benutzerdefinierte Regeln erstellen, sodass die gewünschten Geräte auf die Postfächer des Benutzers zugreifen können. Nachdem Sie eine solche Regel erstellt haben, müssen Sie in der Standardzugriffsregel festlegen, dass alle anderen Geräte blockiert oder unter Quarantäne gestellt werden. Zum Hinzufügen eines neuen Geräts zur Liste „Zulassen“ müssen Sie eine neue benutzerdefinierte Regel erstellen.|
|Liste „Blockieren“|Mit der Liste „Blockieren“ können Sie allen Geräten standardmäßig Zugriff gewähren, aber eine Gruppe von Geräten blockieren, die keinen Zugriff auf Ihr Unternehmen haben sollen. Sie erstellen die Liste „Blockieren“ mithilfe von benutzerdefinierten Regeln, durch die die Geräte blockiert werden, die nicht mit den Postfächern Ihres Unternehmens synchronisiert werden sollen. Die Standardzugriffsregel sollte so festgelegt werden, dass sie den Zugriff auf alle Geräte gewährt, die durch die bestehenden Regeln nicht explizit blockiert werden. Zum Hinzufügen eines neuen Geräts oder einer Gerätegruppe zur Liste „Blockieren“ müssen Sie eine neue benutzerdefinierte Regel erstellen.|
|Gemischtes Zulassen und Blockieren|Sie können nicht nur die Listen „Zulassen“ und „Blockieren“ erstellen, sondern auch neue mobile Geräte unter Quarantäne stellen, wenn sie ganz neu in das Unternehmen eingeführt und noch geprüft werden. Wenn Sie z. B. eine Liste „Blockieren“ für mobile Geräte erstellt haben, die nicht in Ihrem Unternehmen zugelassen sind, und eine Liste „Zulassen“ für mobile Geräte, die im Unternehmen zugelassen sind, können Sie in der Standardregel festlegen, dass Geräte unter Quarantäne gestellt werden sollen. Alle anderen Geräten werden dann automatisch unter Quarantäne gestellt, sodass Sie neue Geräte im Unternehmen erkennen und entscheiden können, ob sie der Liste „Zulassen“ oder der Liste „Blockieren“ hinzugefügt werden sollen.|
Im folgenden Verfahren wird das Erstellen einer benutzerdefinierten Regel beschrieben.

#### Erstellen einer Standardzugriffsregel

1.  Öffnen Sie die [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2.  Klicken Sie dazu im Bereich der Arbeitsbereichsverknüpfungen auf das Symbol **Richtlinie** und dann auf **Exchange-Zugriff für mobile Geräte**.

3.  Wählen Sie in der Liste **Standardregel** die Zugriffsregel aus, die Sie auf alle mobilen Geräte anwenden möchten, die nicht durch eine Regel oder persönliche Ausnahme abgedeckt werden. Klicken Sie auf **Speichern**.

Im folgenden Verfahren wird das Erstellen einer benutzerdefinierten Regel beschrieben.

#### Erstellen einer benutzerdefinierten Zugriffsregel

1.  Öffnen Sie die [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2.  Klicken Sie dazu im Bereich der Arbeitsbereichsverknüpfungen auf das Symbol **Richtlinie** und dann auf **Exchange-Zugriff für mobile Geräte**.

3.  Klicken Sie in der Liste **Benutzerdefinierte Regeln** auf **Regel hinzufügen**, und erstellen Sie eine benutzerdefinierte Regel. Klicken Sie auf **Speichern**.

## Siehe auch
[Vorbereiten der Registrierung von Geräten in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

