---
description: na
keywords: na
title: Exchange ActiveSync policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9cbb826-b155-4df6-abf3-60c6f05b2783
---
# Einstellungen f&#252;r Exchange ActiveSync-Richtlinien in Microsoft Intune
Konfigurieren Sie mit der [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Exchange ActiveSync-Richtlinie Einstellungen, mit denen Sie eine Reihe von Features und Funktionen auf Geräten steuern können, die von Exchange ActiveSync verwaltet werden.

## Erstellen einer Exchange ActiveSync-Richtlinie

#### So geben Sie grundlegende Einstellungen für die Richtlinie an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Klicken Sie auf **Allgemeine Einstellungen für mobile Geräte** &gt; **Exchange ActiveSync** &gt; **Richtlinie erstellen**.

    > [!NOTE]
    > Sie können keine Konfigurationsrichtlinie mit empfohlenen Einstellungen erstellen. Sie müssen eine benutzerdefinierte Richtlinie erstellen.

3.  Geben Sie im Abschnitt **Allgemein** der Seite **Richtlinie erstellen** einen Namen und eine Beschreibung für die neue Richtlinie ein.

4.  Befolgen Sie die Informationen in den folgenden Abschnitten zum Angeben von Einstellungen für die Richtlinie.

5.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## <a name="BKMK_Settings"></a>Richtlinieneinstellungen für Geräte, die von Exchange ActiveSync verwaltet werden

### <a name="BKMK_sec"></a>Sicherheitseinstellungen

|Name der Einstellung|
|------------------------|
|**Anfordern eines Kennworts zum Entsperren mobiler Geräte**|
|**Erforderlicher Kennworttyp**<br /><br />(gibt den erforderlichen Typ des Kennworts an, z. B. nur numerisch oder alphanumerisch)|
|**Minimale Kennwortlänge**|
|**Einfache Kennwörter zulassen**<br /><br />Einfache Kennwörter enthalten '0000' und '1234'.|
|**Anzahl zulässiger wiederholter Anmeldefehler, bevor das Gerät zurückgesetzt wird**|
|**Kennwortablauf (Tage)**|
|**Kennwortverlauf speichern**|
|**Kennwortverlauf speichern** – **Wiederverwendung vorheriger Kennwörter verhindern**|
|**Minuten der Inaktivität, bevor ein Kennwort erforderlich ist**|

### Verschlüsselungseinstellungen

|Name der Einstellung|
|------------------------|
|**Verschlüsselung auf mobilem Gerät anfordern**<sup>1</sup><br /><br />Für Windows Phone 8-Geräte müssen Sie hier **Ja** festlegen.<br /><br />Aktivieren Sie zum Verwenden der Verschlüsselung auf iOS-Geräten die Einstellung **Kennwort zum Entsperren mobiler Geräte erforderlich**.|
|**Verschlüsselung auf Speicherkarten vorschreiben**|
<sup>1</sup> Zusätzliche Informationen für Geräte die Windows 8.1 ausführen

-   Um die Verschlüsselung auf Geräten zu erzwingen, die Windows 8.1 ausführen, installieren Sie das [MDM-Clientupdate für Windows von Dezember 2014](http://support.microsoft.com/kb/3013816) auf jedem Gerät.

-   Wenn Sie diese Einstellung für Windows 8.1-Geräte aktivieren, müssen alle Benutzer des Geräts ein Microsoft-Konto haben.

-   Damit die Verschlüsselung funktioniert, muss das Gerät die Hardwarezertifizierungsanforderungen für Microsoft [InstantGo](http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/) erfüllen.

-   Wenn Sie die Verschlüsselung auf einem Gerät erzwingen, ist der Wiederherstellungsschlüssel nur über das Microsoft-Konto des Benutzers zugänglich, auf das dieser über sein eigenes OneDrive-Konto zugreift. Sie können diesen Schlüssel nicht im Auftrag eines Benutzers wiederherstellen.

### <a name="BKMK_email"></a>E-Mail-Einstellungen

|Name der Einstellung|
|------------------------|
|**Herunterladen von E-Mail-Anhängen für Benutzer zulassen**|
|**Synchronisierungszeitraum für E-Mail**|
|**Synchronisierung mit Exchange ActiveSync für mobile Geräte zulassen, die diese Einstellungen nicht vollständig unterstützen**|

### <a name="BKMK_browser"></a>Anwendungen – Browser

|Name der Einstellung|
|------------------------|
|**Webbrowser zulassen**|

### <a name="BKMK_hard"></a>Gerätefunktionen – Hardware

|Name der Einstellung|
|------------------------|
|**Kamera zulassen**|

## Bereitstellen der Konfigurationsrichtlinie

1.  Stellen Sie die Konfigurationsrichtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen im Arbeitsbereich **Richtlinie** identifizieren Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

