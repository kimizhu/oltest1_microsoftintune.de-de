---
description: na
keywords: na
title: Control what admins can see in the Microsoft Intune admin console
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e0783eaa-67dc-410e-9e80-4d3aa72f36d8
---
# Kontrollieren, was Administratoren in der Microsoft Intune-Verwaltungskonsole anzeigen k&#246;nnen
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] bietet die Möglichkeit, die Verwaltungskonsolenansicht zu filtern, sodass Benutzer nur auf die Elemente Zugriff haben, die sie sehen sollen. Beispielsweise empfiehlt es sich, nur den Operatoren der Verwaltungskonsole die Erlaubnis zu erteilen, Malwaredefinitionen zu aktualisieren oder die Kennung auf Geräten zurückzusetzen. Dies erfolgt mithilfe der vorab festgelegten **Bezeichnungen**, die Sie bestimmten Benutzern zuweisen. Wenn diese Benutzer auf die Verwaltungskonsole zugreifen, sehen sie nur die für ihre Bezeichnung bestimmten Elemente.

Mit dieser Funktion können Sie Mitarbeitern Verwaltungsaufgaben zuweisen, und gleichzeitig die Sicherheit der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Daten gewährleisten.

## Zuweisen einer Bezeichnung zu einem Benutzer

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com) auf **Verwaltung** &gt; **Dienstadministratoren**.

2.  Wählen Sie aus der Liste der Dienstadministratoren den Benutzer, dessen Bezeichnung Sie ändern möchten, und klicken Sie dann auf **Zugriff verwalten**.

3.  Wählen Sie im Dialogfeld **Zugriff verwalten** die Zugriffsebene, die dem ausgewählten Benutzer zugewiesen werden soll. Es gibt folgende Auswahlmöglichkeiten:

    -   **Vollzugriff**

    -   **Schreibgeschützter Zugriff**

    Darüber hinaus können Sie eine der folgenden Bezeichnungen wählen, die benutzerdefinierte Zugriffsebenen für die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungskonsole bieten:

    |Bezeichnung|Der Benutzer kann:|
    |---------------|----------------------|
    |**Helpdesk – Gruppenknoten**|<ul><li>Listen von Benutzern und Geräten anzeigen, ohne die Ansicht jedoch filtern zu können. Sie können jedoch mithilfe der Gruppenfilterung definieren, was der Benutzer sieht. Weitere Informationen finden Sie unter [Verwenden von Gruppen zum Verwalten von Benutzern und Geräten in Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).</li><li>Drucken Sie die Liste der Benutzer und Geräte.</li><li>Exportieren der Liste der Benutzer und Geräte</li><li>Zeigen Sie die Eigenschaften eines Benutzers oder Geräts an.</li><li>Führen Sie die folgenden Remoteaufgaben aus:<br /><br /><ul><li>Vollständige Malwareüberprüfung ausführen</li><li>Malwareschnellüberprüfung ausführen</li><li>Computer neu starten</li><li>Update für Malwaredefinitionen ausführen</li><li>Richtlinien aktualisieren</li><li>Inventur aktualisieren</li><li>Remotesperre für Gerät aktivieren</li><li>Zurücksetzen der Kennung</li></ul></li></ul>|

Wenn der von Ihnen konfigurierte Benutzer das nächste Mal die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungskonsole öffnet, wird ihm die von Ihnen festgelegte Zugriffsebene zugewiesen.

## Siehe auch
[Technische Referenz für Microsoft Intune](../Topic/Technical_reference_for_Microsoft_Intune.md)

