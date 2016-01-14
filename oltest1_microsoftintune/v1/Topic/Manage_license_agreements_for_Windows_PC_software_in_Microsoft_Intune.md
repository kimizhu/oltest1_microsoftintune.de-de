---
description: na
keywords: na
title: Manage license agreements for Windows PC software in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c59d8635-3f66-40f5-824a-a71c738e0341
---
# Verwalten von Lizenzvertr&#228;gen f&#252;r Windows-PC-Software in Microsoft Intune
Mit [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] können Sie Lizenzvertragsinformationen für Software hinzufügen und verwalten, die im Rahmen von Microsoft-Volumenlizenzverträgen gekauft wurde, sowie für Microsoft- oder Nicht-Microsoft-Software, die auf anderem Wege erworben wurde. Diese Informationen lassen sich zudem in logischen Gruppen organisieren.

> [!IMPORTANT]
> Die Funktion dient nur zum Komfort; es wird keine Genauigkeit garantiert. Sie sollten sich nicht darauf beziehen, um die Einhaltung von Microsoft-Volumenlizenzverträgen zu bestätigen. Die erfassten Daten werden nicht von Microsoft genutzt, um Verstöße gegen Lizenzverträge mit Microsoft bzw. um die Einhaltung solcher Verträge zu untersuchen.
> 
> Lizenzen, die Sie zu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] hinzufügen, wirken sich nicht auf Ihre Lizenzverträge oder auf die Nutzungsberechtigungen für Ihre Software aus.  Beispielsweise werden durch das Löschen eines Lizenzvertragsnummernpaars aus [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] keine Lizenzverträge zwischen Ihnen und Microsoft gelöscht oder annulliert.

Im Arbeitsbereich **Lizenzen** der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Administratorkonsole können Sie folgende Aufgaben ausführen:

-   Hinzufügen und Bearbeiten von Microsoft-Volumenlizenzverträgen

-   Hinzufügen und Bearbeiten anderer Softwarelizenzverträge

-   Verwalten von Lizenzen und Gruppen

-   Vergleichen der Berechtigungsinformationen, die von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] aus dem Volume Licensing Service Center (VLSC) abgerufen werden, mit dem Bestand von Microsoft-Software, die von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] auf den verwalteten Windows-PCs erkannt wird.

Darüber hinaus können Sie Berichte zur Zahl der Installationen und Lizenzen für Softwaretitel erstellen. Mit Lizenzberichten können Sie Ihren gesamten Lizenzierungsstand für Microsoft- und Nicht-Microsoft-Softwaretitel beurteilen.

> [!TIP]
> Der Arbeitsbereich **Lizenzen** wird erst dann in der Administratorkonsole angezeigt, wenn Sie mindestens einen Windows-PC mit dem [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Computerclient verwalten.

## Hinzufügen von Microsoft-Volumenlizenzverträgen
In [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Volumenlizenzverträgen werden Lizenzinformationen für Software, die über Microsoft-Volumenlizenzverträge erworben wurde, bereitgestellt. Sie können [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Microsoft-Volumenlizenzverträge hinzufügen, indem Sie passende Paare von Vertragsnummern angeben. Die Vertrags- oder Autorisierungsnummern müssen der richtigen Lizenz- oder Registrierungsnummer zugeordnet werden. Vertragsnummernpaare erhalten Sie vom [Volume Licensing Service Center (VLSC)](http://go.microsoft.com/fwlink/?LinkID=223842), wenn Sie Lizenzverträge erwerben.

### <a name="BKMK_AddVLAgreements"></a>So fügen Sie einen Microsoft-Volumenlizenzvertrag hinzu

1.  Klicken Sie in der [Microsoft Intune-Administratorkonsole](https://account.manage.microsoft.com/admin/default.aspx) auf **Lizenzen**.

2.  Wählen Sie auf der Seite **Verträge hinzufügen** im Bereich **Vertragstyp auswählen** die Option **Volumenlizenzvertrag** aus.

3.  Wählen Sie im Bereich **Vertragsdetails hinzufügen** eine der folgenden Optionen:

    -   **CSV-Datei mit Vertragsdetails hochladen**: Klicken Sie auf „Durchsuchen“, und wählen Sie die CSV-Datei aus, die hochgeladen werden soll.

        -   Die Datei kann entweder zwei oder drei Spalten enthalten; zwei nur für Vertragsnummernpaare oder drei, wenn Sie für jedes Vertragsnummernpaar einen Anzeigenamen hinzufügen möchten.

        -   Die Gesamtzahl der Zeichen in einem Vertragsnummernpaar darf 16 ASCII-Zeichen nicht überschreiten.

        -   Nur ASCII-Zeichen werden unterstützt.

        -   Folgende Zeichen sind im Vertragsnamen nicht zulässig: **~ ! @ # $ ^ &amp; &#42; ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /**. Leerzeichen sind im Namen zulässig.

        -   Der Dateiname darf eine Länge von 128 Zeichen nicht überschreiten.

        -   Die Datei muss mindestens ein Vertragsnummernpaar und darf höchstens 5.000 Vertragsnummernpaare enthalten.

        **Format der Datei**

        Sie können diese Datei erstellen, indem Sie die Vertragsnummernpaare in ein Nur-Text-Dokument einfügen. Verwenden Sie dazu je nach Ihrem bei VLSC registrierten Organisationstyp eines der nachfolgend aufgeführten Formate. Geben Sie pro Zeile ein Vertragsnummernpaar an.

        -   **Open Value-Kunden:** *Vertragsnummer*, *Vertragsnummer wiederholen*, *Vertragsname*

        -   **Open-Kunden:** *Autorisierungsnummer*, *zugehörige Lizenznummer*, *Vertragsname*

        -   **Select- und Enterprise-Kunden:** *Vertragsnummer*, *zugehörige Registrierungsnummer*, *Vertragsname*

        Sie werden beim Hinzufügen eines neuen Vertrags von dem Formular **Verträge hinzufügen** aufgefordert, nach dieser Datei zu suchen.

        Dies ist ein Beispiel für den Inhalt einer CSV-Datei für einen Open Value-Kunden.

        `01-07001, 01-07001, Office agreements`

    -   **Vertragsdetails manuell eingeben**: Geben Sie die folgenden Informationen an, und geben Sie anschließend in den Feldern **Autorisierungs-/Vertragsnummer** und **Lizenz-/Registrierungs-/Kundennummer** die Vertragsnummernpaare ein. Klicken Sie nach Eingabe der beiden Nummern auf das Symbol **Paar hinzufügen**, um die Nummern zu speichern, und fügen Sie dann bei Bedarf ein neues Paar hinzu.

        -   **Vertragsname**: Geben Sie einen eindeutigen Namen für den Vertrag ein.

            Der Vertragsname darf höchstens 256 Zeichen umfassen. Folgende Zeichen sind nicht zulässig: **~ ! @ # $ ^ &amp; &#42; ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /**. Leerzeichen sind im Namen zulässig.

        -   **Autorisierungs-/Vertragsnummer**: Geben Sie die Autorisierungs-/Vertragsnummer des Lizenzpaars ein.

        -   **Lizenz-/Registrierungs-/Kundennummer**: Geben Sie die Lizenz-/Registrierungs-/Kundennummer des Lizenzpaars ein.

        > [!NOTE]
        > Wenn Sie mehrere Vertragsnummernpaare hinzufügen, wird von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ein Vertrag mit dem Namen, den Sie angeben, erstellt, und alle Paare, die Sie hinzugefügt haben, werden Teil dieses Vertrags.

    Klicken Sie auf **+**, um ein weiteres Vertragsnummernpaar hinzuzufügen, bzw. auf **-**, um ein bereits eingegebenes Vertragsnummernpaar zu entfernen.

4.  Führen Sie im Bereich **Lizenzgruppe auswählen** einen der folgenden Schritte aus:

    -   Wenn Sie die neuen Verträge keiner Lizenzgruppe hinzufügen möchten, wählen Sie **Die Verträge der Gruppe „Nicht zugewiesene Verträge“ hinzufügen** aus. Sie können den Vertrag zu einem späteren Zeitpunkt bearbeiten, um ihn zu einer Gruppe hinzuzufügen.

    -   Wählen Sie **Die Verträge einer neuen Lizenzgruppe hinzufügen** aus, um die neuen Verträge einer neuen Lizenzgruppe hinzuzufügen. Sie werden aufgefordert, einen Namen für die neue Lizenzgruppe einzugeben.

    -   Wählen Sie **Die Verträge einer vorhandenen Lizenzgruppe hinzufügen** aus, um die neuen Verträge einer vorhandenen Lizenzgruppe hinzuzufügen Wählen Sie in der Liste **Gruppenname** die Lizenzgruppe aus, der Sie die Verträge hinzufügen möchten.

5.  Klicken Sie auf **OK**.

Die Ansicht **Alle Verträge** wird angezeigt, und [!INCLUDE[sco_dm_2](../Token/sco_dm_2_md.md)] stellt eine Verbindung mit dem Microsoft Volume Licensing Service Center her, um die angegebenen Vertragsnummernpaare zu überprüfen.

Zum Aktualisieren der Volumenlizenzinformationen nach dem Hinzufügen von Lizenzverträgen in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] klicken Sie auf der Seite **Übersicht über Lizenzen** auf **Jetzt aktualisieren**. Auf diese Weise werden die aktuellen Lizenzinformationen vom [Microsoft Volume Licensing Service Center (VLSC)](http://go.microsoft.com/fwlink/?LinkId=223842) abgerufen.

> [!IMPORTANT]
> Bis zur Aktualisierung der Volumenlizenzinformationen stimmen die Daten in der Vertragsliste möglicherweise nicht mit den Berechtigungsinformationen auf der Seite **Vertragsübersicht** überein

Nach dem Aktualisieren der Volumenlizenzinformationen können Sie die Lizenzinformationen mit Ihrer erkannten Microsoft-Software im Arbeitsbereich **Apps** vergleichen. Sie können zudem die folgenden Lizenzberichte ausführen:

-   **Lizenzkaufberichte**: Mit diesen Berichten können Sie die lizenzierte Software in ausgewählten Lizenzgruppen anzeigen, um Lücken in der Abdeckung zu ermitteln.

-   **Lizenzinstallationsberichte**: Anhand dieser Berichte lässt sich ermitteln, ob Sie über ausreichend Lizenzverträge verfügen.

> [!NOTE]
> Als **Produkttitel** wird für alle Microsoft-Volumenlizenzverträge **Nicht verfügbar** angezeigt.

## Hinzufügen und Bearbeiten anderer Softwarelizenzverträge
Außerdem können Sie zusätzlich zu Microsoft-Volumenlizenzverträgen weitere Typen von Lizenzverträgen zu [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] hinzufügen. Diese Verträge können sowohl Software einschließen, die nicht von Microsoft stammt, als auch Software, die von Microsoft stammt und über einen Händler erworben wurde.

> [!IMPORTANT]
> Es muss mindestens ein Windows-PC in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] registriert sein, bevor Sie einen Vertrag hinzufügen können.  Zusätzlich muss auf mindestens einem registrierten Computer ein lizenzierbares Softwarepaket hochgeladen sein, das Sie zum Hinzufügen eines Lizenzvertrags verwenden möchten.

### <a name="BKMK_AddOtherSoftwareAgreement"></a>So fügen Sie andere Softwareverträge hinzu

1.  Klicken Sie in der [Microsoft Intune-Administratorkonsole](https://account.manage.microsoft.com/admin/default.aspx) auf **Lizenzen**.

2.  Klicken Sie im Bereich **Andere Softwarelizenzverträge** auf **Verträge hinzufügen**.

3.  Wählen Sie auf der Seite **Verträge hinzufügen** im Bereich **Vertragstyp auswählen** die Option **Andere Softwarelizenzverträge** aus.

4.  Geben Sie im Bereich **Vertragsdetails hinzufügen** Folgendes an:

    -   **Vertragsname** (erforderlich). Der Vertragsname darf höchstens 256 Zeichen umfassen. Folgende Zeichen sind nicht zulässig: **~ ! @ # $ ^ &amp; &#42; ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /**. Leerzeichen sind im Namen zulässig.

    -   **Herausgeber** (erforderlich). Wenn Sie mit der Eingabe eines Herausgebers beginnen, werden die Namen aller Herausgeber abgerufen, die die eingegebenen Buchstaben enthalten. Wenn Sie beispielsweise "soft" eingeben, werden alle Herausgebernamen abgerufen, die die Zeichenfolge "soft" im Namen enthalten, z. B. "Microsoft" und "Microsoft Research". Die Herausgebernamen werden vom Software Asset-Katalog bezogen. Bevor Sie den Produkttitel eingeben, müssen Sie den Herausgeber auswählen.

        > [!IMPORTANT]
        > Das Unternehmen, das Sie hinzufügen möchten, wird möglicherweise nicht in dieser Liste angezeigt. Sie können nur Softwareverträge für Unternehmen hinzufügen, die bereits im Software Asset-Katalog vorhanden sind. Microsoft arbeitet jedoch kontinuierlich daran, die beliebtesten Softwaretitel hinzuzufügen. Wenn Sie eine Anforderung zum Hinzufügen eines Unternehmens zu dieser Liste absenden möchten, können Sie dies auf der [Intune Uservoice-Website](https://microsoftintune.uservoice.com/) durchführen.

    -   **Produkttitel** (erforderlich). Wenn Sie mit der Eingabe eines Produkttitels beginnen, werden die Titel aller Produkte abgerufen, die die eingegebenen Buchstaben enthalten. Bevor Sie einen **Produkttitel** angeben können, müssen Sie einen **Herausgeber** angeben.

    -   **Lizenzanzahl** (erforderlich). Geben Sie die Anzahl der erworbenen Lizenzen ein.

    -   **Startdatum der Lizenz**. Geben Sie das Startdatum der Lizenzdeckung ein.

    -   **Lizenzablaufdatum**. Geben Sie das Enddatum der Lizenzdeckung ein.

    -   **Vertragsdetails**. Sie können optional auch Kontaktinformationen, Registrierungsschlüssel und andere Informationen angeben.

5.  Führen Sie im Bereich **Lizenzgruppe auswählen** einen der folgenden Schritte aus:

    -   Wenn Sie die neuen Verträge keiner neuen oder vorhandenen Lizenzgruppe hinzufügen möchten, wählen Sie **Die Verträge der Gruppe "Nicht zugewiesene Verträge" hinzufügen** aus. Sie können die Verträge jederzeit zu benutzerdefinierten Lizenzgruppen hinzufügen.

    -   Wählen Sie **Die Verträge einer neuen Lizenzgruppe hinzufügen** aus, um die neuen Verträge einer neuen Lizenzgruppe hinzuzufügen. Sie werden aufgefordert, einen Namen für die neue Lizenzgruppe einzugeben.

    -   Wählen Sie **Die Verträge einer vorhandenen Lizenzgruppe hinzufügen** aus, um die neuen Verträge einer vorhandenen Lizenzgruppe hinzuzufügen Wählen Sie in der Liste **Gruppenname** die Lizenzgruppe aus, der Sie die Verträge hinzufügen möchten.

6.  Klicken Sie auf **OK**.

Die Listenansicht **Alle Verträge** wird angezeigt.

## <a name="BKMK_LicenseGroups"></a>Verwalten von Lizenzverträgen
Softwarelizenzverträge können zu Lizenzgruppen hinzugefügt werden. Sie können Lizenzgruppen verwenden, um Ihre Lizenzverträge in Einheiten zu organisieren, die für Ihre Organisation logisch sind. Darüber hinaus können Sie Lizenzverträge löschen, die Sie zuvor erstellt haben.

|||
|-|-|
|Aufgabe|Details|
|Erstellen einer Lizenzgruppe|Klicken Sie auf der Seite **Übersicht** des Arbeitsbereichs **Lizenzen** im Menü **Aufgaben** auf die Option **Lizenzgruppe erstellen**. **Note:** Sie können insgesamt bis zu 500 Lizenzgruppen erstellen.|
|Umbenennen einer Lizenzgruppe|Wählen Sie im Arbeitsbereich **Lizenzen** eine Lizenzgruppe aus, und klicken Sie anschließend im Menü **Aufgaben** auf die Option **Lizenzgruppe bearbeiten**.|
|Löschen einer Lizenzgruppe|Wählen Sie im Arbeitsbereich **Lizenzen** eine Lizenzgruppe aus, und klicken Sie anschließend im Menü **Aufgaben** auf die Option **Lizenzgruppe löschen**. **Tip:** Alle Lizenzen in der Gruppe mit zu löschenden Lizenzen werden in die Lizenzgruppe **Nicht zugewiesene Verträge** verschoben.|
|Löschen von Lizenzverträgen|Wählen Sie im Arbeitsbereich **Lizenzen** einen Vertrag aus, und klicken Sie auf **Löschen**. **Tip:** Nach dem Löschen von Volumenlizenzverträgen klicken Sie zum Aktualisieren der Lizenzinformationen auf der Seite **Übersicht über Lizenzen** oder auf der Registerkarte **Allgemein** für eine bestimmte Lizenzgruppe auf **Jetzt aktualisieren**.|

## Siehe auch
[Bereitstellen von Apps auf Windows-PCs in Microsoft Intune](../Topic/Deploy_apps_to_Windows_PCs_in_Microsoft_Intune.md)

