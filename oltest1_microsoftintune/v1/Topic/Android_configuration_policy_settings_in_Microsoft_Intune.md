---
description: na
keywords: na
title: Android configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71cc39cf-e726-40fd-8d08-78776e099a4b
---
# Einstellungen f&#252;r Android-Konfigurationsrichtlinien in Microsoft Intune
Verwenden Sie die allgemeine [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**Android-Konfigurationsrichtlinie** zum Konfigurieren von Einstellungen für:

-   **Sicherheitseinstellungen für mobile Geräte** – Treffen Sie in einer Liste mit vordefinierten Einstellungen eine Auswahl, mit denen Sie eine Reihe von Features und Funktionen auf dem Gerät steuern können.

-   **Kiosk-Modus** (nur für Samsung KNOX-Geräte) – Sperren Sie ein Gerät, sodass nur bestimmte Features ausgeführt werden können. Beispielsweise können Sie festlegen, dass auf einem Gerät nur eine von Ihnen angegebene verwaltete App ausgeführt werden kann, oder Sie können die Lautstärkeregler eines Geräts deaktivieren. Diese Einstellungen können für ein Demomodell eines Geräts oder ein Gerät nützlich sein, das nur eine bestimmte Funktion ausführen soll, wie z. B. ein Point-of-Sale-Gerät.

-   **Kompatible und nicht kompatible Apps** – Geben Sie eine Liste von Apps an, die in Ihrem Unternehmen kompatibel oder nicht kompatibel sind. Auf Android- und iOS-Geräten können Sie mit dem **Bericht über nicht kompatible Apps** überprüfen, ob die vom Benutzer installierten Apps zu den als von Ihnen kompatibel angegebenen Apps gehören (die Installation der App kann jedoch nicht blockiert werden).

> [!TIP]
> Sie können Bestimmungen für Benutzer konfigurieren, um sicherzustellen, dass sie bestätigen, dass Apps auf ihrem Gerät, einschließlich persönlicher Apps, ausgewertet werden und dass nicht kompatible Anwendungen entweder blockiert oder als nicht kompatibel gemeldet werden. Benutzer müssen diese Bestimmungen akzeptieren, bevor sie ihr Gerät registrieren und Apps über das Unternehmensportal abrufen können. Weitere Informationen zur Verwendung von Nutzungsbedingungen finden Sie unter [Arbeiten mit Nutzungsbedingungsrichtlinien in Microsoft Intune](http://msdn.microsoft.com/en-us/library/ce59fb93-01fd-4822-a57d-45ca7d89843d).

## Erstellen einer Android-Konfigurationsrichtlinie

#### So geben Sie grundlegende Einstellungen für die Konfigurationsrichtlinie an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Klicken Sie auf **Android** &gt; **Allgemeine Konfiguration**, und klicken Sie dann auf **Richtlinie erstellen**.

    > [!NOTE]
    > Sie können keine Konfigurationsrichtlinie mit empfohlenen Einstellungen erstellen. Sie müssen eine benutzerdefinierte Richtlinie erstellen.

3.  Geben Sie im Abschnitt **Allgemein** der Seite **Richtlinie erstellen** einen Namen und eine Beschreibung für die neue Richtlinie ein.

4.  Befolgen Sie die Informationen in den folgenden Abschnitten zum Angeben von Einstellungen für die Richtlinie.

5.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## <a name="BKMK_Settings"></a>Sicherheitsrichtlinieneinstellungen für mobile Android-Geräte
Wenn die gesuchte Einstellung nicht in dieser Liste enthalten ist, können Sie sie ggf. mithilfe einer benutzerdefinierten Android-Richtlinie erstellen, die Ihnen das Steuern des Geräts mithilfe von OMA-URI-Einstellungen erlaubt. Weitere Informationen finden Sie unter [Benutzerdefinierte Android-Richtlinieneinstellungen in Microsoft Intune](../Topic/Android_custom_policy_settings_in_Microsoft_Intune.md).

### <a name="BKMK_sec"></a>Kennworteinstellungen

|Name der Einstellung|Android 4.0+|Samsung KNOX|
|------------------------|----------------|----------------|
|**Anfordern eines Kennworts zum Entsperren mobiler Geräte**|Ja|Ja|
|**Minimale Kennwortlänge**|Ja|Ja|
|**Anzahl zulässiger wiederholter Anmeldefehler, bevor das Gerät zurückgesetzt wird**|Ja|Ja|
|**Minuten der Inaktivität, bevor der Bildschirm ausgeschaltet wird**|Ja|Ja|
|**Kennwortablauf (Tage)**|Ja|Ja|
|**Kennwortverlauf speichern**|Ja|Ja|
|**Kennwortverlauf speichern** – **Wiederverwendung vorheriger Kennwörter verhindern**|Ja|Ja|
|**Kennwortqualität**|Ja|Ja|
|**Fingerabdruckentsperrung zulassen**|Nein|Ja|

### Verschlüsselungseinstellungen

|Name der Einstellung|Android 4.0+|Samsung KNOX|
|------------------------|----------------|----------------|
|**Verschlüsselung auf mobilem Gerät anfordern**|Ja|Ja|
|**Verschlüsselung auf Speicherkarten vorschreiben**|Nein|Ja|

### Systemeinstellungen

|Name der Einstellung|Android 4.0+|Samsung KNOX|
|------------------------|----------------|----------------|
|**Bildschirmaufnahme zulassen**|Nein|Ja|
|**Übermitteln von Diagnosedaten zulassen**|Nein|Ja|
|**Zurücksetzen auf Werkseinstellungen zulassen**|Nein|Ja|

### <a name="BKMK_cloud"></a>Cloudeinstellungen – Dokumente und Daten

|Name der Einstellung|Android und Samsung KNOX|Android 4.0+|
|------------------------|----------------------------|----------------|
|**Google-Sicherung zulassen**|Nein|Ja|

### Cloudeinstellungen – Konten und Synchronisierung

|Name der Einstellung|Android 4.0+|Samsung KNOX|
|------------------------|----------------|----------------|
|**Automatische Synchronisierung mit Google-Konto zulassen**|Nein|Ja|

### <a name="BKMK_browser"></a>Anwendungseinstellungen – Browser

|Name der Einstellung|Android 4.0+|Samsung KNOX|
|------------------------|----------------|----------------|
|**Webbrowser zulassen**|Nein|Ja|
|**AutoAusfüllen zulassen**|Nein|Ja|
|**Popupblocker zulassen**|Nein|Ja|
|**Cookies zulassen**|Nein|Ja|
|**Active Scripting zulassen**|Nein|Ja|

### <a name="BKMK_apps"></a>Anwendungseinstellungen – Apps

|Name der Einstellung|Android 4.0+|Samsung KNOX|
|------------------------|----------------|----------------|
|**Google Play Store zulassen**|Nein|Ja|

### <a name="BKMK_hard"></a>Einstellungen für Gerätefunktionen - Hardware

|Name der Einstellung|Android 4.0+|Samsung KNOX|
|------------------------|----------------|----------------|
|**Kamera zulassen**|Ja|Ja|
|**Wechselspeichermedien zulassen**|Nein|Ja|
|**WLAN zulassen**|Nein|Ja|
|**WLAN-Tethering zulassen**|Nein|Ja|
|**Geolocation zulassen**<br /><br />(erlaubt dem Gerät die Nutzung von Standortinformationen)|Nein|Ja|
|**NFC zulassen**<br /><br />(erlaubt Vorgänge, die NFC bzw. Near Field Communication verwenden)|Nein|Ja|
|**Bluetooth zulassen**|Nein|Ja|
|**Ausschalten zulassen**<sup>1</sup>|Nein|Ja|
<sup>1</sup> Wenn diese Einstellung deaktiviert ist, funktioniert die Einstellung **Anzahl der zulässigen wiederholten Anmeldefehler, bevor die Gerätedaten zurückgesetzt werden** für Samsung KNOX-Geräte nicht.

### Einstellungen für Gerätefunktionen - Mobiltelefon

|Name der Einstellung|Android 4.0+|Samsung KNOX|
|------------------------|----------------|----------------|
|**Sprachroaming zulassen**|Nein|Ja|
|**Datenroaming zulassen**|Nein|Ja|
|**SMS/MMS-Messaging zulassen**|Nein|Ja|

### Einstellungen für Gerätefunktionen - Funktionen

|Name der Einstellung|Android 4.0+|Samsung KNOX|
|------------------------|----------------|----------------|
|**Sprach-Assistent zulassen**|Nein|Ja|
|**Sprachwahl zulassen**|Nein|Ja|
|**Kopieren und Einfügen zulassen**|Nein|Ja|
|**Freigabe der Zwischenablage zwischen Anwendungen zulassen**|Nein|Ja|
|**YouTube zulassen**|Nein|Ja|

## Einstellungen für kompatible und nicht kompatible Anwendungen
Geben Sie in der **Liste der kompatiblen und nicht kompatiblen Apps** eine Liste kompatibler oder nicht kompatibler mit den folgenden Informationen ein:

> [!NOTE]
> Eine einzelne Richtlinie kann nur eine Liste kompatibler oder eine Liste nicht kompatibler Apps enthalten. Sie können nicht beide Typen in derselben Richtlinie angeben.

|Name der Einstellung|Weitere Informationen|
|------------------------|-------------------------|
|**Nichtkompatibilität melden, wenn Benutzer die aufgelisteten Apps installieren**|Listet die Apps auf, die nicht von Intune verwaltet werden und die Benutzer nicht installieren und ausführen dürfen.|
|**Nichtkompatibilität nicht melden, wenn Benutzer die aufgelisteten Apps installieren**|Listet die Apps auf, die Benutzer installieren dürfen. Benutzer können keine anderen Apps installieren. Apps, die von Intune verwaltet werden, sind automatisch zugelassen.|
|**Hinzufügen**|Fügt eine App zur ausgewählten Liste hinzu. Geben Sie einen Namen Ihrer Wahl sowie die URL zur App im App-Store und optional den Herausgeber der App an.<br /><br />[Angeben von URLs zu App-Stores](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md#BKMK_URL)|
|**Anwendungen importieren**|Importiert eine Liste von Apps, die Sie in einer CSV-Datei angegeben haben. Verwenden Sie in der Datei das Format Anwendungsname, Herausgeber und App-URL.|
|**Bearbeiten**|Ermöglicht Ihnen das Bearbeiten von Name, Herausgeber und URL der ausgewählten App.|
|**Löschen**|Löscht die ausgewählte App aus der Liste.|

## Einstellungen für den Kioskmodus
Geben Sie die folgenden Einstellungen für **Samsung KNOX-Geräte** an:

|Name der Einstellung|Weitere Informationen|
|------------------------|-------------------------|
|**Wählen Sie eine verwalteten App aus, die ausgeführt werden darf, während sich das Gerät im Kiosk-Modus befindet**|Klicken Sie auf **Durchsuchen**, und wählen Sie dann eine verwaltete App oder eine App aus einem Store aus, die ausgeführt werden darf, wenn sich das Gerät im Kiosk-Modus befindet. Andere Apps dürfen auf dem Gerät nicht ausgeführt werden.<br /><br />[Angeben von URLs zu App-Stores](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md#BKMK_URL)|
|**Lautstärkeregler zulassen**|Aktiviert oder deaktiviert die Verwendung der Lautstärkeregler am Gerät.|
|**Schaltfläche für Standby und Aktivieren zulassen**|Aktiviert oder deaktiviert die Taste für Standby/Aktivierung des Bildschirms am Gerät.|

## Bereitstellen der Konfigurationsrichtlinie

1.  Stellen Sie die Konfigurationsrichtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen im Arbeitsbereich **Richtlinie** identifizieren Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

## Referenzinformationen für kompatible und nicht kompatible Apps

### Überwachen kompatibler und nicht kompatibler Apps
Im **Bericht über nicht kompatible Apps** können Sie sich über die Konformität zulässiger und blockierter Anwendungen informieren.

##### So führen Sie den Bericht über nicht kompatible Apps aus

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Berichte** &gt; **Bericht über nicht kompatible Apps**.

2.  Wählen Sie die Gerätegruppen aus, die Sie überprüfen möchten, geben Sie an, ob Sie nach kompatiblen und/oder nicht kompatiblen Apps suchen möchten, und klicken Sie dann auf **Bericht anzeigen**.

### <a name="BKMK_URL"></a>Angeben von URLs zu App-Stores
Um eine App-URL in der Liste mit kompatiblen und nicht kompatiblen Apps oder in der Option **Verwaltete App auswählen, die ausgeführt werden darf, wenn sich das Gerät im Kioskmodus befindet (nur iOS)** anzugeben, verwenden Sie das folgende Format:

Suchen Sie im [Apps-Bereich von Google Play](https://play.google.com/store/apps) nach der App, die Sie verwenden möchten.

Öffnen Sie die Installationsseite für die App, und kopieren Sie die URL in die Zwischenablage. Jetzt können Sie diese als URL in der Liste mit kompatiblen oder nicht kompatiblen Apps verwenden.

**Beispiel:** Suchen Sie in Google Play nach „Microsoft Office Mobile“. Die URL, die Sie verwenden, ist **https://play.google.com/store/apps/details?id=com.microsoft.office.officehub**.

## Nächste Schritte

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

