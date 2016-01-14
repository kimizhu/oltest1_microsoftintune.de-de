---
description: na
keywords: na
title: Windows Team configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38194ef3-e26e-4682-958d-14b395fccba1
---
# Einstellungen f&#252;r Windows Team-Konfigurationsrichtlinie in Microsoft Intune
Verwenden Sie die [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **allgemeine Windows 10 Team-Konfigurationsrichtlinie**, um Einstellungen für registrierte Windows 10 Team-Geräte (z. B. Microsoft Surface Hub) zu konfigurieren.

## Erstellen einer Windows 10 Team-Konfigurationsrichtlinie

#### So geben Sie grundlegende Einstellungen für die Konfigurationsrichtlinie an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Klicken Sie auf **Windows** &gt; **Allgemeine Konfiguration (Windows 10 Team und höher)**, und klicken Sie dann auf **Richtlinie erstellen**.

    > [!NOTE]
    > Sie können keine Konfigurationsrichtlinie mit empfohlenen Einstellungen erstellen. Sie müssen eine benutzerdefinierte Richtlinie erstellen.

3.  Geben Sie im Abschnitt **Allgemein** der Seite **Richtlinie erstellen** einen Namen und eine Beschreibung für die neue Richtlinie ein.

4.  Verwenden Sie die Informationen im folgenden Abschnitt, um die Einstellungen für die Richtlinie festzulegen.

5.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## <a name="BKMK_Settings"></a>Liste der Einstellungen für diese Richtlinie

### <a name="BKMK_sec"></a>Geräteeinstellungen

|Name der Einstellung|Details|
|------------------------|-----------|
|**Wenn sich jemand im Raum automatisch zu reaktivieren Bildschirms zulassen**|Ermöglicht das automatische Aktivieren des Geräts, wenn der Sensor eine Person im Raum erkennt.|
|**PIN für funkprojektion anfordern**|Gibt an, ob Sie eine PIN eingeben müssen, bevor Sie die drahtlosen Projektionsfunktionen des Geräts verwenden können.|
|**Wartungsfenster festlegen**|Konfiguriert das Fenster, in dem Updates am Gerät vorgenommen werden können. Sie können die Startzeit und Länge des Fensters (1 bis 5 Stunden) konfigurieren.|

## Bereitstellen der Konfigurationsrichtlinie

1.  Stellen Sie die Konfigurationsrichtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen im Arbeitsbereich **Richtlinie** identifizieren Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

