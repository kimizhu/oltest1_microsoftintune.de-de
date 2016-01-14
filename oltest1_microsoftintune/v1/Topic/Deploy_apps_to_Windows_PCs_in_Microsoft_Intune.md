---
description: na
keywords: na
title: Deploy apps to Windows PCs in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4105b676-11f1-4cd2-88a4-b37d186cdbdb
---
# Bereitstellen von Apps auf Windows-PCs in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f13201fed29755ea6bde03a4eda76cb2" id="tgt1" class="tgtSentence">Nachdem Sie sich mit den <externalLink><linkText>ersten Schritten</linkText><linkUri>https://technet.microsoft.com/library/dn646955.aspx</linkUri></externalLink> bei der Bereitstellung von Apps mit <token>wit_firstref</token> vertraut gemacht haben, erfahren Sie in diesem Thema, wie Sie Apps für die von Ihnen verwalteten Windows-PCs konfigurieren und darauf bereitstellen.</caps:sentence>
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
            <caps:sentence sentenceid="223d8227707afeb1da9b03ad1e2ddce4" id="tgt4" class="tgtSentence">Die Informationen in diesem Thema helfen Ihnen beim Bereitstellen von Apps auf <externalLink><linkText>Windows-PCs, die Sie mithilfe der Clientsoftware verwalten</linkText><linkUri>https://technet.microsoft.com/library/dn646959.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence sentenceid="5d2519637707b0c96fd08c71025ba4d2" id="tgt5" class="tgtSentence"> Wenn Sie Apps auf <externalLink><linkText>registrierten Windows-PCs</linkText><linkUri>https://technet.microsoft.com/library/mt346003.aspx</linkUri></externalLink> und anderen mobilen Geräten bereitstellen möchten, finden Sie entsprechende Informationen unter <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy apps to mobile devices in Microsoft Intune</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="BKMK_Conf">
        <title>
          <caps:sentence sentenceid="c0f31e254bf659b63314100f70766e66" id="tgt6" class="tgtSentence">Konfigurieren der App</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7367510a2b22b9f8ffbcc3221990a091" id="tgt7" class="tgtSentence">In dieser Vorgehensweise verwenden Sie den Intune-Softwareherausgeber, um die Eigenschaften der App zu konfigurieren und sie in Ihren Cloudspeicher hochzuladen.</caps:sentence>
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
                    <caps:sentence sentenceid="d7ddc7ab077fbd4c863dc649eb1e3908" id="tgt12" class="tgtSentence">
                      <ui>Wählen Sie aus, wie diese Software für Geräte bereitgestellt werden soll.</ui> – Wählen Sie <ui>Softwareinstallationsprogramm</ui>, und legen Sie dann Folgendes fest:</caps:sentence>
                  </para>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt13" class="tgtSentence">Einstellung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt14" class="tgtSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="ca64f3dcc207c6e7b42eac6c8af3d5c0" id="tgt15" class="tgtSentence">Wählen Sie den Dateityp des Softwareinstallationsprogramms aus</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="81fb4f6963cee019f57c26e75574a651" id="tgt16" class="tgtSentence">Hiermit wird die Art der Software angegeben, die Sie bereitstellen möchten.</caps:sentence>
                            <caps:sentence sentenceid="ba55eb4724fe33a89b94eeba7536d1fd" id="tgt17" class="tgtSentence"> Wählen Sie für einen Windows-PC <ui>Windows Installer</ui> aus.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="fc961e16156fb2c205083cbdd949121e" id="tgt18" class="tgtSentence">Geben Sie den Speicherort der Softwaresetupdateien an</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6a4c45ba9ab5f2dffc730d5917ec8fcb" id="tgt19" class="tgtSentence">Geben Sie den Speicherort der Installationsdateien ein, oder klicken Sie auf <ui>Durchsuchen</ui>, um den Speicherort aus einer Liste auszuwählen.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="edf169adb37f4ca4ec523c582ffd880c" id="tgt20" class="tgtSentence">Weitere Dateien und Unterordner aus dem gleichen Ordner einschließen</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1ed4340b17b5b8f936c440d6213f4864" id="tgt21" class="tgtSentence">Mitunter sind für eine Software, bei der Windows Installer verwendet wird, unterstützende Dateien erforderlich, die sich meist im gleichen Ordner befinden wie die Installationsdateien.</caps:sentence>
                            <caps:sentence sentenceid="7e6599a260177be50424286ed3e77cdc" id="tgt22" class="tgtSentence"> Wählen Sie diese Option aus, wenn Sie auch diese unterstützenden Dateien bereitstellen möchten.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence sentenceid="a15490e75d1e801d7d3cea23f9c90109" id="tgt23" class="tgtSentence">Bei diesem Installationstyp wird etwas Cloudspeicherplatz in Anspruch genommen.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt24" class="tgtSentence">Konfigurieren Sie auf der Seite <ui>Softwarebeschreibung</ui> Folgendes:</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="8d772e196a95796a3f5c068004ea5cba" id="tgt25" class="tgtSentence">Je nach verwendeter Installationsdatei werden einige dieser Werte möglicherweise automatisch eingetragen, oder sie werden nicht angezeigt.</caps:sentence>
                    </para>
                  </alert>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt26" class="tgtSentence">Einstellung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt27" class="tgtSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="52aded165360352a0f5857571d96d68f" id="tgt28" class="tgtSentence">Herausgeber</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="bac22e0408d90d8a255371397d43e4cd" id="tgt29" class="tgtSentence">Geben Sie den Namen des Herausgebers der App ein.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt30" class="tgtSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="965bae69a4253fd60f0e5812bc980e39" id="tgt31" class="tgtSentence">Geben Sie den Namen der App ein, wie er im Unternehmensportal angezeigt wird.</caps:sentence>
                          </para>
                          <alert class="tip">
                            <para>
                              <caps:sentence sentenceid="c4611f906f1d0b74584b641e6b484e36" id="tgt32" class="tgtSentence">Stellen Sie sicher, dass alle App-Namen eindeutig sind.</caps:sentence>
                              <caps:sentence sentenceid="fa2125a5b0726ce0076537556c3398fd" id="tgt33" class="tgtSentence"> Wenn ein App-Name zweimal vergeben wird, wird den Benutzern im Unternehmensportal nur eine der Apps angezeigt.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt34" class="tgtSentence">Beschreibung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2ded9347f84eb8711ecc85a52f001495" id="tgt35" class="tgtSentence">Geben Sie eine Beschreibung der App ein.</caps:sentence>
                            <caps:sentence sentenceid="595ee1efe69e96f5dbad1550ba41f6a0" id="tgt36" class="tgtSentence"> Diese Beschreibung wird den Benutzern im Unternehmensportal angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="a4d47b7de08502f9627b7ab7c0e4a3b4" id="tgt37" class="tgtSentence">URL für Softwareinformationen</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b894bba71a3b18965e9b558b54b6592f" id="tgt38" class="tgtSentence">Optional: Geben Sie eine URL zu einer Website ein, die Informationen über diese App enthält.</caps:sentence>
                            <caps:sentence sentenceid="3da2a333c1f468a6cbef1d89d6b3867b" id="tgt39" class="tgtSentence"> Diese URL wird den Benutzern im Unternehmensportal angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="a031a9b88fe7d5f1b62c960fb61e3893" id="tgt40" class="tgtSentence">URL zu den Datenschutzbestimmungen</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a7976417e47168cfb87ce2ecdb18c35c" id="tgt41" class="tgtSentence">Optional: Geben Sie eine URL zu einer Website ein, die Datenschutzinformationen für diese App enthält.</caps:sentence>
                            <caps:sentence sentenceid="3da2a333c1f468a6cbef1d89d6b3867b" id="tgt42" class="tgtSentence"> Diese URL wird den Benutzern im Unternehmensportal angezeigt.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="c4ef352f74e502ef5e7bc98e6f4e493d" id="tgt43" class="tgtSentence">Kategorie</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="372721e72d95ae3ca8b9b1dea5563029" id="tgt44" class="tgtSentence">Optional: Wählen Sie eine der integrierten App-Kategorien aus.</caps:sentence>
                            <caps:sentence sentenceid="e5f8d715b93dc06a9cd972d1b2ee37c7" id="tgt45" class="tgtSentence"> Dadurch wird es für die Benutzer leichter, die App im Unternehmensportal zu finden.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="baec6461b0d69dde1b861aefbe375d8a" id="tgt46" class="tgtSentence">Symbol</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="dd049378b556fe8bc56d760d2ece5025" id="tgt47" class="tgtSentence">Optional: Laden Sie ein Symbol hoch, das der App zugeordnet wird.</caps:sentence>
                            <caps:sentence sentenceid="ab8e51a58b9e0470f5dd3802f5d28e3f" id="tgt48" class="tgtSentence"> Dies ist das Symbol, das gemeinsam mit der App angezeigt wird, wenn die Benutzer das Unternehmensportal durchsuchen.</caps:sentence>
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
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt49" class="tgtSentence">Legen Sie auf der Seite <ui>Anforderungen</ui> die Anforderungen fest, die erfüllt sein müssen, bevor die App auf einem Gerät installiert werden kann. Legen Sie dort folgende Einstellungen fest:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="be0782d9fb865cebc634ed32966da27b" id="tgt50" class="tgtSentence">
                          <ui>Architektur</ui>: Wählen Sie aus, ob die App auf 32-Bit-Betriebssystemen, 64-Bit-Betriebssystemen oder auf beiden Betriebssystemarten installiert werden kann.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4d7c961b3a752fb0ee108f8a9064c88c" id="tgt51" class="tgtSentence">
                          <ui>Betriebssystem</ui>: Wählen Sie die niedrigste Betriebssystemvariante aus, unter der die App installiert werden kann.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="4079902f721aa1dc05159ff969035f5d" id="tgt52" class="tgtSentence">Nur für den <ui>Windows Installer</ui>-Dateityp (nur EXE): Auf der Seite <ui>Erkennungsregeln</ui> können Sie Regeln konfigurieren, anhand derer erkannt wird, ob die konfigurierte App bereits auf dem PC vorhanden ist. Sie können aber auch die Standarderkennungsregeln verwenden, bei denen alle zuvor installierten Versionen der App überschrieben werden.</caps:sentence>
                    <caps:sentence sentenceid="3971844fccc26a2efc8d56c585826cbd" id="tgt53" class="tgtSentence"> Sie können folgende Regeln konfigurieren:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="204c7efe90364f861ac9c6d72dff5a3c" id="tgt54" class="tgtSentence">
                          <ui>Die Datei ist vorhanden</ui>: Geben Sie den Pfad zu der Datei an, die Sie erkennen möchten.</caps:sentence>
                        <caps:sentence sentenceid="d4ee77429152a51978896620de692c25" id="tgt55" class="tgtSentence"> Sie können den PC unter <ui>%ProgramFiles%</ui> durchsuchen (dabei wird <ui>Programme</ui>\<placeholder>&lt;Pfad&gt;</placeholder> und <ui>Programme (x86)</ui>\<placeholder>&lt;Pfad&gt;</placeholder> durchsucht) oder unter <ui>%SystemDrive%</ui> (dabei wird das Stammlaufwerk des PCs durchsucht, in der Regel C:)</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="5058f1af8388633f609cadb75a75dc9d" id="tgt56" class="tgtSentence">.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="51ba8b693db25ae97d6ba110b0b7b149" id="tgt57" class="tgtSentence">
                          <ui>Der MSI-Produktcode ist vorhanden</ui>: Klicken Sie auf <ui>Durchsuchen</ui>, um die zu erkennende Windows Installer-Datei (MSI-Datei) auszuwählen.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d1b2b4d18ff616e79f6c87808d2b47f0" id="tgt58" class="tgtSentence">
                          <ui>Der Registrierungsschlüssel ist vorhanden</ui>: Geben Sie einen Registrierungsschlüssel an, der mit <ui>HKEY_LOCAL_MACHINE\</ui> beginnt.</caps:sentence>
                        <caps:sentence sentenceid="1f835ddf660534a48ec15be6cb405504" id="tgt59" class="tgtSentence"> Es werden 32-Bit- und 64-Bit-Registrierungspfade durchsucht.</caps:sentence>
                        <caps:sentence sentenceid="ea6f63f9af103ad987700fb749090462" id="tgt60" class="tgtSentence"> Wenn der angegebene Schlüssel an einem der beiden Speicherorte vorhanden ist, ist die Erkennungsregel erfüllt.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="a3fe19f6d266374fffbee7c66a9a96ef" id="tgt61" class="tgtSentence">Wenn die App eine der konfigurierten Regeln erfüllt, wird sie nicht installiert.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="4079902f721aa1dc05159ff969035f5d" id="tgt62" class="tgtSentence">Nur für den <ui>Windows Installer</ui>-Dateityp (MSI und EXE): Geben Sie auf der Seite <ui>Befehlszeilenargumente</ui> an, ob Sie optionale Befehlszeilenargumente für das Installationsprogramm angeben möchten.</caps:sentence>
                    <caps:sentence sentenceid="ed3b3c356dd44f04127d588580de948f" id="tgt63" class="tgtSentence"> Beispielsweise unterstützen einige Installationsprogramme das Argument <ui>/q</ui> für eine unbeaufsichtigte Installation ohne Benutzereingriff.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="4079902f721aa1dc05159ff969035f5d" id="tgt64" class="tgtSentence">Nur für den <ui>Windows Installer</ui>-Dateityp (nur EXE): Auf der Seite <ui>Rückgabecodes</ui> können Sie neue Fehlercodes eingeben, die von Intune interpretiert werden, wenn die App auf einem verwalteten Windows-PC installiert wird.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="e6dcdb79d138fe36d54b44d6d9d8cc9c" id="tgt65" class="tgtSentence">Standardmäßig werden in <token>wit_nextref</token> die branchenüblichen Rückgabecodes verwendet, um eine fehlerhafte oder erfolgreiche Installation eines App-Pakets zu melden.</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a7050d7297a8cd0e8250f2d7c3e833d3" id="tgt66" class="tgtSentence">
                          <ui>0</ui>: Erfolg</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="56723e9a487cb2206bc17785c577513a" id="tgt67" class="tgtSentence">
                          <ui>3010</ui>: Erfolg mit Neustart</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="6d7a2fb60dcfb48b6b9ecc45591b1bc5" id="tgt68" class="tgtSentence">Sie können der Liste auch Ihre eigenen Rückgabecodes hinzufügen.</caps:sentence>
                    <caps:sentence sentenceid="866ea51ac8952248498a57b8da25429e" id="tgt69" class="tgtSentence"> Wenn Sie eine Liste von Rückgabecodes angeben und bei der App-Installation ein in der Liste nicht enthaltener Code zurückgegeben wird, wird er als Fehler interpretiert.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt70" class="tgtSentence">Überprüfen Sie auf der Seite <ui>Zusammenfassung</ui> die von Ihnen angegebenen Informationen.</caps:sentence>
                    <caps:sentence sentenceid="32cf8fc7e52a049a637ac352863f0fb9" id="tgt71" class="tgtSentence"> Sobald Sie bereit sind, klicken Sie auf <ui>Hochladen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt72" class="tgtSentence">Klicken Sie zum Fertigstellen auf <ui>Schließen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="9a2c275183ba10acac49df2abb5fa44a" id="tgt73" class="tgtSentence">Die App wird im Arbeitsbereich <ui>Apps</ui> im Knoten <ui>Apps</ui> angezeigt.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Depl">
        <title>
          <caps:sentence sentenceid="e976e39d4b760d8da395411a44b71d36" id="tgt74" class="tgtSentence">Bereitstellen der App</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9412f190751e2f4c4e69940b1af50104" id="tgt75" class="tgtSentence">In dieser Vorgehensweise stellen Sie die App auf ausgewählten Geräten oder für ausgewählte Benutzer bereit.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="3bbba4611c105d665deb8d806dfc3b56" id="tgt76" class="tgtSentence">So stellen Sie die App bereit</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt77" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Administratorkonsole</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink> auf <ui>Apps</ui> &gt; <ui>Apps</ui>, um die Liste der von Ihnen verwalteten Apps anzuzeigen.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="6f025b31ab813962481e438ec094f3f1" id="tgt78" class="tgtSentence">Wählen Sie die bereitzustellende App aus, und klicken Sie anschließend auf <ui>Bereitstellung verwalten</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt79" class="tgtSentence">Wählen Sie im Dialogfeld <placeholder>&lt;Name der App&gt;</placeholder> zuerst auf der Seite <ui>Gruppen auswählen</ui> die Benutzer- oder Gerätegruppen aus, für die die App bereitgestellt werden soll.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt80" class="tgtSentence">Konfigurieren Sie auf der Seite <ui>Bereitstellungsaktion</ui> Folgendes:</caps:sentence>
                  </para>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt81" class="tgtSentence">Einstellung</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt82" class="tgtSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="fb251350149d040f301da700807ee378" id="tgt83" class="tgtSentence">Genehmigung</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="928fad22ec42c58fd57333359bc58b05" id="tgt84" class="tgtSentence">Wählen Sie aus, welchen Status die App haben soll:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="eec066325ae1683ee4aa953af436a17f" id="tgt85" class="tgtSentence">
                                  <ui>Erforderlich</ui>: Die Installation ist obligatorisch.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="27ebdfaef3842ee0fabce8f995464a0b" id="tgt86" class="tgtSentence">
                                  <ui>Verfügbar</ui>: Die Benutzer installieren die App vom Unternehmensportal nach Bedarf.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="5a6858ff4e2cfaa29829bbfb743ba9bb" id="tgt87" class="tgtSentence">
                                  <ui>Nicht verfügbar</ui>: Die App wird nicht installiert und nicht im Unternehmensportal angezeigt.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="772aa52764bbe2bbc8864be2e9e3cb2b" id="tgt88" class="tgtSentence">
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
                              <caps:sentence sentenceid="30e482a8ab57cfc19075dece53b0a56b" id="tgt89" class="tgtSentence">Stichtag</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="57102fd148be16c568b26fbaf7aedf24" id="tgt90" class="tgtSentence">Geben Sie für erforderliche Installationen an, wann die App bereitgestellt wird.</caps:sentence>
                            <caps:sentence sentenceid="7a6d0c547347492aaacb033d2aed7d11" id="tgt91" class="tgtSentence"> Sie können hier vordefinierte Werte auswählen oder <ui>Benutzerdefiniert</ui> auswählen, um einen eigenen Stichtag zu konfigurieren.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Monitor">
        <title>
          <caps:sentence sentenceid="a3950bed7aa350e6c1998e5aa6f0cff5" id="tgt92" class="tgtSentence">Überwachen der App</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ba0e68e92b51e4de5bf2eedaf9177182" id="tgt93" class="tgtSentence">Die von Ihnen verwalteten Apps und ihr Bereitstellungsstatus werden in der <token>wit_nextref</token>-Konsole angezeigt.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="0ef071cc630160ad0da78a540417af1c" id="tgt94" class="tgtSentence">So zeigen Sie die von Ihnen verwalteten Apps und ihren Status an</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt95" class="tgtSentence">Klicken Sie im Arbeitsbereich <ui>Apps</ui> auf den Knoten <ui>Apps</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="93ec56b0c309d958af0b1fbc466c461f" id="tgt96" class="tgtSentence">Es wird eine Liste der von Ihnen verwalteten Apps angezeigt.</caps:sentence>
                <caps:sentence sentenceid="9967169ff47ffc7c670c1f1a70496bdb" id="tgt97" class="tgtSentence"> Sie können auf eine beliebige App klicken, um im unteren Bereich des Konsolenfensters den Installationsstatus anzuzeigen.</caps:sentence>
                <caps:sentence sentenceid="d1911f5df9459bbe4e10b89ad02a4818" id="tgt98" class="tgtSentence"> Klicken Sie auf diesen Status, um weitere Details anzuzeigen.</caps:sentence>
                <caps:sentence sentenceid="ae43c7788094a3e9c4d3c0e6deacdcf7" id="tgt99" class="tgtSentence"> Angenommen, es wird folgender Status angezeigt: <ui>1 Benutzer steht diese Software zur Verfügung</ui>. Sie können dann auf diese Meldung klicken, um den Namen des Benutzers anzuzeigen. </caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence sentenceid="796a75db26fb2b5ed1340e1b901fe1fd" id="tgt100" class="tgtSentence">Über die Dropdownliste <ui>Filter</ui> können Sie die Anzeige auf diejenigen Apps beschränken, die von Ihnen angegebenen Kriterien entsprechen, z. B. die Apps, bei denen ein Installationsfehler aufgetreten ist oder die erfolgreich installiert wurden.</caps:sentence>
                </para>
                <para>
                  <mediaLinkInline>
                    <image xlink:href="ee926c78-12c0-4646-8ecc-f844efec9677"></image>
                  </mediaLinkInline>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="e81da430f315cf899496be6fdf605b23" id="tgt101" class="tgtSentence">Außerdem wird im Arbeitsbereich <ui>Dashboard</ui> eine Übersicht über den Status der Apps angezeigt.</caps:sentence>
                <caps:sentence sentenceid="4740240a4242b517dcc0e05ebe42b89c" id="tgt102" class="tgtSentence"> Wenn Sie in der Übersicht auf eine beliebige Stelle klicken, gelangen Sie zur Liste der Apps.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="e18c90954b5c3873f69df3817af5893e" id="tgt103" class="tgtSentence">So zeigen Sie detailliertere Informationen über eine App an</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="f4ed942cec93e3a59c4549f9f47f02ea" id="tgt104" class="tgtSentence">Wählen Sie in der Liste der Apps eine beliebige App aus, und klicken Sie dann auf <ui>Eigenschaften anzeigen</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt105" class="tgtSentence">Klicken Sie auf der Seite <ui>Softwareeigenschaften</ui> für die App auf eine der folgenden Registerkarten:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1c32f515b151586e6c9773ea7ad85b32" id="tgt106" class="tgtSentence">
                      <ui>Allgemein</ui>: Zeigt allgemeine Informationen über die App und deren Installationsstatus an.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="daae565972d4a62060813cb6cf27afee" id="tgt107" class="tgtSentence">
                      <ui>Geräte</ui>: Zeigt die Geräte an, bei denen eine gezielte Bereitstellung der App erfolgreich installiert wurde.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="782093c4b20cb05c910e14bb8bf992e9" id="tgt108" class="tgtSentence">
                      <ui>Benutzer</ui>: Zeigt die Benutzer an, auf deren Geräten eine gezielte Bereitstellung der App erfolgreich installiert wurde.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="e2949bb0f7d9e1d820fc89af9671fa5a" id="tgt109" class="tgtSentence">Wie bereits zuvor können Sie auch hier die Dropdownliste <ui>Filter</ui> verwenden, um die auf den Registerkarten angezeigten Werte zu konfigurieren.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Now that you've <externalLink><linkText>learned the basics</linkText><linkUri>https://technet.microsoft.com/library/dn646955.aspx</linkUri></externalLink> about <token>wit_firstref</token> app deployment, in this topic, you'll learn how to actually configure and deploy apps to Windows PCs you manage.</caps:sentence>
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
            <caps:sentence id="src4" class="srcSentence">The information in this topic helps you to deploy apps to <externalLink><linkText>Windows PCs that you manage using the client software</linkText><linkUri>https://technet.microsoft.com/library/dn646959.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> If you want to deploy apps to <externalLink><linkText>enrolled Windows PCs</linkText><linkUri>https://technet.microsoft.com/library/mt346003.aspx</linkUri></externalLink> and other mobile devices, see <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy apps to mobile devices in Microsoft Intune</link>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section address="BKMK_Conf">
        <title>
          <caps:sentence id="src6" class="srcSentence">Configure the app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">In this procedure, you'll use the Intune Software Publisher to configure the properties of the app and upload it to your cloud storage space.</caps:sentence>
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
                      <ui>Select how this software is made available to devices</ui> - Choose <ui>Software installer</ui>, then specify:</caps:sentence>
                  </para>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src13" class="srcSentence">Setting</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src14" class="srcSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src15" class="srcSentence">Select the software installer file type</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src16" class="srcSentence">This indicates the type of software you want to deploy.</caps:sentence>
                            <caps:sentence id="src17" class="srcSentence"> For a Windows PC, choose <ui>Windows Installer</ui>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src18" class="srcSentence">Specify the location of the software setup files</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src19" class="srcSentence">Enter the location of the installation files or click <ui>Browse</ui> to select the location from a list.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src20" class="srcSentence">Include additional files and subfolders from the same folder</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src21" class="srcSentence">Some software that uses Windows Installer requires supporting files which are typically found in the same folder as the installation files.</caps:sentence>
                            <caps:sentence id="src22" class="srcSentence"> Select this option if you also want to deploy these supporting files.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">This installation type uses some of your cloud storage space.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">On the <ui>Software description</ui> page, configure the following:</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src25" class="srcSentence">Depending on the installer file you are using, some of these values might have been automatically entered, or might not appear.</caps:sentence>
                    </para>
                  </alert>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src26" class="srcSentence">Setting</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src27" class="srcSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src28" class="srcSentence">Publisher</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src29" class="srcSentence">Enter the name of the publisher of the app.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src30" class="srcSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src31" class="srcSentence">Enter the name of the app as it will be displayed in the company portal.</caps:sentence>
                          </para>
                          <alert class="tip">
                            <para>
                              <caps:sentence id="src32" class="srcSentence">Make sure all app names you use are unique.</caps:sentence>
                              <caps:sentence id="src33" class="srcSentence"> If the same app name exists twice, only one of the apps will be displayed to users in the company portal.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src34" class="srcSentence">Description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src35" class="srcSentence">Enter a description for the app.</caps:sentence>
                            <caps:sentence id="src36" class="srcSentence"> This will be displayed to users in the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src37" class="srcSentence">URL for software information</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src38" class="srcSentence">(optional) Enter a URL to a website that contains information about this app.</caps:sentence>
                            <caps:sentence id="src39" class="srcSentence"> The URL will be displayed to users in the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src40" class="srcSentence">Privacy URL</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src41" class="srcSentence">(optional) Enter a URL to a website that contains privacy information for this app.</caps:sentence>
                            <caps:sentence id="src42" class="srcSentence"> The URL will be displayed to users in the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src43" class="srcSentence">Category</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src44" class="srcSentence">(optional) Select one of the built-in app categories.</caps:sentence>
                            <caps:sentence id="src45" class="srcSentence"> This will make it easier for users to find the app when they browse the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src46" class="srcSentence">Icon</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src47" class="srcSentence">(optional) Upload an icon that will be associated with the app.</caps:sentence>
                            <caps:sentence id="src48" class="srcSentence"> This is the icon that will be displayed with the app when users browse the company portal.</caps:sentence>
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
                    <caps:sentence id="src49" class="srcSentence">On the <ui>Requirements</ui> page, select the requirements that must be met before the app can start to install on a device from:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">
                          <ui>Architecture</ui> - Select whether this app can be installed on 32-bit, 64-bit, or both operating systems.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">
                          <ui>Operating System</ui>  - Select the minimum operating system on which this app can be installed.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">For the <ui>Windows Installer</ui> file type only (exe only): On the <ui>Detection rules</ui> page, you can configure rules to detect if the app you are configuring is already installed on a PC, or  you can use the default detection rules to automatically overwrite any previously installed versions of the app.</caps:sentence>
                    <caps:sentence id="src53" class="srcSentence"> The rules you can configure are:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">
                          <ui>File exists</ui> - Specify the path to the file you want to detect.</caps:sentence>
                        <caps:sentence id="src55" class="srcSentence"> You can search under <ui>%ProgramFiles%</ui> (which searches <ui>Program Files</ui>\<placeholder>&lt;path&gt;</placeholder> and <ui>Program Files (x86)</ui>\<placeholder>&lt;path&gt;</placeholder>) on the PC or <ui>%SystemDrive%</ui> (which searches from the root drive of the PC, typically C:)</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">
                          <ui>MSI product code exists</ui> - Click <ui>Browse</ui> to choose the Windows Installer (msi) file you want to detect.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">
                          <ui>Registry key exists</ui> - Specify a registry key that begins with <ui>HKEY_LOCAL_MACHINE\</ui>.</caps:sentence>
                        <caps:sentence id="src59" class="srcSentence"> Both 32-bit and 64-bit registry paths are searched.</caps:sentence>
                        <caps:sentence id="src60" class="srcSentence"> If the key you specified exists in either location, the detection rule is satisfied.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">If the app satisfies any of the rules you have configured, it will not be installed.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">For the <ui>Windows Installer</ui> file type only (msi and exe): On the <ui>Command line arguments</ui> page, choose whether you want to supply optional command-line arguments for the installer.</caps:sentence>
                    <caps:sentence id="src63" class="srcSentence"> For example, some installers might support the argument <ui>/q</ui> to install silently with no user intervention.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">For the <ui>Windows Installer</ui> file type only (exe only): On the <ui>Return codes</ui> page, you can add new error codes that are interpreted by Intune when the app installs on a managed Windows PC.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">By default, <token>wit_nextref</token> uses industry-standard return codes to report the failure or success of an app package installation:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">
                          <ui>0</ui> - Success</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">
                          <ui>3010</ui> - Success with restart</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">You can also add your own return codes to this list.</caps:sentence>
                    <caps:sentence id="src69" class="srcSentence"> If you specify a list of return codes and the app installation returns a code that isn't on the list, it is interpreted as a failure.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">On the <ui>Summary</ui> page, review the information you specified.</caps:sentence>
                    <caps:sentence id="src71" class="srcSentence"> Once you are ready, click <ui>Upload</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">Click <ui>Close</ui> to finish.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src73" class="srcSentence">The app is displayed on the <ui>Apps</ui> node of the <ui>Apps</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Depl">
        <title>
          <caps:sentence id="src74" class="srcSentence">Deploy the app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src75" class="srcSentence">In this procedure, you'll deploy the app to selected devices or users.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src76" class="srcSentence">To deploy the app</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administrator console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Apps</ui> &gt; <ui>Apps</ui> to view the list of apps you manage.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">Select the app you want to deploy, and then click <ui>Manage Deployment</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">In the <placeholder>&lt;app name&gt;</placeholder> dialog box, first, on the <ui>Select Groups</ui> page, choose the user or device groups to which you want to deploy the app.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">On the <ui>Deployment Action</ui> page, configure the following:</caps:sentence>
                  </para>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src81" class="srcSentence">Setting</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src82" class="srcSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src83" class="srcSentence">Approval</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src84" class="srcSentence">Choose whether the deployment is:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src85" class="srcSentence">
                                  <ui>Required</ui> (mandatory install)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src86" class="srcSentence">
                                  <ui>Available</ui> (users install from the company portal on demand)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src87" class="srcSentence">
                                  <ui>Not Applicable</ui> (the app is not installed or shown in the company portal)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src88" class="srcSentence">
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
                              <caps:sentence id="src89" class="srcSentence">Deadline</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src90" class="srcSentence">For required installations, choose how soon the app will be deployed.</caps:sentence>
                            <caps:sentence id="src91" class="srcSentence"> You can choose from the predefined values, or select <ui>Custom</ui> to configure your own deadline.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Monitor">
        <title>
          <caps:sentence id="src92" class="srcSentence">Monitor the app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src93" class="srcSentence">You can see the apps you manage, and their deployment status in the <token>wit_nextref</token> console.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src94" class="srcSentence">To view the apps you manage and their status</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src95" class="srcSentence">In the <ui>Apps</ui> workspace, click the <ui>Apps</ui> node.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src96" class="srcSentence">The list of apps you manage will be displayed.</caps:sentence>
                <caps:sentence id="src97" class="srcSentence"> You can click on any app to see an installation status in the lower pane of the console windows.</caps:sentence>
                <caps:sentence id="src98" class="srcSentence"> Click on this status to see further details.</caps:sentence>
                <caps:sentence id="src99" class="srcSentence"> For example, if the status shows <ui>1 user has this software available</ui>, you can click the message to see the name of the user.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence id="src100" class="srcSentence">You can use the <ui>Filters</ui> drop-down list to show only apps that meet the criteria you specify, like apps that failed to install, or apps that were successfully deployed.</caps:sentence>
                </para>
                <para>
                  <mediaLinkInline>
                    <image xlink:href="ee926c78-12c0-4646-8ecc-f844efec9677"></image>
                  </mediaLinkInline>
                </para>
              </alert>
              <para>
                <caps:sentence id="src101" class="srcSentence">Additionally, the <ui>Dashboard</ui> workspace shows an overview of the status of your apps.</caps:sentence>
                <caps:sentence id="src102" class="srcSentence"> If you click anywhere in the overview, you'll be taken to the list of apps.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src103" class="srcSentence">To view more detailed information about an app</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src104" class="srcSentence">In the list of apps, select any app, and then click <ui>View Properties</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src105" class="srcSentence">On the <ui>Software Properties</ui> page for the app, click one of these tabs:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">
                      <ui>General</ui> - Shows general information about the app and it's installation status.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">
                      <ui>Devices</ui> - Shows the devices that successfully installed a targeted deployment of the app.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">
                      <ui>Users</ui> - Shows the users who's devices successfully installed a targeted deployment of the app.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src109" class="srcSentence">As before, you can use the <ui>Filters</ui> drop-down list to configure the values shown on each of the tabs.</caps:sentence>
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