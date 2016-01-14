---
description: na
keywords: na
title: Network infrastructure requirements for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: 074de65b-84a5-4a01-a824-18ffd838eab0
---
# Anforderungen an die Netzwerkinfrastruktur f&#252;r Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="36e7484d991415e8c2a969a0514e177d" id="tgt1" class="tgtSentence">Für <token>wit_firstref</token> ist es erforderlich, dass Kommunikation zwischen den Geräten, die Sie verwalten und zum Verwalten des Abonnements verwenden, und den Websites im Internet, die vom cloudbasierten Dienst verwendet werden, von Ihrer Netzwerkinfrastruktur weitergeleitet wird.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="510db0d3ef7f985985127c7a5696f285" id="tgt2" class="tgtSentence">Es ist nicht erforderlich, eine lokale Infrastruktur (z. B. einen Server, bei dem Sie Software installieren müssen) zu verwenden. Es gibt jedoch Optionen zum Verwenden von lokaler Infrastruktur einschließlich Synchronisierungstools für Exchange und Active Directory.</caps:sentence>
        </para>
      </introduction>
      <section address="BKMK_NetworkReqs">
        <title>
          <caps:sentence sentenceid="0fa769f19527a7b0b265507a8a6fcf10" id="tgt3" class="tgtSentence">Netzwerkinfrastruktur</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="743accde94089318461e5cbf7d28222a" id="tgt4" class="tgtSentence">Zum Verwalten von Computern, die sich hinter Firewalls und Proxyservern befinden, müssen Sie die Firewalls und Proxyserver so einrichten, dass Kommunikation bei <token>wit_nextref</token> zugelassen wird.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_FirewallReqs">
            <title>
              <caps:sentence sentenceid="2808fefce413f598cb5a424408ea5cf3" id="tgt5" class="tgtSentence">Anforderungen an Firewalls, Ports und Domänen</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="c3e218c09e94478e7e1f6ae8c2651b22" id="tgt6" class="tgtSentence">Für verwaltete Geräte sind Konfigurationen erforderlich, mit denen <ui>Alle Benutzer</ui> durch Firewalls auf verschiedene Dienste zugreifen können.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e8ab6e158a71832dee6fab6ee38cd00a" id="tgt7" class="tgtSentence">In der folgenden Tabelle sind die Domänen und Dienste aufgeführt, auf die vom <token>wit_nextref</token>-Client zugegriffen wird:</caps:sentence>
              </para>
              <table>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence sentenceid="4d066bbb0e40abe54f3000755a45aa6e" id="tgt8" class="tgtSentence">Zweck</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence sentenceid="ad5f82e879a9c5d6b5b442eb37e50551" id="tgt9" class="tgtSentence">Domain</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence sentenceid="47f06098d3034f593871b524ce4f7965" id="tgt10" class="tgtSentence">Ports</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD rowspan="13">
                      <para>
                        <caps:sentence sentenceid="e18b8b3c20f7f02d18a31dc620754203" id="tgt11" class="tgtSentence">Microsoft Intune und verwandte Dienste</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9392cf092359f776e70fc5bbb647d4c1" id="tgt12" class="tgtSentence">*.manage.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt13" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="49c1a5569b93dd3a3ee8b6a0d55bdb07" id="tgt14" class="tgtSentence">*manage.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt15" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="279ab96b5e9c52f956f4f8274a089fcb" id="tgt16" class="tgtSentence">manage.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt17" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7bdb803df62260b54bd5f96b2dcd7eb9" id="tgt18" class="tgtSentence">*.microsoftonline-p.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt19" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2a124d68f425f7660dbcbe579f46d4c4" id="tgt20" class="tgtSentence">*.microsoftonline-p.net</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt21" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5f88455367d181a50d58c073dba9dee2" id="tgt22" class="tgtSentence">*.portal.office.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt23" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b0c61c248f2f1b75b2fe1ed87f3ab67c" id="tgt24" class="tgtSentence">*.spynet2.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="13f3cf8c531952d72e5847c4183e6910" id="tgt25" class="tgtSentence">443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="72836b7903474360317c180671414487" id="tgt26" class="tgtSentence">c.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt27" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fd7e72c734e21220fe613ea1005910d" id="tgt28" class="tgtSentence">c1.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt29" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e3db2053e5eb9febe03b3e5c47b86a6b" id="tgt30" class="tgtSentence">blob.core.windows.net</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt31" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="71d5bd6fe0ae16c9a269531841d2a259" id="tgt32" class="tgtSentence">ajax.aspnetcdn.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt33" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3dbdf785b7394f58c2cb64bcb1ce1ad2" id="tgt34" class="tgtSentence">*.googleapis.com<superscript>1</superscript></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt35" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a62f8b45ef41e2907d4734429602dace" id="tgt36" class="tgtSentence">wustat.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt37" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD rowspan="8">
                      <para>
                        <caps:sentence sentenceid="8c5a3e7661ea4eb94ea78c6329bd3a9b" id="tgt38" class="tgtSentence">Microsoft Update Services</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b4c63e1a02782fa1da394c40444707c8" id="tgt39" class="tgtSentence">*.update.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt40" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1a34d8272348282803adbb71053d241b" id="tgt41" class="tgtSentence">download.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt42" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3dfef91e52b19e8bc2b5c88bdf9d7a52" id="tgt43" class="tgtSentence">update.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt44" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc12b071660bc429d61a1105fb0f83e" id="tgt45" class="tgtSentence">*.download.windowsupdate.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt46" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="683ca3c4043fb12d3bb49c2470a087ea" id="tgt47" class="tgtSentence">download.windowsupdate.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt48" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="32fa9b961c28b39d125ad95c30a8adb4" id="tgt49" class="tgtSentence">*.windowsupdate.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt50" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="61138c8874db6a74253f3e6472c73c24" id="tgt51" class="tgtSentence">windowsupdate.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt52" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="40ef01d37461ab4affb0fdc88462aba9" id="tgt53" class="tgtSentence">ntservicepack.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt54" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9ba19f33544f52d093b1dc829916f3ab" id="tgt55" class="tgtSentence">DNS-Lookupanforderungen</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f4258153ae1d9a3760975e4bdbc1cbd1" id="tgt56" class="tgtSentence">manage.microsoft.com.nsatc.net</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f033ab37c30201f73f142449d037028d" id="tgt57" class="tgtSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6abaa6ea93510e01304a220ad4e481bf" id="tgt58" class="tgtSentence">Samsung KNOX-Gerätekommunikation über die Firewall </caps:sentence>
                      </para>
                    </TD>
                    <TD colspan="2">
                      <para>
                        <caps:sentence sentenceid="d52988662dbebd9d84c452c89688849d" id="tgt59" class="tgtSentence">Damit Samsung KNOX-Geräte über die Firewall mit KNOX-Servern kommunizieren können, folgen Sie den Anweisungen in den <externalLink><linkText>häufig gestellten Fragen zu Samsung KNOX</linkText><linkUri>https://www.samsungknox.com/en/faq/our-corporate-devices-are-behind-firewall-how-do-i-enable-knox-devices-contact-samsung-servers</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD rowspan="7">
                      <para>
                        <caps:sentence sentenceid="f4c1eb7d09c2402ee98ecbc372053ed3" id="tgt60" class="tgtSentence">Dokumentation, Hilfe und Support</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60bb4483051c15c2dfa7dd6f50de9d63" id="tgt61" class="tgtSentence">*.livemeeting.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt62" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="27be46b3683119d6d88f554f4638293d" id="tgt63" class="tgtSentence">*.microsoftonline.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1e843244050957d73fa9aa34411aab32" id="tgt64" class="tgtSentence">80 und 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="89748fba5256b0a9527acd8ce872bd7c" id="tgt65" class="tgtSentence">*.social.technet.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f033ab37c30201f73f142449d037028d" id="tgt66" class="tgtSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0b83c1110314d30de574e9bf72aa87ed" id="tgt67" class="tgtSentence">blogs.technet.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f033ab37c30201f73f142449d037028d" id="tgt68" class="tgtSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e3e9274bea3629d0cf0cdf4df232c4d5" id="tgt69" class="tgtSentence">go.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f033ab37c30201f73f142449d037028d" id="tgt70" class="tgtSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="353d479d7fc12a82557dc46ac5c06e05" id="tgt71" class="tgtSentence">onlinehelp.Microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f033ab37c30201f73f142449d037028d" id="tgt72" class="tgtSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c439589400212f33bcef65939bd8c69f" id="tgt73" class="tgtSentence">www.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f033ab37c30201f73f142449d037028d" id="tgt74" class="tgtSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="69f8ee48020c84f3835de35d1835798e" id="tgt75" class="tgtSentence">
                  <superscript>1</superscript> Diese Domäne ist für JQuery-Unterstützung bei Verwendung der Unternehmensportal-Website erforderlich.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_ProxyReqs">
            <title>
              <caps:sentence sentenceid="7b745b5f2d8b8d7a3404c954ee30bf6d" id="tgt76" class="tgtSentence">Anforderungen an Proxyserver </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a560908426df5dda02b12592950f9395" id="tgt77" class="tgtSentence">Beim Verwalten von Computern, die sich hinter einem Proxyserver befinden, berücksichtigen Sie Folgendes:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2e7659cfca0c6fed4083a1fbc1cc1e5c" id="tgt78" class="tgtSentence">Vom Proxyserver muss sowohl <embeddedLabel>HTTP</embeddedLabel> als auch <embeddedLabel>HTTPS</embeddedLabel> unterstützt werden, da von <token>wit_nextref</token>-Clients beide Protokolle verwendet werden.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a6b973d314b4803abc18f9d41211d836" id="tgt79" class="tgtSentence">
                      <token>wit_nextref</token> unterstützt nicht authentifizierte Proxyserver.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="2d2f76bf845dd02e6e268035bc6327d7" id="tgt80" class="tgtSentence">Sie können Proxyservereinstellungen entweder auf einzelnen Clientcomputern modifizieren oder mithilfe der Gruppenrichtlinieneinstellungen für alle Clientcomputer hinter einem bestimmten Proxyserver ändern.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="bfbb0838b69d85c83cdc0dd3c8755d33" id="tgt81" class="tgtSentence">Sie können außerdem einen Proxyserver verwenden, der die Inhalte im Cache speichert, um <externalLink><linkText>die Bandbreitennutzung</linkText><linkUri>http://technet.microsoft.com/library/dn646966.aspx#BKMK_reduceBandwidth</linkUri></externalLink> durch  <token>wit_nextref</token>-Clients im Netzwerk zu verringern.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_OnPremisesReqs">
        <title>
          <caps:sentence sentenceid="d6167847a99d514149a0df6871047aed" id="tgt82" class="tgtSentence">Lokale Infrastruktur</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2fdff60ca1d9d7b567efd803c71381a4" id="tgt83" class="tgtSentence">In der folgenden Tabelle ist lokale Infrastruktur aufgeführt, die Sie mit <token>wit_firstref</token> verwenden können.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6e3301c94e4de897ec67fa9735a848d5" id="tgt84" class="tgtSentence">Infrastruktur</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt85" class="tgtSentence">Weitere Informationen</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d90358363d8cfded0bdd9a07057008c9" id="tgt86" class="tgtSentence">On-Premises Connector</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt87" class="tgtSentence">Verwenden Sie <embeddedLabel>On-Premises Connector</embeddedLabel>, um Daten aus Exchange Server zu synchronisieren:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="1022f4306450723da9d41975682a1228" id="tgt88" class="tgtSentence">Wenn Ihre Exchange Server-Instanz lokal ist, müssen Sie Microsoft Intune On-Premises Connector herunterladen, auf einem Computer in Ihrer Infrastruktur installieren und <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_EX_OP">set up the Microsoft Intune On-Premises Connector</link>.</caps:sentence>
                        <caps:sentence sentenceid="0229367fdfa702b230b81a5c2206b918" id="tgt89" class="tgtSentence"> Von diesem Connector kann auch eine Verbindung mit Exchange in der Cloud hergestellt werden.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="76c71141dccc39b2804db9870d83a2fa" id="tgt90" class="tgtSentence">Wenn Ihre Exchange Server-Instanz in einem cloudbasierten Dienst gehostet wird, können Sie On-Premises Connector installieren und konfigurieren, oder Sie können <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_S_S">configure the built-in Microsoft Intune Service to Service Connector</link>, für dessen Hosting kein lokaler Server erforderlich ist.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="004d632ab659e788ccf3107519606389" id="tgt91" class="tgtSentence">Bevor Sie einen Connector zum Verbinden von <token>wit_nextref</token> mit Ihrem Exchange-Server verwenden können, müssen Sie die <externalLink><linkText>Active Directory-Synchronisierung</linkText><linkUri>http://technet.microsoft.com/library/dn646983.aspx#BKMK_SyncUsersFromAD</linkUri></externalLink> einrichten, damit Ihre lokalen Benutzer und Sicherheitsgruppen mit Ihrer Instanz von Azure AD synchronisiert werden.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="20942b4dbe3286cd6e037e52f07f5afa" id="tgt92" class="tgtSentence">Proxyserver</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e0b971ee1ed9042702b3e6341bc3e92e" id="tgt93" class="tgtSentence">Wenn Sie Clients verwalten, die über einen Proxyserver auf das Internet zugreifen, finden Sie entsprechende Informationen unter <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0#BKMK_ProxyReqs">Requirements for proxy servers</link>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="2dc574849ec54889c16a219f2b954832" id="tgt94" class="tgtSentence">Sie können außerdem einen Proxyserver verwenden, von dem Inhalt im Cache gespeichert wird, um die Bandbreitennutzung im Netzwerk zu verringern.</caps:sentence>
                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt95" class="tgtSentence"> Weitere Informationen finden Sie unter <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268#BKMK_ReduceBandwidth">Reduce network bandwidth use</link> im Thema <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268">What to know before setting up Microsoft Intune</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
        <sections>
          <section address="BKMK_ExchanceConnectorReqs">
            <title>
              <caps:sentence sentenceid="34ec164bc5813cd6d00a0d18c00d2c85" id="tgt96" class="tgtSentence">Anforderungen für On-Premises Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="64fb5527b08aeb6d49176cce5a93cd92" id="tgt97" class="tgtSentence">In der folgenden Tabelle finden Sie die Anforderungen an den Computer, auf dem Sie On-Premises Connector installieren.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ba12fb48e2d23bb2bd2819f64d02ec7e" id="tgt98" class="tgtSentence">Anforderungen</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt99" class="tgtSentence">Weitere Informationen</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f1624e5afb6a846cd36867a4c4671722" id="tgt100" class="tgtSentence">Betriebssysteme</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="223551596e60cadc89be2a55ed2871b9" id="tgt101" class="tgtSentence">
                          <token>wit_nextref</token> unterstützt On-Premises Connector auf Computern, auf denen eine beliebige Edition der folgenden Betriebssysteme ausgeführt wird: </caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="f20c638b8fad74c9c205afe4c2124168" id="tgt102" class="tgtSentence">
                              <token>longhornshort</token> SP2 (64 Bit)</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <token>nextref_server_7</token>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <token>win8_server_2</token>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <token>winblue_server_2</token>
                          </para>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="d8d392b1c8ed998bcb4612024c6c1dd7" id="tgt103" class="tgtSentence">Auf Server Core-Installationen wird der Connector nicht unterstützt.</caps:sentence>
                        </para>
                      </alert>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1222404a50294459e637db75bdbf38cf" id="tgt104" class="tgtSentence">Microsoft Exchange-Version</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3d34ac4492df210e49e995ae06b89d5b" id="tgt105" class="tgtSentence">Der On-Premises Connector erfordert Microsoft Exchange 2010 SP1 oder höher.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3ca14c518d1bf901acc339e7c9cd6d7f" id="tgt106" class="tgtSentence">Hardware</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9856162e273eb39086b9520d3892f6d7" id="tgt107" class="tgtSentence">Beim Computer, auf dem Sie den Connector installieren, ist mindestens folgende Hardwareausstattung erforderlich: </caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="00644bd440ce2521f43183c50f774129" id="tgt108" class="tgtSentence">CPU mit 1,6 GHz</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ae4fc75576d2b46844420b759efee464" id="tgt109" class="tgtSentence">2 GB RAM</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fb5cd9d02c26eedbf114d5a283476492" id="tgt110" class="tgtSentence">10 GB freier Festplattenspeicher</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f186aeb2673beb336c5521b04059ed87" id="tgt111" class="tgtSentence">Zusätzliche Software</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2d2ab85486fa66a05bcb7e35f586352d" id="tgt112" class="tgtSentence">Folgendes muss auf dem Computer installiert sein, auf dem der Connector gehostet wird:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="88ce4775e41656d7a11e1180b774d76e" id="tgt113" class="tgtSentence">Vollständige Installation von Microsoft .NET Framework 4</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="578bc86193e08c6ece961a841620d5ce" id="tgt114" class="tgtSentence">
                              <token>wps_2</token> 2.0 oder höher</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="80df76ee8e0b399cc2cbbe6bf636eb64" id="tgt115" class="tgtSentence">Der Connector wird auf Computern, auf denen Exchange Server-Rollen ausgeführt werden, nicht unterstützt.</caps:sentence>
                        </para>
                      </alert>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="91e02cd2b8621d0c05197f645668c5c4" id="tgt116" class="tgtSentence">Netzwerk</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6869f930d8b88fe2483e729923b610bb" id="tgt117" class="tgtSentence">Der Computer, auf dem Sie den Connector installieren, muss sich in einer Domäne befinden, die sich mit der Domäne, in der Exchange Server gehostet wird, in einer Vertrauensstellung befindet.</caps:sentence>
                      </para>
                      <para></para>
                      <para>
                        <caps:sentence sentenceid="e6fc5203c4bb33d8b2cb6798948f5988" id="tgt118" class="tgtSentence">Für den Computer sind Konfigurationen erforderlich, damit ein Zugriff auf den <token>wit_nextref</token>-Dienst durch Firewalls und Proxyserver über die Ports 80 und 443 möglich ist.</caps:sentence>
                        <caps:sentence sentenceid="6654329b23ebfc0fbac9edd268cbde37" id="tgt119" class="tgtSentence">
                          <token>wit_nextref</token> verwendet unter anderem folgende Domänen:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="279ab96b5e9c52f956f4f8274a089fcb" id="tgt120" class="tgtSentence">manage.microsoft.com</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="49c1a5569b93dd3a3ee8b6a0d55bdb07" id="tgt121" class="tgtSentence">*manage.microsoft.com</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9392cf092359f776e70fc5bbb647d4c1" id="tgt122" class="tgtSentence">*.manage.microsoft.com</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_ServiceConnectorReqs">
            <title>
              <caps:sentence sentenceid="f9747c77ff164bc42ed5cf00bb6d193a" id="tgt123" class="tgtSentence">Anforderungen an Service to Service Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="8dc0ed75f4e39259a4eb573d91a9dda4" id="tgt124" class="tgtSentence">Von Service to Service Connector wird nur cloudbasiertes Exchange unterstützt. Es bestehen keine Anforderungen an die lokale Infrastruktur.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ea226dfc03ed8b5224272e8c0b55d2e3" id="tgt125" class="tgtSentence">Allerdings muss zum Verwenden dieses Connectors folgende Voraussetzung erfüllt sein:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="27f99d4a8d0cc6a5f1250977998b8288" id="tgt126" class="tgtSentence">Sie verfügen über ein Office 365-Abonnement mit einem Exchange Server 2013-Mandanten.</caps:sentence>
                    <caps:sentence sentenceid="fed2f2f9d9413c0c0d4b9f052797c700" id="tgt127" class="tgtSentence"> Solange der Mandant Exchange Server 2013-fähig ist, wird in der gleichen Umgebung Exchange Server 2010 vom Connector unterstützt.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b151bed7565262a52ccf57446dd8c817" id="tgt128" class="tgtSentence">Bei dem Benutzerkonto, das zum Installieren von On-Premises Connector verwendet wird, muss es sich um einen Mandantenadministrator für <token>wit_nextref</token> und um einen Administrator des Exchange-Mandanten mit einer Lizenz zum Verwenden von Exchange Server 2013 handeln.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268">What to know before setting up Microsoft Intune</link>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="bd854e819a9550dafe0c9b715e019a4d" id="tgt129" class="tgtSentence">Intune-Bezugsquellen</caps:sentence>
          </linkText>
          <linkUri>http://technet.microsoft.com/library/dn646949.aspx</linkUri>
        </externalLink>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <token>wit_firstref</token> requires your network infrastructure to pass communications between the devices you manage and use to manage your subscription, and the websites on the Internet that the cloud-based service uses.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">There is no requirement to use on-premises infrastructure (like a server where you must install software), but there are options to use on-premises infrastructure including Exchange and Active Directory synchronization tools.</caps:sentence>
        </para>
      </introduction>
      <section address="BKMK_NetworkReqs">
        <title>
          <caps:sentence id="src3" class="srcSentence">Network infrastructure</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">To manage computers that are behind firewalls and proxy servers, you must set up firewalls and proxy servers to allow communications for <token>wit_nextref</token>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_FirewallReqs">
            <title>
              <caps:sentence id="src5" class="srcSentence">Requirements for firewalls, ports, and domains</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src6" class="srcSentence">Managed devices require configurations that let <ui>All Users</ui> access various services through firewalls.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src7" class="srcSentence">The following table lists the domains and services that the <token>wit_nextref</token> client accesses.</caps:sentence>
              </para>
              <table>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence id="src8" class="srcSentence">Purpose</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence id="src9" class="srcSentence">Domain</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence id="src10" class="srcSentence">Ports</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD rowspan="13">
                      <para>
                        <caps:sentence id="src11" class="srcSentence">Microsoft Intune and related services</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src12" class="srcSentence">*.manage.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src13" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">*manage.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src15" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">manage.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src17" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">*.microsoftonline-p.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">*.microsoftonline-p.net</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src21" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">*.portal.office.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src23" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src24" class="srcSentence">*.spynet2.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">c.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src27" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src28" class="srcSentence">c1.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src29" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src30" class="srcSentence">blob.core.windows.net</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src31" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">ajax.aspnetcdn.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">*.googleapis.com<superscript>1</superscript></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">wustat.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD rowspan="8">
                      <para>
                        <caps:sentence id="src38" class="srcSentence">Microsoft Update Services</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src39" class="srcSentence">*.update.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">download.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">update.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">*.download.windowsupdate.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">download.windowsupdate.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src48" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">*.windowsupdate.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">windowsupdate.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">ntservicepack.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src55" class="srcSentence">DNS lookup requests</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">manage.microsoft.com.nsatc.net</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Samsung KNOX device communication through the firewall </caps:sentence>
                      </para>
                    </TD>
                    <TD colspan="2">
                      <para>
                        <caps:sentence id="src59" class="srcSentence">To enable Samsung KNOX devices to contact KNOX servers through the firewall, follow the instructions on the <externalLink><linkText>Samsung KNOX FAQ</linkText><linkUri>https://www.samsungknox.com/en/faq/our-corporate-devices-are-behind-firewall-how-do-i-enable-knox-devices-contact-samsung-servers</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD rowspan="7">
                      <para>
                        <caps:sentence id="src60" class="srcSentence">Documentation, Help, and support</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src61" class="srcSentence">*.livemeeting.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">*.microsoftonline.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">80 and 443</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">*.social.technet.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">blogs.technet.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">go.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">onlinehelp.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src72" class="srcSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">www.microsoft.com</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">80</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src75" class="srcSentence">
                  <superscript>1</superscript> This domain is required for JQuery support when you use the company portal website.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_ProxyReqs">
            <title>
              <caps:sentence id="src76" class="srcSentence">Requirements for proxy servers </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src77" class="srcSentence">To manage computers that are behind a proxy server, consider the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">The proxy server must support both <embeddedLabel>HTTP</embeddedLabel> and <embeddedLabel>HTTPS</embeddedLabel> because <token>wit_nextref</token> clients use both protocols.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">
                      <token>wit_nextref</token> supports unauthenticated proxy servers.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src80" class="srcSentence">You can modify proxy server settings on individual client computers, or you can use Group Policy settings to change settings for all client computers that are located behind a specified proxy server.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src81" class="srcSentence">You can also use a proxy server that caches content to <externalLink><linkText>reduce network bandwidth</linkText><linkUri>http://technet.microsoft.com/library/dn646966.aspx#BKMK_reduceBandwidth</linkUri></externalLink> use by <token>wit_nextref</token> clients.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_OnPremisesReqs">
        <title>
          <caps:sentence id="src82" class="srcSentence">On-premises infrastructure</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src83" class="srcSentence">The following table identifies on-premises infrastructure you can use with <token>wit_firstref</token>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">Infrastructure</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">More information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">On-Premises Connector</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">Use the <embeddedLabel>On-Premises Connector</embeddedLabel> to synchronize data from Exchange Server:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">If your instance of Exchange Server is on-premises, you must download, install, and <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_EX_OP">set up the Microsoft Intune On-Premises Connector</link> on a computer in your infrastructure.</caps:sentence>
                        <caps:sentence id="src89" class="srcSentence"> This connector can also connect to Exchange in the cloud.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">If your instance of Exchange Server is hosted in a cloud-based service, you can install and configure the On-Premises Connector, or you can <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_S_S">configure the built-in Microsoft Intune Service to Service Connector</link> which does not require an on-premises server to host the connector.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">Before you can use either connector to connect <token>wit_nextref</token> to your Exchange Server, you must <externalLink><linkText>set up Active Directory synchronization</linkText><linkUri>http://technet.microsoft.com/library/dn646983.aspx#BKMK_SyncUsersFromAD</linkUri></externalLink> so that your local users and security groups are synchronized with your instance of Azure AD.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src92" class="srcSentence">Proxy server</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">If you manage clients that access the Internet through a proxy server, see <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0#BKMK_ProxyReqs">Requirements for proxy servers</link>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">You can also use a proxy server that caches content to reduce network bandwidth.</caps:sentence>
                    <caps:sentence id="src95" class="srcSentence"> For more information, see <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268#BKMK_ReduceBandwidth">Reduce network bandwidth use</link> in the <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268">What to know before setting up Microsoft Intune</link> topic.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
        <sections>
          <section address="BKMK_ExchanceConnectorReqs">
            <title>
              <caps:sentence id="src96" class="srcSentence">Requirements for the On-Premises Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src97" class="srcSentence">The following table lists the requirements for the computer where you install the On-Premises Connector.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">Requirement</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src99" class="srcSentence">More information</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">Operating systems</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">
                          <token>wit_nextref</token> supports the On-Premises Connector on a computer that runs any edition of the following operating systems: </caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src102" class="srcSentence">
                              <token>longhornshort</token> SP2 64 bit</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <token>nextref_server_7</token>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <token>win8_server_2</token>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <token>winblue_server_2</token>
                          </para>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src103" class="srcSentence">The connector is not supported on any Server Core installation.</caps:sentence>
                        </para>
                      </alert>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">Microsoft Exchange version</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">The On-Premises Connector requires Microsoft Exchange 2010 SP1 or later.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">Hardware</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">The computer where you install the connector requires the following minimum hardware: </caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src108" class="srcSentence">1.6 GHz CPU</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src109" class="srcSentence">2 GB ram</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src110" class="srcSentence">10 GB of free disk space</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src111" class="srcSentence">Additional software</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src112" class="srcSentence">The following must be installed on the computer that hosts the connector:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src113" class="srcSentence">Full installation of Microsoft .NET Framework 4</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src114" class="srcSentence">At a minimum, <token>wps_2</token> 2.0</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src115" class="srcSentence">The connector is not supported on a computer that runs an Exchange Server role.</caps:sentence>
                        </para>
                      </alert>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src116" class="srcSentence">Network</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">The computer where you install the connector must be in a domain that has a trust relationship to the domain that hosts your Exchange Server.</caps:sentence>
                      </para>
                      <para></para>
                      <para>
                        <caps:sentence id="src118" class="srcSentence">The computer requires configurations to enable it to access the <token>wit_nextref</token> service through firewalls and proxy servers over Ports 80 and 443.</caps:sentence>
                        <caps:sentence id="src119" class="srcSentence"> Domains used by <token>wit_nextref</token> include:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src120" class="srcSentence">manage.microsoft.com</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src121" class="srcSentence">*manage.microsoft.com</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src122" class="srcSentence">*.manage.microsoft.com</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_ServiceConnectorReqs">
            <title>
              <caps:sentence id="src123" class="srcSentence">Requirements for the Service to Service Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src124" class="srcSentence">The Service to Service Connector supports only cloud-based Exchange and has no requirements for on-premises infrastructure.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src125" class="srcSentence">However, to use this connector, the following must be true:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">You have an Office 365 subscription that has an Exchange Server 2013 tenant.</caps:sentence>
                    <caps:sentence id="src127" class="srcSentence"> So long as the tenant is Exchange Server 2013, the connector supports Exchange Server 2010 in that same environment.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">The user account that you use to install the On-Premises Connector must be a tenant administrator for <token>wit_nextref</token> and be an administrator in the Exchange tenant with a license to use Exchange Server 2013.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268">What to know before setting up Microsoft Intune</link>
        <externalLink>
          <linkText>
            <caps:sentence id="src129" class="srcSentence">How to buy Intune</caps:sentence>
          </linkText>
          <linkUri>http://technet.microsoft.com/library/dn646949.aspx</linkUri>
        </externalLink>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>