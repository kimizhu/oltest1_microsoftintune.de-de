---
description: na
keywords: na
title: Manage Internet access using managed browser policies with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc946303-e09b-4d73-8bf4-87742299bc54
---
# Verwalten des Internetzugriffs mittels Richtlinien f&#252;r verwaltete Browser mit Microsoft Intune
Der verwaltete Browser ist eine Webbrowser-Anwendung, die Sie in Ihrer Organisation mit [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] bereitstellen können. Eine Richtlinie für verwaltete Browser konfiguriert die Liste "Zulassen" oder "Blockieren", um die Websites einzuschränken, die Benutzer des verwalteten Browsers besuchen können.

Da diese App eine verwaltete App ist, können Sie darauf auch Verwaltungsrichtlinien für mobile Anwendungen anwenden. Hierzu zählt beispielsweise, die Verwendung der Funktionen zum Ausschneiden, Kopieren und Einfügen zu steuern, Bildschirmaufnahmen zu verhindern und sicherzustellen, dass Links zu Inhalten, auf die Benutzer klicken, in anderen verwalteten Apps geöffnet werden. Details finden Sie unter [Schützen von Daten mithilfe der Verwaltungsrichtlinien für mobile Anwendungen mit Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md).

> [!IMPORTANT]
> Wenn Benutzer den verwalteten Browser selbst installieren, wird er durch keine von Ihnen angegebenen Richtlinien verwaltet. Um sicherzustellen, dass der Browser von Intune verwaltet wird, muss die App deinstalliert werden, bevor Sie sie als verwaltete Anwendung bereitstellen können.

Sie können Richtlinien für verwaltete Browser für die folgenden Gerätetypen erstellen:

-   Geräte unter Android 4 und höher

-   Geräte unter iOS 7 und höher

## Erstellen einer Richtlinie für verwaltete Browser

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie einen der folgenden Richtlinientypen für **Software**:

    -   **Richtlinie für Managed Browser (Android 4 und höher)**

    -   **Richtlinie für Managed Browser (iOS 7 und höher)**

    Weitere Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie im Thema [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Orientieren Sie sich bei der Konfiguration der Richtlinieneinstellungen für verwaltete Browser an der folgenden Tabelle:

    |Name der Einstellung|Weitere Informationen|
    |------------------------|-------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für die Richtlinie für verwaltete Browser ein, damit Sie sie leichter in der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole identifizieren können.|
    |**Beschreibung**|Geben Sie eine Beschreibung ein, die einen Überblick über die Richtlinie für verwaltete Browser bietet, sowie weitere relevante Informationen, mit denen Sie danach suchen können.|
    |**Aktivieren Sie eine Zulassungsliste oder Sperrliste, um die URLs zu beschränken, die vom verwalteten Browser geöffnet werden können.**|Wählen Sie eine der folgenden Optionen aus:<br /><br />-   **Der verwaltete Browser kann nur die unten aufgeführten URLs öffnen** – Geben Sie eine Liste mit URLs an, die der verwaltete Browser öffnen kann.<br />-   **Der verwaltete Browser kann die unten aufgeführten URLs nicht öffnen** – Geben Sie eine Liste mit URLs an, die der verwaltete Browser nicht öffnen kann. **Note:** Eine Richtlinie für verwaltete Browser kann nicht sowohl zulässige als auch blockierte URLs enthalten.<br />Weitere Informationen zu den festlegbaren URL-Formaten finden Sie in diesem Thema unter [URL-Format für zulässige und blockierte URLs](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md#BKMK_URLs).|

4.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## Erstellen einer Softwarebereitstellung für die Managed Browser-App
Nachdem Sie die Richtlinie für verwaltete Browser erstellt haben, können Sie eine Softwarebereitstellung für die Managed Browser-App erstellen und der von Ihnen erstellten Richtlinie für verwaltete Browser zugeordnet.

> [!IMPORTANT]
> Richtlinien für verwaltete Browser werden nicht auf die gleiche Weise wie andere [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinien bereitgestellt. Diese Art von Richtlinie muss dem Softwarepaket für verwaltete Browser zugeordnet werden.

Wenn Sie die App bereitstellen, wählen Sie die Richtlinie für verwaltete Browser auf der Seite **Mobile App-Verwaltung** aus, um die App mit der Richtlinie zu verknüpfen.

Weitere Informationen über das Bereitstellen von Apps finden Sie unter [Bereitstellen von Apps für mobile Geräte in Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md).

## Sicherheit und Datenschutz für den verwalteten Browser

-   Auf iOS-Geräten können von Benutzern besuchte Websites, deren Zertifikat abgelaufen oder nicht vertrauenswürdig ist, nicht geöffnet werden.

-   Einstellungen, die Benutzer für den integrierten Browser auf ihren Geräten vornehmen, werden nicht vom verwalteten Browser verwendet. Dies liegt daran, da der verwaltete Browser keinen Zugriff auf diese Einstellungen hat.

-   Wenn Sie die Option **Einfache PIN für Zugriff anfordern** oder **Unternehmensanmeldeinformationen für Zugriff anfordern** in einer Richtlinie für die Verwaltung mobiler Anwendung konfigurieren, die mit dem verwalteten Browser verknüpft ist, und ein Benutzer auf der Authentifizierungsseite auf den Hilfe-Link klickt, kann er beliebige Websites auch dann durchsuchen, wenn diese in der Richtlinie für verwaltete Browser einer Sperrliste hinzugefügt wurden.

-   Der verwaltete Browser kann nur den Zugriff auf Websites blockieren, wenn darauf direkt zugegriffen wird. Der Zugriff auf die Website kann nicht blockiert werden, wenn dafür Zwischendienste (z. B. ein Übersetzungsdienst) verwendet werden.

-   Um die Authentifizierung zuzulassen, ist **&#42;.microsoft.com** von den Zulassungs- und Sperrlisten ausgenommen – diese Adresse ist immer zugelassen.

## Referenzinformationen

### <a name="BKMK_URLs"></a>URL-Format für zulässige und blockierte URLs
Nachfolgend wird erläutert, welche Formate und Platzhalter Sie zum Festlegen von URLs in den Zulassungs- und Sperrlisten verwenden können.

-   Sie können das Platzhaltersymbol '**&#42;**" gemäß den Regeln in der nachfolgenden Liste mit zugelassenen Mustern verwenden.

-   Stellen Sie sicher, dass Sie bei der Eingabe in die Liste allen URLs **http** oder **https** voranstellen.

-   Sie können Portnummern in der Adresse angeben. Wenn Sie keine Portnummer angeben, werden folgende Werte verwendet:

    -   Port 80 für http

    -   Port 443 für https

    Das Verwenden von Platzhaltern für die Portnummer wird nicht unterstützt: Beispiele: **http://www.contoso.com :&#42;** und **http://www.contoso.com: / &#42;**

-   In der folgenden Tabelle sind die zugelassenen Muster aufgeführt, die Sie zum Festlegen von URLs verwenden können:

    |URL|Beschreibung|Treffer|Stimmt nicht überein mit|
    |-------|----------------|-----------|----------------------------|
    |http://www.contoso.com|Entspricht einer einzelnen Seite|www.contoso.com|host.contoso.com<br /><br />www.contoso.com/images<br /><br />contoso.com/|
    |http://contoso.com|Entspricht einer einzelnen Seite|contoso.com/|host.contoso.com<br /><br />www.contoso.com/images<br /><br />www.contoso.com|
    |http://www.contoso.com/&#42;|Entspricht allen URLs, die mit www.contoso.com beginnen|www.contoso.com<br /><br />www.contoso.com/images<br /><br />www.contoso.com/videos/tvshows|host.contoso.com<br /><br />host.contoso.com/images|
    |http://&#42;.contoso.com/&#42;|Entspricht allen Unterdomänen unter "contoso.com"|developer.contoso.com/resources<br /><br />news.contoso.com/images<br /><br />news.contoso.com/videos|contoso.host.com|
    |http://www.contoso.com/images|Entspricht einem einzelnen Ordner|www.contoso.com/images|www.contoso.com/images/dogs|
    |http://www.contoso.com:80|Entspricht einer einzelnen Seite mit einer Portnummer|http://www.contoso.com:80||
    |https://www.contoso.com|Entspricht einer einzelnen, sicheren Seite|https://www.contoso.com|http://www.contoso.com|
    |http://www.contoso.com/images/&#42;|Entspricht einem einzelnen Ordner und allen Unterordnern|www.contoso.com/images/dogs<br /><br />www.contoso.com/images/cats|www.contoso.com/videos|

-   Es folgen Beispiele für einige der Eingaben, die Sie nicht festlegen können:

    -   &#42;.com

    -   &#42;.contoso/&#42;

    -   www.contoso.com/&#42;images

    -   www.contoso.com/&#42;images&#42;pigs

    -   www.contoso.com/page&#42;

    -   IP-Adressen

    -   https://&#42;

    -   http://&#42;

    -   http://www.contoso.com:&#42;

    -   http://www.contoso.com: /&#42;

### Lösen von Konflikten zwischen der Zulassungs- und Sperrliste
Wenn mehrere Richtlinien für verwaltete Browser für ein Gerät bereitgestellt werden und Einstellungen in Konflikt stehen, werden sowohl der Modus (zulassen oder blockieren) als auch die URL-Listen ausgewertet. Bei einem Konflikt gilt folgendes Verhalten:

-   Wenn die Modi in jeder Richtlinie identisch sind, aber die URL-Listen voneinander abweichen, werden die URLs auf dem Gerät nicht erzwungen.

-   Wenn die Modi in jeder Richtlinie voneinander abweichen, aber die URL-Listen identisch sind , werden die URLs auf dem Gerät nicht erzwungen.

-   Wenn ein Gerät erstmals Richtlinien für verwaltete Browser empfängt und zwei Richtlinien in Konflikt stehen, werden die URLs auf dem Gerät nicht erzwungen. Sie können die Konflikte über den Knoten **Richtlinienkonflikte** des Arbeitsbereichs **Richtlinie** anzeigen.

-   Wenn ein Gerät bereits ein Richtlinie für verwaltete Browser erhalten hat und eine zweite Richtlinie mit in Konflikt stehenden Einstellungen bereitgestellt wird, bleiben die ursprünglichen Einstellungen auf dem Gerät bestehen. Sie können die Konflikte über den Knoten **Richtlinienkonflikte** des Arbeitsbereichs **Richtlinie** anzeigen.

## Siehe auch
[Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

