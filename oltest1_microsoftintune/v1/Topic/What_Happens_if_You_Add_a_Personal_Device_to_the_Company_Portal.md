---
description: na
keywords: na
title: What Happens if You Add a Personal Device to the Company Portal
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5703d18a-8b5b-4f47-a393-c2cc6cf7a614
---
# Was geschieht, wenn Sie dem Unternehmensportal ein pers&#246;nliches Ger&#228;t hinzuf&#252;gen?
Wenn Sie dem Unternehmensportal ein Gerät hinzufügen, können Sie problemlos zu installierende Unternehmens-Apps ermitteln, andere von Ihnen hinzugefügte Geräte anzeigen und die Kontaktinformationen Ihres IT-Administrators aufrufen. Sie gestatten damit Ihrem IT-Administrator, Ihr Gerät zu verwalten, damit die Unternehmensinformationen auf dem Gerät geschützt werden. Das Hinzufügen eines Geräts ist für jeden Gerätetyp etwas anders: Einige Geräte werden über die Einstellungen auf dem jeweiligen Gerät und andere durch Herunterladen einer App aus dem App Store des Geräts hinzugefügt.

## <a name="BKMK_IT_can_see"></a>Für die IT nach der Geräteregistrierung in Intune einsehbare und nicht einsehbare Elemente
Anweisungen zum Registrieren Ihres Geräts in Intune finden Sie unter [Registrieren Ihres Geräts in Microsoft Intune](../Topic/Enroll_your_device_in_Microsoft_Intune.md).

|Nicht für die IT einsehbar|Für die IT einsehbar|
|------------------------------|------------------------|
|-   Anrufliste<br />-   SMS<br />-   Persönliche E-Mail, Kontakte und Kalender<br />-   Webverlauf<br />-   Speicherort<br />-   Eigene Aufnahmen<br />-   Personenbezogene Daten|-   Besitzer<br />-   Gerätename<br />-   Seriennummer<br />-   Hersteller<br />-   Modell<br />-   Betriebssystem<br />-   Unternehmens-Apps<br />-   Persönliche Apps|
Wählen Sie den Link für den Typ Ihres Geräts aus, um weitere Details zu erhalten:

-   [Windows Vista, Windows 7, Windows 8 und Windows 8.1 Enterprise und Professional und Windows 10](#BKMK_what_happens_vista)

-   [Windows RT](#BKMK_what_happens_rt)

-   [Windows Phone 8 oder Windows Phone 8.1](#BKMK_what_happens_phone8)

-   [iOS-Geräte (iPhone und iPad)](#BKMK_what_happens_ios)

-   [Android-Geräte](#BKMK_what_happens_android)

-   [Geräte, die nur für E-Mail konfiguriert sind](#BKMK_what_happens_email)

## <a name="BKMK_what_happens_vista"></a>Windows Vista, Windows 7, Windows 8 und Windows 8.1 Enterprise und Professional und Windows 10
Wenn Sie einen Computer hinzufügen:

-   Sie werden auf Ihrem Computer Software sicherlich installiert haben, mit deren Hilfe Ihr IT-Administrator den Computer verwalten kann und mit der Sie Unternehmensressourcen wie Apps und Supportinformationen abrufen können. Diese Software kann automatisch von Ihrem IT-Administrator aktualisiert werden.

-   [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Endpoint Protection ist möglicherweise auf Ihrem Computer installiert. Dies ist eine Software, die den Computer auf Viren und Malware überprüft. Weitere Informationen finden Sie in den [Datenschutzbestimmungen für Microsoft System Center 2012 Endpoint Protection](http://go.microsoft.com/fwlink/?LinkID=247324).

-   Ihr IT-Administrator kann die gesamte auf dem Computer installierte Software inventarisieren. Software, die Sie persönlich installiert haben, kann dabei geschlossen werden.

-   Sie müssen die Bedingungen akzeptieren.

-   Der IT-Administrator kann Daten von der Festplatte Ihres Computers sammeln oder löschen. Ihr IT-Administrator kann auch die gesamte Festplatte löschen.

-   Ihr IT-Administrator kann Apps und Updates auf dem Computer installieren.

-   Ihr IT-Administrator kann Richtlinien auf dem Computer erzwingen. Beispielsweise kann es erforderlich sein, dass Sie ein Kennwort oder eine PIN auf dem Computer festlegen, wobei zu viele falsche Versuche bei der Kennworteingabe zu einer Sperrung des Computers oder zum Löschen sämtlicher Daten von der Festplatte des Computers führen können.

## <a name="BKMK_what_happens_rt"></a>Windows RT
Wenn Sie Ihr Windows RT-Gerät hinzufügen, gewähren Sie Ihrem IT-Administrator eine Zugriffsberechtigung für das Gerät. IT-Administratoren können folgende Dinge tun:

-   Zurücksetzen des Geräts auf die standardmäßigen Werkseinstellungen. Dies ist hilfreich, wenn das Gerät verloren geht oder gestohlen wird.

-   Entfernen aller unternehmensrelevanten Daten und installierten Branchen-Apps. Ihre persönlichen Daten und Einstellungen werden nicht entfernt.

-   Sie müssen die Bedingungen akzeptieren.

-   Erzwingen eines Kennworts oder einer PIN für das Gerät. Dies kann bei zu vielen falschen Versuchen bei der Kennworteingabe zu einer Sperrung des Geräts oder dazu führen, dass das Gerät auf die werkseitigen Standardeinstellungen zurückgesetzt wird. Dabei können auch Daten gelöscht werden.

-   Aktivieren oder Deaktivieren der Verwendung eines Bildkennworts auf Ihrem Gerät.

-   Installieren von Updates für Apps auf dem Gerät.

    > [!NOTE]
    > Dies betrifft nur Updates. IT-Administratoren können nicht erzwingen, dass neue Apps auf Ihrem Gerät installiert werden. Sie können jedoch nach Bedarf Apps, die Ihnen im Unternehmensportal angeboten werden, installieren.

## <a name="BKMK_what_happens_phone8"></a>Windows Phone 8 oder Windows Phone 8.1
Wenn Sie Ihr Windows Phone-Gerät hinzufügen, gewähren Sie Ihrem IT-Administrator eine Zugriffsberechtigung für das Gerät. IT-Administratoren können folgende Dinge tun:

-   Zurücksetzen des Geräts auf die standardmäßigen Werkseinstellungen. Dies ist hilfreich, wenn das Gerät verloren geht oder gestohlen wird.

-   Entfernen aller unternehmensrelevanten Daten und installierten Branchen-Apps. Ihre persönlichen Daten und Einstellungen werden nicht entfernt.

-   Erzwingen eines Kennworts oder einer PIN für das Gerät. Dies kann bei zu vielen falschen Versuchen bei der Kennworteingabe zu einer Sperrung des Geräts oder dazu führen, dass das Gerät auf die werkseitigen Standardeinstellungen zurückgesetzt wird. Dabei können auch Daten gelöscht werden.

-   Erzwingen, dass alle Daten auf dem Gerät verschlüsselt werden. Dadurch werden die Daten geschützt, wenn das Gerät verloren geht oder gestohlen wird.

-   Sie müssen die Bedingungen akzeptieren.

-   Deaktivieren der SD-Karte.

-   Installieren von Updates für Apps auf dem Gerät. Dies betrifft nur Updates. IT-Administratoren können nicht erzwingen, dass neue Apps auf Ihrem Gerät installiert werden. Sie können jedoch nach Bedarf Apps, die Ihnen im Unternehmensportal angeboten werden, installieren.

-   Nachdem das Gerät zum Unternehmensportal hinzugefügt wurde, erfolgt im Intervall von ca. acht Stunden Folgendes:

    -   Herunterladen aller Richtlinien- oder App-Updates, die Ihr IT-Administrator zur Verfügung gestellt hat.

    -   Senden aller Hardwareinventur-Updates.

    -   Senden aller Unternehmens-App-Inventaraktualisierungen.

## <a name="BKMK_what_happens_ios"></a>iOS-Geräte (iPhone und iPad)
Wenn Sie Ihr iPhone- oder iPad-Gerät hinzufügen, gewähren Sie Ihrem IT-Administrator eine Zugriffsberechtigung für das Gerät. IT-Administratoren können folgende Dinge tun:

-   Zurücksetzen des Geräts auf die standardmäßigen Werkseinstellungen. Dies ist hilfreich, wenn das Gerät verloren geht oder gestohlen wird.

-   Entfernen aller unternehmensrelevanten Daten und installierten Branchen-Apps. Ihre persönlichen Daten und Einstellungen werden nicht entfernt.

-   Erzwingen eines Kennworts oder einer PIN auf dem Gerät.

-   Sie müssen die Bedingungen akzeptieren.

-   Aktivieren oder Deaktivieren der Kamera auf dem Gerät.

-   Aktivieren oder Deaktivieren von Webbrowsen auf dem Gerät.

-   Aktivieren oder Deaktivieren der Sicherung in der iCloud.

-   Aktivieren oder Deaktivieren der Dokumentsynchronisierung mit der iCloud.

-   Aktivieren oder Deaktivieren eines Fotostreams in die iCloud.

-   Aktivieren oder Deaktivieren von Datenroaming auf dem Gerät. Wenn Datenroaming zulässig ist, können Roaminggebühren anfallen.

-   Aktivieren oder Deaktivieren von Sprachroaming auf dem Gerät. Wenn Sprachroaming zulässig ist, können Roaminggebühren anfallen.

-   Aktivieren oder Deaktivieren einer automatischen Synchronisierung von Dateien im Roamingmodus auf dem Gerät. Wenn die automatische Synchronisierung von Dateien zulässig ist, können Roaminggebühren anfallen.

## <a name="BKMK_what_happens_android"></a>Android-Geräte
> [!IMPORTANT]
> Wenn Sie auf Ihrem Gerät die ausführliche Protokollierung aktivieren und Protokolle an den Administrator senden, enthalten die Protokolle, die Sie senden, Ihre E-Mail-Adresse.

Wenn Sie Ihr Android-Gerät hinzufügen, gewähren Sie Ihrem IT-Administrator eine Zugriffsberechtigung für das Gerät. IT-Administratoren können folgende Dinge tun:

-   Zurücksetzen des Geräts auf die standardmäßigen Werkseinstellungen. Dies ist hilfreich, wenn das Gerät verloren geht oder gestohlen wird.

-   Entfernen aller unternehmensrelevanten Daten. Ihre persönlichen Daten und Einstellungen werden nicht entfernt.

-   Erzwingen eines Kennworts oder einer PIN für das Gerät. Dies kann bei zu vielen falschen Versuchen bei der Kennworteingabe zu einer Sperrung des Geräts oder dazu führen, dass das Gerät auf die werkseitigen Standardeinstellungen zurückgesetzt wird. Dabei können auch Daten gelöscht werden.

-   Sie müssen die Bedingungen akzeptieren.

-   Aktivieren oder Deaktivieren der Kamera auf dem Gerät.

-   Erzwingen, dass alle Daten, inklusive aller persönlichen und Unternehmensdaten, auf dem Gerät verschlüsselt werden. Dadurch werden die Daten geschützt, wenn das Gerät verloren geht oder gestohlen wird.

-   Nachdem das Gerät zum Unternehmensportal hinzugefügt wurde, erfolgt im Intervall von ca. acht Stunden Folgendes:

    -   Herunterladen aller Richtlinien- oder App-Updates, die Ihr IT-Administrator zur Verfügung gestellt hat.

    -   Senden aller Hardwareinventur-Updates (diese Updates enthalten keine persönlichen Informationen).

    -   Senden aller Unternehmens-App-Inventaraktualisierungen (diese Updates enthalten keine persönlichen Informationen).

## <a name="BKMK_what_happens_email"></a>Geräte, die nur für E-Mail konfiguriert sind
Wenn Sie Ihr Gerät so konfigurieren, dass Sie Ihre geschäftlichen E-Mails verwenden können, gewähren Sie Ihrem IT-Administrator die Zugriffsberechtigung für das Gerät. Hier sind einige Dinge, die IT-Administratoren tun können:

-   Manuelles Zurücksetzen Ihres Geräts auf die Standardeinstellungen des Herstellers oder Konfigurieren des Geräts für die Zurücksetzung, falls zu viele ungültige Versuche bei der Kennworteingabe vorgenommen wurden. Dies ist hilfreich, wenn das Gerät verloren geht oder gestohlen wird.

    > [!IMPORTANT]
    > Durch das Zurücksetzen des Geräts auf die standardmäßigen Werkseinstellungen werden alle von Ihnen installierten persönlichen und Unternehmensdaten und -Apps entfernt.

-   Verlangen, dass das Gerät und alle wechselbaren Speicherkarten verschlüsselt werden müssen.

-   Aktivieren oder Deaktivieren des Herunterladens von E-Mail-Anhängen auf dem Gerät.

-   Angeben, wie oft auf dem Gerät auf geschäftliche E-Mails überprüft wird.

-   Aktivieren oder Deaktivieren von Webbrowsen auf dem Gerät.

-   Festlegen der Anforderungen für das Kennwort oder die PIN, das bzw. die Sie für das Gerät verwenden. IT-Administratoren können z. B. Folgendes vorschreiben:

    -   Bestimmte Länge von Kennwörtern (von vier bis 18 Buchstaben oder Zahlen).

    -   Kombination aus Groß- und Kleinbuchstaben, die im Kennwort verwendet werden muss.

    -   Verwendung von Buchstaben und Symbolen zusätzlich zu Zahlen.

    -   Wie lange ein Gerät inaktiv sein kann, bevor Sie ein Kennwort zum Entsperren eingeben müssen.

    -   Verhindern, dass Sie Kennwörter verwenden, die Sie bisher verwendet haben.

    -   Erzwingen, dass das Gerät auf die standardmäßigen Werkseinstellungen zurückgesetzt wird, wenn es zu viele falsche Kennworteingabeversuche gibt. Dies schützt das Gerät bei Verlust oder Diebstahl.

