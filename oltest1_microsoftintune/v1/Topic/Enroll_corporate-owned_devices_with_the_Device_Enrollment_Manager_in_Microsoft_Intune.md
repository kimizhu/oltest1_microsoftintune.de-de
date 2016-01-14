---
description: na
keywords: na
title: Enroll corporate-owned devices with the Device Enrollment Manager in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a23abc61-69ed-44f1-9b71-b86aefc6ba03
---
# Registrieren von firmeneigenen Ger&#228;ten mit dem Ger&#228;teregistrierungs-Manager in Microsoft Intune
Mit Intune können Organisationen eine Vielzahl mobiler Geräte mit einem einzelnen Benutzerkonto verwalten. Das Konto *Geräteregistrierungs-Manager* ist ein spezielles Intune-Konto mit Berechtigung zum Registrieren von mehr als fünf Geräten. Sie können beispielsweise einem Speicher-Manager oder Supervisor ein Benutzerkonto für einen Geräteregistrierungs-Manager zuweisen, um ihm folgende Möglichkeiten zu geben:

-   Registrieren von Geräten in Intune

-   Anmelden beim Unternehmensportal, um Unternehmens-Apps abzurufen

-   Installieren und Deinstallieren von Software

-   Konfigurieren des Zugriffs auf Unternehmensdaten

Der Speicher-Manager kann das Gerät nicht über das Unternehmensportal zurücksetzen.

**Beispiele für ein Geräteregistrierungs-Manager-Szenario:**
 Ein Restaurant wünscht Point-of-Sale-Tablets für sein Bedienpersonal und die Bestellmonitore für seine Küchenmitarbeiter. Die Mitarbeiter müssen niemals auf Unternehmensdaten zugreifen und sich nie als Benutzer anmelden. Der Intune-Administrator erstellt ein Konto für den Geräteregistrierungs-Manager und registriert die firmeneigenen Geräte mit diesem Konto. Alternativ kann der Administrator die Anmeldeinformationen des Geräteregistrierungs-Managers einem Restaurant-Manager geben, sodass dieser die Geräte registrieren und verwalten kann.

Der Administrator oder Manager kann rollenspezifische Apps auf den Restaurantgeräten bereitstellen. Ein Administrator kann das Gerät auch in der Intune-Konsole auswählen und es über die Verwaltungskonsole aus der Verwaltung mobiler Geräte entfernen.

## Konten für Geräteregistrierungs-Manager in Intune
Konten für Geräteregistrierungs-Manager sind Benutzerkonten mit der Berechtigung, eine große Anzahl firmeneigener Geräten anzumelden. Nur Benutzer in der Intune-Konsole können Geräteregistrierungs-Manager sein.

#### Hinzufügen eines Geräteregistrierungs-Managers zu Intune

1.  Navigieren Sie zum [Microsoft Intune-Kontenportal](http://go.microsoft.com/fwlink/p/?LinkID=329938), und melden Sie sich bei Ihrem Administratorkonto an.

2.  Klicken Sie auf **Benutzer hinzufügen**.

3.  Vergewissern Sie sich, dass das Benutzerkonto aufgeführt wird, das ein Geräteregistrierungs-Manager werden soll. Ist dies nicht der Fall, fügen Sie den Benutzer hinzu, indem Sie auf **Neu** klicken und den Prozess zum Hinzufügen eines Benutzers ausführen. Weitere Informationen zum Hinzufügen von Benutzern finden Sie unter [Task 3: Add users and assign licenses for your subscription](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md#Anchor_3). Eine Abonnementlizenz ist für jeden Benutzer erforderlich, der auf den Dienst zugreift und der *Geräteregistrierungs-Manager* kann kein Intune-Administrator sein. Stellen Sie fest, ob Sie weitere Lizenzen benötigen, bevor Sie diese Funktion verwenden.

4.  Melden Sie sich bei der [Microsoft Intune-Verwaltungskonsole](http://manage.microsoft.com) mit Ihren Administratoranmeldedaten an.

5.  Klicken Sie im Navigationsbereich auf **Admin**, gehen Sie zu **Administratorverwaltung**, und wählen Sie **Geräteregistrierungs-Manager**. Die Seite "Geräteregistrierungs-Manager" wird geöffnet.

6.  Klicken Sie auf **Hinzufügen…**. Das Dialogfeld **Geräteregistrierungs-Manager hinzufügen** wird geöffnet.

7.  Geben Sie die **Benutzer-ID** des Intune-Kontos ein, und klicken Sie auf **OK**. Der Geräteregistrierungs-Manager kann kein Intune-Administrator sein.

8.  Der Geräteregistrierungs-Manager kann nun Mobilgeräte über das Verfahren registrieren, das ein Endbenutzer für ein BYOD-Szenario im Unternehmensportal verwendet. Informationen zum Registrieren von Geräten über das Unternehmensportal finden Sie unter [Aktivieren der Registrierung mobiler Geräte über das Microsoft Intune-Kontoportal](../Topic/Enable_mobile_device_enrollment_with_the_Microsoft_Intune_Account_Portal.md).

#### Löschen eines Geräteregistrierungs-Managers aus Intune

1.  Melden Sie sich beim [Microsoft Intune-Kontoportal](http://manage.microsoft.com) mit Ihren Administratoranmeldedaten an.

2.  Klicken Sie im Navigationsbereich auf **Admin**, gehen Sie zu **Administratorverwaltung**, und wählen Sie **Geräteregistrierungs-Manager**. Die Seite "Geräteregistrierungs-Manager" wird geöffnet.

3.  Wählen Sie den Registrierungs-Manager-**Benutzer** aus, den Sie löschen möchten, und klicken Sie dann auf **Löschen**. Dieser Benutzer wird nicht aus Intune gelöscht, und die Geräte, die diese Benutzer verwaltet, bleiben in Intune angemeldet. Durch das Löschen eines Geräteregistrierungs-Manager wird verhindert, dass der Benutzer mehr Geräte in Intune registrieren kann.

4.  Klicken Sie auf **Ja**, um das Löschen des Geräteregistrierungs-Managers zu bestätigen.

Wenn Sie einen Geräteregistrierungs-Manager löschen, wirkt sich dies nicht auf registrierte Geräte aus. Wenn ein Geräteregistrierungs-Manager gelöscht wird:

-   sind keine registrierten Geräte betroffen

-   werden registrierte Geräte weiterhin vollständig verwaltet

-   bleiben die gelöschten Kontoanmeldedaten für den Geräteregistrierungs-Manager für die Anmeldung beim Unternehmensportal zum Zugriff auf Apps gültig

-   können über die Kontoanmeldedaten für den Geräteregistrierungs-Manager weiterhin keine Geräte zurückgesetzt oder deaktiviert werden

-   bleibt die Beziehung des gelöschten Geräteregistrierungs-Manager-Kontos zu registrierten Geräten bestehen, es können jedoch keine zusätzlichen Geräte registriert werden.

## Siehe auch
[Erste Schritte mit einem kostenpflichtigen Abonnement in Microsoft Intune](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md)
[Vorbereiten der Registrierung von Geräten in Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)
[Aktivieren der Registrierung mobiler Geräte über das Microsoft Intune-Kontoportal](../Topic/Enable_mobile_device_enrollment_with_the_Microsoft_Intune_Account_Portal.md)

