---
description: na
keywords: na
title: Configure apps with mobile app configuration policies in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc6b645a-e837-4b2a-a10f-144065cbd8dd
---
# Konfigurieren von Apps mit Konfigurationsrichtlinien f&#252;r mobile Apps in Microsoft Intune
Verwenden Sie Konfigurationsrichtlinien für mobile Apps in [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], um Einstellungen anzugeben, die beim Ausführen einer App durch den Benutzer erforderlich sind. Beispielsweise kann eine App vom Benutzer Folgendes anfordern:

-   Eine benutzerdefinierte Portnummer für die Ausführung

-   Spracheinstellungen

-   Sicherheitseinstellungen

-   Brandingeinstellungen wie z. B. ein Unternehmenslogo

Wenn diese Einstellungen vom Benutzer nicht ordnungsgemäß eingegeben werden, kann dies zur erhöhten Belastung Ihres Helpdesks führen und auch die Annahme der neuen Apps verlangsamen..

Mit Konfigurationsrichtlinien für mobile Apps können Sie diese Probleme beseitigen, da Sie diese Einstellungen für Benutzer in einer Richtlinie bereitstellen können, bevor die Benutzer die App ausführen. Die Einstellungen werden dann automatisch bereitgestellt, und der Benutzer muss keine weitere Aktion durchführen.

Sie stellen diese Richtlinien nicht direkt für Benutzer und Geräte bereit. Stattdessen verknüpfen Sie die Richtlinie mit einer App und stellen dann die App bereit. Die Richtlinieneinstellungen werden immer dann verwendet, wenn die Anwendung danach sucht (in der Regel beim ersten Ausführen).

> [!TIP]
> Dieser Richtlinientyp ist zurzeit nur für Geräte unter iOS 7.1 und höher verfügbar und unterstützt die folgenden App-Installationstypen:
> 
> -   **Verwaltete iOS-App aus dem App Store**
> -   **App-Paket für iOS**
> 
> Weitere Informationen zu den App-Installationstypen finden Sie unter [Erste Schritte mit der Bereitstellung von Apps in Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md).

## Konfigurieren einer Konfigurationsrichtlinie für mobile Apps

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Erweitern Sie in der Liste der Richtlinien den Eintrag **iOS**, klicken Sie auf **Mobile App-Konfiguration**, und klicken Sie dann auf **Richtlinie erstellen**.

    > [!TIP]
    > Sie können für diesen Richtlinientyp nur benutzerdefinierte Einstellungen konfigurieren. Empfohlene Einstellungen sind nicht verfügbar.

3.  Im Abschnitt **Allgemein** der Seite **Richtlinie erstellen** geben Sie einen Namen und eine optionale Beschreibung für die Konfigurationsrichtlinie für mobile Apps an.

4.  Geben oder fügen Sie im Abschnitt **Konfigurationsrichtlinie für mobile Apps** der Seite eine XML-Eigenschaftenliste mit den App-Konfigurationseinstellungen ein, die im Feld verwendet werden sollen.

    > [!TIP]
    > Weitere Informationen zu XML-Eigenschaftenlisten finden Sie unter [Understanding XML Property Lists](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/PropertyLists/UnderstandXMLPlist/UnderstandXMLPlist.html)in der iOS Developer Library.
    > 
    > Das Format der XML-Eigenschaftenliste variiert je nach der App, die Sie konfigurieren. Wenden Sie sich an den Hersteller der App, um ausführliche Informationen über das genau zu verwendende Format zu erhalten.
    > 
    > [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] unterstützt die folgenden Datentypen in einer Eigenschaftenliste:
    > 
    > -   &lt;integer&gt;
    > -   &lt;real&gt;
    > -   &lt;string&gt;
    > -   &lt;array&gt;
    > -   &lt;dict&gt;
    > -   &lt;true /&gt; oder &lt;false /&gt;
    > 
    > Weitere Informationen zu Datentypen finden Sie unter [About Property Lists](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/PropertyLists/AboutPropertyLists/AboutPropertyLists.html) in der iOS Developer Library.

5.  Klicken Sie auf **Überprüfen** um sicherzustellen, dass der eingegebene XML-Code einem gültigen Format für Eigenschaftenlisten entspricht.

    > [!IMPORTANT]
    > Beim Klicken auf **Überprüfen** prüft [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], ob der von Ihnen eingegebenen XML-Code in einem gültigen Format vorliegt. Es wird nicht überprüft, ob die XML-Eigenschaftenliste mit der App verwendet werden kann, der sie zugeordnet ist.

6.  Klicken Sie abschließend auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** angezeigt.

## Zuordnen einer Konfigurationsrichtlinie für mobile Apps zu einer App
Nachdem Sie eine Konfigurationsrichtlinie für mobile Apps erstellt haben, müssen Sie sie der iOS-App zuordnen, für die die Einstellungen in der Konfigurationsrichtlinie gelten sollen.

Befolgen Sie zu diesem Zweck die Schritte zum Erstellen einer App-Bereitstellung in [Bereitstellen von Apps für mobile Geräte in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md). Wenn Sie die Seite **Mobile App-Konfiguration** des Assistenten erreichen, wählen Sie in der Dropdownliste **App-Konfigurationsrichtlinie** die Richtlinie aus, die Sie der App zuordnen möchten.

Fahren Sie mit dem Bereitstellen und Überwachen der App-Bereitstellung wie gewohnt fort.

Wenn die bereitgestellte App auf einem Gerät gestartet wird, wird sie mit den Einstellungen ausgeführt, die Sie in der Konfigurationsrichtlinie für mobile Apps konfiguriert haben.

> [!TIP]
> Wenn mindestens eine Konfigurationsrichtlinie für mobile Apps einen Konflikt verursacht, wird keine Richtlinie durchgesetzt, und der Konflikt wird im **Dashboard** der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungskonsole gemeldet .

## Siehe auch
[Bereitstellen und Konfigurieren von Apps mit Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)
[Bereitstellen von Apps für mobile Geräte in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)

