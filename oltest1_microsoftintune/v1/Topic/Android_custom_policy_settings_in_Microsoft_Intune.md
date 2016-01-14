---
description: na
keywords: na
title: Android custom policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 15904440-5a05-47c9-818e-48073b4090e7
---
# Benutzerdefinierte Android-Richtlinieneinstellungen in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt1" class="tgtSentence">Stellen Sie mithilfe der <token>wit_firstref</token> <ui>benutzerdefinierten Android-Konfigurationsrichtlinie</ui> Einstellungen für OMA-URI (Open Mobile Alliance Uniform Resource Identifier) bereit, um Funktionen auf Android-Geräten zu steuern.</caps:sentence>
          <caps:sentence sentenceid="8d40fac4ac37509f820ec2d303c38d24" id="tgt2" class="tgtSentence"> Dies sind die Standardeinstellungen, die viele Hersteller von mobilen Geräten verwenden, um Gerätefunktionen zu steuern.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a6664ebfd2b0c892d1eb8ce0c9d3d045" id="tgt3" class="tgtSentence">Diese Funktion soll es Ihnen ermöglichen, Android-Einstellungen bereitzustellen, die nicht mit <token>wit_nextref</token>-Richtlinien konfigurierbar sind.</caps:sentence>
          <caps:sentence sentenceid="4c4623cc4a431eaa78a301d7856090ea" id="tgt4" class="tgtSentence"> Informationen zu den Einstellungen, die Sie mit diesen Richtlinien konfigurieren können, finden Sie im Abschnitt <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure security policy for mobile devices in Microsoft Intune</link>.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="2580290ca57957a94c6aee8185d7453a" id="tgt5" class="tgtSentence">Derzeit unterstützen benutzerdefinierte Android-Richtlinien unterstützt nur das Konfigurieren von WLAN-Einstellungen für Android-Geräte, die einen vorinstallierten Schlüssel enthalten.</caps:sentence>
            <caps:sentence sentenceid="78876cede6e051df998fab51465986f4" id="tgt6" class="tgtSentence"> Informationen hierzu finden Sie unter <link xlink:href="15904440-5a05-47c9-818e-48073b4090e7#BKMK_Example">Example: Configure a custom Wi-Fi profile with a pre-shared key</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="c1456742ddf67eedff174d238e79382d" id="tgt7" class="tgtSentence">Erstellen einer benutzerdefinierte Android-Richtlinie</caps:sentence>
        </title>
        <content>
          <para></para>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt8" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink> auf <ui>Richtlinie</ui> &gt; <ui>Übersicht</ui> &gt; <ui>Richtlinie hinzufügen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="371909b1c7699fc23050a0a2afea4577" id="tgt9" class="tgtSentence">Konfigurieren Sie eine Richtlinie vom Typ <ui>Android</ui> &gt; <ui>Benutzerdefinierte Konfiguration</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="bb959fafb75abf3f883c3e8a465d8f67" id="tgt10" class="tgtSentence">Informationen zum Erstellen und Bereitstellen von Richtlinien finden Sie unter <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f04b005611928fdd585b401e8cbeea51" id="tgt11" class="tgtSentence">Sie können nur benutzerdefinierte Richtlinien dieses Typs erstellen und bereitstellen.</caps:sentence>
                    <caps:sentence sentenceid="e3b2888d8f4d059bda2997d26638a507" id="tgt12" class="tgtSentence"> Empfohlene Einstellungen sind nicht verfügbar.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="606f1d2158988f6e69e06586b9f24c1d" id="tgt13" class="tgtSentence">Orientieren Sie sich bei der Konfiguration der allgemeinen Richtlinieneinstellungen an der folgenden Tabelle:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt14" class="tgtSentence">Name der Einstellung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt15" class="tgtSentence">Weitere Informationen</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt16" class="tgtSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b7b3cfd9342696ddabcf267be61a98d1" id="tgt17" class="tgtSentence">Geben Sie einen eindeutigen Namen für die benutzerdefinierte Android-Richtlinie ein, damit Sie sie leichter in der <token>wit_nextref</token>-Konsole identifizieren können.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt18" class="tgtSentence">Beschreibung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a4d80837b28f4b2a5075d7562396586a" id="tgt19" class="tgtSentence">Geben Sie eine Beschreibung ein, die einen Überblick über die Richtlinie bietet, und andere relevante Informationen, die Ihnen die Suche danach erleichtern.</caps:sentence>
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
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt20" class="tgtSentence">Klicken Sie im Abschnitt <ui>OMA-URI-Einstellungen</ui> auf <ui>Hinzufügen</ui>, um eine Einstellung hinzuzufügen.</caps:sentence>
                    <caps:sentence sentenceid="d02e9eef2acac6cb33d9b16639243048" id="tgt21" class="tgtSentence"> Sie können auch eine vorhandene Einstellung bearbeiten oder löschen.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt22" class="tgtSentence">Geben Sie im Dialogfeld <ui>OMA-URI hinzufügen oder bearbeiten</ui> die folgenden Informationen an:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="447b7147e84be512208dcc0995d67ebc" id="tgt23" class="tgtSentence">Element</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt24" class="tgtSentence">Weitere Informationen</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt25" class="tgtSentence">Name der Einstellung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b25be43287736dc29249283789580234" id="tgt26" class="tgtSentence">Geben Sie einen eindeutigen Namen für die OMA-URI-Einstellung ein, damit Sie sie in der Liste der Einstellungen leichter identifizieren können.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="6754b3fdad38016213d4b9d46256de42" id="tgt27" class="tgtSentence">Beschreibung der Einstellung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="62493ef9a08271cdd406c1864a42de5f" id="tgt28" class="tgtSentence">Geben Sie eine Beschreibung ein, die einen Überblick über die Einstellung bietet, und andere relevante Informationen, die Ihnen die Suche danach erleichtern.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="1443a7220ce58bf7476b59728760e6f7" id="tgt29" class="tgtSentence">Datentyp</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="68c572e87552f9ec55886c4212f96685" id="tgt30" class="tgtSentence">Wählen Sie den Datumstyp aus, in dem Sie diese OMA-URI-Einstellung angeben.</caps:sentence>
                            <caps:sentence sentenceid="a286929ca0f740e14eb1d567ac54d6cb" id="tgt31" class="tgtSentence"> Wählen Sie aus:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt32" class="tgtSentence">Zeichenfolge</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="573bb660411b4996a98b98028247498b" id="tgt33" class="tgtSentence">Zeichenfolge (XML)</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="88412b82a0b294501c4de9d554a6494e" id="tgt34" class="tgtSentence">Datum und Uhrzeit</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="157db7df530023575515d366c9b672e8" id="tgt35" class="tgtSentence">Ganze Zahl</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="1403c9489f9bb53f4e3a25339d22eebb" id="tgt36" class="tgtSentence">Gleitkomma</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="84e2c64f38f78ba3ea5c905ab5a2da27" id="tgt37" class="tgtSentence">Boolesch</caps:sentence>
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
                              <caps:sentence sentenceid="45ba21357c2a6fc435ad3d9b494a7071" id="tgt38" class="tgtSentence">OMA-URI (Groß-/Kleinschreibung beachten)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9415acd2602a372a442381707563fcc8" id="tgt39" class="tgtSentence">Geben Sie den OMA-URI an, für den Sie eine Einstellung festlegen möchten.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt40" class="tgtSentence">Wert</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7217f3564ec322de578b94b7c66f7cb7" id="tgt41" class="tgtSentence">Geben Sie den mit der zuvor festgelegten OMA-URI-Einstellung zu verknüpfenden Wert an.</caps:sentence>
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
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt42" class="tgtSentence">Klicken Sie auf <ui>OK</ui>, um die Einstellung zu speichern und zur Seite <ui>Richtlinie erstellen</ui> zurückzukehren.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="27112a11f9261caf4068fbcbe965797f" id="tgt43" class="tgtSentence">Fügen Sie weitere benötige Einstellungen hinzu.</caps:sentence>
                    <caps:sentence sentenceid="118fb1a3f502368b3803f2a34a6170ec" id="tgt44" class="tgtSentence"> Klicken Sie abschließend auf <ui>Richtlinie speichern</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt45" class="tgtSentence">Die neue Richtlinie wird im Knoten <ui>Konfigurationsrichtlinien</ui> des Arbeitsbereichs <ui>Richtlinie</ui> angezeigt.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="afb09fd2f3b41d8def6e04dc04e106e8" id="tgt46" class="tgtSentence">Bereitstellen einer benutzerdefinierten Android-Richtlinie</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="2d0f41cb652b213e5146783ffaf1a568" id="tgt47" class="tgtSentence">Stellen Sie die benutzerdefinierte Android-Richtlinie für eine oder mehrere Gruppen von Benutzern oder Geräten in Ihrer Organisation bereit.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="7694f5d96c63b5ed65c6cfe05a537801" id="tgt48" class="tgtSentence">Hilfestellung bei der Bereitstellung von Richtlinien finden Sie unter <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="01d86b2114262db694dc64c0bb564e2d" id="tgt49" class="tgtSentence">Eine Statuszusammenfassung und Warnungen auf der Seite <ui>Übersicht</ui> des Arbeitsbereichs <ui>Richtlinie</ui> identifiziert Probleme mit der Richtlinie, die Ihre Aufmerksamkeit erfordern.</caps:sentence>
            <caps:sentence sentenceid="f38e8d4a29f6e64f69b2faa73bb44771" id="tgt50" class="tgtSentence"> Darüber hinaus wird eine Statusübersicht im Arbeitsbereich <ui>Dashboard</ui> angezeigt.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_Example">
        <title>
          <caps:sentence sentenceid="872dc2f2ddf174a207cfb3381ff933a4" id="tgt51" class="tgtSentence">Beispiel: Konfigurieren eines benutzerdefinierten WLAN-Profils mit einem vorinstallierten Schlüssel</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0f8aac06958771570af4f77da5cba7d2" id="tgt52" class="tgtSentence">Obwohl <token>wit_nextref</token> WLAN-Profile für Android-Geräte unterstützt, ist derzeit das Einbeziehen eines vorinstallierten Schlüssels in die Konfiguration nicht möglich.</caps:sentence>
            <caps:sentence sentenceid="34b270d319970c7ff14c75f6af020825" id="tgt53" class="tgtSentence"> In diesem Beispiel erfahren Sie, wie Sie eine benutzerdefinierte Android-Richtlinie erstellen, die ein WLAN-Profil mit einem vorinstallierten Schlüssel auf dem Android-Gerät erstellt.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="fdaf8b6d5559e2ab7174f20d1b39d233" id="tgt54" class="tgtSentence">So erstellen Sie ein WLAN-Profil mit einem vorinstallierten Schlüssel</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="6b0661f97471ac3cdd88fe2980dc036f" id="tgt55" class="tgtSentence">Stellen Sie sicher, dass die Benutzer die neueste Version der <externalLink><linkText>Intune-Unternehmensportal-App</linkText><linkUri>https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal</linkUri></externalLink> für Android verwenden.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="7284835dead44bba1542971414e33d9b" id="tgt56" class="tgtSentence">Erstellen Sie eine benutzerdefinierte Android-Richtlinie, und fügen Sie die folgende OMA-URI-Einstellung hinzu:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt57" class="tgtSentence">Name der Einstellung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt58" class="tgtSentence">Weitere Informationen</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt59" class="tgtSentence">Name der Einstellung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f14dc8de0724d44d6f3f6b88de28d508" id="tgt60" class="tgtSentence">Geben Sie einen Namen Ihrer Wahl für die Einstellung ein.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="6754b3fdad38016213d4b9d46256de42" id="tgt61" class="tgtSentence">Beschreibung der Einstellung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2e179abd8b721a6d1efe48e9c14acbf6" id="tgt62" class="tgtSentence">Geben Sie eine Beschreibung für die Einstellung ein.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="1443a7220ce58bf7476b59728760e6f7" id="tgt63" class="tgtSentence">Datentyp</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt64" class="tgtSentence">Wählen Sie <ui>Zeichenfolge (XML)</ui>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="bf0a958d204cf14f6ea5ba5ad2d8f605" id="tgt65" class="tgtSentence">OMA-URI</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="92ef5ea648ebc2a3724bbe80633019fb" id="tgt66" class="tgtSentence">Geben Sie folgenden Code ein:</caps:sentence>
                          </para>
                          <code>./Vendor/MSFT/WiFi/Profile/<placeholder xmlns="">&lt;Wi-Fi profile&gt;</placeholder>/Settings
</code>
                          <para>
                            <caps:sentence sentenceid="6b9cf579910e539767e730fe9e4e9211" id="tgt67" class="tgtSentence">Wobei <placeholder>&lt; WLAN-Profil &gt;</placeholder> ein eindeutiger Name für das Profil ist.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt68" class="tgtSentence">
                              <ui>Beispiel:</ui> </caps:sentence>
                          </para>
                          <code>./Vendor/MSFT/WiFi/Profile/ContosoWiFi/Settings
</code>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt69" class="tgtSentence">Wert</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="66e8e780aed7c3ec5511cc359213dc29" id="tgt70" class="tgtSentence">Kopieren und fügen Sie den folgenden XML-Code ein:</caps:sentence>
                          </para>
                          <code>&lt;!-- WEP Wifi Profile <placeholder xmlns="">&lt;Name of wifi profile&gt;</placeholder> = Name of profile <placeholder xmlns="">&lt;SSID of wifi profile&gt;</placeholder> = Plain text of SSID. Does not need to be escaped, could be &lt;name&gt;Your Company's Network&lt;/name&gt; <placeholder xmlns="">&lt;WEP password&gt;</placeholder> = Password to connect to the network --&gt; &lt;WLANProfile xmlns="http://www.microsoft.com/networking/WLAN/profile/v1"&gt; &lt;name&gt;<placeholder xmlns="">&lt;Name of wifi profile&gt;</placeholder>&lt;/name&gt; &lt;SSIDConfig&gt; &lt;SSID&gt; &lt;name&gt;<placeholder xmlns="">&lt;SSID of wifi profile&gt;</placeholder>&lt;/name&gt; &lt;/SSID&gt; &lt;/SSIDConfig&gt; &lt;connectionType&gt;ESS&lt;/connectionType&gt; &lt;MSM&gt; &lt;security&gt; &lt;authEncryption&gt; &lt;authentication&gt;open&lt;/authentication&gt; &lt;encryption&gt;WEP&lt;/encryption&gt; &lt;useOneX&gt;false&lt;/useOneX&gt; &lt;/authEncryption&gt; &lt;sharedKey&gt; &lt;keyType&gt;networkKey&lt;/keyType&gt; &lt;protected&gt;false&lt;/protected&gt; &lt;keyMaterial&gt;<placeholder xmlns="">&lt;WEP password&gt;</placeholder>&lt;/keyMaterial&gt; &lt;/sharedKey&gt; &lt;keyIndex&gt;0&lt;/keyIndex&gt; &lt;/security&gt; &lt;/MSM&gt; &lt;/WLANProfile&gt;</code>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a6a19bb38ff73c131c5ce7938b8f996a" id="tgt71" class="tgtSentence">Wenn Sie fertig sind, speichern Sie die Richtlinie und stellen sie den erforderlichen Android-Geräten bereit.</caps:sentence>
                    <caps:sentence sentenceid="683ed056aa0cba469438ac6dcccd0abe" id="tgt72" class="tgtSentence"> Das neue WLAN-Profil wird in der Liste der Verbindungen auf dem Gerät angezeigt.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the <token>wit_firstref</token> <ui>Android custom configuration policy</ui> to deploy OMA-URI (Open Mobile Alliance Uniform Resource Identifier) settings that can be used to control features on Android devices.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> These are standard settings that many mobile device manufacturers use to control device features.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">This capability is intended to allow you to deploy Android settings that are not configurable with <token>wit_nextref</token> policies.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For information about the settings you can configure with these policies, see <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure security policy for mobile devices in Microsoft Intune</link>.</caps:sentence>
        </para>
        <alert class="note">
          <para>
            <caps:sentence id="src5" class="srcSentence">Currently, Android custom policies only support configuring Wi-Fi settings for Android devices that include a pre-shared key.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> See <link xlink:href="15904440-5a05-47c9-818e-48073b4090e7#BKMK_Example">Example: Configure a custom Wi-Fi profile with a pre-shared key</link> to learn how to do this.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">How to create an Android custom policy</caps:sentence>
        </title>
        <content>
          <para></para>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Overview</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Configure a policy of the type <ui>Android</ui> &gt; <ui>Custom Configuration</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">For help creating and deploying policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">You can only create and deploy a custom policy of this type.</caps:sentence>
                    <caps:sentence id="src12" class="srcSentence"> Recommended settings are not available.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Use the following table to help you configure the general policy settings:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src14" class="srcSentence">Setting name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src15" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src16" class="srcSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src17" class="srcSentence">Enter a unique name for the Android custom policy to help you identify it in the <token>wit_nextref</token> console.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src18" class="srcSentence">Description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src19" class="srcSentence">Provide a description that gives an overview of the Android custom policy and other relevant information that helps you to locate it.</caps:sentence>
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
                    <caps:sentence id="src20" class="srcSentence">In the <ui>OMA-URI Settings</ui> section, click <ui>Add</ui> to add a setting.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> You can also edit or delete an existing setting.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">In the <ui>Add or Edit OMA-URI Setting</ui> dialog box, specify the following information:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src23" class="srcSentence">Item</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src24" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src25" class="srcSentence">Setting name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src26" class="srcSentence">Enter a unique name for the OMA-URI setting to help you identify it in the list of settings.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src27" class="srcSentence">Setting description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src28" class="srcSentence">Provide a description that gives an overview of the setting and other relevant information to help you locate it.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src29" class="srcSentence">Data type</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src30" class="srcSentence">Select the date type in which you will specify this OMA-URI setting.</caps:sentence>
                            <caps:sentence id="src31" class="srcSentence"> Choose from:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src32" class="srcSentence">String</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src33" class="srcSentence">String (XML)</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src34" class="srcSentence">Date and time</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src35" class="srcSentence">Integer</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src36" class="srcSentence">Floating point</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src37" class="srcSentence">Boolean</caps:sentence>
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
                              <caps:sentence id="src38" class="srcSentence">OMA-URI (case sensitive)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src39" class="srcSentence">Specify the OMA-URI you want to supply a setting for.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src40" class="srcSentence">Value</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src41" class="srcSentence">Specify the value to associate with the OMA-URI you specified previously.</caps:sentence>
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
                    <caps:sentence id="src42" class="srcSentence">Click <ui>OK</ui> to save the setting and return to the <ui>Create Policy</ui> page.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Continue to add as many settings as you require.</caps:sentence>
                    <caps:sentence id="src44" class="srcSentence"> When you are done, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src46" class="srcSentence">Deploy an Android custom policy</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src47" class="srcSentence">Deploy the Android custom policy to one or more groups of users or devices in your organization.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src48" class="srcSentence">For help deploying policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src49" class="srcSentence">A status summary and alerts on the <ui>Overview</ui> page of the <ui>Policy</ui> workspace identify issues with the policy that require your attention.</caps:sentence>
            <caps:sentence id="src50" class="srcSentence"> Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_Example">
        <title>
          <caps:sentence id="src51" class="srcSentence">Example: Configure a custom Wi-Fi profile with a pre-shared key</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src52" class="srcSentence">Although <token>wit_nextref</token> supports Wi-Fi profiles for Android devices, this feature does not currently support the inclusion of a pre-shared key in the configuration.</caps:sentence>
            <caps:sentence id="src53" class="srcSentence"> In this example, you’ll learn how to create an Android custom policy that creates a Wi-Fi profile with a pre-shared key on the Android device.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src54" class="srcSentence">To create a Wi-Fi profile with a pre-shared key</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Ensure that your users are using the latest version of the <externalLink><linkText>Intune Company Portal</linkText><linkUri>https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal</linkUri></externalLink> app for Android.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">Create an Android custom policy and add the following OMA-URI setting:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src57" class="srcSentence">Setting name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src58" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src59" class="srcSentence">Setting name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src60" class="srcSentence">Specify a name of your choice for the setting.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src61" class="srcSentence">Setting description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src62" class="srcSentence">Specify a description for the setting.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src63" class="srcSentence">Data type</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src64" class="srcSentence">Select <ui>String (XML)</ui>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src65" class="srcSentence">OMA-URI</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src66" class="srcSentence">Enter:</caps:sentence>
                          </para>
                          <code>./Vendor/MSFT/WiFi/Profile/<placeholder xmlns="">&lt;Wi-Fi profile&gt;</placeholder>/Settings
</code>
                          <para>
                            <caps:sentence id="src67" class="srcSentence">Where <placeholder>&lt;Wi-Fi profile&gt;</placeholder> is a unique name for the profile.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src68" class="srcSentence">
                              <ui>Example:</ui> </caps:sentence>
                          </para>
                          <code>./Vendor/MSFT/WiFi/Profile/ContosoWiFi/Settings
</code>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src69" class="srcSentence">Value</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src70" class="srcSentence">Copy and paste the following XML code:</caps:sentence>
                          </para>
                          <code>&lt;!-- WEP Wifi Profile <placeholder xmlns="">&lt;Name of wifi profile&gt;</placeholder> = Name of profile <placeholder xmlns="">&lt;SSID of wifi profile&gt;</placeholder> = Plain text of SSID. Does not need to be escaped, could be &lt;name&gt;Your Company's Network&lt;/name&gt; <placeholder xmlns="">&lt;WEP password&gt;</placeholder> = Password to connect to the network --&gt; &lt;WLANProfile xmlns="http://www.microsoft.com/networking/WLAN/profile/v1"&gt; &lt;name&gt;<placeholder xmlns="">&lt;Name of wifi profile&gt;</placeholder>&lt;/name&gt; &lt;SSIDConfig&gt; &lt;SSID&gt; &lt;name&gt;<placeholder xmlns="">&lt;SSID of wifi profile&gt;</placeholder>&lt;/name&gt; &lt;/SSID&gt; &lt;/SSIDConfig&gt; &lt;connectionType&gt;ESS&lt;/connectionType&gt; &lt;MSM&gt; &lt;security&gt; &lt;authEncryption&gt; &lt;authentication&gt;open&lt;/authentication&gt; &lt;encryption&gt;WEP&lt;/encryption&gt; &lt;useOneX&gt;false&lt;/useOneX&gt; &lt;/authEncryption&gt; &lt;sharedKey&gt; &lt;keyType&gt;networkKey&lt;/keyType&gt; &lt;protected&gt;false&lt;/protected&gt; &lt;keyMaterial&gt;<placeholder xmlns="">&lt;WEP password&gt;</placeholder>&lt;/keyMaterial&gt; &lt;/sharedKey&gt; &lt;keyIndex&gt;0&lt;/keyIndex&gt; &lt;/security&gt; &lt;/MSM&gt; &lt;/WLANProfile&gt;</code>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">When you are done, save the policy and deploy it to the required Android devices.</caps:sentence>
                    <caps:sentence id="src72" class="srcSentence"> The new Wi-Fi profile will appear in the list of connections on the device.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>