---
description: na
keywords: na
title: Mac OS X configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 98b2f19b-bee8-42d7-a215-a716d56a25a3
---
# Einstellungen f&#252;r Mac OS X-Konfigurationsrichtlinien in Microsoft Intune
Verwenden Sie die allgemeine [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**Mac OS X-Konfigurationsrichtlinie** zum Konfigurieren von Einstellungen für:

-   **Gerätesicherheitseinstellungen**: Treffen Sie in einer Liste mit vordefinierten Einstellungen eine Auswahl, mit denen Sie eine Reihe von Features und Funktionen auf dem Gerät steuern können.

-   **Kompatible und nicht kompatible Apps** – Geben Sie eine Liste von Apps an, die in Ihrem Unternehmen kompatibel oder nicht kompatibel sind. Mit dem Bericht über nicht richtlinienkonforme Apps können Sie überprüfen, ob die vom Benutzer installierten Apps zu den von Ihnen als richtlinienkonform angegebenen Apps gehören (die Installation der App kann jedoch nicht blockiert werden).

## Erstellen einer allgemeinen Mac OS X-Konfigurationsrichtlinie

#### So geben Sie grundlegende Einstellungen für die Konfigurationsrichtlinie an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Klicken Sie auf **Mac OS X** &gt; **Allgemeine Konfiguration**, und klicken Sie dann auf **Richtlinie erstellen**.

    > [!NOTE]
    > Sie können keine Konfigurationsrichtlinie mit empfohlenen Einstellungen erstellen. Sie müssen eine benutzerdefinierte Richtlinie erstellen.

3.  Geben Sie im Abschnitt **Allgemein** der Seite **Richtlinie erstellen** einen Namen und eine Beschreibung für die neue Richtlinie ein.

4.  Befolgen Sie die Informationen in den folgenden Abschnitten zum Angeben von Einstellungen für die Richtlinie.

5.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

## Einstellungen für Mac OS X-Geräte
Wenn die gesuchte Einstellung nicht in dieser Liste enthalten ist, können Sie sie ggf. mithilfe einer benutzerdefinierten Mac OS X-Richtlinie erstellen, die Ihnen das Importieren von Einstellungen erlaubt, die Sie mit dem Apple Configurator-Tool erstellt haben. Weitere Informationen finden Sie unter [Benutzerdefinierte Mac OS X-Richtlinieneinstellungen in Microsoft Intune](../Topic/Mac_OS_X_custom_policy_settings_in_Microsoft_Intune.md).

### Kennworteinstellungen

|Name der Einstellung|Beschreibung|
|------------------------|----------------|
|**Anfordern eines Kennworts zum Entsperren von Geräten**|Gibt an, ob für den Zugriff auf einen Mac-Computer ein Kennwort verwendet werden muss. **Important:** Im Gegensatz zu iOS-Geräten wird der Benutzer bei Mac OS X-Geräten nicht umgehend zum Aktualisieren seines Kennworts aufgefordert, um dieser Einstellung zu entsprechen.|
|**Erforderlicher Kennworttyp**|Gibt an, ob das verwendete Kennwort ausschließlich Zahlen enthalten darf oder ob die Verwendung **alphanumerischer Zeichen** (Buchstaben und Zahlen) erforderlich ist. **Important:** Diese Einstellung wird lediglich unter Mac OS X 10.10.3 und höher unterstützt.|
|**Erforderliche Anzahl komplexer Zeichen im Kennwort**|Gibt die Anzahl komplexer Zeichen an, die das Kennwort enthalten muss (**0** bis **4**).<br /><br />Bei komplexen Zeichen handelt es sich um Symbole (z. B. ein Fragezeichen **?**).|
|**Minimale Kennwortlänge**|Gibt die Mindestlänge des Kennworts an (zwischen **4** und **14** Zeichen).|
|**Einfache Kennwörter zulassen**|Ermöglicht die Verwendung einfacher Kennwörter (z. B. **0000** oder **1234**).|
|**Minuten der Inaktivität, bevor ein Kennwort erforderlich ist**|Gibt an, wie lange der Computer inaktiv sein muss, bevor er mithilfe eines Kennworts entsperrt werden muss.|
|**Kennwortablauf (Tage)**|Gibt die Anzahl von Tagen an, nach der der Benutzer das Kennwort ändern muss (**1** bis **255** Tage).|
|**Kennwortverlauf speichern**|Mit dieser Einstellung wird verhindert, dass der Benutzer ein bereits verwendetes Kennwort erneut verwendet. Bei Auswahl dieser Einstellung kann auch **Wiederverwendung vorheriger Kennwörter verhindern** festgelegt werden, um die Anzahl von vorherigen Kennwörtern anzugeben, die nicht erneut verwendet werden dürfen (ein Wert zwischen **1** und **24**).|
|**Minuten Inaktivität bis zur Aktivierung des Bildschirmschoners**|Gibt den Zeitraum in Minuten an, während dessen sich der Computer im Leerlauf befinden muss, bevor der Bildschirmschoner aktiviert wird.|

## Einstellungen für kompatible und nicht kompatible Anwendungen
Aktivieren Sie in der **Liste der richtlinienkonformen und nicht richtlinienkonformen Apps für Mac OS X** die Einstellung **Verwaltete Einstellungen für Geräte**, und geben Sie eine Liste richtlinienkonformer oder nicht richtlinienkonformer Apps mit den folgenden Informationen an:

> [!NOTE]
> Eine einzelne Richtlinie kann nur eine Liste kompatibler oder eine Liste nicht kompatibler Apps enthalten. Sie können nicht beide Typen in derselben Richtlinie angeben.
> 
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ermöglicht das Erstellen eines Berichts mit Geräten, auf denen nicht richtlinienkonforme Apps installiert sind. Die Installation der Apps wird jedoch nicht verhindert, und nicht richtlinienkonforme Apps werden nicht entfernt.

|Name der Einstellung|Beschreibung|
|------------------------|----------------|
|**Nichtkompatibilität melden, wenn Benutzer die aufgelisteten Apps installieren**|Listet die Mac OS X-Apps auf, die Benutzer nicht installieren dürfen. Wenn Benutzer diese Apps installieren, werden sie in den **Berichten über nicht richtlinienkonforme Apps** aufgeführt.|
|**Nichtkonformität melden, wenn Benutzer die nicht aufgelisteten Apps installieren**|Listet die Mac OS X-Apps auf, die Benutzer installieren dürfen. Wenn Benutzer andere Apps installieren, werden diese in den **Berichten über nicht richtlinienkonforme Apps** aufgeführt.|
|**Hinzufügen**|Fügt eine App zur ausgewählten Liste hinzu. Geben Sie einen Namen Ihrer Wahl, optional den Herausgeber der App sowie die Paket-ID der App an. **Tip:** Zum Ermitteln der Paket-ID einer App führen Sie auf einem Mac-Computer, auf dem die App installiert ist, die folgenden Schritte aus:<ol><li>Öffnen Sie den Ordner, in dem die App installiert ist (z. B. **/Programme**)</li><li>Wählen Sie das Paket *&lt;App-Name&gt;***.app** und anschließend **Paketinhalt anzeigen** aus.</li><li>Öffnen Sie die Datei **Info.plist**.</li><li>Überprüfen Sie den Wert, der dem Schlüssel **CFBundleIdentifier** zugewiesen ist.</li></ol>Die Paket-ID weist das Format **com.contoso.appname** auf.|
|**Anwendungen importieren**|Importiert eine Liste von Apps, die Sie in einer CSV-Datei angegeben haben. Verwenden Sie in der Datei das Format App-Name, Herausgeber, Paket-ID der App.|
|**Bearbeiten**|Ermöglicht Ihnen das Bearbeiten der Werte für Name, Herausgeber und Paket-ID der ausgewählten App.|
|**Löschen**|Löscht die ausgewählte App aus der Liste.|
> [!TIP]
> Weitere Informationen zu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Berichten finden Sie unter [Einblicke in Microsoft Intune-Vorgänge durch Berichte](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md).

## Bereitstellen der Konfigurationsrichtlinie
Stellen Sie die Konfigurationsrichtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.

Weitere Informationen zum Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen im Arbeitsbereich **Richtlinie** identifizieren Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

> [!IMPORTANT]
> Wenn sich ein Mac OS X-Gerät im Energiesparmodus befindet, können keine Richtlinien oder Profile bereitgestellt oder inventarisiert werden. Infolgedessen zeigt die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole möglicherweise vorübergehend den Status **Richtlinieneinstellungen mit Fehlern** an, bis das Gerät erneut aktiviert und der Energiesparmodus beendet wird.

## Überwachen kompatibler und nicht kompatibler Apps
Anhand der **Berichte über nicht richtlinienkonforme Apps** können Sie überprüfen, ob die angegebenen Apps richtlinienkonform sind.

#### Ausführen des Berichts

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Berichte** &gt; **Berichte über nicht richtlinienkonforme Apps**.

2.  Wählen Sie die Gerätegruppen aus, die Sie überprüfen möchten, geben Sie an, ob Sie nach kompatiblen und/oder nicht kompatiblen Apps suchen möchten, und klicken Sie dann auf **Bericht anzeigen**.

## Siehe auch
[Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

