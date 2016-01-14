---
description: na
keywords: na
title: Enable access to company resources with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3dd8dd4e-e165-4d0c-97b7-b3e86ebab909
---
# Aktivieren des Zugriffs auf Unternehmensressourcen mit Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **Profile für den Ressourcenzugriff** werden gemeinsam verwendet, um Benutzern den Zugriff auf die Dateien und Ressourcen zu ermöglichen, die sie für ihre Arbeit benötigen – unabhängig davon, wo sie gespeichert sind.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] stellt zu diesem Zweck die folgenden Richtlinien für mobile Geräte bereit. Klicken Sie auf die Elemente in der Tabelle, um ausführliche Informationen zum Konfigurieren der Richtlinie anzuzeigen:

## Profile für den Ressourcenzugriff und unterstützte Plattformen

|Intune-Richtlinie|Funktion|Windows 8.1 und höher|Windows Phone 8.1 und höher|iOS|Android|Samsung KNOX|
|---------------------|------------|-------------------------|-------------------------------|-------|-----------|----------------|
|[Zertifikatprofile](https://technet.microsoft.com/library/dn818904.aspx)|Ermöglichen den sicheren Zugriff auf Unternehmensressourcen einschließlich Drahtlosnetzwerken und VPN-Verbindungen.|Ja|Ja|Ja|Ja|Ja|
|[WLAN-Profile](https://technet.microsoft.com/library/dn818903.aspx)|Bereitstellen von Einstellungen für drahtlose Netzwerke für Ihre Benutzer. Durch Bereitstellen dieser Einstellungen erleichtern Sie dem Endbenutzer das Herstellen einer Verbindung mit dem Unternehmensnetzwerk.|Ja (Sie können ein Windows-WLAN-Profil importieren)|Ja (Sie können den OMA-URI konfigurieren) <sup>1</sup>|Ja|Ja|Ja|
|[VPN-Profile](https://technet.microsoft.com/library/dn818905.aspx)|Stellen Einstellungen für ein virtuelles privates Netzwerk (VPN) für Benutzer bereit. Durch Bereitstellen dieser Einstellungen erleichtern Sie dem Endbenutzer das Herstellen einer Verbindung mit Ressourcen im Unternehmensnetzwerk.|Ja|Ja|Ja|Ja|Ja|
|[E-Mail-Profile](https://technet.microsoft.com/library/dn800672.aspx)|Dienen zum Erstellen, Bereitstellen und Überwachen von E-Mail-Einstellungen für Exchange ActiveSync auf Geräten im Unternehmen.|Nein|Ja|Ja|Nein|Ja|
<sup>1</sup> Informationen zum Konfigurieren eines WLAN-Profils für Windows Phone 8.1 mithilfe von OMA-URI finden Sie [in diesem Blogbeitrag](http://blogs.technet.com/b/microsoftintune/archive/2015/02/23/using-oma-uri-to-create-custom-wi-fi-profiles-for-windows-phone-8-1.aspx).

## Siehe auch
[Konfigurieren und Verwalten von Geräten mit Microsoft Intune](../Topic/Configure_and_manage_devices_with_Microsoft_Intune.md)

