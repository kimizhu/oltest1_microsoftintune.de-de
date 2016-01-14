---
description: na
keywords: na
title: Your computer is already enrolled
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d3a40f5-99e9-48dc-9706-f7a3a23e5704
---
# Ihr Computer ist bereits registriert
Sie sehen diese Seite, da Sie Setup für die [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Clientsoftware ausgeführt haben. Die Software ist jedoch bereits auf Ihrem Computer installiert, und Setup kann nicht fortgesetzt werden.

Mögliche Gründe hierfür sind:

-   Die Clientsoftware wude bereits früher installiert, und Setup wird erneut ausgeführt.

-   Setup wurde auf dem Computer ausgeführt, nachdem ein IT-Administrator Ihr Gerät in [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] deaktiviert hat. Nachdem Ihr Gerät deaktiviert wurde, kann es mehrere Stunden dauern, bis die Clientsoftware von Ihrem Computer entfernt wird.

-   Setup hat eine kürzlich fehlgeschlagene Installation oder Fehler beim Entfernen der Clientsoftware erkannt.

## <a name="bkmk_install"></a>Was Setup auf dem Computer installiert
Setup installiert den [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Client. Nach Abschluss der Installation wird die Clientsoftware weiterhin im Hintergrund ausgeführt, wo sie Ihren Computer für die Verwendung mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] konfiguriert. Dieser Vorgang kann einige Zeit in Anspruch nehmen und umfasst Folgendes:

-   Registrieren Ihres Computer bei [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

-   Senden einer Bestandsaufnahme der Computerhardware und der installierten Software

-   Konfigurieren der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Richtlinie, einschließlich Installation von Endpoint Protection (sofern konfiguriert)

-   Installieren von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center

Nach der Installation von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center können Sie es für den Zugriff auf das Unternehmensportal verwenden, wo Sie Ihren Computer mit Ihrem Geschäftskonto verknüpfen können.

## <a name="bkmk_center"></a>Microsoft Intune Center
Das [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center wird als App auf Ihrem Computer installiert, nachdem der Computer die Clientsoftware installiert und den Computer bei [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] registriert hat. Mit dem [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Centen können folgende Aktionen ausgeführt werden:

-   **Abrufen von Anwendungen aus dem Unternehmensportal** – Suchen und installieren Sie Apps, die von Ihrem IT-Administrator bereitgestellt werden. Wenn Sie sich auf einem neu registrierten Computer erstmalig beim Unternehmensportal anmelden, erhalten Sie die Möglichkeit, Ihr Geschäftskonto mit dem betreffenden Computer zu verknüpfen.

-   **Prüfen auf Softwareupdates** – Suchen Sie Softwareupdates, die vom [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Administrator bereitgestellt werden.

-   **Starten einer Endpoint Protection-Überprüfung Ihres Computers** – Sie können Ihren Computer auf bösartige Software überprüfen.

-   **Anfordern von Remoteunterstützung** – Diese Option steht zur Verfügung, wenn das Betriebssystem Ihres Computers die Remoteunterstützung unterstützt.

## <a name="bkmk_validate"></a>Überprüfen, ob die Clientsoftware installiert ist oder entfernt wurde
**Überprüfen, ob der Client installiert ist:**
Die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Client-Installation ist abgeschlossen, wenn die folgenden Apps auf dem Computer verfügbar sind:

-   **[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center**

-   **[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Endpoint Protection** (wenn Endpoint Protection von Ihrem IT-Administrator aktiviert ist)

Wenn Sie mit der Verwendung von Task-Manager vertraut sind, können Sie nach dem [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Clientdienst suchen, der ausgeführt werden sollte:

-   **OmcSvc**

**Überprüfen, ob der Client entfernt wurde:**
Nachdem der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Client von einem Computer deinstalliert wurde, werden die bei Installation des Clients installierten Apps einschließlich des [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center entfernt.

Die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Clientdienst **OmcSvc** wird entfernt.

## <a name="bkmk_remove"></a>Entfernen der Clientsoftware vom Computer
Standardmäßig wird die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Clientsoftware mehrere Stunden nach der Abkoppelung Ihres Computers von der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Verwaltungskonsole von Ihrem Computer deinstalliert.

Zum manuellen Deinstallieren der [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Clientsoftware von einem Computer können Sie die folgenden Schritte verwenden, um die Deinstallation zu erzwingen:

1.  Öffnen Sie auf dem Computer eine Eingabeaufforderung im Administratormodus.

2.  Wechseln Sie zu dem Ordner **%programfiles%\Microsoft\OnlineManagement\Common**.

3.  Führen Sie den folgenden Befehl aus: **ProvisioningUtil.exe /UninstallAgents /MicrosoftIntune**

Dadurch wird das Entfernen der Clientsoftware geplant.

