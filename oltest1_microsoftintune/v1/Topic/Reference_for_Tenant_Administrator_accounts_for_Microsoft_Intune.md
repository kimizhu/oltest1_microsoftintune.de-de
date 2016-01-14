---
description: na
keywords: na
title: Reference for Tenant Administrator accounts for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e4eff7b9-4dcd-4959-b1d6-97dc4640dbe2
---
# Referenz f&#252;r die Mandantenadministratorkonten f&#252;r Microsoft Intune
Jedem Mandantenadministrator ist eine der folgenden Rollen zugewiesen:

|Rolle|Details|
|---------|-----------|
|**Rechnungsadministrator**|Tätigt Erwerbe, verwaltet Abonnements, verwaltet Supporttickets und überwacht den Dienststatus.|
|**Globaler Administrator**|Hat Zugriff auf alle Administratorfunktionen. Standardmäßig wird die Person, die sich registriert, um einen Microsoft-Cloud-Dienst im Auftrag Ihres Unternehmens zu erwerben, automatisch der erste globale Administrator Ihres Mandanten.<br /><br />-   Nur globale Administratoren können weitere Administratorrollen zuweisen.<br />-   Es kann mehr als einen globalen Administrator in Ihrem Unternehmen geben.|
|**Kennwortadministrator**|Setzt Kennwörter zurück, verwaltet Serviceanfragen und überwacht den Dienststatus. Kennwortadministratoren können Kennwörter ausschließlich für Benutzer und für andere Kennwortadministratoren zurücksetzen.|
|**Dienstunterstützungsadministrator**|Verwaltet Serviceanfragen und überwacht den Dienststatus.|
|**Benutzerverwaltungsadministrator**|Setzt Kennwörter zurück, überwacht den Dienststatus und verwaltet Benutzerkonten, Benutzergruppen und Serviceanfragen.|
Jede Administratorrolle verfügt über die folgenden Berechtigungen:

|Berechtigung|Rechnungsadministrator|Globaler Administrator|Kennwortadministrator|Dienstunterstützungsadministrator|Benutzerverwaltungsadministrator|
|----------------|--------------------------|--------------------------|-------------------------|-------------------------------------|------------------------------------|
|Anzeigen von Organisations- und Benutzerinformationen|Ja|Ja|Ja|Ja|Ja|
|Verwalten von Supporttickets|Ja|Ja|Ja|Ja|Ja|
|Zurücksetzen von Benutzerkennwörtern|Nein|Ja|Ja|Nein|Ja, mit Beschränkungen. Dieser Administrator kann keine Kennwörter für Rechnungsadministratoren, globale Administratoren und Dienstadministratoren zurücksetzen.|
|Durchführen von Vorgängen für Rechnungen und Erwerbe|Ja|Ja|Nein|Nein|Nein|
|Erstellen und Verwalten von Benutzeransichten|Nein|Ja|Nein|Nein|Ja|
|Erstellen, Bearbeiten und Löschen von Benutzern und Gruppen sowie Verwalten von Benutzerlizenzen|Nein|Ja|Nein|Nein|Ja, mit Beschränkungen. Dieser Administrator kann keinen globalen Administrator löschen und keine anderen Administratoren erstellen.|
|Verwalten von Domänen|Nein|Ja|Nein|Nein|Nein|
|Verwalten von Organisationsinformationen|Nein|Ja|Nein|Nein|Nein|
|Delegieren von Administratorrollen an andere Benutzer|Nein|Ja|Nein|Nein|Nein|
|Verwenden der Verzeichnissynchronisierung|Nein|Ja|Nein|Nein|Nein|
Weitere Informationen zu Administratorkonten in [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] erhalten Sie unter [Verschiedene Administratorkonten und Berechtigungen für separate Aufgaben](http://technet.microsoft.com/library/dn646966.aspx). Hilfestellung bei der Verwaltung von Administratoren finden Sie unter [Task 5: Assign administrative users](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md#BKMK_AssignAdmins) in [Erste Schritte mit einem kostenpflichtigen Abonnement in Microsoft Intune](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md).

