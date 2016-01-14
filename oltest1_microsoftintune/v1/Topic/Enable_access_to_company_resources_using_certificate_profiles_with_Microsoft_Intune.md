---
description: na
keywords: na
title: Enable access to company resources using certificate profiles with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8cbb8499-611d-4217-a7b4-e9b864785dd0
---
# Aktivieren des Zugriffs auf Unternehmensressourcen mithilfe von Zertifikatprofilen in Microsoft Intune
Zertifikatprofile sind [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinien zum Konfigurieren verwalteter Geräte mit den Zertifikaten, die benötigt werden, damit Gerätebenutzer über Verbindungen wie WLAN oder VPN auf die lokalen Unternehmensressourcen zugreifen können. Wenn Sie Zertifikatprofile bereitstellen, stellen Sie Geräte mit einem vertrauenswürdigen Stammzertifikat für Ihre PKI bereit und konfigurieren diese so, dass sie gerätespezifische Zertifikate anfordern.

Sie können drei Arten von Zertifikatprofilen erstellen:

-   Zertifikatprofil vom Typ "PKCS #12 (.PFX)": Kann mit Android 4.0 oder höher und Windows 10 (Desktop und mobil) und höher verwendet werden.

-   SCEP-Zertifikatprofil: Kann mit iOS 6.0 und höher, Android 4.0 oder höher und Windows Phone 8.1 und höher verwendet werden.

-   Vertrauenswürdiges Zertifikatprofil: Kann mit iOS 6.0 und höher, Android 4.0 oder höher und Windows Phone 8.1 und höher verwendet werden.

|Informationen zu Zertifikatprofilen|Details|
|---------------------------------------|-----------|
|Sie können Zertifikatprofile für Folgendes verwenden:|-   zum automatischen Konfigurieren von Geräten, sodass auf Unternehmensressourcen zugegriffen werden kann, ohne dass Zertifikate manuell oder mithilfe eines Out-of-Band-Prozesses installiert werden müssen,<br />-   zur Unterstützung beim Schützen von Unternehmensressourcen, indem Sie die Public Key-Infrastruktur (PKI) Ihres Unternehmens verwenden,<br />-   zur Verwendung der Serverauthentifizierung für alle WLAN- und VPN-Verbindungen, da Sie die erforderlichen Zertifikate auf den verwalteten Geräten bereitgestellt haben.|
|Zertifikatprofile bieten die folgenden Verwaltungsfunktionen:|<ul><li>Zertifikatregistrierung und -erneuerung über eine Unternehmenszertifizierungsstelle (CA) für Geräte, die Folgendes ausführen:<br /><br /><ul><li>Android</li><li>iOS</li><li>Windows 8.1</li><li>Windows Phone 8.1</li></ul></li></ul>Diese Zertifikate können dann für Verbindungen mit unserer lokalen Infrastruktur verwendet werden.<br /><br />-   Bereitstellung von vertrauenswürdigen Stammzertifizierungsstellenzertifikaten und Zwischenzertifizierungsstellenzertifikaten, um eine Vertrauenskette von Geräten für Verbindungen zu konfigurieren, für die eine Serverauthentifizierung erforderlich ist.<br />-   Überwachen und Melden der installierten Zertifikate.|
|Beispiele für die Verwendung von Zertifikatprofilen:|-   Mitarbeiter müssen Verbindungen mit WLAN-Hotspots an verschiedenen Unternehmensstandorten herstellen können. Sie können Zertifikatprofile verwenden, um die zum Schutz der WLAN-Verbindung erforderlichen Zertifikate bereitzustellen.<br />-   Sie haben eine PKI eingerichtet und möchten Zertifikate auf eine flexiblere, sicherere Art und Weise bereitstellen, die Benutzern ohne Beeinträchtigung der Sicherheit den Zugriff auf Unternehmensressourcen über ihre persönlichen Geräten ermöglicht. Dazu können Sie Zertifikatprofile mit Einstellungen und Protokollen konfigurieren, die von der jeweiligen Geräteplattform unterstützt werden. Die Geräte können diese Zertifikate dann automatisch von einem mit dem Internet verbundenen Registrierungsserver anfordern. Anschließend konfigurieren Sie VPN-Profile, die diese Zertifikate verwenden, damit das Gerät auf Unternehmensressourcen zugreifen kann.|

|Arten von Zertifikatprofilen|Details|
|--------------------------------|-----------|
|**Vertrauenswürdiges Stammzertifikatprofil**|Verwenden Sie dieses Profil, um das Zertifikat der vertrauenswürdigen Stammzertifizierungsstelle oder das Zertifikat der Zwischenzertifizierungsstelle für Geräte bereitzustellen:<br /><br />-   Erstellen Sie ein vertrauenswürdiges Stammzertifikatprofil für jede verwendete Plattform. Sie verbinden dieses Profil mit den einzelnen SCEP-Zertifikatprofilen, die Sie für die gleiche Plattform erstellen.|
|**PFX-Zertifikatprofile**|Verwenden Sie dieses Profil, um plattformspezifische Einstellungen für Gerätezertifikatanforderungen bereitzustellen:<br /><br />-   Erstellen Sie ein PFX-Zertifikatprofil für jede verwendete Plattform, und verbinden Sie es mit dem Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle.<br />-   Um das Erstellen eines PFX-Zertifikatprofils abzuschließen, müssen Sie ein zuvor erstelltes Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle auswählen.|
|**SCEP-Einstellungsprofil (Simple Certificate Enrollment-Protokoll)**|Verwenden Sie dieses Profil, um plattformspezifische Einstellungen für Gerätezertifikatanforderungen bereitzustellen:<br /><br />-   Erstellen Sie ein SCEP-Zertifikatprofil für jede verwendete Plattform, und verbinden Sie dieses mit dem Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle.<br />-   Um das Erstellen eines SCEP-Zertifikatprofils abzuschließen, müssen Sie ein zuvor erstelltes Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle auswählen.|
Um SCEP-Zertifikatprofile verwenden zu können, müssen Sie die folgende lokale Infrastruktur in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] integrieren:

-   einen Server, der den Registrierungsdienst für Netzwerkgeräte ausführt,

-   eine Unternehmenszertifizierungsstelle,

-   den Intune-Zertifikatconnector, der auf dem Windows Server 2012 R2-Server installiert wird, auf dem NDES ausgeführt wird.

Um PFX-Zertifikatprofile verwenden zu können, müssen Sie die folgende lokale Infrastruktur in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] integrieren:

-   eine Unternehmenszertifizierungsstelle,

-   einen Computer, der mit der Zertifizierungsstelle kommunizieren oder den Computer der Zertifizierungsstelle selbst verwenden werden kann,

-   den Intune Zertifikatconnector, der auf dem Computer ausgeführt wird, der mit der Zertifizierungsstelle kommunizieren kann.

In diesem Thema:

-   [Anforderungen für Zertifikatprofile](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md#BKMK_CertProfileRequirements)

-   [Konfigurieren der Infrastruktur](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md#BKMK_ConfigureInfrastructure)

-   [Konfigurieren von Zertifikatprofilen](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md#BKMK_ConfigProfiles)

-   [Bereitstellen von Zertifikatprofilen](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md#BKMK_Deploy)

## <a name="BKMK_CertProfileRequirements"></a>Anforderungen für Zertifikatprofile

### <a name="BKMK_OnPremises"></a>Lokale Infrastruktur

|Infrastruktur|Details|
|-----------------|-----------|
|**Active Directory-Domäne**|Alle in diesem Abschnitt aufgeführten Server (außer dem Webanwendungsproxy-Server) müssen der Active Directory-Domäne angehören.|
|**Zertifizierungsstellenserver**|Sie müssen über eine Unternehmenszertifizierungsstelle (CA) verfügen (als „ausstellende Zertifizierungsstelle“ bezeichnet), die auf einer Enterprise-Edition von [!INCLUDE[nextref_server_7](../Token/nextref_server_7_md.md)] oder höher ausgeführt wird.<br /><br />-   Eine eigenständige Zertifizierungsstelle wird nicht unterstützt.<br /><br />Anleitungen zum Einrichten einer Zertifizierungsstelle finden Sie unter [Installieren der Zertifizierungsstelle](http://technet.microsoft.com/library/jj125375.aspx).<br /><br />Wenn die Zertifizierungsstelle unter Windows Server 2008 R2 ausgeführt wird, müssen Sie [den Hotfix von KB2483564 installieren](http://support.microsoft.com/kb/2483564/).|
|Nur für SCEP-Profil: **NDES-Server**|Auf einem Server mit [!INCLUDE[winblue_server_2](../Token/winblue_server_2_md.md)] oder höher müssen Sie den Registrierungsdienst für Netzwerkgeräte einrichten:<br /><br />-   [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] unterstützt die Verwendung des Registrierungsdiensts für Netzwerkgeräte nicht, wenn es auf einem Server ausgeführt wird, der auch die Unternehmenszertifizierungsstelle ausführt.<br />-   Im [Leitfaden für den Registrierungsdienst für Netzwerkgeräte](http://technet.microsoft.com/library/hh831498.aspx) finden Sie Anweisungen zum Konfigurieren von [!INCLUDE[winblue_server_2](../Token/winblue_server_2_md.md)] als Host für den Registrierungsdienst für Netzwerkgeräte.|
|Nur für PFX-Zertifikatprofile: **Computer, die mit der Zertifizierungsstelle kommunizieren können**|Verwenden Sie alternativ den Computer mit der Zertifizierungsstelle selbst.|
|**Webanwendungsproxy-Server** (optional)|Als Webanwendungsproxy-Server (WAP) können Sie einen Server verwenden, der [!INCLUDE[winblue_server_2](../Token/winblue_server_2_md.md)] oder höher ausführt. Diese Konfiguration:<br /><br />-   ermöglicht Geräten das Empfangen von Zertifikaten über eine Internetverbindung,<br />-   ist eine Sicherheitsempfehlung, wenn Geräte eine Verbindung über das Internet herstellen, um Zertifikate zu empfangen oder zu erneuern.<br /><br />Auf dem Server, der den WAP hostet, [muss ein Update installiert werden](http://blogs.technet.com/b/ems/archive/2014/12/11/hotfix-large-uri-request-in-web-application-proxy-on-windows-server-2012-r2.aspx), das die Unterstützung für lange URLs aktiviert, die vom Registrierungsdienst für Netzwerkgeräte verwendet werden. Dieses Update ist im [Updaterollup vom Dezember 2014](http://support.microsoft.com/kb/3013769) enthalten oder kann auch einzeln von [KB3011135](http://support.microsoft.com/kb/3011135) heruntergeladen werden.<br /><br />Darüber hinaus muss der Server, der WAP hostet, folgende Bedingungen erfüllen:<br /><br />-   Er muss über ein SSL-Zertifikat verfügen, das mit dem Namen übereinstimmt, der für externe Clients veröffentlicht wird.<br />-   Er muss dem SSL-Zertifikat vertrauen, das auf dem NDES-Server verwendet wird.<br /><br />Diese Zertifikate ermöglichen dem WAP-Server, die SSL-Verbindung von Clients zu beenden und eine neue SSL-Verbindung mit dem NDES-Server herzustellen.<br /><br />Weitere Informationen über Zertifikate für WAP finden Sie im Abschnitt **Planen von Zertifikaten** des Themas [Installieren und Konfigurieren des Webanwendungsproxys für die Veröffentlichung interner Anwendungen](https://technet.microsoft.com/en-us/library/dn383650.aspx).<br /><br />Allgemeine Informationen zu WAP-Servern finden Sie unter [Verwenden des Webanwendungsproxys](http://technet.microsoft.com/library/dn584113.aspx).|
|**Microsoft Intune-Zertifikatconnector**|Sie nutzen die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungskonsole zum Herunterladen des Installationsprogramms für den **Zertifikatconnector** (**ndesconnectorssetup.exe**). Führen Sie **ndesconnectorssetup.exe** dann auf dem Computer aus, auf dem Sie den Zertifikatconnector installieren möchten. Installieren Sie für PFX-Zertifikatprofile den Zertifikatconnector auf dem Computer, der mit der Zertifizierungsstelle kommuniziert.|

### <a name="BKMK_CertsAndTemplates"></a>Zertifikate und Vorlagen

|Objekt|Details|
|----------|-----------|
|**Zertifikatvorlage**|Sie konfigurieren diese Vorlage auf der ausstellenden Zertifizierungsstelle.|
|**Clientauthentifizierungszertifikat**|Dieses Zertifikat, das von der ausstellenden oder öffentlichen Zertifizierungsstelle angefordert wurde, installieren Sie auf dem NDES-Server.|
|**Serverauthentifizierungszertifikat**|Dieses SSL-Zertifikat, das von der ausstellenden Zertifizierungsstelle oder öffentlichen Zertifizierungsstelle angefordert wurde, installieren und binden Sie in IIS auf dem NDES-Server.|
|**Zertifikat der vertrauenswürdigen Stammzertifizierungsstelle**|Sie exportieren dies als eine **CER**-Datei von der ausstellenden Zertifizierungsstelle oder von Geräten, die der ausstellenden Zertifizierungsstelle vertrauen, und stellen es mit dem Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle für Geräte bereit.<br /><br />-   Sie verwenden für jede Betriebssystemplattform ein einzelnes Zertifikat der vertrauenswürdigen Stammzertifizierungsstelle und ordnen es dem jeweiligen vertrauenswürdigen Stammzertifikatprofil zu, das Sie erstellen.<br />-   Sie können bei Bedarf zusätzliche vertrauenswürdige Stammzertifizierungsstellenzertifikate verwenden. Sie können dies zum Beispiel vornehmen, um einer Zertifizierungsstelle eine Vertrauensstellung zu gewähren, die die Serverauthentifizierungszertifikate für Ihre WLAN-Zugriffspunkte signiert.|

### <a name="BKMK_Accounts"></a>Konten

|Name|Details|
|--------|-----------|
|**NDES-Dienstkonto**|Sie geben ein Domänenbenutzerkonto an, das als NDES-Dienstkonto verwendet werden soll.|

## <a name="BKMK_ConfigureInfrastructure"></a>Konfigurieren der Infrastruktur
Vor dem Konfigurieren von Zertifikatprofilen müssen Sie die folgenden Aufgaben ausführen, für die Sie Kenntnisse über Windows Server 2012 R2 und Active Directory-Zertifikatdienste (ADCS) benötigen:

**Aufgabe 1**: Konfigurieren von Zertifikatvorlagen auf der Zertifizierungsstelle 
**Aufgabe 2**: nur für SCEP-Profile: Konfigurieren der Voraussetzungen auf dem NDES-Server 
**Aufgabe 3**:  nur für SCEP-Profile: Konfigurieren des NDES zur Verwendung mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] 
**Aufgabe 4**: Aktivieren, Installieren und Konfigurieren des Intune-Zertifikatconnectors

### <a name="BKMK_ConfigOnPremTask1"></a>Aufgabe 1: Konfigurieren von Zertifikatvorlagen für die Zertifizierungsstelle
Im Rahmen dieser Aufgabe führen Sie die folgenden Aktionen aus:

-   Erstellen eines NDES-Dienstkontos

    > [!NOTE]
    > Zum Widerrufen von Zertifikaten benötigt das NDES-Dienstkonto die Berechtigung *Zertifikate ausstellen und verwalten* für jede Zertifikatvorlage, die von einem Zertifikatprofil verwendet.

-   Konfigurieren einer Zertifikatvorlage für NDES

-   Veröffentlichen der Zertifikatvorlage für NDES

##### So konfigurieren Sie die Zertifizierungsstelle

1.  Erstellen Sie ein Domänenbenutzerkonto, das als NDES-Dienstkonto verwendet werden soll. Sie geben dieses Konto an, wenn Sie Vorlagen auf der ausstellenden Zertifizierungsstelle konfigurieren, bevor Sie NDES installieren und konfigurieren.

2.  Verwenden Sie auf der ausstellenden Zertifizierungsstelle das Zertifikatsvorlagen-Snap-In, um eine neue benutzerdefinierte Vorlage zu erstellen oder eine vorhandene Vorlage zu kopieren. Bearbeiten Sie dann eine vorhandene Vorlage (z. B. die Vorlage „Benutzer“) für die Verwendung mit NDES.

    Die Vorlage muss wie folgt konfiguriert sein:

    -   Geben Sie einen aussagekräftigen **Vorlagenanzeigenamen** für die Vorlage ein.

    -   Wählen Sie auf der Registerkarte **Antragstellername** die Option **Informationen werden in der Anforderung angegeben**. (Sicherheit wird durch das [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinienmodul für NDES erzwungen.)

    -   Stellen Sie sicher, dass auf der Registerkarte **Erweiterungen** die **Beschreibung der Anwendungsrichtlinien** die **Clientauthentifizierung** umfasst.

        > [!IMPORTANT]
        > Bearbeiten Sie für iOS-Zertifikatvorlagen auf der Registerkarte **Erweiterungen** die Option **Schlüsselverwendung**, und stellen Sie sicher, dass die Option **Signatur ist Ursprungsnachweis** nicht ausgewählt ist.

    -   Fügen Sie auf der Registerkarte **Sicherheit** das Dienstkonto für NDES hinzu, und weisen Sie der Vorlage Berechtigungen zum **Lesen** und **Registrieren** zu.

3.  Prüfen Sie auf der Registerkarte **Allgemein** die **Gültigkeitsdauer** der Vorlage. In der Standardeinstellung verwendet [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] den für die Vorlage konfigurierten Wert. Sie haben jedoch die Möglichkeit, die Zertifizierungsstelle so zu konfigurieren, dass dem Antragsteller ermöglicht wird, einen anderen Wert anzugeben, den Sie dann in der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungskonsole festlegen können. Wenn Sie immer den in der Vorlage festgelegten Wert verwenden möchten, überspringen Sie den Rest dieses Schritts.

    > [!IMPORTANT]
    > Die iOS-Plattform verwendet immer den in der Vorlage festgelegten Wert, unabhängig von anderen Konfigurationen, die Sie vornehmen.

    Um die Zertifizierungsstelle so zu konfigurieren, dass der Antragsteller die Gültigkeitsdauer festlegen kann, führen Sie auf der Zertifizierungsstelle die folgenden Befehle aus:

    1.  **certutil -setreg Policy\EditFlags +EDITF_ATTRIBUTEENDDATE**

    2.  **net stop certsvc**

    3.  **net start certsvc**

4.  Verwenden Sie auf der ausstellenden Zertifizierungsstelle das Zertifizierungsstellen-Snap-In, um die Zertifikatvorlage zu veröffentlichen.

    1.  Wählen Sie den Knoten **Zertifikatvorlagen**, klicken Sie auf **Aktion** &gt; **Neu** &gt; **Auszustellende Zertifikatvorlage**, und wählen Sie dann die Vorlage, die Sie in Schritt 2 erstellt haben.

    2.  Überprüfen Sie, ob die Vorlage veröffentlicht wurde, indem Sie sie im Ordner **Zertifikatvorlagen** anzeigen.

5.  Für PFX-Profile:  Stellen Sie auf dem Zertifizierungsstellencomputer sicher, dass der Computer, den Intune-Zertifikatconnector hostet, die Berechtigung "Registrieren" hat, damit dieser auf die Vorlage zugreifen kann, die zum Erstellen des PFX-Profils verwendet wurde. Legen Sie diese Berechtigung auf der Registerkarte **Sicherheit** in den Eigenschaften des Computers mit der Zertifizierungsstelle fest.

### <a name="BKMK_ConfigOnPremTask2"></a>Aufgabe 2 (nur für SCEP-Profile): Konfigurieren der erforderlichen Komponenten auf dem NDES-Server
Im Rahmen dieser Aufgabe führen Sie die folgenden Aktionen aus:

-   Hinzufügen von NDES zu einem Windows-Server und Konfigurieren von IIS zur Unterstützung von NDES

-   Hinzufügen des NDES-Dienstkontos zur Gruppe „IIS_IUSR“

-   Festlegen des SPN für das NDES-Dienstkonto

##### So konfigurieren Sie die Voraussetzungen für den NDES-Server

1.  Auf dem Server, der NDES hosten soll, müssen Sie sich als **Unternehmensadministrator** anmelden und dann den [Assistenten zum Hinzufügen von Rollen und Features](https://technet.microsoft.com/library/hh831809.aspx) zum Installieren von NDES verwenden:

    1.  Wählen Sie im Assistenten die Option **Active Directory-Zertifikatdienste**, um Zugriff auf die Rollendienste der AD-Zertifikatdienste zu erhalten. Wählen Sie die Option **Registrierungsdienst für Netzwerkgeräte**, deaktivieren Sie die Option **Zertifizierungsstelle**, und schließen Sie den Assistenten dann ab.

        > [!TIP]
        > Klicken Sie auf der Seite **Installationsvorgang** des Assistenten nicht auf **Schließen**. Klicken Sie stattdessen auf den Link **Active Directory-Zertifikatdienste auf dem Zielserver konfigurieren**. Daraufhin wird der Assistent zur **AD CS-Konfiguration** geöffnet, den Sie für die nächste Aufgabe verwenden. Nachdem der Assistent für die AD CS-Konfiguration geöffnet wurde, können Sie den Assistenten zum Hinzufügen von Rollen und Features schließen.

    2.  Wenn NDES zum Server hinzugefügt wird, installiert der Assistent ebenfalls IIS. Stellen Sie sicher, dass IIS wie folgt konfiguriert ist:

        -   **Webserver** &gt; **Sicherheit** &gt; **Anforderungsfilterung**

        -   **Webserver** &gt; **Anwendungsbereitstellung** &gt; **ASP.NET 3.5**. Bei der Installation von ASP.NET 3,5 wird .NET Framework 3,5 installiert. Installieren Sie bei Installation von .NET Framework 3.5 sowohl das Feature **.NET Framework 3.5** als auch die **HTTP-Aktivierung**.

        -   **Webserver** &gt; **Anwendungsbereitstellung** &gt; **ASP.NET 4.5**. Bei der Installation von ASP.NET 4.5 wird .NET Framework 4.5 installiert. Installieren Sie bei der Installation von .NET Framework 4.5 das Kernfeature **.NET Framework 4.5**, das Feature **ASP.NET 4.5** und das Feature **WCF-Dienste** &gt; **HTTP-Aktivierung**.

        -   **Verwaltungstools** &gt; **IIS 6-Verwaltungskompatibilität** &gt; **IIS 6-Metabasiskompatibilität**

        -   **Verwaltungstools** &gt; **IIS 6-Verwaltungskompatibilität** &gt; **IIS 6-WMI-Kompatibilität**

2.  Fügen Sie auf dem Server das NDES-Dienstkonto als Mitglied der Gruppe **IIS_IUSR** hinzu.

3.  Führen Sie den folgenden Befehl aus, um den SPN des NDES-Dienstkontos festzulegen:

    -   **setspn -s http/&lt;DNS-Name des NDES-Servers&gt; &lt;Domänenname&gt;\&lt;NDES-Dienstkontoname&gt;**

    Wenn der NDES-Server zum Beispiel den Namen **Server01** hat, die Domäne **Contoso.com** ist und das Dienstkonto **NDESService** lautet, verwenden Sie Folgendes:

    -   **setspn –s http/Server01.contoso.com contoso\NDESService**

### <a name="BKMK_ConfigOnPremTask3"></a>Aufgabe 3 (nur für SCEP-Profile): Konfigurieren von NDES für die Verwendung mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]
Im Rahmen dieser Aufgabe führen Sie die folgenden Aktionen aus:

-   Konfigurieren von NDES für die Verwendung mit der ausstellenden Zertifizierungsstelle

-   Binden des Serverauthentifizierungszertifikats (SSL) in IIS

-   Konfigurieren der Anforderungsfilterung in IIS

##### So konfigurieren Sie NDES für die Verwendung mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

1.  Öffnen Sie auf dem NDES-Server den AD CS-Konfigurations-Assistenten, und nehmen Sie dann die folgenden Konfigurationen vor.

    > [!TIP]
    > Dieser Assistent ist bereits geöffnet, wenn Sie in der vorherigen Aufgabe auf den Link geklickt haben. Andernfalls öffnen Sie den Server-Manager, um auf die Konfiguration nach der Bereitstellung der Active Directory-Zertifikatdienste zuzugreifen.

    -   Wählen Sie auf der Seite **Rollendienste** die Option **Registrierungsdienst für Netzwerkgeräte**.

    -   Geben Sie auf der Seite **Dienstkonto für NDES** das NDES-Dienstkonto an.

    -   Klicken Sie auf der Seite **ZS für NDES** auf **Auswählen**, und wählen Sie dann die ausstellende Zertifizierungsstelle aus, auf der Sie die Zertifikatvorlage konfiguriert haben.

    -   Legen Sie auf der Seite **Kryptografie für NDES** die Schlüssellänge entsprechend den Anforderungen Ihres Unternehmens fest.

    Klicken Sie auf der Seite **Bestätigung** auf **Konfigurieren**, um den Assistenten zu beenden.

2.  Bearbeiten Sie nach Beendigung des Assistenten den folgenden Registrierungsschlüssel auf dem NDES-Server:

    -   **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Cryptography\MSCEP\**

    Um diesen Schlüssel zu bearbeiten, ermitteln Sie den **Zweck** der Zertifikatvorlage, wie auf der entsprechenden Registerkarte **Anforderungsverarbeitung** aufgeführt, und bearbeiten Sie dann den zugehörigen Eintrag in der Registrierung. Ersetzen Sie hierzu die vorhandenen Daten durch den Namen der Zertifikatvorlage (nicht den Anzeigenamen der Vorlage), den Sie in Aufgabe 1 festgelegt haben.  In der folgenden Tabelle ist der Zertifikatvorlagenzweck den Werten in der Registrierung zugeordnet:

    |Zertifikatvorlagenzweck (auf der Registerkarte „Anforderungsverarbeitung“)|Zu bearbeitender Registrierungswert|In der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungskonsole für das SCEP-Profil angezeigter Wert|
    |------------------------------------------------------------------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
    |-   Signatur|-   SignatureTemplate|-   Digitale Signatur|
    |-   Verschlüsselung|-   EncryptionTemplate|-   Schlüsselverschlüsselung|
    |-   Signatur und Verschlüsselung|-   GeneralPurposeTemplate|-   Schlüsselverschlüsselung<br />-   Digitale Signatur|
    Wenn der Zweck der Zertifizierungsvorlage zum Beispiel **Verschlüsselung** ist, bearbeiten Sie den Wert **EncryptionTemplate** so, dass er dem Namen der Zertifikatvorlage entspricht.

3.  Führen Sie nach dem Bearbeiten der Registrierung **iisreset** auf dem Server aus, um zu erzwingen, dass der Server die aktuellen Konfigurationsänderungen übernimmt.

##### So installieren und binden Sie Zertifikate auf dem NDES-Server

1.  Fordern Sie auf dem NDES-Server ein **Serverauthentifizierungszertifikat** von der internen oder einer öffentlichen Zertifizierungsstelle an, und installieren Sie es. Sie binden dieses SSL-Zertifikat anschließend in IIS.

    > [!TIP]
    > Nachdem Sie das SSL-Zertifikat in IIS gebunden haben, installieren Sie auch ein Clientauthentifizierungszertifikat. Dieses Zertifikat kann von jeder Zertifizierungsstelle ausgestellt werden, die vom NDES-Server als vertrauenswürdig eingestuft wird. Obwohl es sich nicht um die bewährte Methode handelt, können Sie das gleiche Zertifikat für die Server und die Clientauthentifizierung verwenden, solange das Zertifikat über beide erweiterten Schlüsselverwendungen (EKUs) verfügt. In den folgenden Schritten finden Sie Informationen zu diesen Authentifizierungszertifikaten.

    1.  Nachdem Sie das Serverauthentifizierungszertifikat erhalten haben, öffnen Sie den **IIS-Manager**, wählen im Fenster **Verbindungen** die Option **Standardwebsite**, und klicken dann im Fenster **Aktionen** auf **Bindungen**.

    2.  Klicken Sie auf **Hinzufügen**, legen Sie als **Typ** die Option **https** fest, und stellen Sie sicher, dass der Port **443** ist. (Für eigenständige [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] wird nur Port 443 unterstützt.)

    3.  Geben Sie unter **SSL-Zertifikat** das Serverauthentifizierungszertifikat an.

        > [!NOTE]
        > Wenn der NDES-Server sowohl einen externen als auch einen internen Namen für eine einzelne Netzwerkadresse verwendet, muss das Serverauthentifizierungszertifikat über einen **Antragstellernamen** mit einem externen öffentlichen Servernamen sowie einen **alternativen Antragstellernamen** verfügen, der den Namen des internen Servers enthält.

2.  Fordern Sie auf dem NDES-Server ein **Clientauthentifizierungszertifikat** von der internen oder einer öffentlichen Zertifizierungsstelle an, und installieren Sie es. Dies kann dasselbe Zertifikat wie das Serverauthentifizierungszertifikat sein, wenn dieses Zertifikat über beide Funktionen verfügt.

    Das Clientauthentifizierungszertifikat muss die folgenden Eigenschaften aufweisen:

    -   **Erweiterte Schlüsselverwendung**: Dies muss die **Clientauthentifizierung** umfassen.

    -   **Antragstellername**: Dies muss mit dem DNS-Namen des Servers identisch sein, auf dem das Zertifikat installiert wird (d. h. dem NDES-Server).

##### So konfigurieren Sie die IIS-Anforderungsfilterung

1.  Öffnen Sie auf dem NDES-Server den **IIS-Manager**, wählen Sie im Fenster **Verbindungen** die Option **Standardwebsite**, und öffnen Sie dann die **Anforderungsfilterung**.

2.  Klicken Sie auf **Featureeinstellungen bearbeiten**, und legen Sie dann Folgendes fest:

    -   **Abfragezeichenfolge (Bytes)** = **65534**

    -   **Maximale URL-Länge (Bytes)** = **65534**

3.  Überprüfen Sie den folgenden Registrierungsschlüssel:

    -   **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\HTTP\Parameters**

    Stellen Sie sicher, dass die folgenden Werte als DWORD-Einträge festgelegt sind:

    -   Name: **MaxFieldLength** mit einem Dezimalwert von **65534**

    -   Name: **MaxRequestBytes** mit einem Dezimalwert von **65534**

4.  Starten Sie den NDES-Server neu. Der Server ist jetzt bereit zur Unterstützung des Zertifikatconnectors.

### <a name="BKMK_ConfigOnPremTask4"></a>Aufgabe 4: Aktivieren, Installieren und Konfigurieren des Intune-Zertifikatconnectors: Für SCEP- und PFX-Zertifikate.
Im Rahmen dieser Aufgabe führen Sie die folgenden Aktionen aus:

-   Aktivieren der Unterstützung für NDES in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

-   Herunterladen, Installieren und Konfigurieren des Zertifikatconnectors auf dem NDES-Server

##### So aktivieren Sie die Unterstützung für den Zertifikatconnector

1.  Öffnen Sie die [Intune-Verwaltungskonsole](https://manage.microsoft.com), und klicken Sie auf **Verwaltung** &gt; **Zertifikatconnector**.

2.  Klicken Sie auf **Lokalen Zertifikatconnector konfigurieren**.

3.  Wählen Sie **Zertifikatconnector aktivieren** aus, und klicken Sie dann auf **OK**.

##### So wird der Zertifikatconnector heruntergeladen, installiert und konfiguriert

1.  Öffnen Sie die [Intune-Verwaltungskonsole](https://manage.microsoft.com), und klicken Sie dann auf **Admin** &gt; **Verwaltung von Mobilgeräten** &gt; **Zertifikatconnector** &gt; **Zertifikatconnector herunterladen**.

2.  Nachdem der Download abgeschlossen ist, führen Sie das heruntergeladene Installationsprogramm (**ndesconnectorssetup.exe**) aus:

    -   Führen Sie für PFX-Zertifikate das Installationsprogramm auf dem Computer aus, der eine Verbindung mit der Zertifizierungsstelle herstellen kann. Wählen Sie die Option „PFX-Verteilung“ aus, und klicken Sie auf „Installieren“. Fahren Sie nach Abschluss der Installation mit dem Erstellen eines Zertifikatprofils fort.

    -   Führen Sie für SCEP-Zertifikate das Installationsprogramm auf einem Server mit Windows Server 2012 R2 aus.

    Bei der Option "SCEP" installiert das Installationsprogramm auch das Richtlinienmodul für NDES und der CRP-Webdienst. (Der CRP-Webdienst „CertificateRegistrationSvc“ wird als Anwendung in IIS ausgeführt.)

    > [!NOTE]
    > Bei der Installation von NDES für eigenständiges [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] wird der CRP-Dienst automatisch mit dem Zertifikatconnector installiert. Bei Verwendung von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] mit dem Konfigurations-Manager installieren Sie den Zertifikatregistrierungspunkt als eine separate Standortsystemrolle.

3.  Wenn Sie zur Eingabe des Clientzertifikats für den Zertifikatconnector aufgefordert werden, klicken Sie auf **Auswählen**, und wählen Sie das **Clientauthentifizierungszertifikat** aus, das Sie in Aufgabe 3 auf dem NDES-Server installiert haben.

    Nachdem Sie das Clientauthentifizierungszertifikat ausgewählt haben, wird erneut die Oberfläche **Clientzertifikat für den Microsoft Intune-Zertifikatconnector** angezeigt. Auch wenn das ausgewählte Zertifikat nicht angezeigt wird, klicken Sie auf **Weiter**, um die Eigenschaften des Zertifikats anzuzeigen. Klicken Sie dann auf **Weiter**, und klicken Sie anschließend auf **installieren**.

4.  Nach Abschluss des Assistenten, jedoch vor dem Schließen des Assistenten, klicken Sie auf **Zertifikatconnector-Benutzeroberfläche starten**.

    > [!TIP]
    > Wenn Sie den Assistenten schließen, bevor Sie die Benutzeroberfläche des Zertifikatconnectors starten, können Sie sie mit dem folgenden Befehl erneut öffnen:
    > 
    > -   **&lt;Installationspfad&gt;\NDESConnectorUI\NDESConnectorUI.exe**

5.  Gehen Sie auf der Benutzeroberfläche von **Zertifikatconnector** so vor:

    -   Klicken Sie auf **Anmelden**, und geben Sie Ihre [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienstadministrator-Anmeldeinformationen oder Anmeldeinformationen für einen Mandantenadministrator mit der globalen Administratorberechtigung ein.

    -   Wenn Ihre Organisation einen Proxyserver verwendet und der Proxy erforderlich ist, damit der NDES-Server auf das Internet zugreifen kann, klicken Sie auf **Proxyserver verwenden**, und geben Sie dann den Proxyservernamen, Port und die Kontoanmeldedaten für die Verbindung an.

    -   Wählen Sie die Registerkarte **Erweitert** aus, und geben Sie dann die Anmeldeinformationen für ein Konto ein, das über die Berechtigung **Zertifikate ausgeben und verwalten** für die ausstellende Zertifizierungsstelle verfügt, und klicken Sie dann auf **Anwenden**.

    Sie können jetzt die Benutzeroberfläche des Zertifikatconnectors schließen.

6.  Öffnen Sie eine Eingabeaufforderung, und geben Sie **services.msc** ein. Drücken Sie dann die **EINGABETASTE**, klicken Sie mit der rechten Maustaste auf **Zertifikatconnectordienst**, und klicken Sie dann auf **Neu starten**.

Um zu überprüfen, das der Dienst ausgeführt wird, öffnen Sie einen Browser, und geben Sie die folgenden URL ein. Es sollte ein **403**-Fehler zurückgegeben werden:

-   **http:// &lt;FQDN_Ihres_NDES-Servers&gt;/certsrv/mscep/mscep.dll**

Jetzt können Sie Zertifikatprofile konfigurieren.

## <a name="BKMK_ConfigProfiles"></a>Konfigurieren von Zertifikatprofilen
Nachdem Sie Ihre Infrastruktur und Zertifikate konfiguriert haben, können Sie Zertifikatprofile konfigurieren:

**Aufgabe 1**: Exportieren des vertrauenswürdigen Stammzertifizierungsstellenzertifikats 
**Aufgabe 2**: Erstellen von Zertifikatprofilen der vertrauenswürdigen Zertifizierungsstelle 
**Aufgabe 3**: Eine der Optionen:

-   Erstellen von SCEP-Zertifikatprofilen

-   Erstellen von PFX-Zertifikatprofilen

### <a name="BKMK_ConfigExportRootCA"></a>Aufgabe 1: Exportieren des vertrauenswürdigen Stammzertifizierungsstellenzertifikats
Exportieren Sie das vertrauenswürdige Stammzertifizierungsstellenzertifikat als eine **CER**-Datei von der ausstellenden Zertifizierungsstelle oder von einem Gerät, das die ausstellenden Zertifizierungsstelle als vertrauenswürdig erachtet. Sie exportieren den privaten Schlüssel nicht.

Sie importieren dieses Zertifikat, wenn Sie ein Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle konfigurieren.

### <a name="BKMK_ConfigRootCA"></a>Aufgabe 2: Erstellen von Zertifikatprofilen der vertrauenswürdigen Zertifizierungsstelle
Sie müssen ein **Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle** erstellen, bevor Sie ein Profil für **Einstellungen für Simple Certificate Enrollment Protocol** (SCEP, Registrierungsdienst für Netzwerkgeräte) erstellen können. Beide Profile sind für alle mobilen Geräteplattformen erforderlich.

##### So erstellen Sie ein vertrauenswürdiges Zertifikatprofil

1.  Öffnen Sie die [Intune-Verwaltungskonsole](https://manage.microsoft.com), und klicken Sie auf **Richtlinie** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie einen der folgenden Richtlinientypen:

    -   **Android &gt; Profil des vertrauenswürdigen Zertifikats (Android 4 und höher)**

    -   **iOS &gt; Profil des vertrauenswürdigen Zertifikats (iOS 5 und höher)**

    -   **Windows Phone und registrierte Windows-Geräte &gt; Profil des vertrauenswürdigen Zertifikats (Windows 8.1 und höher)**

    -   **Windows Phone und registrierte Windows-Geräte &gt; Profil des vertrauenswürdigen Zertifikats (Windows Phone 8.1 und höher)**

    Erfahren Sie mehr: [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Verwenden Sie die folgenden Informationen, um die Profileinstellungen vertrauenswürdiger Zertifikate für Android, iOS, Windows 8.1 oder Windows Phone 8.1 zu konfigurieren:

    |Name der Einstellung|Plattform|Weitere Informationen|
    |------------------------|-------------|-------------------------|
    |**Name**|All|Geben Sie einen aussagekräftigen Namen für das Zertifikatprofil ein.|
    |**Beschreibung**|All|Geben Sie eine optionale Beschreibung für das Zertifikat ein.|
    |**Zertifikatdatei**|All|Klicken Sie auf **Importieren**, und wählen Sie dann das vertrauenswürdige Stammzertifizierungsstellenzertifikat (**.cer**) aus, das Sie von der ausstellenden Zertifizierungsstelle exportiert haben.|
    |**Zielspeicher**|Windows 8.1|Wählen Sie für Geräte, die mehr als einen Zertifikatspeicher haben, den Speicherort des Zertifikats aus. Wählen Sie aus unter:<br /><br />-   **Computerzertifikatspeicher – Stamm**<br />-   **Computerzertifikatspeicher – Zwischenspeicher**<br />-   **Benutzerzertifikatspeicher – Zwischenspeicher**<br /><br />Bei Geräten, die nur einen Speicher haben, wird diese Einstellung ignoriert.|

4.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Arbeitsbereich **Richtlinie** angezeigt und kann nun bereitgestellt werden.

### <a name="BKMK_ConfigSCEP"></a>Aufgabe 3: Erstellen von SCEP- oder PFX-Zertifikatprofilen
Nachdem Sie ein Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle erstellt haben, erstellen Sie SCEP- oder PFX-Zertifikatprofile für jede Plattform, die Sie verwenden möchten. Wenn Sie ein SCEP-Zertifikatprofil erstellen, müssen Sie ein Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle für dieselbe Plattform angeben. Auf diese Weise werden die beiden Zertifikatprofile verknüpft. Sie müssen jedoch weiterhin jedes Profil separat bereitstellen.

##### Erstellen eines SCEP-Zertifikatprofils

1.  Klicken Sie in der [Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie einen der folgenden Richtlinientypen:

    -   **Android &gt; SCEP-Zertifikatprofil (Android 4 und höher)**

    -   **iOS &gt; SCEP-Zertifikatprofil (iOS 5 und höher)**

    -   **Windows Phone und registrierte Windows-Geräte &gt; SCEP-Zertifikatprofil (Windows 8.1 und höher)**

    -   **Windows Phone und registrierte Windows-Geräte &gt; SCEP-Zertifikatprofil (Windows Phone 8.1 und höher)**

    Erfahren Sie mehr: [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Verwenden Sie die folgenden Informationen, um die SCEP-Zertifikatprofileinstellungen für Android, iOS, Windows 8.1 oder Windows Phone 8.1 zu konfigurieren:

    |Name der Einstellung|Plattform|Weitere Informationen|
    |------------------------|-------------|-------------------------|
    |**Name**|All|Geben Sie einen aussagekräftigen Namen für das Zertifikatprofil ein.|
    |**Beschreibung**|All|Geben Sie eine optionale Beschreibung für das Zertifikat ein.|
    |**Erneuerungsschwellenwert (%)**|All|Geben Sie den Prozentsatz der Zertifikatgültigkeitsdauer an, die verbleibt, bevor das Gerät eine Erneuerung des Zertifikats anfordert.|
    |**Schlüsselspeicheranbieter (KSP)**|Android <br />Windows 8.1 <br />Windows Phone 8.1|Geben Sie an, wo der Schlüssel für das Zertifikat gespeichert wird. Wählen Sie eine der folgenden Optionen:<br /><br />-   **Auf Trusted Platform Module (TPM) installieren, falls vorhanden** - Installiert den Schlüssel auf dem TPM. Wenn das TPM nicht vorhanden ist, wird der Schlüssel im Speicheranbieter für den Softwareschlüssel installiert.<br />-   **Auf Trusted Platform Module (TPM) installieren, andernfalls Fehler** - Installiert den Schlüssel auf dem TPM. Wenn das TPM-Modul nicht vorhanden ist, tritt ein Fehler bei der Installation auf.<br />-   **Im Softwareschlüsselspeicher-Anbieter installieren** - Installiert den Schlüssel im Speicheranbieter für den Softwareschlüssel.|
    |**SCEP-Server-URL**|All|Geben Sie eine URL (mit dem Präfix **http://** oder **https://**) ein, und klicken Sie dann auf **Hinzufügen**, oder wählen Sie eine URL, und klicken Sie dann auf **Löschen**.<br /><br />Eine SCEP-Server-URL kann beispielsweise wie folgt aussehen: **https://mdmndes1.contoso.com/certsrv/mscep/mscep.dll**<br /><br />Jedes SCEP-Profil unterstützt eine einzelne SCEP-Server-URL.|
    |**Format des Antragstellernamens**|Android <br />Windows 8.1 <br />Windows Phone 8.1|Wählen Sie in der Liste aus, wie [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] den Antragstellernamen in der Zertifikatanforderung automatisch erstellt. Wenn das Zertifikat für einen Benutzer bestimmt ist, können Sie auch die E-Mail-Adresse des Benutzers im Antragstellernamen einschließen.<br /><br />Wählen Sie **Allgemeiner Name** oder **Allgemeiner Name und E-Mail-Adresse**.|
    |**Alternativer Antragstellername**|All|Wählen Sie **E-Mail-Adresse**, **Benutzerprinzipalname (UPN)** oder beides aus.|
    |**Gültigkeitsdauer des Zertifikats**|All|Geben Sie die Zeitdauer vor Ablauf des Zertifikats an.|
    |**Schlüsselverwendung**|All|Geben Sie Schlüsselverwendungsoptionen für das Zertifikat an. Sie können unter folgenden Optionen wählen:<br /><br />-   **Digitale Signatur** (SignatureTemplate): zum digitalen Signieren von Daten<br />-   **Schlüsselverschlüsselung** (EncryptionTemplate): für die Verschlüsselung<br />-   **Schlüsselverschlüsselung + digitale Signatur** (GeneralPurposeTemplate): zum digitalen Signieren und für die Verschlüsselung|
    |**Schlüsselgröße (Bit)**|All|Wählen Sie die Größe des Schlüssels in Bits aus, wie vom Ihren Gerät unterstützt.<br /><br />Wählen Sie **1024** oder **2048**.|
    |**Hash-Algorithmus**|Android <br />Windows 8.1 <br />Windows Phone 8.1|Wählen Sie einen der verfügbaren Hashalgorithmustypen, der für dieses Zertifikat verwendet werden soll. Wählen Sie die höchste Sicherheitsebene aus, die die verbundenen Geräten unterstützen.<br /><br />Wählen Sie **SHA-1**, **SHA-2** oder beides.|
    |**Erweiterte Schlüsselverwendung**|All|Klicken Sie auf **Auswählen**, um Werte für den beabsichtigten Zweck des das Zertifikats hinzuzufügen. In den meisten Fällen erfordert das Zertifikat **Clientauthentifizierung**, damit der Benutzer bzw. das Gerät auf einem Server authentifiziert werden kann. Sie können jedoch nach Bedarf weitere Schlüsselverwendungen hinzufügen.|
    |**Auswählen des Stammzertifikats**|All|Klicken Sie auf **Auswählen**, um ein Profil für ein Stamm-Zertifizierungsstellenzertifikat auszuwählen, das Sie zuvor konfiguriert und für den Benutzer oder das Gerät bereitgestellt haben. Dieses Zertifizierungsstellenzertifikat muss das Stammzertifikat für die Zertifizierungsstelle sein, die das Zertifikat ausstellt, das Sie in diesem Zertifikatprofil konfigurieren.|

4.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Arbeitsbereich **Richtlinie** angezeigt und kann nun bereitgestellt werden.

##### So erstellen Sie ein PFX-Zertifikatprofil

1.  Klicken Sie in der [Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie einen der folgenden Richtlinientypen:

    -   **Android &gt; PFX-Zertifikatprofil (Android 4 und höher)**

    -   **Windows Phone und registrierte Windows-Geräte &gt; PFX-Zertifikatprofil (Windows 10 und höher)**

    -   **Windows Phone und registrierte Windows-Geräte &gt; PFX-Zertifikatprofil (Windows Phone 10 und höher)**

    Erfahren Sie mehr: [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Verwenden Sie die folgenden Informationen, um die PFX-Zertifikatprofileinstellungen für Android, iOS, Windows 10 oder Windows Phone 10 zu konfigurieren:

    |Name der Einstellung|Plattform|Weitere Informationen|
    |------------------------|-------------|-------------------------|
    |**Name**|Android <br />Windows 10 <br />Windows Phone 10|Geben Sie einen aussagekräftigen Namen für das Zertifikatprofil ein.|
    |**Beschreibung**|Android <br />Windows 10 <br />Windows Phone 10|Geben Sie eine optionale Beschreibung für das Zertifikat ein.|
    |**Erneuerungsschwellenwert (%)**|Android <br />Windows 10 <br />Windows Phone 10|Geben Sie den Prozentsatz der Zertifikatgültigkeitsdauer an, die verbleibt, bevor das Gerät eine Erneuerung des Zertifikats anfordert.|
    |**Zertifizierungsstelle**|Android <br />Windows 10 <br />Windows Phone 10|Geben Sie den vollqualifizierten Domänennamen der Zertifizierungsstelle an, z. B. *device.certs.contoso.com*.|
    |**Name der Zertifizierungsstelle**|Android <br />Windows 10 <br />Windows Phone 10|Geben Sie den vollqualifizierten Domänennamen der Zertifizierungsstelle an, z. B. *device-contoso-CA*.|
    |**Name der Zertifikatvorlage**|Android <br />Windows 10 <br />Windows Phone 10|Geben Sie den Namen der Zertifikatvorlage an (nicht den Anzeigenamen).|
    |**Format des Antragstellernamens**|Android <br />Windows 10 <br />Windows Phone 10|Geben Sie ein Format des Antragstellernamens aus den angegebenen Optionen an:<br /><br />-   Allgemeiner Name<br />-   Allgemeiner Name und E-Mail-Adresse|
    |**Alternativer Antragstellername**|Android <br />Windows 10 <br />Windows Phone 10|Wählen Sie die alternativen Antragstellernamen.|
    |**Gültigkeitsdauer des Zertifikats**|Android <br />Windows 10 <br />Windows Phone 10|Geben Sie die Zeitdauer vor Ablauf des Zertifikats an.|

4.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Arbeitsbereich **Richtlinie** angezeigt und kann nun bereitgestellt werden.

## <a name="BKMK_Deploy"></a>Bereitstellen von Zertifikatprofilen
Wenn Sie Zertifikatprofile bereitstellen, wird die Zertifikatdatei aus dem Zertifikatprofil der vertrauenswürdigen Zertifizierungsstelle auf Geräten installiert. Das SCEP- oder PFX-Zertifikatprofil wird vom Gerät verwendet, um eine Zertifikatsanforderung zu erstellen.

Zertifikatprofile werden nur auf den Geräten installiert, die der beim Erstellen des Profils verwendeten Plattform entsprechen.

-   Sie können Zertifikatprofile für Benutzer- oder Gerätesammlungen bereitstellen.

    > [!TIP]
    > Damit Zertifikate möglichst schnell auf Geräten nach deren Registrierung veröffentlicht werden können, stellen Sie dieses Zertifikatprofil für eine Benutzergruppe (nicht für eine Gerätegruppe) bereit. Wenn Sie es für eine Gerätegruppe bereitstellen, muss eine vollständige Geräteregistrierung stattfinden, bevor das Gerät die Richtlinie empfängt.

-   Obwohl jedes Profil einzeln bereitgestellt wird, muss sowohl das vertrauenswürdige Stamm- als auch das SCEP/PFX-Profil bereitgestellt werden, da bei der SCEP/PFX-Zertifikatrichtlinie sonst ein Fehler auftritt.

Sie stellen Zertifikatprofile auf die gleiche Weise bereit wie andere Richtlinien für [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Informationen über das Bereitstellen und Verwalten von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

## Siehe auch
[Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

