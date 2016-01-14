---
description: na
keywords: na
title: iOS configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab46be6c-ab73-4c99-8492-66d1dd418293
---
# Einstellungen f&#252;r iOS-Konfigurationsrichtlinien in Microsoft Intune
Verwenden Sie die allgemeine [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**iOS-Konfigurationsrichtlinie** zum Konfigurieren von Einstellungen für:

-   **Sicherheitseinstellungen für mobile Geräte** – Treffen Sie in einer Liste mit vordefinierten Einstellungen eine Auswahl, mit denen Sie eine Reihe von Features und Funktionen auf dem Gerät steuern können.

-   **Kioskmodus** – Sie können ein Gerät so konfigurieren, dass nur bestimmte Features funktionieren. Beispielsweise können Sie festlegen, dass auf einem Gerät nur eine von Ihnen angegebene verwaltete App ausgeführt werden kann, oder Sie können die Lautstärkeregler eines Geräts deaktivieren. Diese Einstellungen können für ein Demomodell eines Geräts oder ein Gerät nützlich sein, das nur eine bestimmte Funktion ausführen soll, wie z. B. ein Point-of-Sale-Gerät.

-   **Kompatible und nicht kompatible Apps** – Geben Sie eine Liste von Apps an, die in Ihrem Unternehmen kompatibel oder nicht kompatibel sind. Auf Android- und iOS-Geräten können Sie mit dem **Bericht über nicht kompatible Apps** überprüfen, ob die vom Benutzer installierten Apps zu den als von Ihnen kompatibel angegebenen Apps gehören (die Installation der App kann jedoch nicht blockiert werden).

> [!TIP]
> Sie können Bestimmungen für Benutzer konfigurieren, um sicherzustellen, dass sie bestätigen, dass Apps auf ihrem Gerät, einschließlich persönlicher Apps, ausgewertet werden und dass nicht kompatible Anwendungen entweder blockiert oder als nicht kompatibel gemeldet werden. Benutzer müssen diese Bestimmungen akzeptieren, bevor sie ihr Gerät registrieren und Apps über das Unternehmensportal abrufen können. Weitere Informationen zur Verwendung von Nutzungsbedingungen finden Sie unter [Arbeiten mit Nutzungsbedingungsrichtlinien in Microsoft Intune](http://msdn.microsoft.com/en-us/library/ce59fb93-01fd-4822-a57d-45ca7d89843d).

## Erstellen einer allgemeinen iOS-Konfigurationsrichtlinie

#### So geben Sie grundlegende Einstellungen für die Konfigurationsrichtlinie an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Klicken Sie auf **iOS** &gt; **Allgemeine Konfiguration**, und klicken Sie dann auf **Richtlinie erstellen**.

    > [!NOTE]
    > Sie können keine Konfigurationsrichtlinie mit empfohlenen Einstellungen erstellen. Sie müssen eine benutzerdefinierte Richtlinie erstellen.

3.  Geben Sie im Abschnitt **Allgemein** der Seite **Richtlinie erstellen** einen Namen und eine Beschreibung für die neue Richtlinie ein.

4.  Befolgen Sie die Informationen in den folgenden Abschnitten zum Angeben von Einstellungen für die Richtlinie.

5.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## <a name="BKMK_Settings"></a>Einstellungen für iOS-Geräte
Wenn die gesuchte Einstellung nicht in dieser Liste enthalten ist, können Sie sie ggf. mithilfe einer benutzerdefinierten iOS-Richtlinie erstellen, die Ihnen das Importieren von Einstellungen erlaubt, die Sie mit dem [Apple Configurator Tool](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) erstellt haben. Weitere Informationen finden Sie unter [Benutzerdefinierte iOS-Richtlinieneinstellungen in Microsoft Intune](../Topic/iOS_custom_policy_settings_in_Microsoft_Intune.md).

### <a name="BKMK_sec"></a>Sicherheitseinstellungen

|Name der Einstellung|iOS|
|------------------------|-------|
|**Anfordern eines Kennworts zum Entsperren mobiler Geräte**|Ja|
|**Erforderlicher Kennworttyp**<br /><br />(gibt den erforderlichen Typ des Kennworts an, z. B. nur numerisch oder alphanumerisch)|Ja|
|**Erforderlicher Kennworttyp – Mindestanzahl von Zeichensätzen**<br /><br />Es gibt vier Zeichensätze: Kleinbuchstaben, Großbuchstaben, Zahlen und Symbole. Diese Einstellung gibt an, wie viele Zeichensätze im Kennwort enthalten sein müssen. Für iOS-Geräte wird hiermit jedoch die erforderliche Anzahl von Symbolzeichen im Kennwort angegeben.|Ja|
|**Minimale Kennwortlänge**|Ja|
|**Einfache Kennwörter zulassen**<br /><br />Einfache Kennwörter enthalten '0000' und '1234'.|Ja|
|**Anzahl zulässiger wiederholter Anmeldefehler, bevor das Gerät zurückgesetzt wird**|Ja|
|**Minuten der Inaktivität, bevor der Bildschirm ausgeschaltet wird**<sup>1</sup>|Ja|
|**Kennwortablauf (Tage)**|Ja|
|**Kennwortverlauf speichern**|Ja|
|**Kennwortverlauf speichern** – **Wiederverwendung vorheriger Kennwörter verhindern**|Ja|
|**Minuten der Inaktivität, bevor ein Kennwort erforderlich ist**<sup>1</sup>|Ja|
|**Fingerabdruckentsperrung zulassen**|iOS 7.1 und höher|
<sup>1</sup> Wenn Sie für iOS-Geräte die Einstellungen **Minuten der Inaktivität, bevor der Bildschirm ausgeschaltet wird** und **Minuten Inaktivität vor erneuter Anforderung des Kennworts** konfigurieren, werden sie nacheinander angewendet. Wenn Sie beispielsweise den Wert für beide Einstellungen auf **5** Minuten einstellen, wird der Bildschirm automatisch nach 5 Minuten deaktiviert, und das Gerät wird nach weiteren 5 Minuten gesperrt. Wenn der Benutzer den Bildschirm jedoch manuell deaktiviert, wird die zweite Einstellung sofort angewendet. Im selben Beispiel wird das Gerät 5 Minuten später gesperrt, nachdem der Benutzer den Bildschirm deaktiviert hat.

### Systemeinstellungen

|Name der Einstellung|iOS|
|------------------------|-------|
|**Bildschirmfoto zulassen**|Ja|
|**Kontrollcenter auf Sperrbildschirm zulassen**|iOS 7.1 und höher|
|**Benachrichtigungsansicht auf Sperrbildschirm zulassen**|iOS 7.1 und höher|
|**Ansicht "Heute" auf Sperrbildschirm zulassen**|iOS 7.1 und höher|
|**Übermitteln von Diagnosedaten zulassen**|Ja|
|**Nicht vertrauenswürdige TLS-Zertifikate zulassen**|Ja|
|**Passbook bei Sperre zulassen**|Ja|

### <a name="BKMK_cloud"></a>Cloudeinstellungen – Dokumente und Daten

|Name der Einstellung|iOS|
|------------------------|-------|
|**Sicherung in iCloud zulassen**|Ja|
|**Dokumentsynchronisierung in iCloud zulassen**|Ja|
|**Photo Stream-Synchronisierung in iCloud zulassen**|Ja|
|**Verschlüsselte Sicherung erforderlich**|Ja|

### <a name="BKMK_browser"></a>Anwendungseinstellungen – Browser

|Name der Einstellung|iOS|
|------------------------|-------|
|**Safari zulassen**|Ja|
|**AutoAusfüllen zulassen**|Ja|
|**Popupblocker zulassen**|Ja|
|**Cookies zulassen**|Ja|
|**JavaScript zulassen**|Ja|
|**Betrugswarnung zulassen**|Ja|

### <a name="BKMK_apps"></a>Anwendungseinstellungen – Apps

|Name der Einstellung|iOS|
|------------------------|-------|
|**App Store zulassen**|Ja|
|**Kennwort für den Zugriff auf den Anwendungsspeicher erforderlich**|Ja|
|**In-App-Einkäufe zulassen**|Ja|
|**Verwaltete Dokumente in anderen nicht verwalteten Apps zulassen**|iOS 7.1 und höher|
|**Nicht verwaltete Dokumente in anderen verwalteten Apps zulassen**|iOS 7.1 und höher|
|**Videokonferenz zulassen**|Ja|
|**Nicht jugendfreie Inhalte im Medienstore zulassen**|Ja|

### Anwendungseinstellungen – Spiele

|Name der Einstellung|iOS|
|------------------------|-------|
|**Hinzufügung von Game Center-Freunden zulassen**|Ja|
|**Spielen für mehrere Spieler zulassen**|Ja|

### <a name="BKMK_hard"></a>Einstellungen für Gerätefunktionen - Hardware

|Name der Einstellung|iOS|
|------------------------|-------|
|**Kamera zulassen**|Ja|

### Einstellungen für Gerätefunktionen - Mobiltelefon

|Name der Einstellung|iOS|
|------------------------|-------|
|**Sprachroaming zulassen**|Ja|
|**Datenroaming zulassen**|Ja|
|**Globales Abrufen im Hintergrund beim Roaming zulassen**|Ja|

### Einstellungen für Gerätefunktionen - Funktionen

|Name der Einstellung|iOS|
|------------------------|-------|
|**Siri zulassen**|Ja|
|**Siri bei gesperrtem Gerät zulassen**|Ja|
|**Sprachwahl zulassen**|Ja|
|**Freigabe der Zwischenablage zwischen Anwendungen zulassen**|Nein|
|**YouTube zulassen**|Nein|

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
Geben Sie die folgenden Einstellungen für **iOS-Geräte** an:

|Name der Einstellung|Weitere Informationen|
|------------------------|-------------------------|
|**Wählen Sie eine verwalteten App aus, die ausgeführt werden darf, während sich das Gerät im Kiosk-Modus befindet**|Klicken Sie auf **Durchsuchen**, und geben Sie dann die verwaltete App oder eine App aus einem Store an, die ausgeführt werden darf, wenn sich das Gerät im Kiosk-Modus befindet. Andere Apps dürfen auf dem Gerät nicht ausgeführt werden.<br /><br />[Angeben von URLs zu App-Stores](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md#BKMK_URL).|
|**Toucheingabe zulassen**|Aktiviert oder deaktiviert den Touchscreen des Geräts.|
|**Bildschirmdrehung zulassen**|Aktiviert oder deaktiviert die Funktion zum Ändern der Bildschirmausrichtung, wenn Sie das Gerät drehen.|
|**Lautstärkeregler zulassen**|Aktiviert oder deaktiviert die Verwendung der Lautstärkeregler am Gerät.|
|**Ruftonschalter zulassen**|Aktiviert oder deaktiviert den Ruftonschalter (Stummschaltung) am Gerät.|
|**Schaltfläche für Standby und Aktivieren zulassen**|Aktiviert oder deaktiviert die Taste für Standby/Aktivierung des Bildschirms am Gerät.|
|**Automatische Sperrung zulassen**|Aktiviert oder deaktiviert die automatische Sperrung des Geräts.|
|**Mono-/Audio aktivieren**|Aktiviert oder deaktiviert die Barrierefreiheitseinstellung **Mono/Audio**.|
|**Voice-over aktivieren**|Aktiviert oder deaktiviert die Barrierefreiheitseinstellung **VoiceOver**, die den Text auf dem Gerätedisplay laut vorliest.|
|**Voice-over-Anpassungen aktivieren**|Aktiviert oder deaktiviert Voice-over-Anpassungen, die Ihnen das Anpassen der VoiceOver-Funktion ermöglichen (z. B. wie schnell Bildschirmtext vorgelesen wird).|
|**Zoom aktivieren**|Aktiviert oder deaktiviert die Barrierefreiheitseinstellung **Zoom**, die Ihnen das Vergrößern des Texts auf dem Gerätedisplay durch Toucheingabe ermöglicht.|
|**Zoom-Anpassungen aktivieren**|Aktiviert oder deaktiviert Zoom-Anpassungen zum individuellen Einrichten der Zoomfunktion.|
|**Farben umkehren zulassen**|Aktiviert oder deaktiviert die Barrierefreiheitseinstellung **Farben umkehren**, die die Anzeige für Benutzer mit eingeschränkter Sehfähigkeit anpasst.|
|**Farbumkehr-Anpassungen aktivieren**|Aktiviert oder deaktiviert Farbumkehr-Anpassungen, mit denen Sie die Funktion zur Farbumkehr individuell einrichten können.|
|**Touch-Unterstützung aktivieren**|Aktiviert oder deaktiviert die Barrierefreiheitseinstellung **Touch-Unterstützung**, die Benutzer bei der Ausführung von Bildschirmgesten unterstützt, die ihnen Schwierigkeiten bereiten.|
|**Touch-Unterstützungsanpassungen aktivieren**|Aktiviert oder deaktiviert Touch-Unterstützungsanpassungen, mit denen Sie die Funktion der Touch-Unterstützung individuell einrichten können.|
|**Sprachauswahl aktivieren**|Aktiviert oder deaktiviert die Barrierefreiheitseinstellung **Sprachauswahl**, mit der ausgewählter Text vorgelesen werden kann.|
> [!NOTE]
> Die folgenden Hinweise gelten für Kiosk-Moduseinstellungen für iOS-Geräte:
> 
> -   Bevor Sie ein iOS-Gerät für den Kiosk-Modus konfigurieren können, müssen Sie das Gerät mithilfe des [Apple Configurator-Tools](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) oder des Geräteregistrierungs-Managers in den überwachten Modus versetzen. Weitere Informationen zum Apple Configurator-Tool finden Sie in der Apple-Dokumentation.
> -   Wenn die angegebene iOS-App nach der Bereitstellung der Konfigurationsrichtlinie installiert wird, wird das Gerät erst nach einem Neustart in den Kiosk-Modus versetzt.

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

Suchen Sie mithilfe einer Suchmaschine die gewünschte App im iTunes App Store, und öffnen Sie die Seite für die App.

Kopieren Sie die URL der Seite, und verwenden Sie diese als URL zur Konfiguration der Liste kompatibler oder nicht kompatibler Apps oder der App, die Sie im Kioskmodus ausführen möchten.

**Beispiel:** Suche nach **Microsoft Word for iPad**. Die URL, die Sie verwenden, ist **https://itunes.apple.com/us/app/microsoft-word-for-ipad/id586447913?mt=8**.

> [!NOTE]
> Sie können auch die iTunes-Software verwenden, um die App zu suchen, und dann den Befehl **Link kopieren**, um die App-URL abzurufen.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

