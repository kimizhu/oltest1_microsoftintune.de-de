---
description: na
keywords: na
title: Help secure Windows PCs with Endpoint Protection for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 682a83ec-bcf4-46ed-9a74-61b87b6a86a3
---
# Sch&#252;tzen von Windows-PCs mit Endpoint Protection f&#252;r Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] kann Sie dabei unterstützen, Ihre verwalteten Computer auf vielfältige Weise zu schützen, einschließlich Endpoint Protection, das Echtzeitschutz gegen Malwarebedrohungen bietet, Malwaredefinitionen auf dem aktuellen Stand hält und Computer automatisch überprüft.[!INCLUDE[epshort](../Token/epshort_md.md)] bietet außerdem Tools, mit denen Sie Angriffe durch Malware kontrollieren und überwachen können.

Wenn Sie den [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Client noch nicht auf Ihren Computern installiert haben, finden Sie weitere Informationen unter [Installieren des Windows-PC-Clients mit Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

Verwenden Sie die Informationen in den folgenden Abschnitten zum Konfigurieren, Bereitstellen und Überwachen von [!INCLUDE[epshort](../Token/epshort_md.md)].

## Verwenden von Endpoint Protection in Microsoft Intune

### Vorbereitung
Eine ihrer wichtigsten Aufgaben als IT-Administrator besteht darin, die von Ihnen verwalteten Computer frei von Malware und Viren zu halten. Bevor Sie [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] auf Clientcomputern in Ihrer Organisation bereitstellen, sollten Sie entscheiden, wie Sie Ihre Computer schützen. Hierzu wählen Sie eine der folgenden Optionen aus und konfigurieren die zugehörigen Richtlinieneinstellungen:

|Ziel:|Richtlinieneinstellungen für Endpoint Protection|Weitere Informationen|
|---------|----------------------------------------------------|-------------------------|
|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] nur verwenden, wenn keine Endpunktschutzanwendung eines Drittanbieters installiert ist<br /><br />Sie können [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] auf allen Computern verwenden, auf denen keine Endpunktschutzanwendung eines Drittanbieters installiert ist.|-   Endpoint Protection installieren = **Ja**<br />-   Endpoint Protection aktivieren = **Ja**<br />-   Endpoint Protection auch dann installieren, wenn eine Endpunktschutzanwendung von Drittanbietern installiert ist = **Nein**|Wenn die Endpunktschutzanwendung eines Drittanbieters erkannt wird, wird [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] nicht installiert. Eine bereits installierte Instanz wird deinstalliert.|
|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] verwenden, auch wenn eine Endpunktschutzanwendung eines Drittanbieters installiert ist<br /><br />Bei dieser Vorgehensweise führen Sie [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] und die Endpunktschutzanwendung des Drittanbieters (sofern installiert) gleichzeitig aus. Von einer solchen Konfiguration wird aufgrund möglicher Leistungsprobleme abgeraten.|-   Endpoint Protection installieren = **Ja**<br />-   Endpoint Protection aktivieren = **Ja**<br />-   Endpoint Protection auch dann installieren, wenn eine Endpunktschutzanwendung von Drittanbietern installiert ist = **Ja**|Zu verwenden in folgenden Fällen:<br /><br />-   Sie möchten zu [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] wechseln.<br />-   Sie stellen einen neuen Client bereit, der [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] verwendet.<br />-   Sie aktualisieren einen Client, der [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] verwendet.|
|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] ohne [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] verwenden<br /><br />In diesem Fall verwenden Sie [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] nicht zum Schutz Ihrer Computer vor Malware und Viren. Stattdessen greifen Sie auf die Endpunktschutzanwendung eines Drittanbieters zurück.|-   Endpoint Protection installieren = **Nein**|Wenn Sie keine Endpunktschutzanwendung eines Drittanbieters verwenden, wird von dieser Konfiguration abgeraten, denn in diesem Fall wären die Computer in Ihrer Organisation anfällig für Malware oder andere Angriffe.<br /><br />[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)] wird nicht installiert. Eine bereits installierte Instanz wird deinstalliert.|
Wenn Sie von Ihrer aktuellen Endpunktschutzanwendung zu [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)] wechseln möchten, verwenden Sie die folgende Schritte, die im Verlauf dieses Themas ausführlich erläutert werden:

1.  Beenden Sie Ihre aktuelle Endpunktschutzanwendung nicht, während Sie die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Clientsoftware auf den betreffenden Computern bereitstellen.

2.  Vergewissern Sie sich, dass [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] installiert ist und die Clientcomputer auf diese Weise abgesichert sind.

3.  Entfernen Sie die Endpunktschutzsoftware des Drittanbieters auf folgende Weise:

    -   Stellen Sie über die [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]-Softwareverteilung ein Tool des Herstellers der Endpunktschutzanwendung bereit, mit dessen Hilfe diese entfernt werden kann. Weitere Informationen finden Sie unter [Bereitstellen und Konfigurieren von Apps mit Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md).

    -   Entfernen Sie die von einem Drittanbieter stammende Endpunktschutzanwendung manuell.

> [!NOTE]
> Endpunktschutzanwendungen von Drittanbietern werden von [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nicht deinstalliert.

### <a name="BKMK_HowtoConf"></a>So konfigurieren Sie Microsoft Intune Endpoint Protection
Konfigurieren Sie mithilfe des folgenden Verfahrens [!INCLUDE[epshort](../Token/epshort_md.md)] für [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] kann [!INCLUDE[epshort](../Token/epshort_md.md)] für Windows 10 Technical Preview verwalten. Bestimmte Richtlinieneinstellungen sind nur für Windows 10 verfügbar.

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Richtlinie** &gt; **Richtlinie hinzufügen**.

2.  Konfigurieren Sie eine Richtlinie für **Microsoft Intune-Agent-Einstellungen** für die [!INCLUDE[epshort](../Token/epshort_md.md)]-Einstellungen, und stellen Sie sie bereit. Sie können die empfohlenen Einstellungen verwenden oder die Einstellungen anpassen. Weitere Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie im Thema [Allgemeine Aufgaben zur Verwaltung von Windows-PCs mit dem Microsoft Intune-Computerclient](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md).

    In den Tabellen unter dieser Vorgehensweise sind die Werte aufgeführt, die Sie in der Richtlinie konfigurieren können, sowie die empfohlenen Werte, die verwendet werden, wenn Sie die Richtlinie nicht anpassen. Sie finden diese Einstellungen im Bereich **Endpoint Protection**.

Sie können die bereitgestellte [!INCLUDE[epshort](../Token/epshort_md.md)]-Richtlinie auf der Seite **Alle Richtlinien** des Arbeitsbereichs **Richtlinie** anzeigen.

#### Endpoint Protection-Diensteinstellungen

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Endpoint Protection installieren**|Legen Sie hier **Ja** fest, um [!INCLUDE[epshort](../Token/epshort_md.md)] auf verwalteten Computern zu installieren. Wird während der Installation die Endpunktschutzanwendung eines Drittanbieters erkannt, dann wird [!INCLUDE[epshort](../Token/epshort_md.md)] nur dann installiert, wenn **Endpoint Protection auch dann installieren, wenn eine Endpunktschutzanwendung von Drittanbietern installiert ist** auf **Ja** festgelegt ist. **Note:** Intune [!INCLUDE[epshort](../Token/epshort_md.md)] wird auf verwalteten Computern standardmäßig installiert. Wenn Sie nicht möchten, dass [!INCLUDE[epshort](../Token/epshort_md.md)] auf Ihren verwalteten Computern installiert wird, müssen Sie diese Richtlinie explizit auf **Nein** festlegen. Wenn [!INCLUDE[epshort](../Token/epshort_md.md)] zuvor installiert war, und die Richtlinie wird auf **Nein** aktualisiert, so wird der [!INCLUDE[epshort](../Token/epshort_md.md)]-Client deinstalliert.<br />Empfohlener Wert: **Ja**|
|**Endpoint Protection auch dann installieren, wenn eine Endpunktschutzanwendung von Drittanbietern installiert ist**|Legen Sie hier **Ja** fest, um [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] auch dann zu installieren, wenn die Endpunktschutzanwendung eines Drittanbieters erkannt wird.<br /><br />Empfohlener Wert: **Ja**|
|**Aktivieren von Endpoint Protection**|Legen Sie hier **Ja** fest, um [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] auf Computern zu aktivieren, auf denen der [!INCLUDE[epshort](../Token/epshort_md.md)]-Client vorhanden ist.<br /><br />Wenn hier der Wert **Nein** festgelegt und [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] installiert ist, wird den Benutzern die Benutzeroberfläche des [!INCLUDE[epshort](../Token/epshort_md.md)]-Clients nicht angezeigt, und alle Schutzfunktionen sind inaktiv.<br /><br />Empfohlener Wert: **Ja**|
|**Clientbenutzeroberfläche deaktivieren**|Legen Sie hier **Ja** fest, um die Benutzeroberfläche des [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)]-Clients für Benutzer auszublenden. Damit die Einstellung wirksam wird, ist ein Neustart des Clientcomputers erforderlich.<br /><br />Empfohlener Wert: **Nein**|
|**Endpoint Protection auch dann installieren, wenn eine Endpunktschutzanwendung von Drittanbietern installiert ist**|Legen Sie hier **Ja** fest, um die Installation von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] auch dann zu erzwingen, wenn die Endpunktschutzanwendung eines Drittanbieters erkannt wird.<br /><br />Empfohlener Wert: **Nein**|
|**Vor der Entfernung von Malware einen Systemwiederherstellungspunkt erstellen**|Legen Sie hier **Ja** fest, um vor dem Entfernen von Malware einen Windows-Systemwiederherstellungspunkt zu erstellen.<br /><br />Empfohlener Wert: **Ja**|
|**Behandelte Malware nachverfolgen (Tage)**|Hiermit ist es [!INCLUDE[epshort](../Token/epshort_md.md)] möglich, erkannte Malware für einen festgelegten Zeitraum nachzuverfolgen, damit Sie vormals infizierte verwaltete Computer manuell überprüfen können.<br /><br />Sie können einen Wert zwischen 0 und 30 Tagen angeben.<br /><br />Empfohlener Wert: **7 Tage**|
Wenn Sie die Richtlinienwerte für **Endpoint Protection installieren** und **Endpoint Protection aktivieren** auf **Ja** sowie den Richtlinienwert für **Endpoint Protection auch dann installieren, wenn eine Endpunktschutzanwendung von Drittanbietern installiert ist** auf **Nein** festgelegt haben, wird die Installation einer anderen Endpunktschutzanwendung von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] erkannt. In diesem Fall wird die Installation nicht durchgeführt bzw. eine bereits vorhandene Instanz deinstalliert (allerdings werden von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] Angaben zur Integrität der anderen Endpunktschutzanwendung ermittelt und in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] angezeigt).

#### Einstellungen für den Echtzeitschutz

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Echtzeitschutz aktivieren**|Hiermit werden Überwachung und Überprüfung aller Dateien und Anwendungen aktiviert, auf die zugegriffen wird. Zudem werden schädliche Dateien oder Anwendungen blockiert, bevor sie auf Computern ausgeführt werden können.<br /><br />Empfohlener Wert: **Ja**|
|**Alle Downloads werden überprüft**|Hiermit wird die Überprüfung aller Dateien und Anhänge aktiviert, die aus dem Internet auf Clientcomputer heruntergeladen werden.<br /><br />Empfohlener Wert: **Ja**|
|**Datei- und Programmaktivität auf Computern überwachen**|Hiermit wird die Überwachung eingehender und ausgehender Dateien sowie von Programmaktivitäten auf Computern aktiviert. Mit dieser Einstellung wird von [!INCLUDE[epshort](../Token/epshort_md.md)] überwacht, wann die Ausführung von Dateien und Programmen beginnt, und Sie werden über alle Aktionen informiert, die von bzw. an ihnen durchgeführt werden.<br /><br />Empfohlener Wert: **Ja**|
|**Überwachte Dateien**|Wenn **Datei- und Programmaktivität auf Computern überwachen** aktiviert ist, ermöglicht es Ihnen diese Einstellung, auszuwählen, ob nur eingehende, nur ausgehende oder alle Dateien überwacht werden.<br /><br />Empfohlener Wert: **Alle Dateien überwachen**|
|**Aktivieren der Verhaltensüberwachung**|Hiermit können Clientcomputer von [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] auf bestimmte verdächtige Aktivitätsmuster geprüft werden.<br /><br />Empfohlener Wert: **Ja**|
|**Netzwerkinspektionssystem aktivieren**|Hiermit wird das Netzwerkinspektionssystem (NIS) auf Clientcomputern aktiviert. Im NIS werden Signaturen bekannter Sicherheitsrisiken aus dem [Microsoft Malware Protection Center (Microsoft Center zum Schutz vor Malware)](http://go.microsoft.com/fwlink/?LinkId=234249) verwendet, um schädlichen Netzwerkdatenverkehr zu erkennen und zu blockieren.<br /><br />Empfohlener Wert: **Ja**|

#### Einstellungen für den Überprüfungszeitplan

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Eine tägliche Schnellüberprüfung planen**|Hiermit wird eine tägliche Schnellüberprüfung von häufig verwendeten Dateien und wichtigen Systemdateien auf verwalteten Computern geplant. Diese Schnellüberprüfung wirkt sich geringfügig auf die Leistung aus.<br /><br />Empfohlener Wert: **Ja**|
|**Eine Schnellüberprüfung ausführen, wenn zwei aufeinander folgende Schnellüberprüfungen verpasst wurden**|Hiermit wird [!INCLUDE[epshort](../Token/epshort_md.md)] so konfiguriert, dass automatisch eine Schnellüberprüfung auf Computern ausgeführt wird, wenn bei diesen zwei aufeinanderfolgende geplante Schnellüberprüfungen verpasst wurden.<br /><br />Empfohlener Wert: **Ja**|
|**Vollständige Überprüfung planen**|Hiermit wird eine vollständige Überprüfung aller Dateien und Ressourcen auf den lokalen Festplatten der Computer konfiguriert. Diese Überprüfung kann einige Zeit in Anspruch nehmen und sich abhängig von der Anzahl der überprüften Dateien und Ressourcen auf die Computerleistung auswirken.<br /><br />Empfohlener Wert: **Nein**|
|**Eine vollständige Überprüfung ausführen, wenn zwei aufeinander folgende vollständige Überprüfungen verpasst wurden**|Hiermit wird [!INCLUDE[epshort](../Token/epshort_md.md)] so konfiguriert, dass automatisch eine vollständige Überprüfung auf Computern ausgeführt wird, wenn bei diesen zwei aufeinanderfolgende geplante vollständige Überprüfungen verpasst wurden.<br /><br />Empfohlener Wert: Nicht konfiguriert|

#### Einstellungen für Überprüfungsoptionen

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Nach der Installation von Endpoint Protection eine vollständige Überprüfung ausführen**|Hiermit wird [!INCLUDE[epshort](../Token/epshort_md.md)] so konfiguriert, dass nach der Installation auf Computern automatisch eine vollständige Systemüberprüfung durchgeführt wird. Um Auswirkungen auf die Benutzerproduktivität zu minimieren, wird diese Überprüfung nur ausgeführt, wenn sich die entsprechenden Computer im Leerlauf befinden.<br /><br />Empfohlener Wert: **Ja**|
|**Bei Bedarf automatisch eine vollständige Überprüfung nach der Beseitigung von Malware ausführen**|Legen Sie hier **Ja** fest, damit von [!INCLUDE[epshort](../Token/epshort_md.md)] nach dem Entfernen von Malware automatisch eine vollständige Systemüberprüfung auf Computern durchgeführt wird, um zu bestätigen, dass andere Dateien nicht betroffen waren.<br /><br />Empfohlener Wert: **Ja**|
|**Geplante Überprüfung nur starten, wenn sich der Computer im Leerlauf befindet**|Legen Sie hier **Ja** fest, um zu verhindern, dass geplante Überprüfungen auf Computern gestartet werden, während diese benutzt werden, und so eine Beeinträchtigung der Benutzerproduktivität zu vermeiden.<br /><br />Empfohlener Wert: **Ja**|
|**Vor dem Start der Überprüfung die aktuellsten Malwaredefinitionen abrufen**|Legen Sie hier **Ja** fest, um [!INCLUDE[epshort](../Token/epshort_md.md)] so zu konfigurieren, dass vor einer Überprüfung von Clientcomputern automatisch nach den neuesten Malwaredefinitionen gesucht wird.<br /><br />Empfohlener Wert: **Ja**|
|**Archivdateien überprüfen**|Legen Sie hier **Ja** fest, um [!INCLUDE[epshort](../Token/epshort_md.md)] so zu konfigurieren, dass Archivdateien wie ZIP- oder CAB-Dateien auf Computern auf Malware überprüft werden.<br /><br />Empfohlener Wert: **Nein**|
|**Scannen von E-Mail-Nachrichten**|Legen Sie hier **Ja** fest, um [!INCLUDE[epshort](../Token/epshort_md.md)] so zu konfigurieren, dass eingehende E-Mail-Nachrichten auf Computern überprüft werden.<br /><br />Empfohlener Wert: **Ja**|
|**Dateien überprüfen, die in freigegebenen Netzwerkordnern geöffnet wurden**|Legen Sie hier **Ja** fest, um [!INCLUDE[epshort](../Token/epshort_md.md)] zum Überprüfen von Dateien zu konfigurieren, die in freigegebenen Netzwerkordnern geöffnet werden. In der Regel sind dies Dateien, auf die über einen UNC-Pfad zugegriffen wird. Die Aktivierung dieser Funktion kann Benutzern Probleme bereiten, die nur über Lesezugriff verfügen, da sie Malware nicht entfernen können.<br /><br />Empfohlener Wert: **Nein**|
|**Zugeordnete Netzwerklaufwerke überprüfen**|Legen Sie hier **Ja** fest, um [!INCLUDE[epshort](../Token/epshort_md.md)] für das Überprüfen von Dateien auf zugeordneten Netzwerklaufwerken zu konfigurieren. Die Aktivierung dieser Funktion kann Benutzern Probleme bereiten, die nur über Lesezugriff verfügen, da sie Malware nicht entfernen können.<br /><br />Empfohlener Wert: **Nein**|
|**Wechseldatenträger überprüfen**|Legen Sie hier **Ja** fest, um [!INCLUDE[epshort](../Token/epshort_md.md)] für das Überprüfen von Wechseldatenträgern (z. B. USB-Flashlaufwerke) auf Malware und unerwünschte Software beim Ausführen einer vollständigen Überprüfung auf Computern zu konfigurieren.<br /><br />Empfohlener Wert: **Ja**|
|**Prozessornutzung während der Überprüfung begrenzen auf**|Hiermit wird der maximale Prozentsatz der Prozessornutzung festgelegt, der bei geplanten Überprüfungen auf Clientcomputern beansprucht werden darf. Sie können hierfür einen Wert zwischen 1 und 100 Prozent festlegen.<br /><br />Empfohlener Wert: **50 %**|

#### Standardeinstellungen für Aktionen

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Auswählen, wie von Endpoint Protection mit Malware der folgenden Warnstufen verfahren werden soll**|Hiermit wird die Standardaktion angegeben, die von [!INCLUDE[epshort](../Token/epshort_md.md)] durchgeführt wird, wenn Malware verschiedener Warnstufen erkannt wird.<br /><br />Sie können für jede Warnstufe festlegen, dass die Malware entfernt oder in Quarantäne versetzt oder die von Microsoft empfohlene Aktion ausgeführt wird.<br /><br />Empfohlener Wert: **Empfohlene Aktion**|

#### Einstellungen für ausgeschlossene Dateien und Ordner

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Von der Überprüfung oder dem Echtzeitschutz auszuschließende Dateien und Ordner**|Hiermit können Sie auf Computern bestimmte Dateien oder Ordner von der Überprüfung oder vom Echtzeitschutz ausschließen.|

#### Einstellungen für ausgeschlossene Prozesse

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Prozesse, die beim Ausführen einer Überprüfung oder bei Verwendung des Echtzeitschutzes auszuschließen sind**|Hiermit können Sie bestimmte Prozesse von der Überprüfung oder vom Echtzeitschutz ausschließen. Sie können nur Dateien mit der Erweiterung **.exe**, **.com** oder **.scr** ausschließen.|

#### Einstellungen für ausgeschlossene Dateitypen

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Dateierweiterungen, die beim Ausführen einer Überprüfung oder bei Verwendung des Echtzeitschutzes auszuschließen sind**|Hiermit können Sie auf Computern bestimmte Dateinamenserweiterungen von der Überprüfung oder vom Echtzeitschutz ausschließen.|

#### Einstellungen für Microsoft Active Protection Service
Microsoft Active Protection Service ist eine Online-Community, die Ihnen hilft zu entscheiden, wie Sie auf potenzielle Bedrohungen reagieren. Diese Community trägt auch dazu bei, die Weiterverbreitung neuer Infektionen mit Malware zu unterbinden.

|Richtlinieneinstellung|Weitere Informationen|
|--------------------------|-------------------------|
|**Microsoft Active Protection Service beitreten**|Bei **Ja** werden automatisch Informationen zu erkannter Malware an den Microsoft Active Protection Service gesendet. Microsoft verwendet die auf diese Weise erfassten Informationen nicht, um Sie zu identifizieren oder mit Ihnen Kontakt aufzunehmen.<br /><br />Empfohlener Wert: **Ja**|
|**Mitgliedschaftsebene**|Wenn Sie sich dafür entschieden haben, dem Microsoft Active Protection Service beizutreten, können Sie über diese Einstellung eine der folgenden Mitgliedschaftsebenen auswählen:<br /><br />-   **Einfach:** Hierbei werden grundlegende Informationen zu erkannter Malware an Microsoft gesendet. Hierzu gehören Angaben dazu, woher die Software stammt, welche Aktionen Sie anwenden oder von [!INCLUDE[epshort](../Token/epshort_md.md)] automatisch angewendet werden, und ob diese Aktionen erfolgreich waren.<br />-   **Premium:** Hierbei werden zusätzliche Informationen über Malware, Spyware oder möglicherweise unerwünschte Software an Microsoft gesendet. Hierzu gehören Angaben zu dem Speicherort der Software, den Dateinamen, der Funktionsweise der Software und der Auswirkung der Software auf Ihren Computer.<br /><br />Empfohlener Wert: **Erweitert**|
|**Dynamische Definitionen auf Basis von Microsoft Active Protection Service-Berichten empfangen**|Bei **Ja** werden von Computern dynamische Malwaredefinitionen empfangen, die auf Informationen über erkannte Malware basieren, die von [!INCLUDE[epshort](../Token/epshort_md.md)] an den Microsoft Active Protection Service übermittelt werden.<br /><br />Empfohlener Wert: **Ja**|

### Verwaltungsaufgaben für Endpoint Protection
Mithilfe der folgenden Aufgaben können Sie verschiedene Verwaltungsaufgaben auf verwalteten Computern ausführen, auf denen [!INCLUDE[epshort](../Token/epshort_md.md)] ausgeführt wird.

|Ziel:|Über die [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]-Konsole|Auf dem verwalteten Computer|
|---------|--------------------------------------------------------------------------|--------------------------------|
|Update für Malwaredefinitionen ausführen|Wählen Sie im Arbeitsbereich **Gruppen** die zu aktualisierenden Computer aus.<br /><br />Klicken Sie auf **Remoteaufgaben** &gt; **Update für Malwaredefinitionen ausführen**.|Starten Sie die [!INCLUDE[epshort](../Token/epshort_md.md)]-Clientsoftware über den Windows-Benachrichtigungsbereich.<br /><br />Klicken Sie zunächst auf die Registerkarte **Aktualisieren** und dann auf **Aktualisieren**.|
|Malwareüberprüfung ausführen|Wählen Sie im Arbeitsbereich **Gruppen** die zu überprüfenden Computer aus.<br /><br />Klicken Sie auf **Vollständige Malwareüberprüfung ausführen** oder auf **Malwareschnellüberprüfung ausführen**.|Starten Sie die [!INCLUDE[epshort](../Token/epshort_md.md)]-Clientsoftware über den Windows-Benachrichtigungsbereich.<br /><br />Wählen Sie **Schnell**, **Vollständig** oder **Benutzerdefiniert** aus, und klicken Sie auf **Jetzt überprüfen**.|
Zur Anzeige des Status einer Remoteaufgabe klicken Sie auf den Link **Remoteaufgaben** unten rechts in der [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

Im Dialogfeld **Status des Remote-Tasks** werden aktuelle Remoteaufgaben, ihr Status, der Gerätename und etwaige berichtete Fehler ggf. mit einem Link zu Problembehandlungsinformationen aufgelistet.

### <a name="BKMK_SCEPmon"></a>So überwachen Sie Endpoint Protection
Sie können den Malwarestatus Ihrer Computer mithilfe des Arbeitsbereichs **Schutz** der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) überwachen. Dieser Arbeitsbereich enthält zwei Seiten:

|Name der Seite|Weitere Informationen|
|------------------|-------------------------|
|**Übersicht über Endpoint Protection**|Hier werden wichtige Probleme als Links angezeigt, die Sie anklicken können, um weitere Informationen zu erhalten. Die folgenden Arten von Problemen können angezeigt werden:<br /><br />-   **Malwareinstanzen, die Nachverfolgung erfordern:** Klicken Sie auf den Link, um eine Liste mit Malwareproblemen sowie den zur Lösung des jeweiligen Problems erforderlichen Folgemaßnahmen anzuzeigen. Sie können sich über diese Liste auch anzeigen lassen, welche Computer betroffen sind.<br />-   **Computer mit Malware, die Nachverfolgung erfordern:** Klicken Sie auf den Link, um alle Computer mit ungelösten Malwareproblemen sowie den zur Lösung des jeweiligen Problems erforderlichen Folgemaßnahmen anzuzeigen.<br />-   **Ungeschützte Geräte:** Klicken Sie auf den Link, um Computer anzuzeigen, die von keiner Endpunktschutzsoftware geschützt sind, weil eine solche Software entweder nicht installiert ist, oder weil ein Fehler aufgetreten ist. Wählen Sie einen Computer aus, um weitere Details anzuzeigen.<br />-   **Geräte, auf denen eine andere Endpunktschutzanwendung ausgeführt wird:** Klicken Sie auf den Link, um Computer anzuzeigen, auf denen die Endpunktschutzanwendung eines Drittanbieters ausgeführt wird.|
|**Sämtliche Malware**|Hiermit wird eine Liste der gesamten auf Ihren Computern gefundenen aktiven Malware angezeigt. Sie können sich über diese Liste auch alle Computer anzeigen lassen, die von einer bestimmten Malware betroffen sind, oder eine der folgenden Aufgaben auswählen:<br /><br />-   **Eigenschaften anzeigen**: Es wird eine Seite mit weiteren Informationen zur ausgewählten Schadsoftware geöffnet.<br />-   **Informationen zu dieser Malware**: Es wird ein Thema aus dem Microsoft Center zum Schutz vor Malware mit weiteren Informationen zur Schadsoftware geöffnet.|
> [!IMPORTANT]
> Der Arbeitsbereich **Schutz** wird in der Administratorkonsole erst angezeigt, wenn Sie den Client installiert haben und Sie mindestens einen Computerclient erfolgreich verwalten.

### Anzeigen der letzten Erkennungspfade für Malware auf Computern
Intune kann die Pfade der 10 zuletzt erkannten Instanzen von Malware auf einem Gerät anzeigen. Die Option **Letzter Erkennungspfad** ist standardmäßig deaktiviert. So aktivieren Sie diese Anzeige:

##### Aktivieren letzter Erkennungspfade für Malware

1.  Klicken Sie in der [Microsoft Intune-Verwaltungskonsole](https://manage.microsoft.com/) auf **Gruppen** &gt; **Alle Geräte**.**Malware**.

2.  Klicken Sie mit der rechten Maustaste auf eine Spaltenüberschrift. Eine Liste der verfügbaren Spalten wird angezeigt.

3.  Aktivieren Sie das Kontrollkästchen **Letzte Erkennungspfade** in der Liste. Die Spalte **Letzte Erkennungspfade** wird angezeigt. Sie enthält bis zu 10 der zuletzt auf dem Gerät überwachten Malwareinstanzen.

## Benötigen Sie weitere Hilfe?
Weitere Hilfe und weiteren Support finden Sie unter [Problembehandlung für Endpoint Protection in Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

## Siehe auch
[Verwalten von Windows-PCs mit Microsoft Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

