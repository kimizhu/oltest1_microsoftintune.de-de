---
description: na
keywords: na
title: Manage alerts in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 74dc4ce4-21da-4f40-a07f-3eea34561eee
robots: noindex,nofollow
---
# Verwalten von Warnungen in Microsoft Intune
Über den Arbeitsbereich **Warnungen** in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] können Sie sich schnell einen Überblick über die Gesamtintegrität der verwalteten Geräte innerhalb Ihres Unternehmens verschaffen und Probleme erkennen.

#### So zeigen Sie aktive Warnungen an

1.  Führen Sie in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] einen der folgenden Schritte aus:

    -   **Zum Anzeigen allgemeiner Informationen zu Warnungen** einschließlich der drei wichtigsten Warnungen klicken Sie auf **Systemübersicht**. Sie können die Links dieser Warnungen anklicken, um ausführlichere Informationen aufzurufen.

    -   **Zum Anzeigen von Zusammenfassungsdaten für Warnungen** klicken Sie auf **Warnungen &gt; Übersicht**. Auf der Seite **Warnungsübersicht** wird im Bereich **Warnungstypübersicht** eine Zusammenfassung der Warnungen angezeigt. Kritische Warnungen werden zuerst angezeigt. Sie können die Links dieser Warnungen anklicken, um ausführlichere Informationen aufzurufen.

        > [!NOTE]
        > In einigen Fällen kann ein Warnungstyp mehr als einmal in der Liste **Warnungstypübersicht** erscheinen.
        > 
        > Beispiel: Die folgenden Instanzen des Warnungstyps "Freier Speicherplatz auf logischem Datenträger" werden möglicherweise in der Liste angezeigt:
        > 
        > -   3 Freier Speicherplatz auf logischem Datenträger
        > -   2 Freier Speicherplatz auf logischem Datenträger
        > 
        > Diese Situation tritt auf, wenn derselbe Warnungstyp für Geräte mit unterschiedlichen Betriebssystemen generiert wird. In dem Beispiel wurde die erste Instanz des Warnungstyps "Freier Speicherplatz auf logischem Datenträger" (3 Freier Speicherplatz auf logischem Datenträger) möglicherweise von Computern generiert, auf denen [!INCLUDE[firstref_client_7](../Token/firstref_client_7_md.md)] ausgeführt wird. Die zweite Instanz des Warnungstyps wurde möglicherweise von Computern generiert, auf denen [!INCLUDE[firstref_vista](../Token/firstref_vista_md.md)] ausgeführt wird.

    -   **Zum Anzeigen aller aktiven Warnungen** klicken Sie auf **Warnungen &gt; Alle Warnungen**. Auf der Seite **Warnungen** wird eine Liste aller aktiven Warnungen mit folgenden Spalten angezeigt:

        1.  **Name**: Dies ist der Name des Warnungstyps, von dem die Warnung generiert wurde.

        2.  **Quelle**: Dies ist ein Link zur Quelle der Warnung. Wenn der Anzeigeschwellenwert des Warnungstyps auf **Alle anzeigen** festgelegt ist, wird über diesen Link ein einzelnes Gerät angezeigt. Wenn der Anzeigeschwellenwert des Warnungstyps auf einen Wert festgelegt ist, wird über diesen Link eine Liste aller Geräte angezeigt, die von dieser Warnung betroffen sind.

        3.  **Zuletzt aktualisiert**: Hier wird angegeben, wann die Warnung zuletzt geändert wurde. Wenn eine Warnung geschlossen ist, wird hier die Uhrzeit angezeigt, zu der die Warnung geschlossen wurde.

        4.  **Schweregrad**: Gibt den Schweregrad der Warnung an.

## Anzeigen von Warnungen am Schwarzen Brett
In am Schwarzen Brett angezeigten Warnungen werden wichtige Dienstankündigungen wie beispielsweise anstehende Upgrades, Wartungen oder Ausfälle von Diensten aufgeführt. Mithilfe dieses Verfahrens können Sie Warnungen am Schwarzen Brett anzeigen und verwalten.

#### So zeigen Sie Warnungen am Schwarzen Brett an und verwalten sie

1.  Klicken Sie im [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] auf **Systemübersicht**.

2.  Wenn wichtige Dienstankündigungen vorliegen, werden Sie im Bereich **Schwarzes Brett** angezeigt.

3.  Wenn Sie eine am Schwarzen Brett angezeigte Warnung in eine CSV-Datei (mit kommagetrennten Werten) oder eine HTML-Datei importieren möchten, klicken Sie in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] auf **Warnungen &gt; Alle Warnungen &gt; Benachrichtigungen**. Wählen Sie eine Benachrichtigung aus, klicken Sie auf das Symbol zum Exportieren der Liste, und folgen Sie dann den Anweisungen.

## Überprüfen der Intune-Status
Im Arbeitsbereich **Systemübersicht** können Sie Probleme, die Ihre sofortige Aufmerksamkeit erfordern, anhand der Systemstatusübersichten für Endpoint Protection, Updates, Agent-Integrität, Richtlinien und Software erkennen und priorisieren. In Fehlermeldungen nach Systemunterbrechungen ist ebenfalls ein Link zur Übersicht **Dienststatus** enthalten. In der Übersicht **Dienststatus** werden Details zum Problem an jedem Speicherort sowie der Zeitpunkt der letzten Aktualisierung angezeigt.

#### So zeigen Sie den Status Ihres Abonnements an

1.  Klicken Sie im [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] auf **Systemübersicht**.

2.  Im Bereich **Systemstatus** können Sie den Status der verschiedenen [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Komponenten untersuchen. In vielen dieser Elemente sind Links enthalten, mit denen Sie weitere Informationen anzeigen können. Wenn Sie beispielsweise unter **Endpoint Protection** die Anzahl der Instanzen auswählen, wird im Arbeitsbereich **Endpoint Protection** eine Liste mit erkannter Malware angezeigt. Bei Auswahl der Anzahl der Geräte wird der Arbeitsbereich **Gruppen** mit einer Liste von Geräten angezeigt, auf denen die Malware gefunden wurde.

## Schließen und erneutes Aktivieren von Warnungen
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Warnungen bleiben bis zum Auftreten eines der folgenden Ereignisse aktiv:

-   Das Problem, das die Generierung der Warnung verursacht hatte, wird beseitigt.

-   Die Warnung wird manuell geschlossen.

-   Seit dem Generieren der Warnung sind fünf Tage vergangen. Nach 45 Tagen läuft die Warnung ab und wird automatisch geschlossen.

Warnungen, die als geschlossen markiert sind, werden nach 90 Tagen dauerhaft gelöscht.

#### So schließen Sie eine Warnung manuell

1.  Führen Sie in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] einen der folgenden Schritte aus:

    1.  **Zum Schließen einer Warnung in der Warnungsliste** klicken Sie auf **Warnungen &gt; Alle Warnungen**. Wählen Sie eine Warnung aus, und klicken Sie dann auf **Warnung schließen**.

    2.  **Zum Schließen einer Warnung für ein bestimmtes Gerät** klicken Sie auf **Warnungen &gt; Alle Geräte**. Wählen Sie ein Gerät aus, und klicken Sie auf **Eigenschaften anzeigen**. Wählen Sie dann auf der Registerkarte **Warnungen** eine Warnung aus, und klicken Sie auf **Warnung schließen**.

    3.  **Zum Schließen einer auf dem Schwarzen Brett angezeigten Warnung** klicken Sie auf **Systemübersicht**. Klicken Sie neben der Warnung am Schwarzen Brett auf das **X**.

#### So zeigen Sie geschlossene Warnungen an und aktivieren sie erneut

1.  Klicken Sie im [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] auf **Warnungen &gt; Alle Warnungen**.

2.  Klicken Sie in der Liste **Filter** auf **Geschlossen**.

    Die Namen und zusätzliche Informationen zu den Warnungen werden im Verwaltungslistenbereich angezeigt. Details zur ausgewählten Warnung werden im Vorschaufenster angezeigt.

3.  Klicken Sie zum erneuten Aktivieren der ausgewählten Warnung auf **Warnung erneut aktivieren**.

