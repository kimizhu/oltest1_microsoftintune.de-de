---
description: na
keywords: na
title: Configure access to corporate email using email profiles with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 10f0cd61-e514-4e44-b13e-aeb85a8e53ae
---
# Konfigurieren des Zugriffs auf Unternehmens-E-Mail mithilfe von E-Mail-Profilen in Microsoft Intune
Mit E-Mail-Profilen in [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] können Sie Exchange ActiveSync-E-Mail-Einstellungen auf Geräten erstellen, bereitstellen und überwachen.Auf diese Weise erhalten Benutzer Zugriff auf Unternehmens-E-Mails, ohne dafür ein Setup vornehmen zu müssen.

Sie können E-Mail-Profile verwenden, um die folgenden Gerätetypen zu konfigurieren:

-   Geräte unter Windows Phone 8 und höher

-   Geräte unter iOS 5 und höher

-   Geräte unter Samsung KNOX Standard (4.0 oder höher)

Sie können nicht nur ein E-Mail-Konto auf dem Gerät konfigurieren, sondern auch Synchronisierungseinstellungen (beispielsweise wie viele E-Mails synchronisiert werden sollen und abhängig vom Gerätetyp die zu synchronisierenden Inhaltstypen).

> [!IMPORTANT]
> Wählen Sie nach Möglichkeit die sichersten Optionen aus, die von der E-Mail-Infrastruktur und den Clientbetriebssystemen unterstützt werden.E-Mail-Profile bieten eine praktische Methode zum zentralen Verteilen und Verwalten von E-Mail-Einstellungen, die Ihre Geräte bereits unterstützen.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] bietet keine zusätzlichen E-Mail-Funktionen.

## Wie E-Mail-Profile geschützt werden
E-Mail-Profile können mit einer von zwei Methoden geschützt werden:

### Zertifikate
Beim Erstellen des E-Mail-Profils wählen Sie ein SCEP-Zertifikatprofil aus, das Sie zuvor in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] erstellt haben.Dieses wird als Identitätszertifikat bezeichnet und dient zur Authentifizierung anhand eines von Ihnen erstellten vertrauenswürdigen Zertifikatprofils (oder eines Stammzertifikats), mit dem überprüft wird, ob das Gerät des Benutzers eine Verbindung herstellen darf.Das vertrauenswürdige Zertifikat wird auf dem Computer bereitgestellt, der die E-Mail-Verbindung authentifiziert. In der Regel ist dies der Exchange-Server.

Weitere Informationen zum Erstellen und Verwenden von Zertifikatprofilen in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] finden Sie unter [Aktivieren des Zugriffs auf Unternehmensressourcen mithilfe von Zertifikatprofilen in Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).

### Benutzername und Kennwort
Der Benutzer wird beim Exchange-Server durch die Bereitstellung seines Benutzernamens und Kennworts authentifiziert.

Das Kennwort ist nicht im E-Mail-Profil enthalten, sodass der Benutzer dieses beim Herstellen einer Verbindung zum E-Mail-System bereitstellen muss.

### Erstellen eines E-Mail-Profils

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie einen der folgenden Richtlinientypen:

    -   **E-Mail-Profil für Samsung KNOX Standard (4.0 oder höher)**

    -   **E-Mail-Profil (iOS 5 und höher)**

    -   **E-Mail-Profil (Windows Phone 8 und höher)**

    Sie können nur benutzerdefinierte E-Mail-Profilrichtlinien erstellen.Empfohlene Einstellungen sind nicht verfügbar.

    Weitere Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie im Thema [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Verwenden Sie die folgende Tabelle, um Einstellungen von E-Mail-Profilen für Samsung KNOX zu konfigurieren:

    |Name der Einstellung|Weitere Informationen|
    |------------------------|-------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für das E-Mail-Profil ein.|
    |**Beschreibung**|Geben Sie eine Beschreibung, die einen Überblick über das E-Mail-Profil bietet, und andere relevante Informationen an, mit denen Sie danach suchen können.|
    |**Host**|Geben Sie den Hostnamen des Exchange-Servers Ihres Unternehmens an, der die Exchange ActiveSync-Dienste hostet.|
    |**Kontoname**|Geben Sie den Anzeigenamen für das E-Mail-Konto so an, wie er den Benutzern auf ihren Geräten angezeigt wird.|
    |**Benutzername**|Wählen Sie, wie der Benutzername für das E-Mail-Konto abgerufen wird:<br /><br />-   Wählen Sie für einen lokalen Exchange-Server **Benutzername**.<br />-   Wählen Sie für Office 365 **Benutzerprinzipalname** aus dem Dropdown-Menü.|
    |**E-Mail-Adresse**|Wählen Sie, wie die E-Mail-Adresse für den Benutzer auf jedem Gerät generiert wird.<br /><br />-   **Primäre SMTP-Adresse**: Verwendet die primäre SMTP-Adresse des Benutzers, um sich bei Exchange anzumelden.<br />-   **Benutzerprinzipalname**: Verwendet den vollständigen Benutzerprinzipalnamen als E-Mail-Adresse.|
    |**Authentifizierungsmethode**|Wählen Sie die Authentifizierungsmethode aus, die vom E-Mail-Profil verwendet wird:<br /><br />-   **Benutzername und Kennwort**<br />-   **Zertifikate**|
    |**Wählen Sie ein Clientzertifikat für die Clientauthentifizierung (Identitätszertifikat) aus**|Wählen Sie das zuvor erstellte SCEP-Clientzertifikat aus, das zur Authentifizierung der Exchange-Verbindung verwendet werden soll.Weitere Informationen zur Verwendung von Zertifikatprofilen in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] finden Sie unter [Aktivieren des Zugriffs auf Unternehmensressourcen mithilfe von Zertifikatprofilen in Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). **Note:** Diese Option wird nur für die Authentifizierungsmethode **Zertifikate** angezeigt.|
    |**S/MIME verwenden**|Ausgehende E-Mails werden mithilfe von S/MIME-Verschlüsselung gesendet.|
    |**Signaturzertifikat**|Wählen Sie das Signaturzertifikat aus, das zum Signieren von ausgehenden E-Mails verwendet werden soll. **Note:** Diese Option wird nur angezeigt, wenn Sie **S/MIME verwenden** auswählen.|
    |**Anzahl der Tage für die E-Mail-Synchronisierung**|Wählen Sie in der Dropdownliste die Anzahl der Tage von E-Mails aus, die synchronisiert werden sollen, oder wählen Sie **Unbegrenzt** aus, um alle verfügbaren E-Mail-Nachrichten zu synchronisieren.|
    |**Synchronisierungszeitplan**|Wählen Sie den Zeitplan aus, nach dem Geräte mit Daten vom Exchange-Server synchronisiert werden.Sie können auch **Wenn Nachrichten eintreffen** auswählen, wobei die Daten sofort bei Eintreffen synchronisiert werden, oder **Manuell**, wobei der Benutzer des Geräts die Synchronisierung initiieren muss.|
    |**SSL verwenden**|Verwendet SSL-Kommunikation (Secure Sockets Layer) beim Senden und Empfangen von E-Mails sowie bei der Kommunikation mit dem Exchange-Server. **Note:** Für Geräte mit Samsung KNOX 4.0 oder höher müssen Sie Ihr Exchange Server-SSL-Zertifikat exportieren und es als ein Android Trusted Certificate Profile in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] bereitstellen.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] unterstützt den Zugriff auf dieses Zertifikat nicht, wenn es auf andere Weise auf dem Exchange Server installiert wurde.|
    |**Zu synchronisierender Inhaltstyp**|Wählen Sie die Inhaltstypen aus, die auf Geräten synchronisiert werden sollen.Wählen Sie aus:<br /><br />-   **E-Mail**<br />-   **Kontakte**<br />-   **Kalender**<br />-   **Aufgaben**<br />-   **Hinweise**|
    Verwenden Sie die folgende Tabelle, um Einstellungen von E-Mail-Profilen für iOS zu konfigurieren:

    |Name der Einstellung|Weitere Informationen|
    |------------------------|-------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für das E-Mail-Profil ein.|
    |**Beschreibung**|Geben Sie eine Beschreibung, die einen Überblick über das E-Mail-Profil bietet, und andere relevante Informationen an, mit denen Sie danach suchen können.|
    |**Host**|Geben Sie den Hostnamen des Exchange-Servers Ihres Unternehmens an, der die Exchange ActiveSync-Dienste hostet.|
    |**Kontoname**|Geben Sie den Anzeigenamen für das E-Mail-Konto so an, wie er den Benutzern auf ihren Geräten angezeigt wird.|
    |**Benutzername**|Wählen Sie, wie der Benutzername für das E-Mail-Konto auf jedem Gerät generiert wird.Sie können eine der folgenden Optionen aus der Dropdownliste wählen:<br /><br />-   **Primäre SMTP-Adresse**: Verwendet die primäre SMTP-Adresse des Benutzers, um sich bei Exchange anzumelden.<br />-   **Benutzerprinzipalname**: Verwendet den vollständigen Benutzerprinzipalnamen für die Anmeldung bei Exchange.|
    |**E-Mail-Adresse**|Wählen Sie, wie die E-Mail-Adresse für den Benutzer auf jedem Gerät generiert wird.Sie können eine der folgenden Optionen aus der Dropdownliste wählen:<br /><br />-   **Primäre SMTP-Adresse**: Verwendet die primäre SMTP-Adresse des Benutzers, um sich bei Exchange anzumelden.<br />-   **Benutzerprinzipalname**: Verwendet den vollständigen Benutzerprinzipalnamen als E-Mail-Adresse.|
    |**Authentifizierungsmethode**|Wählen Sie die Authentifizierungsmethode aus, die vom E-Mail-Profil verwendet wird:<br /><br />-   **Benutzername und Kennwort**<br />-   **Zertifikate**|
    |**Wählen Sie ein Clientzertifikat für die Clientauthentifizierung (Identitätszertifikat) aus**|Wählen Sie das zuvor erstellte SCEP-Clientzertifikat aus, das zur Authentifizierung der Exchange-Verbindung verwendet werden soll.Weitere Informationen zur Verwendung von Zertifikatprofilen in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] finden Sie unter [Aktivieren des Zugriffs auf Unternehmensressourcen mithilfe von Zertifikatprofilen in Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). **Note:** Diese Option wird nur für die Authentifizierungsmethode **Zertifikate** angezeigt.|
    |**S/MIME verwenden**|Ausgehende E-Mails werden mithilfe von S/MIME-Verschlüsselung gesendet.|
    |**Signaturzertifikat**|Wählen Sie optional das Signaturzertifikat aus, das zum Signieren von ausgehenden E-Mails verwendet werden soll. **Note:** Diese Option wird nur angezeigt, wenn Sie **S/MIME verwenden** auswählen.|
    |**Anzahl der Tage für die E-Mail-Synchronisierung**|Wählen Sie in der Dropdownliste die Anzahl der Tage von E-Mails aus, die synchronisiert werden sollen, oder wählen Sie **Unbegrenzt** aus, um alle verfügbaren E-Mail-Nachrichten zu synchronisieren.|
    |**SSL verwenden**|Verwendet SSL-Kommunikation (Secure Sockets Layer) beim Senden und Empfangen von E-Mails sowie bei der Kommunikation mit dem Exchange-Server.|
    |**Verschieben von Nachrichten in andere E-Mail-Konten zulassen**|Ermöglicht es Benutzern, E-Mail-Nachrichten zwischen verschiedenen Konten zu verschieben, die sie auf ihrem Gerät konfiguriert haben.|
    |**Senden von E-Mails über Anwendungen von Drittanbietern zulassen**|Ermöglicht Benutzern das Senden von E-Mails aus anderen Apps als der standardmäßigen E-Mail-App.|
    |**Zuletzt verwendete E-Mail-Adressen synchronisieren**|Synchronisiert die Liste der E-Mail-Adressen, die auf dem Gerät zuletzt verwendet wurden.|
    Verwenden Sie die folgende Tabelle, um Einstellungen von E-Mail-Profilen für Windows Phone zu konfigurieren:

    |Name der Einstellung|Weitere Informationen|
    |------------------------|-------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für das E-Mail-Profil ein.|
    |**Beschreibung**|Geben Sie eine Beschreibung, die einen Überblick über das E-Mail-Profil bietet, und andere relevante Informationen an, mit denen Sie danach suchen können.|
    |**Host**|Geben Sie den Hostnamen des Exchange-Servers Ihres Unternehmens an, der die Exchange ActiveSync-Dienste hostet.|
    |**Kontoname**|Geben Sie den Anzeigenamen für das E-Mail-Konto so an, wie er den Benutzern auf ihren Geräten angezeigt wird.|
    |**Benutzername**|Wählen Sie, wie der Benutzername für das E-Mail-Konto auf jedem Gerät generiert wird.Sie können eine der folgenden Optionen aus der Dropdownliste wählen:<br /><br />-   **Primäre SMTP-Adresse**: Verwendet die primäre SMTP-Adresse des Benutzers, um sich bei Exchange anzumelden.<br />-   **Benutzerprinzipalname**: Verwendet den vollständigen Benutzerprinzipalnamen für die Anmeldung bei Exchange.|
    |**E-Mail-Adresse**|Wählen Sie, wie die E-Mail-Adresse für den Benutzer auf jedem Clientgerät generiert wird.Sie können eine der folgenden Optionen aus der Dropdownliste wählen:<br /><br />-   **Primäre SMTP-Adresse** – Die primäre SMTP-Adresse von Benutzern wird zum Anmelden bei Exchange verwendet.<br />-   **Benutzerprinzipalname** – Der vollständige Benutzerprinzipalname wird als E-Mail-Adresse verwendet.|
    |**Anzahl der Tage für die E-Mail-Synchronisierung**|Wählen Sie in der Dropdownliste die Anzahl der Tage von E-Mails aus, die synchronisiert werden sollen, oder wählen Sie **Unbegrenzt** aus, um alle verfügbaren E-Mail-Nachrichten zu synchronisieren.|
    |**Synchronisierungszeitplan**|Wählen Sie den Zeitplan aus, nach dem Geräte mit Daten vom Exchange-Server synchronisiert werden.Sie können auch **Wenn Nachrichten eintreffen** auswählen, wobei die Daten sofort bei Eintreffen synchronisiert werden, oder **Manuell**, wobei der Benutzer des Geräts die Synchronisierung initiieren muss.|
    |**SSL verwenden**|Verwendet SSL-Kommunikation (Secure Sockets Layer) beim Senden und Empfangen von E-Mails sowie bei der Kommunikation mit dem Exchange-Server.|
    |**Zu synchronisierender Inhaltstyp**|Wählen Sie die Inhaltstypen aus, die auf Geräten synchronisiert werden sollen.Wählen Sie aus:<br /><br />-   **E-Mail**<br />-   **Kontakte**<br />-   **Kalender**<br />-   **Aufgaben**|
    > [!IMPORTANT]
    > Wenn Sie ein E-Mail-Profil bereitgestellt haben und dann die Werte für **Exchange ActiveSync-Host** oder **E-Mail-Adresse** ändern möchten, müssen Sie das vorhandene E-Mail-Profil löschen und ein neues mit den erforderlichen Werten erstellen.

4.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

### Bereitstellen eines E-Mail-Profils

1.  Stellen Sie das E-Mail-Profil für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrem Unternehmen bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen auf der Seite **Übersicht** des Arbeitsbereichs **Richtlinie** identifiziert Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern.Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

> [!NOTE]
> Wenn Sie ein E-Mail-Profil von einem Gerät entfernen, bearbeiten Sie die Bereitstellung, und entfernen Sie alle Gruppen, in denen das Gerät Mitglied ist.

## Nächste Schritte
Nach der erfolgreichen Bereitstellung werden die Geräte des Benutzers mit den richtigen Einstellungen für den Zugriff auf Unternehmens-E-Mail konfiguriert.

## Siehe auch
[Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

