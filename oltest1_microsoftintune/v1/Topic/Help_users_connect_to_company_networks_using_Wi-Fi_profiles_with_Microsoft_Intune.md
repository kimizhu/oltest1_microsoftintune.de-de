---
description: na
keywords: na
title: Help users connect to company networks using Wi-Fi profiles with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b1b86ed-2e80-474d-8437-17dd4bc07b55
---
# Benutzern mithilfe von WLAN-Profilen mit Microsoft Intune die Verbindung mit Unternehmensnetzwerken erleichtern
Verwenden Sie WLAN-Profile in [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], um Benutzern und Geräten in Ihrer Organisation Einstellungen für Drahtlosnetzwerke bereitzustellen. Diese Einstellungen vereinfachen die Verbindung mit Drahtlosnetzwerken für Endbenutzer.

Beispiel:

-   Sie richten ein neues WLAN-Netzwerk mit dem Namen **Contoso Wi-Fi** ein und möchten die nötigen Verbindungseinstellungen auf allen iOS-Geräten bereitstellen.

-   Hierzu erstellen Sie ein WLAN-Profil mit den Einstellungen, die zum Verbinden mit dem Drahtlosnetzwerk **Contoso Wi-Fi** erforderlich sind.

-   Anschließend stellen Sie dieses Profil für alle Benutzer mit iOS-Geräten bereit.

-   Auf den Endgeräten der Benutzer erscheint das Netzwerk **Contoso Wi-Fi** in der Liste der Drahtlosnetzwerke, und es kann bequem eine Verbindung zu diesem Netzwerk hergestellt werden.

Sie können WLAN-Profile auf den folgenden Plattformen bereitstellen:

-   Android 4,0 und höher

-   iOS 7.1 und höher

-   Mac OS X 10.9 und höher

Darüber hinaus können Sie ein WLAN-Profile für Geräte ab Windows 8.1 aus einer vorher exportierten Datei importieren. Details finden Sie unter [Importieren eines WLAN-Profils (Windows 8.1 oder neuer)](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md#BKMK_Import).

## Schritte zum Erstellen und Bereitstellen eines WLAN-Profils

### Schritt 1: Erstellen eines WLAN-Profils mit Angabe allgemeiner Informationen

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Richtlinie hinzufügen**.

2.  Wählen Sie einen der folgenden Richtlinientypen aus, und klicken Sie dann auf **Richtlinie erstellen**:

    -   **WLAN-Profil (Android 4 und höher)**

    -   **WLAN-Profil (iOS 7.1 und höher)**

    -   **WLAN-Profil (Mac OS X 10.9 und höher)**

    Es gibt keine empfohlenen Einstellungen für diesen Richtlinientyp. Sie müssen eine benutzerdefinierte Richtlinie erstellen.

3.  Geben Sie die folgenden allgemeinen Informationen an:

    |Einstellung|Weitere Informationen|
    |---------------|-------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für das WLAN-Profil ein, um es in der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole identifizieren zu können.|
    |**Beschreibung**|Geben Sie eine Beschreibung für das WLAN-Profil ein, um es besser zuordnen zu können.|

### Schritt 2: Konfigurieren der Netzwerk-Verbindungseinstellungen
Geben Sie die **Netzwerkverbindungen**-Werte an:

|Einstellung|Weitere Informationen|
|---------------|-------------------------|
|**Netzwerkname**|Geben Sie einen beschreibenden Namen für das Funknetzwerk an. Dies ist der Name, der auf dem Gerät eines Benutzers angezeigt wird, wenn er ein Drahtlosnetzwerk auswählt.|
|**SSID (Service Set Identifier)**|Geben Sie die (SSID) des Drahtlosnetzwerks an, mit dem sich die Geräte verbinden sollen. Bei der SSID wird die Groß-/Kleinschreibung beachtet. Die SSID wird Benutzern nicht angezeigt.|
|**Automatisch verbinden, wenn dieses Netzwerk in Reichweite ist**|Wählen Sie diese Option, damit sich Geräte automatisch mit dem Drahtlosnetzwerk verbinden, wenn es in Reichweite ist.|
|**Verbinden, selbst wenn das Netzwerk seinen Namen nicht sendet (SSID)**|Wählen Sie diese Option, damit Geräte mit dem Netzwerk verbunden werden können, wenn es nicht in der Liste der Netzwerke angezeigt wird (weil es ausgeblendet ist und seinen Namen nicht sendet).|

### Schritt 3: Konfigurieren der Sicherheitseinstellungen
Konfigurieren Sie die **Sicherheitseinstellungen** für die ausgewählte Plattform. Die verfügbaren Einstellungen hängen von den Typen der Drahtlossicherheit ab, die Sie auswählen.

#### Für Android-Geräte

|Name der Einstellung|Weitere Informationen|Zu verwenden in folgenden Fällen:|
|------------------------|-------------------------|-------------------------------------|
|**Sicherheitstyp**|Wählen Sie das Sicherheitsprotokoll für das Drahtlosnetzwerk:<br /><br />-   **WPA-Enterprise/WPA2-Enterprise**<br />-   **Keine Authentifizierung (Offen)**, wenn das Netzwerk nicht gesichert ist.|Immer|
|**EAP-Typ**|Wählen Sie die den EAP-Typ (Extensible Authentication-Protokoll) zur Authentifizierung von gesicherten Drahtlosverbindungen:<br /><br />-   **EAP-TLS**<br />-   **PEAP**<br />-   **EAP-TTLS**|Wenn Sie den Sicherheitstyp **WPA-Enterprise/WPA2-Enterprise** ausgewählt haben.|
|**Stammzertifikate für die Serverüberprüfung auswählen**|Klicken Sie auf **Auswählen**, und wählen Sie dann das vertrauenswürdige Stammzertifikatprofil zur Authentifizierung der Verbindung. **Important:** Informationen zum Erstellen des vertrauenswürdigen Zertifikatprofils finden Sie unter [Aktivieren des Zugriffs auf Unternehmensressourcen mithilfe von Zertifikatprofilen in Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|Wenn ein beliebiger **EAP-Typ** ausgewählt wurde.|
|**Authentifizierungsmethode**|Wählen Sie die Authentifizierungsmethode für die Verbindung aus:<br /><br />-   **Zertifikate** zur Angabe des Clientzertifikats<br />-   **Benutzername und Kennwort** für eine andere Methode zur Authentifizierung|Bei **PEAP** oder **EAP-TTLS** als **EAP-Typ**.|
|**EAP-fremde Authentifizierungsmethode auswählen (Innere Identität)**|Wählen Sie, wie Sie die Verbindung authentifizieren möchten:<br /><br />-   **Keine**<br />-   **Unverschlüsseltes Kennwort (PAP)**<br />-   **Challenge Handshake Authentication-Protokoll (CHAP)**<br />-   **Microsoft CHAP (MS-CHAP)**<br />-   **Microsoft CHAP, Version 2 (MS-CHAP v2)**<br /><br />Die verfügbaren Optionen hängen vom ausgewählten EAP-Typ ab.|Die **Authentifizierungsmethode** ist **Benutzername und Kennwort**.|
|**Identitätsschutz aktivieren (Äußere Identität)**|Geben Sie den Text ein, der als Antwort auf eine EAP-Identity-Request gesendet werden soll. Dies kann ein beliebiger Text sein. Während der Authentifizierung wird zuerst diese anonyme Identität gesendet und anschließend die echte Kennung über einen sicheren Tunnel.|Bei **PEAP** oder **EAP-TTLS** als **EAP-Typ**.|
|**Wählen Sie ein Clientzertifikat für die Clientauthentifizierung (Identitätszertifikat) aus**|Klicken Sie auf **Auswählen**, und wählen Sie dann das vertrauenswürdige SCEP-Zertifikatprofil zur Authentifizierung der Verbindung. **Important:** Informationen zum Erstellen eines SCEP-Zertifikatprofils finden Sie unter [Aktivieren des Zugriffs auf Unternehmensressourcen mithilfe von Zertifikatprofilen in Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|Der Sicherheitstyp ist **WPA-Enterprise/WPA2-Enterprise** und ein beliebiger **EAP-Typ** wurde ausgewählt.|

#### Für iOS- und Mac OS X-Geräte

|Name der Einstellung|Weitere Informationen|Zu verwenden in folgenden Fällen:|
|------------------------|-------------------------|-------------------------------------|
|**Sicherheitstyp**|Wählen Sie das Sicherheitsprotokoll für das Drahtlosnetzwerk:<br /><br />-   **WPA-Personal/WPA2-Personal**<br />-   **WPA-Enterprise/WPA2-Enterprise**<br />-   **WEP**<br />-   **Keine Authentifizierung (Offen)**, wenn das Netzwerk nicht gesichert ist.|Immer|
|**EAP-Typ**|Wählen Sie die den EAP-Typ (Extensible Authentication-Protokoll) zur Authentifizierung von gesicherten Drahtlosverbindungen:<br /><br />-   **EAP-TLS**<br />-   **PEAP**<br />-   **EAP-TLS**<br />-   **EAP-AST**<br />-   **LEAP**<br />-   **EAP-SIM**|Sie haben den Sicherheitstyp **WPA-Enterprise/WPA2-Enterprise** ausgewählt.|
|**Namen der vertrauenswürdigen Serverzertifikate**|Wählen Sie das vertrauenswürdige Stammzertifikatprofil zur Authentifizierung der Verbindung. **Important:** Informationen zum Erstellen des vertrauenswürdigen Zertifikatprofils finden Sie unter [Aktivieren des Zugriffs auf Unternehmensressourcen mithilfe von Zertifikatprofilen in Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|Sie haben als EAP-Typ **EAP-TLS**, **PEAP**, **EAP-TTLS** oder **EAP-FAST** ausgewählt.|
|**Geschützte Zugriffsanmeldeinformationen (PAC) verwenden**|Wählen Sie die Verwendung von geschützten Zugriffsanmeldeinformationen zum Herstellen eines authentifizierten Tunnels zwischen dem Client und dem Authentifizierungsserver. Eine vorhandene PAC-Datei wird ggf. verwendet.|Der **EAP-Typ** ist **EAP-FAST**.|
|**PAC bereitstellen**|Stellt die PAC-Datei auf Ihren Geräten bereit.<br /><br />Bei Verwendung dieser Option können Sie auch **PAC anonym bereitstellen** auswählen, damit die PAC-Datei ohne Authentifizierung des Servers bereitgestellt wird.|**Geschützte Zugriffsanmeldeinformationen (PAC) verwenden** wurde ausgewählt.|
|**Authentifizierungsmethode**|Wählen Sie die Authentifizierungsmethode für die Verbindung aus:<br /><br /><ul><li>**Zertifikate** zur Angabe des Clientzertifikats</li><li>**Benutzername und Kennwort** für eine der folgenden EAP-fremden Methoden zur Authentifizierung (auch als innere Identität bekannt):<br /><br /><ul><li>**Keine**</li><li>**Unverschlüsseltes Kennwort (PAP)**</li><li>**Challenge Handshake Authentication-Protokoll (CHAP)**</li><li>**Microsoft CHAP (MS-CHAP)**</li><li>**Microsoft CHAP, Version 2 (MS-CHAP v2)**</li><li>**EAP-TLS**</li></ul></li></ul>|Bei **PEAP** oder **EAP-TTLS** als **EAP-Typ**.|
|**Wählen Sie ein Clientzertifikat für die Clientauthentifizierung (Identitätszertifikat) aus**|Wählen Sie das SCEP-Zertifikatprofil zur Authentifizierung der Verbindung. **Important:** Informationen zum Erstellen eines SCEP-Zertifikatprofils finden Sie unter [Aktivieren des Zugriffs auf Unternehmensressourcen mithilfe von Zertifikatprofilen in Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|Wenn der Sicherheitstyp **WPA-Enterprise/WPA2-Enterprise** ist und **EAP-TLS**, **PEAP** oder **EAP-TTLS** als **EAP-Typ** ausgewählt wurde.|
|**Identitätsschutz aktivieren (Äußere Identität)**|Geben Sie den Text ein, der als Antwort auf eine EAP-Identity-Request gesendet werden soll. Dies kann ein beliebiger Text sein.<br /><br />Während der Authentifizierung wird zuerst diese anonyme Identität gesendet und anschließend die echte Kennung über einen sicheren Tunnel.|Wenn **PEAP**, **EAP-TTLS** oder **EAP-FAST** als **EAP-Typ** ausgewählt wurde.|

### Schritt 4: Konfigurieren von Proxyeinstellungen (nur iOS und Mac OS X)

1.  Nehmen Sie für iOS- und Mac OS X-WLAN-Profile die folgenden Einstellungen unter **Proxyeinstellungen** vor (falls Sie einen Proxyserver zum Schutz Ihres Netzwerks verwenden):

    |Name der Einstellung|Weitere Informationen|Zu verwenden in folgenden Fällen:|
    |------------------------|-------------------------|-------------------------------------|
    |**Proxyeinstellungen für diese WLAN-Verbindung**|Wählen Sie die Art der Proxyeinstellungen aus:<br /><br />-   **Keine** (Standard)<br />-   **Manuell**: Sie möchten die URL und die Portnummer des Proxyservers manuell angeben.<br />-   **Automatisch**: Sie möchten eine Konfigurationsdatei verwenden, um den Proxyserver zu konfigurieren.|Immer|
    |**Proxyserveradresse** und **Portnummer**|Geben Sie die URL und die Portnummer des Proxyservers an.|Für **Proxyeinstellungen für diese WLAN-Verbindung** wurde **Manuell** ausgewählt.|
    |**Proxyserver-URL**|Geben Sie die URL der Datei an, die die Proxyservereinstellungen enthält.|Für **Proxyeinstellungen für diese WLAN-Verbindung** wurde **Automatisch** ausgewählt.|

### Schritt 5: Speichern des WLAN-Profils

1.  Klicken Sie danach auf **Richtlinie speichern**.

Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

### Schritt 6: Bereitstellen des WLAN-Profils

1.  Stellen Sie das WLAN-Profil für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrem Unternehmen bereit.

Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Eine Statuszusammenfassung und Warnungen im Arbeitsbereich **Richtlinie** identifizieren Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern. Darüber hinaus wird eine Statusübersicht im Arbeitsbereich **Dashboard** angezeigt.

Nach der erfolgreichen Bereitstellung können sich Benutzer über ihre Geräte automatisch mit dem drahtlosen Unternehmensnetzwerk verbinden, das Sie konfiguriert haben.

## <a name="BKMK_Import"></a>Importieren eines WLAN-Profils (Windows 8.1 oder neuer)
Verwenden Sie zum Importieren von WLAN-Einstellungen für die Bereitstellung an die benötigten Benutzer- und Gerätegruppen **WLAN-Importrichtlinie für Windows**.

> [!TIP]
> In Windows können Sie WLAN-Profile mit dem Dienstprogramm **netsh wlan** in eine XML-Datei exportieren, die von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] gelesen werden kann.
> 
> Geben Sie zum Beispiel den folgenden Befehl zum Exportieren der WLAN-Verbindung **MyConnection** als XML-Datei in der Windows-Eingabeaufforderung ein:
> 
> **netsh wlan export profile MyConnection**

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Richtlinie** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie eine Richtlinie vom Typ **Windows** &gt; **WLAN-Importrichtlinie für Windows**.

    Sie können nur benutzerdefinierte WLAN-Importrichtlinien erstellen und bereitstellen. Empfohlene Einstellungen sind nicht verfügbar.

    Weitere Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie im Thema [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Geben Sie die folgenden allgemeinen Informationen für die WLAN-Importrichtlinie an:

    |Name der Einstellung|Weitere Informationen|
    |------------------------|-------------------------|
    |**Name**|Geben Sie einen eindeutigen Namen für das WLAN-Profil ein, um es in der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole identifizieren zu können.|
    |**Beschreibung**|Geben Sie eine Beschreibung des WLAN-Profils sowie weitere relevante Informationen ein, um es besser zuordnen zu können.|

4.  Geben Sie unter der Überschrift **Benutzerdefiniertes WLAN-Profil** die folgenden Werte en:

    |Name der Einstellung|Weitere Informationen|
    |------------------------|-------------------------|
    |**Profil-Konfigurationsdatei**|Klicken Sie auf **importieren**, und wählen Sie die XML-Datei mit den WLAN-Profileinstellungen, die Sie in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] importieren möchten.|
    |**Name des benutzerdefinierten Konfigurationsprofils (zur Anzeige beim Benutzer)**|Zeigt den Namen des WLAN-Profils an, wie er auf dem Gerät des Benutzers angezeigt wird.|
    |**Details zum Konfigurationsprofil**|Zeigt den XML-Code des ausgewählte Konfigurationsprofils an.|

5.  Klicken Sie danach auf **Richtlinie speichern**.

6.  Die neue Richtlinie wird im Knoten **Konfigurationsrichtlinien** des Arbeitsbereichs **Richtlinie** angezeigt.

Sie können das WLAN-Profil nun mit den Informationen aus **Schritt 6** oben bereitstellen.

## Siehe auch
[Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

