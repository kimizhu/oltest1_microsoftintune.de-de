---
description: na
keywords: na
title: Windows configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6982a2bc-aafa-475a-9236-4840b709e5a1
---
# Einstellungen f&#252;r Windows-Konfigurationsrichtlinien in Microsoft Intune
Verwenden Sie die **Windows-Konfigurationsrichtlinie** von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], um Einstellungen für registrierte Windows 8- und Windows 8.1-Geräte zu konfigurieren:

## Erstellen einer allgemeinen Windows-Konfigurationsrichtlinie

#### So geben Sie grundlegende Einstellungen für die Konfigurationsrichtlinie an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Klicken Sie auf **Windows** &gt; **Allgemeine Konfiguration (Windows 8.1 und höher)**, und klicken Sie dann auf **Richtlinie erstellen**.

    > [!NOTE]
    > Sie können keine Konfigurationsrichtlinie mit empfohlenen Einstellungen erstellen. Sie müssen eine benutzerdefinierte Richtlinie erstellen.

3.  Geben Sie im Abschnitt **Allgemein** der Seite **Richtlinie erstellen** einen Namen und eine Beschreibung für die neue Richtlinie ein.

4.  Befolgen Sie die Informationen in den folgenden Abschnitten zum Angeben von Einstellungen für die Richtlinie.

5.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## <a name="BKMK_Settings"></a>Einstellungen für registrierte Windows-Geräte

### <a name="BKMK_sec"></a>Sicherheitseinstellungen

|Name der Einstellung|Windows 8.1 und Windows RT 8.1|Windows RT|
|------------------------|----------------------------------|--------------|
|**Erforderlicher Kennworttyp**<br /><br />(gibt den erforderlichen Typ des Kennworts an, z. B. nur numerisch oder alphanumerisch)|Ja|Ja|
|**Erforderlicher Kennworttyp – Mindestanzahl von Zeichensätzen**<br /><br />Es gibt vier Zeichensätze: Kleinbuchstaben, Großbuchstaben, Zahlen und Symbole. Diese Einstellung gibt an, wie viele Zeichensätze im Kennwort enthalten sein müssen. Für iOS-Geräte wird hiermit jedoch die erforderliche Anzahl von Symbolzeichen im Kennwort angegeben.|Ja|Ja|
|**Minimale Kennwortlänge**<sup>1</sup>|Ja|Ja|
|**Anzahl zulässiger wiederholter Anmeldefehler, bevor das Gerät zurückgesetzt wird**|Ja|Ja|
|**Minuten der Inaktivität, bevor der Bildschirm ausgeschaltet wird**|Ja|Ja|
|**Kennwortablauf (Tage)**|Ja|Ja|
|**Kennwortverlauf speichern**|Ja|Ja|
|**Kennwortverlauf speichern** – **Wiederverwendung vorheriger Kennwörter verhindern**|Ja|Ja|
|**Bildkennwort und PIN zulassen**|Ja|Ja|
<sup>1</sup> Wenn Sie eine Kennwortlängenrichtlinie für Geräte mit Windows RT bereitstellen, müssen Benutzer ihr Kennwort zurücksetzen, selbst wenn ihr aktuelles Kennwort den Richtlinienanforderungen entspricht.

### Verschlüsselungseinstellungen

|Name der Einstellung|Windows 8.1 und Windows RT 8.1|Windows RT|
|------------------------|----------------------------------|--------------|
|**Verschlüsselung auf mobilem Gerät anfordern**<sup>1</sup><br /><br />Für Windows Phone 8-Geräte müssen Sie hier **Ja** festlegen.|Ja|Nein|
<sup>1</sup> Zusätzliche Informationen für Geräte die Windows 8.1 ausführen

-   Um die Verschlüsselung auf Geräten zu erzwingen, die Windows 8.1 ausführen, installieren Sie das [MDM-Clientupdate für Windows von Dezember 2014](http://support.microsoft.com/kb/3013816) auf jedem Gerät.

-   Wenn Sie diese Einstellung für Windows 8.1-Geräte aktivieren, müssen alle Benutzer des Geräts ein Microsoft-Konto haben.

-   Damit die Verschlüsselung funktioniert, muss das Gerät die Hardwarezertifizierungsanforderungen für Microsoft [InstantGo](http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/) erfüllen.

-   Wenn Sie die Verschlüsselung auf einem Gerät erzwingen, ist der Wiederherstellungsschlüssel nur über das Microsoft-Konto des Benutzers zugänglich, auf das dieser über sein eigenes OneDrive-Konto zugreift. Sie können diesen Schlüssel nicht im Auftrag eines Benutzers wiederherstellen.

### Malwareeinstellungen

|Name der Einstellung|Windows 8.1 und Windows RT 8.1|Windows RT|
|------------------------|----------------------------------|--------------|
|**Netzwerkfirewall erforderlich**|Ja|Nein|
|**SmartScreen aktivieren**|Ja|Nein|

### Systemeinstellungen

|Name der Einstellung|Windows 8.1 und Windows RT 8.1|Windows RT|
|------------------------|----------------------------------|--------------|
|**Automatische Updates erforderlich**|Ja|Nein|
|**Automatische Updates erforderlich – Mindestklassifizierung von Updates, die automatisch installiert werden** <sup>1</sup><br /><br />Wählen Sie die Klassifizierungen der Updates, die automatisch installiert werden:<br /><br />-   **Wichtig** – Installiert alle Updates, die als wichtig klassifiziert sind.<br />-   **Empfohlen** – Installiert alle Updates, die als wichtige oder empfohlene klassifiziert sind.|Ja|Nein|
|**Benutzerkontensteuerung**|Ja|Nein|
|**Übermitteln von Diagnosedaten zulassen**|Ja|Nein|
<sup>1</sup> Um die Verschlüsselung auf Geräten zu erzwingen, die Windows 8.1 ausführen, installieren Sie das [MDM-Clientupdate für Windows von Dezember 2014](http://support.microsoft.com/kb/3013816) auf jedem Gerät.

### <a name="BKMK_cloud"></a>Cloudeinstellungen – Dokumente und Daten

|Name der Einstellung|Windows 8.1 und Windows RT 8.1|Windows RT|
|------------------------|----------------------------------|--------------|
|**URL der Arbeitsordner**<br /><br />(legt die URL des Arbeitsordners so fest, dass Dokumente auf verschiedenen Geräten synchronisiert werden können)|Ja|Nein|

### <a name="BKMK_email"></a>E-Mail-Einstellungen

|Name der Einstellung|Windows 8.1 und Windows RT 8.1|Windows RT|
|------------------------|----------------------------------|--------------|
|**Microsoft-Konto in Windows Mail-Anwendung optional machen**|Ja|Nein|

### <a name="BKMK_browser"></a>Anwendungseinstellungen – Browser

|Name der Einstellung|Windows 8.1 und Windows RT 8.1|Windows RT|
|------------------------|----------------------------------|--------------|
|**AutoAusfüllen zulassen**|Ja|Nein|
|**Popupblocker zulassen**|Ja|Nein|
|**Plug-Ins zulassen**|Ja|Nein|
|**Active Scripting zulassen**|Ja|Nein|
|**Betrugswarnung zulassen**|Ja|Nein|
|**Wechsel zu Intranetsite nach Eingabe eines einzelnen Worts zulassen**<br /><br />(erlaubt die Verwendung eines einzelnen Wortes, um Internet Explorer auf eine Website wie "Bing" weiterzuleiten)|Ja|Nein|
|**Automatische Erkennung des Intranets zulassen**|Ja|Nein|
|**Sicherheitsstufe für Internet**|Ja|Nein|
|**Sicherheitsstufe für Intranet**|Ja|Nein|
|**Sicherheitsstufe für vertrauenswürdige Sites**|Ja|Nein|
|**Sicherheitsstufe für eingeschränkte Sites**|Ja|Nein|
|**Header "Nicht nachverfolgen" senden**|Ja|Nein|
|**Menüzugriff im Enterprise-Modus erlauben**|Ja|Nein|
|**Ort der Standortliste für Enterprise-Modus**|Ja|Nein|

### Einstellungen für Gerätefunktionen - Mobiltelefon

|Name der Einstellung|Windows 8.1 und Windows RT 8.1|Windows RT|
|------------------------|----------------------------------|--------------|
|**Datenroaming zulassen**|Ja|Nein|

## Bereitstellen der Konfigurationsrichtlinie

1.  Stellen Sie die Konfigurationsrichtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen im Arbeitsbereich **Richtlinie** identifizieren Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

