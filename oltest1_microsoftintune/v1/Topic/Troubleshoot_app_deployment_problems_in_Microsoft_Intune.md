---
description: na
keywords: na
title: Troubleshoot app deployment problems in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 28ac298e-fb73-4c1c-b3fd-8336639e05e6
---
# Behandlung von Problemen mit der App-Bereitstellung in Microsoft Intune
Dieses Thema enthält Ressourcen, die Ihnen bei der Behebung von Problemen bei der Bereitstellung von Apps mit [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] behilflich sind.

## <a name="BKMK_TypicalProblems"></a>Hilfe bei üblichen Problemen bei der App-Bereitstellung

#### Sie können sich nicht beim [!INCLUDE[wit_iwportal_1](../Token/wit_iwportal_1_md.md)] anmelden

1.  Überprüfen Sie, ob Ihr Konto im [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] vorhanden ist oder ob es deaktiviert ist.

2.  Stellen Sie sicher, dass Ihnen dieses Konto im [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] bereitgestellt wurde.

3.  Stellen Sie im [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] sicher, dass Sie zum Anmelden bei [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] den richtigen Benutzernamen und das richtige Kennwort verwenden und dass der Benutzername das Format **joe@domain.com** aufweist.

#### Im Unternehmensportal fehlen die Kontaktinformationen der IT-Abteilung

1.  Klicken Sie in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] auf **Admin** &gt; **Unternehmensportal**.

2.  Legen Sie die Details unter **An IT-Abteilung wenden** fest.

#### In der Liste werden bestimmte Apps nicht angezeigt

1.  Stellen Sie sicher, dass Sie die App-Liste für einen Benutzer oder ein Gerät prüfen, auf dem die App bereitgestellt wurde.

2.  Stellen Sie sicher, dass das Gerät die entsprechenden Geräteanforderungen erfüllt.

#### Beim Herunterladen einer App erhalten Sie eine Fehlermeldung

1.  Stellen Sie sicher, dass nicht zu viele gleichzeitige Downloads pro Benutzer stattfinden. Jeder Benutzer kann gleichzeitig eine einzelne App herunterladen.

2.  Stellen Sie sicher, dass nicht zu viele gleichzeitige Downloads pro Konto stattfinden. Warten Sie einige Minuten, und versuchen Sie es erneut.

3.  Wenn Sie eine Meldung von iOS erhalten, dass die Installation nicht möglich ist oder abgebrochen wurde oder Sie den Vorgang wiederholen müssen, liegt möglicherweise vorübergehend eine starke Auslastung vor. Warten Sie einige Minuten, und versuchen Sie es erneut.

4.  Wenn die Statusanzeige für das Herunterladen von Apps in iOS vollständig ist, aber die App nicht ordnungsgemäß installiert wird, liegt möglicherweise ein Fehler bei den bereitgestellten App-Dateien vor.

#### Wenn Sie auf einen Link zu einer iOS-App klicken, gelangen Sie zu einem früheren Ort im iTunes App Store.

1.  Von der aktuellen iTunes App Store-Sitzung wird die vorherige App-Seite geöffnet.

2.  Schließen Sie den iTunes App Store auf dem Gerät, und folgen Sie den Link erneut.

#### Beim Starten einer iOS-App erhalten Sie eine Fehlermeldung

1.  Das Ablaufdatum der App ist möglicherweise nicht gültig.

#### Der Upload Ihrer App bleibt im Zustand "Läuft" stehen

1.  Wenn eine App hochgeladen wird, werden zunächst die Metadaten und dann das App-Paket hinzugefügt. Nach dem Hochladen der Metadaten läuft die App scheinbar. Wenn Sie feststellen, dass der Upload Ihrer App ungewöhnlich lange im Zustand "Läuft" verbleibt, löschen Sie die App, und laden Sie sie erneut hoch.

2.  Achten Sie darauf, die Bereitstellung der App nicht zu verwalten, solange sie sich im Zustand „Läuft“ befindet.

#### Bei der Installation einer iOS-App tritt ein Fehler auf

1.  Stellen Sie sicher, dass der Zugriff auf die Apple-Bereitstellungs- und -Zertifizierungswebsites durch die Firewall Ihrer Organisation zugelassen wird.

2.  Weitere Informationen finden Sie in der Apple-Entwicklerdokumentation.

#### Wenn der Installationsstatus von verwalteten Anwendungen nicht gemeldet wird

-   Bei verwalteten App-Installationen wurden vor dem Microsoft Intune-Dienstupdate im November 2014 keine Informationen zum Installationsstatus erfasst. Bei Geräten, auf denen vor diesem Dienstupdate verwaltete Apps installiert wurden, muss jede App-Bereitstellung mit der geeigneten Bereitstellungsaktion aktualisiert werden (z. B. **Verfügbare Installation**). Jedes Gerät wird die App während die automatische Prüfung auf verfügbare Apps aktualisieren. Weitere Informationen finden Sie unter [Aktualisieren von Apps mit Microsoft Intune](../Topic/Update_apps_using_Microsoft_Intune.md).

## <a name="BKMK_SoftDistErrorCodes"></a>Fehlercodes von App-Bereitstellungsfehlern
Die folgende Tabelle enthält eine Übersicht über Fehler, die bei der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-App-Bereitstellung häufig auftreten, die wahrscheinlichen Fehlerursachen und mögliche Lösungen.

|Fehlercode|Mögliches Problem|Lösungsvorschlag|
|--------------|---------------------|--------------------|
|0x80073CFF<br /><br />0x80CF201C (Clientfehler)|Zur Installation der Anwendung müssen Sie über ein zum Querladen fähiges System verfügen.|Stellen Sie sicher, dass das App-Paket mit einer vertrauenswürdigen Signatur signiert und auf auf einem zur Domäne gehörenden Gerät mit aktivierter Richtlinie "AllowAllTrustedApps" oder auf einem Gerät mit Windows Sideloading-Lizenz und aktivierter Richtlinie "AllowAllTrustedApps" (wird bei Registrierung eines Windows RT-Geräts angewendet) installiert ist.|
|0x80073CF0|Das Paket konnte nicht geöffnet werden.|Mögliche Ursachen:<br /><br />-   Das Paket ist nicht signiert.<br />-   Der Namen des Herausgebers stimmt nicht mit dem Signaturzertifikat des Antragstellers überein.<br /><br />Prüfen Sie das Ereignisprotokoll „AppxPackagingOM“, um weitere Informationen zu erhalten.|
|0x80073CF3|Fehler bei Updates des Pakets (Abhängigkeits- oder Konfliktüberprüfung)|Mögliche Ursachen:<br /><br />-   Das eingehende Paket ist mit einem installierten Paket nicht vereinbar.<br />-   Eine angegebene Paketabhängigkeit wurde nicht gefunden.<br />-   Das Paket unterstützt nicht die richtige Prozessorarchitektur.<br /><br />Prüfen Sie das Ereignisprotokoll „AppXDeployment-Server“, um weitere Informationen zu erhalten.|
|0x80073CFB|Das bereitgestellte Paket ist bereits installiert, und eine erneute Installation des Pakets wird blockiert.|Dieser Fehler kann auftreten, wenn Sie ein Paket installieren, das nicht bitweise mit dem bereits installierten Paket identisch ist. Überprüfen Sie, ob die digitale Signatur auch Teil des Pakets ist. Wenn ein Paket erneut erstellt oder signiert wird, ist das Paket nicht mehr bitweise identisch mit dem zuvor installierten Paket. Es gibt zwei Möglichkeiten, diesen Fehler zu beheben:<br /><br />-   Erhöhen Sie die Versionsnummer der Anwendung, und erstellen und signieren Sie das Paket dann erneut.<br />-   Entfernen Sie das alte Paket für jeden Benutzer des Systems, bevor Sie das neue Paket installieren.|

## Siehe auch
[Problembehandlung bei Microsoft Intune](../Topic/Troubleshoot_Microsoft_Intune.md)
[Bereitstellen und Konfigurieren von Apps mit Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)

