---
description: na
keywords: na
title: Keep Windows PCs up to date with software updates in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64ba8e58-fab1-4480-a440-164268810138
---
# Aktualisieren Ihrer Windows-PCs mit Softwareupdates in Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] unterstützt Sie auf vielfältige Weise bei der Sicherung Ihrer verwalteten Computer, z. B. durch die Verwaltung von Softwareupdates – diese stellt sicher, dass die neuesten Patches und Softwareupdates schnell installiert werden, sodass Ihre Computer immer auf dem neuesten Stand sind.

Wenn Sie den [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Client noch nicht auf Ihren Computern installiert haben, finden Sie weitere Informationen unter [Installieren des Windows-PC-Clients mit Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

Wenn neue Updates bei Microsoft Update verfügbar sind oder Sie ein Drittanbieterupdate erstellt haben und diese Updates auf die von Ihnen verwalteten Computer anwendbar sind, wird eine Benachrichtigung auf der Seite **Übersicht** des Arbeitsbereichs **Updates** angezeigt. Klicken Sie auf diesen Benachrichtigungslink, dann können Sie verschiedene Vorgänge durchführen. Sie können beispielsweise weitere Informationen zum Update anzeigen, das Update genehmigen oder ablehnen und die Computer anzeigen, auf denen das Update im Falle der Genehmigung installiert wird.

> [!IMPORTANT]
> Der Arbeitsbereich **Updates** wird in der Administratorkonsole erst angezeigt, wenn Sie den Client installiert haben und Sie mindestens einen Computerclient erfolgreich verwalten.

Wenn Updates genehmigt und installiert werden, können Sie Erfolg oder Fehlschlag der Installation im Arbeitsbereich **Updates** der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Konsole untersuchen.

Verwenden Sie die Informationen in den folgenden Abschnitten, um die Software auf den von Ihnen verwalteten Computern auf dem aktuellen Stand zu halten.

## Vorbereitung
Bevor Sie mit dem Erstellen und Genehmigen von Softwareupdates beginnen, konfigurieren Sie Richtlinien, mit denen gesteuert wird, wann und wie die Updates installiert werden, und stellen Sie diese auf Ihren Computern bereit.

#### So konfigurieren Sie Einstellungen für Updaterichtlinien

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Richtlinie** &gt; **Übersicht** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie eine Richtlinie für **Microsoft Intune-Agent-Einstellungen** für die Update-Einstellungen, und stellen Sie sie bereit. Sie können die empfohlenen Einstellungen verwenden oder die Einstellungen anpassen. Weitere Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie im Thema [Allgemeine Aufgaben zur Verwaltung von Windows-PCs mit dem Microsoft Intune-Computerclient](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md).

    In den folgenden Tabellen sind die Werte, die Sie in der Richtlinie konfigurieren können, sowie die empfohlenen Werte aufgeführt, die verwendet werden, wenn Sie die Richtlinie nicht anpassen. Sie finden diese Einstellungen im Bereich **Updates**.

    |Richtlinieneinstellung|Weitere Informationen|
    |--------------------------|-------------------------|
    |**Häufigkeit der Suche nach Updates und Anwendungen (Stunden)**|Gibt an, wie häufig (von 8 bis 22 Stunden) [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Überprüfungen auf neue Updates und Anwendungen ausführt.<br /><br />Empfohlener Wert: **8** Stunden.|
    |**Automatische Installation von Updates und Anwendungen oder Installation auf Aufforderung**|Hiermit wird festgelegt, ob Updates automatisch installiert werden, oder ob vor der Installation eine Benutzeraufforderung angezeigt wird. Darüber hinaus können Sie mit dieser Einstellung die Installation von Updates und Anwendungen planen.<br /><br />-   **Mit der automatischen Installation von Updates und Anwendungen nach Plan** werden Updates und Anwendungen unter Berücksichtigung des angegebenen Zeitplans installiert.<br />    **Automatische Wartung für Windows-Computer verwenden** ist eine abhängige Richtlinieneinstellung und gibt an, dass Updates und Anwendungen während des automatischen Wartungsfensters von Windows installiert werden.<br />-   Mit **Benutzer zur Installation auffordern** wird der Benutzer zur Installation aufgefordert, wenn Updates bereitstehen.<br /><br />Empfohlene Werte:<br /><br />-   **Updates und Anwendungen automatisch wie geplant installieren** aktiviert<br />-   **Geplant am: Täglich**<br />-   **Geplante Zeit: 03:00 Uhr**<br />-   **Automatische Wartung für Windows-Computer verwenden** aktiviert|
    |**Sofortige Installation von Updates zulassen, die Windows nicht unterbrechen**|-   **Zulassen** installiert Updates sofort nach dem Herunterladen, außer Updates, die Windows unterbrechen oder neu starten würden. Diese Updates werden entsprechend der Konfiguration der Einstellung **Automatische Installation oder Updateinstallation nach Aufforderung** installiert.<br />-   Durch **Nicht zulassen** werden Updates entsprechend der Konfiguration der Einstellung **Automatische Installation von Updates oder Installation auf Aufforderung** installiert.<br /><br />Empfohlener Wert: **Zulassen**|
    |**Verzögerung des Windows-Neustarts nach der Installation geplanter Updates und Anwendungen (in Minuten)**|Hiermit wird angegeben, wie lange nach der Installation geplanter Updates und Anwendungen gewartet werden soll, bevor Windows neu gestartet wird. Der Wertebereich liegt zwischen 1 und 30 Minuten.<br /><br />Empfohlener Wert: **15 Minuten**|
    |**Verzögerung nach einem Windows-Neustart bis zum Beginn der Installation verpasster geplanter Updates und Anwendungen (Minuten)**|Hiermit wird festgelegt, wie viel Zeit nach einem Windows-Neustart verstreichen darf, bis mit der Installation von Updates und Anwendungen begonnen wird, wenn ein geplantes Update verpasst wurde. Der Wertebereich liegt zwischen 1 und 60 Minuten.<br /><br />Empfohlener Wert: **5 Minuten**|
    |**Angemeldetem Benutzer die Steuerung des Windows-Neustarts nach der Installation geplanter Updates und Anwendungen gestatten**|Hiermit wird angegeben, ob der angemeldete Benutzer den Neustart von Windows verzögern kann (Einstellung **Ja**) oder über den automatischen Neustart von Windows benachrichtigt wird (Einstellung **Nein**). Wenn zum Zeitpunkt der Installation geplanter Updates und Anwendungen kein Benutzer angemeldet ist, wird Windows bei Bedarf automatisch neu gestartet. Bei der Einstellung **Nein** ist die Zeit bis zum Windows-Neustart standardmäßig auf 5 Minuten festgelegt.<br /><br />Empfohlener Wert: **Ja**|
    |**Bei obligatorischen Updates des [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Client-Agents Benutzer zum Neustart von Windows auffordern**|Hiermit wird festgelegt, ob angemeldete Benutzer zum Neustart von Windows aufgefordert werden, wenn ein obligatorisches Update des [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Clients einen Windows-Neustart erfordert.<br /><br />Empfohlener Wert: **Ja**|
    |**Zeitplan für die Installation von obligatorischen Updates des Client-Agents von Microsoft Intune**|Hiermit wird geplant, wann die Installation von Clientupdates stattfindet.<br /><br />Empfohlener Wert: "nicht konfiguriert"|
    |**Verzögerung zwischen Aufforderungen zum Neustart von Windows nach Installation geplanter Updates und Anwendungen (in Minuten)**|Hiermit wird angegeben, wie häufig der Benutzer aufgefordert wird, Windows neu zu starten, wenn nach der Installation eines Updates oder eine Anwendung ein Windows-Neustart erforderlich ist und der Benutzer diesen Neustart verzögert. Der Wertebereich liegt zwischen 1 und 1440 Minuten.<br /><br />Empfohlener Wert: **30 Minuten**|

## Aktualisieren von Microsoft-Software
Das Aktualisieren von Microsoft-Software ist sehr unkompliziert. Bevor Sie jedoch beginnen, müssen Sie zweierlei konfigurieren:

-   **Produktkategorien und Updateklassifizierungen:** Hiermit werden die Kategorien und Klassifizierungen der Updates definiert, die Sie auf Computern verfügbar machen möchten. Sie können beispielsweise festlegen, dass nur kritische Updates für Microsoft Office installiert werden.

-   **Automatische Genehmigungsregeln:** Mit diesen Regeln werden bestimmte Arten von Updates automatisch genehmigt, wodurch der Verwaltungsaufwand verringert wird. Sie sollten beispielsweise automatisch alle kritischen Softwareupdates genehmigen.

Bereiten Sie die Verwendung von Softwareupdates mithilfe der folgenden beiden Verfahren vor:

#### Konfigurieren Sie die Produktkategorien und Updateklassifizierungen, die Sie auf verwalteten Computern verfügbar machen möchten.

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Verwaltung** &gt; **Updates**.

2.  Wählen Sie auf der Seite **Diensteinstellungen: Updates** in der Liste **Produktkategorie** die Updatekategorien aus, die Sie auf Computern verfügbar machen möchten. Beachten Sie, dass die am häufigsten verwendeten Updates standardmäßig aktiviert sind.

    > [!IMPORTANT]
    > Damit sichergestellt ist, dass Computer die vom Administrator genehmigten Updates erhalten, darf die Windows Server Update Services-Gruppenrichtlinieneinstellung **Internen Pfad für den Microsoft Updatedienst angeben** auf die in [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] registrierten Computer nicht angewendet werden.

3.  Wählen Sie in der Liste **Updateklassifizierung** die Updateklassen aus, die Sie auf verwalteten Computern verfügbar machen möchten. Auch hier sind die am häufigsten verwendeten Optionen standardmäßig aktiviert.

4.  Klicken Sie auf **Speichern**, um Ihre Auswahl zu speichern.

#### So konfigurieren Sie automatische Genehmigungsregeln für Softwareupdates

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Verwaltung** &gt; **Updates**.

2.  Klicken Sie im Bereich **Automatische Genehmigungsregeln** der Seite **Servereinstellungen: Updates** auf **Neu**.

3.  Geben Sie auf der Seite **Allgemein** des Assistenten zum Erstellen von automatischen Genehmigungsregeln einen Namen und optional eine Beschreibung für die Regeln an.

4.  Wählen Sie auf der Seite **Produktkategorien** alle Produkte aus, für die Updates automatisch genehmigt werden sollen.

5.  Geben Sie auf der Seite **Updateklassifizierungen** die Updateklassifizierungen an, die automatisch genehmigt werden sollen.

6.  Gehen Sie auf der Seite **Bereitstellung** folgendermaßen vor:

    -   Wählen Sie die Computergruppen aus, für die die neue Regel bereitgestellt werden soll, und klicken Sie auf **Hinzufügen**.

    -   Aktivieren Sie zum Angeben eines Installationszeitlimits für die Updates das Kontrollkästchen **Erzwingen Sie ein Installationszeitlimit für diese Updates**, und wählen Sie aus der Liste **Installationszeitlimit** ein Installationszeitlimit aus.

        > [!NOTE]
        > Wenn Sie ein Installationszeitlimit angeben, muss der verwaltete Computer nach Ablauf des entsprechenden Intervalls möglicherweise einmal oder mehrmals neu gestartet werden.

    -   Klicken Sie danach auf **Weiter**.

7.  Überprüfen Sie auf der Seite **Zusammenfassung** die Einstellungen für die neue Regel, und klicken Sie dann auf **Fertig stellen**.

Die neue Regel wird im Bereich **Automatische Genehmigungsregeln** der Seite **Diensteinstellungen: Updates** angezeigt.

> [!NOTE]
> Wenn Sie eine automatische Genehmigungsregel erstellen, gilt diese nur für zukünftige Updates. In [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] bereits vorhandene Updates werden nicht automatisch genehmigt. Zum Genehmigen dieser Updates müssen Sie die automatische Genehmigungsregel ausführen. Weitere Informationen finden Sie unter [So können Sie eine Regel für die automatische Genehmigung von Updates bearbeiten, ausführen oder löschen](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md#BKMK_editrun) weiter unten in diesem Thema.

### <a name="BKMK_editrun"></a>So können Sie eine Regel für die automatische Genehmigung von Updates bearbeiten, ausführen oder löschen

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Verwaltung** &gt; **Updates**.

2.  Wählen Sie im Bereich **Automatische Genehmigungsregeln** eine Regel aus, und führen Sie dann einen der folgenden Schritte aus:

    -   Klicken Sie zum Bearbeiten der Regel auf **Bearbeiten**, und ändern Sie dann im **Assistenten für automatische Update-Genehmigungsregeln** die Parameter der Regel.

    -   Klicken Sie zum Ausführen der Regel auf **Ausgewählten Satz ausführen**.

    -   Klicken Sie zum Löschen der Regel auf **Löschen**.

        > [!NOTE]
        > Das Löschen einer Regel hat keine Auswirkungen auf vorherige Updates, die durch diese Regel genehmigt wurden.

## Aktualisieren von Software, die nicht von Microsoft herausgegeben wird
Sie können Updates für Software bereitstellen, die nicht von Microsoft stammt. Hierzu verwenden Sie den **Assistenten zum Hochladen von Updates**, mit dem Sie das Update in Ihren Cloud Speicher hochladen; danach können Sie das Update ebenso wie bei Microsoft-Software genehmigen oder ablehnen.

### <a name="procstartwiz"></a>So laden Sie ein Drittanbieterupdate hoch und konfigurieren es

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Updates** &gt; **Übersicht** &gt; **Hochladen**.

2.  Klicken Sie auf der Seite **Updatedateien** auf **Durchsuchen**, um die Setupdateien auszuwählen, die zur Installation des Updatepakets benötigt werden. Hierbei kann es sich um eine Windows Installer-Datei (MSI), eine Windows Installer-Patchdatei (MSP) oder eine Programmdatei (EXE) handeln. Außerdem können Sie ggf. zusätzliche Dateien oder Ordner einschließen, die sich im selben Ordner wie die Setupdatei befinden.

    Die Gesamtgröße der ausgewählten hochzuladenden Dateien wird angezeigt. Beachten Sie, dass diese Größe nicht die unkomprimierten Größen der Installationsdateien beinhaltet.

3.  Nachdem Sie die Setupdateien angegeben haben, werden auf der Seite **Updatebeschreibung** der Name, die Beschreibung und die Klassifizierung für Softwareinformationen angezeigt, die von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] aus den Softwaresetupdateien extrahiert wurden. Sie können eine Klassifizierung auswählen, um den Typ des bereitzustellenden Updates zu markieren (Updates, Kritische Updates, Sicherheitsupdates, Updaterollups oder Service Packs). Klicken Sie auf **Weiter**, wenn Sie fertig sind.

4.  Wählen Sie auf der Seite **Anforderungen** des Assistenten die Architektur (32- und/oder 64-Bit) und die Betriebssysteme der verwalteten Computer aus, auf die das Update anwendbar sein soll.

5.  Geben Sie auf der Seite **Erkennungsregeln** an, wie von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] bestimmt wird, ob ein Update bereits auf verwalteten Computern vorhanden ist. Wenn Sie die Standardoption **Standarderkennungsregeln verwenden** verwenden, wird das Updatepaket von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] auf jedem Zielcomputer genau einmal installiert.

    > [!NOTE]
    > Wenn es sich bei der von Ihnen angegebenen Updatesetupdatei um eine Windows Installer- oder MSP-Datei handelt, wird die Seite **Erkennungsregeln** des Assistenten nicht angezeigt. Dies liegt daran, dass Windows Installer- und MSP-Dateien über eigene Anweisungen zum Erkennen vorheriger Updateinstallationen verfügen.

    Wählen Sie mindestens eine der folgenden Regeln aus, um festzustellen, ob das Update bereits auf verwalteten Computern installiert ist:

    -   **Die Datei ist vorhanden.**

    -   **Der MSI-Produktcode ist vorhanden.**

    -   **Der Registrierungsschlüssel ist vorhanden.**

6.  Geben Sie ggf. weitere Informationen an, die zur Konfiguration der Erkennungsregeln erforderlich sind – beispielsweise einen Dateipfad und -namen, den Windows Installer-Produktcode oder einen Registrierungsschlüssel –, und klicken Sie dann auf **Weiter**.

7.  Auf der Seite **Erforderliche Komponenten** des Assistenten geben Sie an, welche Software bereits installiert sein muss, damit dieses Update installiert werden kann. Sie können **Keine** angeben, ein bereits hinzugefügtes und von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltetes Softwarepaket auswählen oder eine der folgenden Regeln zur Beschreibung der Software angeben:

    -   **Die Datei ist vorhanden.**

    -   **Der MSI-Produktcode ist vorhanden.**

    -   **Der Registrierungsschlüssel ist vorhanden.**

8.  Geben Sie ggf. weitere Informationen an, die zur Konfiguration der Erkennungsregeln erforderlich sind – beispielsweise einen Dateipfad und -namen, den Windows Installer-Produktcode oder einen Registrierungsschlüssel –, und klicken Sie dann auf **Weiter**.

9. Auf der Seite **Befehlszeilenargumente** des Assistenten können Sie erforderliche Installationseigenschaften zur Installationsbefehlszeile hinzufügen, um das Verhalten der Setupdatei zu ändern. Beispielsweise unterstützen verschiedene Softwareprogramme die Eigenschaft **/q** zum Ermöglichen einer automatischen Installation. Weitere Informationen zu unterstützten Befehlszeilenargumenten finden Sie in der Dokumentation zu Ihrem Softwarepaket. Geben Sie ggf. erforderliche Befehlszeilenargumente an, und klicken Sie dann auf **Weiter**.

    > [!NOTE]
    > Wird vom Update keine automatische Installation unterstützt, dann können Sie es nicht mithilfe von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] installieren.

10. Auf der Seite **Rückgabecodes** des Assistenten können Sie angeben, wie Rückgabecodes der Updateinstallation interpretiert werden. Standardmäßig werden in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] die branchenüblichen Rückgabecodes verwendet, um eine fehlerhafte oder erfolgreiche Installation eines Updatepakets zu melden. Die bereitgestellten Rückgabecodes sind:

    |Rückgabecode|Interpretation|
    |----------------|------------------|
    |**0**|Erfolgreich|
    |**3010**|Erfolg mit Neustart|
    Alle nicht aufgeführten Rückgabecodes weisen auf Fehler bei der Installation hin.

    Bei einigen Updates gelten die Standardinterpretationen für Rückgabecodes nicht. In diesem Fall können Sie eigene Interpretationen für die Rückgabecodes angeben.

    Geben Sie die erforderlichen Rückgabecodes an, oder bearbeiten Sie sie, und klicken Sie dann auf **Weiter**.

11. Überprüfen Sie auf der Seite **Zusammenfassung** des Assistenten die Aktionen, die ausgeführt werden, und klicken Sie dann auf **Hochladen**, um den Assistenten abzuschließen.

Das hochgeladene Update wird in dem von Ihnen erworbenen [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Cloudspeicher gespeichert. Wenn nicht mehr ausreichend freier Speicherplatz zur Verfügung steht, um das Updatepaket hochzuladen, werden Sie während des Uploadprozesses darauf hingewiesen.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] kann erst nach dem Start des Updateuploads ermitteln, ob genügend Speicherplatz vorhanden ist, da für komprimierte Setup- und Installationsdateien mehr Speicherplatz benötigt wird, wenn sie entpackt sind.

Nach dem Upload in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] wird ein Drittanbieterupdate im Fensterbereich **Alle Updates** des Arbeitsbereichs **Updates** angezeigt. Sie können das Update dann genehmigen und bereitstellen. Weitere Informationen finden Sie im Abschnitt [Genehmigen und Ablehnen von Updates](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md#BKMK_Approve1) in diesem Thema.

## <a name="BKMK_Approve1"></a>Genehmigen und Ablehnen von Updates
Wenn Updates zur Installation bereit sind, wird auf der Seite **Updateübersicht** des Arbeitsbereichs **Updates** unter **Updatestatus** eine Meldung angezeigt. Klicken Sie auf diese Meldung, um die Seite **Alle Updates** zu öffnen und die Updates anzuzeigen, die zur Genehmigung bereit sind.

Mithilfe der Liste **Filter** können Sie das Suchen nach Updates erleichtern. Beispielsweise können Sie nur fehlgeschlagene oder aber nur solche Updates auflisten, die abgelöst werden.

Wenn Sie ein Update aus der Liste auswählen, werden weitere Befehle verfügbar, mit denen Sie Updates verwalten können. Diese sind in der folgenden Tabelle aufgeführt:

|Aufgabe|Weitere Informationen|
|-----------|-------------------------|
|**Eigenschaften anzeigen**|Hiermit werden ausführliche Informationen zum Update einschließlich der Anzahl der Computer angezeigt, auf die dieses Update angewendet werden kann.|
|**Bearbeiten**|Nur für nicht von Microsoft stammende Updates. Hiermit können Sie die Eigenschaften des Updates bearbeiten.|
|**Genehmigen**|Hiermit wird das ausgewählte Update genehmigt und Ihnen ermöglicht, die Gruppen zu konfigurieren, in denen es bereitgestellt wird. Weitere Informationen finden Sie im Verfahren [So genehmigen Sie Updates](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md#BKMK_Approve) in diesem Thema.|
|**Ablehnen**|Hiermit werden alle früheren Genehmigungen für das Update zurückgezogen, und das Update wird in den Standardansichten ausgeblendet. Darüber hinaus werden alle Berichtsdaten für das Update entfernt.<br /><br />Wenn Sie zu einem späteren Zeitpunkt nach einem abgelehnten Updates suchen möchten, legen Sie für den Filter auf der Seite **Alle Updates** die Einstellung **Abgelehnt** fest. Sie können das Update dann erforderlichenfalls genehmigen. **Note:** Wenn ein Update abgelehnt wurde, weil es in Microsoft Update abgelaufen war, kann dieses Update in [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] nicht genehmigt werden. **Note:** Wenn Sie eine Richtlinie für Updates löschen, die auf Computern bereitgestellt wurde, werden die Werte dieser Updateeinstellungen auf den Standardstatus für das installierte Betriebssystem zurückgesetzt.|
|**Löschen**|Nur für nicht von Microsoft stammende Updates. Hiermit wird das ausgewählte Update gelöscht.|
|**Hochladen**|Hiermit wird der **Assistent zum Hochladen von Updates** gestartet, mit dem Sie bereitzustellende Nicht-Microsoft-Updates hochladen können.|

### <a name="BKMK_Approve"></a>So genehmigen Sie Updates

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Updates** &gt; **Übersicht** &gt; **Neue zu genehmigende Updates**.

    Klicken Sie im Arbeitsbereich **Updates** auf **Übersicht** &gt; **Neue zu genehmigende Updates**.

    > [!NOTE]
    > Der Link **Neue zu genehmigende Updates** wird nur dann im Bereich **Updatestatus** angezeigt, wenn mindestens ein verwalteter Computer vorhanden ist, für den ein Update genehmigt werden muss.

2.  Wählen Sie ein Update aus, überprüfen Sie unten auf der Seite die Updateeigenschaften, um sich zu vergewissern, dass Sie das Update genehmigen möchten, und klicken Sie dann auf **Genehmigen**. Sie können bei gedrückter **CTRL**-Taste auch mehrere Updates auswählen.

3.  Wählen Sie auf der Seite **Gruppen auswählen** eine Gruppe aus, für die Sie die Updates bereitstellen möchten, und klicken Sie auf **Hinzufügen**. Wenn Sie alle Gruppen ausgewählt haben, klicken Sie auf **Weiter**.

4.  Führen Sie auf der Seite **Bereitstellungsaktion** folgende Schritte für jede Gruppe in der Liste aus:

    -   Wählen Sie in der Liste **Genehmigung** eine der folgenden Optionen aus:

        -   **Erforderliche Installation:** Das Update wird auf Computern in der angegebenen Gruppe installiert.

        -   **Nicht installieren:** Hiermit wird nur gemeldet, dass das Update anwendbar ist, es wird jedoch nicht installiert.

        -   **Verfügbare Installation:** Der Benutzer kann die Anwendung bei Bedarf über das Unternehmensportal installieren.

        -   **Deinstallieren:** Hiermit werden Updates von Computern in der Zielgruppe entfernt.

            > [!IMPORTANT]
            > Das Update wird auch dann entfernt, wenn es nicht von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] installiert wurde.

    -   Wählen Sie in der Liste **Stichtag** eine der folgenden Optionen aus:

        -   **Keine:** Es wird kein Stichtag für die Installation des Updates erzwungen, und die Benutzer können das Update immer wieder ablehnen.

        -   **So bald wie möglich** Das Update wird bei nächster Gelegenheit auf allen Zielcomputern installiert.

        -   **Benutzerdefiniert:** Hiermit wird der Zeitpunkt (Datum und Uhrzeit) festgelegt, zu dem genehmigte Updates installiert werden.

        -   **Eine Woche**, **Zwei Wochen**, **Ein Monat**: Hiermit wird das Update innerhalb des angegebenen Zeitraums installiert.

5.  Klicken Sie auf **Fertig stellen**, um die Einstellungen zu speichern, oder klicken Sie auf **Abbrechen**, um die Einstellungen zu verwerfen und zur Updateliste zurückzukehren.

    > [!IMPORTANT]
    > Wenn die Aktion **Nicht installieren**, **Erforderliche Installation** oder **Deinstallieren** nicht explizit für eine untergeordnete Gruppe konfiguriert wurde, wird eine Aktion, die für eine übergeordnete Gruppe konfiguriert wurde, von allen dieser Gruppe untergeordneten Gruppen geerbt.

6.  Sie können unten auf der Seite **Alle Updates** im Detailbereich überprüfen, ob Erinnerungsmeldungen zu dem Update vorhanden sind.

## Benötigen Sie weitere Hilfe?
Weitere Hilfe und weiteren Support finden Sie unter [Problembehandlung für Endpoint Protection in Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

## Siehe auch
[Verwalten von Windows-PCs mit Microsoft Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

