---
description: na
keywords: na
title: Plan for app deployment in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b770f4f-6d36-41e4-b535-514b46e29aaa
---
# Erste Schritte mit der Bereitstellung von Apps in Microsoft Intune
Bevor Sie in [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Apps verwalten und bereitstellen, informieren Sie sich anhand dieses Abschnitts über:

-   [Den Arbeitsbereich "Apps"](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_SoftwareWorkspace)

-   [Microsoft Intune Software Publisher](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_SoftwarePublisher)

-   [Anforderungen an das Betriebssystem](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_OSRequirements)

-   [Softwareinstallationstypen](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_Types)

-   [Allgemeiner Bereitstellungsprozess für Apps](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_SoftwareDistProcess)

-   [Grundlegendes zu App-Bereitstellungsaktionen](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_Depl)

## <a name="BKMK_SoftwareWorkspace"></a>Den Arbeitsbereich "Apps"
Der Arbeitsbereich **Apps** in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] enthält Informationen zu erkannten und verwalteten Apps. Die folgenden Seiten sind verfügbar:

|Seite mit dem Arbeitsbereich "Apps"|Details|
|---------------------------------------|-----------|
|**Übersicht**|Listet Warnungen zur App-Bereitstellung und zum aktuellen Status Ihres Cloudspeichers auf.|
|**Erkannte Software**|Zeigt die Softwareinventar-Daten, die [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] auf verwalteten Computern erkennt. Das Softwareinventar ist nur für Computer verfügbar. Daher werden Apps für verwaltete mobile Geräte von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nicht erkannt und nicht aufgelistet. Im Arbeitsbereich **Erkannte Software** können Sie die folgenden Aufgaben ausführen:<br /><br />-   Anzeigen von App-Eigenschaften<br />-   Hinzufügen von Lizenzverträgen für erkannte Software|
|**Apps**|Auf der Seite **Apps** werden die Apps, die Sie für Ihre verwalteten Computer und mobilen Geräte bereitstellen möchten, hochgeladen, bereitgestellt und fortlaufend verwaltet. Sie können folgende Aufgaben ausführen:<br /><br />-   Anzeigen und Ändern von App-Eigenschaften<br />-   Hinzufügen von Lizenzverträgen zu verwalteten Apps<br />-   Verwalten von App-Bereitstellungen<br />-   Hinzufügen neuer Apps<br />-   Bearbeiten der Eigenschaften verwalteter Apps<br />-   Löschen von Apps|

## <a name="BKMK_SoftwarePublisher"></a>Microsoft Intune Software Publisher
Der **Microsoft Intune-Softwareherausgeber** wird gestartet, wenn Sie in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] Apps hinzufügen oder ändern. Im Herausgeber wählen Sie einen Typ des Softwareinstallationsprogramms aus, von dem entweder Apps (Programme für Computer oder Apps für mobile Geräte) zum Speichern im [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Cloudspeicher hochgeladen oder Links zu einem Onlineshop bzw. zu Webanwendungen bereitgestellt werden.

### <a name="BKMK_PublisherRequirements"></a>Anforderungen des Microsoft Intune-Softwareherausgebers
Bevor Sie mit der Verwendung des [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Softwareherausgebers beginnen, müssen Sie die Vollversion von Microsoft .NET Framework 4.0 installieren. Nach der Installation von .NET Framework müssen Sie möglicherweise den Computer neu starten, damit der [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Softwareherausgeber ordnungsgemäß geöffnet wird. Details finden Sie unter [Microsoft .NET Framework 4 (Webinstaller)](http://www.microsoft.com/download/details.aspx?id=17851).

### <a name="BKMK_CloudStorage"></a>Cloudspeicheranforderungen
Bereitgestellte Apps müssen als Paket in den Cloudspeicher von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] hochgeladen werden. Vergewissern Sie sich vor dem Bereitstellen von Apps, dass genügend Speicherplatz zum Hochladen der App verfügbar ist. Ein Testabonnement von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] umfasst 2 GB Cloudspeicherplatz zur Speicherung verwalteter Apps und Updates. Das kostenpflichtige Abonnement umfasst 20 GB. In diesem Fall besteht zudem die Möglichkeit, mithilfe des [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Extra Storage-Add-Ons weiteren Speicherplatz in Erweiterungsschritten von 1 GB hinzuzukaufen. Die folgenden Regeln gelten für den Kauf zusätzlichen Cloudspeicherplatzes für [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

-   Es ist nicht möglich, während des Zeitraums einer [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Vorabversion oder -Testversion zusätzlichen Speicher zu erwerben.

-   Sie benötigen ein aktives kostenpflichtiges Abonnement, um zusätzlichen Speicherplatz zu kaufen.

-   Nur Rechnungsadministratoren oder globale Administratoren für Ihren Microsoft Online Service können zusätzlichen Speicher über das [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Kontenportal erwerben. Um diese Administratoren hinzuzufügen, zu löschen oder zu verwalten, müssen Sie ein globaler Administrator sein und beim [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Kontenportal angemeldet sein.

-   Volumenlizenzkunden, die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] oder das [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Add-On über ein Enterprise Agreement gekauft haben, erhalten Preisinformationen und zusätzlichen Speicherplatz beim zuständigen Microsoft-Kundenbetreuer oder Microsoft-Partner.

##### So kaufen Sie zusätzlichen Speicher

1.  Klicken Sie im [Microsoft Intune-Kontenportal](https://account.manage.microsoft.com) im linken Bereich unter **Abonnements** auf **Verwalten**.

2.  Klicken Sie auf der Seite **Abrechnungs- und Abonnementverwaltung** auf das [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Abonnement, für das Sie zusätzlichen Speicher erwerben möchten.

3.  Klicken Sie auf der Seite **Abonnementdetails** unter **Optionale Add-Ons** auf **Weitere hinzufügen**.

4.  Geben Sie auf der Seite **Anzahl der Lizenzen auswählen** unter **Optionale Add-Ons** die Menge an zusätzlichem Speicher in GB ein, die Sie für das Extra Storage-Add-On von Microsoft Intune kaufen möchten. Wenn Sie beispielsweise gegenwärtig über 20 GB verfügen und weitere 10 GB hinzufügen möchten, geben Sie "10" ein.

5.  Prüfen Sie auf der Seite **Wichtige Informationen prüfen** die Auftragsinformationen, und klicken Sie dann auf **Bestellung aufgeben**.

6.  Die Seite **Auftragsbestätigung** wird geöffnet, die die Auftragsdetails enthält. Klicken Sie auf **Fertig stellen**, um den Vorgang abzuschließen.

## <a name="BKMK_OSRequirements"></a>Anforderungen an das Betriebssystem
Auf mobilen Geräten und Computern muss zum Installieren von Apps, die unter Verwendung von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] bereitgestellt werden, ein unterstütztes Betriebssystem ausgeführt werden.

**Mobile Geräte**

Eine vollständige Liste der unterstützten Betriebssysteme für mobile Geräte finden Sie unter [Verwaltungsfunktionen für mobile Geräte in Microsoft Intune](../Topic/Mobile_device_management_capabilities_in_Microsoft_Intune.md).

**Computer**

Eine vollständige Liste unterstützter Betriebssysteme für verwaltete Computer finden Sie unter [Funktionen für die Windows-PC-Verwaltung in Microsoft Intune](../Topic/Windows_PC_management_capabilities_in_Microsoft_Intune.md).

## <a name="BKMK_Types"></a>Softwareinstallationstypen
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ermöglicht das Bereitstellen der folgenden Arten von Softwareinstallation:

### <a name="BKMK_SoftwareInstallers"></a>Softwareinstallationsprogramm
Verwenden Sie den Installationstyp **Software Installer** zu folgenden Zwecken:

-   Hochladen eines signierten App-Pakets in den Microsoft Intune-Cloudspeicher und Bereitstellen der App für Benutzer über das [!INCLUDE[wit_iwportal_1](../Token/wit_iwportal_1_md.md)].

-   Hochladen von Apps, die auf Computern bereitgestellt wird, auf denen der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Computerclient ausgeführt wird.

-   Installieren von Apps auf verwalteten mobilen Geräten über eine Installationsdatei, unter Umgehung des App Store (als Sideloading bezeichnet).

Verwenden Sie die folgende Tabelle, um die verschiedenen Dateitypen des Softwareinstallationsprogramms zu verstehen:

|||
|-|-|
|**Typ des Softwareinstallationsprogramms**|**Anforderungen**|
|**Windows Installer (&#42;.exe, &#42;.msi)**|-   Die Windows Installer-Dateien müssen die automatische Installation unterstützen, d. h., es ist kein Benutzereingriff erforderlich. Wenn für Ihre App ein anderer Setupdateityp verwendet wird oder während des Setups ein Eingreifen des Benutzers erforderlich ist, kann die App nicht mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] installiert werden.<br />    Suchen Sie in Ihrer App-Dokumentation nach relevanten Befehlszeilenoptionen wie "/q", mit denen eine Hintergrundinstallation der App auf den verwalteten Computern erzwungen wird.<br />-   Wenn zusätzliche Dateien und Ordner für das Setupprogramm der App erforderlich sind, müssen sie an dem für die Setupdateien angegebenen Speicherort verfügbar sein.<br />-   In den meisten Fällen müssen bei Windows Installer-Dateien (MSI) und Windows Installer Patch-Dateien (MSP-Dateien) keine Befehlszeilenargumente von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] installiert werden. Überprüfen Sie die Dokumentation Ihrer App. Sind Befehlszeilenargumente erforderlich, müssen sie in "Name=Wert"-Paaren (z. B. TRANSFORMS=custom_transform.mst) eingegeben werden.|
|**App-Paket für Android (APK-Datei)**|Das App-Paket für Android ist als Typ des Softwareinstallationsprogramms erst dann verfügbar, wenn Sie [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] als Autorität für die Verwaltung mobiler Geräte festlegen.<br /><br />Details finden Sie unter [Einrichten der Android-Verwaltung mit Microsoft Intune](../Topic/Set_up_Android_management_with_Microsoft_Intune.md).|
|**App-Paket für iOS (IPA-Datei)**|-   Zum Bereitstellen von iOS-Apps müssen Sie über ein gültiges IPA-Paket verfügen.<br />-   Das IPA-Paket muss von Apple signiert sein, und das im Bereitstellungsprofil angegebene Ablaufdatum darf noch nicht erreicht sein.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] kann iOS-Anwendungen mit Unternehmenszertifikat verteilen. Es werden nicht alle Apps mit Entwicklerzertifikat von Apple unterstützt.<br />-   Ihr Unternehmen muss für das iOS Developer Enterprise Program registriert sein.<br />-   Stellen Sie sicher, dass der Zugriff auf die iOS-Bereitstellungs- und -Zertifizierungswebsites durch die Firewall Ihrer Organisation zugelassen wird.<br /><br />Details finden Sie unter [Einrichten der iOS-Verwaltung mit Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|
|**Windows Phone-App-Paket (&#42;.xap, &#42;.appx, &#42;.appxbundle)**|Bevor Sie ein Windows Phone 8- oder Windows Phone 8.1-App-Paket verteilen können, müssen Sie [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] als Autorität für die Verwaltung mobiler Geräte festlegen, Benutzer einrichten und ein Codesignaturzertifikat für mobile Geräte erwerben. Details finden Sie unter [Einrichten der Windows Phone-Verwaltung mit Microsoft Intune](../Topic/Set_up_Windows_Phone_management_with_Microsoft_Intune.md).|
|**Windows-App-Paket (&#42;.appx, &#42;.appxbundle)**|Das Windows-Appx-Paket für Windows RT- und registrierte Windows 8.1-Geräte ist erst verfügbar, wenn Sie [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] als Autorität für die Verwaltung mobiler Geräte festlegen, Benutzer bereitstellen sowie ein Codesignaturzertifikat und Sideload-Produktaktivierungsschlüssel erwerben. Details finden Sie unter [Einrichten der Windows Phone-Verwaltung mit Microsoft Intune](../Topic/Set_up_Windows_Phone_management_with_Microsoft_Intune.md).<br /><br />Weitere Informationen zur Installation von Branchen-UWP-Apps (Universelle Windows-Plattform) mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] finden Sie weiter unten.|
|**Windows Installer über MDM (&#42;.msi)**|Mit diesem Installationstyp können Sie Windows Installer-basierte Apps auf registrierten Geräten unter Windows 10 erstellen und bereitstellen.<br /><br />Folgendes muss berücksichtigt werden, wenn Sie diese Art Installationsprogramm verwenden:<br /><br />-   Sie können nur eine einzelne Datei mit der Erweiterung **MSI** hochladen.<br />-   Produktcode und Produktversion der Datei werden zur Erkennung der App verwendet.<br />-   Es wird das standardmäßige Verhalten bei Neustart der App verwendet.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] steuert dies nicht.<br />-   Pro Benutzer definierte MSI-Pakete werden für einen einzigen Benutzer installiert.<br />-   Pro Gerät definierte MSI-Pakete werden für alle Benutzer des Geräts installiert.<br />-   MSI-Pakete im Dualmodus werden zurzeit nur für alle Benutzer des Geräts installiert.<br />-   App-Updates werden nur unterstützt, wenn jede Version den gleichen MSI-Produktcode aufweist.|

#### Unterstützung für UWP-Apps (Universelle Windows-Plattform)
Windows 10-Geräte erfordern keinen Sideload-Schlüssel für die Installation von Branchen-Apps. Allerdings muss der Registrierungsschlüssel **HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\Appx\AllowAllTrustedApps** einen Wert von **1** haben, um das Querladen zu aktivieren.

Wenn dieser Registrierungsschlüssel nicht konfiguriert ist, legt [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] diesen Wert automatisch auf **1** fest, wenn Sie zum ersten Mal eine App auf dem Gerät bereitstellen. Wenn Sie diesen Wert auf **0** festgelegt haben, kann [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] den Wert nicht automatisch ändern, und die Bereitstellung von Branchen-Apps schlägt fehl.

Branchen-UWP-Apps müssen mit einem codesignierten Zertifikat signiert sein, das auf jedem Gerät, auf dem die App bereitgestellt ist, als vertrauenswürdig eingestuft ist. Sie können Zertifikate aus einer internen PKI-Infrastruktur verwenden oder ein Zertifikat von einer öffentlichen Drittanbieter-Stammzertifizierungsstelle, das auf dem Gerät installiert ist.

Auf Windows 10 Mobile-Geräten können Sie ein nicht von Symantec stammendes Codesignaturzertifikat zum Signieren universeller **APPX**-Apps verwenden. Für **XAP** -apps sowie für **APPX**-Pakete, die für Windows Phone 8.1 erstellt wurden, die Sie auf Windows 10 Mobile-Geräten installieren möchten, müssen Sie ein Codesignaturzertifikat von Symantec verwenden.

### <a name="BKMK_ExternalLinks"></a>Externer Link
Verwenden Sie den Installationstyp **Externer Link**, wenn Sie über Folgendes verfügen:

-   Eine **URL**, mit der Benutzer eine App aus dem Onlineshop herunterladen können. Dieser Installationstyp wird durch die folgenden Geräteplattformen unterstützt:

    -   Windows 8 und höher

    -   Windows RT

    -   Windows Phone 8 und höher

    -   iOS

    -   Android-Geräte

-   Einen **Link** zu einer webbasierten App, die im Webbrowser ausgeführt wird.

    Dieser Installationstyp ist für alle von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] unterstützten Geräte verfügbar.

Externe Links werden den Benutzern über das [!INCLUDE[wit_iwportal_1](../Token/wit_iwportal_1_md.md)] zur Verfügung gestellt.

### Verwaltete iOS-App aus dem App Store
Verwenden Sie den Installationstyp **Verwaltete iOS-App aus dem App Store** zum Verwalten und Bereitstellen von iOS-Apps, die kostenlos im App Store erhältlich sind. Sie können diesen Installationsprogrammtyp als erforderliche Installationskomponente bereitstellen, um ihn auf verwalteten Geräten obligatorisch zu machen (wodurch er auch vom Mobilportal installiert werden kann), oder als verfügbar bereitstellen, damit Benutzer ihn vom Mobilportal herunterladen können. Sie können auch Richtlinien für die Verwaltung mobiler Anwendungen mit kompatiblen Apps verknüpfen und ihren Status in der Administratorkonsole überprüfen. Verwaltete iOS-Apps werden nicht in Ihrem [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Cloudspeicher gespeichert.

## <a name="BKMK_SoftwareDistProcess"></a>Allgemeiner Bereitstellungsprozess für Apps
Dieser Abschnitt enthält eine Übersicht über den App-Bereitstellungsprozess in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

|Schritt|Weitere Informationen|
|-----------|-------------------------|
|Stellen Sie sicher, dass die bereitzustellende App von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] unterstützt wird.|[Erste Schritte mit der Bereitstellung von Apps in Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md)|
|Erstellen Sie Gruppen von Benutzern oder Geräten, auf denen Sie die App bereitstellen können.|[Verwenden von Gruppen zum Verwalten von Benutzern und Geräten in Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md)|
|Veröffentlichen Sie die App im [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Cloudspeicher.|[Publish mobile device apps to Microsoft Intune cloud storage](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md#BKMK_PublishSoftware)<br /><br />[Publish computer apps to Microsoft Intune cloud storage](../Topic/Deploy_apps_to_Windows_PCs_in_Microsoft_Intune.md#BKMK_PublishSoftware)|
|Stellen Sie die App mit der erforderlichen Bereitstellungsaktion auf mobilen Geräten oder Computern bereit.|[Bereitstellen von Apps für mobile Geräte in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)<br /><br />[Bereitstellen von Apps auf Windows-PCs in Microsoft Intune](../Topic/Deploy_apps_to_Windows_PCs_in_Microsoft_Intune.md)|
|Überwachen der App-Bereitstellung|[Monitor mobile device apps](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md#BKMK_MonitorSoftware)<br /><br />[Monitor computer apps](../Topic/Deploy_apps_to_Windows_PCs_in_Microsoft_Intune.md#BKMK_MonitorSoftware)|

## <a name="BKMK_Depl"></a>Grundlegendes zu App-Bereitstellungsaktionen
Wenn Sie Apps bereitstellen, können Sie eine der folgenden Bereitstellungsaktionen auswählen:

-   **Erforderliche Installation**: Die App wird auf dem Gerät installiert, ohne dass ein Benutzereingriff erforderlich ist.

    > [!NOTE]
    > Bei iOS-Geräten, die nicht betreut werden, muss der Benutzer das App-Angebot vor der Installation akzeptieren.  Weitere Informationen zur Verwendung von [betreuten Geräten](http://support.apple.com/en-is/HT202837) in Microsoft Intune finden Sie unter [Einstellungen für iOS-Konfigurationsrichtlinien in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md).
    > 
    > Sie können keine neuen App-Bereitstellungen für iOS-Geräte mehr erstellen, auf denen ein älteres Betriebssystem als iOS 7.1 ausgeführt wird. Alle vorhandenen App-Bereitstellungen auf Geräten, auf denen ein älteres Betriebssystem als iOS 7.1 ausgeführt wird, funktionieren weiterhin und werden auch weiterhin von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltet.

    > [!NOTE]
    > Bei Android-Geräten muss der Benutzer das App-Angebot vor der Installation akzeptieren.

-   **Verfügbare Installation**: Die App wird im Unternehmensportal angezeigt, und Endbenutzer können sie bei Bedarf installieren.

-   **Deinstallieren**: Die App wird vom Gerät deinstalliert.

-   **Nicht verfügbar**: Die App wird nicht im Unternehmensportal angezeigt und wird auf keinem Gerät installiert.

|Plattform|Erforderliche Installation|Verfügbare Installation|Deinstallieren|Nicht zutreffend|
|-------------|------------------------------|---------------------------|------------------|--------------------|
|Windows-App-Paket (für eine Benutzergruppe bereitgestellt)|Ja|Ja|Ja|Ja|
|Windows-App-Paket (auf einer Gerätegruppe bereitgestellt)|Ja|Nein|Ja|Ja|
|App-Paket für mobile Geräte (für eine Benutzergruppe bereitgestellt)|Ja|Ja|Ja|Ja|
|App-Paket für mobile Geräte (auf einer Gerätegruppe bereitgestellt)|Ja|Nein|Ja|Ja|
|Windows Installer (für eine Benutzergruppe bereitgestellt)|Nein|Ja|Nein|Ja|
|Windows Installer (auf einer Gerätegruppe bereitgestellt)|Ja|Nein|Ja|Ja|
|Externer Link (für eine Benutzergruppe bereitgestellt)|Nein|Ja|Nein|Ja|
|Externer Link (auf einer Gerätegruppe bereitgestellt)|Nein|Nein|Nein|Nein|
|Verwaltete iOS-App aus dem App Store (für eine Benutzergruppe bereitgestellt)|Ja|Ja|Ja|Ja|
|Verwaltete iOS-App aus dem App Store (auf einer Gerätegruppe bereitgestellt)|Ja|Nein|Ja|Ja|
Wenn zwei Bereitstellungen mit der gleichen Bereitstellungsaktion von einem Gerät empfangen werden, gelten die folgenden Regeln:

-   Bereitstellungen auf einer Gerätegruppe haben Vorrang vor Bereitstellung für eine Benutzergruppe. Wenn jedoch eine App für eine Benutzergruppe mit der Bereitstellungsaktion **Verfügbar** bereitgestellt wird und dieselbe App auf einer Gerätegruppe mit der Bereitstellungsaktion **Nicht verfügbar** bereitgestellt wird, wird die App im Unternehmensportal Benutzern zur Installation zur Verfügung gestellt.

-   Die Absicht des IT-Administrators hat Vorrang vor dem Wunsch des Endbenutzers.

-   Eine Installationsaktion hat Vorrang vor einer Deinstallationsaktion.

-   Wenn eine erforderliche Installation und eine verfügbare Installation von einem Gerät empfangen werden, werden die Aktionen zusammengefasst (die App ist erforderlich und verfügbar).

## Siehe auch
[Bereitstellen und Konfigurieren von Apps mit Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)

