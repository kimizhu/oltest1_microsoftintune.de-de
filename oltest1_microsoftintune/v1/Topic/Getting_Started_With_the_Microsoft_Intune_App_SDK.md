---
description: na
keywords: na
title: Getting Started With the Microsoft Intune App SDK
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38ebd3f5-cfcc-4204-8a75-6e2f162cd7c1
---
# Erste Schritte mit Microsoft Intune App SDK
Dieses Handbuch "Erste Schritte" soll Ihnen dabei helfen, Ihre mobile Anwendung schnell für die mobile Anwendungsverwaltung (MAM) mit Microsoft Intune zu aktivieren. Es ist sicherlich hilfreich, sich zunächst mit den Vorteilen des Intune App SDK vertraut zu machen und das Dokument [Vorteile von Intune App SDK](Benefits_of_the_Intune_App_SDK.md) zu lesen.

Dieses Handbuch behandelt die wichtigsten Schritte zum Aktivieren der mobilen Anwendungsverwaltung in Ihrer App mit Microsoft Intune. Intune App SDK unterstützt plattformübergreifend vergleichbare Szenarien und soll für den IT-Administrator eine plattformübergreifende konsistente Umgebung darstellen. Bei der Unterstützung bestimmter Funktionen gibt es jedoch geringfügige Unterschiede, die auf Einschränkungen der jeweiligen Plattform zurückzuführen sind.

# Erste Schritte

## Registrieren für Microsoft Connect

Intune App SDK ist derzeit über Microsoft Connect verfügbar und setzt eine Anmeldung voraus. Dazu müssen Sie sich mit Ihrer geschäftlichen E-Mail-Adresse für ein [Microsoft-Konto](https://connect.microsoft.com/ConfigurationManagervnext/InvitationUse.aspx?ProgramID=8967&InvitationID=8967-YJYJ-8G6X) registrieren.

Ihre Registrierung erhält den Status "Ausstehend", bis das Intune-Team die Anforderung überprüft hat. Die normale Reaktionszeit beträgt 2 bis 3 Arbeitstage. Im Anschluss an die Genehmigung erhalten Sie eine E-Mail-Benachrichtigung mit einem oder mehreren Links, über die Sie das Intune App SDK für Ihre Plattform(en) und alle entsprechenden Handbücher herunterladen können. Sie können diese Handbücher auch auf der MSDN-Website aufrufen.

## Registrieren Ihrer Store-App bei Microsoft Intune

**Ihre aktivierte App soll nur intern im Unternehmen und nicht im Apple oder Google App Store verfügbar sein**: Sie brauchen Ihre App nicht zu registrieren. Derartige interne Apps lädt der IT-Administrator zur Bereitstellung direkt in die Microsoft Intune-Verwaltungskonsole. Intune erkennt, dass die App mit dem SDK erstellt wurde, und bietet dem IT-Administrator die Möglichkeit, eine MAM-Richtlinie zuzuweisen. Sie können den Abschnitt [Aktivieren von mobilen iOS- oder Android-Apps für die mobile Anwendungsverwaltung (MAM) mit dem SDK](#enableapp) überspringen .

**Sie sind ein ISV und entwickeln eine App, die für Kunden im Apple oder Google App Store verfügbar sein soll**: Sie müssen die App zuerst bei Microsoft Intune registrieren und den Registrierungsbedingungen zustimmen. Bei dieser Gelegenheit können Sie auch den Deep-Link der App angeben. Anschließend kann ein IT-Administrator der App eine Intune-MAM-Richtlinie zuweisen. Solange die Registrierung nicht abgeschlossen und vom Microsoft Intune-Team bestätigt wurde, gibt es keine Möglichkeit, in der Verwaltungskonsole dem Deep-Link der App eine MAM-Richtlinie zuzuweisen. Microsoft bietet auch eine Microsoft Intune-Partnerwebsite an, auf der die App registriert wird. Dadurch weiß der Kunde, dass sie Microsoft Intune-MAM-Richtlinien unterstützt.

Zu Beginn des Registrierungsvorgangs müssen Sie die Microsoft Intune-Partnervereinbarung **lesen und unterschreiben**. Diese Vereinbarung enthält die Bedingungen, denen Ihr Unternehmen zustimmen muss, bevor es ein Microsoft Intune-App-Partner werden kann. Sie müssen sich anmelden, um dieses Dokument anzeigen zu können. Sie finden die Vereinbarung auf der Microsoft Connect-Website unter Intune App SDK auf der Registerkarte "Surveys" oder hier. Sie werden auch nach dem Namen der App und Ihres Unternehmens gefragt und müssen den Deep-Link Ihrer Anwendung für den Google oder iTunes Store angeben.

![Microsoft Connect](/Image/Microsoft_Connect.png)

Wir verwenden die bei der Registrierung angegebene E-Mail-Adresse, um den Eingang des Registrierungsvorgangs zu bestätigen und diesen abzuschließen. Über diese Registrierungsadresse nehmen wir bei Fragen oder Problemen auch Kontakt mit Ihnen auf.

**Informationen zum Registrierungsvorgang**: Nachdem Sie das Formular gesendet haben, nimmt Microsoft über die bei der Registrierung angegebene E-Mail-Adresse Kontakt mit Ihnen auf, um den erfolgreichen Eingang zu bestätigen oder zusätzliche Informationen anzufordern, um die Registrierung abschließen zu können. Sie erhalten ebenso Nachricht, wenn Ihre App erfolgreich bei Microsoft Intune registriert wurde und auf der Microsoft Intune-Partnerwebsite empfohlen wird. Nachdem der Eingang der Informationen bestätigt wurde, wird der Deep-Link Ihrer App in das nächste monatliche Intune-Dienstupdate einbezogen. Wenn die Registrierung mit allen Informationen beispielsweise im Juli abgeschlossen ist, wird der Deep-Link der App Mitte August unterstützt. Wenn sich in Zukunft der Deep-Link Ihrer Store-App ändert, müssen Sie die App neu registrieren. Außerdem müssen Sie uns informieren, wenn Sie Ihre App mit einer neuen Intune App SDK-Version aktualisieren.

**Hinweis**: Alle Daten, die in obigem Formular oder über die E-Mail-Korrespondenz mit dem Intune-Team erfasst werden, unterliegen der [Microsoft-Datenschutzrichtlinie](https://www.microsoft.com/en-us/privacystatement/default.aspx).

## <a name="enableapp"></a> Aktivieren von mobilen iOS- oder Android-Apps für die mobile Anwendungsverwaltung (MAM) mit dem SDK

Zum Aktivieren Ihrer mobilen iOS-App benötigen Sie Folgendes:

1. **Handbuch [Intune App SDK für iOS-Entwickler](Microsoft_Intune_App_SDK_for_iOS_Developer_Guide.md)**: In diesem Dokument wird Schritt für Schritt erläutert, wie Sie Ihre mobile iOS-App mit dem Intune App SDK aktivieren. Sie finden dieses Dokument im Dokumentationsordner, der im heruntergeladenen Intune App SDK-Paket enthalten ist.
2. **Intune App SDK für iOS**: Das von Microsoft Intune heruntergeladene Intune App SDK-Paket enthält den signierten Ordner "Intune App SDK for iOS". Dieser Ordner enthält alle Inhalte des Intune App SDK für iOS.

Zum Aktivieren Ihrer mobilen Android-App mit Intune App SDK benötigen Sie Folgendes:

1. **Handbuch **Intune App SDK für Android-Entwickler****: In diesem Dokument wird Schritt für Schritt erläutert, wie Sie Ihre mobile Android-App mit dem Intune App SDK aktivieren. Sie finden dieses Dokument im Dokumentationsordner, der im heruntergeladenen Intune App SDK-Paket enthalten ist.
2. **Intune App SDK für Android**: Das von Microsoft Intune heruntergeladene Intune App SDK-Paket enthält den signierten Ordner "Intune App SDK for Android". Dieser Ordner enthält alle Inhalte des Intune App SDK für Android.

## Deaktivieren der Telemetrie für Ihre App

**Entwickler mit iOS MAM SDK**: Das SDK protokolliert standardmäßig SDK-Telemetriedaten zu Verwendungsereignissen. Diese Daten werden an Microsoft Intune gesendet.

Wenn von Ihrer Anwendung keine SDK-Telemetriedaten an Microsoft Intune gesendet werden sollen, müssen Sie die SDK-Telemetrieübertragung **deaktivieren**, indem Sie unter `IntuneMAMSettings` die Eigenschaft `MAMTelemetryDisabled` auf "YES" setzen.

**Entwickler mit Android MAM SDK**: Vom SDK werden keine SDK-Telemetriedaten protokolliert.

## Testen MAM-fähiger Apps mit Microsoft Intune

Nachdem Sie die notwendigen Schritte zur Integration des Intune App SDK in Ihre iOS- oder Android-App abgeschlossen haben, müssen Sie sicherstellen, dass alle Anwendungsverwaltungsrichtlinien für den Endbenutzer und IT-Administrator aktiviert und funktionsfähig sind. Zum Testen Ihrer aktivierten App benötigen Sie Folgendes:

1. **Testen MAM-fähiger Apps mit Microsoft Intune**: Dieses Dokument zeigt Schritt für Schritt, wie Sie aktivierte iOS- oder Android-Apps mit Microsoft Intune testen. Sie finden dieses Dokument im Dokumentationsordner, der im heruntergeladenen Intune App SDK-Paket enthalten ist.
2. **Microsoft Intune-Konto**: Zum Testen MAM-fähiger Apps mit Microsoft Intune benötigen Sie ein Microsoft Intune-Konto. ISVs, die ihre iOS- oder Android-Store-Apps für MAM aktivieren, erhalten nach Abschluss ihrer Registrierung bei Microsoft Intune (wie unter Registrierung beschrieben) einen Promo-Code. Der Promo-Code bietet die Möglichkeit, sich für eine Microsoft Intune-Testversion (1 Jahr erweiterte Verwendung) anzumelden. Wenn Sie eine spartenspezifische App entwickeln, die nicht an den Store gesendet wird, sollten Sie über Ihre Organisation auf Microsoft Intune zugreifen können. Sie können sich auch bei [Microsoft Intune](https://portal.office.com/Signup/Signup.aspx?OfferId=40BE278A-DFD1-470a-9EF7-9F2596EA7FF9&dl=INTUNE_A&ali=1#0) für eine kostenlose Testversion (1 Monat) anmelden.





