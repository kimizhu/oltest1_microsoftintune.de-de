---
description: na
keywords: na
title: Windows 10 configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 00a602d9-b339-4fd8-ab70-defbf6686855
---
# Einstellungen f&#252;r Windows&#160;10-Konfigurationsrichtlinien in Microsoft Intune
Verwenden Sie die [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**allgemeine -Konfigurationsrichtlinie** für Windows 10, um Einstellungen für registrierte Windows 10 Desktop- und Windows 10 Mobile-Geräte zu konfigurieren:

## Erstellen einer allgemeinen Konfigurationsrichtlinie für Windows 10

#### So geben Sie grundlegende Einstellungen für die Konfigurationsrichtlinie an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Klicken Sie auf **Windows** &gt; **Allgemeine Konfiguration (Windows 10 Desktop und Windows 10 Mobile und höher)**, und klicken Sie dann auf **Richtlinie erstellen**.

    > [!NOTE]
    > Sie können keine Konfigurationsrichtlinie mit empfohlenen Einstellungen erstellen. Sie müssen eine benutzerdefinierte Richtlinie erstellen.

3.  Geben Sie im Abschnitt **Allgemein** der Seite **Richtlinie erstellen** einen Namen und eine Beschreibung für die neue Richtlinie ein.

4.  Befolgen Sie die Informationen in den folgenden Abschnitten zum Angeben von Einstellungen für die Richtlinie.

5.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## Sicherheitseinstellungen

### Kennwort

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**Anfordern eines Kennworts zum Entsperren von Geräten**|Ja|Ja|
|**Erforderlicher Kennworttyp**<br /><br />(Gibt den erforderlichen Typ des Kennworts an, z. B. nur numerisch oder alphanumerisch)|Ja|Ja|
|**Erforderlicher Kennworttyp** – **Mindestanzahl von Zeichensätzen**<br /><br />Es gibt vier Zeichensätze: Kleinbuchstaben, Großbuchstaben, Zahlen und Symbole. Diese Einstellung gibt an, wie viele Zeichensätze im Kennwort enthalten sein müssen.|Ja|Ja|
|**Minimale Kennwortlänge (nur Windows 10 Desktop)** **Important:** Diese Einstellung wird nicht mehr unterstützt und künftig entfernt. Sie können die nachfolgende Einstellung für Windows 10 Mobile für Desktopcomputer verwenden.|Ja|Nein|
|**Minimale Kennwortlänge (nur Windows 10 Mobile)**|Nein|Ja|
|**Anzahl zulässiger wiederholter Anmeldefehler, bevor das Gerät zurückgesetzt wird**|Ja|Ja|
|**Minuten der Inaktivität, bevor der Bildschirm ausgeschaltet wird**|Ja|Ja|
|**Kennwortablauf (Tage)**|Ja|Ja|
|**Kennwortverlauf speichern**|Ja|Ja|
|**Kennwortverlauf speichern** – **Wiederverwendung vorheriger Kennwörter verhindern**|Ja|Ja|
|**Bildkennwort und PIN zulassen**<br /><br />Ermöglicht Ihnen die Verwendung einfacher Gesten auf einem Bild oder einer einfachen PIN zur Anmeldung.|Ja|Nein|
|**Kennwort anfordern, wenn das Gerät aus dem Leerlauf zurückkehrt**|Nein|Ja|

### Verschlüsselung

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**Verschlüsselung auf mobilem Gerät anfordern**|Nein|Ja|

### System

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**Bildschirmaufnahme zulassen**|Nein|Ja|
|**Manuelles Aufheben der Registrierung zulassen**<br /><br />Ermöglicht dem Benutzer das manuelle Löschen des Unternehmensbereichskontos vom Gerät.|Ja|Ja|
|**Manuelle Installation des Stammzertifikats zulassen**<br /><br />Gibt an, ob der Benutzer Stammzertifikate manuell installieren kann.|Nein|Ja|
|**Senden von Diagnose- und Verwendungsdaten an Microsoft zulassen**|Ja|Ja|

## Cloud-Einstellungen

### Konto und Synchronisierung

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**Microsoft-Konto erlauben**|Ja|Ja|
|**Manuelles Hinzufügen von Nicht-Microsoft-Konten zulassen**|Ja|Ja|
|**Synchronisierung von Einstellungen für Microsoft-Konten zulassen**|Ja|Ja|

## E-Mail-Einstellungen

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**Microsoft-Konto in Windows Mail-Anwendung optional machen**|Ja|Nein|

## Anwendungseinstellungen

### Microsoft Edge

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**Webbrowser zulassen**|Nein|Ja|
|**Suchvorschläge auf der Adressleiste zulassen**|Ja|Ja|
|**Senden von Intranetdatenverkehr an Internet Explorer zulassen**|Ja|Nein|
|**Do Not Track (nicht verfolgen) zulassen**|Ja|Ja|
|**SmartScreen aktivieren**|Ja|Ja|
|**Active Scripting zulassen**|Ja|Ja|
|**Popups zulassen**|Ja|Nein|
|**Cookies zulassen**|Ja|Ja|
|**AutoAusfüllen zulassen**|Ja|Nein|
|**Kennwort-Manager zulassen**|Ja|Ja|
|**Ort der Standortliste für Enterprise-Modus**<br /><br />Gibt an, wo Sie die Liste der Websites finden, die im Unternehmensmodus geöffnet werden. Benutzer können diese Liste nicht bearbeiten.|Ja|Nein|

### Apps

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**App Store zulassen**|Nein|Ja|

## Gerätefunktionseinstellungen

### Mobilfunk

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**Datenroaming zulassen**|Ja|Ja|
|**VPN über Mobilfunk zulassen**|Ja|Ja|
|**VPN-Roaming über Mobilfunk zulassen**|Ja|Ja|

### Hardware

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**Kamera zulassen**|Ja|Ja|
|**Wechselspeichermedien zulassen**|Ja|Ja|
|**WLAN zulassen**|Nein|Ja|
|**Internetfreigabe zulassen**|Ja|Ja|
|**Manuelle WLAN-Konfiguration zulassen**|Nein|Ja|
|**Automatische Verbindung mit unverschlüsselten WLAN-Hotspots zulassen**|Ja|Ja|
|**Geolocation zulassen**<br /><br />Gibt an, ob das Gerät Ortungsdienstinformationen verwenden kann.|Ja|Ja|
|**NFC zulassen**|Ja|Ja|
|**Bluetooth zulassen**|Ja|Ja|
|**Sichtbaren Modus für Bluetooth zulassen**|Ja|Ja|
|**Bluetooth-Werbung zulassen**<br /><br />Ermöglicht Geräten dem Empfang von Werbung über Bluetooth.|Ja|Ja|
|**Verbindungsfähigen Modus für Bluetooth zulassen** **Important:** Diese Einstellung wird von Windows 10 nicht mehr unterstützt und künftig entfernt.|Ja|Ja|
|**Handyzurücksetzung zulassen**|Ja|Ja|
|**USB-Verbindung zulassen**|Ja|Ja|
|**Diebstahlschutzmodus zulassen**<br /><br />Konfigurieren Sie, ob der Windows-Diebstahlschutzmodus aktiviert ist.|Ja|Ja|

### Features

|Name der Einstellung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------------|---------------------|
|**Kopieren und Einfügen zulassen**|Nein|Ja|
|**Sprachaufzeichnung zulassen**|Nein|Ja|
|**Cortana zulassen**|Ja|Ja|
|**Info-Center-Benachrichtigungen zulassen**|Nein|Ja|

## Updateeinstellungen

|Name der Einstellung|Beschreibung|Windows 10 Desktop|Windows 10 Mobile|
|------------------------|----------------|----------------------|---------------------|
|**Automatische Updates zulassen**|Aktivieren Sie diese Einstellung, um automatische Updates zuzulassen. Konfigurieren Sie dann eine der folgenden Einstellungen, um das Updateverhalten zu steuern:<br /><br /><ul><li>**Download benachrichtigen**</li><li>**Automatische Installation während der Wartung**</li><li>**Automatische Installation und Neustart während der Wartung**</li><li>**Automatische Installation und Neustart zur geplanten Zeit**<br /><br />    Wenn diese Option aktiviert ist, können Sie auch die folgenden Einstellungen konfigurieren:<br /><br /><ul><li>**Benachrichtigung für Endbenutzer unterdrücken**</li><li>**Installationstag für geplante Updates definieren**</li></ul></li></ul>|Ja|Nein|

## Bereitstellen der Konfigurationsrichtlinie

1.  Stellen Sie die Konfigurationsrichtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen im Arbeitsbereich **Richtlinie** identifizieren Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

