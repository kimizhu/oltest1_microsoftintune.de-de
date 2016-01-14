---
description: na
keywords: na
title: Get started with a paid subscription to Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: d158503c-1276-422b-ab81-5f66c1cd7e7a
---
# Erste Schritte mit einem kostenpflichtigen Abonnement in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f716ac2d78f1254442bfc407cc38bfab" id="tgt1" class="tgtSentence">Microsoft Intune bietet Ihnen eine schnelle und einfache Möglichkeit zur Verwaltung von mobilen Geräten und Computern in Ihrem Unternehmen, unabhängig davon, ob Sie mit einer kostenlosen 30-Tage-Testversion oder einem kostenpflichtigen Abonnement starten.</caps:sentence>
          <caps:sentence sentenceid="f629f2897971d13568d8158121caf8ac" id="tgt2" class="tgtSentence"> In diesem Abschnitt werden Sie durch die Schritte bei der Einrichtung einer rein cloudbasierten Instanz von <token>wit_firstref</token> geleitet.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3f0f8eb313c35054af8f3ebd9d440f41" id="tgt3" class="tgtSentence">Wenn Sie in einem berechtigenden Plan mindestens 150 Lizenzen für Microsoft Intune erwerben, können Sie das „FastTrack Center-Leistungsangebot“ nutzen, einen Dienst, bei dem Microsoft-Spezialisten Sie bei der Vorbereitung Ihrer Umgebung für Intune unterstützen.</caps:sentence>
          <caps:sentence sentenceid="78876cede6e051df998fab51465986f4" id="tgt4" class="tgtSentence"> Siehe auch <externalLink><linkText>Microsoft Intune-Servicevorteil – Beschreibung</linkText><linkUri>https://technet.microsoft.com/library/mt228265.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ea698d75c36b5ddbb573fc590c2af6cc" id="tgt5" class="tgtSentence">Die ersten Schritte bei einem kostenpflichtigen Abonnement sind in vielen Punkten mit den ersten Schritten bei einer <externalLink><linkText>kostenlosen 30-Tage-Testversion</linkText><linkUri>https://technet.microsoft.com/library/dn646983.aspx</linkUri></externalLink> identisch.</caps:sentence>
          <caps:sentence sentenceid="f3f430b0b4fe1db481cbaa14fdd71084" id="tgt6" class="tgtSentence"> In diesem Thema werden jedoch auch einige zusätzliche Bereiche behandelt, die von den meisten Benutzern bei der Bereitstellung von Testversionen nicht behandelt werden müssen. Dazu zählen die folgenden Bereiche:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="52a34a138cdcc2644f1307c4de8b8000" id="tgt7" class="tgtSentence">Synchronisieren von lokalen Active Directory-Konten mit Intune und Azure Active Directory</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="d3f0a480853d2966263d63731527f2d0" id="tgt8" class="tgtSentence">Überlegungen zu Domänen- und DNS-Diensten</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8241b7ab6a781cdd9624c64f1d850f06" id="tgt9" class="tgtSentence">Anpassen von Intune-Features für die Produktion</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="e687519a6c776c73d43fb8b9d7a5c876" id="tgt10" class="tgtSentence">Dieses Thema konzentriert sich auf die Konfiguration von Intune als eigenständigen Dienst.</caps:sentence>
            <caps:sentence sentenceid="7f03ec9164a857655b9a6d07248aef1b" id="tgt11" class="tgtSentence"> Wenn Sie derzeit Microsoft System Center Configuration Manager (ConfigMgr) zum Verwalten von Computern und Servern verwenden, können Sie Intune in einer Hybridbereitstellung mit ConfigMgr verbinden.</caps:sentence>
            <caps:sentence sentenceid="2fa8229e6b356ee32674f426b14afaaf" id="tgt12" class="tgtSentence"> Diese Konfiguration bietet verschiedene Vorteile und nutzt die vorhandene lokale Infrastruktur.</caps:sentence>
            <caps:sentence sentenceid="78876cede6e051df998fab51465986f4" id="tgt13" class="tgtSentence"> Weitere Informationen zu Hybridbereitstellungen mit Intune und ConfigMgr finden Sie unter <externalLink><linkText>Verwalten von mobilen Geräten mit dem Konfigurations-Manager und Microsoft Intune</linkText><linkUri>https://technet.microsoft.com/library/jj884158.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="9cfdb68e3099bd19e0667068a62a3ece" id="tgt14" class="tgtSentence">Vorbereitung</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="165d88c34b9d265d5f73fddef049af59" id="tgt15" class="tgtSentence">Wenn Sie mit einem kostenpflichtigen Abonnement beginnen, bedeutet dies, dass Sie eine <externalLink><linkText>Intune-Testversion abgeschlossen</linkText><linkUri>https://technet.microsoft.com/library/dn646983.aspx</linkUri></externalLink> haben und jetzt bereit sind, Intune bereitzustellen und Änderungen an Ihrer vorhandenen Netzwerkinfrastruktur vorzunehmen.</caps:sentence>
            <caps:sentence sentenceid="173b915621468b19e0d19a028b100f76" id="tgt16" class="tgtSentence"> Dies könnte das einfache Hinzufügen oder Aktualisieren Ihrer internen und externen DNS-Einträge umfassen, um Ihre vorhandenen Active Directory-Konten mit Azure Active Directory zu verbinden.</caps:sentence>
            <caps:sentence sentenceid="9dc1e0636c4c182bdca7ad102ca05e9d" id="tgt17" class="tgtSentence"> Unabhängig von der Kombination von Intune-Features zur Verwaltung mobiler Geräte, die Sie nutzen, müssen Sie sorgfältig planen, wie Intune mit Ihren vorhandenen Netzwerkkomponenten und Diensten interagiert.</caps:sentence>
            <caps:sentence sentenceid="427367f1bbdf1e7f2aff966210759a0e" id="tgt18" class="tgtSentence"> Insbesondere sollten Sie Folgendes überprüfen:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="a733612084a65afc1788c44f0d3c7634" id="tgt19" class="tgtSentence">
                  <legacyBold>Verwalten von Benutzeridentitäten</legacyBold>: Für die meisten mittelgroßen und großen Unternehmen stellt die Verbindung ihrer vorhandenen Verzeichnisdienste mit Intune über Azure Active Directory die beste und einfachste Methode dar, um die Benutzeridentität mit Intune zu verwalten.</caps:sentence>
                <caps:sentence sentenceid="7a06feeb6d075547cef74e7d2462ea82" id="tgt20" class="tgtSentence"> Dies gilt insbesondere dann, wenn Sie bereits andere Microsoft Cloud Services wie Office 365 und Exchange Online verwenden.</caps:sentence>
                <caps:sentence sentenceid="be1773f1672a72c73e5252317fea8a9c" id="tgt21" class="tgtSentence"> Das Synchronisieren Ihrer vorhandenen Benutzerkonten mit <externalLink><linkText>Microsoft AD Connect</linkText><linkUri>https://www.microsoft.com/download/details.aspx?id=47594</linkUri></externalLink> ist eine schnelle und einfache Möglichkeit, um Ihr lokales Active Directory mit Azure Active Directory zu verbinden und eine Einmalanmeldungsauthentifizierung für Ihre Benutzer zu konfigurieren.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1a600e16f64bbf2729b68547041b719b" id="tgt22" class="tgtSentence">
                  <legacyBold>Auswirkungen auf DNS</legacyBold>: Wenn Sie Ihren eigenen Domänennamen anstelle der Standarddomäne „onmicrosoft.com“ verwenden möchten, die vom Intune-Dienst erstellt wird, sind einige Aktualisierungen öffentlicher DNS-Einträge erforderlich, wenn Sie Azure (oder andere Microsoft Cloud Services) für die Verwendung Ihrer benutzerdefinierten Domäne konfigurieren.</caps:sentence>
                <caps:sentence sentenceid="917458e5c5305b3278d428fc0d3d52e9" id="tgt23" class="tgtSentence"> DNS-Einträge sind erforderlich, damit der Intune-Dienst von mobilen Geräten gefunden werden kann. Zudem sorgen sie dafür, dass andere Dienste zur Verwaltung der Mobilität ordnungsgemäß funktionieren.</caps:sentence>
                <caps:sentence sentenceid="83105d1019e4891b10c085da09e8c030" id="tgt24" class="tgtSentence"> Sie müssen entscheiden, ob Ihre DNS-Einträge auf dem DNS-Host verwaltet werden oder die DNS-Einträge für Ihre Domäne von Azure oder Office 365 erstellt und verwaltet werden, nachdem Sie die DNS-Einträge geändert haben, damit diese auf die entsprechenden Dienste verweisen.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ae7ed9d1fdf39520344565eee2483ddf" id="tgt25" class="tgtSentence">Bereit für die ersten Schritte?</caps:sentence>
            <caps:sentence sentenceid="3d9184f658e4cbb1cb7fe373692d2ac0" id="tgt26" class="tgtSentence"> Folgendes ist beim Starten eines kostenpflichtigen Abonnements von Intune erforderlich:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="99ed1cdd7c99b12a08652a5e99f536d5" id="tgt27" class="tgtSentence">
           Ein Gerät mit einem Silverlight-fähigen Webbrowser, mit dessen Hilfe Sie auf die Websites zugreifen können, auf denen Sie Intune-Benutzerkonten erstellen (<embeddedLabel>Intune-Kontenportal</embeddedLabel>) sowie Geräte, Gruppen und Richtlinien verwalten (<embeddedLabel>Intune-Verwaltungskonsole</embeddedLabel>) können.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ae4a092776f33b41b5f62754fae60078" id="tgt28" class="tgtSentence">
           Ein zweites Gerät mit einem Webbrowser, über das Sie auf das Unternehmensportal zugreifen können. So sehen Sie, wie die meisten <token>wit_nextref</token>-Benutzer ihre Geräte registrieren und verwalten, Software suchen und installieren und Hilfe bei Administratoren anfordern.</caps:sentence>
                <caps:sentence sentenceid="e790e06e10502d78be5d26232fae24a7" id="tgt29" class="tgtSentence"> Statt ein zweites Gerät mit einem Webbrowser zu verwenden, können Sie in dem Browser, den Sie zur Verwaltung von <token>wit_nextref</token> verwenden, auch den Datenschutzmodus aktivieren. In Internet Explorer beispielsweise klicken Sie hierzu auf <ui>Extras</ui> &gt; <ui>InPrivate-Browsen</ui>).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2bd64bd32056072ed36e6355b94da5ea" id="tgt30" class="tgtSentence">
           Wenn Sie über ein vorhandenes Microsoft Online Services-Konto verfügen, dann benötigen Sie die Anmeldeinformationen des Administrators für dieses Konto.</caps:sentence>
                <caps:sentence sentenceid="2bdb2fb7025750b72bb4b52df58b2ccf" id="tgt31" class="tgtSentence"> Wenn Sie nicht über ein solches Konto verfügen oder diesen Intune-Mandanten nur zu Evaluierungszwecken verwenden möchten, dann benötigen Sie keine Anmeldeinformationen des Mandantenadministrators.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="84f0adeb04f20986d1e19791b19fcc7f" id="tgt32" class="tgtSentence">
           Wenn Sie iOS- oder Windows Phone-Geräte mit Intune verwalten möchten, benötigen Sie Zertifikate (oder Schlüssel) und Konten, um diese Zertifikate abzurufen.</caps:sentence>
                <caps:sentence sentenceid="640b90b4e79487a5c7fe24cd37e44c0b" id="tgt33" class="tgtSentence"> Für Android-Geräte sind keine zusätzlichen Zertifikate erforderlich:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt34" class="tgtSentence">Plattform</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ab3259eabfda655690d59aefca17f756" id="tgt35" class="tgtSentence">Zertifikatanforderungen</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt36" class="tgtSentence">Weitere Informationen</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="29777c09c4d10e222863eca49091ebc0" id="tgt37" class="tgtSentence">
                   Windows Phone 8.1 und <token>winphone8_client_1</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6bda7521bfb63aa1a7c28522c299b612" id="tgt38" class="tgtSentence">Für Benutzer von Windows Phone 8.1, die die Unternehmensportal-App über den Store installieren, ist kein Zertifikat erforderlich.</caps:sentence>
                        <caps:sentence sentenceid="661da19850cf36eac8aca5e39277c5c7" id="tgt39" class="tgtSentence"> Für Windows Phone 8.0 oder zur Verwendung von Intune zum Bereitstellen der Unternehmensportal-App auf Windows Phone 8.1-Geräten ist ein Symantec-Zertifikat erforderlich.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e3aaba704845ef99a933ccf191dd787d" id="tgt40" class="tgtSentence">In dieser Anleitung wird davon ausgegangen, dass Ihre Benutzer die Unternehmensportal-App aus dem Store auf ein Gerät mit Windows Phone 8.1 oder höher abrufen.</caps:sentence>
                        <caps:sentence sentenceid="0f7aaa2f2b6fd4bb3d9a817353983744" id="tgt41" class="tgtSentence"> Weitere Informationen zur Unterstützung von Windows Phone 8.0 finden Sie unter <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Set up Windows Phone management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="595077e2c36638f388814d08152b719a" id="tgt42" class="tgtSentence">
                  Geräte mit Windows 10, <token>winblue_winrt_2</token>, <token>win8RT_client_1</token> oder <token>winblue_client_2</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1f3406931ab09b76a2c74533fc93f405" id="tgt43" class="tgtSentence">Es bestehen keine Zertifikatanforderungen beim Registrieren von Geräten mit Windows RT und Windows.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5058f1af8388633f609cadb75a75dc9d" id="tgt44" class="tgtSentence">
                          <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be Managed by Intune</link>.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="da5d01ccbd98496aea51cdbbae671f59" id="tgt45" class="tgtSentence">iOS oder Mac OS X</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b134f6982d0432a26f914236c233fc7b" id="tgt46" class="tgtSentence">Beziehen Sie ein Apple Push Notification Service-Zertifikat.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5a7cf9300c87d3ef6ebde83a702220fb" id="tgt47" class="tgtSentence">Fordern Sie ein Apple Push Notification Service-Zertifikat bei Apple an, wie hier beschrieben: <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Start managing iOS devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </listItem>
          </list>
        </content>
      </section>
      <section address="Step1" expanded="true">
        <title>
          <caps:sentence sentenceid="6bcead0b46c85aca93b67ef043f48453" id="tgt48" class="tgtSentence">Schritt 1: Registrieren oder Anmelden bei Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="300ab4a1dadb2e2153532043d8f86fa2" id="tgt49" class="tgtSentence">Berücksichtigen Sie Folgendes, bevor Sie sich bei Intune registrieren oder anmelden:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f8f79359e30aec95ee5f62ea542e076a" id="tgt50" class="tgtSentence">Ob Ihr Unternehmen bereits über ein Geschäfts- oder Schulkonto für Microsoft Online Services verfügt</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="dad666cfe971b6a07310989948a1c7dd" id="tgt51" class="tgtSentence">Ob Sie über ein Enterprise Agreement oder einen vergleichbaren Volumenlizenzvertrag mit Microsoft verfügen</caps:sentence>
              </para>
            </listItem>
          </list>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aca6632ac0524c927acaf39d3afec2f4" id="tgt52" class="tgtSentence">Registrieren Sie sich für ein neues Konto, wenn eine der folgenden Aussagen zutrifft:</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa5299cbcad6f25505650f207bd9d3af" id="tgt53" class="tgtSentence">Melden Sie sich mit Ihrem Geschäfts- oder Schulkonto an, wenn Folgendes zutrifft:</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4e7727ae8c8b925ee9705bc11067aab4" id="tgt54" class="tgtSentence">
                          <embeddedLabel>Sie besitzen kein Geschäfts- oder Schulkonto.</embeddedLabel> Ein Geschäfts- oder Schulkonto wird bereitgestellt, wenn Sie einen Volumenlizenzvertrag mit Microsoft abschließen oder Office 365 abonnieren.</caps:sentence>
                        <caps:sentence sentenceid="e97b0125d9352822ba0a00f688d4c6f6" id="tgt55" class="tgtSentence"> Wenn Ihre Organisation kein Enterprise Agreement oder keinen entsprechenden Volumenlizenzvertrag mit Microsoft abgeschlossen hat (oder nicht über ein Office 365-Konto verfügt), verfügen Sie nicht über ein Microsoft Online Services-Konto, mit dem Sie sich bei Microsoft Online Services anmelden können.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ba5573358da7ed1e06edc1a8aef7b23e" id="tgt56" class="tgtSentence">
                          <embeddedLabel>Sie verwerfen Ihren Intune-Mandanten nach Abschluss der 30-Tage-Testversion.</embeddedLabel> Wenn Sie Ihr kostenloses <token>wit_nextref</token>-Testabonnement nur zu Evaluierungszwecken nutzen und beabsichtigen, die Einrichtung des <token>wit_nextref</token>-Dienstes und die Gerätebereitstellung nach der Testversion erneut durchzuführen, sollten Sie ein neues Konto registrieren.</caps:sentence>
                        <caps:sentence sentenceid="263586ad67d631b089612d62738606a4" id="tgt57" class="tgtSentence"> Dies ist die empfohlene Option, wenn Sie planen, <token>wit_nextref</token> mit System Center 2012 Configuration Manager zu verwenden.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="985da9f53d3ceb9576fa782f2e2b32cc" id="tgt58" class="tgtSentence">Wenn Sie ein neues Konto registrieren, können Sie zum Verwalten dieses Kontos kein vorhandenes Arbeits- oder Schulkonto mehr verwenden und es auch nicht mehr mit vorhandenen Volumenlizenzverträgen kombinieren.</caps:sentence>
                    </para>
                  </alert>
                  <para></para>
                </TD>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="3992510defc50f1858f7fc797c863e36" id="tgt59" class="tgtSentence">Sie verfügen über ein Geschäfts- oder Schulkonto, das über einen Volumenlizenzvertrag oder über ein Office 365-Abonnement bereitgestellt wurde, und verwenden diese Testversion zur Auswertung von <token>wit_nextref</token>.</caps:sentence>
                    </embeddedLabel>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="90e4a1a311adce28bd2c892a0c552fc1" id="tgt60" class="tgtSentence">Wenn Sie <token>wit_nextref</token> für ein vorhandenes Konto einrichten, wird empfohlen, dass Sie sich <link xlink:href="3b4e778d-ac13-4c23-974f-5122f74626bc">Configure Microsoft Intune</link> ansehen, bevor Sie den Vorgang mit diesen Schritten fortsetzen.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
            </tbody>
          </table>
          <procedure address="BKMK_ToSignUpforSubscription" expanded="true">
            <title>
              <caps:sentence sentenceid="3555133b92fda8c56521d00deb443335" id="tgt61" class="tgtSentence">Registrieren oder Anmelden bei Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="11326bf9695e7dbca512166e2b4d695b" id="tgt62" class="tgtSentence">
                      <externalLink>
                        <linkText>Klicken Sie zunächst hier, um zur Intune-Anmeldeseite zu gelangen.</linkText>
                        <linkUri>https://portal.office.com/Signup/Signup.aspx?OfferId=40BE278A-DFD1-470a-9EF7-9F2596EA7FF9&amp;dl=INTUNE_A&amp;ali=1#0 </linkUri>
                      </externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt63" class="tgtSentence">Sie können sich auf der Seite <ui>Registrieren</ui> anmelden oder registrieren.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="dc92e8cecf74b08b0b6e54f936a4149a" id="tgt64" class="tgtSentence">Wenn Sie die Registrierung abgeschlossen haben, werden Sie mit dem Mandantenadministratorkonto automatisch am <token>wit_icp_1</token> angemeldet.</caps:sentence>
                  <caps:sentence sentenceid="633dd09852763b5e45ff3c99d1d76a45" id="tgt65" class="tgtSentence"> Zudem wird eine E-Mail mit Ihren Kontoinformationen an die von Ihnen bei der Registrierung angegebene E-Mail-Adresse gesendet.</caps:sentence>
                  <caps:sentence sentenceid="22c6546b4a09911ac81795315c83f234" id="tgt66" class="tgtSentence"> Diese E-Mail bestätigt, dass Ihr Abonnement aktiv ist.</caps:sentence>
                  <caps:sentence sentenceid="11d3cf0f8c18164870d00e474a728f2a" id="tgt67" class="tgtSentence"> Wenn Sie sich anmelden, werden Sie automatisch zum Intune-Verwaltungsportal weitergeleitet.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ConfigureDomain">
        <title>
          <caps:sentence sentenceid="f843400d1cab1ef7e3bbc6d1e5d5e4dc" id="tgt68" class="tgtSentence">Schritt 2: Konfigurieren eines benutzerdefinierten Domänennamens</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e6dcdb79d138fe36d54b44d6d9d8cc9c" id="tgt69" class="tgtSentence">Standardmäßig wird von <token>wit_firstref</token> der Domänenname, den Sie beim Abonnieren des Dienstes ausgewählt haben, im Format <ui>&lt;Domäne&gt;.onmicrosoft.com</ui> verwendet.</caps:sentence>
            <caps:sentence sentenceid="77d29f97a224183330cdf5e28b6c9006" id="tgt70" class="tgtSentence"> Verfügt Ihre Organisation über eine eigene Domäne, dann können Sie Ihre <token>wit_nextref</token>-Instanz so konfigurieren, dass diese Domäne anstelle des bei der Einrichtung Ihres Abonnements angegebenen Domännennamens verwendet wird.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1f36783cd8fb1206de9382e358371134" id="tgt71" class="tgtSentence">Bevor Sie neue Benutzerkonten erstellen oder Kunden aus ihrem lokalen Active Directory synchronisieren, wird dringend empfohlen, dass Sie entscheiden, ob nur die .onmicrosoft.com-Domäne verwendet oder benutzerdefinierte Domänennamen hinzugefügt werden sollen.</caps:sentence>
            <caps:sentence sentenceid="9f5a5e7884f2d356ae84b03bdca1bc7f" id="tgt72" class="tgtSentence"> Wenn Sie keinen benutzerdefinierten Domänennamen mit Suffix konfigurieren, wird bei jedem importierten Benutzerkonto lediglich das Suffix „onmicrosoft.com“ für den Benutzerprinzipalnamen (UPN) verwendet.</caps:sentence>
            <caps:sentence sentenceid="b4e8dd211da65725cb3f6caf5fab0643" id="tgt73" class="tgtSentence"> Das Konfigurieren einer benutzerdefinierten Domäne vor dem Hinzufügen von Benutzern kann die Verwaltung von Benutzeridentitäten für Ihr Abonnement vereinfachen, denn die Benutzer werden auf diese Weise in die Lage versetzt, sich mit den Anmeldeinformationen anzumelden, mit denen sie auch auf andere Domänenressourcen zugreifen.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8c09db1482cf73766a199138c36f06a4" id="tgt74" class="tgtSentence">Die Aufgaben beim Konfigurieren von <token>wit_nextref</token> zum Verwenden des benutzerdefinierten Domänennamens Ihrer Organisation sind identisch mit denen bei den anderen Azure AD-Mandanten. Orientieren Sie sich daher an den Informationen und Verfahren unter <externalLink><linkText>Hinzufügen Ihrer Domäne</linkText><linkUri>http://technet.microsoft.com/library/hh969247.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0a4e5fa97d40710bd3b16744cbaab497" id="tgt75" class="tgtSentence">Weitere Informationen zum Verwenden Ihrer benutzerdefinierten Domäne mit einem cloudbasierten Dienst von Microsoft finden Sie unter <externalLink><linkText>Internetdomänen</linkText><linkUri>http://technet.microsoft.com/library/hh969248.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="9052be419f45fc5869c4f10e199e6399" id="tgt76" class="tgtSentence">Wenn Sie einen cloudbasierten Dienst von Microsoft abonnieren, wird Ihre Instanz dieses Diensts zu einem Mandanten von Microsoft Azure Active Directory (Azure AD), durch das Identitäts- und Verzeichnisdienste für Ihren cloudbasierten Dienst bereitgestellt werden.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="d3dec703138771807e7b767d293a65ea" id="tgt77" class="tgtSentence">Weitere Informationen zu Ihrem Azure AD-Mandanten finden Sie unter <externalLink><linkText>Was ist ein Windows Azure AD-Mandant?</linkText><linkUri>http://technet.microsoft.com/library/jj573650.aspx</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section address="BKMK_SyncUsersFromAD">
        <title>
          <caps:sentence sentenceid="5045607049949c0d397006d501b46353" id="tgt78" class="tgtSentence">Schritt 3: Synchronisieren von Active Directory und Hinzufügen von Benutzern zu Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="231a8e7d7351b92281c8ca02e46b2abd" id="tgt79" class="tgtSentence">Wie bereits erwähnt, können Sie die Verzeichnissynchronisierung so konfigurieren, dass Benutzerkonten aus Ihrem lokalen Active Directory in Microsoft Azure Active Directory importiert werden.</caps:sentence>
            <caps:sentence sentenceid="181d133f3de6eb68931d1dfe9a58f135" id="tgt80" class="tgtSentence"> Darüber hinaus aktivieren Sie dieses Feature für alle Microsoft Cloud Services, die Sie abonniert haben, wenn Sie die Active Directory-Synchronisierung für Ihren Intune-Mandanten aktivieren.</caps:sentence>
            <caps:sentence sentenceid="ee56b69c4896f58c791a32b9c0a2bbc1" id="tgt81" class="tgtSentence"> Wenn Sie mit dem gleichen Azure AD mehrere Dienste verwenden, stehen die synchronisierten Benutzerkonten jedem cloudbasierten Dienst zur Verfügung, von dem Ihr Azure AD verwendet wird.</caps:sentence>
            <caps:sentence sentenceid="7639c939e65ad36c40f5f998cc768ec3" id="tgt82" class="tgtSentence"> Wenn Ihr lokaler Active Directory-Dienst mit all Ihren Azure Active Directory-basierten Diensten verbunden ist, gestaltet sich die Verwaltung der Benutzeridentität viel einfacher.</caps:sentence>
            <caps:sentence sentenceid="2adb1a8107fdcc2bf1a4532a6990810e" id="tgt83" class="tgtSentence"> Sie können auch Features für die einmalige Anmeldung konfigurieren, damit die Benutzer mit der Art der Authentifizierung vertraut sind und diese problemlos verläuft.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt84" class="tgtSentence">Der <externalLink><linkText>Azure AD Connect-Assistent </linkText><linkUri>https://www.microsoft.com/download/details.aspx?id=47594</linkUri></externalLink> stellt das Tool und die Anleitung zum Herstellen der Verbindung zwischen Ihrer lokalen Identitätsinfrastruktur und der Cloud dar.</caps:sentence>
            <caps:sentence sentenceid="8abca209d0cfffe0304cdfbbda7b0784" id="tgt85" class="tgtSentence">  Wählen Sie die Topologie und Anforderungen aus (einzelne oder mehrere Verzeichnisse, Kennwortsynchronisierung oder Verbund), woraufhin der Assistent dann alle Komponenten bereitstellt und konfiguriert, die zum Einrichten und Aktivieren Ihrer Verbindung erforderlich sind, einschließlich der Synchronisierungsdienste, der Active Directory Federation Services (AD FS) und des Azure AD PowerShell-Moduls.</caps:sentence>
            <caps:sentence sentenceid="2b2dfed46a172095c09326cab33613c5" id="tgt86" class="tgtSentence"> Azure AD Connect umfasst Funktionen, die zuvor als Dirsync und Azure AD Sync veröffentlicht wurden.</caps:sentence>
            <caps:sentence sentenceid="2a4e636e2b4a4b06927a54e5f369f3c5" id="tgt87" class="tgtSentence"> Weitere Informationen zur Verzeichnisintegration finden Sie unter <externalLink><linkText>Verzeichnisintegration</linkText><linkUri>http://technet.microsoft.com/library/jj573653.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f139c8fc16efbd381a14906f98b0761f" id="tgt88" class="tgtSentence">Nachdem Sie Ihrem Intune-Abonnement Benutzer hinzugefügt haben, sollten Sie einigen Benutzerkonten Administratoranmeldeinformationen gewähren.</caps:sentence>
            <caps:sentence sentenceid="b75c325390e5e46eaa2cf1dd94a78f4a" id="tgt89" class="tgtSentence"> Welche Konsole Sie für das Zuweisen von Administratoranmeldeinformationen verwenden, hängt davon ab, welchen Administratortyp Sie zuweisen möchten:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f8b0d8601b389b7f8462d41037b2007f" id="tgt90" class="tgtSentence">
                  <embeddedLabel>Mandantenadministrator</embeddedLabel>: Weisen Sie über das <embeddedLabel><token>wit_icp_1</token></embeddedLabel> diesen Administratortyp zum Verwalten Ihres Abonnements zu. Dies schließt Abrechnungen, Cloudspeicher und das Verwalten von Benutzern ein, die <token>wit_nextref</token> verwenden dürfen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f8b0d8601b389b7f8462d41037b2007f" id="tgt91" class="tgtSentence">
                  <embeddedLabel>Dienstadministrator</embeddedLabel>: Weisen Sie mithilfe der <embeddedLabel><token>wit_adminconsole</token></embeddedLabel> diesen Administratortyp für tägliche Aufgaben zu. Dies schließt das Verwalten mobiler Geräte oder Computer, das Bereitstellen von Richtlinien oder Software und das Ausführen von Berichten ein.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="48fcfd6e524e106cde00ce10592035ca" id="tgt92" class="tgtSentence">Weitere Informationen zu Administratorkonten finden Sie unter <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268#BKMK_AdminAccounts">Intune administrator accounts</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f437bb55445388dbe46c91737c36fd23" id="tgt93" class="tgtSentence">Informationen zu den Vorteilen der Synchronisierung von Benutzerkonten aus Ihrem lokalen Verzeichnis mit Azure AD finden Sie unter <externalLink><linkText>Ähnlichkeiten zwischen Active Directory und Microsoft Azure AD</linkText><linkUri>http://technet.microsoft.com/library/dn518177.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_AssignWitLicenses">
        <title>
          <caps:sentence sentenceid="d476bf0960d1185b667675e781df97c1" id="tgt94" class="tgtSentence">Schritt 4: Verwalten von Intune-Lizenzen</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a8878429f5a079d7d8fee26e30d43fa2" id="tgt95" class="tgtSentence">Zum Anmelden und zum Verwenden des Diensts benötigen Benutzer eine Lizenz für Ihr Intune-Abonnement.</caps:sentence>
            <caps:sentence sentenceid="f2c5cf56de3ad62460022b3dc0e0ba79" id="tgt96" class="tgtSentence"> Verfügen Benutzer über eine Lizenz, sind sie Mitglieder der <token>wit_firstref</token>-Benutzergruppe.</caps:sentence>
            <caps:sentence sentenceid="ccec2324b466bfe6d198134bf4d78e37" id="tgt97" class="tgtSentence"> In dieser Gruppe sind alle Benutzer enthalten, die über eine Lizenz zur Verwendung des Abonnements verfügen.</caps:sentence>
            <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt98" class="tgtSentence">
              <embeddedLabel>Durch jede Benutzerlizenz wird die Registrierung von bis zu fünf Geräten unterstützt</embeddedLabel>.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="02843a8b7395e35301dfa8c0b65ab33b" id="tgt99" class="tgtSentence">
                  <embeddedLabel>Wenn Sie Ihrem Abonnement mit dem <token>wit_icp_2</token> Benutzer</embeddedLabel> wahlweise manuell oder durch einen Massenimport aus einer CSV-Datei hinzufügen, wird jedem Konto von <token>wit_nextref</token> eine verfügbare Lizenz zugewiesen.</caps:sentence>
                <caps:sentence sentenceid="754e7fb366e51055b65cae7e7452dee8" id="tgt100" class="tgtSentence"> Ist keine Lizenz verfügbar, dann wird auch keine zugewiesen.</caps:sentence>
                <caps:sentence sentenceid="e0c0b6981f09538f8916989c5257172a" id="tgt101" class="tgtSentence"> Bei beiden Methoden können Sie Ihrem Abonnement neue Benutzerkonten hinzuzufügen, ohne den Konten dabei Lizenzen zuzuweisen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fc763cb31e9938f37737394681228f83" id="tgt102" class="tgtSentence">
                  <embeddedLabel>Wenn Sie Benutzer aus Ihrem lokalen Active Directory importieren</embeddedLabel>, wird den einzelnen Benutzerkonten von <token>wit_nextref</token> keine Lizenz zugewiesen.</caps:sentence>
                <caps:sentence sentenceid="90a809bd0b12df66356fd0f268b94ab8" id="tgt103" class="tgtSentence"> Sie müssen die Benutzerkonten daher zu einem späteren Zeitpunkt bearbeiten, um den Benutzern eine Lizenz zuzuweisen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d11e6e67c43a22f3ef63cd043456d758" id="tgt104" class="tgtSentence">
                  <embeddedLabel>Wenn Azure AD von Ihrem Konto und anderen Azure AD-Mandanten gemeinsam verwendet wird</embeddedLabel>, haben Sie Zugriff auf Benutzer, die diesen Diensten hinzugefügt wurden.</caps:sentence>
                <caps:sentence sentenceid="1e0d34407f824106000cf3fa4baa4199" id="tgt105" class="tgtSentence"> Diese Benutzer verfügen nicht über eine <token>wit_nextref</token>-Lizenz, bis Sie jedem von ihnen eine Lizenz zuweisen.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="73b2a820cad766bc267997d671921178" id="tgt106" class="tgtSentence">Wenn die Option zum Zuweisen oder Widerrufen einer Lizenz für <token>wit_nextref</token> deaktiviert ist, schließt ihr Abonnement möglicherweise Volumenlizenzoptionen wie jene ein, die bei Verwendung der <externalLink><linkText>Enterprise Mobility Suite</linkText><linkUri>http://www.microsoft.com/server-cloud/products/enterprise-mobility-suite/default.aspx</linkUri></externalLink> verfügbar sind.</caps:sentence>
            <caps:sentence sentenceid="dbd4987a06d29791f27ec90d329fa4bd" id="tgt107" class="tgtSentence"> Informationen zum Zuweisen oder Widerrufen von Lizenzen entnehmen Sie der Dokumentation Ihrer Lizenzoptionen.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="Step3" expanded="true">
        <title>
          <caps:sentence sentenceid="31825e25fe5d4f7a1a56baac9979aa83" id="tgt108" class="tgtSentence">Schritt 5: Erstellen von Gruppen zum Organisieren von Benutzern und Geräten</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="902ce6ab3337de9d748dde1562a4cefd" id="tgt109" class="tgtSentence">Mit Gruppen erhalten Sie in <token>wit_nextref</token> maximale Flexibilität beim Verwalten Ihrer Geräte und Benutzer.</caps:sentence>
            <caps:sentence sentenceid="d706f68d2ffd6eb78c13b818e0ad5389" id="tgt110" class="tgtSentence"> Sie können Gruppen einrichten, die Ihren organisatorischen Anforderungen (z. B. nach geografischem Standort, nach Abteilung oder nach Hardwareeigenschaften) entsprechen und diese dazu verwenden, um eine Vielzahl von Verwaltungsaufgaben ausführen, die von der Bereitstellung von Richtlinien für eine Gruppe von Benutzern bis zur Bereitstellung von Anwendungen auf einer Reihe von Geräten reichen.</caps:sentence>
          </para>
          <para></para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="8d18cc695293fda22645a516102649df" id="tgt111" class="tgtSentence">Erstellen einer Gerätegruppe</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="231d3aed688848a9d9519d8935008928" id="tgt112" class="tgtSentence">Verwenden Sie Gerätegruppen zum Bereitstellen von Apps und Updates sowie zum Konfigurieren anderer Features.</caps:sentence>
                <caps:sentence sentenceid="f07847ac9101417795aaf78809714773" id="tgt113" class="tgtSentence"> Richten Sie z. B. die Gruppe „Meine Geräte“ mithilfe der folgenden Schritte ein:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt114" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Gruppen</ui> &gt; <ui>Übersicht</ui> &gt; <ui>Gruppe erstellen</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4079902f721aa1dc05159ff969035f5d" id="tgt115" class="tgtSentence">Geben Sie unter <embeddedLabel>Gruppenname</embeddedLabel> „Meine Geräte“ ein, wählen Sie aus der übergeordneten Gruppenliste <embeddedLabel>Alle Geräte</embeddedLabel> aus, und klicken Sie dann auf <ui>Weiter</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt116" class="tgtSentence">Wählen Sie <ui>Alle Geräte</ui> auf der Seite <embeddedLabel>Mitgliedschaftskriterien definieren</embeddedLabel> aus, um anzugeben, dass die Gruppe sowohl mobile Geräte als auch Computer enthält.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt117" class="tgtSentence">Klicken Sie auf der Seite <ui>Direkte Mitgliedschaft definieren</ui> auf <embeddedLabel>Weiter</embeddedLabel>.</caps:sentence>
                    <caps:sentence sentenceid="1fbda84ad49f7d80c56df6d391be6601" id="tgt118" class="tgtSentence"> Hätten Sie zuvor eine Gruppe erstellt, die nicht alle Geräte enthält, und wollten Sie dieser neuen Gruppe nun bestimmte Geräte hinzufügen, dann können Sie dies an dieser Stelle tun.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt119" class="tgtSentence">Überprüfen Sie auf der Seite <ui>Zusammenfassung</ui> die Aktionen, die ausgeführt werden, und klicken Sie dann auf <ui>Fertig stellen</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="0db75d0aec9dc01ec9aa603cd0cdce0c" id="tgt120" class="tgtSentence">Sie finden die neue Gruppe in der Liste <ui>Gruppen</ui> im Arbeitsbereich <ui>Gruppen</ui> unter <embeddedLabel>Alle Geräte</embeddedLabel>.</caps:sentence>
                <caps:sentence sentenceid="9fbfdf7aa4c5de6ec931d6f9764a4c8f" id="tgt121" class="tgtSentence"> Hier können Sie die Gruppe auch bearbeiten oder löschen.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="2ccb91e3e9d58a5ef912a0d0e1f4d277" id="tgt122" class="tgtSentence">Erstellen einer Benutzergruppe</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e5fd5c2fc49a0352228654be50d50780" id="tgt123" class="tgtSentence">Verwenden Sie Benutzergruppen, um Software- und Geräterichtlinien bereitzustellen.</caps:sentence>
                <caps:sentence sentenceid="2041d3d7fc8ba82cf5e89f85c52b9ca1" id="tgt124" class="tgtSentence"> Richten Sie z. B. die Gruppe „Intune-Benutzer“ mithilfe der folgenden Schritte ein:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt125" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Gruppen</ui> &gt; <ui>Übersicht</ui> &gt; <ui>Gruppe erstellen</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4079902f721aa1dc05159ff969035f5d" id="tgt126" class="tgtSentence">Geben Sie unter <embeddedLabel>Gruppenname</embeddedLabel> „Intune-Benutzer“ ein, wählen Sie aus der übergeordneten Gruppenliste <embeddedLabel>Alle Benutzer</embeddedLabel> aus, und klicken Sie dann auf <ui>Weiter</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt127" class="tgtSentence">Setzen Sie auf der Seite <ui>Mitgliedschaftskriterien definieren</ui> die Option <ui>Gruppenmitgliedschaft starten mit</ui> auf <ui>Alle Benutzer in der übergeordneten Gruppe</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fbe61e5fb5cf7459e7f0ef57a2fda844" id="tgt128" class="tgtSentence">Klicken Sie neben <embeddedLabel>Mitglieder dieser Sicherheitsgruppen ausschließen</embeddedLabel> auf <embeddedLabel>Durchsuchen</embeddedLabel> und anschließend auf <ui>Unternehmensadministrator</ui>.</caps:sentence>
                    <caps:sentence sentenceid="d60da6b920a7059eff1bb779bd6f40ed" id="tgt129" class="tgtSentence"> Durch diesen Ausschluss können Sie die Gruppe „Intune-Benutzer“ verwalten, ohne dass das Konto „Unternehmensadministrator“ (auch als Mandantenadministrator bezeichnet) davon betroffen ist.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt130" class="tgtSentence">Klicken Sie auf der Seite <ui>Direkte Mitgliedschaft definieren</ui> auf <embeddedLabel>Weiter</embeddedLabel>.</caps:sentence>
                    <caps:sentence sentenceid="93d8eb9154df6f24f890975224ee7913" id="tgt131" class="tgtSentence"> Hier brauchen Sie nichts zu tun, denn die Gruppe „Intune-Benutzer“ soll alle Benutzer außer dem Unternehmensadministrator einschließen.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt132" class="tgtSentence">Überprüfen Sie auf der Seite <ui>Zusammenfassung</ui> die Aktionen, die ausgeführt werden, und klicken Sie dann auf <ui>Fertig stellen</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="0db75d0aec9dc01ec9aa603cd0cdce0c" id="tgt133" class="tgtSentence">Sie finden die neue Gruppe in der Liste <ui>Gruppen</ui> im Arbeitsbereich <ui>Gruppen</ui> unter <embeddedLabel>Alle Benutzer</embeddedLabel>.</caps:sentence>
                <caps:sentence sentenceid="9fbfdf7aa4c5de6ec931d6f9764a4c8f" id="tgt134" class="tgtSentence"> Hier können Sie die Gruppe auch bearbeiten oder löschen.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="05c2e7401296f58eb6e552c205147831" id="tgt135" class="tgtSentence">Weitere Informationen zum Verwenden von Gruppen finden Sie unter <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use Groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="Step4" expanded="true">
        <title>
          <caps:sentence sentenceid="fa41a4df1b867cedec3032c774bbcb49" id="tgt136" class="tgtSentence">Schritt 6: Erstellen von Richtlinien und Veröffentlichen einer App</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a8a321851e678a342be057ae5e30e283" id="tgt137" class="tgtSentence">Mit <token>wit_nextref</token>-Richtlinien stehen Einstellungen bereit, mit deren Hilfe Sie die Sicherheitseinstellungen auf mobilen Geräten steuern, die Windows-Firewall- und Endpoint Protection-Einstellungen für Computer warten und Anwendungen bereitstellen können.</caps:sentence>
            <caps:sentence sentenceid="24800f3018e57d504f7744979abb05f8" id="tgt138" class="tgtSentence"> Wenn Sie planen, Intune nach Ablauf der Testversion auf Geräten zu verwenden, die für die Produktion konfiguriert werden, müssen Sie unbedingt die Anweisungen unter <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure policy for mobile devices in Microsoft Intune</link> und <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Microsoft Intune</link> befolgen.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0843e33b7a4632e2b8eb427c5c8ead84" id="tgt139" class="tgtSentence">Sie können zwei Arten von App-Installationen mithilfe von Intune ausführen:</caps:sentence>
            <caps:sentence sentenceid="630af92259b34fe6e82ef27d3ec198b9" id="tgt140" class="tgtSentence"> Die erste ist eine <legacyBold>erforderliche Installation</legacyBold>, bei der die App automatisch auf verwalteten Computern bereitgestellt wird.</caps:sentence>
            <caps:sentence sentenceid="e83840104ca38273e1019a2a7b97a40b" id="tgt141" class="tgtSentence"> Die andere ist eine <legacyBold>verfügbare Installation</legacyBold>, bei der die App oder ein Link auf die App über das Intune-Unternehmensportal bereitgestellt wird, damit Benutzer auswählen können, ob die App auf ihren Computern oder mobilen Geräten installiert werden soll.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="566b5db6392dff724e19d4c5daa80230" id="tgt142" class="tgtSentence">Bevor Sie Intune zum Bereitstellen von Apps verwenden, stellen Sie sicher, dass Sie über die erforderlichen Lizenzen zum Veröffentlichen, Verteilen und Verwenden der App verfügen.</caps:sentence>
            <caps:sentence sentenceid="fc2403706e1f4165e8bf190b1d3cd775" id="tgt143" class="tgtSentence"> Im Arbeitsbereich „Lizenzen“ können Sie Lizenzvertragsinformationen für Apps oder Software, die im Rahmen von Microsoft-Volumenlizenzverträgen gekauft wurden, und für Microsoft- oder Nicht-Microsoft-Software, die auf anderem Wege gekauft wurde, hinzufügen und verwalten.</caps:sentence>
            <caps:sentence sentenceid="436f3af65dce14d652d54bf6ac14200b" id="tgt144" class="tgtSentence"> Sie können dann Lizenzberichte erstellen, die dann Informationen zur Verwendung verwalteter Lizenzen im gesamten Unternehmen anzeigen, damit Sie über Aktivitäten zur Nutzung von Lizenzen auf dem Laufenden bleiben.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1667acc3b4c25214b4bd1eeefede5a8a" id="tgt145" class="tgtSentence">In den folgenden Schritten werden Sie eine Konfigurationsrichtlinie für mobile Geräte und eine Firewallrichtlinie für Windows-Computer einrichten und Skype als verfügbare Installation für mobile Geräte konfigurieren, nachdem diese registriert wurden.</caps:sentence>
            <caps:sentence sentenceid="048ec8cd50527abfafacb47b8f27579f" id="tgt146" class="tgtSentence"> Nachdem Sie eine neue Richtlinie hinzugefügt und bereitgestellt haben, erben alle Benutzer oder Geräte in der Gruppe, für die Sie die Richtlinie bereitgestellt haben, die Einstellungen als Basisrichtlinie.</caps:sentence>
            <caps:sentence sentenceid="f48ccdca55207c0485aad1af701202a3" id="tgt147" class="tgtSentence"> Sie können die Details dieser Richtlinien später jederzeit über den Arbeitsbereich für Richtlinien überprüfen und bearbeiten.</caps:sentence>
          </para>
          <procedure expanded="true">
            <title>
              <caps:sentence sentenceid="cc67870df06ef28b77e928d2e30af7f3" id="tgt148" class="tgtSentence">Erstellen und Bereitstellen einer Konfigurationsrichtlinie für mobile Geräte</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt149" class="tgtSentence">Öffnen Sie die <externalLink><linkText>Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a0ee12f9384564e8aed10a645e0a29eb" id="tgt150" class="tgtSentence">Klicken Sie im linken Bereich auf das Symbol <ui>Richtlinie</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt151" class="tgtSentence">Klicken Sie auf der Seite <ui>Richtlinienübersicht</ui> in der Liste <ui>Aufgaben</ui> auf <ui>Richtlinie hinzufügen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b38bb80f7b7f5dd9e62c7355c1d36301" id="tgt152" class="tgtSentence"> Erweitern Sie in der Richtlinienliste die Plattform, für die Sie eine Richtlinie erstellen möchten, und wählen Sie dann <ui>Allgemeine Konfiguration</ui> sowie <ui>Richtlinie mit den empfohlenen Einstellungen erstellen und bereitstellen</ui> aus, und klicken Sie anschließend auf <ui>Richtlinie erstellen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="64aaaf966ef0bf0a24f2e1cf0a17069a" id="tgt153" class="tgtSentence">Wählen Sie nach Aufforderung in <ui>Gruppen auswählen, die Sie diese Richtlinie bereitstellen möchten</ui> in der Liste <ui>Meine Testbenutzer</ui> aus, und klicken Sie auf <ui>Hinzufügen</ui> &gt; <ui>OK</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="6657cd4c2251c9914b15d124292e878a" id="tgt154" class="tgtSentence">Die Richtlinie wird in der Liste der Konfigurationsrichtlinien angezeigt und wurde für die Gruppe <ui>Meine Testbenutzer</ui> bereitgestellt.</caps:sentence>
                  <caps:sentence sentenceid="f36a7afd4ca10f6514de8a76b54b4d1f" id="tgt155" class="tgtSentence"> Doppelklicken Sie auf die Richtlinie, um die Einstellungen anzuzeigen.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="true">
            <title>
              <caps:sentence sentenceid="5af5312711de3e4154d9fd8eafca7245" id="tgt156" class="tgtSentence">Veröffentlichen der Skype-App für mobile Geräte</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt157" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf das Symbol <ui>Apps</ui> und dann auf <ui>Apps</ui> &gt; <ui>App hinzufügen</ui>.</caps:sentence>
                    <caps:sentence sentenceid="60ab622426a76c724fa473ded4287eaa" id="tgt158" class="tgtSentence"> Geben Sie Ihre <token>wit_nextref</token>-Anmeldeinformationen ein, wenn Sie dazu aufgefordert werden.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="0aba49aa1480b69479b1182c63e784f9" id="tgt159" class="tgtSentence">Wenn Sie den <embeddedLabel>Intune-Softwareherausgeber</embeddedLabel> erstmals ausführen, kommt es zu einer kurzen Verzögerung, während die Anwendung installiert wird.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d2c04c3bcbd23695a5a7243390ee921c" id="tgt160" class="tgtSentence">
                Überprüfen Sie die Sicherheitswarnung, und klicken Sie auf <ui>Ausführen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt161" class="tgtSentence">Klicken Sie auf der Seite <ui>Vorbereitung</ui> auf <ui>Weiter</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt162" class="tgtSentence">Wählen Sie auf der Seite <ui>Softwaresetup</ui> unter <ui>Wählen Sie aus, wie diese Software für Geräte bereitgestellt werden soll</ui> die Option <ui>Externer Link</ui> aus.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="64dcd71bb43433626470d0d8c87e347f" id="tgt163" class="tgtSentence">Geben Sie unter <ui>Geben Sie die URL an</ui> den externen Link für die Software ein, und klicken Sie dann auf <ui>Weiter</ui>.</caps:sentence>
                    <caps:sentence sentenceid="8dbab34a42c878950bec876f4c0b902e" id="tgt164" class="tgtSentence"> Achten Sie darauf, der URL <legacyBold>http://</legacyBold> voranzustellen.</caps:sentence>
                    <caps:sentence sentenceid="9fb0463c4d10fb15b0a8b20b27de9c07" id="tgt165" class="tgtSentence"> Verwenden Sie für die Skype-App den nachfolgenden Link, der der Plattform für mobile Geräte entspricht, die Sie verwenden:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt166" class="tgtSentence">
                          <embeddedLabel>iOS:</embeddedLabel> <externalLink><linkText>https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8</linkText><linkUri>https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt167" class="tgtSentence">
                          <embeddedLabel>Android:</embeddedLabel> <externalLink><linkText>https://play.google.com/store/apps/details?id=com.skype.raider</linkText><linkUri>https://play.google.com/store/apps/details?id=com.skype.raider</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt168" class="tgtSentence">
                          <embeddedLabel>Windows Phone 8 oder Windows Phone 8.1:</embeddedLabel> <externalLink><linkText>http://www.windowsphone.com/en-us/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</linkText><linkUri>http://www.windowsphone.com/en-us/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt169" class="tgtSentence">Geben Sie auf der Seite <ui>Softwarebeschreibung</ui> die Informationen ein, die den Benutzern im Unternehmensportal zu der Software angezeigt werden sollen. Klicken Sie dann auf <ui>Weiter</ui>.</caps:sentence>
                    <caps:sentence sentenceid="97f592205562199b8073000d43c71be5" id="tgt170" class="tgtSentence"> Die folgenden Einstellungen stehen zur Verfügung (dieses Beispiel bezieht sich auf Skype):</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="57caaaa3def65c87f65fb4ad3d489e5a" id="tgt171" class="tgtSentence">
                          <legacyBold>Herausgeber:</legacyBold> Geben Sie den Namen des Herausgebers ein: „Microsoft“. </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="88185ee36b2baf5e64a4a1d2e8bed743" id="tgt172" class="tgtSentence">
                          <legacyBold>Name: </legacyBold>Geben Sie <embeddedLabel>Skype</embeddedLabel> ein.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c88e9b15e88445390feb212979ffc23a" id="tgt173" class="tgtSentence">
                          <legacyBold>Beschreibung:</legacyBold> Geben Sie eine Beschreibung für die Software ein, z. B. <embeddedLabel>Skype-Kommunikations-App</embeddedLabel>. </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="454b13ac784c57577cdf67b2b973ebbd" id="tgt174" class="tgtSentence">
                          <legacyBold>Kategorie: </legacyBold>Wählen Sie die Kategorie aus, die dieser Software am ehesten entspricht, z. B. <embeddedLabel>Zusammenarbeit</embeddedLabel>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f90adaaebff9d5c69d792885016798b4" id="tgt175" class="tgtSentence">
                          <legacyBold>Als ausgewählte App anzeigen und im Unternehmensportal hervorheben:</legacyBold> Wählen Sie diese Option, wenn Sie die App im Unternehmensportal auf mobilen Geräten hervorgehoben anzeigen möchten.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="1ebfcefd6d209280bbd536064bcaa884" id="tgt176" class="tgtSentence">
                          <legacyBold>Symbol: </legacyBold>Wählen Sie aus, ob der Software ein Symbol zugeordnet werden soll.</caps:sentence>
                        <caps:sentence sentenceid="7a717d29de5e56bac161ce80947323cf" id="tgt177" class="tgtSentence"> Die maximale Größe für das Symbol beträgt 250 x 250 Pixel.</caps:sentence>
                        <caps:sentence sentenceid="12c7d0e8fdb84868d3ba9585d87c9393" id="tgt178" class="tgtSentence"> Die empfohlene Größe ist 32 x 32 Pixel.</caps:sentence>
                        <caps:sentence sentenceid="375c9b99d61872ffb69176290dcb7c3a" id="tgt179" class="tgtSentence"> Diese Einstellung ist für den Intune-Testmandanten optional.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt180" class="tgtSentence">Überprüfen Sie auf der Seite <ui>Zusammenfassung</ui> die Softwareinformationen, und klicken Sie dann auf <ui>Hochladen</ui>.</caps:sentence>
                    <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt181" class="tgtSentence"> Klicken Sie auf <ui>Schließen</ui>, um den Assistenten zu beenden.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt182" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Apps</ui> &gt; <ui>Apps</ui> &gt; <ui>Skype</ui> &gt; <ui>Bereitstellung verwalten</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt183" class="tgtSentence">Wählen Sie auf der Seite <ui>Gruppen auswählen</ui> die Option <ui>Meine Testbenutzer</ui> aus, um die Software für diese Benutzergruppe bereitzustellen, und klicken Sie auf <ui>Hinzufügen</ui> &gt; <ui>Weiter</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt184" class="tgtSentence">Wählen Sie auf der Seite <ui>Bereitstellungsaktion</ui> in der Spalte <ui>Genehmigung</ui> bei jeder Gruppe <ui>Verfügbare Installation</ui> aus.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt185" class="tgtSentence">Klicken Sie auf <ui>Fertig stellen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="cbc48cad1228f2bb33bc63bb8b4782ed" id="tgt186" class="tgtSentence">Die Skype-App kann jetzt über das Unternehmensportal auf mobilen Geräten installiert werden, jedoch müssen Sie zunächst <token>wit_nextref</token>-Software auf Computern und mobilen Geräten installieren.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ConfigureCompanyPortal">
        <title>
          <caps:sentence sentenceid="46c94158fc52ea69ab26c62d21c9ba4f" id="tgt187" class="tgtSentence">Schritt 7: Anpassen des Unternehmensportals</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt188" class="tgtSentence">Im <token>wit_iwportal_1</token> können Benutzer auf Unternehmensdaten zugreifen, häufige Aufgaben wie das Registrieren von Geräten und das Installieren von Apps ausführen und sich über Unterstützungsmöglichkeiten durch Ihre IT-Abteilung informieren.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9497c9d728f416a8477d3356e0ff8828" id="tgt189" class="tgtSentence">Wenn Sie das Unternehmensportal anpassen, gelten die Konfigurationen sowohl für die Unternehmensportalwebsite als auch für die Unternehmensportal-Apps.</caps:sentence>
          </para>
          <procedure expanded="true" address="BKMK_ToCustomizeCompanyPortal">
            <title>
              <caps:sentence sentenceid="3a064b0b9e01dfff8d3958f44c342998" id="tgt190" class="tgtSentence">Einstellungen zum Anpassen des Unternehmensportals</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt191" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink> auf <ui>Verwaltung</ui> &gt; <ui>Unternehmensportal</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="bc6c35cb92615f724c1e68459fef160b" id="tgt192" class="tgtSentence">Konfigurieren Sie beliebig viele der folgenden optionalen Elemente:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b06b1fdffac8a8d7f85ec0d73a8c9b4d" id="tgt193" class="tgtSentence">Konfigurationsbereich</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="bfaad773361a781112fb325b433d54f7" id="tgt194" class="tgtSentence">Feldname</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6e97c2db4d6d812002d257c5625125e9" id="tgt195" class="tgtSentence">Maximale Zeichenlänge</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt196" class="tgtSentence">Weitere Informationen</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD rowspan="6">
                          <para>
                            <caps:sentence sentenceid="80f41ee55ae984604a7bd65a194d73ab" id="tgt197" class="tgtSentence">Kontaktdaten und Datenschutzerklärung des Unternehmens</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9bb4c85dfbafa8c61f627241bb21358c" id="tgt198" class="tgtSentence">Firmenname</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d645920e395fedad7bbbed0eca3fe2e0" id="tgt199" class="tgtSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e163c87f97ede943ecc0ad5150dfd0e2" id="tgt200" class="tgtSentence">Dieser Name wird als Titel des Unternehmensportals angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="16576d71cb733d359db3b6e40b97b228" id="tgt201" class="tgtSentence">Kontaktname für IT-Abteilung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d645920e395fedad7bbbed0eca3fe2e0" id="tgt202" class="tgtSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="974edf181ade78ffb7241bf97b9d5083" id="tgt203" class="tgtSentence">Dieser Name wird auf der Seite <ui>An IT-Abteilung wenden</ui> angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="965d8e507652fcc1b19d4b13823cf800" id="tgt204" class="tgtSentence">Telefonnummer der IT-Abteilung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="98f13708210194c475687be6106a3b84" id="tgt205" class="tgtSentence">20</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="65e0114a82b32a48ec5af50a41b2d3df" id="tgt206" class="tgtSentence">Diese Telefonnummer wird auf der Seite <ui>An IT-Abteilung wenden</ui> angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="17301e373b6094b08e5cf38e75d1a0b3" id="tgt207" class="tgtSentence">E-Mail-Adresse der IT-Abteilung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d645920e395fedad7bbbed0eca3fe2e0" id="tgt208" class="tgtSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="31bd76e4f571d40223816e8c5f288cdf" id="tgt209" class="tgtSentence">Diese Kontaktadresse wird auf der Seite <ui>An IT-Abteilung wenden</ui> angezeigt.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="bac5314577aa12f439fa36cf4330ab96" id="tgt210" class="tgtSentence">Sie müssen eine gültige E-Mail-Adresse im Format <userInput>alias@domainname.com</userInput> eingeben.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt211" class="tgtSentence">Weitere Informationen</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="da4fb5c6e93e74d3df8527599fa62642" id="tgt212" class="tgtSentence">120</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="0a4109098d37608f6585e276d67047a8" id="tgt213" class="tgtSentence">Dies wird auf der Seite <ui>An IT-Abteilung wenden</ui> angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2ddf6ec5ba19603e0bbf4dd9dd16b1c5" id="tgt214" class="tgtSentence">URL der Datenschutzrichtlinie des Unternehmens</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d1fe173d08e959397adf34b1d77e88d7" id="tgt215" class="tgtSentence">79</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="175727eec4cd6ffc901ad78b72e62191" id="tgt216" class="tgtSentence">Sie können eine eigene Datenschutzrichtlinie für Ihr Unternehmen angeben. Diese wird angezeigt, wenn die Benutzer im Unternehmensportal auf die Datenschutzlinks klicken.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="0472d2a822cb582a87d6bb241f912301" id="tgt217" class="tgtSentence">Sie müssen eine gültige URL im Format <userInput>https://www.contoso.com</userInput> eingeben.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD rowspan="2">
                          <para>
                            <caps:sentence sentenceid="a4a0cf3b94f4024c16574d3f299f1c1e" id="tgt218" class="tgtSentence">Supportkontakte</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a1139ec9f31e95e744ec5a994f6e15fb" id="tgt219" class="tgtSentence">URL der Supportwebsite</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7ef605fc8dba5425d6965fbd4c8fbe1f" id="tgt220" class="tgtSentence">150</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f77ead1287db660ad16fe436ed7c7ade" id="tgt221" class="tgtSentence">Wenn Sie über eine Supportwebsite verfügen, die Ihre Benutzer verwenden sollen, geben Sie hier die URL an.</caps:sentence>
                            <caps:sentence sentenceid="e383a6033d2f9bcf460bc85f2cd9673b" id="tgt222" class="tgtSentence"> Die URL muss das Format <userInput>https://www.contoso.com</userInput> aufweisen.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="69bbef7c22fdfd3a84ae3f2eb515f26f" id="tgt223" class="tgtSentence">Wenn Sie keine URL angeben, wird im Unternehmensportal auf der Seite <ui>An IT-Abteilung wenden</ui> keine Supportwebsite angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="ca75dc95767c2d020aba7b02bb2837c8" id="tgt224" class="tgtSentence">Websitename</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d645920e395fedad7bbbed0eca3fe2e0" id="tgt225" class="tgtSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="100c1c9fca941c2033c1772e0757c657" id="tgt226" class="tgtSentence">Dies ist der Anzeigename der URL für die Supportwebsite.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e63d54d32c6ef36898a448b157c2719f" id="tgt227" class="tgtSentence">Wenn Sie für die Supportwebsite eine URL, aber keinen Anzeigenamen angeben, wird im Unternehmensportal auf der Seite <ui>An IT-Abteilung wenden</ui> der Text <ui>Zur IT-Website wechseln</ui> angezeigt.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD rowspan="3">
                          <para>
                            <caps:sentence sentenceid="50a04ed5229b48c39039e72dbedb84fc" id="tgt228" class="tgtSentence">Anpassung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="50806248555606b2a51599138f16c2e9" id="tgt229" class="tgtSentence">Farbdesign</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt230" class="tgtSentence">Nicht zutreffend</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f14122331d56a0996b939f974850112b" id="tgt231" class="tgtSentence">Wählen Sie ein Farbdesign aus, das auf das Unternehmensportal angewendet werden soll.</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f6c1de868188712d2b05e2f32659ccfa" id="tgt232" class="tgtSentence">Firmenlogo einschließen</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt233" class="tgtSentence">Nicht zutreffend</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="86636fac9d8e40f9e61c5e7e8b5829a6" id="tgt234" class="tgtSentence">Wenn Sie diese Option aktivieren, können Sie Ihr Firmenlogo hochladen. Dieses wird dann im Unternehmensportal angezeigt.</caps:sentence>
                            <caps:sentence sentenceid="446a0243f5e7b01e37a746c71baf2c2c" id="tgt235" class="tgtSentence"> Sie können zwei Logos hochladen:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="9562d2823694124a4187690543d9eb87" id="tgt236" class="tgtSentence">Ein Logo zur Anzeige bei weißem Hintergrund des Unternehmensportals</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="008848a756c926fec2fd9c71caac0583" id="tgt237" class="tgtSentence">Ein Logo zur Anzeige bei einer Hintergrundfarbe des Unternehmensportals entsprechend Ihrem Farbdesign</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence sentenceid="2df8f1bfa0cf61868ef3b080347a1f22" id="tgt238" class="tgtSentence">Die Logodateien müssen PNG- oder JPG-Dateien sein und die folgenden Kriterien erfüllen:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="7350e7b91330cbbdc7f2bbc050a60650" id="tgt239" class="tgtSentence">Auflösung: 400 × 100 Pixel maximal</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="8b57a9deb971de85472a4d8745ed9090" id="tgt240" class="tgtSentence">Größe: 750 KB maximal</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e646bd3ec8157320c646ae3df4c64e50" id="tgt241" class="tgtSentence">Hintergrund für die <token>win8_client_2</token>-Unternehmensportal-App auswählen</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt242" class="tgtSentence">Nicht zutreffend</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2108e0f45b2c1cb850b5c341526c2ec7" id="tgt243" class="tgtSentence">Diese Einstellung betrifft nur den Hintergrund der Unternehmensportal-App für <token>win8_client_2</token>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt244" class="tgtSentence">Klicken Sie auf <ui>Speichern</ui>, um Ihre Änderungen zu speichern.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="4d2f1a2e8e21bffe8aafcaa7a13ec0eb" id="tgt245" class="tgtSentence">Nach dem Speichern Ihrer Änderungen können Sie über die Links, die am unteren Rand der Seite <ui>Unternehmensportal</ui> in der Verwaltungskonsole angegeben sind, die Unternehmensportalwebsite anzeigen.</caps:sentence>
                  <caps:sentence sentenceid="0807d1e3cc22f55e2220391b59ce2c71" id="tgt246" class="tgtSentence"> Diese Links können nicht geändert werden.</caps:sentence>
                  <caps:sentence sentenceid="1ccb48a7b8cfc8ec25c97e4c65abffda" id="tgt247" class="tgtSentence"> Wenn ein Benutzer sich anmeldet, werden über diese Links Ihre Abonnements im Unternehmensportal angezeigt.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="Step5" expanded="true">
        <title>
          <caps:sentence sentenceid="118a220075d9446a6e1b49bd06cbb300" id="tgt248" class="tgtSentence">Schritt 8: Registrieren von Computern in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f1bad5e9b1f61c9f835fd22052613802" id="tgt249" class="tgtSentence">Sie können die <token>wit_nextref</token>-Clientsoftware auf folgende Weise auf Computern installieren:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="ce5e33133c939503d42d666db2a6a77f" id="tgt250" class="tgtSentence">Benutzer können ein vom Administrator bereitgestelltes Installationsprogramm für die manuelle Registrierung verwenden.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="356464023a0325e716430b9038462c47" id="tgt251" class="tgtSentence">
                  <token>wit_nextref</token>-Software kann in einem Betriebssystemimage enthalten sein oder mithilfe einer Gruppenrichtlinie bereitgestellt werden.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="977b769708b270bbc273f62413bc50df" id="tgt252" class="tgtSentence">Endbenutzer können ihre Geräte über das <token>wit_firstref</token>-Unternehmensportal selbst registrieren.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="32ab4153375d385b3d6ae81a309ab08b" id="tgt253" class="tgtSentence">Jeder registrierte Computer wird mit dem Benutzerkonto verknüpft, das zum Installieren der Clientsoftware verwendet wurde.</caps:sentence>
            <caps:sentence sentenceid="f16e169ab1f5eb03d1a0a698bbf7b019" id="tgt254" class="tgtSentence"> Microsoft Intune Endpoint Protection wird ebenfalls standardmäßig während der Intune-Clientinstallation auf Computern installiert.</caps:sentence>
            <caps:sentence sentenceid="9eb3ae8fa9dfc080d73d3864a807557d" id="tgt255" class="tgtSentence"> Mit Endpoint Protection können Sie die Computer in Ihrem Unternehmen schützen, indem Sie Echtzeitschutz gegen mögliche Bedrohungen bereitstellen, Malwaredefinitionen stets auf dem neuesten Stand halten und geplante Überprüfungen automatisch ausführen.</caps:sentence>
            <caps:sentence sentenceid="187d60fff6b2798d43e6e725ce4c63ae" id="tgt256" class="tgtSentence"> Zur Erhöhung der Sicherheit können Sie auch Intune-Richtlinien zum Verwalten von Windows-Firewall-Einstellungen auf verwalteten Computern verwenden.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5c574c2ce945d8316ca01e56bb548d77" id="tgt257" class="tgtSentence">Was Sie wissen sollten, bevor Sie beginnen:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="44eb4a00219592c0f5d5ea04447be9fd" id="tgt258" class="tgtSentence">Der Benutzer muss ein Administrator auf dem Computer sein, um die Clientsoftware zu installieren.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="adcea97639acf6a03275b132d53e528c" id="tgt259" class="tgtSentence">Für die Selbstregistrierung muss Internet Explorer auf dem Clientcomputer installiert sein.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f27842e450a48e7919b71487e067ea77" id="tgt260" class="tgtSentence">Bei jeder Selbstregistrierung eines Computers durch einen Benutzer wird eine <token>wit_firstref</token>-Lizenz verwendet.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e4ee29910343259f71d5440afddefd8c" id="tgt261" class="tgtSentence">Bei der Selbstregistrierung eines Computers muss ein Microsoft Online Services-Konto (für die Arbeit oder Schule) verwendet werden.</caps:sentence>
                <caps:sentence sentenceid="b53aa5252c8c3aee2df8e5b9e2e80ac0" id="tgt262" class="tgtSentence"> Dies ist entweder das Konto, mit dem Sie sich angemeldet haben, oder das Administratorkonto, das erstellt wurde, als Sie sich für die kostenlose Testversion registriert haben.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="2dbfdff62fdd4435252a64a08ebf83ac" id="tgt263" class="tgtSentence">In diesem Beispiel werden wir die Methode der Selbstregistrierung verwenden:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt264" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Verwaltung</ui> &gt; <ui>Unternehmensportal</ui>, und scrollen Sie zum unteren Rand des Bildschirms.</caps:sentence>
                <caps:sentence sentenceid="869aa2e57f526dbda4a32e6b9f6cf86e" id="tgt265" class="tgtSentence"> Kopieren Sie die unter <ui>Intune-Unternehmensportal</ui> gezeigte URL.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5e760ff30358b675373f5c7e21c2a992" id="tgt266" class="tgtSentence">Navigieren Sie mit Internet Explorer zu der Unternehmensportal-URL, die Sie im vorherigen Schritt notiert haben, und melden Sie sich mit Ihren Administratoranmeldeinformationen an.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt267" class="tgtSentence">Klicken Sie auf <ui>Gerät hinzufügen</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt268" class="tgtSentence">Klicken Sie auf <ui>Software herunterladen</ui> und dann auf <ui>Ausführen</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt269" class="tgtSentence">Klicken Sie auf <ui>Weiter</ui>, um den <token>wit_firstref</token>-Setup-Assistenten zu starten.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2cd806a671c80ccf7c83ea4a4f35260b" id="tgt270" class="tgtSentence">Klicken Sie nach Abschluss des Setup-Assistenten auf <ui>Fertig stellen</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ddf17fc7894cf72ade97323197b171f8" id="tgt271" class="tgtSentence">Weitere Informationen zur Verwaltung von Computern mit <token>wit_nextref</token> finden Sie unter <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be managed by Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b0e32c991dfd7befb8ebe2e54dc9b555" id="tgt272" class="tgtSentence">Weitere Informationen zur Verwaltung von Software mit <token>wit_nextref</token> finden Sie unter <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Manage software with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="Step6" expanded="true">
        <title>
          <caps:sentence sentenceid="739d06d3058bc6a82d61c01f5736959c" id="tgt273" class="tgtSentence">Schritt 9: Registrieren mobiler Geräte und Installieren einer App</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e519d541bd7bb7c411f0a650e1289f7e" id="tgt274" class="tgtSentence">Um die Verwaltung mobiler Geräte mit Intune einzurichten, müssen Sie zunächst die Verwaltungsstelle für mobile Geräte festlegen, die Verwaltung der Geräteplattformen aktivieren und Ihre Geräte anschließend in der Unternehmensportal-App registrieren.</caps:sentence>
            <caps:sentence sentenceid="ff1d43ede2bfa6f58cd9400d72714f28" id="tgt275" class="tgtSentence"> Sie können dann die von Ihnen veröffentlichte Microsoft Skype-Anwendung bereitstellen.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="40b0f1eb9993c21c2d628a71d3055e13" id="tgt276" class="tgtSentence">Aktivieren der Geräteverwaltung und Registrieren von Geräten</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt277" class="tgtSentence">
                      <embeddedLabel>Festlegen von Intune als Verwaltungsstelle für mobile Geräte</embeddedLabel>
                      <br />Klicken Sie in der <externalLink><linkText>Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Verwaltung</ui> &gt; <ui>Verwaltung mobiler Geräte</ui>. Wählen Sie unter <ui>Aufgaben</ui> die Option <ui>MDM-Autorität festlegen</ui>.</caps:sentence>
                    <caps:sentence sentenceid="c0a500b8fb422e9590506aa1459c4776" id="tgt278" class="tgtSentence">  Klicken Sie im Dialogfeld „MDM-Autorität“ auf <ui>Ja</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="200b0116ac2aa3e51d0a657cfeb83876" id="tgt279" class="tgtSentence">
                      <embeddedLabel>Aktivieren von MDM für Ihre Geräteplattform</embeddedLabel>
                      <br />Aktivieren Sie die Verwaltung mobiler Geräte für die Geräteplattform, die Sie verwalten möchten.</caps:sentence>
                    <caps:sentence sentenceid="f8a682d66ce3de58a2df7fd290687704" id="tgt280" class="tgtSentence"> Je nach Plattform sind andere Anforderungen relevant:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="80219166c3d3f038c1a3799845545f82" id="tgt281" class="tgtSentence">
                          <embeddedLabel>iOS und Mac OS X</embeddedLabel>: Siehe <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Set up iOS management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="80219166c3d3f038c1a3799845545f82" id="tgt282" class="tgtSentence">
                          <embeddedLabel>Windows Phone</embeddedLabel>: Siehe <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Set up Windows Phone management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9d4e891992bcb69b759ec4e29264d447" id="tgt283" class="tgtSentence">
                          <embeddedLabel>Android</embeddedLabel>: Mobile Android-Geräte ermöglichen Benutzern die Registrierung über die Unternehmensportal-App, die in Google Play zur Verfügung steht.</caps:sentence>
                        <caps:sentence sentenceid="68b2fbaa00b39392cb6dfa27deeabc8e" id="tgt284" class="tgtSentence"> Es ist keine weitere Konfiguration in Intune erforderlich.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="853ae90f0351324bd73ea615e6487517" id="tgt285" class="tgtSentence">
                      <embeddedLabel>Geräte registrieren</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="404587f525772cc3d94d516b0ee17bb3" id="tgt286" class="tgtSentence">
                          <embeddedLabel>Android</embeddedLabel>: Installieren Sie die <ui>Intune-Unternehmensportal-App</ui> der Microsoft Corporation, die auf <externalLink><linkText>Google Play</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkId=386612</linkUri></externalLink> verfügbar ist, und melden Sie sich mit den oben hinzugefügten Intune-Anmeldeinformationen an.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="404587f525772cc3d94d516b0ee17bb3" id="tgt287" class="tgtSentence">
                          <embeddedLabel>iOS und Mac OS X</embeddedLabel>: Installieren Sie die <ui>Microsoft Intune-Unternehmensportal-App</ui> der Microsoft Corporation, die im App Store verfügbar ist, und melden Sie sich mit den oben hinzugefügten Intune-Anmeldeinformationen an.</caps:sentence>
                        <caps:sentence sentenceid="5c43821480580ddd18f45f98ae4db8e9" id="tgt288" class="tgtSentence"> Rufen Sie <ui>Angemeldete Geräte</ui> auf, um Ihr Gerät hinzuzufügen.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f75132817f647ace33eee99c7949baa6" id="tgt289" class="tgtSentence">
                          <embeddedLabel>Windows Phone 8.1</embeddedLabel>: Benutzer installieren die <ui>Unternehmensportal</ui>-App der Microsoft Corporation, die im Windows Phone Store verfügbar ist, und melden sich mit den oben hinzugefügten Intune-Anmeldeinformationen an.</caps:sentence>
                        <caps:sentence sentenceid="7e7309c5dc1a8a75499274c3c25077d8" id="tgt290" class="tgtSentence">  Rufen Sie <ui>Angemeldete Geräte</ui> auf, um Ihr Gerät hinzuzufügen.<ui></ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="afd97dfc4973a178fd4a70c6e7c732bb" id="tgt291" class="tgtSentence">
                          <embeddedLabel>Windows Phone 8.0 </embeddedLabel>: Benutzer klicken auf <ui>Systemeinstellungen</ui> &gt; <ui>Unternehmens-Apps</ui>, und registrieren sich mit den oben hinzugefügten Intune-Anmeldeinformationen.</caps:sentence>
                        <caps:sentence sentenceid="1f802e1d645f632facd3cf39ce59a497" id="tgt292" class="tgtSentence"> Die Unternehmensportal-App wird auf Ihrem Telefon bereitgestellt.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="ea6a17d77b012113a5ea26c9e24e89cd" id="tgt293" class="tgtSentence">Wenn Sie zur Eingabe einer <ui>Serveradresse</ui> aufgefordert werden, geben Sie "manage.microsoft.com" ein.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5622cde8fde107230ede3cc661406799" id="tgt294" class="tgtSentence">Öffnen Sie auf dem Gerät das Unternehmensportal, wählen Sie <ui>Apps</ui> aus, und installieren Sie dann <ui>Microsoft Skype</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence sentenceid="cf88674febdb52c69bbfc8e9942cc381" id="tgt295" class="tgtSentence">Weitere Informationen zum Verwalten von mobilen Geräten mit <token>wit_nextref</token> finden Sie unter <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage Mobile Devices with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="485192fc8154e7a2a3fce28d1b02efa6" id="tgt296" class="tgtSentence">Aufgaben nach der Konfiguration</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="19e99304a48dd547e2e8deec510341d0" id="tgt297" class="tgtSentence">Nach Abschluss der anfänglichen Konfigurationsschritte für ein kostenpflichtiges Intune-Abonnement können Sie zusätzliche Verwaltungsfunktionen für mobile Geräte aktivieren.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f50afbaecc6fe608f03e672bd5539dd5" id="tgt298" class="tgtSentence">
                  <legacyBold>Verbinden von Exchange mit Intune:</legacyBold> Für Benutzer von mobilen Geräten, die noch nicht in Intune registriert sind, können Sie mithilfe eines Connectors für lokales Exchange und Exchange Online die Exchange ActiveSync-Verwaltung in Microsoft Office 365 aktivieren.</caps:sentence>
                <caps:sentence sentenceid="9a76b3282712c2b463d0a7d6e8043436" id="tgt299" class="tgtSentence"> Mit dem Exchange Connector stellen Sie eine Verbindung mit Ihrer Exchange-Bereitstellung her und können mobile Geräte über die Intune-Verwaltungskonsole verwalten.</caps:sentence>
                <caps:sentence sentenceid="b5b9f45bb1c4d5f850d0a730f4169533" id="tgt300" class="tgtSentence"> Weitere Informationen zum Exchange Connector finden Sie unter <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Mobile device management with Exchange ActiveSync and Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4e0f18efba708372e43c567e31a79b2a" id="tgt301" class="tgtSentence">
                  <legacyBold>Intune-Berichte:</legacyBold> Microsoft Intune bietet Warnungen und Berichte, mit denen Sie Geräte überwachen können, sowie Softwarelizenz-Statusangaben und Aktionen, die sich auf Geräte auswirken (z. B. das Zurücksetzen eines Geräts).</caps:sentence>
                <caps:sentence sentenceid="f8ffa50d491d9f4257ddc1e9fc49f7d9" id="tgt302" class="tgtSentence">  Weitere Informationen zur Berichterstellung finden Sie unter <link xlink:href="0f7dc155-cb8e-477b-ba02-2623194a9575">Monitoring and reporting with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5160ef7a7a552413f3c0d40c3cf088a4" id="tgt303" class="tgtSentence">
                  <legacyBold>Schützen von Unternehmensressourcen:</legacyBold> Nachdem Sie Intune konfiguriert und Ihre Geräte registriert haben, sollten Sie sicherstellen, dass Sie die Geräte vor Datenverlust und anderen Bedrohungen schützen.</caps:sentence>
                <caps:sentence sentenceid="43d03f893ee8f63b6db8893f31064088" id="tgt304" class="tgtSentence"> Weitere Informationen zum Schutz von Ressourcen finden Sie unter <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1bfd1a23-681d-4cc8-834c-c7856d69d409">Get started with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Whether you start with a 30-day free trial,  or start with a paid subscription, Microsoft Intune provides a quick and easy way for you to manage mobile devices and computers in your organization.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This topic  leads you through the steps of setting up a cloud-only instance of <token>wit_firstref</token>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">If you purchase at least 150 licenses for Microsoft Intune in an eligible plan, you can use the "FastTrack Center Benefit," a service where Microsoft specialists work with you to get your environment ready for Intune.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> See <externalLink><linkText>Microsoft Intune Service Benefit Description</linkText><linkUri>https://technet.microsoft.com/library/mt228265.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">Getting started with a paid subscription of Intune shares many of the same steps as starting with a <externalLink><linkText>free 30-day trial</linkText><linkUri>https://technet.microsoft.com/library/dn646983.aspx</linkUri></externalLink>.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> However  in this topic, you'll also cover some additional areas that most people might not need to address in trial deployments, including:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Synchronizing on-premises Active Directory accounts with Intune and Azure Active Directory</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Domain and DNS service considerations</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Customizing Intune features for production use</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence id="src10" class="srcSentence">This topic focuses on configuring Intune as a standalone service.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> If you're currently using Microsoft System Center Configuration Manager (ConfigMgr) to manage computers and servers, you can connect Intune with ConfgMgr in a hybrid deployment.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> This configuration offers several benefits and leverages your existing on-premises infrastructure.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> See <externalLink><linkText>Manage Mobile Devices with Configuration Manager and Microsoft Intune</linkText><linkUri>https://technet.microsoft.com/library/jj884158.aspx</linkUri></externalLink> for more information about hybrid Intune and ConfigMgr deployments.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Before you begin</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">Starting with a paid subscription means that you've <externalLink><linkText>completed an Intune trial</linkText><linkUri>https://technet.microsoft.com/library/dn646983.aspx</linkUri></externalLink> and that you're ready to deploy Intune and make changes to your existing network infrastructure.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> This could range from simply adding or updating your internal and external DNS records to connecting your existing Active Directory accounts to Azure Active Directory.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Whatever mix of Intune  mobile device management features you leverage, you'll need to  carefully plan how Intune will interact with your existing network components and services.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Specifically, you should review:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">
                  <legacyBold>How you'll manage user identity</legacyBold>:  For most medium-level and enterprise-level organizations, connecting your existing directory services to Intune via Azure Active Directory is the best and most convenient way to manage user identity with Intune.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> This is especially true if you already use other Microsoft cloud services, such as Office 365 or Exchange Online.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> Synchronizing your existing user accounts using <externalLink><linkText>Microsoft's AD Connect</linkText><linkUri>https://www.microsoft.com/download/details.aspx?id=47594</linkUri></externalLink> is a quick and easy way to connect your on-premises Active Directory to Azure Active Directory and configure a single sign-on authentication experience for your users.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">
                  <legacyBold>How DNS will be impacted</legacyBold>: If you want to use your own domain name instead of the default onmicrosoft.com domain generated by the Intune service, some public DNS record updates will be needed when configuring Azure (or other Microsoft cloud services) to use your custom domain.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> DNS records are required so that mobile devices can locate the Intune service, as well as making other mobility management services work correctly.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> You'll need to decide if you want  to manage your DNS records at your DNS host  or have Azure or Office 365 create and manage the DNS records for your domain after you change your DNS records to point to these services.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src25" class="srcSentence">Ready to get started?</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> You'll need the following when starting your paid subscription to Intune:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src27" class="srcSentence">
           A device with a Silverlight-enabled web browser that you can use to access the websites where you'll  create Intune user accounts (the <embeddedLabel>Intune Account Portal</embeddedLabel>) and where you'll manage devices, groups, and policies  (the <embeddedLabel>Intune administration console</embeddedLabel>).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src28" class="srcSentence">
           A second device with a web browser, which you can use to access the company portal to see how most <token>wit_nextref</token> users will enroll and manage their devices, find and install software, and request help from administrators.</caps:sentence>
                <caps:sentence id="src29" class="srcSentence"> Instead of using a second device with a web browser, you can use the “privacy mode” setting on the same browser that you use for <token>wit_nextref</token> administration (for example: in Internet Explorer, you can click <ui>Tools</ui> &gt; <ui>InPrivate Browsing</ui>).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src30" class="srcSentence">
           If you have an existing Microsoft Online Services account, you'll need the administrator credentials for that account.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> If you don’t have such an account, or if you want to use this Intune tenant for evaluation purposes only, you don't need tenant administrator credentials.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src32" class="srcSentence">
           If you'll manage iOS or Windows Phone devices with Intune, you'll need certificates (or keys) and accounts to retrieve those certificates.</caps:sentence>
                <caps:sentence id="src33" class="srcSentence"> Android devices don't need any additional certificates:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">Platform</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Certificate Requirements</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">More information</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">
                   Windows Phone 8.1 and <token>winphone8_client_1</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">No certificate is required for Windows Phone 8.1 users who install the company portal app from the Store.</caps:sentence>
                        <caps:sentence id="src39" class="srcSentence"> A Symantec certificate is required for Windows Phone 8.0 or to use Intune to deploy the company portal app to Windows Phone 8.1 devices.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">This guidance assumes your users get the company portal app from the Store on a Windows Phone 8.1 or later device.</caps:sentence>
                        <caps:sentence id="src41" class="srcSentence"> For information about Windows Phone 8.0 support, see <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Set up Windows Phone management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">
                  Windows 10, <token>winblue_winrt_2</token>, <token>win8RT_client_1</token>, or <token>winblue_client_2</token> devices</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">There are no certificate requirements for enrolling Windows RT and Windows devices.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">
                          <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be Managed by Intune</link>.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">iOS or Mac OS X</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Get an Apple Push Notification service certificate.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">Request an Apple Push Notification service certificate from Apple, as described here: <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Start managing iOS devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </listItem>
          </list>
        </content>
      </section>
      <section address="Step1" expanded="true">
        <title>
          <caps:sentence id="src48" class="srcSentence">Step 1: Sign up or sign in to Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src49" class="srcSentence">Before  you either sign up or sign in to Intune,  you should consider the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src50" class="srcSentence">Whether your organization already has a Microsoft Online Services work or school account</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src51" class="srcSentence">Whether you have an Enterprise Agreement or equivalent volume licensing agreement with Microsoft</caps:sentence>
              </para>
            </listItem>
          </list>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Sign up for a NEW account if either of the following is true:</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">Sign in with your WORK or SCHOOL account if:</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">
                          <embeddedLabel>You don’t have a work or school account.</embeddedLabel> A work or school account is provided when you sign a volume licensing agreement with Microsoft or subscribe to Office 365.</caps:sentence>
                        <caps:sentence id="src55" class="srcSentence"> If your organization has not signed an Enterprise Agreement or equivalent volume licensing agreement with Microsoft (or has an Office 365 account), then you do not have a Microsoft Online Services account that you can use to sign in to Microsoft Online Services.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">
                          <embeddedLabel>You will discard your Intune tenant after completing the 30-day trial.</embeddedLabel> You should sign up for a new account if you are using your <token>wit_nextref</token> free trial subscription for evaluation purposes only, and you plan to redo your <token>wit_nextref</token> service setup and device provisioning after the trial.</caps:sentence>
                        <caps:sentence id="src57" class="srcSentence"> This is the recommended option if you plan to use <token>wit_nextref</token> with System Center 2012 Configuration Manager.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src58" class="srcSentence">If you sign up for a new account, you cannot later use an existing work or school account to manage that account, or combine it with existing volume licensing agreements.</caps:sentence>
                    </para>
                  </alert>
                  <para></para>
                </TD>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src59" class="srcSentence">You have a work or school account provided with a volume licensing agreement or Office 365 subscription, and you are using this trial to evaluate <token>wit_nextref</token>.</caps:sentence>
                    </embeddedLabel>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src60" class="srcSentence">If you are setting up <token>wit_nextref</token> on an existing account, we recommend that you review <link xlink:href="3b4e778d-ac13-4c23-974f-5122f74626bc">Configure Microsoft Intune</link> before continuing with these steps.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
            </tbody>
          </table>
          <procedure address="BKMK_ToSignUpforSubscription" expanded="true">
            <title>
              <caps:sentence id="src61" class="srcSentence">Sign up or sign in to Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">First, <externalLink><linkText>click here to visit the Intune Sign up page</linkText><linkUri>https://portal.office.com/Signup/Signup.aspx?OfferId=40BE278A-DFD1-470a-9EF7-9F2596EA7FF9&amp;dl=INTUNE_A&amp;ali=1#0 </linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">On the <ui>Sign up</ui> page, sign in or sign up.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src64" class="srcSentence">If  you complete the sign-up process, you're automatically signed in to the <token>wit_icp_1</token> with the tenant administrator account.</caps:sentence>
                  <caps:sentence id="src65" class="srcSentence"> An email message that contains your account information is also sent to the email address that you provided during sign-up.</caps:sentence>
                  <caps:sentence id="src66" class="srcSentence"> This email confirms your subscription is active.</caps:sentence>
                  <caps:sentence id="src67" class="srcSentence"> If you sign in, you're automatically directed to the Intune admin portal.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ConfigureDomain">
        <title>
          <caps:sentence id="src68" class="srcSentence">Step 2: Configure a custom domain name</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src69" class="srcSentence">By default, <token>wit_firstref</token> uses the domain name that you select when you subscribe to the service, which looks like <ui>&lt;domain&gt;.onmicrosoft.com</ui>.</caps:sentence>
            <caps:sentence id="src70" class="srcSentence"> When your organization owns a custom domain, you can configure your instance of <token>wit_nextref</token> to use that domain instead of the domain name provided with your subscription.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src71" class="srcSentence">Before you create new user accounts or synchronize accounts from your on-premises Active Directory, we strongly recommend that you decide whether to use only the .onmicrosoft.com domain or to add one or more of your custom domain names.</caps:sentence>
            <caps:sentence id="src72" class="srcSentence"> If you don't configure a custom domain name and suffix, each user account you import receives the onmicrosoft.com suffix for its user principal name (UPN).</caps:sentence>
            <caps:sentence id="src73" class="srcSentence"> Configuring a custom domain before adding users can help simplify the management of user identities for your subscription by enabling users to sign in with the credentials they use to access other domain resources.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src74" class="srcSentence">Because the tasks to configure <token>wit_nextref</token> to use your organizations custom domain name are the same as for other Azure AD tenants, use the information and procedures found in <externalLink><linkText>Add your domain</linkText><linkUri>http://technet.microsoft.com/library/hh969247.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src75" class="srcSentence">For more information about using your custom domain with a cloud-based service from Microsoft, see <externalLink><linkText>Internet domain management</linkText><linkUri>http://technet.microsoft.com/library/hh969248.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src76" class="srcSentence">When you subscribe to a cloud-based service from Microsoft, your instance of that service becomes a tenant of Microsoft Azure Active Directory (Azure AD), which provides identity and directory services for your cloud-based service.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src77" class="srcSentence">For more information about your Azure AD tenant, see <externalLink><linkText>What is an Azure AD tenant?</linkText><linkUri>http://technet.microsoft.com/library/jj573650.aspx</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section address="BKMK_SyncUsersFromAD">
        <title>
          <caps:sentence id="src78" class="srcSentence">Step 3: Synchronize Active Directory and add users to Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src79" class="srcSentence">As mentioned, you can configure directory synchronization to import user accounts from your on-premises Active Directory to Microsoft Azure Active Directory.</caps:sentence>
            <caps:sentence id="src80" class="srcSentence"> Additionally, when you activate directory synchronization in your Intune tenant, you are turning on this feature across  all the Microsoft cloud services that you are subscribed to.</caps:sentence>
            <caps:sentence id="src81" class="srcSentence"> When you use multiple services with the same Azure AD, the user accounts that you synchronize are available to each cloud-based service that shares your Azure AD.</caps:sentence>
            <caps:sentence id="src82" class="srcSentence"> Having your on-premises Active Directory service connected with all of your Azure Active Directory-based services makes managing user identity much simpler.</caps:sentence>
            <caps:sentence id="src83" class="srcSentence"> You can also configure single sign-on features to make the authentication experience for your users familiar and easy.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src84" class="srcSentence">The <externalLink><linkText>Azure AD Connect wizard</linkText><linkUri>https://www.microsoft.com/download/details.aspx?id=47594</linkUri></externalLink> is the single tool and guided experience for connecting your on-premises identity infrastructure to the cloud.</caps:sentence>
            <caps:sentence id="src85" class="srcSentence">  Choose your topology and needs (single or multiple directories, password sync or federation), and the wizard will deploy and configure all components required to get your connection up and running, including sync services, Active Directory Federation Services (AD FS), and the Azure AD PowerShell module.</caps:sentence>
            <caps:sentence id="src86" class="srcSentence"> Azure AD Connect encompasses functionality that was previously released as Dirsync and Azure AD Sync.</caps:sentence>
            <caps:sentence id="src87" class="srcSentence"> Learn more about directory integration at <externalLink><linkText>Directory integration</linkText><linkUri>http://technet.microsoft.com/library/jj573653.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src88" class="srcSentence">After you've added users to your Intune subscription, we recommend that you grant a few user accounts administrative credentials.</caps:sentence>
            <caps:sentence id="src89" class="srcSentence"> The console that you use to assign administrative credentials depends on the type of administrator you want to assign:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src90" class="srcSentence">
                  <embeddedLabel>Tenant administrator</embeddedLabel>: Use the <embeddedLabel><token>wit_icp_1</token></embeddedLabel> to assign this type of administrator to manage your subscription, including billing, cloud storage, and managing the users who can use <token>wit_nextref</token>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src91" class="srcSentence">
                  <embeddedLabel>Service administrator</embeddedLabel>: Use the <embeddedLabel><token>wit_adminconsole</token></embeddedLabel> to assign this type of administrator for day-to-day tasks including management of mobile devices or computers, deploying policy or software, and running reports.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src92" class="srcSentence">To learn more about administrator accounts, see <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268#BKMK_AdminAccounts">Intune administrator accounts</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src93" class="srcSentence">To learn about the benefits of synchronizing user accounts from your local directory to Azure AD, see <externalLink><linkText>Similarities between Active Directory and Azure AD</linkText><linkUri>http://technet.microsoft.com/library/dn518177.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_AssignWitLicenses">
        <title>
          <caps:sentence id="src94" class="srcSentence">Step 4: Manage Intune licenses</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src95" class="srcSentence">A user must have a license to your Intune subscription before they can sign in to use the service.</caps:sentence>
            <caps:sentence id="src96" class="srcSentence"> When users have a license, they are a member of the <token>wit_firstref</token> user group.</caps:sentence>
            <caps:sentence id="src97" class="srcSentence"> This group includes all users who have a license to use the subscription.</caps:sentence>
            <caps:sentence id="src98" class="srcSentence">
              <embeddedLabel>Each user license supports enrolling up to five devices</embeddedLabel>.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src99" class="srcSentence">
                  <embeddedLabel>When you use the <token>wit_icp_2</token> to add users</embeddedLabel> to your subscription, either manually or by bulk import from a CSV file, <token>wit_nextref</token> assigns an available license to each user account.</caps:sentence>
                <caps:sentence id="src100" class="srcSentence"> If you do not have an available license, then no license is assigned.</caps:sentence>
                <caps:sentence id="src101" class="srcSentence"> With both methods, you have the option to not assign licenses to the new user accounts at the time you add them to your subscription.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src102" class="srcSentence">
                  <embeddedLabel>When you import users from your on-premises Active Directory</embeddedLabel>, <token>wit_nextref</token> does not assign a license to each user account.</caps:sentence>
                <caps:sentence id="src103" class="srcSentence"> Instead, at a later time, you must edit the user account to assign a license to the user.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src104" class="srcSentence">
                  <embeddedLabel>When your subscription shares Azure AD with other Azure AD tenants</embeddedLabel>, you have access to users that were added to those services.</caps:sentence>
                <caps:sentence id="src105" class="srcSentence"> These users do not have a license to <token>wit_nextref</token> until you assign a license to each of them.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src106" class="srcSentence">If the option to assign or revoke a license to <token>wit_nextref</token> is disabled, your subscription might include volume licensing options, such as the options available when using <externalLink><linkText>Enterprise Mobility Suite</linkText><linkUri>http://www.microsoft.com/server-cloud/products/enterprise-mobility-suite/default.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence id="src107" class="srcSentence"> For information on how to assign or revoke licenses, see the documentation for your licensing options.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="Step3" expanded="true">
        <title>
          <caps:sentence id="src108" class="srcSentence">Step 5: Create groups to organize users and devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src109" class="srcSentence">Groups in <token>wit_nextref</token> give you great flexibility for managing your devices and users.</caps:sentence>
            <caps:sentence id="src110" class="srcSentence"> You can set up groups to suit your organizational needs (for example, by geographic location, department, or hardware characteristics) and use them to perform a wide variety of administrative tasks, from deploying policies for a set of users to deploying applications to a set of devices.</caps:sentence>
          </para>
          <para></para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src111" class="srcSentence">Create a device group</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src112" class="srcSentence">Use device groups to deploy apps and updates, and configure other features.</caps:sentence>
                <caps:sentence id="src113" class="srcSentence"> For example, set up a "My Devices" group using the following steps:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>Overview</ui> &gt; <ui>Create Group</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">For the <embeddedLabel>Group name</embeddedLabel>, type “My Devices” and, from the parent group list, select <embeddedLabel>All Devices</embeddedLabel>, and then click <ui>Next</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">On the <ui>Define Membership Criteria</ui> page, select <embeddedLabel>All devices</embeddedLabel> to indicate that the group includes both mobile devices and computers.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">On the <ui>Define Direct Membership</ui> page, click <embeddedLabel>Next</embeddedLabel>.</caps:sentence>
                    <caps:sentence id="src118" class="srcSentence"> If you previously created a group that did not include all devices, and you wanted to add specific devices to your new group, you can do that here.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">On the <ui>Summary</ui> page, review the actions that will be taken, and then click <ui>Finish</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src120" class="srcSentence">You can find the newly created group in the <ui>Groups</ui> list, in the <ui>Groups</ui> workspace, under <embeddedLabel>All Devices</embeddedLabel>.</caps:sentence>
                <caps:sentence id="src121" class="srcSentence"> From here, you can also edit or delete the group.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src122" class="srcSentence">Create a user group</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src123" class="srcSentence">Use user groups to deploy software and device policies.</caps:sentence>
                <caps:sentence id="src124" class="srcSentence"> For example, set up an "Intune Users" group using the following steps:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>Overview</ui> &gt; <ui>Create Group</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">For the <embeddedLabel>Group name</embeddedLabel>, type “Intune Users” and, from the parent group list, select <embeddedLabel>All Users</embeddedLabel>, and then click <ui>Next</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">On the <ui>Define Membership Criteria</ui> page, set <ui>Start group membership with</ui> to <ui>All users in the Parent group</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">Beside <embeddedLabel>Exclude members from these security groups</embeddedLabel>, click <embeddedLabel>Browse</embeddedLabel> and then select <ui>Company Administrator</ui>.</caps:sentence>
                    <caps:sentence id="src129" class="srcSentence"> This exclusion lets you manage the Intune Users group without affecting the Company Administrator account (also known as the tenant administrator).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">On the <ui>Define Direct Membership</ui> page, click <embeddedLabel>Next</embeddedLabel>.</caps:sentence>
                    <caps:sentence id="src131" class="srcSentence"> You don’t need to do anything here because you want the Intune Users group to include all users, except for the Company Administrator.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">On the <ui>Summary</ui> page, review the actions that will be taken, and then click <ui>Finish</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src133" class="srcSentence">You can find the newly created group in the <ui>Groups</ui> list, in the <ui>Groups</ui> workspace, under <embeddedLabel>All Users</embeddedLabel>.</caps:sentence>
                <caps:sentence id="src134" class="srcSentence"> From here, you can also edit or delete the group.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src135" class="srcSentence">To learn more about using groups, see <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use Groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="Step4" expanded="true">
        <title>
          <caps:sentence id="src136" class="srcSentence">Step 6: Create policies and publish an app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src137" class="srcSentence">
              <token>wit_nextref</token> policies provide settings that help you control the security settings on mobile devices, maintain Windows Firewall and Endpoint Protection settings for computers, and deploy applications.</caps:sentence>
            <caps:sentence id="src138" class="srcSentence"> If you are planning to use Intune for devices that you configure for production use after the trial, it's absolutely essential that you follow the instructions in <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure policy for mobile devices in Microsoft Intune</link> and <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src139" class="srcSentence">You can perform two types of app installations using Intune.</caps:sentence>
            <caps:sentence id="src140" class="srcSentence"> The first is a <legacyBold>required install</legacyBold>, which automatically deploys the app to managed computers.</caps:sentence>
            <caps:sentence id="src141" class="srcSentence"> The other is an <legacyBold>available install</legacyBold>, which deploys the app, or a link to the app, to the Intune company portal so that users can choose whether to install it on their computers or on their mobile devices.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src142" class="srcSentence">Before using Intune to deploy apps, make sure that you have the appropriate licenses to publish, distribute, and use the app.</caps:sentence>
            <caps:sentence id="src143" class="srcSentence"> The Licenses workspace lets you add and manage license agreement information for apps or software purchased through Microsoft Volume Licensing agreements, and for Microsoft or non-Microsoft software that was purchased by other means.</caps:sentence>
            <caps:sentence id="src144" class="srcSentence"> You can then create license reports that display managed license usage information throughout your company to stay informed of license usage activity.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src145" class="srcSentence">In these steps, you'll set up a mobile device configuration policy and a Windows computer firewall policy, and configure Skype as an available install for mobile devices after they're enrolled.</caps:sentence>
            <caps:sentence id="src146" class="srcSentence"> After you add and deploy a new policy, all users or devices in the group to which you deployed the policy inherit the settings as their baseline policy.</caps:sentence>
            <caps:sentence id="src147" class="srcSentence"> You can always review and edit the details of these policies later from the Policy workspace.</caps:sentence>
          </para>
          <procedure expanded="true">
            <title>
              <caps:sentence id="src148" class="srcSentence">Create and deploy a mobile device configuration policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">Open the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">In the left pane, click the <ui>Policy</ui> icon.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">In the <ui>Tasks</ui> list on the <ui>Policy Overview</ui> page, click <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src152" class="srcSentence"> In the policy list, expand the platform you want to create a policy for, then select <ui>General Configuration</ui>, choose <ui>Create and Deploy a Policy with the Recommended Settings</ui>, and then click <ui>Create Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">When prompted to <ui>Select the groups to which you want to deploy this policy</ui>, select <ui>My Trial Users</ui> from the list, and click <ui>Add</ui> &gt; <ui>OK</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src154" class="srcSentence">Your policy appears in the list of configuration policies, and has been deployed to the <ui>My Trial Users</ui> group.</caps:sentence>
                  <caps:sentence id="src155" class="srcSentence"> Double-click the policy to view its settings.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="true">
            <title>
              <caps:sentence id="src156" class="srcSentence">Publish the Skype app for mobile devices</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click the <ui>Apps</ui> icon, then click <ui>Apps</ui> &gt; <ui>Add App</ui>.</caps:sentence>
                    <caps:sentence id="src158" class="srcSentence"> If prompted, enter your <token>wit_nextref</token> credentials.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src159" class="srcSentence">When you start the <embeddedLabel>Intune Software Publisher</embeddedLabel> for the first time, a short delay occurs while the application is installed.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">
                Review the security warning and click <ui>Run</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">On the <ui>Before you begin</ui> page, click <ui>Next</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">On the <ui>Software setup</ui> page in <ui>Select how this software is made available to devices</ui>, select <ui>External link</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">Enter the external link for the software in <ui>Specify the URL</ui>, and then click <ui>Next</ui>.</caps:sentence>
                    <caps:sentence id="src164" class="srcSentence"> Make sure that you preface the URL with <legacyBold>http://</legacyBold>.</caps:sentence>
                    <caps:sentence id="src165" class="srcSentence"> For the Skype app, use the link below that matches the mobile device platform you're using:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src166" class="srcSentence">
                          <embeddedLabel>iOS:</embeddedLabel> <externalLink><linkText>https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8</linkText><linkUri>https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src167" class="srcSentence">
                          <embeddedLabel>Android:</embeddedLabel> <externalLink><linkText>https://play.google.com/store/apps/details?id=com.skype.raider</linkText><linkUri>https://play.google.com/store/apps/details?id=com.skype.raider</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src168" class="srcSentence">
                          <embeddedLabel>Windows Phone 8 or Windows Phone 8.1:</embeddedLabel> <externalLink><linkText>http://www.windowsphone.com/en-us/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</linkText><linkUri>http://www.windowsphone.com/en-us/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">On the <ui>Software description</ui> page, provide the information that you want users to see in the company portal for the software, and then click <ui>Next</ui>.</caps:sentence>
                    <caps:sentence id="src170" class="srcSentence"> The following settings are available (this example refers to Skype):</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src171" class="srcSentence">
                          <legacyBold>Publisher:</legacyBold> Enter the name of the publisher, "Microsoft" </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src172" class="srcSentence">
                          <legacyBold>Name: </legacyBold>Enter <embeddedLabel>Skype</embeddedLabel></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src173" class="srcSentence">
                          <legacyBold>Description:</legacyBold> Enter a description for the software, such as <embeddedLabel>Skype communication app</embeddedLabel> </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src174" class="srcSentence">
                          <legacyBold>Category: </legacyBold>Select the category that best fits this software, such as <embeddedLabel>Collaboration</embeddedLabel></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src175" class="srcSentence">
                          <legacyBold>Display this as a featured app and highlight it in the company portal:</legacyBold> Select this option to display the app prominently in the company portal on mobile devices.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src176" class="srcSentence">
                          <legacyBold>Icon: </legacyBold>Choose whether to associate an icon with the software.</caps:sentence>
                        <caps:sentence id="src177" class="srcSentence"> The maximum size for the icon is 250 x 250 pixels.</caps:sentence>
                        <caps:sentence id="src178" class="srcSentence"> The recommended size is 32 x 32 pixels.</caps:sentence>
                        <caps:sentence id="src179" class="srcSentence"> This setting is optional for the Intune trial tenant.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">On the <ui>Summary</ui> page, verify the software information, and then click <ui>Upload</ui>.</caps:sentence>
                    <caps:sentence id="src181" class="srcSentence"> Click <ui>Close</ui> to exit the wizard.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Apps</ui> &gt; <ui>Apps</ui> &gt; <ui>Skype</ui> &gt; <ui>Manage Deployment</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">On the <ui>Select Groups</ui> page, select <ui>My Trial Users</ui> to deploy the software to that user group, and then click <ui>Add</ui> &gt; <ui>Next</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">On the <ui>Deployment Action</ui> page, select <ui>Available Install</ui> from the <ui>Approval</ui> column for your group.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src185" class="srcSentence">Click <ui>Finish</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src186" class="srcSentence">The Skype app is now available to install on mobile devices from the company portal, but first you need to install <token>wit_nextref</token> software on computers and mobile devices.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ConfigureCompanyPortal">
        <title>
          <caps:sentence id="src187" class="srcSentence">Step 7: Customize the company portal</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src188" class="srcSentence">The <token>wit_iwportal_1</token> is where users access company data and can do common tasks like enrolling devices, installing apps, and locating information for assistance from your IT department.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src189" class="srcSentence">When you customize the company portal, the configurations apply to both the company portal website and company portal apps.</caps:sentence>
          </para>
          <procedure expanded="true" address="BKMK_ToCustomizeCompanyPortal">
            <title>
              <caps:sentence id="src190" class="srcSentence">Settings for customizing the company portal</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administrator console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Company Portal</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">Configure one or more of the following optional items.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src193" class="srcSentence">Configuration area</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src194" class="srcSentence">Field name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src195" class="srcSentence">Maximum character length</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src196" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD rowspan="6">
                          <para>
                            <caps:sentence id="src197" class="srcSentence">Company contact information and privacy statement</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src198" class="srcSentence">Company name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src199" class="srcSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src200" class="srcSentence">This name is displayed as the title of the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src201" class="srcSentence">IT department contact name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src202" class="srcSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src203" class="srcSentence">This name is displayed on the <ui>Contact IT</ui> page.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src204" class="srcSentence">IT department phone number</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src205" class="srcSentence">20</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src206" class="srcSentence">This contact number is displayed on the <ui>Contact IT</ui> page.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src207" class="srcSentence">IT department email address</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src208" class="srcSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src209" class="srcSentence">This contact address is displayed on the <ui>Contact IT</ui> page.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src210" class="srcSentence">You must enter a valid email address in the format <userInput>alias@domainname.com</userInput>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src211" class="srcSentence">Additional information</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src212" class="srcSentence">120</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src213" class="srcSentence">Displayed on the <ui>Contact IT</ui> page.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src214" class="srcSentence">Company privacy statement URL</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src215" class="srcSentence">79</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src216" class="srcSentence">You can specify your own company privacy statement that appears when users click the privacy links from the company portal.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src217" class="srcSentence">You must enter a valid URL in the format <userInput>https://www.contoso.com</userInput>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD rowspan="2">
                          <para>
                            <caps:sentence id="src218" class="srcSentence">Support contacts</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src219" class="srcSentence">Support website URL</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src220" class="srcSentence">150</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src221" class="srcSentence">If you have a support website that you want your users to use, specify the URL here.</caps:sentence>
                            <caps:sentence id="src222" class="srcSentence"> The URL must be in the format <userInput>https://www.contoso.com</userInput>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src223" class="srcSentence">If you don't specify a URL, nothing is displayed for the support website on the <ui>Contact IT</ui> page in the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src224" class="srcSentence">Website name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src225" class="srcSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src226" class="srcSentence">This name is the friendly name that is displayed for the URL to the support website.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src227" class="srcSentence">If you specify a support website URL and no friendly name, then <ui>Go to IT website</ui> is displayed on the <ui>Contact IT</ui> page in the company portal.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD rowspan="3">
                          <para>
                            <caps:sentence id="src228" class="srcSentence">Customization</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src229" class="srcSentence">Theme color</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src230" class="srcSentence">Not applicable</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src231" class="srcSentence">Select a theme color to apply to the company portal.</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src232" class="srcSentence">Include company logo</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src233" class="srcSentence">Not applicable</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src234" class="srcSentence">When you enable this option, you can upload your company logo to show in your company portal.</caps:sentence>
                            <caps:sentence id="src235" class="srcSentence"> You can upload two logos:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src236" class="srcSentence">One logo that is displayed when the company portal background is white</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src237" class="srcSentence">One logo that is displayed when the company portal background uses your selected theme color</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence id="src238" class="srcSentence">Each logo must be a .png or .jpg file type and meet the following criteria:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src239" class="srcSentence">Maximum resolution of 400 x 100 pixels</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src240" class="srcSentence">Size of 750 KB or less</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src241" class="srcSentence">Choose a background for <token>win8_client_2</token> company portal app</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src242" class="srcSentence">Not applicable</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src243" class="srcSentence">This setting affects the background for the <token>win8_client_2</token> company portal app only.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">Click <ui>Save</ui> to save your changes.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src245" class="srcSentence">After you save your changes, you can use the links provided at the bottom of the <ui>Company Portal</ui> page of the administration console to view the company portal website.</caps:sentence>
                  <caps:sentence id="src246" class="srcSentence"> These links cannot be changed.</caps:sentence>
                  <caps:sentence id="src247" class="srcSentence"> When a user signs in, these links display your subscriptions in the company portal.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="Step5" expanded="true">
        <title>
          <caps:sentence id="src248" class="srcSentence">Step 8: Enroll computers in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src249" class="srcSentence">You can install the <token>wit_nextref</token> client software on computers in the following ways:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src250" class="srcSentence">Users can use an installer provided by the administrator to manually enroll</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src251" class="srcSentence">
                  <token>wit_nextref</token> software can be included in an OS image or deployed using Group Policy</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src252" class="srcSentence">End users can also self-enroll their devices through the <token>wit_firstref</token> company portal</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src253" class="srcSentence">Each enrolled computer is linked to the user account that was used to install the client software.</caps:sentence>
            <caps:sentence id="src254" class="srcSentence"> Microsoft Intune Endpoint Protection is also installed by default during Intune client installation on computers.</caps:sentence>
            <caps:sentence id="src255" class="srcSentence"> Endpoint Protection helps to secure the computers in your organization by providing real-time protection against potential threats, keeping malicious software definitions up to date, and automatically running scheduled scans.</caps:sentence>
            <caps:sentence id="src256" class="srcSentence"> For added security, you can also use Intune policies to manage Windows Firewall settings on managed computers.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src257" class="srcSentence">What to know before you start:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src258" class="srcSentence">The user must be an administrator on the computer to install the client software.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src259" class="srcSentence">Self-enrolling requires that Internet Explorer is installed on the client computer.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src260" class="srcSentence">Each time a user self-enrolls a computer, it uses a <token>wit_firstref</token> license.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src261" class="srcSentence">You must use a Microsoft Online Services work or school account to self-enroll a computer.</caps:sentence>
                <caps:sentence id="src262" class="srcSentence"> This is the account that you used to sign in, or the administrator account that was created when you signed up for the free trial.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src263" class="srcSentence">For this example, you'll use the self-enrollment approach:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src264" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Company Portal</ui>, and then scroll to the bottom of the screen.</caps:sentence>
                <caps:sentence id="src265" class="srcSentence"> Copy the URL shown under <ui>Intune company portal</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src266" class="srcSentence">Use Internet Explorer to browse to the company portal URL that you acquired in the previous step, and log in with your administrator credentials.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src267" class="srcSentence">Click <ui>Add Device</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src268" class="srcSentence">Click <ui>Download Software</ui> and then click <ui>Run</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src269" class="srcSentence">Click <ui>Next</ui> to start the <token>wit_firstref</token> Setup wizard.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src270" class="srcSentence">When the Setup wizard has completed, click <ui>Finish</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src271" class="srcSentence">To learn more about computer management using <token>wit_nextref</token>, see <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be managed by Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src272" class="srcSentence">To learn more about software management using <token>wit_nextref</token>, see <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Manage software with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="Step6" expanded="true">
        <title>
          <caps:sentence id="src273" class="srcSentence">Step 9: Enroll mobile devices and install an app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src274" class="srcSentence">To set up mobile device management with Intune, you must  first set the mobile device management authority,  enable management for device platforms, and enroll your devices with the company portal app.</caps:sentence>
            <caps:sentence id="src275" class="srcSentence"> You can then deploy the Microsoft Skype application that you published.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src276" class="srcSentence">Enable device management and enroll devices</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src277" class="srcSentence">
                      <embeddedLabel>Make Intune your mobile device management authority</embeddedLabel>
                      <br />In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui>, and click <ui>Set MDM Authority</ui> under <ui>Tasks</ui>.</caps:sentence>
                    <caps:sentence id="src278" class="srcSentence">  Click <ui>Yes</ui> in the MDM Authority dialog box.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">
                      <embeddedLabel>Enable MDM for your device platform</embeddedLabel>
                      <br />Enable mobile device management for the device platform you want to manage.</caps:sentence>
                    <caps:sentence id="src280" class="srcSentence"> Depending on your platform, different requirements are needed:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src281" class="srcSentence">
                          <embeddedLabel>iOS and Mac OS X</embeddedLabel>: see <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Set up iOS management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src282" class="srcSentence">
                          <embeddedLabel>Windows Phone</embeddedLabel>: see <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Set up Windows Phone management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src283" class="srcSentence">
                          <embeddedLabel>Android</embeddedLabel>: Android mobile devices allow users to enroll using the company portal app available from Google Play.</caps:sentence>
                        <caps:sentence id="src284" class="srcSentence"> No additional configuration in Intune is required.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src285" class="srcSentence">
                      <embeddedLabel>Enroll devices</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src286" class="srcSentence">
                          <embeddedLabel>Android</embeddedLabel> - Install the <ui>Intune Company Portal</ui> app from Microsoft Corporation available on <externalLink><linkText>Google Play</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkId=386612</linkUri></externalLink> and sign in with the Intune user credentials added above.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src287" class="srcSentence">
                          <embeddedLabel>iOS and Mac OS X</embeddedLabel> - Install the <ui>Microsoft Intune Company Portal</ui> app from Microsoft Corporation available in the App Store and sign in with the Intune user credentials added above.</caps:sentence>
                        <caps:sentence id="src288" class="srcSentence"> View <ui>Enrolled devices</ui> to add your device.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src289" class="srcSentence">
                          <embeddedLabel>Windows Phone 8.1</embeddedLabel>- Users install the <ui>Company Portal</ui> app from Microsoft Corporation available in the Windows Phone store and sign in with the Intune user credentials added above.</caps:sentence>
                        <caps:sentence id="src290" class="srcSentence">  View <ui>Enrolled devices</ui> to add your device.<ui></ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src291" class="srcSentence">
                          <embeddedLabel>Windows Phone 8.0 </embeddedLabel> - Users click <ui>system settings</ui> &gt; <ui>company apps</ui>, and sign in with Intune user credentials added above.</caps:sentence>
                        <caps:sentence id="src292" class="srcSentence"> The company portal app is deployed to your phone.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src293" class="srcSentence">If prompted for a <ui>Server address</ui>, type “manage.microsoft.com”.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src294" class="srcSentence">Open the company portal on the mobile device, choose <ui>Apps</ui>, and then install <ui>Microsoft Skype</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence id="src295" class="srcSentence">To learn more about mobile device management using <token>wit_nextref</token>, see <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage Mobile Devices with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src296" class="srcSentence">Post-configuration tasks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src297" class="srcSentence">After you complete the initial configuration steps for an Intune  paid subscription, you should consider enabling additional mobile device management functionality.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src298" class="srcSentence">
                  <legacyBold>Connect Exchange to Intune:</legacyBold> For users with mobile devices  that haven't  enrolled in Intune, you can enable Exchange ActiveSync management using a connector for on-premises Exchange and for Exchange Online in  Microsoft Office 365.</caps:sentence>
                <caps:sentence id="src299" class="srcSentence"> The Exchange connector connects you with your Exchange deployment and lets you manage mobile devices through the Intune administration console.</caps:sentence>
                <caps:sentence id="src300" class="srcSentence"> To learn more about the Exchange connector, see <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Mobile device management with Exchange ActiveSync and Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src301" class="srcSentence">
                  <legacyBold>Intune reports:</legacyBold> Microsoft Intune provides alerts and reports that you can use to help monitor devices, as well as software license status and actions that affect devices (such as wiping a device).</caps:sentence>
                <caps:sentence id="src302" class="srcSentence">  To learn more about reporting, see <link xlink:href="0f7dc155-cb8e-477b-ba02-2623194a9575">Monitoring and reporting with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src303" class="srcSentence">
                  <legacyBold>Protecting company resources:</legacyBold>  After you've configured Intune and enrolled your devices, you'll want to make sure that you're protecting devices against data loss and other threats.</caps:sentence>
                <caps:sentence id="src304" class="srcSentence"> To learn more about protecting resources, see <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1bfd1a23-681d-4cc8-834c-c7856d69d409">Get started with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>