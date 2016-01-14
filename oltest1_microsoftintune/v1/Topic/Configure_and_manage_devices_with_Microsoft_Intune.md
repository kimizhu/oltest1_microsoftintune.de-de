---
description: na
keywords: na
title: Configure and manage devices with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7b938d95-c068-4d71-a580-c1492c4bff27
---
# Konfigurieren und Verwalten von Ger&#228;ten mit Microsoft Intune
![](../Image/Nav_Icons/WIT_Tile_W_Overview.png)![](../Image/Nav_Icons/WIT_Tile_W_GetStarted.png)![](../Image/Nav_Icons/WIT_Tile_W_EnrollDevices.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageDevicesHighlight.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageApps.png)![](../Image/Nav_Icons/WIT_Tile_W_ProtectResources.png)![](../Image/Nav_Icons/WIT_Tile_W_RetireData.png)![](../Image/Nav_Icons/WIT_Tile_W_TechnicalReference.png)![](../Image/Nav_Icons/WIT_Tile_W_Troubleshooting.png)
![](../Image/Nav_Icons/WIT_Banner_ManageDevices.png)

Verwenden Sie VPN-Profile, WLAN-Profile und Konfigurationsrichtlinien, um Mitarbeitern den Zugriff auf Ihr Netzwerk zu gewähren und gleichzeitig die Sicherheitsanforderungen Ihres Unternehmens zu erfüllen.

Benutzer möchten auf vielen verschiedenen Geräten sowie ortsunabhängig auf ihre E-Mails und Arbeit zugreifen. Dies bietet Ihnen die Gelegenheit, die Produktivität zu steigern, stellt aber auch Probleme im Hinblick auf die Sicherheit Ihrer Unternehmensdaten dar.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] kann diese Probleme mithilfe von VPN-Profilen, WLAN-Profilen und Konfigurationsrichtlinien lösen.

## Verwenden von VPN- oder WLAN-Profilen zum Aktivieren des Zugriffs auf Unternehmensressourcen
Mithilfe von [Profilen für den Ressourcenzugriff](https://technet.microsoft.com/library/dn997277.aspx) können Sie Mitarbeitern das Abrufen von E-Mails oder das Einrichten von WLANs bzw. VPNs für den Zugriff auf Unternehmensressourcen erleichtern. Mit diesen Profilen können Sie die Geräte mit den Zugriffseinstellungen vorkonfigurieren, die für E-Mail- und Unternehmensdateien erforderlich sind. Viele Leute verwenden z. B. eine VPN-Verbindung (virtuelles privates Netzwerk), um remote arbeiten zu können. Die Einstellungen zum Erstellen einer VPN-Verbindung (oder eines **Profils**) sind komplex und typische Endbenutzer sind damit möglicherweise überfordert.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ermöglicht es Ihnen, diese Einstellungen vorab zu konfigurieren und auf den Geräten der Benutzer bereitzustellen. Dies bedeutet, dass die Mitarbeiter keine komplexen VPN-Einstellungen eingeben müssen, sondern einfach das VPN-Profil aus einer Liste auswählen, um die Verbindung automatisch herzustellen. Darüber hinaus können Sie die Sicherheitsfunktionen von Zertifikaten zum Schutz dieser Verbindungen nutzen.

## Verwalten von Einstellungen und Features mit Intune-Richtlinien
Stellen Sie sich vor, Sie sind IT-Administrator eines Designbüros. Sie arbeiten an einem neuen Produkt und möchten nicht, dass die Produktdetails an die Öffentlichkeit gelangen. Sie entscheiden sich dazu, die Verwendung der Kamera bei den mobilen Geräten der Mitarbeiter zu deaktivieren, um die Sicherheit zu maximieren. Mit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] können Sie dieses Ziel mithilfe einer **Konfigurationsrichtlinie** auf einfache Weise erreichen.

Obwohl [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] eine [Vielzahl von Einstellungen](https://technet.microsoft.com/library/dn646984.aspx) zum Konfigurieren von Geräten bereitstellt, kann es vorkommen, dass die erforderliche Einstellung nicht verfügbar ist. In vielen Fällen können Sie dieses Problem mit einer benutzerdefinierten Richtlinie beheben, mit der Sie OMA-URI-Einstellungen (einem allgemeinen Standard zum Konfigurieren von mobilen Geräten) konfigurieren können, um die erforderlichen Werte festzulegen.

## Verwalten von Computern
Obwohl Sie [Computer mit Windows 8.1 und höher als mobile Geräte registrieren](https://technet.microsoft.com/library/dn764959.aspx) können, möchten Sie diese aber in manchen Fällen möglicherweise durch Installieren des Intune-Computerclients verwalten. Das [Verwalten von Computern mit Intune](https://technet.microsoft.com/library/dn646959.aspx) bietet Ihnen einige Optionen, die beim Verwalten als mobile Geräte nicht zur Verfügung stehen, z. B. das Verwalten von Windows-Softwareupdates, EndPoint Protection und Windows-Firewall-Einstellungen.

## Siehe auch
[Dokumentation zu Microsoft Intune](../Topic/Documentation_for_Microsoft_Intune.md)

