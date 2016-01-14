---
description: na
keywords: na
title: Understand your devices with inventory in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 312911fe-b963-4949-9911-ae425e0590b2
---
# Verstehen Sie Ihre Ger&#228;te mithilfe des Inventars in Microsoft Intune
Mithilfe von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] können Sie das Inventar der verwalteten Geräte und Computer in Ihrer Organisation anzeigen.

## So zeigen Sie ein Inventar mobiler Geräte an
Um das von den mobilen Geräten gesammelte Inventar anzuzeigen, führen Sie die [Inventurberichte für mobile Geräte](https://technet.microsoft.com/library/dn646977.aspx) aus.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] sammelt das folgende Inventar von den mobilen Geräten:

|Eigenschaftsgruppe|Eigenschaft|Exchange ActiveSync|iOS|Windows RT und Windows 8.1|Windows Phone 8 und Windows Phone 8.1|Hinweise|
|----------------------|---------------|-----------------------|-------|------------------------------|-----------------------------------------|------------|
|System|Name|Ja|Ja|Ja|Ja||
||Eindeutige Geräte-ID||Ja|Ja|Ja||
||Seriennummer||Ja||||
||E-Mail-Adresse|Ja|||||
|Betriebssystem|Betriebssystemtyp|Ja||Ja|Ja||
||Version des Betriebssystems|Ja|Ja|Ja|Ja||
||Betriebssystemsprache|Ja|||Ja||
|Speicher|Gesamtmenge des Speicherplatzes||Ja|Ja||Anzeige in GB|
||Freier Speicherplatz||Ja|Ja||Anzeige in GB|
|Exchange-Details|Letzter Exchange-Status|Ja|||||
||Status der letzten Richtlinienaktualisierung|Ja|||||
||Zugriffsstatus|Ja|||||
||Ursache für Zugriffsstatus|Ja|||||
||ActiveSync-ID|Ja|||||
|Systemgehäuse|Gehäuse|Ja|„Unbekannt“|„Unbekannt“|„Unbekannt“|Bei MDM-verwalteten Geräten wird das Gehäuse als „Unbekannt“ angezeigt.|
||IMEI||Ja||||
||MEID||Ja||||
||Hersteller|||Ja|Ja||
||Modell|Ja|Ja|Ja|Ja||
||Telefonnummer||Ja|||Die Telefonnummer wird mit Ausnahme der letzten 4 Ziffern mit „&#42;“ maskiert.|
|Netzwerkdetails|Netzbetreiber des Abonnenten||Ja||||
||Mobilfunktechnologie||Ja||||
||WiFi-MAC||Ja|Ja|||
|Dienstinformationen|Registrierungsdatum||Ja|Ja|Ja|Anzeige als lokale Zeit|
||Letzter Kontakt|Ja|Ja|Ja|Ja|Anzeige als lokale Zeit|
||Verwaltungsstatus|Ja|||||

## So zeigen Sie ein Computerinventar an
Um das von den Computern gesammelte Inventar anzuzeigen, führen Sie die [ Computerinventurberichte](https://technet.microsoft.com/library/dn646977.aspx) aus.

## Siehe auch
[Überwachung und Berichte in Microsoft Intune](../Topic/Monitoring_and_reports_with_Microsoft_Intune.md)

