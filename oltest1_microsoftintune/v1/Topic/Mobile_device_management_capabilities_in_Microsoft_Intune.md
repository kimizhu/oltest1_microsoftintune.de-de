---
description: na
keywords: na
title: Mobile device management capabilities in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f23b3ee7-78da-4e53-9fc2-78e58401bcf9
---
# Verwaltungsfunktionen f&#252;r mobile Ger&#228;te in Microsoft Intune
Intune unterstützt die Verwaltung von iOS-, Android- und Windows Phone-Mobilgeräten. Darüber hinaus wird die Verwaltung von Computern mit Windows RT, Windows und Mac OS X als Mobilgeräte unterstützt. Benutzer verwenden ein *Unternehmensportal*, um Apps zu installieren, Geräte zu registrieren und zu entfernen sowie die Kontaktaufnahme mit der IT-Abteilung oder dem Helpdesk zu erleichtern. Um Mobilgeräte zu registrieren, müssen Sie [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] als Ihre *Autorität für Mobilgeräte* festlegen und dann die Infrastruktur für die Unterstützung der Plattformen konfigurieren, die Sie verwalten möchten. Dies erfordert das Einrichten einer Vertrauensstellung mit dem Gerät.

## <a name="BKMK_MobileDeviceReqs"></a>Unterstützte Mobilgeräte
Die Anforderungen beim Verwalten eines mobilen Geräts und die Verwaltungsstufe sind davon abhängig, ob das Gerät direkt oder mithilfe von Exchange ActiveSync verwaltet wird:

-   **Direkte Verwaltung**: Verschiedene Arten von mobilen Geräten haben unterschiedliche Anforderungen an die direkte Verwaltung. Beispielsweise ist zum Verwalten von iOS-Geräten ein Apple Push Notification Service-Zertifikat erforderlich, und zum Verwalten von Apps für [!INCLUDE[winblue_winrt_2](../Token/winblue_winrt_2_md.md)]-Geräte benötigen Sie Sideload-Schlüssel und ein Codesignaturzertifikat.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] kann die folgenden Geräte in die Verwaltung mobiler Geräte einbeziehen:

    -   Apple iOS 7.1 und höher

        > [!NOTE]
        > Bereits registrierte iOS 6.0-Geräte bleiben registriert, auf neuen Geräten muss jedoch iOS 7.1 oder höher ausgeführt werden, um diese Geräte für Intune registrieren zu können.

    -   Google Android 4.0 und höher (einschließlich Samsung KNOX)

    -   Windows Phone 8.0 und höher

    -   Windows RT und Windows 8.1 RT

    -   Computer mit Windows 8.1 und höher (als Mobilgeräte verwaltet, siehe [Funktionen für die Windows-PC-Verwaltung in Microsoft Intune](../Topic/Windows_PC_management_capabilities_in_Microsoft_Intune.md))

    -   Mac OS X 10.9 und höher

    Bevor Sie Mobilgeräte direkt verwalten können, ist das [Festlegen von Microsoft Intune als Autorität für die Verwaltung mobiler Geräte](../Topic/Set_mobile_device_management_authority_and_configure_Microsoft_Intune.md) erforderlich.

-   **Exchange ActiveSync**: Zum Verwalten von Geräten mithilfe von Exchange ActiveSync ist das Installieren von On-Premises Connector oder die Verwendung des integrierten Service to Service Connector erforderlich, um eine Verbindung mit Exchange Server herzustellen.

    Weitere Informationen zu den Hardware- und Softwareanforderungen zur Installation von On-Premise Connector finden Sie unter [Anforderungen für On-Premises Connector](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_ExchanceConnectorReqs).

    Informationen zum Verwenden von On-Premises Connector oder Service to Service Connector mit Exchange finden Sie unter [Verwaltung mobiler Geräte mit Exchange ActiveSync und Microsoft Intune](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md).

## Features für die Verwaltung von Mobilgeräten
Intune unterstützt die Verwaltung von iOS-, Android- und Windows Phone-Mobilgeräten. Darüber hinaus wird die Verwaltung von Computern mit Windows RT und Windows als Mobilgeräte unterstützt.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] kann auch die Geräte der Benutzer verwalten (was als "Bring your own device" bzw. BYOD bezeichnet wird). Es dient auch zum Verwalten von Geräten im Besitz des Unternehmens, z. B. in Szenarien, in denen das Unternehmen eine Liste mit Geräten anbietet, aus denen die Benutzer wählen können ("Choose your own device" oder CYOD).

Sie können Geräte registrieren, die die Anforderungen Ihrer Organisation erfüllen:

|Registrierungstyp|BYOD|CYOD|Gemeinsam genutzte Geräte mit Managerkonto|Gemeinsam genutzte Geräte ohne Benutzerkonto|
|---------------------|--------|--------|----------------------------------------------|------------------------------------------------|
|**Beschreibung**|Persönliches, mit Microsoft Intune registriertes Gerät|Firmeneigenes Gerät für einzelnen Benutzer|Firmeneigenes Gerät, das über ein von vielen Benutzern gemeinsam genutztes Managerkonto verwaltet wird|Firmeneigenes, benutzerunabhängiges Gerät, das von vielen Benutzern verwendet wird|
|**Benutzer des Geräts**|Besitzer|Zugewiesener Benutzer|Kein benutzerspezifisches Konto|Kein bestimmter Benutzer|
|**Registriert von**|Besitzer|Administrator|Geräte-Manager|Beliebig|
|**Aufhebung der Registrierung durch**|Besitzer oder Administrator|Administrator|Administrator|Administrator|
|**Berechtigung zum Zurücksetzen**|Besitzer oder Administrator|Administrator|Administrator|Administrator|
Um Mobilgeräte zu registrieren, müssen Sie [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] als Ihre *Autorität für Mobilgeräte* festlegen und dann die Infrastruktur für die Unterstützung der Plattformen konfigurieren, die Sie verwalten möchten. Dies erfordert das Einrichten einer Vertrauensstellung mit dem Gerät.

Verwaltung, Bestandserfassung, Bereitstellung und Außerbetriebnahme von Geräten und Apps erfolgen über die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungskonsole. Benutzer erhalten Zugriff auf das Unternehmensportal, das ihnen ermöglicht, Apps zu installieren, Geräte zu registrieren und zu entfernen und die Kontaktaufnahme mit der IT-Abteilung oder dem Helpdesk erleichtert.

Die **Verwaltungsfunktionen für Mobilgeräte** unterscheiden sich je nach Mobilgerätplattform. Doch alle Plattformen unterstützen Folgendes:

-   **Zertifikat-, E-Mail-, VPN- und WLAN-Profile.** Sie können Zertifikatprofile für Mobilgeräte und auch E-Mail-, VPN- und WLAN-Profile bereitstellen. Weitere Informationen finden Sie unter [Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md).

-   **Verwalten firmeneigener iOS-Geräte.** Sie können Geräte für die Registrierung einrichten und Sie dann an bestimmte Benutzer verteilen, oder Sie können Geräte so registrieren, dass sie von mehreren Benutzern gemeinsam genutzt werden können. Weitere Informationen finden Sie unter [Einrichten der iOS-Verwaltung mit Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).

-   **Verwaltung von mobilen Anwendungen.** Verwaltete mobile Anwendungen können so konfiguriert werden, dass bestimmte App-Vorgänge eingeschränkt werden, wie z. B. Kopieren und Einfügen, damit die Daten des Unternehmens geschützt werden. Außerdem können Sie den verwalteten Browser verwenden, um die Websites zu steuern, die Benutzer besuchen können. Weitere Informationen hierzu finden Sie unter [Schützen von Daten mithilfe der Verwaltungsrichtlinien für mobile Anwendungen mit Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) und [Verwalten des Internetzugriffs mittels Richtlinien für verwaltete Browser mit Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md).

-   **Bedingter Zugriff.** Verwenden Sie die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinien für bedingten Zugriff, um den Zugriff auf das lokale Microsoft Exchange-E-Mail-System von Mobilgeräten aus zu steuern, selbst wenn das Gerät nicht von Intune verwaltet wird. Weitere Informationen finden Sie unter [Verwalten des Zugriffs auf E-Mail und SharePoint mit Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

-   Die **Kennwortverwaltung** unterscheidet sich zwar bei den Mobilgerätplattformen, doch gestatten Ihnen alle Plattformen das Anfordern eines Kennworts, das Beschränken der Anzahl misslungener Anmeldeversuche, das Begrenzen des Zeitraums bis zur Sperrung des Bildschirms, das Festlegen eines Zeitraums für den Kennwortablauf und das Unterbinden der erneuten Verwendung zuvor bereits verwendeter Kennwörter.

-   **Anwendungseinstellungen.** Sie können Browser- und auch Anwendungseinstellungen steuern und so beispielsweise festlegen, ob App Stores auf Mobilgeräten genutzt werden dürfen oder nicht.

-   **Gerätefunktionen, Mobilfunk und Sprache.** Sie können die Verwendung einer Kamera zulassen oder unterbinden, die Roamingeinstellungen steuern und iOS-Funktionen wie den Sprachassistenten oder die Sprachwahl aktivieren oder deaktivieren.

-   **Zurücksetzen von Passcodes und Geräte sperren, selektiv zurücksetzen oder außer Betrieb nehmen.** Sie können Passcodes zurücksetzen, wenn Benutzer nicht mehr auf ihr Gerät zugreifen können, und verlorene oder gestohlene Geräte sperren oder alle darauf vorhandenen Daten zurücksetzen.

## Gerätesicherheit und Konfiguration

|Funktion|Details|Weitere Informationen|
|------------|-----------|-------------------------|
|Konfigurationsrichtlinien|Mit Konfigurationsrichtlinien für mobile Geräte können Sie viele Einstellungen und Features auf mobilen Geräten in Ihrer Organisation verwalten.|[Einstellungen für iOS-Konfigurationsrichtlinien in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md)<br /><br />[Einstellungen für Android-Konfigurationsrichtlinien in Microsoft Intune](../Topic/Android_configuration_policy_settings_in_Microsoft_Intune.md)<br /><br />[Einstellungen für Windows-Konfigurationsrichtlinien in Microsoft Intune](../Topic/Windows_configuration_policy_settings_in_Microsoft_Intune.md)<br /><br />[Einstellungen für Windows Phone-Konfigurationsrichtlinien in Microsoft Intune](../Topic/Windows_Phone_configuration_policy_settings_in_Microsoft_Intune.md)<br /><br />[Einstellungen für Exchange ActiveSync-Richtlinien in Microsoft Intune](../Topic/Exchange_ActiveSync_policy_settings_in_Microsoft_Intune.md)<br /><br />[Sicherheitsrichtlinieneinstellungen für mobile Geräte in Microsoft Intune](../Topic/Mobile_device_security_policy_settings_in_Microsoft_Intune.md)|
|Benutzerdefinierte Richtlinien|Verwenden Sie benutzerdefinierte Richtlinien, wenn Konfigurationsrichtlinien nicht die Einstellung enthalten, die Sie benötigen. Bei iOS-Geräten können Sie die Einstellungen importieren, die Sie aus dem Apple Configurator Tool exportiert haben. Bei anderen Geräten können Sie OMA-URI-Einstellungen verwenden, um Einstellungen und Features auf dem Gerät zu konfigurieren.|[Benutzerdefinierte iOS-Richtlinieneinstellungen in Microsoft Intune](../Topic/iOS_custom_policy_settings_in_Microsoft_Intune.md)<br /><br />[Benutzerdefinierte Android-Richtlinieneinstellungen in Microsoft Intune](../Topic/Android_custom_policy_settings_in_Microsoft_Intune.md)<br /><br />[Benutzerdefinierte Windows Phone-Richtlinieneinstellungen in Microsoft Intune](../Topic/Windows_Phone_custom_policy_settings_in_Microsoft_Intune.md)<br /><br />[Benutzerdefinierte Windows 10-Richtlinieneinstellungen in Microsoft Intune](../Topic/Windows_10_custom_policy_settings_in_Microsoft_Intune.md)|
|Remotezurücksetzen, Remotesperre und Kennungsrückstellung|Löschen Sie vertrauliche Daten, wenn ein Gerät verloren geht oder gestohlen wird. Beispielsweise können Sie das Gerät remote sperren, die Werkseinstellungen wiederherstellen oder nur Unternehmensdaten zurücksetzen.|[Schützen Ihrer Daten mit Remotezurücksetzen, Remotesperre und Kennungszurücksetzung in Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md)|
|Kioskmodus|Hiermit können Sie bestimmte Features von mobilen Geräten sperren, z. B. die Bildschirmaufnahme und den Netzschalter. Außerdem können Sie Geräte auf die Ausführung einer einzigen, von Ihnen angegebenen App beschränken.|[Einstellungen für iOS-Konfigurationsrichtlinien in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md)|

## App-Verwaltung

|Funktion|Details|Weitere Informationen|
|------------|-----------|-------------------------|
|App-Bereitstellung und -Verwaltung|Bietet eine Reihe von Tools zum Verwalten von mobilen Apps während deren Lebenszyklus, einschließlich der App-Bereitstellung von Installationsdateien und App Stores sowie eine detaillierte Überwachung des Status der App und App-Entfernung.|[Bereitstellen von Apps für mobile Geräte in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)|
|Kompatible und nicht kompatible Anwendungen|Damit können Sie Listen der kompatiblen Apps (die Benutzer installieren dürfen) und nicht kompatiblen Apps (die nicht von Benutzern installiert werden dürfen) angeben.|[Einstellungen für iOS-Konfigurationsrichtlinien in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md)|
|Mobile Anwendungsverwaltung|Konfigurieren Sie Einschränkungen für Apps mithilfe einer Richtlinie zur mobilen Anwendungsverwaltung. Dadurch können Sie die Sicherheit Ihrer Unternehmensdaten erhöhen, indem Sie Vorgänge wie das Kopieren und Einfügen, die externe Sicherung von Daten und die Übertragung von Daten zwischen Apps einschränken.|[Schützen von Daten mithilfe der Verwaltungsrichtlinien für mobile Anwendungen mit Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md)<br /><br />[Vorbereiten von iOS-Apps für die Verwaltung mobiler Anwendungen mit dem Microsoft Intune App Wrapper-Tool](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md)<br /><br />[Vorbereiten von Android-Apps für die Verwaltung von mobilen Anwendungen mit dem Microsoft Intune App Wrapper-Tool](../Topic/Prepare_Android_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md)<br /><br />[Microsoft-Apps zur Verwendung mit den Microsoft Intune-Verwaltungsrichtlinien für mobile Anwendungen](../Topic/Microsoft_apps_you_can_use_with_Microsoft_Intune_mobile_application_management_policies.md)|
|Managed Browser|Nachdem Sie den Managed Browser für Ihre Benutzer bereitgestellt haben, können Sie mithilfe einer Richtlinie für Managed Browser steuern, welche Websites die Benutzer besuchen dürfen. Darüber hinaus können Sie Richtlinien zur mobilen Anwendungsverwaltung auf den Managed Browser anwenden.|[Verwalten des Internetzugriffs mittels Richtlinien für verwaltete Browser mit Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md)|

## Zugriff auf Unternehmensressourcen

|Funktion|Details|Weitere Informationen|
|------------|-----------|-------------------------|
|Zertifikatprofile|Erstellt und bietet Tools zum Erstellen und Bereitstellen von vertrauenswürdigen Zertifikatprofilen und Simple Certificate Enrollment Protocol-Zertifikaten (SCEP), die zum Sichern und Authentifizieren von WLAN-, VPN- und E-Mail-Profilen verwendet werden können.|[Aktivieren des Zugriffs auf Unternehmensressourcen mithilfe von Zertifikatprofilen in Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md)|
|WLAN-Profile|Bereitstellen von Einstellungen für drahtlose Netzwerke für Ihre Benutzer. Durch Bereitstellen dieser Einstellungen erleichtern Sie dem Endbenutzer das Herstellen einer Verbindung mit dem Unternehmensnetzwerk.|[Benutzern mithilfe von WLAN-Profilen mit Microsoft Intune die Verbindung mit Unternehmensnetzwerken erleichtern](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md)|
|E-Mail-Profile|Erstellen und Bereitstellen von E-Mail-Einstellungen für Geräte. Auf diese Weise erhalten Benutzer Zugriff auf Unternehmens-E-Mails auf ihren persönlichen Geräten, ohne dafür ein Setup vornehmen zu müssen.|[Konfigurieren des Zugriffs auf Unternehmens-E-Mail mithilfe von E-Mail-Profilen in Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md)|
|VPN-Profile|Stellen Sie VPN-Einstellungen für Benutzer und Geräte in Ihrer Organisation bereit. Durch Bereitstellen dieser Einstellungen erleichtern Sie dem Endbenutzer das Verbinden mit Ressourcen im Unternehmensnetzwerk.|[Unterstützen von Benutzern beim Verbinden mit ihrer Arbeit über VPN-Profile in Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md)|
|Bedingte Zugriffsrichtlinien|Verwalten des Zugriffs auf Microsoft Exchange-E-Mail- und SharePoint Online auf Geräten, die nicht von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltet werden.|[Verwalten des Zugriffs auf E-Mail und SharePoint mit Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md)|

## Inventar und Berichterstellung

|Funktion|Details|Weitere Informationen|
|------------|-----------|-------------------------|
|Inventar und Berichterstellung|Suchen Sie nach Informationen zu den Geräten, die Sie verwalten, und der Software, die sie verwenden.<br /><br />Sie haben eine Reihe von Möglichkeiten, um diese Berichte zu filtern, wie z. B. nach Geräteplattform und danach, ob das Gerät Unternehmensstandards einhält.|[Einblicke in Microsoft Intune-Vorgänge durch Berichte](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md)|

## Siehe auch
[Einführung in Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)
[Vorbereiten der Registrierung von Geräten in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)
[Verwalten von mobilen Geräten und PCs aus der Cloud](http://technet.microsoft.com/library/dn715906.aspx)
[Bring Your Own Device (BYOD) – Entwurfsüberlegungen](http://technet.microsoft.com/library/dn656905.aspx)
[Registrieren Sie sich für eine kostenlose Testversion](https://account.manage.microsoft.com/Signup/MainSignUp.aspx?OfferId=A77BE827-FC8B-4EF2-A0F5-7CD6C813AA65&ali=1)
[Intune-Bezugsquellen](http://technet.microsoft.com/library/dn646949.aspx)
[Starten der Verwendung von Microsoft Intune](../Topic/Start_using_Microsoft_Intune.md)
[Microsoft Intune-Dienstbeschreibung](../Topic/Microsoft_Intune_Service_Description.md)
[Erste Schritte mit einer 30-Tage-Testversion von Microsoft Intune](../Topic/Get_started_with_a_30-day_trial_of_Microsoft_Intune.md)

