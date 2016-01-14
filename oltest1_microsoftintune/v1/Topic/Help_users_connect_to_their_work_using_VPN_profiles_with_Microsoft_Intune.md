---
description: na
keywords: na
title: Help users connect to their work using VPN profiles with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: abc57093-7351-408f-9f41-a30877f96f73
---
# Unterst&#252;tzen von Benutzern beim Verbinden mit ihrer Arbeit &#252;ber VPN-Profile in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a24cf28d4cc042111a8c3b2f736f7bd1" id="tgt1" class="tgtSentence">Über virtuelle private Netzwerke (VPN) können Sie Benutzern sicheren Remotezugriff mit Ihr Unternehmensnetzwerk bieten.</caps:sentence>
          <caps:sentence sentenceid="573cd02596f9fa32a75f1899655150ed" id="tgt2" class="tgtSentence"> Remotebenutzer können genau so arbeiten wie bei einer physischen Verbindung des Geräts mit dem Netzwerk.</caps:sentence>
          <caps:sentence sentenceid="6de470fd8773fc94425fd1c326ecbe3e" id="tgt3" class="tgtSentence"> Geräte verwenden ein VPN-Verbindungsprofil, um eine Verbindung mit dem VPN-Server zu initiieren.</caps:sentence>
          <caps:sentence sentenceid="fc02dd52874869ac12169eb9b5c2d73a" id="tgt4" class="tgtSentence">
            <ui>VPN-Profile</ui> in <token>wit_firstref</token> ermöglichen Ihnen die Bereitstellung von VPN-Einstellungen für Benutzer und Geräte in Ihrer Organisation.</caps:sentence>
          <caps:sentence sentenceid="e9cb44488c71123529ab22933a704709" id="tgt5" class="tgtSentence"> Durch Bereitstellen dieser Einstellungen erleichtern Sie dem Endbenutzer das Verbinden mit Ressourcen im Unternehmensnetzwerk.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0ad14a47ad91828dc064332d4b71185d" id="tgt6" class="tgtSentence">Sie möchten z. B. allen iOS-Geräten, die Einstellungen zur Verfügung stellen, die zum Verbinden mit einer Dateifreigabe im Unternehmensnetzwerk erforderlich sind.</caps:sentence>
          <caps:sentence sentenceid="5c0abb58cb84a25ae056ba7cb98185f9" id="tgt7" class="tgtSentence"> Sie erstellen ein VPN-Profil mit den Einstellungen, die zum Herstellen einer Verbindung mit dem Unternehmensnetzwerk erforderlich sind, und stellen dieses Profil dann für alle Benutzer mit iOS-Geräten bereit.</caps:sentence>
          <caps:sentence sentenceid="275d49e616e5a77b79ace08bbdc57225" id="tgt8" class="tgtSentence"> Die Benutzer sehen die VPN-Verbindung in der Liste der verfügbaren Netzwerke und können mit geringem Aufwand eine Verbindung herstellen.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="776fc50fa60229ec7e609e77e32e6d5b" id="tgt9" class="tgtSentence">Sie können die folgenden Gerätetypen mit VPN-Profilen konfigurieren:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="7c4ad09da3590127d1fc36d19c68aa69" id="tgt10" class="tgtSentence">Geräte unter Android 4 und höher</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="fb307f525a2ea563bfea7bb195c5315b" id="tgt11" class="tgtSentence">Geräte unter iOS 7.1 und höher</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c8d94982d52ad1105480aebf687a1f96" id="tgt12" class="tgtSentence">Geräte unter Mac OS X 10.9 und höher</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8df056569b600a5ccbd9c4db333c678e" id="tgt13" class="tgtSentence">Registrierte Geräte unter Windows 8.1 und höher (einschließlich Windows RT 8.1)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4382915ece0faf46c29a8bb3f2c26512" id="tgt14" class="tgtSentence">Geräte unter Windows Phone 8.1 und höher</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a4e0867f03af341c21b32a9a3fba8fa2" id="tgt15" class="tgtSentence">Geräte unter Windows 10 Desktop und Mobile.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="4b233b626dbecdb7bd8ec0c0f377f5f2" id="tgt16" class="tgtSentence">Die Konfigurationsoptionen für VPN-Profile variieren je nach gewähltem Gerätetyp.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="1df1405f3a1e92fb02874775cd4fd3e9" id="tgt17" class="tgtSentence">VPN-Verbindungstypen</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c567e2eab55155de19e684e269a67535" id="tgt18" class="tgtSentence">
              <token>wit_nextref</token> unterstützt die Erstellung von VPN-Profilen mit den folgenden Verbindungstypen:</caps:sentence>
          </para>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="286b9c555b9c759f1c2c6d8f981dd2a0" id="tgt19" class="tgtSentence">Verbindungstyp</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="e4086d56995ffa234681830d0bb565e2" id="tgt20" class="tgtSentence">iOS und Mac OS X</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="c31b32364ce19ca8fcd150a417ecce58" id="tgt21" class="tgtSentence">Android</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="4693857bd32521105efeea9c79338cde" id="tgt22" class="tgtSentence">Windows Phone 8.1</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt23" class="tgtSentence">Windows 8.1 und Windows RT 8.1</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="95e97f7b7eac8dbf3f8cda1896f56d6e" id="tgt24" class="tgtSentence">Windows 10 Desktop und Mobile</caps:sentence>
                    </ui>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="af700334209a6353f1ef1355c3dcb370" id="tgt25" class="tgtSentence">Cisco AnyConnect</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt26" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt27" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt28" class="tgtSentence">Nein</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt29" class="tgtSentence">Nein</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt30" class="tgtSentence">Nein</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bca47433892229a424f00706cd00694d" id="tgt31" class="tgtSentence">Pulse Secure</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt32" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt33" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt34" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt35" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt36" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2b5febecd6b7c38d5211d4aa9bcb4f12" id="tgt37" class="tgtSentence">F5 Edge Client</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt38" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt39" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt40" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt41" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt42" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3f7901f848d6f7e138dfb72a65f7bc48" id="tgt43" class="tgtSentence">Dell SonicWALL Mobile Connect</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt44" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt45" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt46" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt47" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt48" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c7ddd6c2147e3937318a4c09a2ed7da5" id="tgt49" class="tgtSentence">CheckPoint Mobile VPN</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt50" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt51" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt52" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt53" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt54" class="tgtSentence">Ja</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="067201dc292131ce0abe2dc33d5f195d" id="tgt55" class="tgtSentence">Vor der Verwendung von VPN-Profilen, die auf einem Gerät bereitgestellt werden, müssen Sie die entsprechende VPN-App für das Profil installieren.</caps:sentence>
              <caps:sentence sentenceid="83662ea5e9327f89ce6f9f7c7c217ee0" id="tgt56" class="tgtSentence"> Sie können die Informationen im Thema <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy apps to mobile devices in Microsoft Intune</link> verwenden, um Unterstützung bei der Bereitstellung der entsprechenden Anwendung mit <token>wit_nextref</token> zu erhalten.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c3dac5173e82c880a988bbbd2ec1c2fd" id="tgt57" class="tgtSentence">Schutz von VPN-Profilen</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5c46431cbdfab26261c98530c3bc500b" id="tgt58" class="tgtSentence">VPN-Profile können eine Reihe verschiedener Verbindungstypen und Protokolle von unterschiedlichen Herstellern verwenden.</caps:sentence>
            <caps:sentence sentenceid="5a55a92f35b746c5f34b6a26bb785f5e" id="tgt59" class="tgtSentence"> Diese Verbindungen werden in der Regel mit einer von zwei Methoden gesichert:</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="3cc41d0f46073ba8d93ea9db2412437f" id="tgt60" class="tgtSentence">Zertifikate</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="dda378d51261697005d8a027f6bd5495" id="tgt61" class="tgtSentence">Beim Erstellen des VPN-Profils wählen Sie ein SCEP- oder PFX-Zertifikatprofil aus, das Sie zuvor in <token>wit_nextref</token> erstellt haben.</caps:sentence>
                <caps:sentence sentenceid="eebc7d7cc400394517a55d0f5285ecf6" id="tgt62" class="tgtSentence"> Dieses wird als Identitätszertifikat bezeichnet und dient zur Authentifizierung anhand eines von Ihnen erstellten vertrauenswürdigen Zertifikatprofils (oder eines Stammzertifikats), mit dem überprüft wird, ob das Gerät des Benutzers eine Verbindung herstellen darf.</caps:sentence>
                <caps:sentence sentenceid="65f78562e11e363146f0368d0704976c" id="tgt63" class="tgtSentence"> Das vertrauenswürdige Zertifikat wird auf dem Computer bereitgestellt, der die VPN-Verbindung authentifiziert, in der Regel ist dies der VPN-Server.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="198c7ccd0551d655adebd871142138f6" id="tgt64" class="tgtSentence">Weitere Informationen zum Erstellen und Verwenden von Zertifikatprofilen in <token>wit_nextref</token> finden Sie unter <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0">Use Microsoft Intune Certificate Profiles to secure access to company resources</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="c161342ed0cc808adf28882c27a83f4f" id="tgt65" class="tgtSentence">Benutzername und Kennwort</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="bb0babed61b9ec76720b90de4d22d85d" id="tgt66" class="tgtSentence">Der Benutzer authentifiziert sich beim VPN-Server durch Angabe seines Benutzernamens und Kennworts.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="81c12061a9cc687079192eb6f7e757c1" id="tgt67" class="tgtSentence">Erstellen eines VPN-Profils</caps:sentence>
        </title>
        <content>
          <para></para>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt68" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink> auf <ui>Richtlinie</ui> &gt; <ui>Richtlinie hinzufügen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b6b168a63329fee87145b625df229e46" id="tgt69" class="tgtSentence">Wählen Sie eine Vorlage für die neue Richtlinie aus, indem Sie den entsprechenden Gerätetyp erweitern, und wählen Sie dann das VPN-Profil für dieses Gerät aus:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3011ca4e29a61054036542c635b2f1da" id="tgt70" class="tgtSentence">VPN-Profil (Android 4 und höher)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f9e59745c95cff52cc47f5df1fc53c94" id="tgt71" class="tgtSentence">VPN-Profil (iOS 7.1 und höher)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c5726158dd0a1a730b706bf1090b5b57" id="tgt72" class="tgtSentence">VPN-Profil (Mac OS X 10.9 und höher)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4d34dae81c9c0a7a04e31846574da65c" id="tgt73" class="tgtSentence">VPN-Profil (Windows 8.1 und höher)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ddf0d3ce1b5bfef16137dc7ad1155eb1" id="tgt74" class="tgtSentence">VPN-Profil (Windows Phone 8.1 und höher)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="486bbc595e54d171a713579e84b86a09" id="tgt75" class="tgtSentence">VPN-Profil (Windows 10 Desktop und Mobile und höher)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="4098b20f60d185b78a5a8ae04fc0db5e" id="tgt76" class="tgtSentence">Sie können nur benutzerdefinierte VPN-Profilrichtlinien erstellen und bereitstellen.</caps:sentence>
                    <caps:sentence sentenceid="e3b2888d8f4d059bda2997d26638a507" id="tgt77" class="tgtSentence"> Empfohlene Einstellungen sind nicht verfügbar.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="e19316ff66f05bdcf357a1e5cf0dfea1" id="tgt78" class="tgtSentence">Weitere Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie im Thema <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="4b61c65ae3a8072a82b438a72d8dd8c0" id="tgt79" class="tgtSentence">Orientieren Sie sich bei der Konfiguration der Einstellungen für das VPN-Profil an der folgenden Tabelle:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt80" class="tgtSentence">Name der Einstellung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt81" class="tgtSentence">Weitere Informationen</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt82" class="tgtSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a8c1ddde57730206b273729426a3de96" id="tgt83" class="tgtSentence">Geben Sie einen eindeutigen Namen für das VPN-Profil ein, damit Sie es leichter in der <token>wit_nextref</token>-Konsole identifizieren können.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt84" class="tgtSentence">Beschreibung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5c98020fd03734b60d76b73a847e53ed" id="tgt85" class="tgtSentence">Geben Sie eine Beschreibung mit einem Überblick über das VPN-Profil und anderen relevanten Informationen ein, die Ihnen bei der Suche danach helfen.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="49b175054bdf5d1a9f2cced8d5abfd56" id="tgt86" class="tgtSentence">VPN-Verbindungsname (wird Benutzern angezeigt)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4c5b802ee1c2c78c1667c687bfc6bc83" id="tgt87" class="tgtSentence">Geben Sie einen Namen für das VPN-Profil ein.</caps:sentence>
                            <caps:sentence sentenceid="91e5111b50ab7bda93514d3a71f4f8a2" id="tgt88" class="tgtSentence"> Dies ist der Name, der Benutzern in der Liste der verfügbaren VPN-Verbindungen auf ihren Geräten angezeigt wird.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="286b9c555b9c759f1c2c6d8f981dd2a0" id="tgt89" class="tgtSentence">Verbindungstyp</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f324d28add48609a046e5851965f005b" id="tgt90" class="tgtSentence">Wählen Sie einen der folgenden Verbindungstypen zur Verwendung im VPN-Profil aus:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="7016a6b55b2fce84f04c767b1d5c251d" id="tgt91" class="tgtSentence">
                                  <ui>Cisco AnyConnect</ui> (nicht verfügbar für Windows 8.1 oder Windows Phone 8.1)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="bca47433892229a424f00706cd00694d" id="tgt92" class="tgtSentence">Pulse Secure</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="2b5febecd6b7c38d5211d4aa9bcb4f12" id="tgt93" class="tgtSentence">F5 Edge Client</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="3f7901f848d6f7e138dfb72a65f7bc48" id="tgt94" class="tgtSentence">Dell SonicWALL Mobile Connect</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="c7ddd6c2147e3937318a4c09a2ed7da5" id="tgt95" class="tgtSentence">CheckPoint Mobile VPN</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="d495db26ab521298104f23849144732b" id="tgt96" class="tgtSentence">VPN-Serverbeschreibung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d7196510415def859fd846a5dd381935" id="tgt97" class="tgtSentence">Geben Sie eine Beschreibung für den VPN-Server an, mit dem Geräte eine Verbindung herstellen.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt98" class="tgtSentence">
                              <ui>Beispiel:</ui> <userInputLocalizable>Contoso-VPN-Server</userInputLocalizable></caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="5ca7e91190198ebb8fe674f05aa0ebca" id="tgt99" class="tgtSentence">Wenn der Verbindungstyp <ui>F5 Edge Client</ui> ist, geben Sie im Feld <ui>Serverliste</ui> eine Liste der Serverbeschreibungen und IP-Adressen an.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="2e2be732f20a601222f9044039114992" id="tgt100" class="tgtSentence">IP-Adresse oder FQDN des Servers</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="25fb3d3092f47cea967214bfea065e90" id="tgt101" class="tgtSentence">Geben Sie die IP-Adresse oder den vollständig qualifizierten Domänennamen des VPN-Servers an, mit dem Geräte eine Verbindung herstellen.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt102" class="tgtSentence">
                              <ui>Beispiel:</ui> <userInput>192.168.1.1</userInput></caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt103" class="tgtSentence">
                              <ui>Beispiel:</ui> <userInput>vpn.contoso.com</userInput></caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="5ca7e91190198ebb8fe674f05aa0ebca" id="tgt104" class="tgtSentence">Wenn der Verbindungstyp <ui>F5 Edge Client</ui> ist, geben Sie im Feld <ui>Serverliste</ui> eine Liste der Serverbeschreibungen und IP-Adressen an.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="57d16c66a4277aed71142a86a61c0576" id="tgt105" class="tgtSentence">Serverliste</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt106" class="tgtSentence">Klicken Sie auf <ui>Hinzufügen</ui>, um einen neuen VPN-Server zur Verwendung für die VPN-Verbindung hinzuzufügen.</caps:sentence>
                            <caps:sentence sentenceid="1ebc919e808682af9c6b9809834693e5" id="tgt107" class="tgtSentence"> Sie können auch angeben, welcher Server als Standardserver für die Verbindung dienen soll.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="3f446ebfc333ee6fe8e5c3e98911dd19" id="tgt108" class="tgtSentence">Diese Option wird nur für den Verbindungstyp <ui>F5 Edge Client</ui> angezeigt.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b5f1abe365e4508753eaa81debb996a7" id="tgt109" class="tgtSentence">Gesamten Netzwerkdatenverkehr über die VPN-Verbindung senden</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1ec671169076fb27daa00a98e256e875" id="tgt110" class="tgtSentence">Wenn Sie diese Option aktivieren, wird der gesamte Netzwerkdatenverkehr über die VPN-Verbindung gesendet.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="2de76adf0e2f888feab676322f51fd06" id="tgt111" class="tgtSentence">Wenn Sie diese Option nicht auswählen, verhandelt der Client dynamisch die Routen für getrenntes Tunneln beim Herstellen einer Verbindung mit dem VPN-Server eines Drittanbieters.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="838ff1a6ad411d1be4fc66c1fcc97ea8" id="tgt112" class="tgtSentence">Nur Verbindungen mit dem Unternehmensnetzwerk werden über einen VPN-Tunnel gesendet.</caps:sentence>
                            <caps:sentence sentenceid="712cb97cfa2a3bc15ed218c0bf76369e" id="tgt113" class="tgtSentence"> Beim Verbinden mit Ressourcen im Internet wird VPN-Tunneln nicht verwendet.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="1758359f686cbaa78c47cebf4f12c63d" id="tgt114" class="tgtSentence">Authentifizierungsmethode</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7bdeee5b4c9e7778861c67b88a0718e3" id="tgt115" class="tgtSentence">Wählen Sie die von der VPN-Verbindung verwendete Authentifizierungsmethode aus:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="3cc41d0f46073ba8d93ea9db2412437f" id="tgt116" class="tgtSentence">Zertifikate</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="c161342ed0cc808adf28882c27a83f4f" id="tgt117" class="tgtSentence">Benutzername und Kennwort</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="7899f7a1314f71ceca1d4569e91e8c53" id="tgt118" class="tgtSentence">Die Einstellung <ui>Benutzername und Kennwort</ui> ist für den Verbindungstyp <ui>Cisco AnyConnect</ui> nicht verfügbar.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt119" class="tgtSentence">Die Option <ui>Authentifizierungsmethode</ui> ist für Windows 8.1 nicht verfügbar.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="007184fe17ebe1c9dd806625afa7622e" id="tgt120" class="tgtSentence">Benutzeranmeldeinformationen bei jeder Anmeldung speichern</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="519e6a95a0b4a4de331432fff41e8cf5" id="tgt121" class="tgtSentence">Aktivieren Sie diese Option, um sicherzustellen, dass die Benutzeranmeldeinformationen gespeichert werden, sodass der Benutzer die Anmeldeinformationen nicht bei jeder Verbindungsherstellung erneut eingeben muss.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="a9dd13a5f012698b4fdc82469bf5b440" id="tgt122" class="tgtSentence">Wählen Sie ein Clientzertifikat für die Clientauthentifizierung (Identitätszertifikat) aus</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1a9a11bc5210fcf6285eeb3cd7b7d7a4" id="tgt123" class="tgtSentence">Wählen Sie das SCEP-Clientzertifikat aus, das Sie zuvor erstellt haben und das zur Authentifizierung der VPN-Verbindung verwendet wird.</caps:sentence>
                            <caps:sentence sentenceid="6240249c9f4f5fd3aa7c12866434a436" id="tgt124" class="tgtSentence"> Weitere Informationen zur Verwendung von Zertifikatprofilen in <token>wit_nextref</token> finden Sie unter <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0">Use Microsoft Intune Certificate Profiles to secure access to company resources</link>.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="4dab21bdbe9e3546e1b3bc52007fbb30" id="tgt125" class="tgtSentence">Diese Option wird nur für die Authentifizierungsmethode <ui>Zertifikate</ui> angezeigt.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="29a7e96467b69a9f5a93332e29e9b0de" id="tgt126" class="tgtSentence">Rolle</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c65bdb49dec5cd0393103ef1a8813cb7" id="tgt127" class="tgtSentence">Geben Sie den Namen der Benutzerrolle an, die Zugriff auf diese Verbindung hat.</caps:sentence>
                            <caps:sentence sentenceid="3bab762eba51790a0664b5755c5ec96d" id="tgt128" class="tgtSentence"> Eine Benutzerrolle definiert persönliche Einstellungen und Optionen und aktiviert oder deaktiviert bestimmte Zugriffsfeatures.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="3f446ebfc333ee6fe8e5c3e98911dd19" id="tgt129" class="tgtSentence">Diese Option wird nur für den Verbindungstyp <ui>Pulse Secure</ui> angezeigt.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b94b7ef7f17d2394d6fbdf458dadc7b0" id="tgt130" class="tgtSentence">Bereich</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2e1291f05712460ca0686c6014e2e102" id="tgt131" class="tgtSentence">Geben Sie den Namen des gewünschten Authentifizierungsbereichs an.</caps:sentence>
                            <caps:sentence sentenceid="0f73973051ac72a1209904066ebd8964" id="tgt132" class="tgtSentence"> Ein Authentifizierungsbereich ist eine Gruppe von Authentifizierungsressourcen, die vom Verbindungstyp „Pulse Secure“ verwendet werden.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="3f446ebfc333ee6fe8e5c3e98911dd19" id="tgt133" class="tgtSentence">Diese Option wird nur für den Verbindungstyp <ui>Pulse Secure</ui> angezeigt.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="96db828e7f56733514f6e16fcfc4f330" id="tgt134" class="tgtSentence">Anmeldegruppe oder Domäne</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="56ee84218ddba320625f071556c2cb84" id="tgt135" class="tgtSentence">Geben Sie den Namen der Anmeldegruppe oder Domäne an, mit der Sie eine Verbindung herstellen möchten.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="3f446ebfc333ee6fe8e5c3e98911dd19" id="tgt136" class="tgtSentence">Diese Option wird nur für den Verbindungstyp <ui>Dell SonicWALL Mobile Connect</ui> angezeigt.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="52609e00b7ee307e79eb100099b9a8bf" id="tgt137" class="tgtSentence">Fingerabdruck</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="73e1fc750ae8a3e28723aea114bf28f6" id="tgt138" class="tgtSentence">Geben Sie eine Zeichenfolge wie z. B. „Contoso-Fingerabdruckcode“ an, anhand der überprüft wird, ob der VPN-Server vertrauenswürdig ist.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="bbe1d14a39705507e7ca8318ede0d005" id="tgt139" class="tgtSentence">Mit einem Fingerabdruck kann wie folgt verfahren werden:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="5309e016a59ca32afbb56690c05406e4" id="tgt140" class="tgtSentence">Er kann an den Client gesendet werden, damit dieser weiß, dass alle Server vertrauenswürdig sind, die beim Verbinden den betreffenden Fingerabdruck vorweisen.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="14d28d59062ae717ee1a47c733996cd3" id="tgt141" class="tgtSentence">Wenn das Gerät nicht über den Fingerabdruck verfügt, wird der Benutzer aufgefordert, dem VPN-Server zu vertrauen, mit dem Verbindung hergestellt wird, während der Fingerabdruck angezeigt wird (der Benutzer überprüft den Fingerabdruck manuell und klickt auf <ui>vertrauen</ui>, um die Verbindung herzustellen).</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="3f446ebfc333ee6fe8e5c3e98911dd19" id="tgt142" class="tgtSentence">Diese Option wird nur für den Verbindungstyp <ui>CheckPoint Mobile VPN</ui> angezeigt.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4b23edc82031079aca7850c7f8c8b694" id="tgt143" class="tgtSentence">
                              <ui>VPN für App</ui> (nur iOS)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2260c9a66bc029b71967eccb3f971d89" id="tgt144" class="tgtSentence">Mit dieser Option können Sie diese VPN-Verbindung einer iOS- oder Mac OS X-App zuzuordnen, sodass die Verbindung geöffnet wird, wenn die Anwendung ausgeführt wird.</caps:sentence>
                            <caps:sentence sentenceid="bdb5ab82c9aa698019741faaa895fbcd" id="tgt145" class="tgtSentence"> Die Zuordnung des VPN-Profils zu einer App kann bei der Bereitstellung der Software erfolgen.</caps:sentence>
                            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt146" class="tgtSentence"> Weitere Informationen finden Sie unter <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy software to mobile devices in Windows Intune</link>.</caps:sentence>
                          </para>
                          <alert class="important">
                            <para>
                              <caps:sentence sentenceid="fcc5a68d6b4bfbd33d036055a1d7c0e4" id="tgt147" class="tgtSentence">Wenn Sie eine App bereitstellen, die einem bereitgestellten VPN-Profil zugeordnet ist, und dann die VPN-Profilbereitstellung löschen, können Benutzer die App nicht mehr ausführen.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c831bd025ecbb12a4dd627a7b14872d9" id="tgt148" class="tgtSentence">
                              <ui>Proxyeinstellungen automatisch erkennen</ui> (nur iOS, Mac OS X, Windows 8.1 und Windows Phone 8.1)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6587610643d21d5bcd72578e376c0319" id="tgt149" class="tgtSentence">Geben der VPN-Server einen Proxyserver für die Verbindung erfordert, geben Sie an, ob Geräte die Verbindungseinstellungen automatisch erkennen sollen.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="bf674d78fde6749af9f6c9cb0bc8f7de" id="tgt150" class="tgtSentence">Weitere Informationen finden Sie in der Windows Server-Dokumentation.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c831bd025ecbb12a4dd627a7b14872d9" id="tgt151" class="tgtSentence">
                              <ui>Automatisches Konfigurationsskript verwenden</ui> (nur iOS, Mac OS X, Windows 8.1 und Windows Phone 8.1)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9d905dcdfe4609fa25e98cd892a7083d" id="tgt152" class="tgtSentence">Wenn der VPN-Server einen Proxyserver für die Verbindung erfordert, geben Sie an, ob Sie die Einstellungen mit einem automatischen Konfigurationsskript definieren und dann eine URL zur Datei mit den Einstellungen angeben möchten.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="bf674d78fde6749af9f6c9cb0bc8f7de" id="tgt153" class="tgtSentence">Weitere Informationen finden Sie in der Windows Server-Dokumentation.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c831bd025ecbb12a4dd627a7b14872d9" id="tgt154" class="tgtSentence">
                              <ui>Proxyserver verwenden</ui> (nur iOS, Mac OS X, Windows 8.1 und Windows Phone 8.1)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4ebcfd5e4e3ca16a154d3a454975f0c6" id="tgt155" class="tgtSentence">Wenn der VPN-Server einen Proxyserver für die Verbindung erfordert, aktivieren Sie diese Option, und geben Sie dann die Adresse und die Portnummer des Proxyservers an.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="bf674d78fde6749af9f6c9cb0bc8f7de" id="tgt156" class="tgtSentence">Weitere Informationen finden Sie in der Windows Server-Dokumentation.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="273d239a5063e60aedaae3f03ef72e32" id="tgt157" class="tgtSentence">
                              <ui>Proxyeinstellungen für lokale Adressen umgehen</ui> (nur iOS, Mac OS X, Windows 8.1 und Windows Phone 8.1)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="ba950a3ede458b6805b56455330f5e0a" id="tgt158" class="tgtSentence">Wenn der VPN-Server einen Proxyserver für die Verbindung erfordert, aktivieren Sie diese Option, wenn der Proxyserver für von Ihnen angegebene lokale Adressen nicht verwendet werden soll.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="bf674d78fde6749af9f6c9cb0bc8f7de" id="tgt159" class="tgtSentence">Weitere Informationen finden Sie in der Windows Server-Dokumentation.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="30e1b6d7c656b2a1c7131f4d322bab38" id="tgt160" class="tgtSentence">
                              <ui>Benutzerdefiniertes XML</ui> (nur Windows 8.1 und höher sowie Windows Phone 8.1 und höher)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a8b52bf8944dcd0a1fb42ca42362abb3" id="tgt161" class="tgtSentence">Ermöglicht Ihnen die Angabe benutzerdefinierter XML-Befehle zum Konfigurieren der VPN-Verbindung.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="be945161c473ad325e31768c649d7bc4" id="tgt162" class="tgtSentence">Beispiele:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="62fd3f87581663e4371e40eb51d66e76" id="tgt163" class="tgtSentence">Für <ui>Pulse Secure</ui>:</caps:sentence>
                              </para>
                              <para>
                                <userInput>&lt;pulse-schema&gt;&lt;isSingleSignOnCredential&gt;true&lt;/isSingleSignOnCredential&gt;&lt;/pulse-schema&gt;</userInput>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="62fd3f87581663e4371e40eb51d66e76" id="tgt164" class="tgtSentence">Für <ui>CheckPoint Mobile VPN</ui>:</caps:sentence>
                              </para>
                              <para>
                                <userInput>&lt;CheckPointVPN port="443" name="CheckPointSelfhost" sso="true"  debug="3" /&gt;</userInput>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="62fd3f87581663e4371e40eb51d66e76" id="tgt165" class="tgtSentence">Für <ui>Dell SonicWALL Mobile Connect</ui>:</caps:sentence>
                              </para>
                              <para>
                                <userInput>&lt;MobileConnect&gt;&lt;Compression&gt;false&lt;/Compression&gt;&lt;debugLogging&gt;True&lt;/debugLogging&gt;&lt;packetCapture&gt;False&lt;/packetCapture&gt;&lt;/MobileConnect&gt;</userInput>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="62fd3f87581663e4371e40eb51d66e76" id="tgt166" class="tgtSentence">Für <ui>F5 Edge Client</ui>:</caps:sentence>
                              </para>
                              <para>
                                <userInput>&lt;f5-vpn-conf&gt;&lt;single-sign-on-credential /&gt;&lt;/f5-vpn-conf&gt;</userInput>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence sentenceid="8fbea0408a5a8ea8fb7fe6d5e02e7213" id="tgt167" class="tgtSentence">Weitere Informationen über das Schreiben von benutzerdefinierten XML-Befehlen finden Sie in der VPN-Dokumentation der einzelnen Hersteller.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c3df5fdcf805c1f7337aaa4976c15751" id="tgt168" class="tgtSentence">
                              <ui>DNS-Suffix-Suchliste</ui> (nur Windows Phone 8.1)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a14af1ebc78b2002b0a98ec5a420a549" id="tgt169" class="tgtSentence">Geben Sie in jeder Zeile ein DNS-Suffix an.</caps:sentence>
                            <caps:sentence sentenceid="1fba4b5233247212f6d8452414c1a3af" id="tgt170" class="tgtSentence"> Jedes angegebene DNS-Suffix wird beim Verbinden mit einer Website unter Verwendung eines Kurznamens gesucht.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="515a5f656a4b6ad82e66bccca22dde9d" id="tgt171" class="tgtSentence">Beispiel: Sie geben die DNS-Suffixe <ui>domain1.contoso.com</ui> und <ui>domain2.contoso.com</ui> an und besuchen dann die URL <ui>http://mywebsite</ui>.</caps:sentence>
                            <caps:sentence sentenceid="bd3f256edea494d7902ac122eba4a8e2" id="tgt172" class="tgtSentence"> Die folgenden Adressen werden gesucht.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="232add6e072c0ab0e7933ab8b3c11b0a" id="tgt173" class="tgtSentence">http://mywebsite.domain1.contoso.com</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="32254f91d844d42c07f338cdd1dd48cc" id="tgt174" class="tgtSentence">http://mywebsite.domain2.contoso.com</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c3df5fdcf805c1f7337aaa4976c15751" id="tgt175" class="tgtSentence">
                              <ui>Bei Verbindung mit dem Unternehmens-WLAN VPN umgehen</ui> (nur Windows Phone 8.1)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5b87b3997ae843844a3691fa6546e5a4" id="tgt176" class="tgtSentence">Gibt an, dass die VPN-Verbindung nicht verwendet wird, wenn das Gerät mit dem Unternehmens-WLAN verbunden ist.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c3df5fdcf805c1f7337aaa4976c15751" id="tgt177" class="tgtSentence">
                              <ui>VPN umgehen, wenn mit Heimat-WLAN-Netzwerk verbunden</ui> (nur Windows Phone 8.1)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="659c604d3b832f972e674ab318f3feb1" id="tgt178" class="tgtSentence">Gibt an, dass die VPN-Verbindung nicht verwendet wird, wenn das Gerät mit einem WLAN-Heimnetzwerk verbunden ist.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD colspan="2">
                          <para>
                            <legacyBold>
                              <caps:sentence sentenceid="6e1332a262bc1b470f9edce324a04003" id="tgt179" class="tgtSentence">Einstellungen für Unternehmensgrenzen für Windows 10 Desktop und Mobile</caps:sentence>
                            </legacyBold>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d6c975a88c21e369c22eb5f25e89ab47" id="tgt180" class="tgtSentence">
                        Regeln für den Netzwerkdatenverkehr</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9fc5e0c08c98dfe9c39759a1351501d1" id="tgt181" class="tgtSentence">Legen Sie die Protokolle, die lokalen und Remoteports sowie die Adressbereiche fest, die für die VPN-Verbindung aktiviert werden sollen.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="9db0d0377f02a4396cc5f423b81f243b" id="tgt182" class="tgtSentence">Wenn Sie keine Regel für den Netzwerkdatenverkehr erstellen, werden alle Protokolle, Ports und Adressbereiche aktiviert.</caps:sentence>
                              <caps:sentence sentenceid="9bae097359c33dbe418b163b8d1ab6f2" id="tgt183" class="tgtSentence"> Nachdem Sie eine Regel erstellt haben, werden nur die in dieser oder weiteren Regeln festgelegten Protokolle, Ports und Adressbereiche von der VPN-Verbindung verwendet.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1755347e5f6a762b84a3f6512a3e4e53" id="tgt184" class="tgtSentence">Routen</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="ecbdc34e0ac7b88e2995ad56d1646df8" id="tgt185" class="tgtSentence">Die Routen, welche die VPN-Verbindung verwenden.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3570ac237401dec741acde33499f9f7d" id="tgt186" class="tgtSentence">DNS-Server</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e77f2ca2ca596b8acc7d408e5a9c02f9" id="tgt187" class="tgtSentence">Die DNS-Server, die von der VPN-Verbindung verwendet werden, nachdem die Verbindung hergestellt wurde.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="dc890882c099782a7639b258ae524a8e" id="tgt188" class="tgtSentence">Im Folgenden finden Sie ein Beispiel für die Verwendung von Einstellungen für Unternehmensgrenzen.</caps:sentence>
                      <caps:sentence sentenceid="ea5af402188c6ffd18630d725f1f6110" id="tgt189" class="tgtSentence"> Wenn Sie das VPN nur für Remotedesktops aktivieren möchten, erstellen Sie eine Regel für den Netzwerkdatenverkehr, die Datenverkehr für Protokollnummer 27 am externen Port 3996 zulässt.</caps:sentence>
                      <caps:sentence sentenceid="a2ba7d95df9aa459856bec1941cdfef0" id="tgt190" class="tgtSentence"> Kein anderer Datenverkehr verwendet das VPN.</caps:sentence>
                    </para>
                    <para>
                      <caps:sentence sentenceid="b1871a22552e6b997fb5095a91986e6e" id="tgt191" class="tgtSentence">Das Definieren von Routen innerhalb von Unternehmensgrenzen ist nützlich, wenn Sie für Ihren VPN-Verbindungstyp nicht definieren können, wie Datenverkehr bei getrenntem Tunneln behandelt wird.</caps:sentence>
                      <caps:sentence sentenceid="71a733034498d85e9d24bc3ab2aa3791" id="tgt192" class="tgtSentence"> Verwenden Sie in diesem Fall <ui>Routen</ui>, um die Routen aufzulisten, die das VPN verwenden.</caps:sentence>
                    </para>
                    <para>
                      <caps:sentence sentenceid="4609a0e87c0a9236e443037d5d48cdfc" id="tgt193" class="tgtSentence">Sie können die VPN-Nutzung auf Windows 10-Geräten auf bestimmte Apps beschränken, indem Sie eine benutzerdefinierte OMA-URI-Einstellung definieren.</caps:sentence>
                      <caps:sentence sentenceid="9eb7a9f5d635070a5130106a58ae4785" id="tgt194" class="tgtSentence"> Weitere Informationen zu benutzerdefinierten URI-Einstellungen finden Sie unter <link xlink:href="b05bbc3f-6256-490d-901f-3746203ca160">Custom URI settings for Windows 10 devices</link>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt195" class="tgtSentence">Klicken Sie danach auf <ui>Richtlinie speichern</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt196" class="tgtSentence">Die neue Richtlinie wird im Knoten <ui>Konfigurationsrichtlinien</ui> des Arbeitsbereichs <ui>Richtlinie</ui> angezeigt.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="e09cbf58edf7526d79b00ab829898610" id="tgt197" class="tgtSentence">Bereitstellen eines VPN-Profils</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="7300d957006194ad572b3539bb5e7a7e" id="tgt198" class="tgtSentence">Stellen Sie das VPN-Profil für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="ad5c1bcb5291ef46b20f2e8f623f5ca4" id="tgt199" class="tgtSentence">Weitere Informationen über das Bereitstellen von Richtlinien finden Sie unter <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="01d86b2114262db694dc64c0bb564e2d" id="tgt200" class="tgtSentence">Eine Statuszusammenfassung und Warnungen auf der Seite <ui>Übersicht</ui> des Arbeitsbereichs <ui>Richtlinie</ui> identifiziert Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern.</caps:sentence>
                  <caps:sentence sentenceid="f38e8d4a29f6e64f69b2faa73bb44771" id="tgt201" class="tgtSentence"> Darüber hinaus wird eine Statusübersicht im Arbeitsbereich <ui>Dashboard</ui> angezeigt.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <nextSteps>
        <content>
          <para>
            <caps:sentence sentenceid="e2a6b3d395dcffaab874a0eb04e7cdcc" id="tgt202" class="tgtSentence">Nach der erfolgreichen Bereitstellung sehen Benutzer den von Ihnen angegebenen VPN-Verbindungsnamen in der Liste der VPN-Verbindungen auf ihrem Gerät.</caps:sentence>
          </para>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="5b090c5a-6f12-4e60-ace0-c9929afaa9a3">Enable access to company resources using Windows Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Virtual Private Networks (VPN) let you give your users secure remote access to your company network.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Remote users can work as if their device is physically connected to the network.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Devices use a VPN connection profile to initiate a connection with the VPN server.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Use <ui>VPN profiles</ui> in <token>wit_firstref</token> to deploy VPN settings to users and devices in your organization.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> By deploying these settings, you minimize the end-user effort required to connect to resources on the company network.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">For example, you want to provision all iOS devices with the settings required to connect to a file share on the corporate network.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> You create a VPN profile containing the settings necessary to connect to the corporate network and then deploy this profile to all users with iOS devices.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> The users will see the VPN connection in the list of available networks and can connect with the minimum of effort.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">You can configure the following device types with VPN profiles:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Devices that run Android 4 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Devices that run iOS 7.1 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Devices that run Max OS X 10.9 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">Enrolled devices that run Windows 8.1 and later (includes Windows RT 8.1)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">Devices that run Windows Phone 8.1 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">Devices that run Windows 10 desktop and mobile.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src16" class="srcSentence">The VPN profile configuration options will differ depending on the device type you select.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src17" class="srcSentence">VPN connection types</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src18" class="srcSentence">
              <token>wit_nextref</token> supports creating VPN profiles that use the following connection types:</caps:sentence>
          </para>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src19" class="srcSentence">Connection type</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src20" class="srcSentence">iOS and Mac OS X</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src21" class="srcSentence">Android</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src22" class="srcSentence">Windows Phone 8.1</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src23" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src24" class="srcSentence">Windows 10 Desktop and Mobile</caps:sentence>
                    </ui>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Cisco AnyConnect</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">Pulse Secure</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">F5 Edge Client</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Dell SonicWALL Mobile Connect</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">CheckPoint Mobile VPN</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="important">
            <para>
              <caps:sentence id="src55" class="srcSentence">Before you can use VPN profiles deployed to a device, you must install the applicable VPN app for the profile.</caps:sentence>
              <caps:sentence id="src56" class="srcSentence"> You can use the information in the <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy apps to mobile devices in Microsoft Intune</link> topic to help you deploy the applicable app using <token>wit_nextref</token>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src57" class="srcSentence">How VPN profiles are secured</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src58" class="srcSentence">VPN profiles can use a number of different connection types and protocols from different manufacturers.</caps:sentence>
            <caps:sentence id="src59" class="srcSentence"> These connections are typically secured using one of two methods:</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src60" class="srcSentence">Certificates</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src61" class="srcSentence">When you create the VPN profile, you choose a SCEP or .PFXcertificate profile that you have previously created in <token>wit_nextref</token>.</caps:sentence>
                <caps:sentence id="src62" class="srcSentence"> This is known as the identity certificate and is used to authenticate against a trusted certificate profile (or a root certificate) you created to establish that the user’s device is allowed to connect.</caps:sentence>
                <caps:sentence id="src63" class="srcSentence"> The trusted certificate is deployed to the computer that authenticates the VPN connection, typically, the VPN server.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src64" class="srcSentence">For more information about how to create and use certificate profiles in <token>wit_nextref</token>, see <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0">Use Microsoft Intune Certificate Profiles to secure access to company resources</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src65" class="srcSentence">Username and password</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src66" class="srcSentence">The user authenticates to the VPN server by providing their username and password.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src67" class="srcSentence">Create a VPN profile</caps:sentence>
        </title>
        <content>
          <para></para>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">Select a template for the new policy by expanding the relevant device type, then choose the VPN profile for that device:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src70" class="srcSentence">VPN Profile (Android 4 and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src71" class="srcSentence">VPN Profile (iOS 7.1 and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src72" class="srcSentence">VPN Profile (Mac OS X 10.9 and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src73" class="srcSentence">VPN Profile (Windows 8.1 and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src74" class="srcSentence">VPN Profile (Windows Phone 8.1 and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src75" class="srcSentence">VPN Profile (Windows 10 Desktop and Mobile and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">You can only create and deploy a custom VPN profile policy.</caps:sentence>
                    <caps:sentence id="src77" class="srcSentence"> Recommended settings are not available.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">For more information about how to create and deploy policies, see the <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link> topic.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">Use the following table to help you configure the VPN profile settings:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src80" class="srcSentence">Setting name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src81" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src82" class="srcSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src83" class="srcSentence">Enter a unique name for the VPN profile to help you identify it in the <token>wit_nextref</token> console.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src84" class="srcSentence">Description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src85" class="srcSentence">Provide a description that gives an overview of the VPN profile and other relevant information that helps you to locate it.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src86" class="srcSentence">VPN connection name (displayed to users)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src87" class="srcSentence">Specify a name for the VPN profile.</caps:sentence>
                            <caps:sentence id="src88" class="srcSentence"> This is the name that users will see in the list of available VPN connections on their devices.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src89" class="srcSentence">Connection type</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src90" class="srcSentence">Select one of the following connection types to use in the VPN profile:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src91" class="srcSentence">
                                  <ui>Cisco AnyConnect</ui> (not available for Windows 8.1 or Windows Phone 8.1)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src92" class="srcSentence">Pulse Secure</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src93" class="srcSentence">F5 Edge Client</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src94" class="srcSentence">Dell SonicWALL Mobile Connect</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src95" class="srcSentence">CheckPoint Mobile VPN</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src96" class="srcSentence">VPN server description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src97" class="srcSentence">Specify a description for the VPN server that devices will connect to.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src98" class="srcSentence">
                              <ui>Example:</ui> <userInputLocalizable>Contoso VPN Server</userInputLocalizable></caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src99" class="srcSentence">When the connection type is <ui>F5 Edge Client</ui>, use the <ui>Server list</ui> field to specify a list of server descriptions and IP addresses.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src100" class="srcSentence">Server IP address or FQDN</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src101" class="srcSentence">Provide the IP address or fully qualified domain name of the VPN server that devices will connect to.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src102" class="srcSentence">
                              <ui>Example:</ui> <userInput>192.168.1.1</userInput></caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src103" class="srcSentence">
                              <ui>Example:</ui> <userInput>vpn.contoso.com</userInput></caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src104" class="srcSentence">When the connection type is <ui>F5 Edge Client</ui>, use the <ui>Server list</ui> field to specify a list of server descriptions and IP addresses.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src105" class="srcSentence">Server list</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src106" class="srcSentence">Click <ui>Add</ui> to add a new VPN server to use for the VPN connection.</caps:sentence>
                            <caps:sentence id="src107" class="srcSentence"> You can also specify which server is to be the default server for the connection.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src108" class="srcSentence">This option is displayed only when the connection type is <ui>F5 Edge Client</ui>.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src109" class="srcSentence">Send all network traffic through the VPN connection</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src110" class="srcSentence">If you select this option, all network traffic is sent through the VPN connection.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src111" class="srcSentence">If you do not select this option, the client will dynamically negotiate the routes for split tunneling upon connecting to the 3rd party VPN server.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src112" class="srcSentence">Only connections to the company network are sent over a VPN tunnel.</caps:sentence>
                            <caps:sentence id="src113" class="srcSentence"> VPN tunneling is not used when you connect to resources on the Internet.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src114" class="srcSentence">Authentication method</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src115" class="srcSentence">Select the authentication method used by the VPN connection:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src116" class="srcSentence">Certificates</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src117" class="srcSentence">Username and Password</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src118" class="srcSentence">
                                <ui>Username and Password</ui> setting is not available when the connection type is <ui>Cisco AnyConnect</ui>.</caps:sentence>
                            </para>
                            <para>
                              <caps:sentence id="src119" class="srcSentence">The <ui>Authentication method</ui> option is not available for Windows 8.1</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src120" class="srcSentence">Remember the user credentials at each logon</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src121" class="srcSentence">Select this option to ensure that the user credentials are remembered so that the user does not have to enter credentials each time a connection is established.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src122" class="srcSentence">Select a client certificate for client authentication (Identity Certificate)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src123" class="srcSentence">Select the client SCEP certificate that you previously created that will be used to authenticate the VPN connection.</caps:sentence>
                            <caps:sentence id="src124" class="srcSentence"> For more information about how to use certificate profiles in <token>wit_nextref</token>, see <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0">Use Microsoft Intune Certificate Profiles to secure access to company resources</link>.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src125" class="srcSentence">This option is displayed only when the authentication method is <ui>Certificates</ui>.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src126" class="srcSentence">Role</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src127" class="srcSentence">Specify the name of the user role that has access to this connection.</caps:sentence>
                            <caps:sentence id="src128" class="srcSentence"> A user role defines personal settings, options, and enables or disables certain access features.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src129" class="srcSentence">This option is displayed only when the connection type is <ui>Pulse Secure</ui>.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src130" class="srcSentence">Realm</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src131" class="srcSentence">Specify the name of the authentication realm that you want to use.</caps:sentence>
                            <caps:sentence id="src132" class="srcSentence"> An authentication realm is a grouping of authentication resources that is used by the Pulse Secure connection type.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src133" class="srcSentence">This option is displayed only when the connection type is <ui>Pulse Secure</ui>.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src134" class="srcSentence">Login group or domain</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src135" class="srcSentence">Specify the name of the login group or domain that you want to connect to.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src136" class="srcSentence">This option is displayed only when the connection type is <ui>Dell SonicWALL Mobile Connect</ui>.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src137" class="srcSentence">Fingerprint</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src138" class="srcSentence">Specify a string, for example "Contoso Fingerprint Code" that will be used to verify the VPN server can be trusted.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src139" class="srcSentence">A fingerprint can be:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src140" class="srcSentence">Sent to the client so it knows to trust any server presenting that same fingerprint when connecting.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src141" class="srcSentence">If the device doesn’t already have the fingerprint it will prompt the user to trust the VPN server they are connecting to while showing the fingerprint (the user manually verifies the fingerprint and clicks <ui>trust</ui> to connect).</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src142" class="srcSentence">This option is displayed only when the connection type is <ui>CheckPoint Mobile VPN</ui>.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src143" class="srcSentence">
                              <ui>Per App VPN</ui> (iOS only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src144" class="srcSentence">Select this option if you want to associate this VPN connection with an iOS of Mac OS X app so that the connection will be opened when the app is run.</caps:sentence>
                            <caps:sentence id="src145" class="srcSentence"> You can associate the VPN profile with an app when you deploy the software.</caps:sentence>
                            <caps:sentence id="src146" class="srcSentence"> For more information, see <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy software to mobile devices in Windows Intune</link>.</caps:sentence>
                          </para>
                          <alert class="important">
                            <para>
                              <caps:sentence id="src147" class="srcSentence">If you deploy an app that is associated with a deployed VPN profile and then delete the VPN profile deployment, users will no longer be able to run the app.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src148" class="srcSentence">
                              <ui>Automatically detect proxy settings</ui> (iOS, Mac OS X, Windows 8.1 and Windows Phone 8.1 only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src149" class="srcSentence">If your VPN server requires a proxy server for the connection, specify whether you would like devices to automatically detect the connection settings.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src150" class="srcSentence">For more information, see your Windows Server documentation.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src151" class="srcSentence">
                              <ui>Use automatic configuration script</ui> (iOS, Mac OS X, Windows 8.1 and Windows Phone 8.1 only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src152" class="srcSentence">If your VPN server requires a proxy server for the connection, specify whether you would like to use an automatic configuration script to define the settings and then specify a URL to the file containing the settings.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src153" class="srcSentence">For more information, see your Windows Server documentation.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src154" class="srcSentence">
                              <ui>Use proxy server</ui> (iOS, Mac OS X, Windows 8.1 and Windows Phone 8.1 only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src155" class="srcSentence">If your VPN server requires a proxy server for the connection, select this option, then specify the address and port number of the proxy server.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src156" class="srcSentence">For more information, see your Windows Server documentation.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src157" class="srcSentence">
                              <ui>Bypass proxy settings for local addresses</ui> (iOS, Mac OS X, Windows 8.1 and Windows Phone 8.1 only only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src158" class="srcSentence">If your VPN server requires a proxy server for the connection, select this option if you do not want to use the proxy server for local addresses that you specify.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src159" class="srcSentence">For more information, see your Windows Server documentation.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src160" class="srcSentence">
                              <ui>Custom XML</ui> (Windows 8.1 and later, and Windows Phone 8.1 and later only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src161" class="srcSentence">Allows you to specify custom XML commands that configure the VPN connection.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src162" class="srcSentence">Examples:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src163" class="srcSentence">For <ui>Pulse Secure</ui>:</caps:sentence>
                              </para>
                              <para>
                                <userInput>&lt;pulse-schema&gt;&lt;isSingleSignOnCredential&gt;true&lt;/isSingleSignOnCredential&gt;&lt;/pulse-schema&gt;</userInput>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src164" class="srcSentence">For <ui>CheckPoint Mobile VPN</ui>:</caps:sentence>
                              </para>
                              <para>
                                <userInput>&lt;CheckPointVPN port="443" name="CheckPointSelfhost" sso="true"  debug="3" /&gt;</userInput>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src165" class="srcSentence">For <ui>Dell SonicWALL Mobile Connect</ui>:</caps:sentence>
                              </para>
                              <para>
                                <userInput>&lt;MobileConnect&gt;&lt;Compression&gt;false&lt;/Compression&gt;&lt;debugLogging&gt;True&lt;/debugLogging&gt;&lt;packetCapture&gt;False&lt;/packetCapture&gt;&lt;/MobileConnect&gt;</userInput>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src166" class="srcSentence">For <ui>F5 Edge Client</ui>:</caps:sentence>
                              </para>
                              <para>
                                <userInput>&lt;f5-vpn-conf&gt;&lt;single-sign-on-credential /&gt;&lt;/f5-vpn-conf&gt;</userInput>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence id="src167" class="srcSentence">Refer to each manufacturers VPN documentation for more information about how to write custom XML commands.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src168" class="srcSentence">
                              <ui>DNS Suffix search list</ui> (Windows Phone 8.1 only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src169" class="srcSentence">Specify one DNS suffix on each line.</caps:sentence>
                            <caps:sentence id="src170" class="srcSentence"> Each DNS suffix you specify will be searched when connecting to a website using a short name.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src171" class="srcSentence">For example, you specify the DNS suffices <ui>domain1.contoso.com</ui> and <ui>domain2.contoso.com</ui> and then visit the URL <ui>http://mywebsite</ui>.</caps:sentence>
                            <caps:sentence id="src172" class="srcSentence"> The following addresses will be searched:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src173" class="srcSentence">http://mywebsite.domain1.contoso.com</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src174" class="srcSentence">http://mywebsite.domain2.contoso.com</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src175" class="srcSentence">
                              <ui>Bypass VPN when connected to company Wi-Fi network</ui> (Windows Phone 8.1 only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src176" class="srcSentence">Specifies that the VPN connection will not be used when the device is connected to the company Wi-Fi network.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src177" class="srcSentence">
                              <ui>Bypass VPN when connected to home Wi-Fi network</ui> (Windows Phone 8.1 only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src178" class="srcSentence">Specifies that the VPN connection will not be used when the device is connected to a home Wi-Fi network.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD colspan="2">
                          <para>
                            <legacyBold>
                              <caps:sentence id="src179" class="srcSentence">Corporate Boundaries settings for Windows 10 Desktop and Mobile</caps:sentence>
                            </legacyBold>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src180" class="srcSentence">
                        Network traffic rules</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src181" class="srcSentence">Set which protocols, local and remote port and address ranges will be enabled for the VPN connection.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src182" class="srcSentence">If you do not create a network traffic rule, all protocols, ports and address ranges are enabled.</caps:sentence>
                              <caps:sentence id="src183" class="srcSentence"> Once you create a rule, only the protocols, ports and address ranges that you specify in that rule or in additional rules will be used by the VPN connection.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src184" class="srcSentence">Routes</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src185" class="srcSentence">Which routes will use the VPN connection.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src186" class="srcSentence">DNS servers</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src187" class="srcSentence">Which DNS servers are used by the VPN connection once the connection has been established.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src188" class="srcSentence">Here's an example of when you might use corporate boundaries settings.</caps:sentence>
                      <caps:sentence id="src189" class="srcSentence"> If you want to enable VPN only for remote desktop, you would create a network traffic rule that allows traffic for protocol number 27 on external port 3996.</caps:sentence>
                      <caps:sentence id="src190" class="srcSentence"> No other traffic will use the VPN.</caps:sentence>
                    </para>
                    <para>
                      <caps:sentence id="src191" class="srcSentence">Defining routes in corporate boundaries is useful when your VPN connection type does not allow you to define how traffic is handled in split tunneling.</caps:sentence>
                      <caps:sentence id="src192" class="srcSentence"> In that case, use <ui>Routes</ui> to list the routes that will use the VPN.</caps:sentence>
                    </para>
                    <para>
                      <caps:sentence id="src193" class="srcSentence">You can restrict Windows 10 device VPN usage to specific apps by creating a custom OMA-URI setting.</caps:sentence>
                      <caps:sentence id="src194" class="srcSentence"> To learn more about customer URI settings see <link xlink:href="b05bbc3f-6256-490d-901f-3746203ca160">Custom URI settings for Windows 10 devices</link>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src196" class="srcSentence">The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src197" class="srcSentence">Deploy a VPN profile</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">Deploy the VPN profile to one or more groups of users or devices in your organization.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src199" class="srcSentence">For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src200" class="srcSentence">A status summary and alerts on the <ui>Overview</ui> page of the <ui>Policy</ui> workspace identify issues with the policy that require your attention.</caps:sentence>
                  <caps:sentence id="src201" class="srcSentence"> Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <nextSteps>
        <content>
          <para>
            <caps:sentence id="src202" class="srcSentence">After successful deployment, users will see the VPN connection name you specified in the list of VPN connections on their device.</caps:sentence>
          </para>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="5b090c5a-6f12-4e60-ace0-c9929afaa9a3">Enable access to company resources using Windows Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>