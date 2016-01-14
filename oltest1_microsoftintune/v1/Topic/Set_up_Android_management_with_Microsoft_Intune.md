---
description: na
keywords: na
title: Set up Android management with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dbe5cad1-3e0d-41a9-966b-738156089700
---
# Einrichten der Android-Verwaltung mit Microsoft Intune
Mobile Android-Geräte ermöglichen Benutzern die Registrierung über die Unternehmensportal-App, die in Google Play zur Verfügung steht. Führen Sie die folgenden Schritte aus, um Ihren Benutzern die Registrierung ihrer Geräte in [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zu ermöglichen.

## Einrichten von mobilen Android-Geräten mit Microsoft Intune

1.  **Einrichten von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]**
    Wenn nicht bereits geschehen,  bereiten Sie die Verwaltung mobiler Geräte vor, indem Sie die [Autorität für die Verwaltung mobiler Geräte](https://technet.microsoft.com/library/mt346013.aspx) auf **Microsoft Intune** festlegen.

2.  **Hinzufügen von Intune-Benutzern** 
    Der Eigentümer des mobilen Geräts muss dem Kontoportal hinzugefügt werden, bevor Geräte registriert werden können. Melden Sie sich beim [Microsoft Intune-Kontoportal](http://go.microsoft.com/fwlink/?LinkId=698854) an, klicken Sie auf **Benutzer hinzufügen**, und wählen Sie eine Option aus:

    -   **Benutzer**: Zum Hinzufügen eines einzelnen Benutzers wählen Sie **Neu** &gt; **Benutzer** und geben in den Feldern **Details**, **Rollen zuweisen** und  **Benutzerstandort einstellen** Informationen an. Weisen Sie den Benutzer anschließend einer **Gruppe** zu.

    -   **Per Massenvorgang hinzufügen**: Erstellen Sie eine CSV-Datei (siehe bereitgestellte Beispieldateien), und importieren Sie diese ins Kontoportal. Geben Sie Rollen, den Speicherort und die Gruppe an, und erstellen Sie anschließend die Konten. Beispieldateien und leere CSV-Dateien können vom Kontoportal heruntergeladen werden.

    Sie können auch die Active Directory- oder Azure Active Directory-Synchronisierung aktivieren. Weitere Informationen zur Integration anderer Azure Active Directory-Benutzer in Intune finden Sie unter [Fahrplan zur Verzeichnissynchronisierung](http://go.microsoft.com/fwlink/?LinkId=511540), oder klicken Sie auf **Andere Möglichkeiten zum Hinzufügen von Benutzern** im Kontoportal.

3.  **Erstellen von Gruppen**  (optional)
    Gruppen bieten Flexibilität für die Verwaltung von Geräten und Benutzern. Sie können die Gruppen so einrichten, wie es Ihren organisatorischen Anforderungen am besten entspricht, beispielsweise nach geografischem Standort, Abteilung oder Hardwareeigenschaften.   Weitere Informationen finden Sie unter [Verwenden von Gruppen zum Verwalten von Benutzern und Geräten in Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

4.  **Hinzufügen von Richtlinien für Geräte** (optional)
    Richtlinien sind Gruppen von Einstellungen zum Steuern der Features auf Geräten. Die meisten MDM-Richtlinien sind plattformspezifisch. Sie erstellen Richtlinien mithilfe von Vorlagen, in denen empfohlene oder angepasste Einstellungen enthalten sind, und stellen diese dann für Gruppen bereit. Weitere Informationen finden Sie unter [Verwenden von Richtlinien zum Verwalten von Computern und mobilen Geräten mit Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

5.  **Festlegen der Beschränkung für Registrierungen für das Gerät** (optional) 
    Um die Anzahl von mobilen Geräten zu beschränken, die ein Benutzer registrieren kann, melden Sie sich bei der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) an, klicken Sie auf **Verwaltung** &gt; **Verwaltung mobiler Geräte** &gt; **Registrierungsregeln**. Wählen Sie die maximale Anzahl der Geräte aus, die ein Benutzer registrieren kann, und klicken Sie dann auf **Speichern**.

6.  **Festlegen von Unternehmensportaleinstellungen** 
     Sie können das Intune-Unternehmensportal für Ihr Unternehmen anpassen. Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) auf **Verwaltung** &gt; **Unternehmensportal**. Konfigurieren Sie Folgendes

    -   **Firmenname**

    -   **Kontaktname für IT-Abteilung**

    -   **Telefonnummer der IT-Abteilung**

    -   **Weitere Informationen**

    -   **URL der Datenschutzrichtlinie des Unternehmens**

    -   **URL der Supportwebsite (nicht angezeigt)**

    -   **Websitename**

7.  [!INCLUDE[CPEnrollmentTermsAndConditions](../Token/CPEnrollmentTermsAndConditions_md.md)]

8.  **Erläutern des Zugriffs auf Unternehmensressourcen über das Unternehmensportal**
    Ihre Benutzer müssen wissen, wie sie ihre Geräte registrieren können und was sie erwartet, wenn die Geräte in die Verwaltung eingebunden sind.[Informieren der Endbenutzer über den Einsatz von Microsoft Intune](../Topic/What_to_tell_your_end_users_about_using_Microsoft_Intune.md)

## Siehe auch
[Vorbereiten der Registrierung von Geräten in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

