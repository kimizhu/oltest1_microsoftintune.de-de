---
description: na
keywords: na
title: Common Windows PC management tasks with the Microsoft Intune computer client
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb912c73-54d2-4d78-ac34-3cbe825804c7
---
# Allgemeine Aufgaben zur Verwaltung von Windows-PCs mit dem Microsoft Intune-Computerclient
Lesen Sie die Informationen in diesem Thema, um zu erfahren, wie Sie Computer verwalten, auf denen der [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Client ausgeführt wird. Wenn Sie den Client noch nicht auf Ihren Computern installiert haben, finden Sie weitere Informationen unter [Installieren des Windows-PC-Clients mit Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

## <a name="BKMK_PolicyTasks"></a>Aufgaben, die Microsoft Intune-Richtlinien verwenden

### Verwalten der Windows-Firewall mithilfe von Richtlinien
Mit Richtlinien lässt sich die Verwaltung der Einstellungen der Windows-Firewall auf verwalteten Computern vereinfachen. Details finden Sie unter [Schützen von Windows-PCs mit Endpoint Protection für Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).

### Verwalten des Microsoft Intune Center mithilfe von Richtlinien
Im [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center können Benutzer folgende Aktionen ausführen:

-   Abrufen von Anwendungen aus dem Unternehmensportal

-   Suchen nach Updates

-   Verwalten Sie [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)].

-   Anfordern von Remoteunterstützung

Das [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center ist auf allen verwalteten Computern installiert. Sie können die folgenden Einstellungen in einer [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center-Richtlinie konfigurieren, die dann Benutzern im [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Center angezeigt werden:

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Name**|Name des Administrators, der den Computer verwaltet<br /><br />Maximale Länge: 40 Zeichen|
|**Telefonnummer**|Telefonnummer des Administrators, der den Computer verwaltet<br /><br />Maximale Länge: 20 Zeichen|
|**E-Mail-Adresse**|E-Mail-Adresse des Administrators, der den Computer verwaltet<br /><br />Maximale Länge: 40 Zeichen|
|**Name der Website**|Name der Supportwebsite für Benutzer<br /><br />Maximale Länge: 40 Zeichen|
|**URL der Website**|URL der Supportwebsite<br /><br />Maximale Länge: 150 Zeichen|
|**Hinweise**|Hinweis, der Benutzern angezeigt wird<br /><br />Maximale Länge: 120 Zeichen|

### Verwalten der Einstellungen für Softwareupdates mithilfe von Richtlinien
Mit Richtlinien können Sie die Einstellungen konfigurieren, mit deren Hilfe von verwalteten Computern nach Softwareupdates von Microsoft und Drittanbietern gesucht und diese heruntergeladen werden. Weitere Informationen finden Sie unter [Aktualisieren Ihrer Windows-PCs mit Softwareupdates in Microsoft Intune](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md).

### Verwalten von Endpoint Protection-Einstellungen mithilfe von Richtlinien
Konfigurieren Sie die Einstellungen für [!INCLUDE[epshort](../Token/epshort_md.md)] mithilfe von Richtlinien, und stellen Sie sie dann auf verwalteten Computern bereit. Dies schließt Überprüfungszeitpläne, nach dem Erkennen von Malware durchzuführende Schritte und mehr ein. Weitere Informationen finden Sie unter [Schützen von Windows-PCs mit Endpoint Protection für Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).

## <a name="BKMK_Inventory"></a>Anzeigen des Hardware- und Softwareinventars
Durch [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] werden ausführliche Informationen zur Hardware und Software der verbreiteten Computer erfasst. In den nachfolgend beschriebenen Verfahren lernen Sie, wie Sie

-   Einen Bericht erstellen, in dem Informationen zu den Hardwarefunktionen Ihres Computers aufgeführt sind

-   Einen Bericht erstellen, in dem die auf den jeweiligen Computern installierte Software aufgeführt ist

-   Das Inventar eines Computers aktualisieren, um sicherzustellen, dass die im Bericht enthaltenen Daten aktuell sind

#### So zeigen Sie Informationen zu Ihren Computern an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Berichte** &gt; **Computerinventurberichte**.

2.  Übernehmen Sie auf der Seite **Neuen Bericht erstellen** die Vorgaben, oder passen Sie sie an, um die im Bericht zurückgegebenen Ergebnisse zu filtern. Sie können beispielsweise auswählen, dass nur Computer im Bericht angezeigt werden, auf denen Windows 8.1 ausgeführt wird.

3.  Klicken Sie auf **Bericht anzeigen**, um den **Computerinventurbericht** in einem neuen Fenster anzuzeigen.

    Sie können den Bericht durch Klicken auf die entsprechende Spaltenüberschrift nach jeder Spalte sortieren, z. B. **Name**, **Gehäusetyp** oder **Hersteller**.

#### So zeigen Sie die auf Ihren Computern installierte Software an

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Berichte** &gt; **Berichte zu ermittelter Software**.

2.  Übernehmen Sie auf der Seite **Neuen Bericht erstellen** die Vorgaben, oder passen Sie sie an, um die im Bericht zurückgegebenen Ergebnisse zu filtern. Sie können beispielsweise auswählen, dass nur von Microsoft herausgegebene Software im Bericht angezeigt wird.

3.  Klicken Sie auf **Bericht anzeigen**, um den **Bericht zu ermittelter Software** in einem neuen Fenster anzuzeigen.

    Sie können den Bericht durch Klicken auf die entsprechende Spaltenüberschrift nach jeder Spalte sortieren, z. B. **Name**, **Herausgeber** oder **Kategorie**. Durch Anklicken des Richtungspfeils neben dem Listenelement können Sie die Updates in der Liste erweitern, um weitere Details (zum Beispiel die Computer, auf denen ein Update installiert ist) anzuzeigen.

#### So aktualisieren Sie das Computerinventar, um sicherzustellen, dass es aktuell ist

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Gruppen** &gt; **Alle Geräte** (oder eine andere Gruppe, in der der Computer enthalten ist, für den Sie das Inventar aktualisieren möchten).

2.  Wählen Sie einen Computer aus, oder wählen Sie mit gedrückter **STRG**-Taste mehrere Computer aus.

3.  Klicken Sie auf der Taskleiste auf **Remoteaufgaben** &gt; **Inventar aktualisieren**.

4.  Zur Anzeige des Aufgabenstatus klicken Sie auf **Remoteaufgaben** unten rechts auf der Seite.

    Im Dialogfeld **Taskstatus** werden aktuelle Remoteaufgaben, ihr Status, der Gerätename und etwaige gemeldete Fehler mit einem Link zu Problembehandlungsinformationen aufgelistet.

## <a name="BKMK_Additional"></a>Zusätzliche Aufgaben
Zusätzlich zu den Richtlinien können Sie auch die folgenden Verwaltungsaufgaben auf Ihren Computern ausführen:

#### So führen Sie einen Remoteneustart Ihres Computers durch

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Gruppen** &gt; **Alle Geräte** (oder eine andere Gruppe, in der der Computer enthalten ist, den Sie erneut starten möchten).

2.  Wählen Sie mindestens einen Computer aus, und klicken Sie dann auf **Remoteaufgaben** &gt; **Computer neu starten**.

3.  Zur Anzeige des Aufgabenstatus klicken Sie auf **Remoteaufgaben** unten rechts auf der Seite.

4.  Überprüfen Sie im Dialogfeld **Taskstatus** die aktuellen Remoteaufgaben, den Aufgabenstatus, den Gerätenamen und etwaige gemeldete Fehler.

### <a name="BKMK_Retire"></a>So koppeln Sie einen Computer ab

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Gruppen** &gt; **Alle Geräte** (oder eine andere Gruppe, in der der Computer enthalten ist, den Sie abkoppeln möchten).

2.  Wählen Sie die Geräte aus, die Sie abkoppeln möchten, und klicken Sie dann auf **Abkoppeln/Zurücksetzen**.

Zum erneuten Registrieren eines Computers beim [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienst müssen Sie die Clientsoftware erneut auf dem Computer installieren. Gehen Sie hierzu vor wie im Thema [Installieren des Windows-PC-Clients mit Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md) beschrieben.

Wenn von einem Computer keine Verbindung mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] hergestellt werden kann, wird im Arbeitsbereich **Dashboard** eine Meldung angezeigt.

Wenn Sie einen Computer abkoppeln, werden folgende Aktionen ausgeführt:

-   Der Computer wird aus dem [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Inventar entfernt, und die mit dem Computer verknüpfte Lizenz steht zur erneuten Verwendung zur Verfügung.

-   Der Status des Computers wird nicht mehr in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] angezeigt.

-   Die Clientsoftware wird von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vom Computer entfernt. Wenn der Computer nicht mit dem [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienst verbunden ist, wird die Clientsoftware nach dem nächsten Herstellen der Verbindung entfernt.

-   [!INCLUDE[epshort](../Token/epshort_md.md)] wird vom Computer entfernt. Wenn auf dem Computer eine andere Endpunktanwendung installiert ist und diese deaktiviert ist, kann sie unter Umständen nach dem Entfernen von [!INCLUDE[epshort](../Token/epshort_md.md)] wieder aktiviert werden, um sicherzustellen, dass Ihre Computer geschützt sind.

-   Alle vorhandenen Richtlinien werden vom Computer entfernt, und die durch die Richtlinie festgelegten Werte werden geändert.

-   Der Computer erhält vom [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienst keine Softwareupdates oder aktualisierten Malwaredefinitionen mehr.

-   Abgekoppelte Computer können je nach Konfiguration weiterhin Updates über Windows Server Update Services, Windows Update oder Microsoft Update empfangen.

    > [!IMPORTANT]
    > Wurde die Clientsoftware mithilfe eines Gruppenrichtlinienobjekts installiert, dann müssen Sie zuerst das Gruppenrichtlinienobjekt entfernen, bevor Sie die Clientsoftware entfernen können. So wird verhindert, dass die Software erneut installiert wird.

    Tritt bei der Deinstallation auf dem Client ein Fehler auf, dann finden Sie weitere Hilfe unter [Problembehandlung für Endpoint Protection in Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

### <a name="BKMK_UserDeviceLinking"></a>So verwalten Sie Verknüpfungen zwischen Benutzern und Geräten
Damit Sie Software für einen Benutzer bereitstellen können, müssen Sie diesen zunächst mit einem Computer verknüpfen. Sie können einen Benutzer mit mehreren Computern verknüpfen, aber einzelne Computer nur mit jeweils einem Benutzer. Benutzer werden automatisch mit den Computern verknüpft, die sie über das Unternehmensportal in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] registrieren.

##### So verknüpfen Sie einen Benutzer mit einem Computer

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Gruppen** &gt; **Alle Geräte** (oder eine andere Gruppe, in der der Computer enthalten ist, den Sie mit einem Benutzer verknüpfen möchten).

2.  Wählen Sie den Computer aus, den Sie mit einem Benutzer verknüpfen möchten, und klicken Sie dann auf **Benutzer verknüpfen**.

    Im Dialogfeld **Benutzer verknüpfen** wird eine Liste verfügbarer Benutzer mit ihren Anzeigenamen, Benutzer-IDs und der Anzahl von Computern angezeigt, mit denen die Benutzer jeweils aktuell verknüpft sind. Wenn ein Benutzer bereits mit dem ausgewählten Computer verknüpft ist, werden Name und Benutzer-ID des Benutzers unter **Aktueller Benutzer** angezeigt. Wenn der Computer mit keinem Benutzer verknüpft ist, wird unter **Aktueller Benutzer** der Wert **Kein Benutzer** angezeigt.

3.  Führen Sie einen der folgenden Schritte aus:

    -   Klicken Sie auf **Abbrechen**, um die Verknüpfung des Computers mit einem ggf. vorhandenen aktuellen Benutzer beizubehalten.

    -   Zum Entfernen der Verknüpfung mit dem aktuellen Benutzer klicken Sie ggf. auf **Verknüpfung entfernen** &gt; **OK**.

    -   Zum Verknüpfen des Computers mit einem neuen Benutzer wählen Sie diesen in der Liste **Alle Benutzer** aus. Überprüfen Sie, ob die Benutzerdaten korrekt sind, und klicken Sie auf **OK**.

> [!TIP]
> Wenn Sie die Fähigkeit der Endbenutzer, sich mit Computern zu verknüpfen, einschränken möchten, aktivieren Sie die Option **Fähigkeit der Benutzer einschränken, sich mit Computern zu verknüpfen** in der Richtlinie **-Microsoft Intune-Agent-Einstellungen**.

### Reagieren auf eine Remoteunterstützungsanforderung
Benutzer können mithilfe der Remoteunterstützung über Microsoft Easy Assist, die automatisch auf verwalteten Computern installiert wird, Unterstützung anfordern. Wird eine Anforderung gestellt, dann wird eine Warnung in der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungskonsole angezeigt.

> [!IMPORTANT]
> Eine Remoteunterstützung wird auf Computern mit Windows 8 oder höher nicht unterstützt.
> 
> Wenn Sie eine Remoteunterstützungsanforderung auf einem Computer akzeptieren, auf dem Microsoft Easy Assist nicht installiert ist, werden Sie zur Installation von Easy Assist aufgefordert. Der Computer muss nach der Installation neu gestartet werden. Ziehen Sie in Erwägung, Microsoft Easy Assist bereits vorab auf die Computer Ihres Benutzers zu laden, um diesen Neustart zu umgehen.

##### So verwalten Sie eine Remoteunterstützungsanforderung

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Warnungen** &gt; **Remoteunterstützung**.

2.  Wählen Sie in der Liste **Warnungen** eine Remoteunterstützungsanforderung aus, um die Eigenschaftsseite der Anforderung zu öffnen.

3.  Klicken Sie auf **Anforderung genehmigen und Remoteunterstützung starten**, um ein Dialogfeld mit Optionen zur Behandlung der Warnung zu öffnen.

4.  Führen Sie einen der folgenden Schritte aus:

    -   **Anforderung akzeptieren:** Klicken Sie auf **Remoteunterstützungsanforderung annehmen**, um der Remotesitzung beizutreten.

        Dem Benutzer wird die folgende Meldung angezeigt: **Ihre Anforderung wurde akzeptiert.  Befolgen Sie die Anweisungen in Easy Assist, um ein Programm oder Ihren Desktop für Ihren Systemadministrator freizugeben**.

        > [!IMPORTANT]
        > Sie können keine Remoteunterstützungsanforderung von einem Mac-Computer annehmen, auf dem die [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] ausgeführt wird.

    -   **Anforderung ablehnen:** Schließen Sie das Fenster **Problembehandlungsinformationen anzeigen**, und klicken Sie im Warnungseigenschaftsfenster dann auf **Diese Warnung schließen**.

        Die Anforderung wird geschlossen, und dem Benutzer wird eine Meldung angezeigt, die besagt, dass die Anforderung abgelehnt wurde. Wenn der Benutzer erneut eine Remoteunterstützung anfordern möchte, muss er eine neue Remoteunterstützungsanforderung senden. Wenn Sie versehentlich eine Remoteunterstützungswarnung schließen, wenden Sie sich an den Absender der Remoteunterstützungsanforderung, und bitten Sie diesen Benutzer, eine neue Anforderung zu senden.

## <a name="BKMK_Next"></a>Benötigen Sie weitere Hilfe?
Weitere Hilfe und weiteren Support finden Sie unter [Problembehandlung für Endpoint Protection in Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

## Siehe auch
[Verwalten von Windows-PCs mit Microsoft Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

