---
description: na
keywords: na
title: Fix issues with mobile device enrollment
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e5979ab-fc4c-4c7b-a60c-15317496dfa2
robots: noindex,nofollow
---
# Fix issues with mobile device enrollment
Wenn Sie Probleme mit Mobilgeräten haben, können Sie Ihrem IT-Administrator Protokolle senden, um ihn bei der Problembehandlung zu unterstützen.

## Android-Geräte
Die Protokolle, die Sie senden, enthalten keine persönlichen Daten, es sei denn, Sie aktivieren "Ausführliche Protokollierung". Die Protokolle enthalten dann Ihre E-Mail-Adresse, aber keine anderen persönlichen Daten. Sie können Protokolle mit einer der folgenden Methoden senden.

> [!IMPORTANT]
> Die ausführliche Protokollierung ist auf Ihrem Gerät standardmäßig aktiviert. Wenn Sie auf Ihrem Gerät die ausführliche Protokollierung aktivieren, enthalten die Protokolle, die Sie ab diesem Punkt senden, solange Ihre E-Mail-Adresse, bis Sie die ausführliche Protokollierung wieder deaktivieren.

### Android-Option 1

1.  Öffnen Sie die Unternehmensportal-App.

2.  Tippen Sie auf **Menü**. Je nach Android-Gerät kann dies eine Schaltfläche in der Software oder Taste auf dem Gerät sein.

3.  Tippen Sie im **Menü** auf **Einstellungen** &gt; **Daten senden**.

Sie werden aufgefordert, eine E-Mail-App auszuwählen. Die App erstellt eine voradressierte E-Mail, an die alle benötigten Protokolle angefügt sind.

### Android-Option 2
Wenn Sie beim Versuch, Ihr Gerät in Intune zu registrieren, eine Fehlermeldung erhalten, können Sie den Vorgang durch Tippen auf **Wiederholen** erneut versuchen oder die Fehlerinformationen in einer E-Mail an Ihren IT-Administrator senden, indem Sie auf **Informationen senden** tippen. Eine an den IT-Administrator adressierte E-Mail wird automatisch erstellt und enthält die Protokolle, die vom Administrator für die Problembehandlung Ihres Geräts benötigt werden.

### Android-Option 3

1.  Verbinden Sie Ihr Gerät mit einem USB-Kabel mit einem Computer.

2.  Suchen Sie auf dem Computer nach einem Verzeichnis mit dem Namen Ihres Mobilgeräts. Suchen Sie in diesem Verzeichnis nach "Android-Gerät&gt;\Phone\Android\data\com.microsoft.windowsintune.companyportal\files\".

3.  Fügen Sie alle Dateien an eine E-Mail-Nachricht an, und senden Sie diese an die IT-Abteilung.

(**Hinweis für Administratoren:** Nennen Sie den Endbenutzern Ihre E-Mail-Adresse.)

## Windows Phone 8.1-Gerät

1.  Installieren Sie über den [Windows Phone Store](http://www.windowsphone.com/en-us/store/app/field-medic/73c58570-d5a7-46f8-b1b2-2a90024fc29c) die App "Field Medic".

2.  Öffnen Sie Field Medic, und tippen Sie auf **Advanced**.

3.  Stellen Sie in **Categories** sicher, dass **Enterprise** aktiviert ist.

4.  Tippen Sie auf die Schaltfläche "Zurück", um zur Startseite von Field Medic zurückzukehren, und tippen Sie auf **Start Logging**.

5.  Öffnen Sie Ihre Telefoneinstellungen, tippen Sie auf **Arbeitsplatz** und dann auf **Registriert**.

6.  Klicken Sie auf dem Bildschirm "Neu" dreimal auf die Schaltfläche **Synchronisieren** .

7.  Kehren Sie zu Field Medic zurück, und tippen Sie auf **Stop Logging**. Benennen Sie das Protokoll, und tippen Sie auf das Symbol **Speichern**.

8.  Verbinden Sie anschließend Ihr Mobilgerät mit einem USB-Kabel mit einem Computer. Öffnen Sie auf dem Computer den Datei-Explorer, und öffnen Sie **&lt;Name des Mobilgeräts&gt;** &gt; **Telefon** &gt; **Dokumente** &gt; **FieldMedic** &gt; **Berichte**.

9. Wählen Sie den neuesten Ordner aus, kopieren Sie ihn, und fügen Sie ihn an eine E-Mail an Ihren IT-Administrator an. Die Ordner sind sequenziell nummeriert (WPB_000_JJJJMMTT_xxxxx ).

(Hinweis für Administratoren: Wenn Sie eine bevorzugte Methode für die Freigabe dieses Ordners haben, z. B. auf OneDrive kopieren, beschreiben Sie sie hier).

## iOS-Geräte

1.  Öffnen Sie das Unternehmensportal.

2.  Bewegen Sie das Gerät, und wählen Sie im Popupfenster "Diagnose" **E-Mail** aus. Eine neue E-Mail wird mit den angefügten Protokollen geöffnet. Senden Sie diese E-Mail an die IT-Abteilung.

> [!TIP]
> Wenn das Gerät nicht reagiert, wenn Sie es bewegen, öffnen Sie **Einstellungen** &gt; **Unternehmensportal**, und stellen Sie sicher, dass die Option **Bewegungsgeste** aktiviert ist.

