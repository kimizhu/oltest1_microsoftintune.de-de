---
description: na
keywords: na
title: Windows Phone configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 83f7469c-272e-43f2-8139-b0d7bc34f43f
---
# Einstellungen f&#252;r Windows Phone-Konfigurationsrichtlinien in Microsoft Intune
Konfigurieren Sie mithilfe der [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**allgemeinen Windows Phone-Konfigurationsrichtlinie** die folgenden Einstellungen für Windows Phone 8.1-Geräte:

-   **Sicherheitseinstellungen für mobile Geräte** – Treffen Sie in einer Liste mit vordefinierten Einstellungen eine Auswahl, mit denen Sie eine Reihe von Features und Funktionen auf dem Gerät steuern können.

-   **Kompatible und nicht kompatible Apps** – Geben Sie eine Liste von Apps an, die in Ihrem Unternehmen kompatibel oder nicht kompatibel sind. Die Installation dieser Apps kann auf Windows Phone-Geräten blockiert oder zugelassen werden.

## Erstellen einer allgemeinen Windows Phone-Konfigurationsrichtlinie

#### So geben Sie grundlegende Einstellungen für die Konfigurationsrichtlinie an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Klicken Sie auf **Windows** &gt; **Allgemeine Konfiguration (Windows 8.1 und höher)**, und klicken Sie dann auf **Richtlinie erstellen**.

    > [!NOTE]
    > Sie können keine Konfigurationsrichtlinie mit empfohlenen Einstellungen erstellen. Sie müssen eine benutzerdefinierte Richtlinie erstellen.

3.  Geben Sie im Abschnitt **Allgemein** der Seite **Richtlinie erstellen** einen Namen und eine Beschreibung für die neue Richtlinie ein.

4.  Befolgen Sie die Informationen in den folgenden Abschnitten zum Angeben von Einstellungen für die Richtlinie.

5.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## <a name="BKMK_Settings"></a>Einstellungen für Windows Phone

### <a name="BKMK_sec"></a>Sicherheitseinstellungen

|Name der Einstellung|Windows Phone 8 und Windows Phone 8.1|
|------------------------|-----------------------------------------|
|**Anfordern eines Kennworts zum Entsperren mobiler Geräte**|Ja|
|**Erforderlicher Kennworttyp**<br /><br />(gibt den erforderlichen Typ des Kennworts an, z. B. nur numerisch oder alphanumerisch)|Ja|
|**Erforderlicher Kennworttyp – Mindestanzahl von Zeichensätzen**<br /><br />Es gibt vier Zeichensätze: Kleinbuchstaben, Großbuchstaben, Zahlen und Symbole. Diese Einstellung gibt an, wie viele Zeichensätze im Kennwort enthalten sein müssen. Für iOS-Geräte wird hiermit jedoch die erforderliche Anzahl von Symbolzeichen im Kennwort angegeben.|Ja|
|**Minimale Kennwortlänge**|Ja|
|**Einfache Kennwörter zulassen**<br /><br />Einfache Kennwörter enthalten '0000' und '1234'.|Ja|
|**Anzahl zulässiger wiederholter Anmeldefehler, bevor das Gerät zurückgesetzt wird**|Ja|
|**Minuten der Inaktivität, bevor der Bildschirm ausgeschaltet wird**|Ja|
|**Kennwortablauf (Tage)**|Ja|
|**Kennwortverlauf speichern**|Ja|
|**Kennwortverlauf speichern** – **Wiederverwendung vorheriger Kennwörter verhindern**|Ja|

### Verschlüsselungseinstellungen

|Name der Einstellung|Windows Phone 8 und Windows Phone 8.1|
|------------------------|-----------------------------------------|
|**Verschlüsselung auf mobilem Gerät anfordern**<br /><br />Für Windows Phone 8-Geräte müssen Sie hier **Ja** festlegen.|Ja|

### Systemeinstellungen

|Name der Einstellung|Windows Phone 8 und Windows Phone 8.1|
|------------------------|-----------------------------------------|
|**Bildschirmaufnahme zulassen**|Nur Windows Phone 8.1|
|**Übermitteln von Diagnosedaten zulassen**|Nur Windows Phone 8.1|

### Cloudeinstellungen – Konten und Synchronisierung

|Name der Einstellung|Windows Phone 8 und Windows Phone 8.1|
|------------------------|-----------------------------------------|
|**Microsoft-Konto erlauben**|Nur Windows Phone 8.1|

### <a name="BKMK_email"></a>E-Mail-Einstellungen

|Name der Einstellung|Windows Phone 8 und Windows Phone 8.1|
|------------------------|-----------------------------------------|
|**Benutzerdefinierte E-Mail-Konten erlauben**|Nur Windows Phone 8.1|

### <a name="BKMK_browser"></a>Anwendungseinstellungen – Browser

|Name der Einstellung|Windows Phone 8 und Windows Phone 8.1|
|------------------------|-----------------------------------------|
|**Webbrowser zulassen**|Nur Windows Phone 8.1|

### <a name="BKMK_apps"></a>Anwendungseinstellungen – Apps

|Name der Einstellung|Windows Phone 8 und Windows Phone 8.1|
|------------------------|-----------------------------------------|
|**App Store zulassen**|Nur Windows Phone 8.1|

### <a name="BKMK_hard"></a>Einstellungen für Gerätefunktionen - Hardware

|Name der Einstellung|Windows Phone 8 und Windows Phone 8.1|
|------------------------|-----------------------------------------|
|**Kamera zulassen**|Nur Windows Phone 8.1|
|**Wechselspeichermedien zulassen**|Ja|
|**WLAN zulassen**|Nur Windows Phone 8.1|
|**WLAN-Tethering zulassen**|Nur Windows Phone 8.1|
|**Automatische Verbindung mit unverschlüsselten WLAN-Hotspots zulassen**|Nur Windows Phone 8.1|
|**Berichterstellung für WLAN-Hotspots zulassen**<br /><br />(Informationen über WLAN-Verbindungen senden, um nahegelegene Verbindungen zu ermitteln)|Nur Windows Phone 8.1|
|**Geolocation zulassen**<br /><br />(erlaubt dem Gerät die Nutzung von Standortinformationen)|Nur Windows Phone 8.1|
|**NFC zulassen**<br /><br />(erlaubt Vorgänge, die NFC bzw. Near Field Communication verwenden)|Nur Windows Phone 8.1|
|**Bluetooth zulassen**|Nur Windows Phone 8.1|

### Einstellungen für Gerätefunktionen - Funktionen

|Name der Einstellung|Windows Phone 8 und Windows Phone 8.1|
|------------------------|-----------------------------------------|
|**Kopieren und Einfügen zulassen**|Nur Windows Phone 8.1|

## Einstellungen für kompatible und nicht kompatible Anwendungen
Geben Sie in der **Liste der kompatiblen und nicht kompatiblen Apps** eine Liste kompatibler oder nicht kompatibler mit den folgenden Informationen ein:

> [!NOTE]
> Eine einzelne Richtlinie kann nur eine Liste kompatibler oder eine Liste nicht kompatibler Apps enthalten. Sie können nicht beide Typen in derselben Richtlinie angeben.

|Name der Einstellung|Weitere Informationen|
|------------------------|-------------------------|
|**Öffnen der aufgelisteten Anwendungen durch die Geräte blockieren**|Listet die Apps auf, die nicht von Intune verwaltet werden und die Benutzer nicht installieren und ausführen dürfen.|
|**Geräten nur erlauben, die aufgelisteten Anwendungen zu installieren**|Listet die Apps auf, die Benutzer installieren dürfen. Benutzer können keine anderen Apps installieren. Apps, die von Intune verwaltet werden, sind automatisch zugelassen.|
|**Hinzufügen**|Fügt eine App zur ausgewählten Liste hinzu. Geben Sie einen Namen Ihrer Wahl sowie die URL zur App im App-Store und optional den Herausgeber der App an.<br /><br />[Angeben von URLs zu App-Stores](../Topic/Windows_Phone_configuration_policy_settings_in_Microsoft_Intune.md#BKMK_URL)|
|**Anwendungen importieren**|Importiert eine Liste von Apps, die Sie in einer CSV-Datei angegeben haben. Verwenden Sie in der Datei das Format Anwendungsname, Herausgeber und App-URL.|
|**Bearbeiten**|Ermöglicht Ihnen das Bearbeiten von Name, Herausgeber und URL der ausgewählten App.|
|**Löschen**|Löscht die ausgewählte App aus der Liste.|
> [!IMPORTANT]
> Wenn Sie eine Liste von zulässigen Apps für Windows Phone 8.1-Geräte angeben, müssen Sie die Unternehmensportal-App zu dieser Liste hinzufügen, da sie andernfalls blockiert wird.

## Bereitstellen der Konfigurationsrichtlinie

1.  Stellen Sie die Konfigurationsrichtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen im Arbeitsbereich **Richtlinie** identifizieren Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

## Referenzinformationen für kompatible und nicht kompatible Apps

### <a name="BKMK_URL"></a>Angeben von URLs zu App-Stores
Verwenden Sie zum Festlegen einer App-URL in der Liste konformer und nicht konformer Apps das folgende Format:

Suchen Sie auf der [Windows Phone-Seite für Apps und Spiele](http://www.windowsphone.com/en-us/store/overview) nach der App, die Sie verwenden möchten.

Öffnen Sie die Seite der App, und kopieren Sie die URL in die Zwischenablage. Jetzt können Sie diese als URL in der Liste mit kompatiblen oder nicht kompatiblen Apps verwenden.

**Beispiel:** Durchsuchen Sie den Store nach der App „Skype“. Die URL, die Sie verwenden, ist **http://www.windowsphone.com/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51**.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

