---
description: na
keywords: na
title: Microsoft Intune mobile app management policies and iOS Open In
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a4515c1-b325-4ac1-9f0a-45ac27e00681
---
# Microsoft Intune-Richtlinien f&#252;r die Verwaltung von mobilen Apps und iOS-Feature &quot;&#214;ffnen in&quot;
Mit dem **Open in Management**-Feature für iOS-Geräte kann der Datenfluss zwischen Apps gesteuert werden. Die Einschränkungen für "Open in Management" werden in den Konfigurationsprofileinstellungen festgelegt und mithilfe der MDM-Software bereitgestellt.  Wenn der Benutzer die verwaltete App installiert, werden die Einschränkungen angewendet.

Die Richtlinien für die Verwaltung von mobilen Apps (Mobile App Management, MAM) unterstützen **Open in Management** zum Schutz von Unternehmensdaten auf Geräten wie nachstehend beschrieben:

-   **Von keiner MDM-Lösung verwaltete BYOD-Geräte:** Sie können die MAM-Richtlinieneinstellungen so festlegen, dass dieApp nur Daten an verwaltete Apps übertragen kann. Wenn der Endbenutzer eine geschützte Datei in einer nicht verwalteten App öffnet, kann die Datei nicht gelesen werden.

-   **Von Intune oder einer MDM-Drittanbieterlösung verwaltete Geräte:** Sie können Unternehmensdaten auf die gleiche Weise schützen wie oben beschrieben, indem Sie nur Datenübertragungen an verwaltete Apps zulassen. Sie können auch die Liste der Apps über Ihren MDM-Anbieter steuern.   Weitere Informationen zu Geräten, die von Intune registriert und verwaltet werden, finden Sie unter [Vorbereiten von iOS-Apps für die Verwaltung mobiler Anwendungen mit dem Microsoft Intune App Wrapper-Tool](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md).

## Siehe auch
[Konfigurieren der App-Richtlinien für die Verhinderung von Datenverlust mit Microsoft Intune](../Topic/Configure_data_loss_prevention_app_policies_with_Microsoft_Intune.md)

