---
description: na
keywords: na
title: Ways to do enterprise mobility
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d91b8b5-bf44-4562-ab4a-6611584f9674
---
# Optionen f&#252;r die Mobilit&#228;t im Unternehmen
Microsoft bietet verschiedene Optionen zum Verwalten Ihrer mobilen Geräte. Wir haben auf dieser Seite die Informationen bereitgestellt, die Ihnen dabei helfen, zwischen diesen verschiedenen Optionen für die Mobilität im Unternehmen auszuwählen:

-   [Auswählen zwischen Intune und MDM für Office 365](#BKMK_MDMOfferings)

-   [Wählen zwischen dem eigenständigen Intune oder dem Integrieren von Intune in System Center Configuration Manager](#BKMK_HybridOfferings)

## <a name="BKMK_MDMOfferings"></a>Auswählen zwischen Intune und MDM für Office 365

|Überlegung|MDM für Office 365|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|
|--------------|----------------------|---------------------------------------------------------|
|Kosten|In vielen [kommerziellen Office 365-Abonnements](http://products.office.com/business/enterprise-productivity-tools) enthalten.|Erfordert ein [kostenpflichtiges Abonnement für Microsoft Intune](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/Purchasing.aspx) oder kann mit der [Enterprise Mobility Suite](http://www.microsoft.com/en-us/server-cloud/products/enterprise-mobility-suite/Purchasing.aspx) erworben werden.|
|Verwalten von Geräten|Geräte werden über das [Office 365 Admin Center](https://support.office.com/article/About-the-Office-365-admin-center-58537702-d421-4d02-8141-e128e3703547) verwaltet.|Wenn Sie [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] eigenständig verwenden, verwalten Sie die Geräte mithilfe der [Intune-Verwaltungskonsole](https://technet.microsoft.com/library/dn646966.aspx).<br /><br />Wenn Sie Intune in System Center 2012 Configuration Manager integrieren, verwenden Sie die Configuration Manager-Konsole, um Geräte lokal und in der Cloud zu verwalten.|
|Geräte, die Sie verwalten können|Cloudbasierte Verwaltung für:<br /><br />-   iOS<br />-   Android<br />-   Windows Phone|Cloudbasierte Verwaltung für:<br /><br />-   iOS<br />-   Mac OS X<br />-   Android<br />-   Windows Phone<br />-   Windows-PCs|
|Wichtige Funktionen|-   Stellen Sie sicher, dass auf unternehmensbezogene Office 365-E-Mails und -Dokumente nur auf Mobilgeräten zugegriffen werden kann, die von Ihrem Unternehmen verwaltet werden und mit Ihren IT-Richtlinien kompatibel sind.<br />-   Festlegen und Verwalten von Sicherheitsrichtlinien wie PIN-Sperre auf Geräteebene und Jailbreak-Erkennung, um zu verhindern, dass nicht autorisierte Benutzer auf gestohlenen oder verloren gegangenen Geräten auf unternehmensbezogene E-Mails und -Daten zugreifen.<br />-   Entfernen von Office 365-Unternehmensdaten vom Gerät eines Mitarbeiters, ohne die persönlichen Daten zu entfernen.<br /><br />Die neuesten Informationen zu Office 365 MDM-Funktionen finden Sie unter [Funktionen der integrierten Verwaltung von Mobilgeräten für Office 365](https://technet.microsoft.com/library/ms.o365.cc.devicepolicysupporteddevice.aspx).|MDM für Office 365-Funktionen und zusätzlich:<br /><br />-   Unterstützen von Benutzern beim sicheren Zugriff auf Unternehmensressourcen mit Zertifikaten sowie WLAN-, VPN- und E-Mail-Profilen.<br />-   Registrieren und Verwalten von Sammlungen unternehmenseigener Geräte zur Vereinfachung der Bereitstellung von Richtlinien und Apps.<br />-   Bereitstellen Ihrer internen Branchen-Apps und von Apps in Stores für Benutzer.<br />-   Ermöglichen, dass Ihre Benutzer sicher auf Unternehmensdaten mit den ihnen vertrauten mobilen Office- und Branchen-Apps zugreifen können, und Schützen der Daten durch Beschränken von Aktionen wie *Kopieren*, *Ausschneiden*, *Einfügen* und *Speichern unter* auf die von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwalteten Apps.<br />-   Aktivieren des sicheren Webbrowsens mithilfe der App „[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Managed Browser“.<br />-   Verwalten von PCs in der Cloud ohne erforderliche Infrastruktur mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] oder Verbinden von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] mit [!INCLUDE[cm5short](../Token/cm5short_md.md)] zum Verwalten aller Geräte einschließlich PCs, Macs, Linux- und UNIX-Servern und von Mobilgeräten über eine zentrale Verwaltungskonsole.|
Ab Oktober 2015 können Administratoren Benutzer und ihre mobilen Geräte sowohl mit Intune als auch mit Office 365 gleichzeitig auf demselben Mandanten verwalten. Dadurch können Sie entscheiden, welche Lösung am besten für bestimmte Benutzer und die zugehörigen Geräte geeignet ist. Sie können dann festlegen, ob ein Benutzer und seine Geräte mit Office 365 MDM oder mit der funktional umfangreicheren Intune-Verwaltungslösung verwaltet wird.

## <a name="BKMK_HybridOfferings"></a>Wählen zwischen dem eigenständigen Intune oder dem Integrieren von Intune in System Center Configuration Manager

|Das eigenständige [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] würde sich in diesen Fällen empfehlen:|[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] + Configuration Manager würde sich in diesen Fällen empfehlen:|
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
|-   Sie möchten mobile Geräte verwalten.<br />-   Sie möchten Computer verwalten, die nicht in eine Domäne eingebunden sind.<br />-   Sie müssen weniger als 50.000 Geräte verwalten.<br />-   Sie verfügen über keine (oder nur eine begrenzte) lokale IT-Infrastruktur. **Note:**     [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] erfordert keine lokale IT-Infrastruktur, kann die Funktionen von Exchange ActiveSync oder der Active Directory-Domänendienste allerdings nutzen, sofern diese installiert sind.<br />-   Ihre Mitarbeiter sind mobil oder geografisch weit verstreut. Mit der cloudbasierten Geräteverwaltung können Sie mobile Geräte und Computer weltweit uneingeschränkt verwalten.|-   Sie möchten Computer verwalten, die in eine Domäne eingebunden sind.<br />-   Sie möchten Server verwalten.<br />-   Sie möchten Computer mit dem Configuration Manager-Client, Mac-Computer, Linux- und UNIX-Server und mobile Geräte verwalten, die über dieselbe Konsole mit Intune registriert wurden.<br />-   Sie müssen mehr als 50.000 Geräte verwalten.<br />-   Sie verfügen über eine lokale IT-Infrastruktur oder planen deren Bereitstellung. In dieser Konfiguration ist die Verwaltung von Geräten und Ressourcen vollkommen vereinheitlicht.<br />-   Benutzernamen und Kennwörter werden synchronisiert. Auf diese Weise erhalten Benutzer nur ein Konto, mit dem sie auf Unternehmensressourcen zugreifen können – ob von einem Computer, der Mitglied einer Domäne ist, oder einem mobilen Gerät.|

### Detaillierter Vergleich der Funktionen
Die folgenden Tabellen vergleichen die Geräte- und App-Verwaltungsfunktionen, die Ihnen bei Verwendung von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] allein, Configuration Manager allein oder einer Lösung, die beide Produkte verwendet, zur Verfügung stehen.

Weitere Informationen zur Verwendung von Configuration Manager mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] finden Sie unter [Verwalten von mobilen Geräten mit Configuration Manager und Microsoft Intune](http://msdn.microsoft.com/en-us/library/2c6bd0e5-d436-41c8-bf38-30152d76be10).

#### Unterstützung von Geräten

|Plattform|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|System Center 2012 Configuration Manager SP2|System Center 2012 Configuration Manager SP2 und [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|
|-------------|---------------------------------------------------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------|
|Microsoft Windows|Ja|Ja|Ja|
|Microsoft Windows Server|Nein|Ja|Ja|
|Windows Phone|Ja|Nein|Ja|
|Windows RT|Ja|Nein|Ja|
|iOS|Ja|Nein|Ja|
|Android und Samsung KNOX|Ja|Nein|Ja|
|Mac OS X|Ja|Ja|Ja|
|UNIX/Linux-Server|Nein|Ja|Ja|

#### Produktfunktionen
> [!TIP]
> Wo „(R2)“ angegeben ist, erfordert die aufgelistete Funktion Microsoft System Center 2012 R2 Configuration Manager oder höher.

|Szenario|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|System Center 2012 Configuration Manager SP2|System Center 2012 Configuration Manager SP2 und [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|
|------------|---------------------------------------------------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------|
|**Kompatibilitätseinstellungen**||||
|Bereitstellen und Anpassen von Gerätekonfigurationseinstellungen für Windows-PCs (z. B. WMI, Registrierung)|Nein|Ja|Ja|
|Bereitstellen und Anpassen von Mac OS X-Konfigurationseinstellungen|Ja|Ja|Ja|
|Bereitstellen von Konfigurationseinstellungen auf mobilen Geräten|Ja|Ja|Ja|
|Bereitstellen von benutzerdefinierten Einstellungen für mobile Geräte (z. B. OMA-URI und Apple Configurator)|Ja|Ja|Ja|
|**Bereitstellung**||||
|Bereitstellen von Apps auf Geräten und Windows-PCs|Ja|Ja|Ja|
|Bereitstellen von Windows-Betriebssystemen|Nein|Ja|Ja|
|**Sicherheit und Datenschutz**||||
|Verwalten von Windows-Softwareupdates|Ja|Ja|Ja|
|Überwachen von Windows-PCs mit Endpoint Protection|Ja|Ja|Ja|
|**Verwaltung und Berichterstellung**||||
|Verwenden der Softwaremessung, um zu überwachen, wie oft Software verwendet wird, und entsprechende Berichterstellung|Nein|Ja|Ja|
|Hardware- und Softwareinventur|Ja|Ja|Ja|
|Erweitern des Hardware- und Softwarebestands für Windows-PCs|Nein|Ja|Ja|
|Verwenden der rollenbasierten Verwaltung und Berichterstellung zur Steuerung des Zugriffs auf Produktfunktionen|Nein|Ja|Ja|
|Ausführen von Berichten für Windows-PCs und registrierte Mobilgeräte über die gleiche Konsole|Nein|Nein|Ja|
|Anpassen vorhandener Berichte und Erstellen eigener Berichte mithilfe der SQL Server Reporting Services|Nein|Ja|Ja|
|**Datenschutz für mobile Geräte**||||
|Bereitstellen von Sicherheitsrichtlinien für mobile Geräte|Ja|Ja|Ja|
|Remotezurücksetzung|Ja|Ja|Ja|
|Remotesperre|Ja|Ja|Ja|
|Zurücksetzen der Kennung|Ja|Ja|Ja|
|**Zugriff auf Unternehmensressourcen**||||
|E-Mail-Profile|Ja|Ja (R2)|Ja (R2)|
|WLAN-Profile|Ja|Ja (R2)|Ja (R2)|
|VPN-Profile|Ja|Ja (R2)|Ja (R2)|
|Zertifikatprofile|Ja|Ja (R2)|Ja (R2)|
|Verwalten des Zugriffs auf Exchange-E-Mails und SharePoints mit bedingtem Zugriff|Ja|Ja|Ja|
|Mobile Anwendungsverwaltung|Ja|Ja|Ja|
|App-Konformitätsrichtlinien (konforme und nicht konforme Apps)|Ja|Ja|Ja|
|Kioskmodus|Ja|Ja|Ja|
|Richtlinie für verwaltete Internetbrowser|Ja|Ja|Ja|
|**Automatisierung**||||
|Verwenden von PowerShell zur Automatisierung von Vorgängen|Nein|Ja|Ja|

## Siehe auch
[Einführung in Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)

