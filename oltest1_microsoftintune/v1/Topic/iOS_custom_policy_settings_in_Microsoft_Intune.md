---
description: na
keywords: na
title: iOS custom policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 04e60d5a-3da6-4943-b6ff-e6a331bcbcfa
---
# Benutzerdefinierte iOS-Richtlinieneinstellungen in Microsoft Intune
Verwenden Sie die [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **benutzerdefinierte iOS-Konfigurationsrichtlinie** zum Bereitstellen von Einstellungen, die Sie mit dem [Apple Configurator-Tool](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) für iOS-Geräte erstellt haben. Mit diesem Tool können Sie zahlreiche Einstellungen zur Betriebssteuerung dieser Geräte erstellen und in ein Konfigurationsprofil exportieren. Sie können dieses Konfigurationsprofil anschließend in eine benutzerdefinierte [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] iOS-Richtlinie importieren und die Einstellungen für Benutzer und Geräte in Ihrer Organisation bereitstellen.

Diese Funktion soll es Ihnen ermöglichen, iOS-Einstellungen bereitzustellen, die nicht mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinien konfigurierbar sind. Informationen zu den Einstellungen, die Sie mit diesen Richtlinien konfigurieren können, finden Sie im Abschnitt [Einstellungen für iOS-Konfigurationsrichtlinien in Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md).

## Vorbereitungsmaßnahmen
Bevor Sie beginnen, müssen Sie Apple Configurator installiert und eine Konfigurationsdatei mit den Einstellungen erstellt haben, die Sie für Benutzer oder Geräte bereitstellen möchten. Um Apple Configurator herunterzuladen und mehr darüber zu erfahren, besuchen Sie den [Mac App Store](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12)

> [!NOTE]
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] gibt keine Auskunft über die Kompatibilität der einzelnen Einstellungen einer benutzerdefinierten iOS-Richtlinie. Die Gesamtkompatibilität der Richtlinie wird jedoch angegeben.

## Erstellen einer benutzerdefinierten iOS-Richtlinie

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie eine Richtlinie vom Typ **iOS** &gt; **Benutzerdefinierte Konfiguration**.

    Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

    Sie können nur benutzerdefinierte iOS-Richtlinien erstellen und bereitstellen. Empfohlene Einstellungen sind nicht verfügbar.

3.  Orientieren Sie sich bei der Konfiguration der Richtlinieneinstellungen an der folgenden Tabelle:

    |Name der Einstellung|Weitere Informationen|
    |------------------------|-------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für die benutzerdefinierte iOS-Richtlinie ein, damit Sie sie leichter in der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole identifizieren können.|
    |**Beschreibung**|Geben Sie eine Beschreibung ein, die einen Überblick über die benutzerdefinierte iOS-Richtlinie bietet, sowie weitere relevante Informationen, mit denen Sie danach suchen können.|
    |**Name des benutzerdefinierten Konfigurationsprofils (zur Anzeige beim Benutzer)**|Geben Sie einen Namen für die Richtlinie an, der auf dem Gerät und in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinienberichten angezeigt wird.|
    |**Profil-Konfigurationsdatei**|Klicken Sie auf **Importieren**, und suchen Sie dann das mit Apple Configurator erstellte Konfigurationsprofil. **Note:** Stellen Sie sicher, dass die Einstellungen, die Sie aus dem Apple Configurator-Tool exportieren, mit der iOS-Version auf den Geräten kompatibel sind, für die Sie die benutzerdefinierte iOS-Richtlinie bereitstellen. Um Informationen zum Korrigieren inkompatibler Einstellungen zu erhalten, suchen Sie nach der **Konfigurationsprofilreferenz** und der **Verwaltungsprotokollreferenz für mobile Geräte** auf der Website von [Apple Developer](https://developer.apple.com/).|
    |**Details zum Konfigurationsprofil**|Zeigt den XML-Code des importierten Konfigurationsprofils an.|

4.  Klicken Sie danach auf **Richtlinie speichern**.

5.  Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## Bereitstellen einer benutzerdefinierten iOS-Richtlinie

-   Stellen Sie die benutzerdefinierte iOS-Richtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Hilfestellung bei der Bereitstellung von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen auf der Seite **Übersicht** des Arbeitsbereichs **Richtlinie** identifiziert Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

