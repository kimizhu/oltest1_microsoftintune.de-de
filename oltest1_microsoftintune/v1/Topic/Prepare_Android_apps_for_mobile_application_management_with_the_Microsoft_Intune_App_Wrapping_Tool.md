---
description: na
keywords: na
title: Prepare Android apps for mobile application management with the Microsoft Intune App Wrapping Tool
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9c349c8-51ae-4d73-b74a-6173728a520b
---
# Vorbereiten von Android-Apps f&#252;r die Verwaltung von mobilen Anwendungen mit dem Microsoft Intune App Wrapper-Tool
Verwenden Sie das **Microsoft Intune App Wrapping Tool für Android** zur Steuerung des Verhaltens von internen Android-Apps, um die Funktionen von Apps zu konfigurieren, ohne den Code der eigentlichen App zu ändern.

Das Tool ist eine Windows-Befehlszeilenanwendung, die in PowerShell ausgeführt wird und einen Wrapper um die App erstellt. Sobald die App verarbeitet wurde, können Sie ihre Funktionalität mit einer [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungsrichtlinie für mobile Anwendungen ändern (siehe [Schützen von Daten mithilfe der Verwaltungsrichtlinien für mobile Anwendungen mit Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md)).

Wenn Azure Active Directory Authentication Library (ADAL) von Ihrer App verwendet wird, führen Sie die Schritte unter [Wrappen von Apps, die Azure Active Directory Library (ADAL) verwenden](#BKMK_ADAL_android) aus, bevor Sie Ihre App wrappen. Wenn Sie nicht wissen, ob Ihre Anwendung diese Bibliothek verwendet, wenden Sie sich an den Entwickler der Anwendung.

Lesen Sie vor dem Ausführen des Tools unter [Sicherheitsüberlegungen für das Ausführen des App Wrapping Tools](../Topic/Prepare_Android_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md#BKMK_androidappwraptool). Informationen zum Herunterladen des Tools finden Sie unter [Microsoft Intune App Wrapping Tool für Android](http://www.microsoft.com/en-us/download/details.aspx?id=47267).

## Schritt 1: Erfüllen Sie die Voraussetzungen zur Verwendung des App Wrapping Tools.

-   Sie müssen das App Wrapping Tool auf einem Windows-Computer unter Windows 7 oder höher ausführen.

-   Die Eingabe-App muss ein gültiges Android-Anwendungspaket mit der Dateierweiterung **.apk** sein und folgende Kriterien aufweisen:

    -   Kann nicht verschlüsselt werden

    -   Darf nicht bereits vom App Wrapping Tool umschlossen sein

    -   Muss für Android 4.0 oder höher geschrieben sein

-   Die App muss von Ihrem oder für Ihr Unternehmen entwickelt werden. Mit diesem Tool können Sie keine von Google Play Store heruntergeladenen Apps bearbeiten.

-   Um das App Wrapping Tool auszuführen, müssen Sie die neueste Version der [Java-Laufzeitumgebung](http://java.com/download/) installieren und sicherstellen, dass die Java-Pfadvariable in den Windows-Umgebungsvariablen auf **C:\ProgramData\Oracle\Java\javapath** festgelegt wurde. Weitere Informationen finden Sie in der [Java-Dokumentation](http://java.com/download/help/).

    > [!NOTE]
    > In einigen Fällen kann die 32-Bit-Version von Java zu Speicherproblemen führen. Es wird empfohlen, stattdessen die 64-Bit-Version zu installieren.

## Schritt 2: Installieren Sie das App Wrapping Tool.

#### Installieren des App Wrapping Tools

1.  Laden Sie die Installationsdatei für das App Wrapping Tool aus dem Microsoft Download Center herunter, und öffnen Sie sie auf einem Windows-Computer.

2.  Akzeptieren Sie den Lizenzvertrag, und schließen Sie die Installation ab.

Merken Sie sich den Ordner, in dem Sie das Tool installieren. Der Standardspeicherort istt: **C:\Programme (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool**.

## Schritt 3: Führen Sie das App Wrapping Tool aus.

1.  Öffnen Sie auf dem Windows-Computer, auf dem Sie das App Wrapping Tool installiert haben, ein PowerShell-Fenster.

2.  Importieren Sie aus dem Ordner, in dem Sie das Tool installiert haben, das PowerShell-Modul des App Wrapping Tools:

    ```
    Import-Module .\IntuneAppWrappingTool.psm1
    ```

3.  Führen Sie das Tool mithilfe des Befehls **invoke-AppWrappingTool** gemeinsam mit den folgenden Parametern aus. Parameter, die als "optional" markiert sind, sind für Apps bestimmt, die Azure Active Directory Library (ADAL) verwenden. Weitere Informationen finden Sie unter [Wrappen von Apps, die Azure Active Directory Library (ADAL) verwenden](#BKMK_ADAL_android).

    |Parameter|Weitere Informationen|
    |-------------|-------------------------|
    |**- InputPath** *&lt;Zeichenfolge&gt;*|Pfad der Android-Quelle-App (.apk).|
    |**- OutputPath** *&lt;Zeichenfolge&gt;*|Pfad zur Android-"Ausgabe"-App. Ist dies der gleiche Verzeichnispfad wie InputPath, schlägt das Verpacken fehl.|
    |**- KeyStorePath** *&lt;Zeichenfolge&gt;*|Pfad zur KeyStore-Datei, die das Öffentlich/Privat-Schlüsselpaar für die Signierung enthält.|
    |**- KeyStorePassword** *&lt;SecureString&gt;*|Das Kennwort zum Entschlüsseln des KeyStore.|
    |**-KeyAlias** *&lt;Zeichenfolge&gt;*|Der Name des Schlüssels, der zum Signieren verwendet werden soll.|
    |**-KeyPassword** *&lt;SecureString&gt;*|Das Kennwort zum Entschlüsseln des privaten Schlüssels, der zum Signieren verwendet wird.|
    |**-SigAlg** *&lt;SecureString&gt;*|Der Name des Signaturalgorithmus, der zum Signieren verwendet werden soll. Der Algorithmus muss mit dem privaten Schlüssel kompatibel sein.<br /><br />Beispiele: SHA256withRSA, SHA1withRSA, MD5withRSA|
    |**-ClientID** *&lt;GUID&gt;*|Azure Active Directory-Client-ID der Eingabe-App (optional).|
    |**- AuthorityURI** *&lt;URI&gt;*|Azure Active Directory-Registrierungsstellen-URI der Eingabe-App (optional).|
    |**- SkipBroker** *&lt;Boolesch&gt;*|Gibt an, ob die Eingabeanwendung geräteweites vermitteltes einmaliges Anmelden (Single Sign-On, SSO) unterstützt (optional).<br /><br />-   True – Die Eingabeanwendung unterstützt kein geräteweites vermitteltes SSO. Verwenden Sie den Parameter "NonBrokerRedirectURI".<br />-   False – Die Eingabeanwendung unterstützt geräteweites vermitteltes SSO.|
    |**-NonBrokerRedirectURI** *&lt;URI&gt;*|Der Azure Active Directory-Umleitungs-URI, der verwendet werden soll, wenn SkipBroker "true" ist (optional).|
    |*&lt;Allgemeineparameter&gt;*|(optional – unterstützt allgemeine PowerShell-Parameter wie verbose, debug usw.)<br /><br />Eine Liste der allgemeinen Parameter finden Sie im [Microsoft Script Center](https://technet.microsoft.com/library/hh847884.aspx).|
    Um die Hilfe für das Tool anzuzeigen, geben Sie folgenden Befehl ein:

    ```
    Help Invoke-AppWrappingTool
    ```
    Weitere Informationen zur Integration von Azure Active Directory (AAD) finden Sie [hier](https://technet.microsoft.com/library/dn878028.aspx).

    **Beispiel:**

    ```
    Import-Module "C:\Program Files (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool\IntuneAppWrappingTool.psm1" Invoke-AppWrappingTool –InputPath <input-app.apk> -OutputPath <output-app.apk> -KeyStorePath <path-to-signing.keystore> -KeyAlias <signing-key-name> -ClientID <xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx> -AuthorityURI <http://AzureActivieDirectory.Authority.URL> -SkipBroker<$True|$False> -NonBrokerRedirectURI <urn:xxx:xx:xxxx:xx:xxx>
    ```
    Anschließend werden Sie zur Eingabe des **KeyStorePassword** und **KeyPassword** aufgefordert.

Die umschlossene App wird generiert und zusammen mit einer Protokolldatei in dem von Ihnen angegebenen Ausgabepfad gespeichert.

## <a name="BKMK_androidappwraptool"></a>Sicherheitsüberlegungen für das Ausführen des App Wrapping Tools
So verhindern Sie ein mögliches Spoofing, das Offenlegen von Informationen und Angriffe durch Rechteerweiterungen:

-   Stellen Sie sicher, dass sich die Branchenanwendung für die Eingabe, die Ausgabeanwendung und Java KeyStore auf demselben Computer befinden, auf dem auch das App Wrapping Tool ausgeführt wird.

-   Importieren Sie die Ausgabeanwendung in die Intune-Konsole auf demselben Computer, auf dem das Tool ausgeführt wird.

-   Wenn sich die Ausgabenanwendung und das Tool in einem Universal Naming Convention (UNC)-Pfad befinden und Sie das Tool und die Eingabedateien nicht auf demselben Computer ausführen, schützen Sie die Umgebung, indem Sie [Internet Protocol Security (IPsec)](http://en.wikipedia.org/wiki/IPsec) oder [SMB-Signaturen (Server Message Block)](https://support.microsoft.com/en-us/kb/887429) konfigurieren.

-   Stellen Sie sicher, dass die Anwendung von einer vertrauenswürdigen Quelle stammt. Dies gilt insbesondere, wenn Sie Azure Active Directory (AAD) verwenden, da die Anwendung dann möglicherweise während der Laufzeit auf das AAD-Token zugreifen kann.

-   Sichern Sie das Ausgabeverzeichnis, das die umschlossene Anwendung enthält. Erwägen Sie für die Ausgabe ein Verzeichnis auf Benutzerebene zu verwenden.

## <a name="BKMK_ADAL_android"></a>Wrappen von Apps, die Azure Active Directory Library (ADAL) verwenden
Wenn Azure Active Directory Authentication Library (ADAL) von Ihrer App verwendet wird, führen Sie diese Schritte aus, bevor Sie Ihre App wrappen.

### Schritt 1: Stellen Sie sicher, dass die Anforderungen für ADAL erfüllt sind.
Für Apps, die ADAL verwenden, muss Folgendes zutreffen:

-   In der App muss mindestens ADAL 1.0.2 integriert sein.

-   Der Entwickler muss [grant their app access to the Intune Mobile Application Management resource](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md#BKMK_AD).

### <a name="BKMK_review_IDs"></a>Schritt 2: Überprüfen Sie die Bezeichner, die Sie beim Registrieren der App abrufen müssen.
Im nächsten Schritt verwenden Sie das Azure-Verwaltungsportal zum Registrieren Ihrer Apps (die ADAL mit Azure Active Directory (AAD) verwenden), um die in der folgenden Tabelle aufgeführten eindeutigen Bezeichner zu erhalten. Anschließend übergeben Sie die Bezeichner beim Integrieren von ADAL in die App dem Entwickler. Weitere Informationen über diese Bezeichner finden Sie unter [Microsoft Azure Active Directory Authentication Library (ADAL) für Android](https://github.com/AzureAD/azure-activedirectory-library-for-android/blob/master/README.md).

|ID|Weitere Informationen|Standardwert|
|------|-------------------------|----------------|
|**Client-ID**|Ein eindeutiger GUID-Bezeichner, der für die App nach der Registrierung mit AAD generiert wird.<br /><br />Wenn Sie die Client-ID der App kennen, geben Sie diesen Wert an. Andernfalls verwenden Sie den Standardwert.|6c7e8096-f593-4d72-807f-a5f86dcc9c77|
|**Authority URI**|Der Registrierungsstellen-URI-Wert (Uniform Resource Identifier) für AAD-Objekte (z. B. Benutzer und Gruppen).<br /><br />Der Parameter "AuthorityURI" ist für das App Wrapping Tool optional. Der Standard-URI wird verwendet, wenn Sie den Parameter nicht verwenden.|https://login.windows.net/common/|
|**SkipBroker**|Wert, der angibt, ob das Unternehmensportal als Broker verwendet wird.<br /><br />-   **True** – Unternehmensportal wird nicht für die ADAL-Authentifizierung verwendet.<br />-   **False** – Unternehmensportal wird für die ADAL-Authentifizierung verwendet. Das Unternehmensportal verwendet zu SSO-Zwecken den angemeldeten Benutzer.||
|**Non-Broker Redirect URI**|Anmelde-URI, der verwendet wird, wenn ADAL die Broker-App (Intune-Unternehmensportal) nicht verwendet.|urn:ietf:wg:oauth:2.0:oob|
|**Resource ID**|Zeiger auf die AAD-Ressourcen der App.|https://intunemam.microsoftonline.com|

### <a name="BKMK_AD"></a>Schritt 3: Konfigurieren Sie den Zugriff auf die Verwaltung von mobilen Anwendungen in AAD.
Bevor Sie die AAD-Registrierungswerte einer App im App Wrapping Tool verwenden können, muss der Anwendungsentwickler den Anwendungszugriff auf die mobile Anwendungsverwaltungs-Ressource von Intune unter Verwendung der folgenden Schritte gewähren:

1.  Melden Sie sich bei einem vorhandenen AAD-Konto im Azure-Verwaltungsportal an.

2.  Klicken Sie auf die Option zur **Registrierung von vorhandenen Branchen-Apps**.

3.  Wählen Sie im Abschnitt **Konfigurieren** die Option **Zugriff auf Web-APIs in anderen Anwendungen konfigurieren** aus.

4.  Wählen Sie aus der ersten Dropdownliste im Abschnitt **Berechtigungen für andere Anwendungen** die Option **Intune Mobile Application Management** aus.

Jetzt können Sie die Client-ID der App im App Wrapping Tool verwenden. Die Client-ID finden Sie im Azure Active Directory-Verwaltungsportal, wie in der Tabelle unter [Schritt 2: Überprüfen Sie die Bezeichner, die Sie beim Registrieren der App abrufen müssen.](#BKMK_review_IDs) beschrieben.

### Schritt 4: Verwenden Sie die AAD-Bezeichnerwerte im App Wrapping Tool.
Geben Sie die Werte im App Wrapping Tool unter Verwendung der Bezeichnerwerte aus dem Registrierungsprozess als Befehlszeileneigenschaften ein. Sie müssen alle Werte in der Tabelle angeben, damit Endbenutzer die App erfolgreich authentifizieren können. Wenn Sie einen Wert nicht angeben, wird der entsprechende Standardwert verwendet.

|ID|Parameter|
|------|-------------|
|Client-ID|ClientID|
|Authority URI|Authority-URI|
|SkipBroker|SkipBroker|
|Non-Broker Redirect URI|NonBrokerRedirectURI|
|Resource ID|ResourceID|
Beachten Sie beim Wrappen Ihrer App folgende Punkte:

-   Das App Wrapping Tool sucht nicht nach ADAL-Binärdateien innerhalb der App (sofern vorhanden). Wenn die App mit einer veralteten Version der Binärdateien verknüpft ist, können Laufzeitfehler während der Anmeldung auftreten, falls Sie die Authentifizierungsrichtlinien aktiviert haben.

-   Um zu überprüfen, ob die Authentifizierung erfolgreich war, ruft [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] das der MAM-Ressourcen-ID zugeordnete AAD-Token ab. Das Token wird jedoch in keinem Aufruf verwendet, wodurch die Gültigkeit des Tokens verifiziert würde.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] liest nur den Benutzerprinzipalname (UPN) des angemeldeten Benutzers, um den Zugriff auf die App zu bestimmen. Das AAD-Token wird nicht für weitere Dienstaufrufe verwendet.

-   Authentifizierungstoken werden von Apps desselben Herausgebers gemeinsam genutzt, da sie in einem freigegebenen Schlüsselbund gespeichert sind. Zum Isolieren einer bestimmten App verwenden Sie für diese ein anderes Signaturzertifikat, einen anderen Bereitstellungsprofil-KeyStore und einen anderen Schlüsselalias.

-   Doppelte Anmeldeeingabeaufforderungen werden verhindert, wenn Sie die Client-ID und den Registrierungsstellen-URI der Clientanwendung bereitstellen. Die Client-ID muss für den Zugriff auf die veröffentlichte [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] MAM Ressourcen-ID im AAD-Dashboard registriert werden. Wurde die Client-ID nicht registriert, erhalten Benutzer bei der Anmeldung einen Fehler, wenn die App ausgeführt wird.

## Nächste Schritte
Weitere Informationen zum Bereitstellen Ihrer umschlossenen Apps finden Sie unter [Bereitstellen von Apps für mobile Geräte in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md).

## Siehe auch
[Schützen von Daten mithilfe der Verwaltungsrichtlinien für mobile Anwendungen mit Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md)

