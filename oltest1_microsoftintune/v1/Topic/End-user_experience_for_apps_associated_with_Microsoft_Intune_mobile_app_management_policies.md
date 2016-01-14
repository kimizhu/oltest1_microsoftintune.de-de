---
description: na
keywords: na
title: End-user experience for apps associated with Microsoft Intune mobile app management policies
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b57e6525-b57c-4cb4-a84c-9f70ba1e8e19
---
# Endbenutzer-Erfahrung mit Apps, die den Microsoft Intune-Verwaltungsrichtlinien f&#252;r mobile Apps unterliegen
MAM-Richtlinien (Mobile Application Management, Verwaltung mobiler Anwendungen) werden nur angewendet, wenn Apps im beruflichen Kontext verwendet werden.  Die folgenden Szenarien helfen Ihnen, Ihre Benutzer zu informieren, damit sie verstehen, wie verwaltete Apps funktionieren.

**Gegenstand dieses Themas**

[Szenario: Zugreifen auf OneDrive mit einem iOS-Gerät](#bkmk_OneDriveiOS)

[Szenario: Zugreifen auf OneDrive mit einem Android-Gerät](#bkmk_OneDriveAndroid)

[Szenario: Verwenden von Microsoft Word für berufliche und private Zwecke](#bkmk_wordworkandpersonal)

#### <a name="bkmk_OneDriveiOS"></a>Szenario: Zugreifen auf OneDrive mit einem iOS-Gerät

1.  Starten Sie **OneDrive**, um die Anmeldeseite zu öffnen.

    ![](../Image/AppManagement/iOS_OneDriveLaunch.png)

    > [!NOTE]
    > Auf einem privaten Gerät müsste der Endbenutzer normalerweise die App herunterladen.  Wenn das Gerät jedoch mit einer MDM-Lösung verwaltet wird, können Sie die App auf dem Gerät bereitstellen.

2.  Geben Sie den Benutzernamen Ihres Geschäftskontos ein. Sie werden auf die Seite **Office 365-Authentifizierung** weitergeleitet, auf der Sie Ihre Unternehmensanmeldeinformationen eingeben können.

    ![](../Image/AppManagement/iOS_O365SignInPage.png)

3.  Nachdem Ihre Anmeldeinformationen von Azure Active Directory erfolgreich authentifiziert wurden, werden die MAM-Richtlinien angewendet, und Sie werden aufgefordert, **OneDrive** neu zu starten.

    ![](../Image/AppManagement/iOS_AppRestartforMAM.png)

4.  Wenn Sie **OneDrive** neu starten, wird die App mit aktivierten MAM-Richtlinien gestartet. Sie werden nun aufgefordert, eine **PIN** für die App einzugeben (sofern hierfür eine Richtlinie konfiguriert wurde).

    ![](../Image/AppManagement/iOS_AppPINPrompt.png)

5.  Nachdem Sie die PIN festgelegt und bestätigt haben, können Sie auf Ihre Dateien in **OneDrive for Business** zugreifen.

    ![](../Image/AppManagement/iOS_OneDriveSuccess.png)

    > [!NOTE]
    > Wenn Sie eine schon bereitgestellte Richtlinie ändern, werden die Änderungen beim nächsten Öffnen der App angewendet.

#### <a name="bkmk_OneDriveAndroid"></a>Szenario: Zugreifen auf OneDrive mit einem Android-Gerät

1.  Starten Sie OneDrive, um die Anmeldeseite zu öffnen.

    > [!NOTE]
    > Auf einem privaten Gerät müsste der Endbenutzer normalerweise die App herunterladen.  Wenn das Gerät jedoch mit einer MDM-Lösung verwaltet wird, können Sie die App auf dem Gerät bereitstellen.

2.  Geben Sie den Benutzernamen Ihres Geschäftskontos ein. Sie werden auf die Seite **Office 365-Authentifizierung** weitergeleitet, auf der Sie Ihre Unternehmensanmeldeinformationen eingeben können.

    ![](../Image/AppManagement/Android_O365SignInPage.png)

3.  Nachdem Ihre Anmeldeinformationen von **Azure AD** erfolgreich authentifiziert wurden, sollte eine Meldung mit Anweisungen zur Installation der Unternehmensportal-App angezeigt werden, sofern diese auf dem Gerät noch nicht installiert ist.  Tippen Sie auf **App abrufen**, um fortzufahren.

    ![](../Image/AppManagement/Android_CompanyPortalMessage.png)

4.  Sie befinden sich nun im **Google Play Store**, von wo Sie die App **Unternehmensportal** herunterladen und installieren können.

    Die App "Unternehmensportal" hilft Ihnen, Ihre Daten zu schützen.

    ![](../Image/AppManagement/Android_CompanyPortalInstall.png)

5.  Klicken Sie nach Abschluss der Installation auf **Annehmen**, um die Bedingungen zu akzeptieren.

    ![](../Image/AppManagement/Android_CompanyPortalAccept.png)

6.  **OneDrive** wird automatisch gestartet.

7.  Beim nächsten Öffnen von OneDrive werden Sie aufgefordert, eine **PIN** einzurichten, sofern die Richtlinieneinstellungen vorgeben, dass für den Zugriff auf **OneDrive** eine PIN erforderlich ist.

    ![](../Image/AppManagement/Android_OneDriveSetPIN.png)

8.  Nachdem Sie die PIN festgelegt und bestätigt haben, können Sie **OneDrive** weiterhin verwenden, wobei nun die Richtlinien für verwaltete Apps gelten.

    ![](../Image/AppManagement/Android_OneDriveConfirmPIN.png)

#### <a name="bkmk_wordworkandpersonal"></a>Szenario: Verwenden von Microsoft Word für berufliche und private Zwecke

1.  Öffnen Sie **Word** auf Ihrem Gerät. Zur Darstellung der Schritte wird ein iOS-Gerät verwendet.

2.  Tippen Sie auf **Neu**, um ein neues Word-Dokument zu erstellen.

    ![](../Image/AppManagement/iOS_WordCreateNewDoc.png)

3.  Geben Sie einen oder zwei Sätze ein.  Wenn Sie dieses Dokument speichern, werden sowohl private als auch geschäftliche Speicherorte als Optionen zum Speichern des soeben erstellten Dokuments angezeigt.  An diesem Punkt werden die App-Richtlinien noch nicht angewendet, da der private/geschäftliche Kontext noch nicht eingerichtet wurde.

4.  Speichern Sie das Dokument an Ihrem OneDrive for Business-Speicherort. Das Dokument wird damit als Unternehmensdaten gekennzeichnet, und die Einschränkungen der Richtlinie werden wirksam.

    ![](../Image/AppManagement/iOS_WordCreateCompanyDoc.PNG)

5.  Öffnen Sie das Dokument, das Sie am Unternehmensspeicherort gespeichert haben.  Kopieren Sie den Text, öffnen Sie Ihr privates **Facebook**-Konto, und versuchen Sie, den kopierten Text einzufügen.  Wie Sie sehen, können Sie den Text nicht in den neuen Facebook-Beitrag einfügen. Die Option "Einfügen" ist nicht abgeblendet, aber wenn Sie auf **Einfügen** klicken, erfolgt keine Aktion.

    ![](../Image/AppManagement/iOS_WordCopyCompany.png)

    ![](../Image/AppManagement/iOS_FacebookPasteCompany.png)

6.  Wiederholen Sie nun die Schritte 2 und 3, um ein weiteres neues Dokument zu erstellen, geben Sie einen oder zwei Sätze ein, und speichern Sie das Dokument diesmal nicht mit dem Geschäftskonto, sondern mit Ihrem privaten Konto an einem privaten Speicherort wie **OneDrive – persönlich**.

    ![](../Image/AppManagement/iOS_WordCopyPersonal.png)

7.  Öffnen Sie das Dokument, das Sie auf Ihrem persönlichen Speicherort abgelegt haben.  Kopieren Sie den Text, öffnen Sie die **Facebook**-App, und versuchen Sie, den kopierten Text einzufügen. Wie Sie sehen, können Sie den kopierten Inhalt in einen Facebook-Beitrag einfügen.

    ![](../Image/AppManagement/iOS_FacebookPastePersonal.png)

### Ändern des Benutzerkontos auf einem Gerät
Bei den OneDrive- und Outlook-Apps können Sie auf einem Gerät nur ein Geschäftskonto verwenden, für das eine MAM-Richtlinie gilt.  Das Hinzufügen weiterer Geschäftskonten wird von diesen Apps blockiert.  Sie können jedoch einen Benutzer entfernen und auf dem Gerät einen weiteren Benutzer hinzufügen.

Wenn Sie ein iOS-Gerät verwenden und versuchen, auf demselben Gerät ein zweites Geschäftskonto einzurichten, wird eine Sperrnachricht angezeigt.  Darüber hinaus wird eine Option zum Entfernen des vorhanden Kontos und zum Hinzufügen eines neuen Kontos angezeigt. Klicken Sie hierfür auf **Ja**.

![](../Image/AppManagement/iOS_SwitchUser.PNG)

Wenn Sie ein Android-Gerät verwenden, wird eine Sperrnachricht mit Anweisungen angezeigt, wie Sie das vorhandene Konto entfernen und ein neues Konto hinzufügen können.  Wechseln Sie auf Android-Geräten zum Entfernen eines vorhandenen Kontos zu **Einstellungen &gt; Allgemein &gt; Anwendungs-Manager &gt; Unternehmensportal**, und wählen Sie "Daten löschen" aus.

![](../Image/AppManagement/Android_SwitchUser.png)

## Siehe auch
[Erstellen und Bereitstellen von Verwaltungsrichtlinien für mobile Apps mit Microsoft Intune](../Topic/Create_and_deploy_mobile_app_management_policies_with_Microsoft_Intune.md)

