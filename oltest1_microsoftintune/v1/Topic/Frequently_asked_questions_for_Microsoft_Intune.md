---
description: na
keywords: na
title: Frequently asked questions for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a8126cca-9ec4-454b-a20b-dc1bb6797327
---
# H&#228;ufig gestellte Fragen zu Microsoft Intune
Dieses Thema liefert Antworten auf häufig gestellte Fragen zu Microsoft Intune. Haben Sie Vorschläge für weitere Fragen, die Sie gerne beantwortet hätten? [Dann setzen Sie sich mit uns in Verbindung.](https://microsoftintune.uservoice.com/)

## Info zu diesen FAQs
Diese häufig gestellten Fragen sind in die folgenden Kategorien untergliedert:

-   [Allgemein](#BKMK_General)

-   [Konten](#BKMK_Accounts)

-   [Anmeldung](#BKMK_Enrollment)

-   [Verwaltung mobiler Geräte](#BKMK_MDM)

-   [App-Bereitstellung](#BKMK_App_Deploy)

-   [Sicherheit](#BKMK_Security)

-   [Unternehmensportal](#BKMK_Company_Portal)

-   [Microsoft Intune mit Configuration Manager](#BKMK_hybrid)

### <a name="BKMK_General"></a>Allgemein

-   **Woher weiß ich, wenn der Microsoft Intune-Dienst aktualisiert wurde?**

    Melden Sie sich bei Ihrem Konto bei „manage.microsoft.com“ an. Wählen Sie in der Verwaltungsübersicht „Dienststatus anzeigen“ aus. Dort werden der Speicherort Ihres Mandanten und der Zeitplan für die Datenbankwartung aufgeführt. Ausführliche Informationen zu den Dienstupdates finden Sie unter [Neuheiten in Microsoft Intune](../Topic/What_s_new_in_Microsoft_Intune.md).

-   **Wenn ein Benutzer ein Gerät innerhalb der Unternehmensportal-App umbenennt, wird dadurch auch der Name in Intune oder im Konfigurations-Manager geändert?**

    Nein, diese Namensänderung dient nur zur Vereinfachung für den Benutzer.

-   **Gibt es eine Funktion zur Remoteunterstützung für mobile Geräte in Intune?**

    Nein, gibt es nicht. Drittanbieter-Apps, z. B. [Lumia Beamer](https://www.lumiabeamer.com/), [Bomgar](http://www.bomgar.com/) oder [TeamViewer](https://www.teamviewer.com/), eignen sich zu diesem Zweck.

### <a name="BKMK_Accounts"></a>Konten

-   **Wenn ich Intune teste und einen neuen Mandanten für die Testversion erstelle, kann ich O365 mit den gleichen Mandanten zur Evaluierung hinzufügen?**

    Ja. Melden Sie sich mithilfe eines globalen Administrators in Ihrem vorhandenen Intune-Mandanten/-Abonnement an, wie z. B. *globaleradmin@&lt;Unternehmen&gt;.onmicrosoft.com*.

-   **Wenn ich Intune während eines Testabonnements MDM-Autorität zuweise, erschwert das den Wechsel zum Dienst eines anderen Unternehmens, falls ich meine Meinung zu Intune ändere?**

    Auch wenn Sie diese Entscheidung bezüglich Intune treffen sollten, wirkt sich die Wahl der MDM-Autorität nicht auf einen Wechsel zu einem anderen Dienst aus. Dies ist eine spezielle Option von Intune oder Intune mit System Center Configuration Manager von O365-MDM.

-   **Kann ich meinen vorhandenen Office 365-Domänennamen für mein nachfolgendes Intune-Konto verwenden?**

    Ja, wenn Sie sich mit der Organisations-ID anmelden, die Ihrem vorhandenen O365-Mandanten und der überprüften Domäne beim Erstellen der Intune-Testversion oder Aktivieren der Lizenzen zugeordnet wurde. Intune verwendet dann die gleichen Domänen, Benutzer usw. wie für das O365-Konto. Beachten Sie, dass jeder O365-Benutzer als Intune-Benutzer mit einer Intune-Lizenz aktiviert werden muss. Dies müsste vom globalen Administrator ausgeführt werden, der den Mandanten verwaltet.

### <a name="BKMK_Enrollment"></a>Anmeldung

-   **Wo können Benutzer erfahren, wie sie ihre Geräte registrieren?**

    Sie können dazu die Informationen aus den [Microsoft Intune-Registrierungsanweisungen](http://www.microsoft.com/en-us/download/46398) verwenden oder anpassen.

-   **Wie behebe ich Fehler bei der Geräteregistrierung?**

    Methoden zur Behandlung allgemeiner Probleme bei der Registrierung finden Sie unter [Behandlung von Problemen bei der Geräteregistrierung bei Intune](../Topic/Troubleshoot_device_enrollment_in_Intune.md).

-   **Wie kann ich Registrierungsprotokolle erfassen, wenn bei einem Benutzer Registrierungsprobleme auftreten?**

    Befolgen Sie [diese Anweisungen](http://www.microsoft.com/en-us/download/46391).

### <a name="BKMK_MDM"></a>Verwaltung mobiler Geräte

-   **MDM – allgemein**

    -   **Kann Intune Geräte mit Jailbreak erkennen?**

        Ja, bei einigen Betriebssystemen. Informationen zum Verwalten von Geräten mit Jailbreak finden Sie unter[Verwalten von Gerätekonformitätsrichtlinien für Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md).

    -   **Kann ich Unternehmensdaten von einem Gerät selektiv zurücksetzen?**

        Ja. Informationen zum selektiven Zurücksetzen finden Sie unter [Schützen Ihrer Daten mit Remotezurücksetzen, Remotesperre und Kennungszurücksetzung in Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md).

    -   **Gibt es eine Möglichkeit zum Blockieren bestimmter Websites auf dem mobilen Gerätebrowser über Intune?**

        Nicht in den systemeigenen Browsern aller Plattformen. Sie können URLs jedoch zulassen oder blockieren, wenn Sie den über [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwalteten Webbrowser auf iOS- und Android-Geräten bereitgestellt haben. Weitere Informationen finden Sie unter [Verwalten des Internetzugriffs mittels Richtlinien für verwaltete Browser mit Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md).

    -   **Können wir verhindern, dass ein Benutzer eine App deinstalliert?**

        Im Allgemeinen nicht. Allerdings können Sie auf einem überwachten iOS-Gerät verhindern, dass ein Benutzer eine App deinstalliert, die mithilfe von Apple Configurator verteilt wurde. Weitere Informationen zur Verwendung des überwachten Modus in Microsoft Intune finden Sie unter [Manage access to apps using Microsoft Intune configuration policies - deleted](../Topic/Manage_access_to_apps_using_Microsoft_Intune_configuration_policies_-_deleted.md).

    -   **Gibt es eine Möglichkeit zum Verwalten der mobilen Datennutzung?**

        Nicht direkt, Sie können jedoch sicherstellen, dass WLAN die bevorzugte Methode zum Herstellen einer Verbindung ist, indem Sie WLAN-Profile auf die Geräte übertragen, wie unter [Benutzern mithilfe von WLAN-Profilen mit Microsoft Intune die Verbindung mit Unternehmensnetzwerken erleichtern](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md) beschrieben. Zudem ermöglichen einige Plattformen (z. B. iOS und Android KNOX) die Steuerung von Einstellungen wie Sprach- und Datenroaming.

    -   **Gibt es eine Möglichkeit, zu verhindern, dass ein Benutzer die Registrierung eines Geräts aufhebt? Wie sieht dies bei einem Gerät in Unternehmensbesitz aus?**

        In der Regel nicht. Allerdings können Sie dies auf Windows Phone 8.1 mithilfe von benutzerdefinierten Windows Phone-Einstellungen erzwingen. Darüber hinaus kann bei iOS-Geräten, die überwacht und im Registrierungsprogramm für Apple-Geräte (DEP) registriert werden, verhindert werden, dass ein Benutzer eine Geräteregistrierung aufhebt.

    -   **Kann ich die gewählte MDM-Autorität wechseln?**

        In einigen Situationen können Sie die MDM-Autorität wechseln. Wenden Sie sich dazu an den Support, wie unter [Anfordern von Support für Microsoft Intune](../Topic/How_to_get_support_for_Microsoft_Intune.md) beschrieben. In der folgenden Tabelle wird beschrieben, welche Änderungen möglich sind. Eine Änderung der MDM-Autorität erfordert die erneute Registrierung der Geräte.

        |||||
        |-|-|-|-|
        ||**An:** Intune|**An:** O365|**An:** Configuration Manager mit Intune|
        |**Von:** Intune||Ja&#42;|Ja|
        |**Von:** O365|Ja&#42;||Ja|
        |**Von:** Configuration Manager mit Intune|Ja|Ja||
        &#42;O365- und Intune-MDM-Autoritäten können gleichzeitig verwendet werden, Sie müssen mobile Geräte also nicht erneut anmelden.

-   **Windows**

    -   **Kann ich eine Windows Store-App per Sideload auf ein Gerät übertragen?**

        Öffentlich verfügbare Apps können nicht per Sideload übertragen werden. Obwohl Sie die XAP herunterladen können, kann sie nicht in Intune hochgeladen werden, da es sich um eine öffentliche XAP handelt, die verschlüsselt und mit dem Codesignaturzertifikat des Entwicklers signiert wurde. Sie können nur Apps per Sideload übertragen, die Sie entwickeln und mit Ihrem eigenen Codesignaturzertifikat signieren.

    -   **Erfordern Windows Phone Store-Apps, die über das Unternehmensportal verteilt werden, dass der Endbenutzer ein Microsoft-Konto hat?**

        Ja, der Endbenutzer kann die Apps nicht ohne Microsoft-Konto abrufen. Ausgenommen davon sind private LOB-Apps, die per Sideload übertragen werden und auf einem Gerät ohne Microsoft-Konto bereitgestellt werden können.

    -   **Ist ein Microsoft-Konto auf einem Windows Phone 8.1 erforderlich, damit es mit Intune verwaltet werden kann?**

        Nein. Allerdings ist es erforderlich, um die meisten Apps aus dem öffentlichen Store zu installieren.

-   **Android**

    -   **Wie lange dauert es, ein Android-Gerät zu verschlüsseln?**

        Dies hängt in erster Linie von der Geschwindigkeit des Geräteprozessors und der Menge des gesamten und genutzten Arbeitsspeichers ab, da es keine Funktion von Intune ist.

-   **iOS**

    -   **Benötigt das Gerät eine Apple-ID-Angabe, um die Installation fortzusetzen, wenn bei der Bereitstellung von iOS-Apps mit Intune die IPA- und Manifest-Datei der Anwendung hochgeladen wurde?**

        Nein. Wenn Intune die Bits bereitstellt (IPA wurde in Intune hochgeladen), werden die Anwendungen per Sideload übertragen und benötigen keine Apple-ID.

    -   **Gibt es eine Möglichkeit, Apps auf iOS zu installieren, ohne Zugriff auf den Apple Store zu gewähren?**

        Nein, Sie können jedoch den App Store aktivieren und zugelassene bzw. blockierte Apps auf iOS verwenden, um Benutzeraktionen zu überwachen. Per Sideload übertragene LOB-Apps erfordern keinen Zugriff auf den Apple App Store.

    -   **Erfordern Apple Store-Apps, die über das Unternehmensportal verteilt werden, dass der Endbenutzer über ein iTunes-Konto verfügt?**

        Ja, der Endbenutzer kann die Apps nur mit iTunes-Konto abrufen.

    -   **Kann ich den App Store blockieren?**

        Ja, dadurch werden jedoch alle App-Installationen und Updates aus dem App Store blockiert, nicht nur die vom Benutzer initiierten. Dies bedeutet, dass bei allen öffentlichen App Store-Apps, die Sie über Intune bereitstellen, ebenfalls ein Fehler auftritt.

### <a name="BKMK_App_Deploy"></a>App-Bereitstellung

-   **Wie kann ich eine empfohlene App hinzufügen?**

    In Intune sind diese unter „Empfohlene Apps“ aufgeführt, und die diesbezügliche Dokumentation finden Sie unter [Bereitstellen von Apps für mobile Geräte in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md).

-   **Kann ich zusätzlichen Cloudspeicher für Apps erhalten, die bereitgestellt werden sollen?**

    Ja. Weitere Informationen hierzu finden Sie unter [Erste Schritte mit der Bereitstellung von Apps in Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md) im Abschnitt *Cloudspeicheranforderungen*.

### <a name="BKMK_Security"></a>Sicherheit

-   **Kann BitLocker-Schutz von Intune erzwungen werden?**

    Der OMA-DM-Agent von Windows 8.1/RT ermöglicht das Lesen (Abrufen) des Verschlüsselungsstatus. Dies kann nicht festgelegt werden. Dies gilt für Microsoft Intune und andere Verwaltungsdienste für mobile Geräte.

-   **Kann ich bei einem Windows 8-Tablet mit BitLocker-Verschlüsselung ein vollständiges Zurücksetzen des Geräts erzwingen, wenn eine Benutzeranmeldung mehrmals hintereinander fehlschlägt?**

    Kein Verwaltungsdienst für mobile Geräte, einschließlich Intune, bietet eine Option zum vollständigen Zurücksetzen von Geräten mit Windows 8.1/RT. Intune bietet für diese Geräte selektives Zurücksetzen. Weitere Informationen zum Zurücksetzen/selektiven Zurücksetzen in Intune finden Sie unter [Schützen Ihrer Daten mit Remotezurücksetzen, Remotesperre und Kennungszurücksetzung in Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md).

### <a name="BKMK_Company_Portal"></a>Unternehmensportal

-   **Kann ich das Unternehmensportal anpassen?**

    Ja. Wechseln Sie für diese Einstellungen in der Intune-Administratorkonsole zu **Admin &gt; Unternehmensportal**.

### <a name="BKMK_hybrid"></a>Microsoft Intune mit Configuration Manager

-   **Über welche Konsole verwalte ich meine Geräte, wenn ich Configuration Manager mit Intune verwende?**

    Verwalten Sie all Ihre Geräte selbst dann über die Configuration Manager-Konsole, wenn Geräte mit Intune-Agent in der Intune-Konsole angezeigt werden. Mobile Geräte werden nicht in der Intune-Konsole angezeigt.

-   **Kann ich selektives Zurücksetzen auf Geräten ausführen?**

    Wenn Sie System Center 2012 R2 Configuration Manager oder höher mit Intune verwenden, können Sie Unternehmensdaten per selektivem Zurücksetzen entfernen. Weitere Informationen finden Sie unter [Schützen Ihrer Daten mit Remotezurücksetzen, Remotesperre und Kennungszurücksetzung in Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md).

-   **Wenn ich Configuration Manager zusammen mit Intune verwende, kann ich trotzdem das Intune-Verwaltungsportal weiterhin verwenden?**

    Ja, Sie können jedoch nur Computer mit installiertem Intune-Agent über das Portal verwalten. Das Portal bietet einige nützliche Informationen zu Dienstbenachrichtigungen, zum Dienststatus usw. Die Geräteverwaltungseinstellungen dort werden jedoch nicht auf registrierte Geräte angewendet.

## Siehe auch
[Technische Referenz für Microsoft Intune](../Topic/Technical_reference_for_Microsoft_Intune.md)

