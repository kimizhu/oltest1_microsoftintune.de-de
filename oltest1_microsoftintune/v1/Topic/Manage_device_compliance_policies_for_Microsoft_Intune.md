---
description: na
keywords: na
title: Manage device compliance policies for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0775107a-6662-41c8-9404-be14bbb599f3
---
# Verwalten von Ger&#228;tekonformit&#228;tsrichtlinien f&#252;r Microsoft Intune
**Konformitätsrichtlinien** definieren die Regeln und Einstellungen, die ein Gerät erfüllen muss, damit es als mit bedingten Zugriffsrichtlinien konform eingestuft wird. Konformitätsrichtlinien ermöglichen Ihnen auch, Konformitätsprobleme hinsichtlich Geräten unabhängig von bedingten Zugriffsrechten zu überwachen und zu beheben.

Diese Regeln beinhalten:

-   PIN und Kennwörter

-   Verschlüsselung

-   Ob das Gerät per Jailbreak oder Rooting manipuliert wurde

-   Ob der E-Mail-Dienst auf dem Gerät über eine [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinie verwaltet wird

Sie stellen Konformitätsrichtlinien für Benutzer und Geräte bereit. Wenn Sie eine Konformitätsrichtlinie für einen Benutzer bereitstellen, wird die Konformität aller Geräte des Benutzers überprüft.

Die folgende Tabelle enthält die von Konformitätsrichtlinien unterstützten Gerätetypen. Zudem ist darin angegeben, wie nicht konforme Einstellungen gehandhabt werden, wenn die Richtlinie mit einer bedingten Zugriffsrichtlinie verwendet wird.

|Gerätetyp|PIN- oder Kennwortkonfiguration|Geräteverschlüsselung|Per Jailbreak oder Rooting manipuliertes Gerät|E-Mail-Profil|
|-------------|-----------------------------------|-------------------------|--------------------------------------------------|-----------------|
|Windows 8.1 und höher|Wiederhergestellt|N/V|N/V|N/V|
|Windows Phone 8.1 und höher|Wiederhergestellt|Wiederhergestellt|N/V|N/V|
|iOS 6.0 und höher|Wiederhergestellt|Wiederhergestellt (durch Festlegen der PIN)|Unter Quarantäne gestellt (keine Einstellung)|Isoliert|
|Android 4,0 und höher|Isoliert|Isoliert|Unter Quarantäne gestellt (keine Einstellung)|N/V|
|Samsung KNOX Standard 4.0 und höher|Isoliert|Isoliert|Unter Quarantäne gestellt (keine Einstellung)|N/V|
**Wiederhergestellt** = Konformität wird vom Betriebssystem des Geräts erzwungen (z. B. wird der Benutzer gezwungen, eine PIN festzulegen).  Es gibt keinen Fall, in dem die Einstellung nicht konform ist.

**Unter Quarantäne** = Das Betriebssystem des Geräts erzwingt keine Konformität (z. B. zwingen Android-Geräte den Benutzer nicht dazu, das Gerät zu verschlüsseln).  Dies bedeutet:

-   Das Gerät wird blockiert, wenn dem Benutzer eine bedingte Zugriffsrichtlinie zugewiesen wird.

-   Das Unternehmensportal oder Webportal benachrichtigt den Benutzer bezüglich aller Konformitätsprobleme.

## <a name="BKMK_Compliance"></a>Schritt 1: Erstellen einer Kompatibilitätsrichtlinie

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Konformitätsrichtlinien** &gt; **Hinzufügen**.

2.  Konfigurieren Sie auf der Seite **Richtlinie erstellen** die folgenden Einstellungen nach Bedarf:

    |Name der Einstellung|Weitere Informationen|Unterstützte Plattformen|
    |------------------------|-------------------------|----------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für die Konformitätsrichtlinie ein.|-   All|
    |**Beschreibung**|Geben Sie eine Beschreibung ein, die einen Überblick über die Konformitätsrichtlinie schafft.|-   All|
    |**Anfordern eines Kennworts zum Entsperren mobiler Geräte**|Legen Sie fest, dass Benutzer ein Kennwort eingeben müssen, bevor sie auf ihr Gerät zugreifen können.|-   Windows Phone 8 und höher<br />-   iOS 6 und höher<br />-   Android 4,0 und höher<br />-   Samsung KNOX Standard 4.0 und höher|
    |**Einfache Kennwörter zulassen**|Erlauben Sie, dass Benutzer einfache Kennwörter wie "**1234**" oder "**1111**" verwenden können.|-   Windows Phone 8 und höher<br />-   iOS 6 und höher|
    |**Minimale Kennwortlänge**<sup>1</sup>|Gibt die Mindestanzahl an Ziffern oder Zeichen an, die das Benutzerkennwort enthalten muss.|-   Windows Phone 8 und höher<br />-   Windows 8.1<br />-   iOS 6 und höher<br />-   Android 4,0 und höher<br />-   Samsung KNOX Standard 4.0 und höher|
    |**Erforderlicher Kennworttyp**|Gibt an, ob Benutzer ein **alphanumerisches** oder ein **numerisches** Kennwort erstellen müssen.|-   Windows Phone 8 und höher<br />-   Windows RT und Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 und höher|
    |**Minimale Anzahl von Zeichensätzen**<sup>1</sup>|Wenn **Erforderlicher Kennworttyp** auf **Alphanumerisch** festgelegt ist, gibt diese Einstellung die Mindestanzahl an Zeichensätzen an, die das Kennwort enthalten muss.<br /><br />Es gibt vier Zeichensätze:<br /><br />-   Kleinbuchstaben<br />-   Großbuchstaben<br />-   Symbole<br />-   Zahlen<br /><br />Wenn Sie eine höhere Zahl für diese Einstellung festlegen, müssen Benutzer komplexere Kennwörter erstellen.<br /><br />Bei iOS-Geräten bezieht sich diese Einstellung auf die Anzahl an Sonderzeichen (z. B. **!**, **#** und **&amp;**), die im Kennwort enthalten sein müssen.|-   Windows Phone 8 und höher<br />-   Windows RT und Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 und höher|
    |**Kennwortqualität**|Hiermit werden die Kennwortanforderungen für Android-Geräte konfiguriert. Wählen Sie aus:<br /><br />-   **Biometrie auf niedriger Sicherheitsstufe**<br />-   **Erforderlich**<br />-   **Mindestens numerisch**<br />-   **Mindestens alphabetisch**<br />-   **Mindestens alphanumerisch**<br />-   **Alphanumerisch mit Symbolen**|-   Android 4,0 und höher<br />-   Samsung KNOX Standard 4.0 und höher|
    |**Minuten der Inaktivität, bevor ein Kennwort erforderlich ist**|Gibt die Leerlaufzeit an, nach der ein Benutzer sein Kennwort erneut eingeben muss.|-   iOS 6 und höher|
    |**Kennwortablauf (Tage)**|Wählen Sie die Anzahl der Tage, bevor das Kennwort des Benutzers abläuft und er ein neues erstellen muss.|-   Windows Phone 8 und höher<br />-   Windows RT und Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 und höher<br />-   Android 4,0 und höher<br />-   Samsung KNOX Standard 4.0 und höher|
    |**Kennwortverlauf speichern**|Verwenden Sie diese Einstellung in Verbindung mit **Wiederverwendung vorheriger Kennwörter verhindern**, um zu verhindern, dass der Benutzer zuvor bereits verwendete Kennwörter erstellt.|-   Windows Phone 8 und höher<br />-   Windows RT und Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 und höher<br />-   Android 4,0 und höher<br />-   Samsung KNOX Standard 4.0 und höher|
    |**Wiederverwendung vorheriger Kennwörter verhindern**|Wenn **Kennwortverlauf speichern** aktiviert ist, geben Sie die Anzahl der zuvor verwendeten Kennwörter ein, die nicht erneut verwendet werden dürfen.|-   Windows Phone 8 und höher<br />-   Windows RT und Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 und höher<br />-   Android 4,0 und höher<br />-   Samsung KNOX Standard 4.0 und höher|
    |**Verschlüsselung auf mobilem Gerät anfordern**|Erfordert die Verschlüsselung des Geräts, um eine Verbindung mit Ressourcen herzustellen.<br /><br />Geräte unter Windows Phone 8 werden automatisch verschlüsselt. **Important:** Geräte unter iOS werden verschlüsselt, wenn Sie die Einstellung **Kennwort zum Entsperren mobiler Geräte erforderlich** konfigurieren.|-   Windows Phone 8 und höher<br />-   Android 4,0 und höher<br />-   Samsung KNOX Standard 4.0 und höher|
    |**Gerät darf nicht per Jailbreak oder Rooting manipuliert worden sein**|Bei aktivierter Einstellung sind Geräte, die per Jailbreak (iOS) bzw. Rooting (Android) manipuliert wurden, nicht konform.|-   iOS 6 und höher<br />-   Android 4,0 und höher<br />-   Samsung KNOX Standard 4.0 und höher|
    |**E-Mail-Konto muss von Intune verwaltet werden**|Wenn diese Option aktiviert ist, wird das Gerät als nicht konform gemeldet, wenn der Benutzer ein E-Mail-Konto auf dem Gerät eingerichtet hat, das mit einem Intune-E-Mail-Profil übereinstimmt, das von einem IT-Administrator auf dem Gerät bereitgestellt wurde. Intune kann das vom Benutzer bereitgestellte Profil nicht überschreiben und daher nicht verwalten.<br /><br />Zur Sicherstellung der Konformität muss der Benutzer die vorhandenen E-Mail-Einstellungen entfernen; anschließend kann das verwaltete E-Mail-Profil von Intune installiert werden.<br /><br />Ausführliche Informationen zu E-Mail-Profilen finden Sie unter [Konfigurieren des Zugriffs auf Unternehmens-E-Mail mithilfe von E-Mail-Profilen in Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md).|-   iOS 6 und höher|
    |**Wählen Sie das E-Mail-Profil aus, das von Intune verwaltet werden muss**|Wenn **E-Mail-Konto muss von Intune verwaltet werden** aktiviert ist, klicken Sie auf **Auswählen**, um das Intune-E-Mail-Profil auszuwählen, von dem Geräte verwaltet werden müssen. Das E-Mail-Profil muss auf dem Gerät vorhanden sein.|-   iOS 6 und höher|
    <sup>1</sup> Für Geräte, die Windows ausführen und mit einem Microsoft-Konto gesichert sind, ist keine korrekte Auswertung mit der Konformitätsrichtlinie möglich, wenn **Minimale Kennwortlänge** größer als 8 Zeichen oder die **Minimale Anzahl von Zeichensätzen** größer als 2 ist.

3.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konformitätsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## Bereitstellen einer Konformitätsrichtlinie
Stellen Sie die Konformitätsrichtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Verwenden Sie die Statuszusammenfassung und Warnungen auf der Seite **Übersicht** des Arbeitsbereichs **Richtlinie**, um Probleme mit der Richtlinie zu identifizieren, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

## Überwachen der Konformitätsrichtlinie

#### So zeigen Sie Geräte an, die keiner Konformitätsrichtlinie entsprechen

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Gruppen**.

2.  Öffnen Sie die Registerkarte **Richtlinie** für ein beliebiges Gerät, das Konformitätsrichtlinien entspricht ist.

3.  Wählen Sie in der Dropdownliste **Filter** die Option **Entspricht nicht der Konformitätsrichtlinie** aus.

## Wie Intune-Richtlinienkonflikte gelöst werden
Wenn aufgrund mehrerer auf ein Gerät angewendeter Intune-Einstellungen Konflikte auftreten, gelten die folgenden Regeln:

-   Wenn die in Konflikt stehenden Einstellungen zu einer Intune-Konfigurationsrichtlinie und einer Kompatibilitätsrichtlinie gehören, haben die Einstellungen in der Kompatibilitätsrichtlinie Vorrang vor den Einstellungen in der Intune-Konfigurationsrichtlinie, selbst wenn die Einstellungen in der Konfigurationsrichtlinie sicherer sind.

-   Wenn Sie mehrere Kompatibilitätsrichtlinien bereitgestellt haben, werden die sichersten dieser Richtlinien verwendet.

## Nächste Schritte
Sie können die Konformitätsrichtlinien jetzt zusammen mit bedingten Zugriffsrichtlinien verwenden, um den Zugriff auf Dienste in Ihrer Organisation zu steuern.

## Siehe auch
[Verwalten des Zugriffs auf E-Mail und SharePoint mit Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md)

