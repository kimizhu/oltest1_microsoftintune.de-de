---
description: na
keywords: na
title: Troubleshoot company resource access problems with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40622ced-6029-4abf-873e-b51d2b51934c
---
# Behandlung von Problemen mit dem Zugriff auf Unternehmensressourcen in Microsoft Intune
Verwenden Sie die Informationen in diesem Thema  zur Problembehandlung, wenn von einer [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Aktion ein Fehlercode zurückgegeben wurde.

Wenn sich das Problem mit diesen Informationen nicht beheben lässt, finden Sie unter [Anfordern von Support für Microsoft Intune](../Topic/How_to_get_support_for_Microsoft_Intune.md) weitere Möglichkeiten, um Hilfe zu erhalten.

## Fehlercodes im Zusammenhang mit dem Zugriff auf Unternehmensressourcen

### Statuscodes für MDM-verwaltete Windows-Geräte

|Statuscode|Fehlermeldung|Aktion|
|--------------|-----------------|----------|
|10 (APP_CI_ENFORCEMENT_IN_PROGRESS)|Installation läuft||
|20 (APP_CI_ENFORCEMENT_IN_PROGRESS_WAITING_CONTENT)|Warten auf Inhalt||
|30 (APP_CI_ENFORCEMENT_ERROR_RETRIEVING_CONTENT)|Inhalt wird abgerufen.|Mögliche Ursache: Auftragsstatus 30 gibt an, dass beim Herunterladen einer App durch einen Benutzer ein Fehler aufgetreten ist.<br /><br />Mögliche Ursachen können sein:<br /><br />Die Internetverbindung des Geräts wurde während des Downloads unterbrochen.<br /><br />Möglicherweise ist das Zertifikat abgelaufen, das bei der Registrierung für das Gerät ausgestellt wurde.<br /><br />Lösung:<br /><br />Starten Sie die Unternehmens-Apps-Anwendung in der Systemsteuerung auf dem Gerät, um zu prüfen, ob das Gerätezertifikat noch gültig ist. Andernfalls müssen Sie das Gerät erneut registrieren.<br /><br />Vergewissern Sie sich, dass das Gerät mit dem Internet verbunden ist, und rufen Sie die App erneut ab.|
|40 (APP_CI_ENFORCEMENT_IN_PROGRESS_CONTENT_DOWNLOADED)|Download abgeschlossen.||
|50 (APP_CI_ENFORCEMENT_IN_PROGRESS_INSTALLING)|Installation läuft||
|60 (APP_CI_ENFORCEMENT_ERROR_INSTALLING)|InstallationFehler aufgetreten.|Die heruntergeladene App konnte nicht installiert werden.<br /><br />Das Codesignaturzertifikat, mit dem die Anwendung signiert wurde, ist nicht auf dem Gerät vorhanden.<br /><br />Eine Frameworkabhängigkeit, von der die Anwendung abhängt, ist nicht auf dem Gerät installiert.<br /><br />Stellen Sie sicher, dass das Codesignaturzertifikat, mit dem die App signiert wurde, auf dem Gerät vorhanden ist. Lassen Sie sich zudem vom Administrator bestätigen, dass ein solches Zertifikat für alle im Unternehmen registrierten Windows RT-Geräte vorgesehen war.<br /><br />Falls der Installationsfehler aufgrund einer fehlenden Frameworkabhängigkeit aufgetreten ist, muss der Administrator die Anwendung erneut veröffentlichen und dabei das Framework zusammen mit dem Anwendungspaket verpacken.<br /><br />Das heruntergeladene Anwendungspaket ist kein gültiges Paket, wurde möglicherweise beschädigt oder ist nicht mit der Version des Betriebssystems auf dem Gerät kompatibel.|
|70 (APP_CI_ENFORCEMENT_SUCCEEDED)|Installation erfolgreich.||
|80 (APP_CI_ENFORCEMENT_IN_PROGRESS)|Deinstallation wird durchgeführt.||
|90 (APP_CI_ENFORCEMENT_ERROR)|Fehler beim Deinstallieren.||
|100 (APP_CI_ENFORCEMENT_SUCCEEDED)|Deinstallation erfolgreich.||
|110 (APP_CI_ENFORCEMENT_ERROR)|Inhaltshash stimmt nicht überein.||
|120 (APP_CI_ENFORCEMENT_ERROR)|Laden des SLK/der Seite nicht aktiviert.||
|130 (APP_CI_ENFORCEMENT_ERROR)|Fehler bei der Installation der MSADP-Lizenz.||
|Kein Statuscode (APP_CI_ENFORCEMENT_UNKNOWN)|Nicht zutreffend|Der Status ist aktuell unbekannt.|

### Zugriff auf Unternehmensressourcen (allgemeine Fehler)

|Statuscode|Fehlermeldung|
|--------------|-----------------|
|-2016281101|MDM CRP-Anforderung nicht gefunden.|
|-2016281102|NDES-URL nicht gefunden.|
|-2016281103|MDM CRP-Zertifikatinformationen nicht gefunden.|
|-2016281104|MDM CI-Zertifikatinformationen nicht gefunden.|
|-2016281105|Fehler beim Auswerten der Regel.|
|-2016281106|Nicht anwendbar, da bei der Konfliktauflösung verloren gegangen.|
|-2016281107|Nicht unterstützte Einstellung für Ermittlungsquelle.|
|-2016281108|Referenzierte Einstellung in CI nicht gefunden.|
|-2016281109|Fehler bei der Konvertierung des Datentyps.|
|-2016281110|Ungültiger Parameter für CIM-Einstellung.|
|-2016281111"|Für dieses Gerät nicht anwendbar.|
|-2016281112|Fehler bei Wiederherstellung.|
|-2016330905|App-Status ist unbekannt.|
|-2016330906|Die App wird verwaltet, wurde aber vom Benutzer entfernt.|
|-2016330907|Einlösungscode wird eingelöst.|
|-2016330908|Fehler bei der App-Installation.|
|-2016330909|Aktualisieren der App vom Benutzer abgelehnt.|
|-2016330910|Installieren der App vom Benutzer abgelehnt.|
|-2016330911|Der Benutzer hat die App installiert, bevor eine verwaltete App-Installation stattgefunden hat.|
|-2016330912|Die App ist für die Installation geplant, erfordert jedoch einen Einlösecode, um die Transaktion abschließen zu können.|
|-2016341109|iOS-Gerät hat einen Fehler zurückgegeben.|
|-2016341110|iOS-Gerät hat den Befehl aufgrund eines falschen Formats zurückgewiesen.|
|-2016341111|iOS-Gerät hat einen unerwarteten Leerlaufstatus zurückgegeben.|
|-2016341112|iOS-Gerät ist derzeit ausgelastet.|

### iOS-Geräte haben Fehler zurückgegeben.

|Statuscode|Fehlermeldung|
|--------------|-----------------|
|-2016299111|Interner Fehler.|
|-2016299112|Interner Fehler.|
|-2016300111|36001: (interner Fehler)|
|-2016300112|36000: Mobilfunknetz wurde bereits konfiguriert.|
|-2016301110|35002: Mehrere Schriftarten in einer einzelnen Nutzlast.|
|-2016301111|35001: Fehler bei der Installation der Schriftart.|
|-2016301112|35000: Ungültige Schriftartdaten.|
|-2016302109|34003: Kerberos-Prinzipalname ungültig.|
|-2016302110|34002: Kerberos-Prinzipalname fehlt.|
|-2016302111|34001: Ungültiges URL-Vergleichsmuster.|
|-2016302112|34000: Ungültiges App-ID-Übereinstimmungsmuster.|
|-2016304112|32000: Zu viele Apps.|
|-2016305111|31001: Einstellungen können nicht angewendet werden.|
|-2016305112|31000: Anmeldeinformationen können nicht angewendet werden.|
|-2016306111|30001: Zeitüberschreitung|
|-2016306112|30000: Fehler bei der Authentifizierung.|
|-2016307109|29003: Ungültige Zertifikatdaten.|
|-2016307110|29002:|
|-2016307111|29001:|
|-2016307112|29000: Gerät wird nicht überwacht.|
|-2016308110|28002: Hintergrundbild kann nicht festgelegt werden.|
|-2016308111|28001: Ungültiges Hintergrundbild.|
|-2016308112|28000: Unbekanntes Element.|
|-2016310111|26001: Verschlüsselung auf Dateiebene nicht unterstützt|
|-2016310112|26000: Verschlüsselung auf Blockebene nicht unterstützt.|
|-2016311110|25002: Kann nicht entfernt werden.|
|-2016311111|25001: Kann nicht installiert werden.|
|-2016311112|25000: Ungültiges Profil.|
|-2016312109|24003: Ungültiges finales Profil.|
|-2016312110|24002: Ungültige Identitätsnutzlast.|
|-2016312111|24001: Attributverzeichnis kann nicht signiert werden.|
|-2016312112|24000: Attributverzeichnis kann nicht erstellt werden.|
|-2016313110|23002: Ungültiges Serverzertifikat.|
|-2016313111|23001: Ungültige Serverantwort.|
|-2016313112|23000: Ungültige Identität.|
|-2016314099|22013: Ungültige Antwort auf PKI-Vorgang.|
|-2016314100|22012: CA-Zertifikat kann nicht gespeichert werden.|
|-2016314101|22011: CSR kann nicht generiert werden.|
|-2016314102|22010: Temporäre Identität kann nicht gespeichert werden.|
|-2016314103|22009: Temporäre Identität kann nicht erstellt werden.|
|-2016314104|22008: Identität kann nicht erstellt werden.|
|-2016314105|22007: Ungültiges signiertes Zertifikat.|
|-2016314106|22006: Nicht genügend CACaps.|
|-2016314107|22005: Netzwerkfehler|
|-2016314108|22004: Zertifikatkonfiguration nicht unterstützt.|
|-2016314109|22003: Ungültige RA-Antwort.|
|-2016314110|22002: Ungültige CA-Antwort.|
|-2016314111|22001: Schlüsselpaar kann nicht generiert werden.|
|-2016314112|22000: Ungültige Schlüsselverwendung.|
|-2016315105|21007: Konto kann nicht überprüft werden.|
|-2016315106|21006: Zertifikat kann nicht entschlüsselt werden.|
|-2016315107|21005: Konto nicht eindeutig.|
|-2016315108|21004: Konto kann nicht erstellt werden.|
|-2016315109|21003: Kein Hostname.|
|-2016315110|21002: Verletzung der Verschlüsselungsrichtlinie vom Server.|
|-2016315111|21001: Verletzung der Richtlinie vom Server.|
|-2016315112|21000: Richtlinie kann nicht vom Server abgerufen werden.|
|-2016316110|20002: Konto nicht eindeutig.|
|-2016316111|20001: Kein Hostname.|
|-2016316112|20000: Konto kann nicht erstellt werden.|
|-2016317110|19002: Konto nicht eindeutig.|
|-2016317111|19001: Kein Hostname.|
|-2016317112|19000: Konto kann nicht erstellt werden.|
|-2016318110|18002: Ungültige Anmeldeinformationen.|
|-2016318111|18001: Host nicht erreichbar.|
|-2016318112|18000: Unbekannter Fehler.|
|-2016319110|17002: Konto nicht eindeutig.|
|-2016319111|17001: Kein Hostname.|
|-2016319112|17000: Konto kann nicht erstellt werden.|
|-2016320110|16002: Konto nicht eindeutig.|
|-2016320111|16001: Kein Hostname.|
|-2016320112|16000: Abonnement kann nicht erstellt werden.|
|-2016321109|15003: Ungültiges Zertifikat.|
|-2016321110|15002: Netzwerkkonfiguration kann nicht gesperrt werden.|
|-2016321111|15001: VPN kann nicht entfernt werden.|
|-2016321112|15000: VPN kann nicht installiert werden.|
|-2016322110|14002: Cloudkonfiguration bereits vorhanden.|
|-2016322111|14001: Gerät gesperrt.|
|-2016322112|14000: Ungültiges Feld.|
|-2016323107|13005: Proxy kann nicht eingerichtet werden.|
|-2016323108|13004: EAP kann nicht eingerichtet werden.|
|-2016323109|13003: WLAN-Konfiguration kann nicht erstellt werden.|
|-2016323110|13002: Kennwort erforderlich.|
|-2016323111|13001: Benutzername erforderlich.|
|-2016323112|13000: Kann nicht installiert werden.|
|-2016324070|12042: Unbekannter Gebietsschemacode.|
|-2016324071|12041: Unbekannter Sprachcode.|
|-2016324072|12040: Anmeldung bei iTune Store erforderlich.|
|-2016324073|12039: (Nicht belegt)|
|-2016324074|12038: App nicht verwaltet.|
|-2016324075|12037: Ungültiger Einlösecode.|
|-2016324076|12036: App kann im aktuellen Zustand nicht entfernt werden.|
|-2016324077|12035: App kann nicht erworben werden.|
|-2016324078|12034: URL ist nicht HTTPS.|
|-2016324079|12033: Ungültiges Manifest.|
|-2016324080|12032: Zu viele Apps im Manifest.|
|-2016324081|12031: App-Installation deaktiviert.|
|-2016324082|12030: Ungültige URL.|
|-2016324083|12029: App nicht verwaltet.|
|-2016324084|12028: Auf Einlösung wird nicht gewartet.|
|-2016324085|12027: Dies ist keine App.|
|-2016324086|12026: App bereits in der Warteschlange.|
|-2016324087|12025: App wurde bereits installiert.|
|-2016324088|12024: App-Manifest konnte nicht überprüft werden.|
|-2016324089|12023: App-ID konnte nicht überprüft werden.|
|-2016324090|12022: Ungültiges Thema.|
|-2016324091|12021: Ungültiger Anforderungstyp.|
|-2016324092|12020: Nicht vom Server autorisiert.|
|-2016324093|12019: Hinterlegter geheimer Schlüssel kann nicht kopiert werden.|
|-2016324094|12018: Hinterlegte Schlüsselbunddaten können nicht kopiert werden.|
|-2016324095|12017: Hinterlegter Schlüsselbund kann nicht erstellt werden.|
|-2016324096|12016: Fehlende Identität.|
|-2016324097|12015: Pushtoken nicht abrufbar.|
|-2016324098|12014: Bereitstellungsprofil nicht verwaltet.|
|-2016324099|12013: Profil nicht verwaltet.|
|-2016324100|12012: MDM-Ersetzung stimmt nicht überein.|
|-2016324101|12011: Ungültige MDM-Konfiguration.|
|-2016324102|12010: Interner Inkonsistenzfehler.|
|-2016324103|12009: Ungültiges Austauschprofil.|
|-2016324104|12008: Falsch formatierte Anforderung.|
|-2016324105|12007: Nicht autorisiert.|
|-2016324106|12006: Umleitung abgelehnt.|
|-2016324107|12005: Zertifikat kann nicht gefunden werden.|
|-2016324108|12004: Ungültiges Push-Zertifikat.|
|-2016324109|12003: Ungültige Rückmeldung für Abfrage.|
|-2016324110|12002: Einchecken nicht möglich.|
|-2016324111|12001: Mehrere MDM-Instanzen.|
|-2016324112|12000: Ungültige Zugriffsrechte.|
|-2016325111|11001: Benutzerdefinierter APN wurde bereits installiert.|
|-2016325112|11000: VPN kann nicht installiert werden.|
|-2016326111|10001: Ungültiger Signaturgeber.|
|-2016326112|10000: Standardeinstellungen können nicht installiert werden.|
|-2016327106|9006: Zertifikat ist keine Identität.|
|-2016327107|9005: Zertifikat hat falsches Format.|
|-2016327108|9004: Stammzertifikat kann nicht gespeichert werden.|
|-2016327109|9003: WAPI-Daten können nicht gespeichert werden.|
|-2016327110|9002: Zertifikat kann nicht gespeichert werden.|
|-2016327111|9001: Zu viele Zertifikate in einer Nutzlast.|
|-2016327112|9000: Ungültiges Kennwort.|
|-2016328112|8000: Webclip kann nicht installiert werden.|
|-2016329105|7007: SMTP-Konto ist falsch konfiguriert.|
|-2016329106|7006: POP-Konto ist falsch konfiguriert.|
|-2016329107|7005: IMAP-Konto ist falsch konfiguriert.|
|-2016329108|7004: SMIME-Zertifikat ist ungültig.|
|-2016329109|7003: SMIME-Zertifikat nicht gefunden.|
|-2016329110|7002: Unbekannter Fehler bei der Überprüfung.|
|-2016329111|7001: Ungültige Anmeldeinformationen.|
|-2016329112|7000: Host nicht erreichbar.|
|-2016330110|6002: Abfrage kann nicht erstellt werden.|
|-2016330111|6001: Leere Zeichenfolge.|
|-2016330112|6000: Schlüsselbundsystemfehler|
|-2016331097|5015: Toleranzperiode kann nicht festgelegt werden.|
|-2016331098|5014: Kennung kann nicht festgelegt werden.|
|-2016331099|5013: Kennung kann nicht gelöscht werden.|
|-2016331100|5012: (Nicht belegt)|
|-2016331101|5011: Falsche Kennung.|
|-2016331102|5010: Gerät gesperrt.|
|-2016331103|5009: (Nicht belegt)|
|-2016331104|5008: Kennung zu aktuell.|
|-2016331105|5007: Kennung abgelaufen.|
|-2016331106|5006: Kennung muss Buchstaben enthalten.|
|-2016331107|5005: Kennung muss Zahl enthalten.|
|-2016331108|5004: Kennung enthält aufsteigende/absteigende Zeichen.|
|-2016331109|5003: Kennung enthält sich wiederholende Zeichen.|
|-2016331110|5002: Zu wenige komplexe Zeichen.|
|-2016331111|5001: Zu wenige eindeutige Zeichen.|
|-2016331112|5000: Kennung zu kurz.|
|-2016332093|4019: Mehrere App-Sperre-Nutzlasten.|
|-2016332094|4018: Mehrere APN- oder Mobilfunknetz-Nutzlasten.|
|-2016332095|4017: Mehrere globale HTTPProxy-Nutzlasten.|
|-2016332096|4016: (interner Fehler)|
|-2016332097|4015: Ersatzprofil enthält keine MDM-Nutzlast.|
|-2016332098|4014: Keine Geräteidentität verfügbar.|
|-2016332099|4013: Fehler bei Update.|
|-2016332100|4012: Profil kann nicht aktualisiert werden.|
|-2016332101|4011: Finales Profil ist kein Konfigurationsprofil.|
|-2016332102|4010: Aktualisiertes Profil hat nicht denselben Bezeichner.|
|-2016332103|4009: Gerät gesperrt.|
|-2016332104|4008: Nicht übereinstimmende Zertifikate.|
|-2016332105|4007: Dateiformat nicht erkannt.|
|-2016332106|4006: Datum für Profilentfernung liegt in der Vergangenheit.|
|-2016332107|4005: Kennung nicht kompatibel.|
|-2016332108|4004: Installation durch Benutzer abgebrochen.|
|-2016332109|4003: Profile für Installation nicht in Warteschlange.|
|-2016332110|4002: Doppelte UUID.|
|-2016332111|4001: Fehler bei der Installation.|
|-2016332112|4000: Profil kann nicht analysiert werden.|
|-2016333111|3001: Inkonsistente Wertvergleichserkennung (interner Fehler).|
|-2016333112|3000: Inkonsistente Einschränkungserkennung (interner Fehler).|
|-2016334108|2004: Nicht unterstützter Feldwert.|
|-2016334109|2003: Ungültiger Datentyp in Feld.|
|-2016334110|2002: Pflichtfeld fehlt.|
|-2016334111|2001: Nicht unterstützte Nutzlastversion.|
|-2016334112|2000: Nutzlast falsch formatiert.|
|-2016335102|1010: Nicht unterstützter Feldwert.|
|-2016335103|1009: Fehler bei Profilinstallation.|
|-2016335104|1008: Nicht eindeutige Nutzlastbezeichner.|
|-2016335105|1007: Nicht eindeutige UUIDs.|
|-2016335106|1006: Entschlüsseln nicht möglich.|
|-2016335107|1005: Leeres Profil.|
|-2016335108|1004: Ungültige Signatur.|
|-2016335109|1003: Ungültiger Datentyp in Feld.|
|-2016335110|1002: Pflichtfeld fehlt.|
|-2016335111|1001: Nicht unterstützte Profilversion.|
|-2016335112|1000: Falsche Profilsyntax.|

### OMA-Antwortcodes

|Statuscode|Fehlermeldung|
|--------------|-----------------|
|-2016344008|(1404): Zugriff auf Zertifikat verweigert.|
|-2016344009|(1403): Das Zertifikat wurde nicht gefunden.|
|-2016344010|DCMO(1402): Fehler beim Vorgang.|
|-2016344011|DCMO(1401): Der Benutzer hat den Vorgang bei Aufforderung nicht akzeptiert.|
|-2016344012|DCMO(1400): Clientfehler|
|-2016344108|DCMO(1400): Gerätefunktion ist deaktiviert. Der Benutzer ist zur Reaktivierung berechtigt.|
|-2016344109|DCMO(1203): Gerätefunktion ist deaktiviert. Der Benutzer ist zur Reaktivierung nicht berechtigt.|
|-2016344110|DCMO(1202): Aktivierung wurde erfolgreich ausgeführt, doch die Gerätefunktion ist derzeit getrennt.|
|-2016344111|DCMO(1201): Aktivierung wurde erfolgreich ausgeführt, und die Gerätefunktion ist derzeit angefügt.|
|-2016344112|DCMO(1200): Der Vorgang wurde erfolgreich ausgeführt.|
|-2016345595|Syncml(517): Die Antwort auf einen unteilbaren Befehl war zu groß für eine Einzelmeldung.|
|-2016345596|Syncml(516): Der Befehl befand sich in einem unteilbaren Element, und bei Atomic ist ein Fehler aufgetreten.Der Befehl konnte nicht zurückgesetzt werden.|
|-2016345598|Syncml(514): Der SyncML-Befehl wurde nicht ausgeführt, weil der Vorgang vor Verarbeitung des Befehls abgebrochen wurde.|
|-2016345599|Syncml(513): Der Empfänger unterstützt die angegebene Version des SyncML-Synchronisierungsprotokolls in der SyncML-Abfragemeldung nicht oder weist sie zurück.|
|-2016345600|Syncml(512): Bei der Synchronisierungssitzung ist ein Anwendungsfehler aufgetreten.|
|-2016345601|Syncml(511): Bei der Verarbeitung der Anforderung ist auf dem Server ein schwerwiegender Fehler aufgetreten.|
|-2016345602|Syncml(510): Bei der Verarbeitung der Anforderung ist ein Fehler aufgetreten.Ursache des Fehlers ist ein Fehler im Datenspeicher des Empfängers.|
|-2016345603|Syncml(509): Reserviert für zukünftige Verwendung.|
|-2016345604|Syncml(508): Aufgrund eines Fehlers muss der aktuelle Synchronisierungszustand des Clients auf dem Server aktualisiert werden.|
|-2016345605|Syncml(507): Aufgrund des Fehlers konnte keiner der SyncML-Befehle in einem unteilbaren Element ausgeführt werden.|
|-2016345606|Syncml(506): Bei der Verarbeitung der Anforderung ist ein Fehler aufgetreten.|
|-2016345607|Syncml(505): Der Empfänger unterstützt die angegebene Version der SyncML DTD in der SyncML-Abfragemeldung nicht oder weist sie zurück.|
|-2016345608|Syncml(504): In seiner Funktion als Gateway oder Proxy empfing der Empfänger keine rechtzeitige Antwort von dem im URI angegebenen Upstreamempfänger (z. B. HTTP, FTP, LDAP), oder von einem anderen Hilfsempfänger, auf den bei der Erfüllung der Anforderung zugegriffen werden muss (z. B. DNS).|
|-2016345609|Syncml(503): Die Anforderung kann derzeit aufgrund einer zeitweiligen Überlastung oder einer Wartung des Empfängers nicht verarbeitet werden.|
|-2016345610|Syncml(502): In seiner Funktion als Gateway oder Proxy empfing der Empfänger eine ungültige Antwort von dem Upstreamempfänger, auf den er zur Erfüllung der Anforderung zugegriffen hat.|
|-2016345611|Syncml(501): Der Empfänger unterstützt den zur Erfüllung der Anforderung erforderlichen Befehl nicht.|
|-2016345612|Syncml(500): Aufgrund einer unerwarteten Bedingung konnte die Anforderung vom Empfänger nicht erfüllt werden.|
|-2016345684|Syncml(428): Fehler beim Verschieben.|
|-2016345685|Syncml(427): Das übergeordnete Element enthält untergeordnete Elemente und kann daher nicht gelöscht werden.|
|-2016345686|Syncml(426): Ein unvollständiges Element wurde nicht angenommen.|
|-2016345687|Syncml(425): Beim Anforderungsbefehl ist ein Fehler aufgetreten, weil der Absender auf dem Empfänger keine ausreichende Zugriffssteuerungsberechtigung (ACL) besitzt.|
|-2016345688|Syncml(424): Das aufgeteilte Objekt wurde empfangen, seine Größe entsprach jedoch nicht dem im ersten Teil angegebenen Wert.|
|-2016345689|Syncml(423): Beim Anforderungsbefehl ist ein Fehler aufgetreten, weil das "vorläufig gelöschte" Element zuvor auf dem Server dauerhaft gelöscht wurde.|
|-2016345690|Syncml(422): Beim Anforderungsbefehl auf dem Server ist ein Fehler aufgetreten, weil das CGI-Skript im LocURI fehlerhaft war.|
|-2016345691|Syncml(421): Beim Anforderungsbefehl ist ein Fehler aufgetreten, weil die angegebene Suchgrammatik unbekannt war.|
|-2016345692|Syncml(420): Auf dem Empfänger ist nicht genügend Speicherplatz für die restlichen Synchronisierungsdaten vorhanden.|
|-2016345693|Syncml(419): Aufgrund der Clientanforderung entstand ein Konflikt, der zugunsten des Serverbefehls gelöst wurde.|
|-2016345694|Syncml(418): Der angeforderte Put- oder Add-Befehl konnte nicht ausgeführt werden, da das Ziel bereits vorhanden ist.|
|-2016345695|Syncml(417): Die Anforderung konnte zu diesem Zeitpunkt nicht ausgeführt werden. Der ursprüngliche Absender sollte sie später erneut stellen.|
|-2016345696|Syncml(416): Die Anforderung konnte nicht ausgeführt werden, da die angeforderte Bytegröße zu hoch war.|
|-2016345697|Syncml(415): Typ oder Format des Mediums nicht unterstützt.|
|-2016345698|Syncml(414): Der angeforderte Befehl wurde nicht ausgeführt, weil der URI für die Verarbeitung durch den Empfänger zu lang ist.|
|-2016345699|Syncml(413): Die Anforderung wird vom Empfänger abgewiesen, da das angeforderte Element für die Verarbeitung durch den Empfänger zu groß ist.|
|-2016345700|Syncml(412): Die Anforderung wurde auf dem Empfänger nicht verarbeitet, da sie unvollständig oder nicht korrekt war.|
|-2016345701|Syncml(411): Der Anforderungsbefehl muss eine Bytegrößen- oder Bytelängenangabe im Metaelementtyp enthalten.|
|-2016345702|Syncml(410): Das angeforderte Ziel befindet sich nicht mehr auf dem Empfänger, und der Weiterleitungs-URI ist unbekannt.|
|-2016345703|Syncml(409): Die Anforderung konnte nicht erfüllt werden, da bei den Datenversionen auf Client und Server ein Aktualisierungskonflikt besteht.|
|-2016345704|Syncml(408): Eine erwartete Meldung wurde nicht innerhalb des festgelegten Zeitraums empfangen.|
|-2016345705|Syncml(407): Der angeforderte Befehl konnte nicht ausgeführt werden, da vom Absender richtige Authentifizierungsdaten bereitgestellt werden müssen.|
|-2016345706|Syncml(406): Der angeforderte Befehl konnte nicht ausgeführt werden, da eine optionale Funktion in der Anforderung nicht unterstützt wird.|
|-2016345707|Syncml(405): Der angeforderte Befehl ist auf dem Ziel nicht zulässig.|
|-2016345708|Syncml(404): Das angeforderte Ziel wurde nicht gefunden.|
|-2016345709|Syncml(403): Der angeforderte Befehl konnte nicht ausgeführt werden, er wurde jedoch vom Empfänger verstanden.|
|-2016345710|Syncml(402): Der angeforderte Befehl konnte nicht ausgeführt werden, da die richtige Bezahlung erforderlich ist.|
|-2016345711|Syncml(401): Der angeforderte Befehl konnte nicht ausgeführt werden, da vom Absender richtige Authentifizierungsdaten bereitgestellt werden müssen.|
|-2016345712|Syncml(400): Der angeforderte Befehl konnte aufgrund eines Syntaxfehlers nicht ausgeführt werden.|
|-2016345807|Syncml(305): Auf das angeforderte Ziel muss über den angegebenen Proxy-URI zugegriffen werden.|
|-2016345808|Syncml (304): Der angeforderte SyncML-Befehl wurde auf dem Ziel nicht ausgeführt.|
|-2016345809|Syncml(303): Das angeforderte Ziel besitzt einen anderen URI.|
|-2016345810|Syncml(302): Das angeforderte Ziel wurde vorübergehend an einen anderen URI verschoben.|
|-2016345811|Syncml(301): Das angeforderte Ziel besitzt einen neuen URI.|
|-2016345812|Syncml(300): Das angeforderte Ziel ist eines von mehreren Alternativen.|
|-2016345896|Syncml(216): Der Befehl befand sich in einem unteilbaren Element, und bei Atomic ist ein Fehler aufgetreten.Der Befehl konnte nicht zurückgesetzt werden.|
|-2016345897|Syncml(215): Ein Befehl wurde aufgrund einer Benutzerinteraktion nicht ausgeführt, und der Benutzer hat die Auswahl nicht akzeptiert.|
|-2016345898|Syncml(214): Vorgang abgebrochen.Der SyncML-Befehl wurde erfolgreich abgeschlossen, aber in der Sitzung werden keine weiteren Befehle verarbeitet.|
|-2016345899|Syncml(213): Aufgeteiltes Element akzeptiert und gepuffert.|
|-2016345900|Syncml(212): Authentifizierung akzeptiert.Für den Rest der Synchronisierungssitzung ist keine weitere Authentifizierung erforderlich.Dieser Antwortcode kann nur als Antwort auf eine Anforderung verwendet werden, in der die Anmeldeinformationen bereitgestellt wurden.|
|-2016345901|Syncml(211): Das Element wurde nicht gelöscht.Das angeforderte Element wurde nicht gefunden.Es wurde möglicherweise zuvor gelöscht.|
|-2016345902|Syncml(210): Ohne Archivieren löschen.Die Antwort gibt an, dass die angeforderten Daten erfolgreich gelöscht wurden, ohne sie jedoch vor dem Löschen zu archivieren, da diese OPTIONALE Funktion von der Implementierung nicht unterstützt wurde.|
|-2016345903|Konflikt durch Duplizieren behoben.Die Antwort gibt an, dass die Anforderung einen Aktualisierungskonflikt verursacht hat, der durch Duplizieren der in der Serverdatenbank erstellten Clientdaten behoben wurde.Die Antwort enthält im Statuselement beide Ziel-URI des Duplikats.Darüber hinaus wird bei einer bidirektionalen Synchronisierung ein Add-Befehl mit der duplizierten Datendefinition zurückgegeben.|
|-2016345904|Konflikt behoben, wobei der Clientbefehl "gewinnt".Die Antwort gibt an, dass ein Aktualisierungskonflikt aufgetreten ist, der behoben wurde, indem der Clientbefehl gewinnt.|
|-2016345905|Konflikt durch Zusammenführen behoben.Die Antwort gibt an, dass die Anforderung ein Konflikts erzeugt hat, der durch Zusammenführen der Client- und Serverinstanzen der Daten behoben wurde.Die Antwort enthält im Statuselement die Ziel- und Quell-URL.Darüber hinaus wird ein Replace-Befehl mit zusammengeführten Daten zurückgegeben.|
|-2016345906|Die Antwort gibt an, dass nur ein Teil des Befehls abgeschlossen wurde.Wenn der restliche Befehl später abgeschlossen werden kann, SOLLTE nach Abschluss ein weiterer entsprechender Statuscode für die Abschlussanforderung erstellt werden.|
|-2016345907|Die Quelle SOLLTE ihren Inhalt aktualisieren.Dem Absender der Anforderung wird mitgeteilt, dass der Inhalt synchronisiert werden SOLLTE, um eine aktuelle Version zu erhalten.|
|-2016345908|Die Anforderung wurde erfolgreich abgeschlossen, aber es wurden keine Daten zurückgegeben.Der Antwortcode wird auch als Reaktion auf einen Get-Befehl zurückgegeben, wenn das Ziel keinen Inhalt hat.|
|-2016345909|Nicht-autoritative Antwort.Auf die Anforderung reagiert eine andere Entität als der vorgesehene Empfänger.Die Antwort wird nur zurückgegeben, wenn die Anforderung zu einem 200-Antwortcode vom autorisierenden Empfänger geführt hätte.|
|-2016345910|Zur Verarbeitung angenommen.Die Anforderung zur Remoteausführung einer Anwendung oder zum Warnen eines Benutzers oder einer Anwendung wurde erfolgreich durchgeführt.|
|-2016345911|Das angeforderte Element wurde hinzugefügt.|
|-2016345912|Der SyncML-Befehl wurde erfolgreich abgeschlossen.|
|-2016346011|Der angegebene SyncML-Befehl wird ausgeführt, wurde aber noch nicht abgeschlossen.|

## Siehe auch
[Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

