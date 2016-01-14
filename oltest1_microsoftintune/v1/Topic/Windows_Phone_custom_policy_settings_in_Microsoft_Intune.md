---
description: na
keywords: na
title: Windows Phone custom policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f64674ff-f2a6-471c-82a5-bcff23c7514d
---
# Benutzerdefinierte Windows Phone-Richtlinieneinstellungen in Microsoft Intune
Stellen Sie mithilfe der **benutzerdefinierten Windows Phone-Richtlinie** von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Einstellungen für OMA-URI (Open Mobile Alliance Uniform Resource Identifier) bereit, um Features auf **Windows Phone 8.1-Geräten** zu steuern. Dies sind die Standardeinstellungen, die viele Hersteller von mobilen Geräten verwenden, um Gerätefunktionen zu steuern.

Diese Funktion soll es Ihnen ermöglichen, Windows Phone-Einstellungen bereitzustellen, die nicht mit einer [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinie konfigurierbar sind. Informationen zu den Einstellungen, die Sie mit diesen Richtlinien konfigurieren können, finden Sie im Abschnitt [Verwalten von Einstellungen und Features auf Ihren Geräten mit Microsoft Intune-Richtlinien](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md).

Informationen zum Erstellen von OMA-URI-Einstellungen für Windows Phone-Geräte finden Sie in der [MDM-Protokolldokumentation für Windows Phone 8.1](http://technet.microsoft.com/library/dn499787.aspx).

## Erstellen einer benutzerdefinierten Windows Phone-Richtlinie

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Richtlinie hinzufügen**.

2.  Klicken Sie unter **Windows** auf eine Richtlinie vom Typ **Benutzerdefinierte Konfiguration (Windows Phone 8.1 und höher)**.

    Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

    Sie können nur benutzerdefinierte Richtlinien erstellen und bereitstellen. Empfohlene Einstellungen sind nicht verfügbar.

3.  Orientieren Sie sich bei der Konfiguration der allgemeinen Richtlinieneinstellungen an der folgenden Tabelle:

    |Name der Einstellung|Weitere Informationen|
    |------------------------|-------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für die Richtlinie ein, damit Sie sie leichter in der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole identifizieren können.|
    |**Beschreibung**|Geben Sie eine Beschreibung ein, die einen Überblick über die Richtlinie bietet, und andere relevante Informationen, die Ihnen die Suche danach erleichtern.|

4.  Klicken Sie im Abschnitt **OMA-URI-Einstellungen** auf **Hinzufügen**, um eine Einstellung hinzuzufügen. Sie können auch eine vorhandene Einstellung bearbeiten oder löschen.

5.  Geben Sie im Dialogfeld **OMA-URI hinzufügen oder bearbeiten** die folgenden Informationen an:

    |Element|Weitere Informationen|
    |-----------|-------------------------|
    |**Name der Einstellung**|Geben Sie einen eindeutigen Namen für die OMA-URI-Einstellung ein, damit Sie sie in der Liste der Einstellungen leichter identifizieren können.|
    |**Beschreibung der Einstellung**|Geben Sie eine Beschreibung ein, die einen Überblick über die Einstellung bietet, und andere relevante Informationen, die Ihnen die Suche danach erleichtern.|
    |**Datentyp**|Wählen Sie den Datumstyp aus, in dem Sie diese OMA-URI-Einstellung angeben. Wählen Sie aus:<br /><br />-   **Zeichenfolge**<br />-   **Zeichenfolge (XML)**<br />-   **Datum und Uhrzeit**<br />-   **Ganze Zahl**<br />-   **Gleitkomma**<br />-   **Boolesch**|
    |**OMA-URI (Groß-/Kleinschreibung beachten)**|Geben Sie den OMA-URI an, für den Sie eine Einstellung festlegen möchten.|
    |**Wert**|Geben Sie den mit der zuvor festgelegten OMA-URI-Einstellung zu verknüpfenden Wert an.|

6.  Klicken Sie auf **OK**, um die Einstellung zu speichern und zur Seite **Richtlinie erstellen** zurückzukehren.

7.  Fügen Sie weitere benötige Einstellungen hinzu. Klicken Sie abschließend auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## Bereitstellen einer benutzerdefinierten Windows Phone-Richtlinie

1.  Stellen Sie die Richtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen auf der Seite **Übersicht** des Arbeitsbereichs **Richtlinie** identifiziert Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

