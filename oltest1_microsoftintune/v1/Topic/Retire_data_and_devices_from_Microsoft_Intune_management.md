---
description: na
keywords: na
title: Retire data and devices from Microsoft Intune management
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3dbec400-5d8a-47be-b892-7745811d9de2
---
# Au&#223;erkraftsetzen von Daten und Ger&#228;ten in der Microsoft Intune-Verwaltung
![](../Image/Nav_Icons/WIT_Tile_W_Overview.png)![](../Image/Nav_Icons/WIT_Tile_W_GetStarted.png)![](../Image/Nav_Icons/WIT_Tile_W_EnrollDevices.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageDevices.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageApps.png)![](../Image/Nav_Icons/WIT_Tile_W_ProtectResources.png)![](../Image/Nav_Icons/WIT_Tile_W_RetireDevicesHighlight.png)![](../Image/Nav_Icons/WIT_Tile_W_TechnicalReference.png)![](../Image/Nav_Icons/WIT_Tile_W_Troubleshooting.png)
![](../Image/Nav_Icons/WIT_Banner_RetireDevices.png)

Irgendwann kommt der Punkt, an dem ein Mitarbeiter sich vom Unternehmen oder von seinem Gerät trennen muss. In solchen Fällen müssen Sie sicherstellen können, dass weder der Mitarbeiter noch eine andere Person, die sein Gerät verwendet, auf Unternehmensressourcen zugreifen kann. Sie sollten zudem sicherstellen, dass alle Unternehmensinformationen von dem Gerät entfernt werden.

## Schützen von Unternehmensdaten auf verlorenen oder gestohlenen Geräten
Wenn ein Mitarbeiter ein mobiles Gerät verliert oder es ihm gestohlen wird, sollten Sie zunächst sicherstellen, dass die Unternehmensdaten auf dem Gerät nicht gelesen werden können. Sie sollten auch sicherstellen, dass mit dem Gerät keine Anmeldung bei Unternehmensressourcen möglich ist. Es sind mehrere Optionen verfügbar:

-   Sie können [ Unternehmensdaten und -Apps auf dem Gerät gezielt zurücksetzen](https://technet.microsoft.com/library/jj676679.aspx). Dies ist die bevorzugte Maßnahme für Mitarbeiter, die ihre eigenen Geräte in Intune registriert haben, da persönliche Informationen auf dem Gerät nicht betroffen sind. Durch das gezielte Zurücksetzen wird das Gerät aus Intune entfernt, d. h. die zum Anmelden bei Unternehmensressourcen wie Microsoft SharePoint, E-Mail-Konto oder Office 365 erforderlichen Anmeldeinformationen sind nicht mehr verfügbar.

-   Sie können auch eine vollständige Zurücksetzung ausführen, bei der [ein Gerät auf die werkseitigen Standardeinstellungen zurückgesetzt wird](https://technet.microsoft.com/library/jj676679.aspx). Dadurch wird sichergestellt, dass keine Daten – weder persönliche noch geschäftliche – in die falschen Hände geraten, und es ist auch die empfohlene Aktion für Geräte, die dem Unternehmen gehören. Zusätzlich wird dabei auch das Gerät aus Intune entfernt.

**Zurücksetzen von Kennwörtern, wenn sich Benutzer bei ihren Geräten ausgesperrt haben**
Da der erste Schritt zum Schutz von Unternehmensdaten auf mobilen Geräten darin besteht, eine Kennung abzufragen, damit das Gerät verwendet werden kann, müssen Sie manchmal [eine Kennung zurücksetzen](https://technet.microsoft.com/library/jj676679.aspx#BKMK_passcode) oder einem Mitarbeiter hierbei helfen, entweder indem Sie die Kennung entfernen oder durch Remotefestlegung einer vorübergehenden Kennung.

**Umgehen der Aktivierungssperre auf iOS-Geräten**
Wenn firmeneigene iOS-Geräte durch Aktivierungssperre geschützt sind und das Gerät verloren geht oder gestohlen wird, kann die Aktivierungssperre dafür sorgen, dass das Gerät mit seinen Daten nicht von den falschen Personen verwendet werden kann. Wenn Sie allerdings das Gerät wiederbeschaffen können oder wenn ein Mitarbeiter bei Rückgabe des Geräts vergisst, die Aktivierungssperre zu deaktivieren, müssen Sie das Gerät entsperren. Wenn Sie nicht über die Apple-ID des Benutzers und das Kennwort zum Entsperren verfügen, können Sie die [Umgehung der Aktivierungssperre von Intune](https://technet.microsoft.com/library/mt414176.aspx) verwenden.

## Widerrufen des Zugriffs auf das Unternehmensnetzwerk
Wenn ein Mitarbeiter das Unternehmen verlässt, müssen Sie auch sicherstellen, dass dieser keine Unternehmensdaten mitnimmt, wenn er ein privates Gerät verwendet oder es versäumt hat, firmeneigene Hardware zurückzugeben.  Im ersten Fall ist das [gezielte Zurücksetzen des privaten Geräts des Mitarbeiters](https://technet.microsoft.com/library/jj676679.aspx) ausreichend. Im zweiten Fall können Sie die Hardware [remote sperren](https://technet.microsoft.com/library/jj676679.aspx). Dadurch wird verhindert, dass Firmeninformationen und Firmenhardware missbräuchlich verwendet werden, obwohl Sie das Gerät möglicherweise als Verlust abschreiben müssen.

Sie sollten auch die Lizenz für das Intune-Benutzerkonto des Mitarbeiters widerrufen. Dadurch wird die Lizenz freigegeben, und Sie können sie einem neuen Benutzerkonto zuweisen.

## Außerbetriebnehmen von Hardware
Manchmal ist es das Gerät selbst, das das Ende seines Lebenszyklus erreicht hat. In solchen Fällen werden durch das [Zurücksetzen auf die Werkseinstellungen](https://technet.microsoft.com/library/jj676679.aspx) alle Daten vom Gerät und das Gerät aus Intune entfernt. Dann können Sie die Hardware gemäß der Unternehmensrichtlinie beseitigen.

**Überwachen des Bestands und der Lizenznutzung**
Sie können Änderungen am Bestand und an den Lizenzen über die integrierten [Bestandsberichte](https://technet.microsoft.com/library/dn646977.aspx) verfolgen.

## Siehe auch
[Dokumentation zu Microsoft Intune](../Topic/Documentation_for_Microsoft_Intune.md)

