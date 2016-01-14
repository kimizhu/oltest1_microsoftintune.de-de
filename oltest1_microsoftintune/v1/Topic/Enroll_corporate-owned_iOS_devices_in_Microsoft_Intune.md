---
description: na
keywords: na
title: Enroll corporate-owned iOS devices in Microsoft Intune
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d3ca4ab-f20c-4d56-9413-f8ef19cf0722
robots: noindex,nofollow
---
# Registrieren firmeneigener iOS-Ger&#228;ten in Microsoft Intune
Intune unterstützt die Registrierung von firmeneigenen iOS-Geräten mithilfe des Apple Device Enrollment Program (DEP) oder des Tools [Apple Configurator](http://go.microsoft.com/fwlink/?LinkId=518017), das auf einem Mac-Computer ausgeführt wird.

Sie können firmeneigene iOS-Geräte auf drei Arten registrieren:

-   **Setup-Assistent für die Registrierung**: Setzt das Gerät auf die Werkseinstellungen zurück und bereitet es für die Einrichtung durch den neuen Benutzer des Geräts vor.Diese Methode unterstützt die Registrierung mit DEP oder dem Apple Configurator.

-   **Direkte Anmeldung** – Erstellt eine Apple Configurator-kompatible Datei zur Verwendung während der Vorbereitung des Geräts.Das registrierte Gerät wird nicht auf die Werkseinstellungen zurückgesetzt, aber ist keinem Benutzer zugewiesen.Diese Methode kann nicht für die Registrierung mit DEP verwendet werden.

-   **Device Enrollment Programm (DEP)**: Stellt ein Registrierungsprofil bereit, mit dem das Gerät "drahtlos" registriert wird, und kann die Setup-Assistent-Optionen für das Gerät enthalten.Die Registrierung von Geräten über DEP kann von Benutzern nicht rückgängig gemacht werden.

## Anweisungen für den Setup-Assistenten

1.  **Erstellen einer mobilen Gerätegruppe** (Optional) 
    Wenn Ihr Unternehmen mobile Gerätegruppen zur Verwaltung von Geräten erfordert, erstellen Sie diese Gruppen.[Verwenden von Gruppen zum Verwalten von Benutzern und Geräten in Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

2.  **Erstellen eines Profils für Geräte**
    Ein Registrierungsprofil für Geräte definiert die Einstellungen für eine Gruppe von Geräten.Wenn Sie dies noch nicht getan haben, erstellen Sie ein Registrierungsprofil für iOS-Geräte, die mit Apple Configurator registriert werden.**Eingabeaufforderung für Benutzerzuweisung** sollte für die Registrierung mit dem **Setup-Assistenten** aktiviert werden.

    ###### Anweisungen

    1.  Wechseln Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) zu **Richtlinie** &gt; **Firmeneigene Geräte**, und klicken Sie dann auf **Hinzufügen…**.

    2.  Geben Sie die Details für die Geräteprofile ein:

        -   **Name**: Name des Geräteanmeldungsprofils.(Für Benutzer nicht sichtbar)

        -   **Beschreibung**: Beschreibung des Geräteanmeldungsprofils.(Für Benutzer nicht sichtbar)

        -   **Benutzerzuweisung**: Gibt an, wie Geräte registriert werden.

            -   **Eingabeaufforderung für Benutzeraffinität** – Das Gerät kann während der ersten Installation einem Benutzer zugewiesen werden und dann berechtigt sein, auf Unternehmensdaten und E-Mail im Namen dieses Benutzers zuzugreifen.Dieser Modus unterstützt eine Reihe von Szenarien:

                -   **Persönliches firmeneigenes Gerät**: „Choose Your Own Device“ (CYOD) Ähnlich privaten oder persönlichen Geräten, aber der Administrator hat bestimmte Rechte, z. B. die Berechtigung zum Löschen, Zurücksetzen, Verwalten und Abmelden des Geräts.Der Benutzer des Geräts kann Apps installieren und hat die meisten anderen Berechtigungen für die Verwendung des Geräts, soweit diese nicht durch Verwaltungsrichtlinien gesperrt sind.

                -   **Konto des Geräteregistrierungsmanagers**: Das Gerät wird mit einem speziellen Intune-Administratorkonto registriert.Es kann als privates Konto verwaltet werden, aber nur ein Benutzer, der die Anmeldeinformationen des Registrierungsmanagers kennt, kann Apps installieren, löschen, zurücksetzen, verwalten und das Gerät abmelden.Informationen zum Registrieren von Geräten, die von vielen Benutzern über ein allgemeines Konto gemeinsam verwendet werden, finden Sie unter [Registrieren von firmeneigenen Geräten mit dem Geräteregistrierungs-Manager in Microsoft Intune](../Topic/Enroll_corporate-owned_devices_with_the_Device_Enrollment_Manager_in_Microsoft_Intune.md).

            -   **Keine Benutzeraffinität** – Für das Gerät sind keine Eingriffe durch Benutzer erforderlich.Verwenden Sie diese Zuweisung für Geräte, die Aufgaben ohne den Zugriff auf lokale Benutzerdaten ausführen.Apps, die eine Benutzerzuweisung erfordern, werden deaktiviert oder funktionieren nicht.

        -   **Gerätegruppen-Vorabzuweisung**: Alle Geräte, die mit diesem Profil bereitgestellt werden, gehören anfänglich zu dieser Gruppe.Sie können die Geräte nach der Registrierung erneut zuweisen.

    3.  Klicken Sie auf **Profil speichern**, um das Profil hinzuzufügen.

3.  **Mit dem Setup-Assistenten zu registrierende iOS-Geräte hinzufügen**
    Wechseln Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) zu **Gruppen** &gt; **Alle Geräte** &gt; **Alle firmeneigenen Geräte** &gt; **Alle Geräte**, und klicken Sie dann auf **Geräte hinzufügen**.Sie können Geräte auf zwei Arten hinzufügen:

    -   **Eine CSV-Datei mit Seriennummern hochladen** – Erstellen Sie eine durch Trennzeichen getrennte Liste von zwei Spalten ohne Header, beschränkt auf 5000 Geräte oder 5 MB pro CSV-Datei.

        |||
        |-|-|
        |&lt;Serie 1&gt;|&lt;Gerätedetails 1&gt;|
        |&lt;Serie 2&gt;|&lt;Gerätedetails 2&gt;|
        Diese CSV-Datei wird bei der Anzeige in einem Text-Editor folgendermaßen angezeigt:

        ```
        0000000,PO 1234
        111111111,PO 1234
        ```

    -   **Gerätedetails manuell hinzufügen**: Geben Sie die Seriennummer und Gerätedetails von bis zu fünf Geräten ein.

    > [!NOTE]
    > Wenn Sie später firmeneigene Geräte aus der Intune-Verwaltung entfernen müssen, entfernen Sie die Seriennummer des Geräts in Intune aus der Gruppe **Firmeneigene Geräte**, um die Geräteregistrierung zu deaktivieren.  Wenn Intune eine Notfallwiederherstellung durchführt, während oder nachdem Seriennummern entfernt wurden, müssen Sie sicherstellen, dass in dieser Gruppe nur die Seriennummern aktiver Geräte vorhanden sind.

    Klicken Sie dann auf **Weiter**.

4.  **Auswählen der zu registrierenden Geräte**
    Bestätigen Sie die zu registrierenden Geräte.Bereits registrierte oder anderweitig registrierte Seriennummern werden nicht importiert.Klicken Sie zum Fortfahren auf **Weiter**.

5.  **Zuweisen eines Profils**
    Geben Sie das Profil an, das hinzugefügten Geräten aus der Liste der verfügbaren Profile zugewiesen werden soll, überprüfen Sie die **Registrierungsprofildetails**, und klicken Sie dann auf **Fertig stellen**.Manuell hinzugefügte Geräte können einem Registrierungsprofil zugewiesen werden. Mit DEP synchronisierte Geräte müssen allerdings einem DEP-fähigen Profil zugeordnet sein.

6.  **Auswählen eines Profils zum Bereitstellen auf iOS-Geräten**
    Wechseln Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) zu **Richtlinie** &gt; **Unternehmensgeräteregistrierung**, und wählen Sie das Geräteprofil aus, das auf mobilen Geräten bereitgestellt werden soll.Klicken Sie in der Taskleiste auf **Exportieren...**.Kopieren und speichern Sie die **Profil-URL**.Sie werden sie später in Apple Configurator hochladen, um das von iOS-Geräten verwendete Intune-Profil zu definieren.Bei DEP-Geräte können Sie einfach die Erstkonfiguration mit einem Werksimage durchführen oder das Gerät auf die Werkseinstellungen zurücksetzen.

7.  **Vorbereiten des Geräts mit Apple Configurator** 
    iOS-Geräte werden mit dem Mac-Computer verbunden und für die Verwaltung mobiler Geräte registriert.

    > [!WARNING]
    > Während des Registrierungsprozesses werden die Geräte auf Werkseinstellungen zurückgesetzt.

    1.  Öffnen Sie auf einem Mac-Computer **Apple Configurator**.

    2.  Wählen Sie **Setup** und dann **Geräteregistrierung** aus.Geben Sie die Registrierungs-URL von Intune in **MDM Server-URL**, ein und klicken Sie dann auf **Speichern**.

    3.  Verbinden Sie die mobilen iOS-Geräte über einen USB-Adapter mit dem Apple-Computer.

    4.  Klicken Sie auf **Vorbereiten**.Der Fortschritt wird in Apple Configurator angezeigt.

8.  **Verteilen von Geräten** 
    Die Geräte sind nun für die Unternehmensregistrierung bereit.Schalten Sie die Geräte aus, und verteilen Sie sie an Benutzer.Wenn das Gerät eingeschaltet wird, wird der Setup-Assistent gestartet und fragt die Benutzer nach ihrem Geschäfts- oder Schulkonto.

## Anweisungen für die direkte Registrierung

1.  **Erstellen einer mobilen Gerätegruppe** (Optional) 
    Wenn Ihr Unternehmen oder Ihre Organisation mobile Gerätegruppen zur Verwaltung von Geräten erfordert, erstellen Sie diese Gruppen.[Verwenden von Gruppen zum Verwalten von Benutzern und Geräten in Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

2.  **Erstellen eines Profils für Geräte**
    Ein Registrierungsprofil für Geräte definiert die Einstellungen für Geräte.Wenn Sie dies noch nicht getan haben, erstellen Sie ein Registrierungsprofil für iOS-Geräte, die mit Apple Configurator registriert werden.

    ###### Anweisungen

    1.  Wechseln Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) zu **Richtlinie** &gt; **Unternehmensgeräteregistrierung**, und klicken Sie dann auf **Hinzufügen**.

    2.  Geben Sie die Details für die Geräteprofile ein:

        -   **Name**: Name des Geräteanmeldungsprofils.Für Benutzer nicht sichtbar.

        -   **Beschreibung**: Beschreibung des Geräteanmeldungsprofils.Für Benutzer nicht sichtbar.

        -   **Benutzerzuweisung**: Gibt an, wie Geräte registriert werden.Wählen Sie für die direkte Registrierung **Keine Aufforderung**.

        -   **Gerätegruppen-Vorabzuweisung**: Alle Geräte, die mit diesem Profil bereitgestellt werden, gehören anfänglich zu dieser Gruppe.Sie können die Geräte nach der Registrierung erneut zuweisen.

    3.  Klicken Sie auf **Profil speichern**, um das Profil hinzuzufügen.

3.  **Auswählen und Exportieren einer Registrierungsprofildatei** 
    Wechseln Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) zu **Richtlinie** &gt; **Unternehmensgeräteregistrierung**, und wählen Sie das Geräteprofil aus, das auf iOS-Geräten bereitgestellt werden soll.Klicken Sie in der Taskleiste auf **Exportieren...**.Das Fenster **Apple-Konfigurationsmethode** wird geöffnet.

    Wählen Sie unter **Apple-Konfigurationsmethode** die Option **Direkte Registrierung** aus.Laden Sie die Profildatei für die direkte Registrierung (.mobileconfig) herunter, und speichern Sie sie.Sie müssen diese Datei in Apple Configurator importieren, um das Intune-Profil für iOS-Geräte zu definieren.Eine Registrierungsprofildatei ist zwei Wochen gültig.

4.  **Importieren der Profildatei und Vorbereiten des Geräts** 
    Kopieren Sie die Intune-Registrierungsprofildatei (.mobileconfig) auf einen Mac-Computer, und importieren Sie die Datei in Apple Configurator.Anschließend können Sie iOS-Geräte über USB verbinden, um sie bei Apple Configurator zu registrieren.Geräte, die mit dieser Datei konfiguriert werden, müssen den Setup-Assistenten bereits abgeschlossen haben und benötigen eine Internetverbindung, wenn die Datei angewendet wird.

## Registrieren firmeneigener iOS-Geräte in Microsoft Intune mithilfe des Apple Device Enrollment Program
Zum Verwalten firmeneigener iOS-Geräte mit Apple Device Enrollment Programm (DEP) müssen Unternehmen dem Apple DEP beitreten und Geräte über das Programm beziehen.Details zu diesem Prozess finden Sie unter: [https://deploy.apple.com](https://deploy.apple.com)

Bevor Sie firmeneigene iOS-Geräte mit DEP registrieren können, benötigen Sie einen DEP-Token von Apple.Mit diesem Token kann Intune Informationen zu DEP-Geräten synchronisieren, die Ihrem Unternehmen gehören.Damit kann Intune außerdem Registrierungsprofile an Apple übermitteln und diesen Profile Geräte zuweisen.

### <a name="BKMK_DEPtok"></a>

1.  **Beginnen der Verwaltung von iOS-Geräten mit Microsoft Intune** 
    Bevor Sie iOS DEP-Geräte registrieren können, müssen Sie die Schritte zum [Einrichten der iOS-Verwaltung mit Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) ausführen.

2.  **Abrufen eines Verschlüsselungsschlüssels** 
    Öffnen Sie als Administrator die [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com), wechseln Sie zu **Verwaltung** &gt; **Verwaltung mobiler Geräte** &gt; **iOS** &gt; **Device Enrollment Program**, und klicken Sie auf **Verschlüsselungsschlüssel herunterladen**.Speichern Sie die Verschlüsselungsschlüsseldatei (PEM) lokal.Die PEM-Datei wird verwendet, um ein Vertrauensstellungszertifikat vom Apple Device Enrollment Program-Portal anzufordern.

3.  **Abrufen eines Device Enrollment Program-Tokens** 
    Rufen Sie das [Device Enrollment Program-Portal](https://deploy.apple.com) (https://deploy.apple.com) auf, und melden Sie sich mit der Apple-ID Ihres Unternehmen an.Diese Apple-ID muss später verwendet werden, um das DEP-Token zu erneuern.

    1.  Wechseln Sie im [Device Enrollment Program-Portal](https://deploy.apple.com) zu **Device Enrollment Program** &gt; **Server verwalten**, und klicken Sie dann auf **MDM-Server hinzufügen**.

    2.  Geben Sie den **MDM-Servernamen** ein , und klicken Sie dann auf **Weiter**.Der Servername dient als Referenz zum Identifizieren des MDM-Servers.Es ist nicht der Name oder die URL des Microsoft Intune-Servers.

    3.  Das Dialogfeld **&lt;Servername&gt; hinzufügen** wird geöffnet.Klicken Sie auf **Datei auswählen...**, um die PEM-Datei hochzuladen, und klicken Sie auf **Weiter**.

    4.  Im Dialogfeld **&lt;Servername&gt; hinzufügen** wird der Link **Ihr Servertoken** angezeigt.Laden Sie die Servertokendatei (.p7m) auf Ihren Computer herunter, und klicken Sie dann auf **Fertig**.

    Diese Zertifikatdatei (.p7m) wird verwendet, um eine Vertrauensstellung zwischen dem Intune- und Apple Device Enrollment Program-Server herzustellen.

4.  **Hinzufügen des DEP-Tokens zu Intune** 
    Wechseln Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) zu **Verwaltung** &gt; **Verwaltung mobiler Geräte** &gt; **iOS** &gt; **Device Enrollment Program**, und klicken Sie auf **DEP-Token hochladen**.**Wechseln Sie** zur Zertifikatdatei (.p7m), geben Sie Ihre **Apple-ID** ein, und klicken Sie auf **Hochladen**.

5.  **Hinzufügen der Corporate Device Enrollment-Richtlinie** 
    Wechseln Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) zu **Richtlinie** &gt; **Corporate Device Enrollment**, und klicken Sie dann auf **Hinzufügen**.Geben Sie **allgemeine** Details ein, wie z. B. **Name** und **Beschreibung**. Geben Sie an, ob die dem Profil zugeordneten Geräte zu einem Benutzer oder einer Gruppe gehören, und aktivieren Sie dann **Device Enrollment Program-Einstellungen für diese Richtlinie konfigurieren**, um DEP zu unterstützen.Die **Setup-Assistent-Bereiche** definieren die iOS-Geräteeinstellungen, die während des Setups konfiguriert werden.

6.  **Zuweisen von DEP-Geräten zur Verwaltung** 
    Wechseln Sie zum [Device Enrollment Program-Portal](https://deploy.apple.com) (https://deploy.apple.com), und melden Sie sich mit der Apple-ID Ihres Unternehmens an.Wechseln Sie **Bereitstellungsprogramm** &gt; **Device Enrollment Program** &gt; **Geräte verwalten**.Geben Sie an, wie Sie **Geräte wählen**, fügen Sie Geräteinformationen hinzu, und geben Sie die Details zum Gerät wie **Seriennummer** und **Bestellnummer** an, oder **laden Sie eine CSV-Datei hoch**.Wählen Sie als Nächstes **Zu Server zuweisen**. Wählen Sie den für Microsoft Intune angegebenen &lt;Servernamen&gt; aus, und klicken Sie dann auf **OK**.

7.  **Verteilen von Geräten an Benutzer** 
    Ihre firmeneigenen Geräte können jetzt an Benutzer verteilt werden.Wenn ein iOS-Gerät eingeschaltet wird, wird es für die Verwaltung durch Intune registriert.

8.  **Synchronisieren von mit DEP verwalteten Geräten** 
    Öffnen Sie als Administrator die [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com), wechseln Sie zu **Verwaltung** &gt; **Verwaltung mobiler Geräte** &gt; **iOS** &gt; **Device Enrollment Program**, und klicken Sie auf **Jetzt synchronisieren**.Eine Synchronisierungsanforderung wird an Apple gesendet.Zum Anzeigen von DEP verwalteter Geräte nach der Synchronisierung wechseln Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) zu **Gruppen** &gt; **Alle firmeneigenen Geräte**.Im Arbeitsbereich **Firmeneigene Geräte** wird der **Status** verwalteter Geräte als "Nicht kontaktiert" angezeigt, bis das Gerät eingeschaltet und der Setup-Assistent auf ihm ausgeführt wird.

## Nächste Schritte
**Sobald Geräte registriert sind, können Sie:**

-   [Verstehen Sie Ihre Geräte mithilfe des Inventars in Microsoft Intune](../Topic/Understand_your_devices_with_inventory_in_Microsoft_Intune.md)

-   [Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

-   [Bereitstellen von Apps für mobile Geräte in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)

-   [Verwalten von Einstellungen und Features auf Ihren Geräten mit Microsoft Intune-Richtlinien](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md)

-   [Schützen Ihrer Daten mit Remotezurücksetzen, Remotesperre und Kennungszurücksetzung in Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md)

## Siehe auch
[Vorbereiten der Registrierung von Geräten in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

