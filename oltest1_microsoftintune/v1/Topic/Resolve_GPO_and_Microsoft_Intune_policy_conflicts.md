---
description: na
keywords: na
title: Resolve GPO and Microsoft Intune policy conflicts
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e76af5b7-e933-442c-a9d3-3b42c5f5868b
---
# L&#246;sen von Konflikten mit Gruppenrichtlinienobjekten und Microsoft Intune-Richtlinien
In [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] können Sie Richtlinien zum Verwalten von Einstellungen auf verwalteten Computern verwenden. Beispielsweise könnten Sie eine Richtlinie verwenden, um Einstellungen für die Windows-Firewall auf Computern zu steuern. Viele der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Einstellungen sind mit Einstellungen vergleichbar, die Sie mit Windows-Gruppenrichtlinien konfigurieren können. Es ist allerdings manchmal möglich, dass die beiden Methoden miteinander in Konflikt stehen.

Im Fall eines Konflikts hat die Gruppenrichtlinie auf Domänenebene Vorrang vor der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinie, sofern die Anmeldung des Computers bei der Domäne möglich ist. In diesem Fall wird die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinie auf den Clientcomputer angewendet.

## <a name="BKMK_plan"></a>Vorgehensweise bei Verwendung von Gruppenrichtlinien
Stellen Sie sicher, dass die Richtlinien, die Sie anwenden, nicht von Gruppenrichtlinien verwaltet werden. Zum Vermeiden von Konflikten können Sie eine oder mehrere der folgenden Methoden verwenden:

-   Verschieben Sie Ihre Computer in eine Active Directory-Organisationseinheit (OU), auf die keine Gruppenrichtlinien angewendet werden, bevor Sie den [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Client installieren. Sie können bei OUs mit Computern, die in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] registriert sind und auf die die Gruppenrichtlinieneinstellungen nicht angewendet werden sollen, auch die Vererbung der Gruppenrichtlinie deaktivieren.

-   Verwenden Sie einen WMI-Filter oder einen Sicherheitsfilter, um Gruppenrichtlinienobjekte auf Computer zu beschränken, die nicht mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltet werden. Weitere Informationen und Beispiele hierzu finden Sie unter [So filtern Sie vorhandene Gruppenrichtlinienobjekte, um Konflikte mit Microsoft Intune-Richtlinien zu vermeiden](../Topic/Resolve_GPO_and_Microsoft_Intune_policy_conflicts.md#BKMK_Filter).

-   Deaktivieren oder entfernen Sie Gruppenrichtlinienobjekte, die mit den [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinien in Konflikt stehen.

Weitere Informationen zu Active Directory und Windows-Gruppenrichtlinien finden Sie in Ihrer Windows Server-Dokumentation.

### <a name="BKMK_Filter"></a>So filtern Sie vorhandene Gruppenrichtlinienobjekte, um Konflikte mit Microsoft Intune-Richtlinien zu vermeiden
Wenn Sie GPOs ermittelt haben, deren Einstellungen in Konflikt mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinien stehen, können Sie eine der folgenden Filtermethoden anwenden, um diese GPOs auf Computer zu beschränken, die nicht mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltet werden.

#### Verwenden Sie WMI-Filter.
Von WMI-Filtern werden GPOs selektiv auf Computer angewendet, die die Bedingungen einer Abfrage erfüllen. Stellen Sie zum Anwenden eines WMI-Filters für alle Computer im Unternehmen eine WMI-Klasseninstanz bereit, bevor Sie Computer bei dem [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienst registrieren.

##### <a name="BKMK_filters"></a>So wenden Sie WMI-Filter auf eine GPO an

1.  Erstellen Sie eine Verwaltungsobjektdatei, indem Sie Folgendes kopieren und in eine Textdatei einfügen und diese dann an einem geeigneten Speicherort unter dem Namen **WIT.mof** speichern. Die Datei enthält die WMI-Klasseninstanz, die Sie für Computer, die Sie für den [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienst registrieren möchten, bereitstellen.

    ```
    //Beginning of MOF file. #pragma classflags("forceupdate") #pragma namespace ("\\\\.\\Root") instance of __Namespace { Name = "WindowsIntune"; }; #pragma namespace ("\\\\.\\Root\\WindowsIntune") [ Description("This class defines Microsoft Intune common properties") ] class WindowsIntune_ManagedNode { [ read, Description("This defines whether Microsoft Intune Policy is enabled"): DisableOverride ToSubClass ] boolean WindowsIntunePolicyEnabled; [ read, key, Description("This property defines the version." "Example: 1.0"): ToSubClass ] string Version; }; instance of WindowsIntune_ManagedNode { Version = "1.0"; WindowsIntunePolicyEnabled = 1; };
    ```

2.  Verwenden Sie zum Bereitstellen der Datei entweder ein Startskript oder eine Gruppenrichtlinie. Das Folgende ist der Bereitstellungsbefehl für das Startskript. Bevor Sie Clientcomputer für den [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienst registrieren, muss die WMI-Klasseninstanz bereitgestellt werden.

    **C:/Windows/System32/Wbem/MOFCOMP &lt;path to MOF file&gt;\wit.mof**

3.  Führen Sie einen der folgenden Befehle aus, um die WMI-Filter zu erstellen. Welchen Befehl Sie ausführen, hängt davon ab, ob das zu filternde GPO für mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltete Computer gilt oder für Computer, die nicht mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltet werden.

    -   Verwenden Sie für Gruppenrichtlinienobjekte, die für nicht über [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltete Computer gelten, den folgenden Befehl:

        ```
        Namespace:root\WindowsIntune Query:  SELECT WindowsIntunePolicyEnabled FROM WindowsIntune_ManagedNode WHERE WindowsIntunePolicyEnabled=0
        ```

    -   Verwenden Sie für Gruppenrichtlinienobjekte, die für über [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltete Computer gelten, den folgenden Befehl:

        ```
        Namespace:root\WindowsIntune Query:  SELECT WindowsIntunePolicyEnabled FROM WindowsIntune_ManagedNode WHERE WindowsIntunePolicyEnabled=1
        ```

4.  Bearbeiten Sie das GPO in der Gruppenrichtlinien-Verwaltungskonsole so, dass der im vorangegangenen Schritt erstellte WMI-Filter zur Anwendung kommt.

    -   Für GPOs, die nur für über [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltete Computer gelten sollen, wenden Sie den Filter **WindowsIntunePolicyEnabled=1** an.

    -   Für GPOs, die nur für nicht über [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltete Computer gelten sollen, wenden Sie den Filter **WindowsIntunePolicyEnabled=0** an.

Weitere Informationen zum Anwenden von WMI-Filtern bei Gruppenrichtlinien finden Sie im Blogbeitrag [Security Filtering, WMI Filtering, and Item-level Targeting in Group Policy Preferences (Sicherheitsfilterung, WMI-Filterung und Zielgruppenadressierung auf Elementebene in Gruppenrichtlinieneinstellungen)](http://go.microsoft.com/fwlink/?LinkId=177883).

#### Verwenden von Sicherheitsgruppenfiltern
Mit einer Gruppenrichtlinie können Sie GPOs auf nur die Sicherheitsgruppen anwenden, die im Bereich **Sicherheitsfilterung** der Gruppenrichtlinien-Verwaltungskonsole für ein ausgewähltes GPO festgelegt sind. Standardmäßig gelten GPOs für **Authentifizierte Benutzer**.

-   Erstellen Sie im Snap-In **Active Directory-Benutzer und -Computer** eine neue Sicherheitsgruppe, die Computer und Benutzerkonten enthält, die nicht über [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] verwaltet werden sollen. Nennen Sie die Gruppe z. B. **Nicht in [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**.

-   Klicken Sie auf der Registerkarte **Delegierung** in der Gruppenrichtlinien-Verwaltungskonsole mit der rechten Maustaste auf die neue Sicherheitsgruppe, um den Benutzern und Computern in der Sicherheitsgruppe die geeigneten Berechtigungen **Lesen** und **Gruppenrichtlinie übernehmen** zu delegieren. (Die Berechtigungen **Gruppenrichtlinie übernehmen** befinden sich im Dialogfeld **Erweitert**.)

-   Wenden Sie dann den neuen Sicherheits-Gruppenfilter auf ein ausgewähltes Gruppenrichtlinienobjekt an, und entfernen Sie den Standardfilter **Authentifizierte Benutzer**.

Die neue Sicherheitsgruppe muss in den [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Dienständerungen als Registrierung verwaltet werden.

## Siehe auch
[Verwalten von Windows-PCs mit Microsoft Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

