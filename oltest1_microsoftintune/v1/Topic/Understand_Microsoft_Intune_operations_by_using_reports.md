---
description: na
keywords: na
title: Understand Microsoft Intune operations by using reports
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 857309c2-61c9-4c22-becf-4839fedeaece
---
# Einblicke in Microsoft Intune-Vorg&#228;nge durch Berichte
Anhand der Informationen in diesem Thema können Sie [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Berichte mit Informationen zu Software, Hardware sowie zu Softwarelizenzen in Ihrer Organisation erstellen und verwalten.

## Verwenden von Berichten
In den [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Berichten finden Sie Informationen zu Software, Hardware und Softwarelizenzen in Ihrem Unternehmen. Mithilfe von Berichten können Sie sich über den aktuellen Stand und den zukünftigen Bedarf informieren. Im Arbeitsbereich **Berichte** finden Sie Tools zum Erstellen und Verwalten von Berichten. Weitere Informationen zu Berichten finden Sie unter [Einblicke in Microsoft Intune-Vorgänge durch Berichte](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md).

### Berichtstypen

|Berichtstyp|Beschreibung|
|---------------|----------------|
|**Updateberichte**|Hierin werden die auf Computern in Ihrer Organisation erfolgreich abgeschlossenen Softwareupdates sowie fehlerhafte, ausstehende und erforderliche Updates angezeigt. Weitere Informationen zu Softwareupdates finden Sie unter [Aktualisieren Ihrer Windows-PCs mit Softwareupdates in Microsoft Intune](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md).|
|**Berichte zu ermittelter Software**|Hierin wird Software angezeigt, die auf Computern in Ihrer Organisation installiert ist. Auch die Softwareversionen sind enthalten. Sie können die angezeigten Informationen nach Herausgeber und Kategorie der Software filtern. Durch Anklicken des Richtungspfeils neben dem Listenelement können Sie die Updates in der Liste erweitern, um weitere Details (zum Beispiel die Computer, auf denen ein Update installiert ist) anzuzeigen. **Note:** Wenn Sie Computer zurückziehen oder deren Gruppenmitgliedschaft in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ändern, kann es einige Minuten dauern, bis die Änderungen im Bericht zu ermittelter Software berücksichtigt werden. Um möglichst präzise Softwareinventardaten zu erhalten, warten Sie nach dem Abkoppeln von Computern oder Ändern ihrer Gruppenmitgliedschaft einige Minuten, bevor Sie einen Bericht über erkannte Software ausführen, der diese Computer enthält.|
|**Computerinventurberichte**|Hierin werden Informationen zu verwalteten Computern in Ihrer Organisation angezeigt. Mithilfe dieses Berichts können Sie den Erwerb von Hardware planen und den Hardwarebedarf der Benutzer in Ihrer Organisation besser nachvollziehen. Weitere Informationen zum Arbeiten mit verwalteten Computern finden Sie unter [Verwalten von Windows-PCs mit Microsoft Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md).|
|**Inventurberichte für mobile Geräte**|Hierin werden Informationen zu den mobilen Geräten in Ihrer Organisation angezeigt. Sie können die angezeigten Informationen nach Gruppen, entfernten Nutzungsbeschränkungen und Betriebssystem filtern.|
|**Lizenzkaufberichte**|Hierin werden die Softwaretitel jeder lizenzierten Software in ausgewählten Lizenzgruppen auf Basis ihrer Lizenzverträge angezeigt. Folgende Filter sind verfügbar:<br /><br />-   **Alle Verträge**: Es werden alle lizenzierten Softwareprodukte angezeigt, die mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltet werden.<br />-   **Volumenlizenzverträge** zeigt nur VLSC-Softwareprodukte an.<br />-   **Andere Softwarelizenzverträge** zeigt Softwareprodukte an, die außerhalb des VLSC verwaltet werden. **Note:** Wenn die Softwarelizenzinformationen seit mehr als 24 Stunden nicht aktualisiert wurden, werden sie beim Erstellen eines Lizenzberichts aktualisiert.<br />Ein Lizenzbericht stellt keine genaue Berechnung von verwendeten Softwaretiteln und keinen Nachweis der Erfüllung von Verträgen dar. Der Bericht ist ein Tool, das Ihnen dabei hilft, Lizenzierungsentscheidungen für Ihre Organisation zu treffen. Von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] werden möglicherweise nicht alle Produkte erkannt, für die Microsoft-Volumenlizenzen verfügbar sind.|
|**Lizenzinstallationsberichte**|Hierin wird die auf Computern in Ihrer Organisation installierte Software mit Ihrer aktuellen Lizenzvertragsabdeckung laut Volume Licensing Service Center (VLSC) verglichen. Zu den Filtern gehören:<br /><br />-   **Alle Verträge**: Es werden alle lizenzierten Softwareprodukte angezeigt, die mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltet werden.<br />-   **Volumenlizenzverträge** zeigt nur VLSC-Softwareprodukte an.<br />-   **Andere Softwarelizenzverträge** zeigt Softwareprodukte an, die außerhalb des VLSC verwaltet werden.|
|**Berichte zu Nutzungsbedingungen**|Hierin wird angezeigt, ob die Benutzer die von Ihnen bereitgestellten Nutzungsbedingungen akzeptiert haben und welche Version sie akzeptiert haben. Sie können bis zu 10 Benutzer angeben, deren Annahmestatus von beliebigen ihnen bereitgestellten Nutzungsbedingungen angezeigt werden, oder den Annahmestatus für eine bestimmte Bedingung anzeigen.|
|**Nicht kompatible Apps-Berichte**|Es werden Informationen zu den Benutzern mit installierten Apps angezeigt, die in Ihren Listen der kompatiblen und nicht kompatiblen Apps enthalten sind. Verwenden Sie diesen Bericht, um Benutzer und Geräte zu ermitteln, die nicht mit Ihren Unternehmens-App-Richtlinien konform sind.|
|**Berichte zur Zertifikatkompatibilität**|Zeigt an, welche Zertifikate für Benutzer und Geräte über den Registrierungsdienst für Netzwerkgeräte ausgestellt wurden. Verwenden Sie diesen Bericht, um ausgestellte, abgelaufene und gesperrte Zertifikate zu suchen.|
|**Berichte zum Geräteverlauf**|Zeigt ein historisches Protokoll von Abkoppeln-, Zurücksetzen- und Löschen-Aktionen. Verwenden Sie diesen Bericht, um zu ermitteln, welcher Benutzer in der Vergangenheit Aktionen auf Geräten initiiert hat.|
|**Mac OS X-Hardwarebericht**|Hierin werden Hardwaredetails zu allen registrierten Mac OS X-Geräten in den von Ihnen ausgewählten Gruppen angezeigt. Informationen zu dem von diesen Geräten erfassten Hardwareinventar finden Sie unter [Verstehen Sie Ihre Geräte mithilfe des Inventars in Microsoft Intune](../Topic/Understand_your_devices_with_inventory_in_Microsoft_Intune.md).|
|**Mac OS X-Softwarebericht**|Hierin wird die auf allen Mac OS X-Geräten in den von Ihnen ausgewählten Gruppen installierte Software angezeigt. Im Bericht wird Folgendes aufgeführt:<br /><br />-   Der Softwarename (als Paket-ID)<br />-   Die Kurzversion des Namens (oder der Anzeigename)<br />-   Die Version<br />-   Die Anzahl von Geräten, auf denen die Software installiert ist|

#### So erstellen Sie einen Bericht

1.  Klicken Sie in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] auf **Berichte** und dann auf den Berichtstyp, der erstellt werden soll, wie in der Tabelle oben beschrieben.

2.  Übernehmen Sie auf der Seite **Neuen Bericht erstellen** die Vorgaben, oder passen Sie sie an, um die im Bericht zurückgegebenen Ergebnisse zu filtern. Sie können beispielsweise auswählen, dass nur von Microsoft herausgegebene Software im Bericht über erkannte Software angezeigt werden soll.

3.  Klicken Sie auf **Bericht anzeigen**, um den Bericht in einem neuen Fenster zu öffnen.

Sie können den Bericht nach jeder Spalte sortieren, indem Sie auf die entsprechende Spaltenüberschrift klicken. Zusätzlich können Sie bei einigen Berichten Listenelemente erweitern, um mehr Details anzeigen zu lassen.

## Weitere Berichtsaktionen
Zusätzlich werden von Berichten die folgenden Aktionen unterstützt:

|Aktion|Weitere Informationen|
|----------|-------------------------|
|**Drucken**|Klicken Sie in einem geöffneten Bericht auf das Drucken-Symbol, und folgen Sie den Anweisungen.|
|**Exportieren**|Klicken Sie in einem geöffneten Bericht auf das Exportieren-Symbol, und folgen Sie den Anweisungen. Sie können einen Bericht im CSV- (kommagetrennte Werte) oder HTML-Format exportieren.|
|**Speichern**|Auf der Seite **Neuen Bericht erstellen** können von jedem Benutzer bis zu 100 Berichte gespeichert werden. Konfigurieren Sie die Berichtsparameter wie gewünscht, und klicken Sie dann auf **Speichern** oder auf **Speichern unter**, wenn Sie einen anderen Namen verwenden möchten.|
|**Laden**|Klicken Sie auf der Seite **Neuen Bericht erstellen** auf **Laden**, um zuvor gespeicherte Sätze von Berichtsparametern abzurufen.|
|**Löschen**|Wählen Sie im Arbeitsbereich **Berichte** den gewünschten Berichtstyp aus, klicken Sie auf **Laden** und dann in der Berichtsliste auf das Löschen-Symbol (X) neben dem Bericht.|

## Siehe auch
[Überwachung und Berichte in Microsoft Intune](../Topic/Monitoring_and_reports_with_Microsoft_Intune.md)

