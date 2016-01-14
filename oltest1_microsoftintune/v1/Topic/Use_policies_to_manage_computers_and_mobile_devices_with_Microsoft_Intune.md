---
description: na
keywords: na
title: Use policies to manage computers and mobile devices with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec
---
# Verwenden von Richtlinien zum Verwalten von Computern und mobilen Ger&#228;ten mit Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **Richtlinien** sind Gruppen von Einstellungen zur Steuerung der Features auf mobilen Geräten und Computern. Sie erstellen Richtlinien mithilfe von Vorlagen, in denen empfohlene oder angepasste Einstellungen enthalten sind, und stellen diese dann für Geräte- oder Benutzergruppen bereit.

## Erstellen von Konfigurationsrichtlinien
Die Erstellung von Richtlinien unterscheidet sich je nach Richtlinientyp, den Sie erstellen.

Diese Verfahren beziehen sich auf die Erstellung von Konfigurationsrichtlinien.

-   Hilfe bei der Auswahl der richtigen Richtlinie für Ihre Anforderungen finden Sie unter [Verwalten von Einstellungen und Features auf Ihren Geräten mit Microsoft Intune-Richtlinien](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md).

-   Informationen zum Erstellen von Kompatibilitätsrichtlinien finden Sie unter [Verwalten von Gerätekonformitätsrichtlinien für Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md).

-   Informationen zur Erstellung bedingter Zugriffsrichtlinien finden Sie unter [Verwalten des Zugriffs auf E-Mail und SharePoint mit Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

-   Informationen zu Richtlinien für die Unternehmensgeräteregistrierung finden Sie unter [Einrichten der iOS-Verwaltung mit Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).

#### So erstellen Sie eine Richtlinie

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Richtlinie** &gt; **Konfigurationsrichtlinien** &gt; **Hinzufügen**.

2.  Wählen Sie die gewünschte Richtlinie aus, und wählen Sie, ob Sie die empfohlenen Einstellungen für die Richtlinie verwenden (sofern verfügbar, Sie können diese Einstellungen später ändern) oder eine benutzerdefinierte Richtlinie mit Ihren eigenen Einstellungen erstellen möchten.

    > [!TIP]
    > Hilfe bei der Auswahl der richtigen Richtlinie finden Sie unter [Verwalten von Einstellungen und Features auf Ihren Geräten mit Microsoft Intune-Richtlinien](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md).

3.  Wenn Sie bereit sind, klicken Sie auf **Richtlinie erstellen**.

4.  Konfigurieren Sie im Bildschirm **Richtlinie erstellen** einen Namen und optional eine Beschreibung für die Richtlinie.

5.  Konfigurieren Sie die erforderlichen Richtlinieneinstellungen, und klicken Sie dann auf **Richtlinie speichern**.

6.  Klicken Sie im Bestätigungsdialogfeld auf **Ja**, um die Richtlinie jetzt bereitzustellen, oder auf **Nein**, um die Richtlinie zu erstellen, ohne sie bereitzustellen.

Sie können die neue Richtlinie anzeigen und bearbeiten, indem Sie durch die Abschnitte für die einzelnen Richtlinientypen im Arbeitsbereich **Richtlinie** navigieren.

Wenn sie eine Richtlinie erstellen, bei der die empfohlenen Einstellungen verwendet werden, setzt sich der Name der neuen Richtlinie aus dem Vorlagennamen, dem Datum und der Uhrzeit zusammen. Bearbeiten Sie die Richtlinie, dann werden Datum und Uhrzeit im Namen entsprechend dem Zeitpunkt der Bearbeitung angepasst.

Nachdem Sie nun eine Richtlinie erstellt haben, werden Sie sie in der Regel für eine oder mehrere Gruppen von Benutzern oder Geräten bereitstellen.

> [!TIP]
> Sie stellen nicht alle Richtlinientypen bereit. Beispielsweise wird die mobile Anwendungsverwaltungsrichtlinie nicht bereitgestellt. Diese Richtlinie wird stattdessen einer App zugeordnet, die Sie dann bereitstellen.

#### So stellen Sie eine Richtlinie bereit

1.  Wählen Sie im Arbeitsbereich **Richtlinie** die Richtlinie aus, die Sie bereitstellen möchten, und klicken Sie dann auf **Bereitstellung verwalten**.

2.  Führen Sie im Dialogfeld **Bereitstellung verwalten** folgende Schritte aus:

    -   **Wenn Sie die Richtlinie bereitstellen möchten**: Wählen Sie mindestens eine Gruppe aus, für die Sie die Richtlinie bereitstellen möchten, und klicken Sie auf **Hinzufügen** &gt; **OK**.

    -   **Wenn Sie das Dialogfeld schließen möchten, ohne die Richtlinie bereitzustellen:** Klicken Sie auf **Abbrechen**.

Wenn Sie eine bereitgestellte Richtlinie auswählen, können Sie weitere Informationen zur Bereitstellung im unteren Teil der Richtlinienliste anzeigen.

#### So verwalten Sie Richtlinien, die sie bereits erstellt haben

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Richtlinie**, navigieren Sie zu der Richtlinie, die Sie verwalten möchten, und wählen Sie sie aus.

2.  Wählen Sie eine der Aktionen in der folgenden Tabelle aus:

    |Aktion|Weitere Informationen|
    |----------|-------------------------|
    |**Bearbeiten**|Hiermit werden die Eigenschaften für die ausgewählte Richtlinie geöffnet, und Sie können Änderungen daran vornehmen.|
    |**Löschen**|Hiermit wird die ausgewählte Richtlinie gelöscht.<br /><br />Wenn Sie eine Richtlinie löschen, wird sie aus allen Gruppen entfernt, für die sie bereitgestellt worden war.<br /><br />[Was geschieht, wenn eine Richtlinie gelöscht wird oder nicht mehr anwendbar ist](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md#BKMK_What)|
    |**Bereitstellung verwalten**|Wählen Sie im Dialogfeld **Bereitstellung verwalten** die Gruppe aus, für die Sie die Richtlinie bereitstellen möchten, und klicken Sie dann auf **Hinzufügen**.|

## Für Intune-Richtlinien auszuführende Aufgaben

### <a name="BKMK_Refresh"></a>So aktualisieren Sie die Richtlinien auf einem Gerät, um sicherzustellen, dass sie aktuell sind (gilt nur für Computer)

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Gruppen**, und wählen Sie dann eine Gerätegruppe aus.

2.  Wählen Sie die Geräte aus, auf denen die Richtlinien aktualisiert werden sollen, und klicken Sie dann auf **Remoteaufgaben** &gt; **Richtlinien aktualisieren**.

3.  Klicken Sie in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] unten rechts auf **Remoteaufgaben**.

## Weitere Informationen zu Intune-Richtlinien

### Wie lange dauert es für mobile Geräte, bis Richtlinien oder Apps nach ihrer Bereitstellung abgerufen werden?
Wenn eine Richtlinie oder Anwendung bereitgestellt wird, **beginnt [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] sofort mit dem Versuch, das Gerät zu benachrichtigen und zum Einchecken beim [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienst zu veranlassen.** Dies dauert normalerweise weniger als 5 Minuten.

Wenn ein Gerät sich nach der ersten Benachrichtigung nicht zum Abrufen der Richtlinie eincheckt, werden drei weitere Versuche unternommen.  Wenn das Gerät offline ist (z. B. abgeschaltet oder nicht mit einem Netzwerk verbunden), erhält es die Benachrichtigungen möglicherweise nicht.

In diesem Fall erhält das Gerät die Richtlinie beim nächsten geplanten Einchecken beim [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienst wie folgt:

|Plattform|Eincheckhäufigkeit nach der ersten Benachrichtigung|
|-------------|-------------------------------------------------------|
|iOS|Alle 6 Stunden|
|Android|Alle 8 Stunden|
|Windows Phone|Alle 8 Stunden|
|Windows-PCs, die als Geräte registriert sind|Alle 24 Stunden|
Wenn das Gerät gerade registriert wurde, ist die Eincheckfrequenz höher:

|Plattform|Häufigkeit|
|-------------|--------------|
|iOS|Alle 15 Minuten für 6 Stunden und dann alle 6 Stunden|
|Android|Alle 3 Minuten für 15 Minuten, dann alle 15 Minuten für 2 Stunden und dann alle 8 Stunden|
|Windows Phone|Alle 5 Minuten für 15 Minuten, dann alle 15 Minuten für 2 Stunden und dann alle 8 Stunden|
|Windows-PCs, die als Geräte registriert sind|Alle 3 Minuten für 30 Minuten und dann alle 24 Stunden|
Benutzer können auch jederzeit die Unternehmensportal-App starten und das Gerät synchronisieren, um sofort auf Richtlinien zu prüfen.

### Bei welchen Aktionen sendet Intune sofort eine Benachrichtigung an ein Gerät?
Geräte checken bei [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] entweder beim Erhalt einer Benachrichtigung ein, die sie dazu auffordert, oder während ihres regelmäßigen geplanten Eincheckvorgangs, wie in den obigen Tabellen beschrieben.  Wenn Sie für ein Gerät oder einen Benutzer ausdrücklich eine Aktion durchführen wie Zurücksetzen, Sperren, Zurücksetzen der Kennung, App-Bereitstellung, Profilbereitstellung (WiFi, VPN, E-Mail usw.) oder Bereitstellung der Richtlinie, beginnt [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] sofort mit dem Versuch, das Gerät darauf hinzuweisen, dass es sich zum Erhalten dieser Updates beim Intune-Dienst einchecken soll.

Andere Änderungen, wie z. B. die Überarbeitung der Kontaktinformationen im Unternehmensportal, führen nicht zu einer sofortigen Benachrichtigung von Geräten.

### Wie finde ich heraus, welche Einstellungen angewendet werden, wenn für denselben Benutzer oder dasselbe Gerät mehrere Richtlinien bereitgestellt werden?
Bei Bereitstellung mehrerer Richtlinien für denselben Benutzer oder dasselbe Gerät ist es wichtig zu wissen, dass die Bewertung für die jeweils anwendbare Einstellung auf der Ebene einzelner Einstellungen erfolgt.

-   Kompatibilitätsrichtlinieneinstellungen haben immer Vorrang vor Konfigurationsrichtlinieneinstellungen

-   Die restriktivste Kompatibilitätsrichtlinie wird angewendet, wenn sie gegen dieselbe Einstellung in einer anderen Kompatibilitätsrichtlinie ausgewertet wird

-   Die restriktivste Konfigurationsrichtlinie wird angewendet, wenn sie gegen dieselbe Einstellung in einer anderen Konfigurationsrichtlinie ausgewertet wird

### Was geschieht, wenn MAM-Richtlinien (mobile Anwendungsverwaltung) miteinander in Konflikt stehen? Welche wird auf die App angewendet?
Konfliktwerte sind die restriktivsten Einstellungen, die in einer mobilen Anwendungsverwaltungsrichtlinie zur Verfügung stehen, außer für die Zahleneingabefelder (z. B. PIN-Versuche vor dem Zurücksetzen).  Die Zahleneingabefelder werden auf dieselben Werte gesetzt, die auch verwendet werden, wenn Sie eine MAM-Richtlinie in der Konsole mit der Option der empfohlenen Einstellungen erstellen.

Konflikte treten auf, wenn zwei Richtlinieneinstellungen identisch sind.  Beispielsweise haben Sie zwei MAM-Richtlinien konfiguriert, die mit Ausnahme der Einstellung für Kopieren/Einfügen identisch sind.  In diesem Szenario wird die Einstellung für Kopieren und Einfügen auf den restriktivsten Wert festgelegt, die übrigen Einstellungen werden jedoch wie konfiguriert angewendet.

Wenn eine Richtlinie für die Anwendung bereitgestellt wird und in Kraft tritt und anschließend eine weitere bereitgestellt wird, erhält die zuerst bereitgestellte Richtlinie Vorrang und bleibt wirksam, während die zweite als in Konflikt stehend angezeigt wird. Wenn sie jedoch beide gleichzeitig angewendet werden, sodass es keine vorhergehende Richtlinie gibt, befinden sich beide im Konflikt, und alle in Konflikt stehenden Einstellungen werden auf die restriktivsten Werte festgelegt.

### Was geschieht, wenn Sie benutzerdefinierte iOS-Richtlinien in Konflikt stehen?
Intune bewertet nicht die Nutzlast von Apple-Konfigurationsdateien oder der benutzerdefinierten OMA-URI-Richtlinie, es dient lediglich als Übermittlungsmechanismus.

Wenn Sie daher eine benutzerdefinierte Richtlinie bereitstellen, stellen Sie sicher, dass die konfigurierten Einstellungen nicht mit Kompatibilitäts-, Konfigurations- oder anderen benutzerdefinierten Richtlinien in Konflikt stehen. Bei einer benutzerdefinierten Richtlinie mit Einstellungskonflikten werden die Einstellungen in zufälliger Reihenfolge angewendet.

### <a name="BKMK_What"></a>Was geschieht, wenn eine Richtlinie gelöscht wird oder nicht mehr anwendbar ist
Wenn Sie eine Richtlinie löschen oder ein Gerät aus einer Gruppe entfernen, für die eine Richtlinie bereitgestellt wurde, werden die Richtlinie und die Einstellungen entsprechend den folgenden Tabellen vom Gerät entfernt:

#### Mobile Geräte

|Richtlinientyp|Windows|Android|Windows Phone (nur 8.1)|iOS|
|------------------|-----------|-----------|---------------------------|-------|
|WiFi-, VPN-, Zertifikat- und E-Mail-Profile|Entfernt|Entfernt|Entfernt|Entfernt|
|Alle anderen Richtlinientypen|Nicht entfernt|Nicht entfernt|Die folgenden Einstellungen werden entfernt:<br /><br />-   Anfordern eines Kennworts zum Entsperren mobiler Geräte<br />-   Einfache Kennwörter zulassen<br />-   Minimale Kennwortlänge<br />-   Erforderlicher Kennworttyp<br />-   Kennwortablauf (Tage)<br />-   Kennwortverlauf speichern<br />-   Anzahl zulässiger wiederholter Anmeldefehler, bevor das Gerät zurückgesetzt wird<br />-   Minuten der Inaktivität, bevor ein Kennwort erforderlich ist<br />-   Erforderlicher Kennworttyp – Mindestanzahl von Zeichensätzen<br />-   Kamera zulassen<br />-   Verschlüsselung auf mobilem Gerät anfordern<br />-   Wechselspeichermedien zulassen<br />-   Webbrowser zulassen<br />-   App Store zulassen<br />-   Bildschirmaufnahme zulassen<br />-   Geolocation zulassen<br />-   Microsoft-Konto zulassen<br />-   Kopieren und Einfügen zulassen<br />-   WLAN-Tethering zulassen<br />-   Automatische Verbindung mit unverschlüsselten WLAN-Hotspots zulassen<br />-   Berichterstellung für WLAN-Hotspots zulassen<br />-   Zurücksetzen auf Werkseinstellungen zulassen<br />-   Bluetooth zulassen<br />-   NFC zulassen<br />-   WLAN zulassen|Entfernt, **mit Ausnahme von**:<br /><br />-   Sprachroaming zulassen<br />-   Datenroaming zulassen<br />-   Automatische Synchronisierung beim Roaming zulassen|

#### Computer

|Richtlinientyp|Aktion|
|------------------|----------|
|**Endpoint Protection-Einstellungen**|Die empfohlenen Werte der Einstellungen werden wiederhergestellt. Die einzige Ausnahme ist die Einstellung **Microsoft Active Protection Service beitreten**, deren Standardwert **Nein** lautet. Details finden Sie unter [Schützen von Windows-PCs mit Endpoint Protection für Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).|
|**Einstellungen für Softwareupdates**|Einstellungen werden auf den Standardstatus für das Betriebssystem zurückgesetzt. Details finden Sie unter [Aktualisieren Ihrer Windows-PCs mit Softwareupdates in Microsoft Intune](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md).|
|**[!INCLUDE[wit_tools](../Token/wit_tools_md.md)]-Einstellungen**|Alle Kontaktinformationen für Support, die durch die Richtlinie definiert waren, werden von den Computern gelöscht.|
|**Windows-Firewall-Einstellungen**|Einstellungen werden auf den Standard für das Betriebssystem des Computers zurückgesetzt. Details finden Sie unter [Schützen von Windows-PCs mit Endpoint Protection für Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).|

## Siehe auch
[Technische Referenz für Microsoft Intune](../Topic/Technical_reference_for_Microsoft_Intune.md)
[Verwalten von Einstellungen und Features auf Ihren Geräten mit Microsoft Intune-Richtlinien](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md)

