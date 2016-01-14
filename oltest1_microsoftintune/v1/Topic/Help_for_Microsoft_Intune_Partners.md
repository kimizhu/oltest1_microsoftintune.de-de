---
description: na
keywords: na
title: Help for Microsoft Intune Partners
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9cb7da1d-8ecb-4b08-818a-54782e846def
---
# Hilfe f&#252;r Microsoft Intune-Partner
Das Partnerportal und die enthaltenen Dienste sind eine Erweiterung Ihres [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Abonnements und sind mit Ihrer Partneridentität verknüpft. Wenn Sie sich beim [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Kontoportal mit einem Geschäftskonto anmelden, das mit Ihrer Partner-ID verknüpft ist, erhalten Sie Zugriff auf das Partnerportal über den Link **Partner** im oberen Bereich des Kontoportals.

|Was möchten Sie tun?|Details|
|------------------------|-----------|
|**Überprüfen Ihrer Unternehmensinformationen**|Achten Sie darauf, dass Ihre Firmeninformationen wie Telefonnummern und E-Mail-Adressen stets korrekt sind, da diese Ihren Kunden angezeigt werden.<br /><br />Klicken Sie am linken Rand des Partnerportals auf Ihren Firmennamen, um Ihre Firmeninformationen anzuzeigen und zu bearbeiten.<br /><br />Ihr Benutzerkonto muss ein [globaler Administrator](http://technet.microsoft.com/library/dn646966.aspx#BKMK_AdminAccounts) sein, um Ihre Firmeninformationen bearbeiten zu können.|
|**Kunden finden**|Mit dem Partnerportal können Sie [Suchen und Unterstützen von Kunden](../Topic/Help_for_Microsoft_Intune_Partners.md#BKMK_FindCustomers), denen Sie Dienste anbieten möchten, oder mit denen Sie bereits arbeiten.<br /><br />Sie können Kunden, die Abonnenten von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] sind, nach deren Benutzerkontoname oder deren Domänenname suchen.|
|**Erstellen und Verschicken von Kaufangeboten und Einladungen zum Testen**|Als Partner können Sie [Erstellen von Kaufangeboten und Einladungen zum Testen](../Topic/Help_for_Microsoft_Intune_Partners.md#BKMK_CreateTrials), mit denen Kunden den Dienst zunächst ausprobieren und anschließend einen Kauf vornehmen können.<br /><br />Ihre Angebote enthalten einen Link, über den Kunden auf das Angebot zugreifen können. Der Link enthält einen eingebetteten Code, der Sie als Abonnementberater identifiziert.|
|**Anbieten delegierter Administration**|Als Partner können Sie [Anbieten delegierter Administration](../Topic/Help_for_Microsoft_Intune_Partners.md#BKMK_OfferAdmin). Mit dieser Funktion können Benutzer aus Ihrer Firma Ihren Kunden zusätzlichen Support anbieten.|
|**Konfigurieren Ihrer Benutzer als delegierte Administratoren**|Neben der Verwaltung Ihres eigenen Firmenabonnements, (inkl. der Vergabe von administrativem Zugriff für Ihr Abonnement an Benutzer) können Sie auch [Vergabe von Benutzerberechtigungen für delegierte Administration](../Topic/Help_for_Microsoft_Intune_Partners.md#BKMK_AssignDelAdmin) für Unternehmen, denen Sie Support anbieten.|
|**Verwalten eines Kunden**|Wenn Ihre Benutzer administrativen Zugriff für die Unternehmen haben, denen Sie Support anbieten, können Sie im Kundenportal [Verwalten eines Kunden als delegierter Administrator](../Topic/Help_for_Microsoft_Intune_Partners.md#BKMK_Administer).|
Sie verwenden weiterhin das [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Kontoportal und die Verwaltungskonsole für die Verwaltung Ihres eigenen Abonnements inklusive Geräte und Benutzer. Weitere Informationen zur Verwaltung von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] finden Sie unter [Dokumentation zu Microsoft Intune](../Topic/Documentation_for_Microsoft_Intune.md).

## <a name="BKMK_FindCustomers"></a>Suchen und Unterstützen von Kunden
Mit dem Partnerportal können Sie Kunden identifizieren, denen Sie helfen können. Nachdem Sie einen Kunden gefunden haben, können Sie die folgenden Dienste oder Hilfeleistungen anbieten:

-   Anbieten von kostenpflichtigen und Probeabonnements

-   Verwalten von Kunden, die delegierte Administration akzeptiert haben

-   Erstellen und übermitteln von Serviceanfragen

-   Zurücksetzen von Benutzerkennwörtern

Sie können im Partnerportal über Benutzer- und Domänennamen nach Kunden suchen. Wenn Sie bereits delegierter Administrator für einen Kunden sind, können Sie nach jedem beliebigen Domänennamen suchen, der dem entsprechenden Konto zugeordnet ist.

#### Suchen und Unterstützen von Kunden

1.  Klicken Sie auf der Seite **Partnerübersicht** im [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Partnerportal auf **Nach Benutzer oder Domäne suchen**.

2.  Geben Sie auf der Seite **Nach Benutzer oder Domäne suchen** den kompletten Benutzernamen (person@contoso.com) oder den Domänennamen (contoso.com) ein, nach dem Sie suchen möchten. Der Name muss exakt übereinstimmen. Platzhalter werden nicht unterstützt. Klicken Sie auf **Weiter**, um die Suche zu starten.

3.  Wenn eine Übereinstimmung gefunden wird, wird oben auf der Seite eine Ergebnisseite mit Informationen über das Kundenkonto und Aktionslinks angezeigt. Klicken Sie auf den Link für die gewünschte Aktion.

    |Aktion|Details|
    |----------|-----------|
    |**Verwalten im Namen von**|Nur verfügbar, wenn der Kunde Sie als delegierter Administrator akzeptiert hat.<br /><br />Dieser Link öffnet ein [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Kontoportal für das Abonnement des Kunden.<br /><br />-   Bestätigen Sie das angezeigte Abonnement, indem Sie den Firmennamen prüfen, der oben im linken Bereich angezeigt wird.<br />-   Wenn Ihre Partner-Anmeldeinformationen für **Eingeschränkte Verwaltung** konfiguriert sind, haben Sie keinen Zugriff auf die Knoten **Verwalten**, **Kaufen** oder **Domäne** im Abonnement Ihres Kunden.<br />-   Wenn Sie auf einen Link zu einer verfügbaren Konsole klicken, z. B. auf das Unternehmensportal oder die Verwaltungskonsole, werden Sie zur jeweiligen Konsole für Ihr Unternehmen umgeleitet, und nicht zur Konsole für den Kunden.|
    |**Serviceanfrage erstellen**|Öffnet eine Serviceanfrage im Auftrag des Kunden.|
    |**Alle Administratoren anzeigen**|Zeigt eine Liste aller Mandantenadministratoren für das Unternehmen des Kunden an.|
    |**Kennwort zurücksetzen**|Setzt das Kennwort für das [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Benutzerkonto des Kunden zurück.<br /><br />-   Wenn Sie globaler Administrator sind, können Sie Kennwörter im Partnerportal zurücksetzen.<br />-   Wenn Sie eingeschränkter Administrator sind, können Sie Kennwörter nur im Kontoportal des Kunden zurücksetzen.|

## <a name="BKMK_CreateTrials"></a>Erstellen von Kaufangeboten und Einladungen zum Testen
In einer Einladung zum Testen kann jeweils nur ein Testabonnement angeboten werden.

Kaufangebote können ein oder mehrere Abonnements enthalten, sodass Sie mehrere Abonnements in ein einziges Angebot zusammenfassen können.

**Testversionen und Angebote haben die folgenden Gemeinsamkeiten:**

-   Wenn Sie eine Testeinladung oder ein Angebot erstellen, generiert [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] eine Nachricht mit den Details. Anschließend können Sie diese Nachricht anpassen und an Ihren Kunden senden.

-   Nach dem Anpassen der Nachricht können Sie auf **In E-Mail öffnen** klicken, um automatisch eine E-Mail-Nachricht mit den Nachrichtendetails zu erstellen. Sie können die Nachricht auch manuell kopieren und in ein anderes Kommunikationsformat einfügen.

-   Die Nachrichtendetails enthalten einen Link mit einem eingebetteten Code, mit dem Ihr Unternehmen als Abonnementberater für die angegebenen Dienste identifiziert wird.

-   Sie können dieselbe Nachricht für mehrere Kunden verwenden. Testeinladung oder Kaufangebot enthalten keine kundenspezifischen Daten.

-   Wenn ein Kunde auf den Link in den Nachrichtendetails klickt, wird die jeweilige Testeinladung bzw. das Kaufangebot mit den von Ihnen angegebenen Details angezeigt.

-   Kunden können die Testeinladung bzw. das Kaufangebot akzeptieren, ohne ein Angebot für delegierte Administration zu akzeptieren.

Wenn ein Kunde ein Angebot aus dem Link in der Nachricht akzeptiert, wird er zu einer Standard-Anmeldeseite umgeleitet, um den Test bzw. Kauf des Dienstes vorzunehmen. Die Anmeldeseite enthält einen eingebetteten Code, der Ihr Unternehmen als Abonnementberater identifiziert.

**Berücksichtigen Sie beim Anpassen Ihrer Nachricht Folgendes:**

-   Geben Sie Ihre Identität als ein von Microsoft autorisierter Partner an.

-   Teilen Sie Kunden mit, dass die Rechnung direkt von Microsoft gestellt wird.

-   Informieren Sie Kunden darüber, wie Sie bei Fragen zum Dienst oder zum Angebot kontaktiert werden können.

-   Die Kunden steuern die Anzahl erworbener Benutzerlizenzen. Sie können beim Akzeptieren des Angebots die Anzahl von Lizenzen ändern.

-   Wenn Sie die delegierte Administration anbieten, erläutern Sie, worum es sich dabei handelt und welche Verantwortlichkeiten Sie dabei übernehmen.

#### Erstellen und Verschicken von Kaufangeboten und Testeinladungen

1.  Klicken Sie auf der Seite **Partnerübersicht** im [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Partnerportal auf **Einladungen zur Testversion senden** oder auf **Kaufangebote erstellen**.

2.  Konfigurieren Sie im Assistenten die verfügbaren Optionen:

    -   **Partnerniederlassung**: Wenn Ihr Unternehmen mehrere Niederlassungen umfasst, wählen Sie die Niederlassung aus, die Sie dieser Einladung zum Testen zuordnen möchten. Falls Ihr Standort nicht aufgeführt ist, können Sie neue Standorte auf der [Microsoft Partner Networks](http://go.microsoft.com/fwlink/?linkid=235720)-Webseite hinzufügen. Neue Einträge werden erst bis zu 24 Stunden nach der Erstellung in der Liste **Partnerniederlassung** angezeigt.

    -   **Verwendungsstandort**: Wählen Sie den Standort aus, an dem der Kunde die Dienste verwenden wird.

    -   **Testabonnements** (für Testeinladungen), oder **Abonnements** (für Kaufangebote): Die Liste der verfügbaren Abonnements wird durch den Verwendungsstandort des Kunden (Land oder Region) bestimmt.

        Für Kaufangebote werden Sie nach der Auswahl eines Abonnements aufgefordert, die Anzahl der Benutzerlizenzen einzugeben.

    -   **Delegierte Administration**: Wählen Sie diese Option aus, wenn Sie dem Kunden die delegierte Administration anbieten möchten. Kunden können Testeinladungen mit oder ohne delegierte Administration annehmen.

3.  Wenn Sie fertig sind, klicken Sie auf **In E-Mail öffnen**, um eine neue E-Mail zu öffnen, die den Link zur Einladung enthält. Alternativ können Sie den Link manuell kopieren, in ein Nachrichtenformat Ihrer Wahl einfügen und anschließend an Ihren Kunden senden.

    -   Wenn Benutzerkontensteuerung (User Account Control, UAC) auf Ihrem Computer aktiviert ist und Sie auf **In E-Mail öffnen** klicken, wird neben der E-Mail-Nachricht möglicherweise eine leere Webseite geöffnet.

    -   Notieren Sie sich die **Angebots-ID**. Diese können Sie verwenden, um das Angebot im Microsoft Online Services Partner Commerce Dashboard zu verfolgen.

## <a name="BKMK_OfferAdmin"></a>Anbieten delegierter Administration
Als autorisierter Microsoft-Partner können Sie delegierte Administration anbieten. Mit dieser Funktion können Sie das Abonnement einer Firma in deren Namen verwalten.

Delegierte Administratoren:

-   **Sind Mandantenadministratoren**, die im Kontoportal einfache Aufgaben ausführen können, wie z. B. Benutzer hinzufügen oder Kennwörter für den Kunden zurücksetzen, oder technischere Aufgaben wie z. B. Domänen zum Konto des Kunden hinzufügen.

-   **Sind keine Dienstadministratoren** und haben daher keinen Zugriff auf alltägliche Operationen für den Kunden, wie z. B. Softwarebereitstellung gemäß der Konfiguration in der Verwaltungskonsole.

Bevor Sie das Abonnement eines Kunden verwalten können, muss der [Verwalten von Partnerbeziehungen](../Topic/Maintain_Microsoft_Intune.md#BKMK_ManagePartners). Um die Genehmigung des Kunden zu erhalten, können Sie dem Kunden zuerst ein Angebot für die delegierte Administration schicken, das dieser annehmen kann. Kunden können die Testeinladung bzw. das Kaufangebot akzeptieren, ohne Ihr Angebot für delegierte Administration zu akzeptieren.

-   Sie können die delegierte Administration anbieten, wenn Sie Testeinladungen bzw. Kaufangebote erstellen. So können Sie von Anfang an eine starke Beziehung mit dem Kunden aufbauen.

-   Sie können einem Kunden delegierte Administration anbieten, der zuvor ein Abonnement erworben hat.

Nachdem ein Kunde Ihr Angebot angenommen hat und Ihre Partner-ID als delegierter Administrator konfiguriert hat, können Benutzer aus Ihrem Unternehmen, die Zugriffsberechtigungen für die Firma des Kunden haben, als delegierte Administratoren fungieren.

#### Anbieten der delegierten Administration für ein bestehendes Konto

1.  Klicken Sie auf der Seite **Partnerübersicht** im [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Partnerportal auf **Angebote für die delegierte Administration senden**.

2.  Klicken Sie auf **In E-Mail öffnen**, oder kopieren Sie den Link für das Angebot, und fügen Sie diesen manuell in eine E-Mail ein.

3.  Wenn der Kunde Ihr Angebot mit dem Link erhält, kann er diesem Link folgen, um Sie als delegierten Administrator zu autorisieren.

Sie können die delegierte Administration auch anbieten, wenn Sie ein Testabonnement oder Kaufangebot erstellen oder indem Sie **Autorisierung für die delegierte Administration einschließen** unter den Optionen für den Test bzw. das Angebot auswählen.

## <a name="BKMK_AssignDelAdmin"></a>Vergabe von Benutzerberechtigungen für delegierte Administration
Im [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Kontoportal Ihres Abonnements können Sie für Ihre Benutzer administrativen Zugriff für die Firmen vergeben, denen Sie Support anbieten:

-   Sie können diese nur für Partner verfügbare Konfiguration vornehmen, wenn Sie neue Benutzerkonten erstellen oder wenn Sie bestehende Benutzerkonten bearbeiten.

-   Benutzer müssen keine Administratoren in Ihrem Unternehmen sein, um administrativen Zugriff auf Firmen erhalten zu können, denen Sie Support anbieten.

Delegierte Administratoren haben die folgenden Berechtigungen:

-   Zugriff auf Ihr Partnerportal

-   Suche nach Benutzern und Domänen von Kunden

-   Erstellen von Kaufangeboten und Testeinladungen und anbieten der delegierten Administration an Kunden

-   Verwalten von Kundenabonnements basierend auf der Rolle, die dem Benutzerkonto zugewiesen ist

Weitere Informationen zum Konfigurieren von Administratoren finden Sie unter [Task 5: Assign administrative users](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md#BKMK_AssignAdmins). Informationen zu Administratorrollen und -Berechtigungen finden Sie unter [Zuweisen von Administratorrollen](http://technet.microsoft.com/library/hh967622).

#### Konfigurieren eines Benutzers als delegierter Administrator

1.  Klicken Sie im [Microsoft Intune-Kontenportal](https://account.manage.microsoft.com/) für Ihr Unternehmen auf **Benutzer**.

2.  Wählen Sie das Benutzerkonto aus, das Sie konfigurieren möchten, und klicken Sie auf **Bearbeiten**.

3.  Klicken Sie auf der Registerkarte Einstellungen unter **Administratorzugriff auf von Ihnen unterstützte Unternehmen zuweisen** auf **Ja** und wählen Sie dann die passende Rolle für dieses Konto aus:

    -   **Vollständige Verwaltung**: Verleiht dem Benutzer Berechtigungen äquivalent zur globalen Administratorrolle für die von Ihnen unterstützten Unternehmen.

    -   **Eingeschränkte Verwaltung**: Verleiht dem Benutzer Berechtigungen äquivalent zur Kennwortadministratorrolle für die von Ihnen unterstützten Unternehmen.

4.  Klicken Sie auf **Speichern**, um den Vorgang abzuschließen.

Berechtigungen als delegierter Administrator gelten nur für die Verwaltung eines Kundenabonnements. Benutzer mit diesen Berechtigungen erhalten keine Mandantenadministrator- oder Dienstadministratorberechtigungen für Ihr Firmenabonnement.

## <a name="BKMK_Administer"></a>Verwalten eines Kunden als delegierter Administrator
Nachdem Ihr Kunde Ihre Partner-ID als delegierter Administrator konfiguriert hat, können Ihre als delegierte Administratoren konfigurierten Benutzer das Abonnement des Kunden verwalten.

**Für die Verwaltung des Abonnements Ihres Kunden gilt Folgendes:**

-   Sie können nur auf das Kontoportal Ihres Kunden zugreifen

-   Wenn Sie das Kontoportal Ihres Kunden verlassen, wird die Administrationssitzung für diesen Kunden beendet

-   Wenn Sie auf die "Zurück"-Schaltfläche im Browser klicken, um zum Portal des Kunden zurückzukehren, werden Sie stattdessen auf das Kontoportal für Ihr eigenes Abonnement umgeleitet

-   Um zum Kontoportal für den Kunden zurückzukehren, müssen Sie sich bei Ihrem Partnerportal anmelden, nachdem Kunden suchen und diesen anschließend verwalten

#### Verwalten eines Kunden

1.  Melden Sie sich beim Partnerportal Ihres Unternehmens an.

2.  Klicken Sie in der Seite **Partnerübersicht** auf **Nach Benutzer oder Domäne suchen** und suchen Sie nach dem Abonnement des Kunden, den Sie verwalten möchten.

3.  Wenn Sie den Kunden gefunden haben, klicken Sie auf **Verwalten im Namen von**.

Wenn das [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Portal geöffnet wird, sollten Sie anhand des Firmennamens in der oberen linken Ecke im linken Bereich sicherstellen, dass Sie mit dem richtigen Kunden arbeiten. Anschließend können Sie die entsprechenden Verwaltungsaufgaben ausführen.

