---
description: na
keywords: na
title: Mac OS X custom policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70459e56-17d8-4d3f-803d-22feefa7a5b6
---
# Benutzerdefinierte Mac&#160;OS&#160;X-Richtlinieneinstellungen in Microsoft Intune
Verwenden Sie die [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **benutzerdefinierte Mac OS X-Konfigurationsrichtlinie** zum Bereitstellen von Einstellungen, die Sie mit dem [Apple Configurator-Tool](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) für Mac OS X-Geräte erstellt haben. Mit diesem Tool können Sie zahlreiche Einstellungen zur Betriebssteuerung dieser Geräte erstellen und in ein Konfigurationsprofil exportieren. Sie können dieses Konfigurationsprofil anschließend in eine benutzerdefinierte [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Mac OS X-Richtlinie importieren und die Einstellungen für Benutzer und Geräte in Ihrer Organisation bereitstellen.

Diese Funktion soll es Ihnen ermöglichen, Mac OS X-Einstellungen bereitzustellen, die nicht mit einer allgemeinen [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Mac OS X-Konfigurationsrichtlinie konfigurierbar sind. Informationen zu den Einstellungen, die Sie mit diesen Richtlinien konfigurieren können, finden Sie unter [Einstellungen für Mac OS X-Konfigurationsrichtlinien in Microsoft Intune](../Topic/Mac_OS_X_configuration_policy_settings_in_Microsoft_Intune.md).

## Voraussetzungen
Bevor Sie beginnen, müssen Sie Apple Configurator installiert und eine Konfigurationsdatei mit den Einstellungen erstellt haben, die Sie für Benutzer oder Geräte bereitstellen möchten. Um Apple Configurator herunterzuladen und mehr darüber zu erfahren, besuchen Sie den [Mac App Store](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12)

> [!NOTE]
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] gibt keine Auskunft über die Kompatibilität der einzelnen Einstellungen einer benutzerdefinierten Mac OS X-Richtlinie. Die Gesamtkompatibilität der Richtlinie wird jedoch angegeben.

## Erstellen einer benutzerdefinierten Mac OS X-Richtlinie

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie eine Richtlinie vom Typ **Mac OS X** &gt; **Benutzerdefinierte Konfiguration**.

    Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

    Sie können lediglich benutzerdefinierte Mac OS X-Richtlinien erstellen und bereitstellen. Empfohlene Einstellungen sind nicht verfügbar.

3.  Orientieren Sie sich bei der Konfiguration der Richtlinieneinstellungen an der folgenden Tabelle:

    |Name der Einstellung|Weitere Informationen|
    |------------------------|-------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für die benutzerdefinierte Mac OS X-Richtlinie ein, damit Sie sie leichter in der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole identifizieren können.|
    |**Beschreibung**|Geben Sie eine Beschreibung ein, die einen Überblick über die benutzerdefinierte Mac OS X-Richtlinie bietet, sowie weitere relevante Informationen, mit denen Sie danach suchen können.|
    |**Name des benutzerdefinierten Konfigurationsprofils (zur Anzeige beim Benutzer)**|Geben Sie einen Namen für die Richtlinie an, der auf dem Gerät und in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinienberichten angezeigt wird.|
    |**Profil-Konfigurationsdatei**|Klicken Sie auf **Importieren**, und suchen Sie dann das mit Apple Configurator erstellte Konfigurationsprofil. **Tip:** Im Abschnitt [Erstellen einer Konfigurationsprofildatei](#BKMK_Prof) dieses Themas finden Sie weitere Informationen zum Erstellen des Konfigurationsprofils.|
    |**Details zum Konfigurationsprofil**|Zeigt den XML-Code des importierten Konfigurationsprofils an.|

4.  Klicken Sie danach auf **Richtlinie speichern**.

5.  Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## <a name="BKMK_Prof"></a>Erstellen einer Konfigurationsprofildatei
Die Konfigurationsprofildatei, die von der benutzerdefinierten Richtlinie verwendet wird, kann über zwei Methoden erstellt werden.

-   Exportieren Sie die Datei (mit der Erweiterung **.mobileconfig**) aus dem Apple Configurator-Tool.

-   Erstellen Sie die Datei selbst unter Verwendung des entsprechenden Schemas aus der [Apple Configuration Profile Key Reference](https://developer.apple.com/library/ios/featuredarticles/iPhoneConfigurationProfileRef/Introduction/Introduction.html).

## Bereitstellen einer benutzerdefinierte Mac OS X-Richtlinie

-   Stellen Sie die benutzerdefinierte Mac OS X-Richtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Hilfestellung bei der Bereitstellung von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen auf der Seite **Übersicht** des Arbeitsbereichs **Richtlinie** identifiziert Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

> [!IMPORTANT]
> Wenn sich ein Mac OS X-Gerät im Energiesparmodus befindet, können keine Richtlinien oder Profile bereitgestellt oder inventarisiert werden. Infolgedessen zeigt die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole möglicherweise vorübergehend den Status **Richtlinieneinstellungen mit Fehlern** an, bis das Gerät erneut aktiviert und der Energiesparmodus beendet wird.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

