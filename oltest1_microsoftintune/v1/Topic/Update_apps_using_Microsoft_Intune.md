---
description: na
keywords: na
title: Update apps using Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: beee6933-876a-4be0-b395-4c24cfbd519b
---
# Aktualisieren von Apps mit Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] unterstützt Sie bei der Verwaltung von App-Updates. Anhand der Informationen in diesem Thema erfahren Sie, wie Sie Apps aktualisieren, wenn eine neue Version erforderlich ist.

## Aktualisieren von Apps
Wenn eine neue Version einer von Ihnen bereitgestellten App veröffentlicht wird, können Sie mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] die neuere Version der App aktualisieren und bereitstellen. Sie können eine Bereitstellung nur durch eine neuere Version der gleichen App (mit derselben ID) ersetzen. App-Updates können nicht zum Aktualisieren einer Bereitstellung mit einem anderen App-Paket verwendet werden.

> [!IMPORTANT]
> Beim Bereitstellen einer App mit der Bereitstellungsaktion **Erforderliche Installation** und einer späteren Änderung der Bereitstellungsaktion in **Verfügbare Installation** werden Updates für die App auf Geräten, auf denen die App vor der Bereitstellungsänderung installiert war, nicht automatisch installiert. Gehen Sie wie folgt vor, um dieses Problem zu beheben:
> 
> -   Bitten Sie den Benutzer des Geräts das Unternehmensportal zu öffnen, die installierte App auszuwählen und auf **Installieren** zu klicken.
> -   Ändern Sie die Bereitstellungsaktion in **Deinstallieren**, und stellen Sie die App nach der Deinstallation der App erneut mit der Bereitstellungsaktion **Verfügbare Installation** bereit.

#### So aktualisieren Sie eine App

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://account.manage.microsoft.com/admin/default.aspx) auf **Apps** &gt; **Apps**.

2.  Wählen Sie in der Liste **Apps** die zu aktualisierende App aus, und klicken Sie dann auf **Bearbeiten**.

3.  Geben Sie im Assistenten **Software bearbeiten** neue Details für das App-Paket ein.

4.  Klicken Sie danach auf **Aktualisieren**.

Wenn Geräte das nächste Mal prüfen, ob Apps verfügbar sind, wird die App automatisch auf die neueste Version aktualisiert.

## Siehe auch
[Bereitstellen und Konfigurieren von Apps mit Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)
[Außerkraftsetzen von Apps mit Microsoft Intune](../Topic/Retire_apps_using_Microsoft_Intune.md)

