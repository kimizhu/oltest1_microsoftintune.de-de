---
description: na
keywords: na
title: Enable mobile device enrollment with the Microsoft Intune Account Portal
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3adf63cd-34b6-4641-aa88-766bb59dd853
robots: noindex,nofollow
---
# Aktivieren der Registrierung mobiler Ger&#228;te &#252;ber das Microsoft Intune-Kontoportal
Intune unterstützt die Verwendung privater Geräte (Bring Your Own Device, BYOD), indem Benutzer ihre Geräte über das Microsoft Intune-**Kontoportal** registrieren.Bevor Sie Geräte registrieren können, müssen Sie Intune für die Verwaltung mobiler Geräte konfigurieren.Wenn Sie es nicht bereits getan haben, richten Sie die Verwaltung für jede Geräteplattform in Ihrem Unternehmen ein:

-   [iOS-Verwaltung](http://technet.microsoft.com/library/dn408185.aspx)

-   [Android-Verwaltung](http://technet.microsoft.com/library/dn764960.aspx)

-   [Windows-Verwaltung](http://technet.microsoft.com/library/dn764959.aspx)

## Aktivieren der Registrierung mobiler Geräte über das Intune-Kontoportal

1.  **Hinzufügen von Intune-Benutzern** 
    Der Eigentümer des mobilen Geräts muss dem Microsoft Intune-Kontoportal hinzugefügt werden, bevor Geräte registriert werden können.Melden Sie sich beim [Microsoft Intune-Kontoportal](http://account.manage.microsoft.com) an, klicken Sie auf **Benutzer hinzufügen**, und wählen Sie eine Option aus:

    -   **Benutzer**: Um einen einzelnen Benutzer hinzuzufügen, wählen Sie **Neu** &gt; **Benutzer**, und geben Sie **Details**, **Rollen zuweisen**, **Benutzerstandort einstellen** ein, und weisen Sie dann den Benutzer zu einer **Gruppe** hinzu.

    -   **Massenhinzufügen**: Erstellen Sie eine CSV-Datei (siehe bereitgestellte Beispieldateien), und importieren Sie diese ins Intune-Kontoportal.Geben Sie Rollen, den Speicherort und die Gruppe an, und erstellen Sie anschließend die Konten.Beispieldateien und leere CSV-Dateien können vom Microsoft Intune-Kontoportal heruntergeladen werden.

    Sie können auch die Active Directory- oder Azure Active Directory-Synchronisierung aktivieren.Weitere Informationen zur Integration anderer Azure Active Directory-Benutzer mit Intune finden Sie unter [Fahrplan zur Verzeichnissynchronisierung](http://go.microsoft.com/fwlink/?LinkId=511540), oder klicken Sie auf **Andere Möglichkeiten zum Hinzufügen von Benutzern** im Intune-Kontoportal.

2.  **Erstellen von Gruppen**  (optional)
    Gruppen bieten Flexibilität für die Verwaltung von Geräten und Benutzern.Sie können die Gruppen so einrichten, wie es Ihren organisatorischen Anforderungen am besten entspricht, beispielsweise nach geografischem Standort, Abteilung oder Hardwareeigenschaften.Weitere Informationen finden Sie unter [Verwenden von Gruppen zum Verwalten von Benutzern und Geräten in Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

3.  **Hinzufügen von Richtlinien für Geräte** (optional)
    Richtlinien sind Gruppen von Einstellungen zum Steuern der Features auf Geräten. Die meisten MDM-Richtlinien sind plattformspezifisch. Sie erstellen Richtlinien mithilfe von Vorlagen, in denen empfohlene oder angepasste Einstellungen enthalten sind, und stellen diese dann für Gruppen bereit. Weitere Informationen finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

4.  **Festlegen der Beschränkung für Registrierungen für das Gerät** (optional) 
    Um die Anzahl von mobilen Geräten zu beschränken, die ein Benutzer registrieren kann, melden Sie sich bei der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) an, klicken Sie auf **Verwaltung** &gt; **Verwaltung mobiler Geräte** &gt; **Registrierungsregeln**.Wählen Sie die maximale Anzahl der Geräte aus, die ein Benutzer registrieren kann, und klicken Sie dann auf **Speichern**.

5.  **Festlegen von Unternehmensportaleinstellungen** 
     Sie können das Intune-Unternehmensportal für Ihr Unternehmen anpassen.Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) auf **Verwaltung** &gt; **Unternehmensportal**.Konfigurieren Sie Folgendes

    -   **Firmenname**

    -   **Kontaktname für IT-Abteilung**

    -   **Telefonnummer der IT-Abteilung**

    -   **Weitere Informationen**

    -   **URL der Datenschutzrichtlinie des Unternehmens**

    -   **URL der Supportwebsite (nicht angezeigt)**

    -   **Websitename**

6.  **Festlegen von Nutzungsbedingungen** 
    Sie können die Nutzungsbedingungen veröffentlichen, die den Benutzern angezeigt werden, wenn sie das Unternehmensportal das erste Mal auf einem beliebigen Gerät verwenden.Wechseln Sie in der [Microsoft Intune-Administrationskonsole](http://manage.microsoft.com) zu **Unternehmensportal** &gt; **Nutzungsbedingungen**.

### <a name="BKMK_TermsAndConditions"></a>Informationen zu den Nutzungsbedingungen
Sie können die Nutzungsbedingungen veröffentlichen, die den Benutzern angezeigt werden, wenn sie das Unternehmensportal das erste Mal auf einem beliebigen Gerät verwenden, unabhängig davon, ob das Gerät bereits registriert ist.Benutzer müssen diese Bedingungen für den Zugriff auf das Portal akzeptieren.Wenn Sie die Nutzungsbedingungen maßgeblich aktualisieren und diese von den Benutzern angezeigt und akzeptiert werden sollen, können Sie die neuen Nutzungsbedingungen als neue Version kennzeichnen. Die Benutzer durchlaufen dann denselben Prozess, wenn sie das Portal das nächste Mal besuchen.

Nutzungsbedingungen gelten für Benutzer, nicht für Geräte. Daher müssen die Benutzer die jeweilige Version nur einmal akzeptieren, um das Unternehmensportal von einem ihrer Geräte besuchen zu können.

#### Berichte zu Nutzungsbedingungen
Berichte zu **Nutzungsbedingungen** zeigen an, welche Benutzer die Nutzungsbedingungen akzeptiert haben sowie die zuletzt akzeptierte Versionsnummer und das Datum, an dem diese Version akzeptiert wurde.Exportieren Sie den Bericht, um ein Archiv zu erhalten, wann die Benutzer frühere Versionen akzeptiert haben.Weitere Informationen finden Sie unter [Einblicke in Microsoft Intune-Vorgänge durch Berichte](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md).

### So registrieren Benutzer ihre mobilen Geräte
Nachdem Sie die Registrierung eingerichtet haben, können Sie Benutzer zum Registrieren Ihrer Geräte einladen.Anleitungen für Benutzer zum Registrieren ihrer persönlichen Geräte finden Sie in den [Microsoft Intune-Registrierungsanweisungen](http://go.microsoft.com/fwlink/?LinkID=534864).Weitere Informationen finden Sie unter [Informieren der Endbenutzer über den Einsatz von Microsoft Intune](../Topic/What_to_tell_your_end_users_about_using_Microsoft_Intune.md).

Allgemeine Anweisungen:

1.  Benutzer registrieren und verwalten ihre mobilen Geräte mithilfe der Unternehmensportal-App.Benutzer können auch die Unternehmensportal-Website zum Registrieren von Geräten verwenden.

    -   **Android**: Benutzer installieren die **Unternehmensportal**-App der Microsoft Corporation, die in [Google Play](http://go.microsoft.com/fwlink/p/?LinkId=386612) verfügbar ist.

    -   **iOS**: Benutzer installieren die **Unternehmensportal**-App der Microsoft Corporation, die im App Store verfügbar ist.Benutzer können dann ihre **Geräte** anzeigen, um ihre Mobiltelefone zu registrieren.

    -   **Windows Phone 8.1**: Benutzer installieren die **Unternehmensportal**-App der Microsoft Corporation, die im Windows Phone Store verfügbar ist.Wenn eine signierte Unternehmensportal-App verteilt wurde, können Benutzer zu **Einstellungen** &gt; **Arbeitsbereich** &gt; **Konto hinzufügen** wechseln, sich anmelden und dann auf **Firmenanwendung oder -Hub installieren** tippen, um das Unternehmensportal zu installieren.

    -   **Windows Phone 8.0**: Klicken Sie auf **Systemeinstellungen** &gt; **Unternehmens-Apps**, und melden Sie sich mit Ihrer Benutzer-ID an.Die Unternehmensportal-App wird auf dem Telefon der Benutzer bereitgestellt.

    -   **Windows 8.1 und Windows RT 8.1**: Benutzer laden die **Unternehmensportal**-App aus dem Windows Store herunter.Wenn eine signierte Unternehmensportal-App verteilt wurde, können Benutzer auch zu **PC-Einstellungen** &gt; **Netzwerk** &gt; **Arbeitsbereich** wechseln, sich anmelden, das Kontrollkästchen **Apps und Dienste des IT-Administrators zulassen** aktivieren und dann auf **Teilnehmen** klicken.

    -   **Windows RT**: Klicken Sie auf **Start**, geben Sie „Systemkonfiguration“ ein, und klicken Sie auf das Dialogfeld, um die **Unternehmens-Apps** zu öffnen.

2.  Beim Öffnen des Unternehmensportals werden sie zur Eingabe von Anmeldeinformationen aufgefordert.Wenn Sie die öffentliche Domäne CNAME nicht erstellt haben, werden Benutzer von Windows und Windows Phone zur Eingabe der Serveradresse aufgefordert, und sie müssen dann „manage.microsoft.com“ eingeben.Benutzer von Windows Phone 8.1 und iOS können dann ihre **registrierten Geräte** anzeigen, um ihre Mobiltelefone zu registrieren.

3.  Wenn sich ein Benutzer zuerst registriert oder Sie die Zustimmung zu einer neuen Version der Nutzungsbedingungen angefordert haben, müssen Benutzer den Nutzungsbedingungen zustimmen.Das Gerät wird unabhängig davon registriert, ob sie den Nutzungsbedingungen zustimmen oder nicht.Wenn die Nutzungsbedingungen akzeptiert werden, können sie zum Portal wechseln.Wenn sie ablehnen, werden sie aufgefordert, diesen Vorgang zu bestätigen. Dann erhalten Sie einen Link zu Anweisungen, die Informationen zum Aufheben der Registrierung enthalten.Die Registrierung wird nicht automatisch aufgehoben. Bis die Registrierung aufgehoben wurde, können sie das Gerät weiterhin verwalten.

    An diesem Punkt unterscheidet sich dieser Vorgang für Geräte, deren Registrierung noch nicht aufgehoben wurde, je nach Betriebssystem des Geräts.

    -   Für Windows- und Windows Phone 8.1-Geräte erinnert das Unternehmensportal den Benutzer daran, die Registrierung vorzunehmen.Windows Phone 8.1 verfügt über einen Link zu den Registrierungseinstellungen, während Windows einen Link zu Inhalten der Hilfe verwendet, in denen die Registrierung beschrieben wird.

    -   Für IOS- und Android-Geräte wird der Benutzer durch den Registrierungsvorgang geführt.Benutzer erhalten weiterhin eine Nachricht von Microsoft über die Auswirkungen der Registrierung.

> [!CAUTION]
> Windows- und Windows Phone-Benutzer finden ggf. die Registrierungsoberfläche vor und registrieren sich, ohne Ihre Nutzungsbedingungen zu sehen.Empfehlen Sie Ihren Benutzern, beim Windows Store oder Windows Phone Store zu beginnen, damit Ihre Nutzungsbedingungen mehr Verbreitung finden und akzeptiert werden.

**Sobald Geräte registriert sind, können Sie:**

-   [Verstehen Sie Ihre Geräte mithilfe des Inventars in Microsoft Intune](../Topic/Understand_your_devices_with_inventory_in_Microsoft_Intune.md)

-   [Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

-   [Bereitstellen von Apps für mobile Geräte in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)

-   [Verwalten von Einstellungen und Features auf Ihren Geräten mit Microsoft Intune-Richtlinien](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md)

-   [Schützen Ihrer Daten mit Remotezurücksetzen, Remotesperre und Kennungszurücksetzung in Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md)

## Siehe auch
[Vorbereiten der Registrierung von Geräten in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)
[Registrieren von firmeneigenen Geräten mit dem Geräteregistrierungs-Manager in Microsoft Intune](../Topic/Enroll_corporate-owned_devices_with_the_Device_Enrollment_Manager_in_Microsoft_Intune.md)
[Intune-Bezugsquellen](http://technet.microsoft.com/library/dn646949.aspx)

