---
description: na
keywords: na
title: Deploy apps to mobile devices in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6da30550-9e8e-4333-b9b3-83928de3807a
---
# Bereitstellen von Apps f&#252;r mobile Ger&#228;te in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f13201fed29755ea6bde03a4eda76cb2" id="tgt1" class="tgtSentence">Nachdem Sie sich mit den <externalLink><linkText>ersten Schritten</linkText><linkUri>https://technet.microsoft.com/library/dn646955.aspx</linkUri></externalLink> bei der Bereitstellung von Apps mit <token>wit_firstref</token> vertraut gemacht haben, lernen Sie nun, wie Sie Apps für Geräte konfigurieren und bereitstellen, die bei <token>wit_nextref</token> registriert sind.</caps:sentence>
          <caps:sentence sentenceid="0d7e1b99f40e99888784b29ac58d7696" id="tgt2" class="tgtSentence"> Dies umfasst in der Regel drei Schritte:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="#BKMK_Conf">Configure the app</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="#BKMK_Depl">Deploy the app</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="#BKMK_Monitor">Monitor the app</link>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="b7839bce7e6c7fa6389ae336cfc70db5" id="tgt3" class="tgtSentence">Informationen zum Aktualisieren und Außerkraftsetzen von Apps finden Sie unter <link xlink:href="beee6933-876a-4be0-b395-4c24cfbd519b">Update and retire apps using Microsoft Intune</link>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="223d8227707afeb1da9b03ad1e2ddce4" id="tgt4" class="tgtSentence">Die Informationen in diesem Thema helfen Ihnen, Apps auf <externalLink><linkText>registrierten Windows-PCs</linkText><linkUri>https://technet.microsoft.com/library/mt346003.aspx</linkUri></externalLink> und anderen mobilen Geräten bereitzustellen.</caps:sentence>
            <caps:sentence sentenceid="83bbcc4b30e3c7225a7ad18edf9a01ee" id="tgt5" class="tgtSentence"> Informationen zum Bereitstellen von Apps auf <externalLink><linkText>Windows-PCs, die Sie mithilfe der Clientsoftware verwalten</linkText><linkUri>https://technet.microsoft.com/library/dn646959.aspx</linkUri></externalLink>, finden Sie unter <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb">Deploy apps to Windows PCs in Microsoft Intune</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="BKMK_Conf">
        <title>
          <caps:sentence sentenceid="c0f31e254bf659b63314100f70766e66" id="tgt6" class="tgtSentence">Konfigurieren der App</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="515293c52bc22b89e2b30da73efc5536" id="tgt7" class="tgtSentence">In dieser Vorgehensweise verwenden Sie den Intune-Softwareherausgeber, um die Eigenschaften der App zu konfigurieren und sie, falls zutreffend, in Ihren Cloudspeicher hochzuladen.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="f3b80b5b659c7e3401811b3da369b116" id="tgt8" class="tgtSentence">So konfigurieren Sie eine App</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt9" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Administratorkonsole</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink> auf <ui>Apps</ui> &gt; <ui>Apps hinzufügen</ui>, um den Intune-Softwareherausgeber zu starten.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="a0ba1d9b54ea7d5426a5cd87cb69ff5c" id="tgt10" class="tgtSentence">Möglicherweise müssen Sie Ihren Intune-Benutzernamen und das Kennwort eingeben, bevor der Softwareherausgeber gestartet wird.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt11" class="tgtSentence">Konfigurieren Sie auf der Seite <ui>Softwaresetup</ui> des Softwareherausgebers Folgendes:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="49dfbef0dee6e13d79ecdd1a9e31318c" id="tgt12" class="tgtSentence">
                      <ui>Wählen Sie aus, wie diese Software für Geräte bereitgestellt werden soll</ui> – Wählen Sie eine der folgenden Optionen aus:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f777dcf051d1886e04cdfa9cb2f0a2ce" id="tgt13" class="tgtSentence">
                          <ui>Softwareinstallationsprogramm</ui>, und geben Sie dann Folgendes an:</caps:sentence>
                      </para>
                      <table border="1">
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt14" class="tgtSentence">Einstellung</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt15" class="tgtSentence">Details</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="ca64f3dcc207c6e7b42eac6c8af3d5c0" id="tgt16" class="tgtSentence">Wählen Sie den Dateityp des Softwareinstallationsprogramms aus</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="81fb4f6963cee019f57c26e75574a651" id="tgt17" class="tgtSentence">Hiermit wird die Art der Software angegeben, die Sie bereitstellen möchten.</caps:sentence>
                                <caps:sentence sentenceid="b3e0e1757566bcf89c88afb9265dd055" id="tgt18" class="tgtSentence"> Wenn Sie z. B. eine iOS-App bereitstellen möchten, wählen Sie <ui>App-Paket für iOS (IPA-Datei)</ui> aus.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="fc961e16156fb2c205083cbdd949121e" id="tgt19" class="tgtSentence">Geben Sie den Speicherort der Softwaresetupdateien an</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="6a4c45ba9ab5f2dffc730d5917ec8fcb" id="tgt20" class="tgtSentence">Geben Sie den Speicherort der Installationsdateien ein, oder klicken Sie auf <ui>Durchsuchen</ui>, um den Speicherort aus einer Liste auszuwählen.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="edf169adb37f4ca4ec523c582ffd880c" id="tgt21" class="tgtSentence">Weitere Dateien und Unterordner aus dem gleichen Ordner einschließen</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="4079902f721aa1dc05159ff969035f5d" id="tgt22" class="tgtSentence">Nur für den <ui>Windows Installer</ui>-Dateityp</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="1ed4340b17b5b8f936c440d6213f4864" id="tgt23" class="tgtSentence">Mitunter sind für eine Software, bei der Windows Installer verwendet wird, unterstützende Dateien erforderlich, die sich meist im gleichen Ordner befinden wie die Installationsdateien.</caps:sentence>
                                <caps:sentence sentenceid="bf02e0b04a60880108ab6ba4bcd4e24c" id="tgt24" class="tgtSentence"> Wählen Sie diese Option aus, wenn Sie auch diese Dateien bereitstellen möchten.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <caps:sentence sentenceid="a15490e75d1e801d7d3cea23f9c90109" id="tgt25" class="tgtSentence">Bei diesem Installationstyp wird etwas Cloudspeicherplatz in Anspruch genommen.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f777dcf051d1886e04cdfa9cb2f0a2ce" id="tgt26" class="tgtSentence">
                          <ui>Externer Link</ui>, und geben Sie dann Folgendes an:</caps:sentence>
                      </para>
                      <table border="1">
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt27" class="tgtSentence">Einstellung</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt28" class="tgtSentence">Details</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="69a118ec5428d02db2d51ebbb3e682c2" id="tgt29" class="tgtSentence">Geben Sie die URL an</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="e98fdea035265cde3640d2bdea61b5a8" id="tgt30" class="tgtSentence">Geben Sie die App Store-URL der App an, die Sie bereitstellen möchten.</caps:sentence>
                                <caps:sentence sentenceid="b0d646ea90598eb426cfc7051793ac20" id="tgt31" class="tgtSentence"> Wenn Sie z. B. die Microsoft-Remotedesktop-App für Android bereitstellen möchten, geben Sie <userInput>https://play.google.com/store/apps/details?id=com.microsoft.rdc.android</userInput> an.</caps:sentence>
                              </para>
                              <alert class="tip">
                                <para>
                                  <caps:sentence sentenceid="c63f34af4af8d533187fbead71bec99a" id="tgt32" class="tgtSentence">Suchen Sie die URL der App, indem Sie mithilfe einer Suchmaschine nach der App Store-Seite mit der App suchen.</caps:sentence>
                                  <caps:sentence sentenceid="2546a2aa539309049a1a180a9e81029f" id="tgt33" class="tgtSentence"> Um z. B. die Remotedesktop-App zu suchen, können Sie nach <userInput>Microsoft Remote Desktop Android</userInput> suchen.</caps:sentence>
                                </para>
                              </alert>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <caps:sentence sentenceid="1e99bc974e49d445dab0f77af0b2f408" id="tgt34" class="tgtSentence">Bei diesem Installationstyp wird kein Cloudspeicherplatz in Anspruch genommen.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f777dcf051d1886e04cdfa9cb2f0a2ce" id="tgt35" class="tgtSentence">
                          <ui>Verwaltete iOS-App aus dem App Store</ui>, und geben Sie dann Folgendes an:</caps:sentence>
                      </para>
                      <table border="1">
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt36" class="tgtSentence">Einstellung</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt37" class="tgtSentence">Details</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="69a118ec5428d02db2d51ebbb3e682c2" id="tgt38" class="tgtSentence">Geben Sie die URL an</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="e98fdea035265cde3640d2bdea61b5a8" id="tgt39" class="tgtSentence">Geben Sie die App Store-URL der App an, die Sie bereitstellen möchten.</caps:sentence>
                                <caps:sentence sentenceid="fda2af1aff4f6bab7f83c263b0249ea1" id="tgt40" class="tgtSentence"> Wenn Sie z. B. die Microsoft-Arbeitsordner-App für iOS bereitstellen möchten, geben Sie <userInput>https://itunes.apple.com/us/app/work-folders/id950878067?mt=8</userInput> an.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <caps:sentence sentenceid="1e99bc974e49d445dab0f77af0b2f408" id="tgt41" class="tgtSentence">Bei diesem Installationstyp wird kein Cloudspeicherplatz in Anspruch genommen.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt42" class="tgtSentence">Konfigurieren Sie auf der Seite <ui>Softwarebeschreibung</ui> Folgendes:</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="d55e5490cfb6d78b91208c948a6434ea" id="tgt43" class="tgtSentence">Je nach Art des verwendeten Installationsprogramms werden einige dieser Werte möglicherweise automatisch eingetragen, oder sie werden nicht angezeigt.</caps:sentence>
                    </para>
                  </alert>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt44" class="tgtSentence">Einstellung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt45" class="tgtSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="52aded165360352a0f5857571d96d68f" id="tgt46" class="tgtSentence">Herausgeber</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="bac22e0408d90d8a255371397d43e4cd" id="tgt47" class="tgtSentence">Geben Sie den Namen des Herausgebers der App ein.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt48" class="tgtSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="965bae69a4253fd60f0e5812bc980e39" id="tgt49" class="tgtSentence">Geben Sie den Namen der App ein, wie er im Unternehmensportal angezeigt wird.</caps:sentence>
                          </para>
                          <alert class="tip">
                            <para>
                              <caps:sentence sentenceid="c4611f906f1d0b74584b641e6b484e36" id="tgt50" class="tgtSentence">Stellen Sie sicher, dass alle App-Namen eindeutig sind.</caps:sentence>
                              <caps:sentence sentenceid="fa2125a5b0726ce0076537556c3398fd" id="tgt51" class="tgtSentence"> Wenn ein App-Name zweimal vergeben wird, wird den Benutzern im Unternehmensportal nur eine der Apps angezeigt.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt52" class="tgtSentence">Beschreibung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2ded9347f84eb8711ecc85a52f001495" id="tgt53" class="tgtSentence">Geben Sie eine Beschreibung der App ein.</caps:sentence>
                            <caps:sentence sentenceid="595ee1efe69e96f5dbad1550ba41f6a0" id="tgt54" class="tgtSentence"> Diese Beschreibung wird den Benutzern im Unternehmensportal angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="a4d47b7de08502f9627b7ab7c0e4a3b4" id="tgt55" class="tgtSentence">URL für Softwareinformationen</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3d1ac0ba49f237d975cc278f795ff1a5" id="tgt56" class="tgtSentence">Nur verfügbar, wenn Sie <ui>Softwareinstallationsprogramm</ui> ausgewählt haben.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="b894bba71a3b18965e9b558b54b6592f" id="tgt57" class="tgtSentence">Optional: Geben Sie eine URL zu einer Website ein, die Informationen über diese App enthält.</caps:sentence>
                            <caps:sentence sentenceid="3da2a333c1f468a6cbef1d89d6b3867b" id="tgt58" class="tgtSentence"> Diese URL wird den Benutzern im Unternehmensportal angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="a031a9b88fe7d5f1b62c960fb61e3893" id="tgt59" class="tgtSentence">URL zu den Datenschutzbestimmungen</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3d1ac0ba49f237d975cc278f795ff1a5" id="tgt60" class="tgtSentence">Nur verfügbar, wenn Sie <ui>Softwareinstallationsprogramm</ui> ausgewählt haben.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="a7976417e47168cfb87ce2ecdb18c35c" id="tgt61" class="tgtSentence">Optional: Geben Sie eine URL zu einer Website ein, die Datenschutzinformationen für diese App enthält.</caps:sentence>
                            <caps:sentence sentenceid="3da2a333c1f468a6cbef1d89d6b3867b" id="tgt62" class="tgtSentence"> Diese URL wird den Benutzern im Unternehmensportal angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="c4ef352f74e502ef5e7bc98e6f4e493d" id="tgt63" class="tgtSentence">Kategorie</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="372721e72d95ae3ca8b9b1dea5563029" id="tgt64" class="tgtSentence">Optional: Wählen Sie eine der integrierten App-Kategorien aus.</caps:sentence>
                            <caps:sentence sentenceid="e5f8d715b93dc06a9cd972d1b2ee37c7" id="tgt65" class="tgtSentence"> Dadurch wird es für die Benutzer leichter, die App im Unternehmensportal zu finden.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="91dc74ba2a55475e8d56aa4fc3a0736e" id="tgt66" class="tgtSentence">Als ausgewählte App anzeigen und im Unternehmensportal hervorheben</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <caps:sentence sentenceid="8e2237c00eca06c96d1d66c5a5b546c7" id="tgt67" class="tgtSentence">  <para>Präsentieren Sie die App herausgehoben auf der Hauptseite des Unternehmensportals, wenn die Benutzer nach Apps suchen. </para></caps:sentence>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="baec6461b0d69dde1b861aefbe375d8a" id="tgt68" class="tgtSentence">Symbol</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="dd049378b556fe8bc56d760d2ece5025" id="tgt69" class="tgtSentence">Optional: Laden Sie ein Symbol hoch, das der App zugeordnet wird.</caps:sentence>
                            <caps:sentence sentenceid="ab8e51a58b9e0470f5dd3802f5d28e3f" id="tgt70" class="tgtSentence"> Dies ist das Symbol, das gemeinsam mit der App angezeigt wird, wenn die Benutzer das Unternehmensportal durchsuchen.</caps:sentence>
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
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt71" class="tgtSentence">Legen Sie auf der Seite <ui>Anforderungen</ui> die Anforderungen fest, die erfüllt sein müssen, bevor die App auf einem Gerät installiert werden kann.</caps:sentence>
                    <caps:sentence sentenceid="325b95ca0b87bac2b78485c83b63d65e" id="tgt72" class="tgtSentence"> Zum Beispiel können Sie bei einem App-Paket für iOS die erforderliche Mindestversion von iOS und den nötigen Gerätetyp festlegen (wie iPhone oder iPad). </caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt73" class="tgtSentence">Die Seite <ui>Anforderungen</ui> wird nicht bei allen Arten von Apps angezeigt.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="f67e1db6301b64c915cdf7d46f2d7266" id="tgt74" class="tgtSentence">Wenn Sie den <ui>Windows Installer</ui>-Dateityp auswählen, werden weitere Assistentenseiten angezeigt.</caps:sentence>
                    <caps:sentence sentenceid="de3ea8159f40bf023fd33fdc6f0784b9" id="tgt75" class="tgtSentence"> Dieser Dateityp wird auf mobilen Geräten nicht verwendet.</caps:sentence>
                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt76" class="tgtSentence"> Weitere Informationen finden Sie unter <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb">Deploy apps to Windows PCs in Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt77" class="tgtSentence">Überprüfen Sie auf der Seite <ui>Zusammenfassung</ui> die von Ihnen angegebenen Informationen.</caps:sentence>
                    <caps:sentence sentenceid="32cf8fc7e52a049a637ac352863f0fb9" id="tgt78" class="tgtSentence"> Sobald Sie bereit sind, klicken Sie auf <ui>Hochladen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt79" class="tgtSentence">Klicken Sie zum Fertigstellen auf <ui>Schließen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="9a2c275183ba10acac49df2abb5fa44a" id="tgt80" class="tgtSentence">Die App wird im Arbeitsbereich <ui>Apps</ui> im Knoten <ui>Apps</ui> angezeigt.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Depl">
        <title>
          <caps:sentence sentenceid="e976e39d4b760d8da395411a44b71d36" id="tgt81" class="tgtSentence">Bereitstellen der App</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9412f190751e2f4c4e69940b1af50104" id="tgt82" class="tgtSentence">In dieser Vorgehensweise stellen Sie die App auf ausgewählten Geräten oder für ausgewählte Benutzer bereit.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="3bbba4611c105d665deb8d806dfc3b56" id="tgt83" class="tgtSentence">So stellen Sie die App bereit</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt84" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Administratorkonsole</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink> auf <ui>Apps</ui> &gt; <ui>Apps</ui>, um die Liste der von Ihnen verwalteten Apps anzuzeigen.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="6f025b31ab813962481e438ec094f3f1" id="tgt85" class="tgtSentence">Wählen Sie die bereitzustellende App aus, und klicken Sie anschließend auf <ui>Bereitstellung verwalten</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt86" class="tgtSentence">Wählen Sie im Dialogfeld <placeholder>&lt;Name der App&gt;</placeholder> auf der Seite <ui>Gruppen auswählen</ui> die Benutzer- oder Gerätegruppen aus, für die die App bereitgestellt werden soll.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt87" class="tgtSentence">Konfigurieren Sie auf der Seite <ui>Bereitstellungsaktion</ui> Folgendes:</caps:sentence>
                  </para>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt88" class="tgtSentence">Einstellung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt89" class="tgtSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="fb251350149d040f301da700807ee378" id="tgt90" class="tgtSentence">Genehmigung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="928fad22ec42c58fd57333359bc58b05" id="tgt91" class="tgtSentence">Wählen Sie aus, welchen Status die App haben soll:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="eec066325ae1683ee4aa953af436a17f" id="tgt92" class="tgtSentence">
                                  <ui>Erforderlich</ui>: Die Installation ist obligatorisch.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="27ebdfaef3842ee0fabce8f995464a0b" id="tgt93" class="tgtSentence">
                                  <ui>Verfügbar</ui>: Die Benutzer installieren die App vom Unternehmensportal nach Bedarf.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="5a6858ff4e2cfaa29829bbfb743ba9bb" id="tgt94" class="tgtSentence">
                                  <ui>Nicht verfügbar</ui>: Die App wird nicht installiert und nicht im Unternehmensportal angezeigt.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="772aa52764bbe2bbc8864be2e9e3cb2b" id="tgt95" class="tgtSentence">
                                  <ui>Deinstallieren</ui>: Die App wird von den Zielgeräten deinstalliert.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="30e482a8ab57cfc19075dece53b0a56b" id="tgt96" class="tgtSentence">Stichtag</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="57102fd148be16c568b26fbaf7aedf24" id="tgt97" class="tgtSentence">Geben Sie für erforderliche Installationen an, wann die App bereitgestellt wird.</caps:sentence>
                            <caps:sentence sentenceid="7a6d0c547347492aaacb033d2aed7d11" id="tgt98" class="tgtSentence"> Sie können hier vordefinierte Werte auswählen oder <ui>Benutzerdefiniert</ui> auswählen, um einen eigenen Stichtag zu konfigurieren.</caps:sentence>
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
                    <caps:sentence sentenceid="6d693503e2d7f764624f7039d56aa2e0" id="tgt99" class="tgtSentence">Wenn die bereitzustellende App mithilfe einer <externalLink><linkText>Richtlinie für die mobile Anwendungsverwaltung</linkText><linkUri>https://technet.microsoft.com/library/dn878026.aspx</linkUri></externalLink> konfiguriert werden kann, wird die Seite <ui>Mobile App-Verwaltung</ui> angezeigt.</caps:sentence>
                    <caps:sentence sentenceid="43629601ab761d2318e3a72ddfd606de" id="tgt100" class="tgtSentence"> Wählen Sie auf dieser Seite die Richtlinie für die mobile Anwendungsverwaltung aus, die Sie dieser App zuordnen möchten.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="5058f1af8388633f609cadb75a75dc9d" id="tgt101" class="tgtSentence">
                        <externalLink>
                          <linkText>Informieren Sie sich, welche Microsoft-Apps mit Richtlinien für die mobile Anwendungsverwaltung kompatibel sind</linkText>
                          <linkUri>https://technet.microsoft.com/library/dn708489.aspx</linkUri>
                        </externalLink>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="7e19041d113381bde1d2f903066b4a43" id="tgt102" class="tgtSentence">Wenn die bereitzustellende App mit Intune-VPN-Profilen kompatibel ist, wird die Seite <ui>VPN-Profil</ui> angezeigt.</caps:sentence>
                    <caps:sentence sentenceid="225e4a904b47d86c2a8f6e4f22ee72cd" id="tgt103" class="tgtSentence"> Auf dieser Seite können Sie festlegen, dass iOS-Apps mit einem von Ihnen bereitgestellten VPN-Profil verknüpft werden sollen.</caps:sentence>
                    <caps:sentence sentenceid="dbc1246de6733c480e554c674f743ddc" id="tgt104" class="tgtSentence"> Die VPN-Verbindung wird automatisch geöffnet, wenn die App gestartet wird.</caps:sentence>
                    <caps:sentence sentenceid="994fe4fa956329561f6aea667aa21f55" id="tgt105" class="tgtSentence"> Um ein VPN-Profil verfügbar zu machen, müssen Sie die <ui>VPN pro App</ui>-Profileinstellung aktivieren.</caps:sentence>
                    <caps:sentence sentenceid="39857b8134bea2bf03bf4f49b609965b" id="tgt106" class="tgtSentence"> Informationen zum Konfigurieren von VPN-Profilen einschließlich der Unterstützung für das Verknüpfen von Profilen mit Apps finden Sie unter <link xlink:href="abc57093-7351-408f-9f41-a30877f96f73">Help users connect to their work using VPN profiles with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <table border="1">
                  <tbody>
                    <tr>
                      <TD>
                        <mediaLink>
                          <image xlink:href="c1789b6e-b49c-45ec-b6da-6359d9acdf36"></image>
                        </mediaLink>
                      </TD>
                      <TD>
                        <para>
                          <caps:sentence sentenceid="738da1feda1a88384c2f61fd37a0b91e" id="tgt107" class="tgtSentence">Wenn Sie die App als <ui>Verfügbar</ui> bereitgestellt haben, wird sie auf den Geräten der Benutzer im Unternehmensportal angezeigt, und von dort aus können die Benutzer sie installieren.</caps:sentence>
                          <caps:sentence sentenceid="3010b79e0b14c4c8b060aca46bd5afc6" id="tgt108" class="tgtSentence"> In diesem Screenshot wurde z. B. die App „Bing für iOS“ mit dem Installationstyp <ui>Externer Link</ui> zusammen mit einem benutzerdefinierten Symbol bereitgestellt. Außerdem wurde die Option <ui>Als ausgewählte App anzeigen und im Unternehmensportal hervorheben</ui> ausgewählt.</caps:sentence>
                        </para>
                      </TD>
                    </tr>
                    <tr>
                      <TD>
                        <mediaLink>
                          <image xlink:href="709c650d-e5cb-4d8c-8aea-e76a08843223"></image>
                        </mediaLink>
                      </TD>
                      <TD>
                        <para>
                          <caps:sentence sentenceid="3ff45f9669ef452f1a69d009c479f8bb" id="tgt109" class="tgtSentence">Wenn Sie die App als „Erforderlich“ bereitgestellt haben, wird der Benutzer benachrichtigt, dass diese App zur Installation bereitsteht.</caps:sentence>
                          <caps:sentence sentenceid="1b216fe5bda165c8d9055238c2c5d1de" id="tgt110" class="tgtSentence"> In diesem Screenshot wurde z. B. die App „Arbeitsordner für iOS“ mit dem Installationstyp <ui>Verwaltete iOS-App aus dem App Store</ui> bereitgestellt.</caps:sentence>
                        </para>
                      </TD>
                    </tr>
                  </tbody>
                </table>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Monitor">
        <title>
          <caps:sentence sentenceid="a3950bed7aa350e6c1998e5aa6f0cff5" id="tgt111" class="tgtSentence">Überwachen der App</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ba0e68e92b51e4de5bf2eedaf9177182" id="tgt112" class="tgtSentence">Die von Ihnen verwalteten Apps und ihr Bereitstellungsstatus werden in der <token>wit_nextref</token>-Konsole angezeigt.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="0ef071cc630160ad0da78a540417af1c" id="tgt113" class="tgtSentence">So zeigen Sie die von Ihnen verwalteten Apps und ihren Status an</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt114" class="tgtSentence">Klicken Sie im Arbeitsbereich <ui>Apps</ui> auf den Knoten <ui>Apps</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="93ec56b0c309d958af0b1fbc466c461f" id="tgt115" class="tgtSentence">Es wird eine Liste der von Ihnen verwalteten Apps angezeigt.</caps:sentence>
                <caps:sentence sentenceid="9967169ff47ffc7c670c1f1a70496bdb" id="tgt116" class="tgtSentence"> Sie können auf eine beliebige App klicken, um im unteren Bereich des Konsolenfensters den Installationsstatus anzuzeigen.</caps:sentence>
                <caps:sentence sentenceid="6d0ef0a225d37294badf05fde2c47604" id="tgt117" class="tgtSentence"> Klicken Sie auf den Status, um weitere Details anzuzeigen.</caps:sentence>
                <caps:sentence sentenceid="ae43c7788094a3e9c4d3c0e6deacdcf7" id="tgt118" class="tgtSentence"> Angenommen, es wird folgender Status angezeigt: <ui>1 Benutzer steht diese Software zur Verfügung</ui>. Sie können dann auf diese Meldung klicken, um den Namen des Benutzers anzuzeigen. </caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence sentenceid="796a75db26fb2b5ed1340e1b901fe1fd" id="tgt119" class="tgtSentence">Über die Dropdownliste <ui>Filter</ui> können Sie nur die Apps anzeigen, die Ihren Kriterien entsprechen, z. B. die Apps, bei denen ein Installationsfehler aufgetreten ist oder die erfolgreich installiert wurden.</caps:sentence>
                </para>
                <para>
                  <mediaLinkInline>
                    <image xlink:href="ee926c78-12c0-4646-8ecc-f844efec9677"></image>
                  </mediaLinkInline>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="e81da430f315cf899496be6fdf605b23" id="tgt120" class="tgtSentence">Außerdem wird im Arbeitsbereich <ui>Dashboard</ui> eine Übersicht über den Status der Apps angezeigt.</caps:sentence>
                <caps:sentence sentenceid="4740240a4242b517dcc0e05ebe42b89c" id="tgt121" class="tgtSentence"> Wenn Sie in der Übersicht auf eine beliebige Stelle klicken, gelangen Sie zur Liste der Apps.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="e18c90954b5c3873f69df3817af5893e" id="tgt122" class="tgtSentence">So zeigen Sie detailliertere Informationen über eine App an</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="f4ed942cec93e3a59c4549f9f47f02ea" id="tgt123" class="tgtSentence">Wählen Sie in der Liste der Apps eine beliebige App aus, und klicken Sie dann auf <ui>Eigenschaften anzeigen</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt124" class="tgtSentence">Klicken Sie auf der Seite <ui>Softwareeigenschaften</ui> für die App auf eine der folgenden Registerkarten:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="eefd7f1795aa7bfe0046432cec946ed0" id="tgt125" class="tgtSentence">
                      <ui>Allgemein</ui>: Zeigt allgemeine Informationen über die App und deren Installationsstatus an.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="daae565972d4a62060813cb6cf27afee" id="tgt126" class="tgtSentence">
                      <ui>Geräte</ui>: Zeigt die Geräte an, bei denen eine gezielte Bereitstellung der App erfolgreich installiert wurde.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2be18b8977408631adf1b15bf7f80e64" id="tgt127" class="tgtSentence">
                      <ui>Benutzer</ui>: Zeigt die Benutzer an, auf deren Geräten eine gezielte Bereitstellung der App erfolgreich installiert wurde.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="e2949bb0f7d9e1d820fc89af9671fa5a" id="tgt128" class="tgtSentence">Wie bereits zuvor können Sie auch hier die Dropdownliste <ui>Filter</ui> verwenden, um die auf den Registerkarten angezeigten Werte zu konfigurieren.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Provision and configure apps with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Now that you've <externalLink><linkText>learned the basics</linkText><linkUri>https://technet.microsoft.com/library/dn646955.aspx</linkUri></externalLink> about <token>wit_firstref</token> app deployment, you'll now learn how to configure and deploy apps to devices enrolled with <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This generally involves three steps:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="#BKMK_Conf">Configure the app</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="#BKMK_Depl">Deploy the app</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="#BKMK_Monitor">Monitor the app</link>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src3" class="srcSentence">For information about how to update and retire apps, see <link xlink:href="beee6933-876a-4be0-b395-4c24cfbd519b">Update and retire apps using Microsoft Intune</link>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src4" class="srcSentence">The information in this topic helps you to deploy apps to <externalLink><linkText>enrolled Windows PCs</linkText><linkUri>https://technet.microsoft.com/library/mt346003.aspx</linkUri></externalLink> and other mobile devices.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> If you want to deploy apps to  <externalLink><linkText>Windows PCs that you manage using the client software</linkText><linkUri>https://technet.microsoft.com/library/dn646959.aspx</linkUri></externalLink>, see <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb">Deploy apps to Windows PCs in Microsoft Intune</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="BKMK_Conf">
        <title>
          <caps:sentence id="src6" class="srcSentence">Configure the app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">In this procedure, you'll use the Intune Software Publisher to configure the properties of the app and, where applicable, upload it to your cloud storage space.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src8" class="srcSentence">To configure an app</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administrator console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Apps</ui> &gt; <ui>Add Apps</ui> to start the Intune software publisher.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src10" class="srcSentence">You might need to enter your Intune username and password before the publisher starts.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">On the <ui>Software setup</ui> page of the software publisher, configure the following:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">
                      <ui>Select how this software is made available to devices</ui> - Choose from:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src13" class="srcSentence">
                          <ui>Software installer</ui>, then specify:</caps:sentence>
                      </para>
                      <table border="1">
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src14" class="srcSentence">Setting</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src15" class="srcSentence">Details</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src16" class="srcSentence">Select the software installer file type</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src17" class="srcSentence">This indicates the type of software you want to deploy.</caps:sentence>
                                <caps:sentence id="src18" class="srcSentence"> For example, if you want to install an iOS app, choose <ui>App Package for iOS (*.ipa file)</ui>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src19" class="srcSentence">Specify the location of the software setup files</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src20" class="srcSentence">Enter the location of the installation files or click <ui>Browse</ui> to select the location from a list.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src21" class="srcSentence">Include additional files and subfolders from the same folder</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src22" class="srcSentence">For the <ui>Windows Installer</ui> file type only</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src23" class="srcSentence">Some software that uses Windows Installer requires supporting files which are typically found in the same folder as the installation files.</caps:sentence>
                                <caps:sentence id="src24" class="srcSentence"> Select this option if you also want to deploy these files.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">This installation type uses some of your cloud storage space.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">
                          <ui>External link</ui>, then specify:</caps:sentence>
                      </para>
                      <table border="1">
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src27" class="srcSentence">Setting</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src28" class="srcSentence">Details</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src29" class="srcSentence">Specify the URL</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src30" class="srcSentence">Enter the app store URL of the app you want to deploy.</caps:sentence>
                                <caps:sentence id="src31" class="srcSentence"> For example, if you want to deploy the Microsoft Remote Desktop app for Android, specify <userInput>https://play.google.com/store/apps/details?id=com.microsoft.rdc.android</userInput>.</caps:sentence>
                              </para>
                              <alert class="tip">
                                <para>
                                  <caps:sentence id="src32" class="srcSentence">To find the URL of the app, use a search engine to find the store page containing the app.</caps:sentence>
                                  <caps:sentence id="src33" class="srcSentence"> For example, to find the Remote Desktop app, you could search <userInput>Microsoft Remote Desktop Android</userInput>.</caps:sentence>
                                </para>
                              </alert>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">This installation type does not use any of your cloud storage space.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">
                          <ui>Managed iOS app from the app store</ui>, then specify:</caps:sentence>
                      </para>
                      <table border="1">
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src36" class="srcSentence">Setting</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src37" class="srcSentence">Details</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src38" class="srcSentence">Specify the URL</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src39" class="srcSentence">Enter the app store URL of the app you want to deploy.</caps:sentence>
                                <caps:sentence id="src40" class="srcSentence"> For example, if you want to deploy the Microsoft Work Folders app for iOS, specify <userInput>https://itunes.apple.com/us/app/work-folders/id950878067?mt=8</userInput>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">This installation type does not use any of your cloud storage space.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">On the <ui>Software description</ui> page, configure the following:</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src43" class="srcSentence">Depending on the installer type you are using, some of these values might have been automatically entered, or might not appear.</caps:sentence>
                    </para>
                  </alert>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src44" class="srcSentence">Setting</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src45" class="srcSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src46" class="srcSentence">Publisher</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src47" class="srcSentence">Enter the name of the publisher of the app.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src48" class="srcSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src49" class="srcSentence">Enter the name of the app as it will be displayed in the company portal.</caps:sentence>
                          </para>
                          <alert class="tip">
                            <para>
                              <caps:sentence id="src50" class="srcSentence">Make sure all app names you use are unique.</caps:sentence>
                              <caps:sentence id="src51" class="srcSentence"> If the same app name exists twice, only one of the apps will be displayed to users in the company portal.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src52" class="srcSentence">Description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src53" class="srcSentence">Enter a description for the app.</caps:sentence>
                            <caps:sentence id="src54" class="srcSentence"> This will be displayed to users in the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src55" class="srcSentence">URL for software information</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src56" class="srcSentence">Available only if you selected <ui>Software installer</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src57" class="srcSentence">(optional) Enter a URL to a website that contains information about this app.</caps:sentence>
                            <caps:sentence id="src58" class="srcSentence"> The URL will be displayed to users in the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src59" class="srcSentence">Privacy URL</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src60" class="srcSentence">Available only if you selected <ui>Software installer</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">(optional) Enter a URL to a website that contains privacy information for this app.</caps:sentence>
                            <caps:sentence id="src62" class="srcSentence"> The URL will be displayed to users in the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src63" class="srcSentence">Category</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src64" class="srcSentence">(optional) Select one of the built-in app categories.</caps:sentence>
                            <caps:sentence id="src65" class="srcSentence"> This will make it easier for users to find the app when they browse the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src66" class="srcSentence">Display this as a featured app and highlight it in the company portal</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <caps:sentence id="src67" class="srcSentence">  <para>Display the app prominently on the main page of the company portal when users browse for apps. </para></caps:sentence>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src68" class="srcSentence">Icon</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src69" class="srcSentence">(optional) Upload an icon that will be associated with the app.</caps:sentence>
                            <caps:sentence id="src70" class="srcSentence"> This is the icon that will be displayed with the app when users browse the company portal.</caps:sentence>
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
                    <caps:sentence id="src71" class="srcSentence">On the <ui>Requirements</ui> page, select the requirements that must be met before the app can start to install on a device.</caps:sentence>
                    <caps:sentence id="src72" class="srcSentence"> For example, for an app package for iOS, you can select the minimum version of iOS required, and the type of device it must be, like an iPhone, or an iPad.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src73" class="srcSentence">The <ui>Requirements</ui> page is not displayed for all types of apps.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">Further wizard pages are displayed when you choose the <ui>Windows Installer</ui> file type.</caps:sentence>
                    <caps:sentence id="src75" class="srcSentence"> This file type is not used by mobile devices.</caps:sentence>
                    <caps:sentence id="src76" class="srcSentence"> For more information, see <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb">Deploy apps to Windows PCs in Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">On the <ui>Summary</ui> page, review the information you specified.</caps:sentence>
                    <caps:sentence id="src78" class="srcSentence"> Once you are ready, click <ui>Upload</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">Click <ui>Close</ui> to finish.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src80" class="srcSentence">The app is displayed on the <ui>Apps</ui> node of the <ui>Apps</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Depl">
        <title>
          <caps:sentence id="src81" class="srcSentence">Deploy the app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src82" class="srcSentence">In this procedure, you'll deploy the app to selected devices or users.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src83" class="srcSentence">To deploy the app</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administrator console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Apps</ui> &gt; <ui>Apps</ui> to view the list of apps you manage.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">Select the app you want to deploy, and then click <ui>Manage Deployment</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">In the <placeholder>&lt;app name&gt;</placeholder> dialog box, on the <ui>Select Groups</ui> page, choose the user or device groups to which you want to deploy the app.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">On the <ui>Deployment Action</ui> page, configure the following:</caps:sentence>
                  </para>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src88" class="srcSentence">Setting</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src89" class="srcSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src90" class="srcSentence">Approval</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src91" class="srcSentence">Choose whether the deployment is:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src92" class="srcSentence">
                                  <ui>Required</ui> (mandatory install)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src93" class="srcSentence">
                                  <ui>Available</ui> (users install from the company portal on demand)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src94" class="srcSentence">
                                  <ui>Not Applicable</ui> (the app is not installed or shown in the company portal)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src95" class="srcSentence">
                                  <ui>Uninstall</ui> (the app will be uninstalled from targeted devices)</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src96" class="srcSentence">Deadline</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src97" class="srcSentence">For required installations, choose how soon the app will be deployed.</caps:sentence>
                            <caps:sentence id="src98" class="srcSentence"> You can choose from the predefined values, or select <ui>Custom</ui> to configure your own deadline.</caps:sentence>
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
                    <caps:sentence id="src99" class="srcSentence">If the app you are deploying can be configured by a <externalLink><linkText>mobile application management policy</linkText><linkUri>https://technet.microsoft.com/library/dn878026.aspx</linkUri></externalLink>, the <ui>Mobile App Management</ui> page is displayed.</caps:sentence>
                    <caps:sentence id="src100" class="srcSentence"> On this page, choose the mobile application management policy you want to associate with this app.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src101" class="srcSentence">
                        <externalLink>
                          <linkText>See which Microsoft apps are compatible with mobile application management policies</linkText>
                          <linkUri>https://technet.microsoft.com/library/dn708489.aspx</linkUri>
                        </externalLink>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">If the app you are deploying is compatible with Intune VPN profiles, the <ui>VPN Profile</ui> page is displayed.</caps:sentence>
                    <caps:sentence id="src103" class="srcSentence"> On this page, you can choose to associate iOS apps with a VPN profile you have deployed.</caps:sentence>
                    <caps:sentence id="src104" class="srcSentence"> The VPN connection will be automatically opened when the app is launched.</caps:sentence>
                    <caps:sentence id="src105" class="srcSentence"> To make a VPN profile available, it must have the <ui>Per-app VPN</ui> profile setting enabled.</caps:sentence>
                    <caps:sentence id="src106" class="srcSentence"> For information about how to configure VPN profiles, including support for associating profiles with apps, see <link xlink:href="abc57093-7351-408f-9f41-a30877f96f73">Help users connect to their work using VPN profiles with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <table border="1">
                  <tbody>
                    <tr>
                      <TD>
                        <mediaLink>
                          <image xlink:href="c1789b6e-b49c-45ec-b6da-6359d9acdf36"></image>
                        </mediaLink>
                      </TD>
                      <TD>
                        <para>
                          <caps:sentence id="src107" class="srcSentence">If you deployed the app as <ui>Available</ui>, it will be displayed in the company portal on users device from where they can install the app.</caps:sentence>
                          <caps:sentence id="src108" class="srcSentence"> For example, in this screenshot, the Bing for iOS app was deployed using the <ui>External Link</ui> installation type, with a custom icon, and the option <ui>Display this as a featured app and highlight it in the company portal</ui> was selected.</caps:sentence>
                        </para>
                      </TD>
                    </tr>
                    <tr>
                      <TD>
                        <mediaLink>
                          <image xlink:href="709c650d-e5cb-4d8c-8aea-e76a08843223"></image>
                        </mediaLink>
                      </TD>
                      <TD>
                        <para>
                          <caps:sentence id="src109" class="srcSentence">If you deployed the app as required, the user will get a notification that an app is ready to install.</caps:sentence>
                          <caps:sentence id="src110" class="srcSentence"> For example, in this screenshot, the Work Folders for iOS app was deployed using the <ui>Managed iOS app from the app store</ui> installation type.</caps:sentence>
                        </para>
                      </TD>
                    </tr>
                  </tbody>
                </table>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Monitor">
        <title>
          <caps:sentence id="src111" class="srcSentence">Monitor the app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src112" class="srcSentence">You can see the apps you manage, and their deployment status in the <token>wit_nextref</token> console.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src113" class="srcSentence">To view the apps you manage and their status</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src114" class="srcSentence">In the <ui>Apps</ui> workspace, click the <ui>Apps</ui> node.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src115" class="srcSentence">The list of apps you manage will be displayed.</caps:sentence>
                <caps:sentence id="src116" class="srcSentence"> You can click on any app to see an installation status in the lower pane of the console windows.</caps:sentence>
                <caps:sentence id="src117" class="srcSentence"> Click the status to see more details.</caps:sentence>
                <caps:sentence id="src118" class="srcSentence"> For example, if the status shows <ui>1 user has this software available</ui>, you can click the message to see the name of the user.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence id="src119" class="srcSentence">You can use the <ui>Filters</ui> drop-down list to show only apps that meet the criteria you specify, like apps that failed to install, or apps that were successfully deployed.</caps:sentence>
                </para>
                <para>
                  <mediaLinkInline>
                    <image xlink:href="ee926c78-12c0-4646-8ecc-f844efec9677"></image>
                  </mediaLinkInline>
                </para>
              </alert>
              <para>
                <caps:sentence id="src120" class="srcSentence">Additionally, the <ui>Dashboard</ui> workspace shows an overview of the status of your apps.</caps:sentence>
                <caps:sentence id="src121" class="srcSentence"> If you click anywhere in the overview, you'll be taken to the list of apps.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src122" class="srcSentence">To view more detailed information about an app</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src123" class="srcSentence">In the list of apps, select any app, and then click <ui>View Properties</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src124" class="srcSentence">On the <ui>Software Properties</ui> page for the app, click one of these tabs:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">
                      <ui>General</ui> - Shows general information about the app and its installation status.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">
                      <ui>Devices</ui> - Shows the devices that successfully installed a targeted deployment of the app.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">
                      <ui>Users</ui> - Shows the users whose devices successfully installed a targeted deployment of the app.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src128" class="srcSentence">As before, you can use the <ui>Filters</ui> drop-down list to configure the values shown on each of the tabs.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Provision and configure apps with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>