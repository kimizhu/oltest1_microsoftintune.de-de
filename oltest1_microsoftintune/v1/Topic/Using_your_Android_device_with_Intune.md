---
description: na
keywords: na
title: Using your Android device with Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 465763db-b68d-4392-a5a4-732b5b875c2b
---
# Verwenden Ihres Android-Ger&#228;ts mit Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence sentenceid="8e84352dc3925fd78cdd7f5fef36efa7" id="tgt1" class="tgtSentence">Befolgen Sie diese Schritte für Aufgaben, die Sie auf Ihrem Android-Gerät ausführen müssen, wenn Ihr Unternehmen Microsoft Intune verwendet:</caps:sentence>
        </para>
        <table border="1">
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="54daf68978f49ad4d646edd222e602f1" id="tgt2" class="tgtSentence">Aufgabenkategorie</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e86e187e7bbea2eea4ad12ab7734221e" id="tgt3" class="tgtSentence">Aufgaben, die Sie erledigen können</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e6a2a3272b06e3df4f17efdd8970c4a3" id="tgt4" class="tgtSentence">Installation der Unternehmensportal-App und Intune-Registrierung</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_install_cp_app">Install the Microsoft Intune Company Portal app</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_signin_cp">Sign in to the Company Portal</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_enroll_devc">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f043154e08f9b3476e587eb2d7bdb007" id="tgt5" class="tgtSentence">Aufgaben, die Sie erledigen können, wenn Ihr Gerät bei Intune registriert ist</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_whatis_cp_website">What is the Company Portal website and what can I do with it?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_encrypt_your_device">Encrypt your device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_set_pin">Set your PIN or password</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_install_vpn">Install your company's Virtual Private Network (VPN)</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_unenroll_device">Unenroll your device from Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_data_collect">Turn off Microsoft usage data collection</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c6dc0f40f1debc9ce66e6c01a76742f2" id="tgt6" class="tgtSentence">Beheben von Problemen mit Ihrem Gerät </caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_fix_issues">Fix issues when your device is enrolled in Intune</link>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_verboselogging">Use Verbose Logging to help your IT admin fix issues</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_diag_logs">Send diagnostic data logs to your IT admin using email</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_diag_usbcable">Send diagnostic data logs to your IT admin using a USB cable</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>
                        </para>
                      </listItem>
                    </list>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section expanded="true" address="BKMK_andr_install_cp_app">
        <title>
          <caps:sentence sentenceid="ee6e4eec4eee8a91c4878544868a748a" id="tgt7" class="tgtSentence">Installieren der Microsoft Intune-Unternehmensportal-App</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bcc9ebff81099e0055eecc4f9b04f424" id="tgt8" class="tgtSentence">Das Unternehmensportal ist eine App, die Sie auf Ihrem Gerät installieren, damit Sie Zugriff auf Ihre Unternehmens-, Schul- oder Uni-Apps, E-Mail und das Netzwerk erhalten.</caps:sentence>
            <caps:sentence sentenceid="dda3e2c0b909ad0d8c50a1d863aa82a0" id="tgt9" class="tgtSentence">  Bevor Sie Zugriff erhalten, müssen Sie die Unternehmensportal-App installieren und dann mithilfe der App Ihr Gerät bei Microsoft Intune registrieren.</caps:sentence>
            <caps:sentence sentenceid="5d9ec8c42c2995e1314461554a305101" id="tgt10" class="tgtSentence"> Weitere Informationen dazu, was Registrierung bedeutet, finden Sie unter <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt11" class="tgtSentence">Tippen Sie auf <ui>Home</ui> &gt; <ui>Play Store</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt12" class="tgtSentence">Geben Sie im Feld <ui>Suchen</ui> den Begriff <ui>Unternehmensportal</ui> ein.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt13" class="tgtSentence">Tippen Sie auf <ui>Intune-Unternehmensportal</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="8fe9ef88-1360-4018-aa94-de83f09cb439"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt14" class="tgtSentence">Tippen Sie auf <ui>INSTALLIEREN</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="e41358ab-3546-48ca-973e-e3988f519676"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt15" class="tgtSentence">Tippen Sie auf <ui>AKZEPTIEREN</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="b9366110-0d9a-4848-8357-395933976720"></image>
              </mediaLink>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_signin_cp">
        <title>
          <caps:sentence sentenceid="9f7379f0c4fb464834165f34da1a6a7f" id="tgt16" class="tgtSentence">Anmelden beim Unternehmensportal</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2bb5411102d14c4ba5dc662521c32993" id="tgt17" class="tgtSentence">Nachdem Sie die Unternehmensportal-App installiert haben, müssen Sie sich bei der App anmelden, um Ihr Gerät bei Intune zu registrieren.</caps:sentence>
            <caps:sentence sentenceid="21c131ab9d7bb47da9c359ca3dbb1e4a" id="tgt18" class="tgtSentence"> Nach der Registrierung können Sie sich jederzeit beim Unternehmensportal anmelden, um Unternehmens-Apps herunterzuladen und andere Aufgaben auszuführen.</caps:sentence>
            <caps:sentence sentenceid="40c6475458964e1be627eb195d0a677b" id="tgt19" class="tgtSentence"> Weitere Informationen dazu, was Sie tun können, finden Sie unter <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt20" class="tgtSentence">Tippen Sie in der Liste Ihrer Apps auf <ui>Unternehmensportal</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="fd42b202-1e8d-4dec-b0d9-2bb5025a8685"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt21" class="tgtSentence">Tippen Sie im Bildschirm <ui>Willkommen</ui> auf <ui>Anmelden</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="af8ca93c727c77483a702f613d65e6cc" id="tgt22" class="tgtSentence">Geben Sie Ihre Geschäfts-, Schul- oder Uni-E-Mail-Adresse und das Kennwort ein, und tippen Sie dann auf <ui>Anmelden</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="5542d597-0ff4-4858-ba2b-eb909052c3c6"></image>
              </mediaLink>
              <para>
                <caps:sentence sentenceid="88f4e8855abbb6dcb06cd5d805fb89d4" id="tgt23" class="tgtSentence">Wenn Sie sich zum ersten Mal beim Unternehmensportal anmelden und Ihr Unternehmen oder Ihre Schule/Uni verwendet Intune, werden Sie aufgefordert, Ihr Gerät bei Intune zu registrieren.</caps:sentence>
                <caps:sentence sentenceid="5e948074b31b8a9455d72a9372e2f24d" id="tgt24" class="tgtSentence"> Führen Sie zum Registrieren die folgenden Schritte in <link xlink:href="#BKMK_andr_enroll_devc"> Enroll your device in Intune</link> aus.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_enroll_devc">
        <title>
          <caps:sentence sentenceid="d065e047890c2ebd02738f563a483d28" id="tgt25" class="tgtSentence"> Registrieren Ihres Geräts in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="92ec96c905048e2c17c94c973607a519" id="tgt26" class="tgtSentence">Wenn Sie Ihr Gerät bei Intune registrieren, können Sie auf das Netzwerk des Unternehmens zugreifen und Ihre geschäftlichen E-Mails, Arbeitsdateien und Unternehmens-Apps abrufen.</caps:sentence>
            <caps:sentence sentenceid="e0110f9a2b949d7448b9ccf2746029f1" id="tgt27" class="tgtSentence"> Weitere Informationen dazu, was Sie tun können, wenn Sie sich registrieren, finden Sie unter <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
            <caps:sentence sentenceid="ef4da4bff79fb49620cdc2eca640b8c8" id="tgt28" class="tgtSentence"> Informationen, wenn Sie Probleme beim Registrieren haben, finden Sie unter <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ceba66042f88d32b94366c1376481552" id="tgt29" class="tgtSentence">Verwenden Sie die Schritte, die dem Typ des Geräts entsprechen, das Sie besitzen, um es zu registrieren:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="#BKMK_andr_enroll_native">Enroll your native (non-Samsung device in Intune)</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_andr_enroll_knox">Enroll your Samsung Knox device in Intune</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_andr_enroll_native">
            <title>
              <caps:sentence sentenceid="20f534249b00807c2ca547e95761f998" id="tgt30" class="tgtSentence">Registrieren Ihres systemeigenen (nicht Samsung) Geräts in Intune</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="119edf7313e9135f1531299a00b51371" id="tgt31" class="tgtSentence">Tippen Sie im Unternehmensportal im Bildschirm <ui>Willkommen</ui> auf <ui>Anmelden</ui>, und melden Sie sich dann mit Ihrem Geschäfts-, Schul- oder Unikonto an.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="38af4722b5d89342a4d477c21ddb27ab" id="tgt32" class="tgtSentence">Wenn Ihr IT-Administrator die Geschäftsbedingungen des Unternehmens eingerichtet hat, tippen Sie auf <ui>AKZEPTIEREN</ui>, um sie anzunehmen.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="930b52ef-2c50-4fe8-b551-624e757781f4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt33" class="tgtSentence">Tippen Sie auf <ui>REGISTRIEREN</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="161a5f87-3d27-43bf-8b0a-8bfea06d61cf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt34" class="tgtSentence">Tippen Sie auf <ui>Aktivieren</ui></caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="71bd0ea7-259a-468c-b312-a3cf820ba956"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2b1deb508a675f2cf878e281fccf3338" id="tgt35" class="tgtSentence">Befolgen Sie die Aufforderungen zur Eingabe einer PIN oder eines Kennworts.</caps:sentence>
                    <caps:sentence sentenceid="9767dc1ea2848fa19a8e292a3bb6362c" id="tgt36" class="tgtSentence"> Wenn Sie bereits eine PIN oder ein Kennwort auf diesem Gerät eingerichtet haben, wird dieser Bildschirm nicht angezeigt, und Sie werden nicht zur Eingabe einer neuen PIN oder eines neuen Kennworts aufgefordert.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="3167bf58-b9f3-4260-9ffd-4ca22f633ec4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="38c28950a6f94d6d3f4e8733ad9bccff" id="tgt37" class="tgtSentence">Tippen Sie im Bildschirm <ui>Zertifikat benennen</ui> auf <ui>OK</ui>, um das Standardzertifikat zu akzeptieren.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="e9c96498-e528-4694-bdcc-80ebc7cbd9e4"></image>
                  </mediaLink>
                  <para>
                    <caps:sentence sentenceid="8168930ae7ae8157d6f688dc187f9f6a" id="tgt38" class="tgtSentence">Ihr Gerät ist jetzt bei Intune registriert.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="f849a26d081e296a39efd57b2eff545a" id="tgt39" class="tgtSentence">Informationen, wenn Sie einen Fehler während der Registrierung Ihres Geräts bei erhalten, finden Sie unter <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_andr_enroll_knox">
            <title>
              <caps:sentence sentenceid="bf108b7344f13ecf0abde91c6b70411d" id="tgt40" class="tgtSentence">Registrieren Ihres Samsung Knox-Geräts bei Intune</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b3feb8aaf4b8cee01e15dad758697df0" id="tgt41" class="tgtSentence">Tippen Sie im Unternehmensportal im Begrüßungsbildschirm auf „Anmelden“, und melden Sie sich dann mit Ihrem Geschäfts-, Schul- oder Unikonto an.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="38af4722b5d89342a4d477c21ddb27ab" id="tgt42" class="tgtSentence">Wenn Ihr IT-Administrator die Geschäftsbedingungen des Unternehmens eingerichtet hat, tippen Sie auf <ui>AKZEPTIEREN</ui>, um sie anzunehmen.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="930b52ef-2c50-4fe8-b551-624e757781f4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt43" class="tgtSentence">Tippen Sie auf <ui>REGISTRIEREN</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="161a5f87-3d27-43bf-8b0a-8bfea06d61cf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt44" class="tgtSentence">Tippen Sie auf <ui>AKTIVIEREN</ui></caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="c68d1754-e1a7-4906-a3dc-f13673f7c8d3"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3221064bbc2e7c9caf89313a3d70ccdc" id="tgt45" class="tgtSentence">Akzeptieren Sie die Samsung Knox-Datenschutzrichtlinie, und tippen Sie auf <ui>Bestätigen</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="595681eb-d7f3-47a8-a95d-a427d903a241"></image>
                  </mediaLink>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="8168930ae7ae8157d6f688dc187f9f6a" id="tgt46" class="tgtSentence">Ihr Gerät ist jetzt bei Intune registriert.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_andr_what_happs_add">
        <title>
          <caps:sentence sentenceid="c7771a0e09cd91e94fb6776ff1223ac3" id="tgt47" class="tgtSentence">Was geschieht, wenn ich die Unternehmensportal-App installiere und mein Gerät bei Intune registriere?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f0401535f7b1ac877b8f6af14bd6c40d" id="tgt48" class="tgtSentence">Sie beginnen damit, dass Sie die Unternehmensportal-App installieren und dann Ihr Gerät mithilfe der App bei Intune registrieren.</caps:sentence>
            <caps:sentence sentenceid="9af3ed7432137e078ac63133e9bdc49a" id="tgt49" class="tgtSentence"> Sobald Ihr Gerät registriert ist, können Sie die Unternehmensportal-App für folgende Aufgaben verwenden:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="cd1a40a617eb283f621ef494fdaa498f" id="tgt50" class="tgtSentence">Zugreifen auf das Netzwerk des Unternehmens und auf E-Mail- sowie andere arbeitsbezogene Dateien</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="365f2777fae357fc28b1489affab4a54" id="tgt51" class="tgtSentence">Abrufen von Unternehmens-Apps aus dem Unternehmensportal</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7c7476a0520e0468f40a091eecb0d594" id="tgt52" class="tgtSentence">Automatisches Konfigurieren Ihres geschäftlichen E-Mail-Kontos</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="66b07c74bf99f92822a9939daafde7d3" id="tgt53" class="tgtSentence">Zurücksetzen Ihres Smartphones auf die werkseitigen Standardeinstellungen bei Verlust oder Diebstahl</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="9580373c6a8f78a774ff06c526b5e360" id="tgt54" class="tgtSentence">Wenn Sie Ihr Gerät bei Intune registrieren, gestatten Sie damit Ihrem IT-Administrator, Ihr Gerät zu verwalten, damit die Unternehmensinformationen auf dem Gerät geschützt werden.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49b5c06f816b80fa0b53001b7e064dd0" id="tgt55" class="tgtSentence">Nicht für die IT einsehbar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="919967a6e68fc799764ccfadd49d0d82" id="tgt56" class="tgtSentence">Für die IT einsehbar</caps:sentence>
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
                        <caps:sentence sentenceid="7b15a2dc20f223897228983bcb839a0d" id="tgt57" class="tgtSentence">Anrufliste</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b5c1e4334dd619fce44e7a047bd05a8d" id="tgt58" class="tgtSentence">SMS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="936249fa98a3357097ff1f12312225b4" id="tgt59" class="tgtSentence">Persönliche E-Mail, Kontakte und Kalender</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="827a82394f446cc4d02c0fd5e61f331b" id="tgt60" class="tgtSentence">Webverlauf</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d5189de027922f81005951e6efe0efd5" id="tgt61" class="tgtSentence">Speicherort</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b99bbccd22c782c7f7019bad4a0628f2" id="tgt62" class="tgtSentence">Eigene Aufnahmen</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2c5a2582707f1495992f8b6befe92a6c" id="tgt63" class="tgtSentence">Personenbezogene Daten</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="72122ce96bfec66e2396d2e25225d70a" id="tgt64" class="tgtSentence">Besitzer</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="712778275c556c187fb77a2b8a2af8c4" id="tgt65" class="tgtSentence">Gerätename</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c9f4029ce9dcf8ff7f8f1b70edead843" id="tgt66" class="tgtSentence">Seriennummer</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c2904bca62b22443d6cf5e9d89cab204" id="tgt67" class="tgtSentence">Hersteller</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="20f35e630daf44dbfa4c3f68f5399d8c" id="tgt68" class="tgtSentence">Modell</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d83f147fd8043b67aa813f44f597b39b" id="tgt69" class="tgtSentence">Betriebssystem</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="93a4cf66e1c393e83e3c39b8446f1b71" id="tgt70" class="tgtSentence">Unternehmens-Apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a2da362c93e6fb8f4d57947fe2b2d8fd" id="tgt71" class="tgtSentence">Persönliche Apps</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="7a9bb338270201243cf6be9e712925f2" id="tgt72" class="tgtSentence">Wenn Sie Ihr Android-Gerät hinzufügen, gewähren Sie Ihrem IT-Administrator eine Zugriffsberechtigung für das Gerät.</caps:sentence>
            <caps:sentence sentenceid="c1c2c0f76e506e4c114e45f70033641c" id="tgt73" class="tgtSentence"> IT-Administratoren können folgende Dinge tun:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="2833d6f47e693959641866661f074157" id="tgt74" class="tgtSentence">Zurücksetzen des Geräts auf die standardmäßigen Werkseinstellungen.</caps:sentence>
                <caps:sentence sentenceid="ec2b174c8222d31c80eac2abd68f4f60" id="tgt75" class="tgtSentence"> Dies ist hilfreich, wenn das Gerät verloren geht oder gestohlen wird.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="bbad2fb68e3185a447cf6d63dfb15354" id="tgt76" class="tgtSentence">Entfernen aller unternehmensrelevanten Daten.</caps:sentence>
                <caps:sentence sentenceid="bebc79fbe14286bcca2d83d606469094" id="tgt77" class="tgtSentence"> Ihre persönlichen Daten und Einstellungen werden nicht entfernt.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9ce5937038a7840eaa9bbba565e419a8" id="tgt78" class="tgtSentence">Erzwingen eines Kennworts oder einer PIN für das Gerät. Dies kann bei zu vielen falschen Versuchen bei der Kennworteingabe zu einer Sperrung des Geräts oder dazu führen, dass das Gerät auf die werkseitigen Standardeinstellungen zurückgesetzt wird. Dabei können auch Daten gelöscht werden.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1aa6cfa75e3c98c83374293c4279f76" id="tgt79" class="tgtSentence">Sie müssen die Bedingungen akzeptieren.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f9877cfa9f701abb70b52dc01c3d35e7" id="tgt80" class="tgtSentence">Aktivieren oder Deaktivieren der Kamera auf dem Gerät.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f588fae704de8edfd6f8cdc33793d3f0" id="tgt81" class="tgtSentence">Erzwingen, dass alle Daten, inklusive aller persönlichen und Unternehmensdaten, auf dem Gerät verschlüsselt werden.</caps:sentence>
                <caps:sentence sentenceid="069e34665f9e53073d27ad97b440e0ce" id="tgt82" class="tgtSentence"> Dadurch werden die Daten geschützt, wenn das Gerät verloren geht oder gestohlen wird.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4370aca60d1ad253c0dc1c64f9b54f90" id="tgt83" class="tgtSentence">Nachdem das Gerät zum Unternehmensportal hinzugefügt wurde, erfolgt im Intervall von ca. acht Stunden Folgendes:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5ba4cc4bde2dd286214e46b9c9155365" id="tgt84" class="tgtSentence">Herunterladen aller Richtlinien- oder App-Updates, die Ihr IT-Administrator zur Verfügung gestellt hat.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e135d12cb140527861d03d871f7d01ec" id="tgt85" class="tgtSentence">Senden aller Hardwareinventur-Updates (diese Updates enthalten keine persönlichen Informationen).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ea917e0cc0b6f20af749331177b9f8e0" id="tgt86" class="tgtSentence">Senden aller Unternehmens-App-Inventaraktualisierungen (diese Updates enthalten keine persönlichen Informationen).</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_whatis_cp_website">
        <title>
          <caps:sentence sentenceid="631be7185536cbfc0dd9092b681d30e8" id="tgt87" class="tgtSentence">Was ist die Unternehmensportal-Website, und was kann ich darin tun?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt88" class="tgtSentence">Die <externalLink><linkText>Unternehmensportal-Website</linkText><linkUri>http://portal.manage.microsoft.com</linkUri></externalLink> ist die Weboberfläche Ihres Unternehmens, über die Sie Ihre Arbeitscomputer und -geräte sowie Ihre persönlichen Computer und Geräte verwalten, die Sie für die Arbeit verwenden.</caps:sentence>
            <caps:sentence sentenceid="70037d25cd497b5572e18d1bc35334bc" id="tgt89" class="tgtSentence"> Die meisten Aufgaben, die Sie mithilfe der Unternehmensportal-App ausführen können, die Sie auf Ihrem Gerät installieren, können Sie auch auf der Unternehmensportal-Website ausführen.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="14d658610fe447e446e50ce288d1edc1" id="tgt90" class="tgtSentence">Folgende Aufgaben können Sie auf der Unternehmensportal-Website ausführen:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3dc0b17542da2ec9d90ff0965d19aef1" id="tgt91" class="tgtSentence">Durchsuchen nach und Herunterladen von Unternehmens-Apps</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f82609801e7080daebaa60a46cd06e57" id="tgt92" class="tgtSentence">Umbenennen Ihres Geräts</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2e254e163be6b2905cf22931f4eb4fe0" id="tgt93" class="tgtSentence">Entfernen Ihres Geräts aus Intune</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="680b802dd6afc46294bf85411f86cccf" id="tgt94" class="tgtSentence">Zurücksetzen Ihres mobilen Geräts auf die werkseitigen Standardeinstellungen</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed64c84b76d070c3000586dc8cade916" id="tgt95" class="tgtSentence">Suchen von Kontaktinformationen für Ihren IT-Administrator</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_andr_encrypt_your_device" expanded="true">
        <title>
          <caps:sentence sentenceid="71589dcc021fa7128be6ce02c4bae40c" id="tgt96" class="tgtSentence">Registrieren Ihres Geräts</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8b4bb28ccfe25f26b5b51ac2d7425762" id="tgt97" class="tgtSentence">Wenn Ihr Unternehmen oder Ihre Organisation eine Verschlüsselung Ihres Geräts erfordern, bevor Sie auf Unternehmensdateien, E-Mails oder Daten zugreifen können, befolgen Sie diese Schritte zum Verschlüsseln des Geräts:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="af593d936fba1e3defe54881968496c1" id="tgt98" class="tgtSentence">Stellen Sie sicher, dass Ihr Gerät mit dem Ladegerät verbunden ist.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt99" class="tgtSentence">Tippen Sie auf <ui>Suchen</ui>.</caps:sentence>
                <caps:sentence sentenceid="eef65366d19ec7fa1427057a45c472e7" id="tgt100" class="tgtSentence"> Geben Sie im Feld „Suchen“ den Begriff <ui>Unternehmensportal</ui> ein.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="180a0ae508e82e1fe2f0e7ec1957f07a" id="tgt101" class="tgtSentence">Stellen Sie sicher, dass eine Bildschirmsperren-PIN oder ein Kennwort für das Gerät festgelegt wurde.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c7ea902a3b53e77ab15b83a98de09a95" id="tgt102" class="tgtSentence">Klicken Sie unter „Einstellungen“ auf <ui>Sicherheit</ui> &gt; <ui>Telefon verschlüsseln</ui>.</caps:sentence>
                <caps:sentence sentenceid="e7cd1083a7d14f29c57cfc3f14ea7f3f" id="tgt103" class="tgtSentence"> (Bei einigen Telefonen müssen Sie auf <ui>Speicher</ui> &gt; <ui>Speicherverschlüsselung</ui> klicken).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="48e7a77ebbc375b27095d1424e9ca739" id="tgt104" class="tgtSentence">Folgen Sie den Anweisungen auf dem Bildschirm.</caps:sentence>
                <caps:sentence sentenceid="04fb0e693021f54d4d76c5c98ffd6665" id="tgt105" class="tgtSentence"> Während der Verschlüsselung startet Ihr Gerät möglicherweise mehrmals neu.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="acc3afeae12c8210f39b9c2e3370e615" id="tgt106" class="tgtSentence">Stellen Sie sicher, dass Ihr Gerät mit Microsoft Intune registriert wird, indem Sie die Anweisungen unter <link xlink:href="8373c587-b1ad-4c25-93f9-e0148834d495">Enroll your device in Microsoft Intune</link> befolgen.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <maml:section expanded="true" address="BKMK_andr_set_pin" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="58883bbb934c33d6c14e423ec7876f01" id="tgt107" class="tgtSentence">Festlegen von PIN oder Kennwort</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="298eb8b721760a1ff208e241dcde7e9b" id="tgt108" class="tgtSentence">Tippen Sie auf <maml:ui>Einstellungen</maml:ui> &gt; <maml:ui>Sicherheit</maml:ui> &gt; <maml:ui>Bildschirmsperre</maml:ui> &gt; <maml:ui>Kennwort</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="efcddfbbc5839ce3888c191bec4cde8a" id="tgt109" class="tgtSentence">Wählen und bestätigen Sie das neue Kennwort.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="acc3afeae12c8210f39b9c2e3370e615" id="tgt110" class="tgtSentence">Stellen Sie sicher, dass Ihr Gerät in Microsoft Intune registriert wird, indem Sie die Anweisungen unter <maml:link xlink:href="#BKMK_andr_enroll_devc">Registrieren Ihres Geräts in Intune</maml:link> befolgen.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt111" class="tgtSentence">Tippen Sie auf <maml:ui>ABRUFEN</maml:ui> &gt; <maml:ui>INSTALLIEREN</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_install_vpn" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="177fce649a24942d01315bd8da5e7076" id="tgt112" class="tgtSentence">Installieren Sie das virtuelles private Netzwerk (Virtual Private Network, VPN) Ihres Unternehmens.</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="e8fa9ec145e597718eb06082fa820b16" id="tgt113" class="tgtSentence">Wenn Ihr IT-Administrator eine VPN-App zum Herstellen einer Verbindung mit den Unternehmensressourcen konfiguriert hat, sehen Sie eine Benachrichtigung auf Ihrem Gerät, dass Sie eine VPN-App installieren müssen.</caps:sentence>
            <caps:sentence sentenceid="f9de42cfde03ef98dfc2d6f0a240a551" id="tgt114" class="tgtSentence"> Führen Sie zum Installieren der VPN-App die folgenden Schritte aus:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="f68d8e82a2420b63954d9064aaafbf84" id="tgt115" class="tgtSentence">Öffnen Sie die Benachrichtigung, und tippen Sie auf <maml:ui>Tippen Sie, um diese erforderliche App zu installieren</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt116" class="tgtSentence">Tippen Sie im <maml:ui>Play Store</maml:ui> auf <maml:ui>INSTALLIEREN</maml:ui>, und befolgen Sie die Anweisungen, um die App zu installieren</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt117" class="tgtSentence">Tippen Sie auf <maml:ui>VPN-Unternehmensprofil installieren</maml:ui>, und befolgen Sie die Anweisungen, um die App zu akzeptieren und zu aktivieren.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_unenroll_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="e7334a6647a4beaf7b7148ac205d9349" id="tgt118" class="tgtSentence">Aufheben der Registrierung Ihres Geräts in Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="a0c8593b0b5f285d2c025132d17200c6" id="tgt119" class="tgtSentence">Wenn Sie die Registrierung Ihres Geräts in Intune aufheben, kann Ihr Gerät nicht mehr auf Unternehmensressourcen zugreifen und wird nicht mehr über Intune verwaltet.</caps:sentence>
          </maml:para>
          <maml:para>
            <caps:sentence sentenceid="33ec116fa4d3a05cebd927de0897af22" id="tgt120" class="tgtSentence">So heben Sie die Registrierung Ihres Geräts bei Intune auf</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="5de362ca355ae82e403db3be928ad9fa" id="tgt121" class="tgtSentence">Drücken Sie auf <maml:ui>MEINE GERÄTE</maml:ui>, und wählen Sie das Gerät aus, dessen Registrierung Sie aufheben möchten.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="5de362ca355ae82e403db3be928ad9fa" id="tgt122" class="tgtSentence">Drücken Sie auf <maml:ui>Entfernen</maml:ui> &gt; <maml:ui>OK</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
          <maml:para>
            <caps:sentence sentenceid="715a45f185a63212c320c5ddbe6feb5f" id="tgt123" class="tgtSentence">Wenn Sie die Registrierung Ihres Geräts bei Intune aufheben passiert Folgendes:</caps:sentence>
          </maml:para>
          <maml:list class="bullet">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="19ae91384fd35970ba35834af61f01ac" id="tgt124" class="tgtSentence">Das Gerät wird nicht mehr im Unternehmensportal angezeigt.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="debcc4cc4b3dff0ce773acfc3cba2baa" id="tgt125" class="tgtSentence">Sie können keine Apps mehr über das Unternehmensportal installieren.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="1e73478ca20c90722c6b651b4f099ce6" id="tgt126" class="tgtSentence">Alle Einstellungen, die beim Hinzufügen des Geräts auf diesem geändert wurden, z. B. das Deaktivieren der Kamera oder die Anforderung einer bestimmten Kennwortlänge, werden unwirksam.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="e2e05eddbfd9df781fb51550906d96c8" id="tgt127" class="tgtSentence">Unter Umständen haben Sie auf dem Gerät keinen Zugriff mehr auf einige Unternehmensressourcen, z. B. Dateifreigaben oder interne Websites.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="a1e7c55d94cbaa4a92d89ae197836b91" id="tgt128" class="tgtSentence">Geräte, die nur für E-Mail konfiguriert sind, werden nicht mehr in der Unternehmensportal-App oder auf der Unternehmensportal-Website angezeigt.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_erase_lost_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="c06b6d82e53b630aa8f19483e6047696" id="tgt129" class="tgtSentence">Zurücksetzen (Löschen) Ihres verlorenen oder gestohlenen Geräts</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="25c5afd9a776dc51030b16195ab0a2bd" id="tgt130" class="tgtSentence">Wenn Ihr Smartphone verloren geht oder gestohlen wird, können Sie es auf die werkseitigen Standardeinstellungen zurücksetzen.</caps:sentence>
          </maml:para>
          <maml:alert class="warning">
            <maml:para>
              <caps:sentence sentenceid="cc052fb10fe9bbbc80b2b6df67c21fb9" id="tgt131" class="tgtSentence">Durch das Zurücksetzen eines Geräts auf die werkseitigen Standardeinstellungen werden Ihre darauf befindlichen persönlichen und beruflichen Informationen gelöscht.</caps:sentence>
            </maml:para>
          </maml:alert>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="008ffbf3521115514e18b2a62951487c" id="tgt132" class="tgtSentence">Öffnen Sie die Adresse <maml:ui>portal.manage.microsoft.com</maml:ui> im Browser, und melden Sie sich bei Ihrem Geschäftskonto an.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt133" class="tgtSentence">Tippen Sie auf <maml:ui>Meine Geräte</maml:ui>, und wählen Sie dann den Namen des verlorenen oder gestohlenen Geräts aus.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt134" class="tgtSentence">Klicken Sie auf <maml:ui>Zurücksetzen</maml:ui> &gt; <maml:ui>Zurücksetzen</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:alert class="note">
                <maml:para>
                  <caps:sentence sentenceid="a3544f235a5bb1907e3b26a3816dd4fa" id="tgt135" class="tgtSentence">Wenn Sie Ihr verlorenes oder gestohlenes Gerät nicht zurücksetzen können, bitten Sie Ihren IT-Administrator, es zurückzusetzen.</caps:sentence>
                </maml:para>
              </maml:alert>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section address="BKMK_andr_data_collect" expanded="true">
        <title>
          <caps:sentence sentenceid="b321241f2502b5448f5ba9814524413f" id="tgt136" class="tgtSentence">Deaktivieren der Erfassung von Nutzungsdaten durch Microsoft</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="613c5729b5d70fe8a98c7d50505d4ea7" id="tgt137" class="tgtSentence">Um Produkte und Dienstleistungen zu verbessern, erfasst Microsoft automatisch anonyme Daten über die Zuverlässigkeit und Leistung der Unternehmensportal-App sowie deren Verwendung.</caps:sentence>
            <caps:sentence sentenceid="4150fed1487d3933fae6b75759c4e79e" id="tgt138" class="tgtSentence"> Sie können die Sammlung von Daten mithilfe der Einstellung „Verwendungsdaten“ in der Unternehmensportal-App deaktivieren.</caps:sentence>
            <caps:sentence sentenceid="e1193143312e8b74386d45adac2e9d42" id="tgt139" class="tgtSentence"> IT-Administratoren haben keine Kontrolle über die Erfassung der Daten und können Ihre Auswahl für diese Einstellung nicht ändern.</caps:sentence>
          </para>
        </content>
      </section>
      <maml:section address="BKMK_andr_fix_issues" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="b04d8428c19a919568ee64f356b58ed8" id="tgt140" class="tgtSentence">Beheben von Problemen, wenn Ihr Gerät bei Intune registriert ist</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="cda60aa64bc8e2eab24da8e35e678353" id="tgt141" class="tgtSentence">Verwenden Sie diese Informationen, um Ihrem IT-Administrator bei der Behebung von Problemen zu helfen, die Sie mit Ihrem Gerät haben, wenn Sie die Unternehmensportal-App installiert und Ihr Gerät bei Intune registriert haben.</caps:sentence>
          </maml:para>
        </maml:content>
        <maml:sections>
          <maml:section address="BKMK_andr_verboselogging">
            <maml:title>
              <caps:sentence sentenceid="464b5f790e098fbd41066848f397707c" id="tgt142" class="tgtSentence">Verwenden der ausführlichen Protokollierung zur Unterstützung Ihres IT-Administrators bei der Behebung von Problemen</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence sentenceid="6a27f3853a4e797560d0da86d27bf5fa" id="tgt143" class="tgtSentence">Wenn Ihr Gerät bei Intune registriert ist, können Sie die Einstellung <maml:ui>Ausführliche Protokollierung</maml:ui> verwenden, damit die Unternehmensportal-App und von Intune verwaltete Apps detaillierte Protokolle zu den Vorgängen auf Ihrem Gerät aufzeichnen.</caps:sentence>
                <caps:sentence sentenceid="4647d16a1b693bb166f4677550e42a45" id="tgt144" class="tgtSentence"> Diese Protokolle helfen Ihrem IT-Administrator dabei, Probleme zu beheben, die Sie möglicherweise bei der Verwendung der Unternehmensportal-App oder einer von Intune verwalteten App haben.</caps:sentence>
                <caps:sentence sentenceid="b49b4b5888845bac5e9e9838c5f40a4d" id="tgt145" class="tgtSentence"> Die ausführlicher Protokollierung ist standardmäßig auf Ihrem Gerät aktiviert, und die Protokolle, die an Ihren IT-Administrator gesendet werden, enthalten Ihre E-Mail-Adresse.</caps:sentence>
              </maml:para>
              <maml:para>
                <caps:sentence sentenceid="ace4ed7045b3e834cc1dc2e72b40a0ed" id="tgt146" class="tgtSentence">Um die <maml:ui>Ausführliche Protokollierung</maml:ui> zu aktivieren oder zu deaktivieren, melden Sie sich mit Ihren Geschäfts-, Schul- oder Unianmeldeinformationen bei der Unternehmensportal-App an, tippen Sie auf <maml:ui>Einstellungen</maml:ui>, und tippen Sie neben der Einstellung <maml:ui>Ausführliche Protokollierung</maml:ui> auf die Ein/Aus-Schaltfläche.</caps:sentence>
              </maml:para>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_diag_logs">
            <maml:title>
              <caps:sentence sentenceid="54826dafaa3f8f1bcd109fceb9fdb49a" id="tgt147" class="tgtSentence">Senden von Diagnosedatenprotokollen an Ihren IT-Administrator per E-Mail</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence sentenceid="d6c6972b05cefc1d628b323a67467022" id="tgt148" class="tgtSentence">Wenn Sie eine Fehlermeldung erhalten, während Sie mit Ihren Geschäfts-, Schul- oder Uni-Apps arbeiten und sich in der Unternehmensportal-App befinden, können Sie Diagnosedatenprotokolle senden, um Ihrem IT-Administrator bei der Diagnose und Behebung des Fehlers zu helfen.</caps:sentence>
                <caps:sentence sentenceid="c5dff4ba01265efbc6a07c1ca6060c69" id="tgt149" class="tgtSentence"> Damit alle Details in die Protokolle aufgenommen werden, die Ihrem IT-Administrator die Diagnose des Problems erleichtern, aktivieren Sie die „Ausführliche Protokollierung“.</caps:sentence>
              </maml:para>
              <maml:list class="ordered">
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="d51b26a46aaf963c828838082daa0faa" id="tgt150" class="tgtSentence">Öffnen Sie die Unternehmensportal-App.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt151" class="tgtSentence">Tippen Sie auf <maml:ui>Menü</maml:ui> &gt;  <maml:ui>Einstellungen</maml:ui>.</caps:sentence>
                  </maml:para>
                  <maml:alert class="note">
                    <maml:para>
                      <caps:sentence sentenceid="ff7845375bcca9661b95db848e63d64b" id="tgt152" class="tgtSentence">Je nach Typ des Android-Geräts, das Sie haben, kann <maml:ui>Menü</maml:ui> eine Schaltfläche in der Software oder Taste auf dem Gerät sein.</caps:sentence>
                    </maml:para>
                  </maml:alert>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt153" class="tgtSentence">Tippen Sie unter <maml:ui>Diagnosedaten</maml:ui> auf <maml:ui>Daten senden</maml:ui>.</caps:sentence>
                  </maml:para>
                  <maml:mediaLink>
                    <maml:image xlink:href="e689c712-0ce0-461a-bfb2-5dd59e218a7b"></maml:image>
                  </maml:mediaLink>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="bcebd066e10c9a2776e02c0707ed028c" id="tgt154" class="tgtSentence">Befolgen Sie die Aufforderungen zum Auswählen einer E-Mail-App zum Senden der Protokolle an Ihren IT-Administrator.</caps:sentence>
                    <caps:sentence sentenceid="4746d31faa1b7d55b9d215cc55980dc2" id="tgt155" class="tgtSentence"> Die App erstellt eine voradressierte E-Mail, an die alle Protokolle angefügt sind.</caps:sentence>
                  </maml:para>
                </maml:listItem>
              </maml:list>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_diag_usbcable">
            <maml:title>
              <caps:sentence sentenceid="f7c802cd495ec0ef87d2f01dea55d8e0" id="tgt156" class="tgtSentence">Senden von Diagnosedatenprotokollen an Ihren IT-Administrator über ein USB-Kabel</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence sentenceid="15a2927c1f5b3ed84882b1390f2e9016" id="tgt157" class="tgtSentence">Wenn Sie statt eines mobilen Geräts einen Computer verwenden und Datenprotokolle senden möchten, um Ihren IT-Administrator bei der Diagnose und Behebung des Problems zu unterstützen, gehen Sie folgendermaßen vor:</caps:sentence>
              </maml:para>
              <maml:list class="ordered">
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="503fe34670bdd8a830553f6780b668a8" id="tgt158" class="tgtSentence">Bevor Sie beginnen, stellen Sie sicher, dass Sie über die E-Mail-Adresse Ihres IT-Administrators verfügen.</caps:sentence>
                    <caps:sentence sentenceid="7980b0aa7e39ce184a2838074875cc7f" id="tgt159" class="tgtSentence"> Sie wird in der Regel auf Ihrer Unternehmensportal-Website oder in Ihrer Unternehmensportal-App aufgeführt.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="a35b101a804e644f4fd0393ed4bde8a2" id="tgt160" class="tgtSentence">Verbinden Sie Ihr Gerät mit einem USB-Kabel mit einem Computer.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="82b709c93ab8287b560b7395b7b0df72" id="tgt161" class="tgtSentence">Suchen Sie auf dem Computer nach einem Verzeichnis mit dem Namen Ihres Mobilgeräts.</caps:sentence>
                    <caps:sentence sentenceid="00cbf78559c6c72f2e70bcf6206d1cd1" id="tgt162" class="tgtSentence"> Suchen Sie in diesem Verzeichnis nach „&lt;Android-Gerät&gt;\Phone\Android\data\com.microsoft.windowsintune.companyportal\files\“.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="346ebdc57873b0b6cd9ee65dde880284" id="tgt163" class="tgtSentence">Fügen Sie alle Dateien an eine E-Mail-Nachricht an, und senden Sie diese an Ihren IT-Administrator.</caps:sentence>
                  </maml:para>
                </maml:listItem>
              </maml:list>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_enroll_errors">
            <maml:title>
              <caps:sentence sentenceid="891b8efb4cd4d53df92b65ab29dd0c0f" id="tgt164" class="tgtSentence">Senden von Registrierungsfehlern an Ihren IT-Administrator</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence sentenceid="8c7be865ad1e18ec222f54b2568b702a" id="tgt165" class="tgtSentence">Wenn Sie beim Versuch, Ihr Gerät bei Intune zu registrieren, eine Fehlermeldung erhalten, können Sie versuchen, die Registrierung zu wiederholen, indem Sie auf <maml:ui>Wiederholen</maml:ui> tippen, oder die Fehlerinformationen in einer E-Mail an Ihren IT-Administrator senden, indem Sie auf <maml:ui>Informationen senden</maml:ui> tippen.</caps:sentence>
                <caps:sentence sentenceid="415afde21455ff4dcd18fe07a31c4ace" id="tgt166" class="tgtSentence"> Es wird automatisch eine an den IT-Administrator adressierte E-Mail erstellt, die die Protokolle enthält, die von Ihrem IT-Administrator für die Problembehandlung Ihres Geräts benötigt werden.</caps:sentence>
              </maml:para>
            </maml:content>
          </maml:section>
        </maml:sections>
      </maml:section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use these  steps for tasks that you need to do on your Android device when your company is using Microsoft Intune:</caps:sentence>
        </para>
        <table border="1">
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src2" class="srcSentence">Task category</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Tasks you can do</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Company Portal app installation and Intune enrollment</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_install_cp_app">Install the Microsoft Intune Company Portal app</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_signin_cp">Sign in to the Company Portal</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_enroll_devc">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Things you can do when your device is enrolled in Intune</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_whatis_cp_website">What is the Company Portal website and what can I do with it?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_encrypt_your_device">Encrypt your device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_set_pin">Set your PIN or password</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_install_vpn">Install your company's Virtual Private Network (VPN)</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_unenroll_device">Unenroll your device from Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_data_collect">Turn off Microsoft usage data collection</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Fix issues with your device </caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_fix_issues">Fix issues when your device is enrolled in Intune</link>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_verboselogging">Use Verbose Logging to help your IT admin fix issues</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_diag_logs">Send diagnostic data logs to your IT admin using email</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_diag_usbcable">Send diagnostic data logs to your IT admin using a USB cable</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>
                        </para>
                      </listItem>
                    </list>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section expanded="true" address="BKMK_andr_install_cp_app">
        <title>
          <caps:sentence id="src7" class="srcSentence">Install the Microsoft Intune Company Portal app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">The Company Portal is an app that you install on your device to give you access to your company or school apps, email, and network.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence">  Before you can get access, you have to install the Company Portal app, and then  use the app to enroll your device in Microsoft Intune.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> To find out more about what enrolling means, see <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Tap <ui>Home</ui> &gt; <ui>Play Store</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">In the <ui>Search</ui> box, type <ui>company portal</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Tap <ui>Intune Company Portal</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="8fe9ef88-1360-4018-aa94-de83f09cb439"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">Tap <ui>INSTALL</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="e41358ab-3546-48ca-973e-e3988f519676"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">Tap <ui>ACCEPT</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="b9366110-0d9a-4848-8357-395933976720"></image>
              </mediaLink>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_signin_cp">
        <title>
          <caps:sentence id="src16" class="srcSentence">Sign in to the Company Portal</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">After you install the Company Portal app, you'll need to sign in to the app to enroll your device in Intune.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Once you enroll, you can  sign in to the Company Portal anytime to download company apps and do other tasks.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> For more about what you can do, see <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src20" class="srcSentence">Tap <ui>Company Portal</ui> in your list of apps.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="fd42b202-1e8d-4dec-b0d9-2bb5025a8685"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src21" class="srcSentence">On the <ui>Welcome</ui> screen, tap <ui>Sign in</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">Enter your work or school email and your password, and then Tap <ui>Sign in</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="5542d597-0ff4-4858-ba2b-eb909052c3c6"></image>
              </mediaLink>
              <para>
                <caps:sentence id="src23" class="srcSentence">If you are signing into the Company Portal for the first time, and your company or school is using Intune, you will be prompted to enroll your device in Intune.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> To enroll, follow the steps in <link xlink:href="#BKMK_andr_enroll_devc"> Enroll your device in Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_enroll_devc">
        <title>
          <caps:sentence id="src25" class="srcSentence"> Enroll your device in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src26" class="srcSentence">When you enroll your device in Intune, you can access the company’s network, and get your work email,  work files, and company apps.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> To find out more about what you can do when you enroll, see <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> If you have issues while trying to enroll, see <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">To enroll, use the steps that match the type of device you have:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="#BKMK_andr_enroll_native">Enroll your native (non-Samsung device in Intune)</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_andr_enroll_knox">Enroll your Samsung Knox device in Intune</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_andr_enroll_native">
            <title>
              <caps:sentence id="src30" class="srcSentence">Enroll your native (non-Samsung device in Intune)</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">On the Company Portal <ui>Welcome</ui> screen, tap <ui>Sign in</ui>, and then sign in with your work or school account..</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">If your IT admin set up company terms and conditions, tap <ui>ACCEPT</ui> to accept the terms.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="930b52ef-2c50-4fe8-b551-624e757781f4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Tap <ui>ENROLL</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="161a5f87-3d27-43bf-8b0a-8bfea06d61cf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Tap <ui>Activate</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="71bd0ea7-259a-468c-b312-a3cf820ba956"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Follow the prompts to enter a PIN or password.</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> If you already set up a PIN or password on this device, you won't see this screen or be required to enter a new PIN or password.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="3167bf58-b9f3-4260-9ffd-4ca22f633ec4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">On the  <ui>Name the certificate</ui> screen, tap <ui>OK</ui> to accept the default certificate.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="e9c96498-e528-4694-bdcc-80ebc7cbd9e4"></image>
                  </mediaLink>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Your device is now enrolled in Intune.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src39" class="srcSentence">If you get an error while trying to enroll your device in Intune, see <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_andr_enroll_knox">
            <title>
              <caps:sentence id="src40" class="srcSentence">Enroll your Samsung Knox device in Intune</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">On the Company Portal Welcome screen, tap Sign in, and then sign in with your work or school account.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">If your IT admin set up company terms and conditions, tap <ui>ACCEPT</ui> to accept the terms.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="930b52ef-2c50-4fe8-b551-624e757781f4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Tap <ui>ENROLL</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="161a5f87-3d27-43bf-8b0a-8bfea06d61cf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Tap <ui>ACTIVATE</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="c68d1754-e1a7-4906-a3dc-f13673f7c8d3"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Accept the Samsung Knox Privacy Policy and tap <ui>Confirm</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="595681eb-d7f3-47a8-a95d-a427d903a241"></image>
                  </mediaLink>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src46" class="srcSentence">Your device is now enrolled in Intune.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_andr_what_happs_add">
        <title>
          <caps:sentence id="src47" class="srcSentence">What happens when I install the Company Portal app and enroll my device in Intune?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src48" class="srcSentence">You start by installing the Company Portal app, and then use the app to enroll your device in Intune.</caps:sentence>
            <caps:sentence id="src49" class="srcSentence"> Once your device is enrolled, you  can use the Company Portal app to:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src50" class="srcSentence">Access the company’s network, and your email and work files</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src51" class="srcSentence">Get company apps from the Company Portal</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src52" class="srcSentence">Automatically configure your company email account</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src53" class="srcSentence">Reset your phone to factory settings if it is lost or stolen</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src54" class="srcSentence">When  you enroll your device in Intune, you are giving your IT administrator permission to manage your device to help protect the company information on the device.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">IT cannot see</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">IT can see</caps:sentence>
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
                        <caps:sentence id="src57" class="srcSentence">Call history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Text messages</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src59" class="srcSentence">Personal email, contacts, and calendar</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src60" class="srcSentence">Web history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src61" class="srcSentence">Location</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">Camera roll</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">Personal data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">Owner</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">Device name</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Serial number</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">Manufacturer</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">Model</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">Operating system</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">Company apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Personal apps</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src72" class="srcSentence">When you add your Android device, you are giving your IT administrator permission to access the device.</caps:sentence>
            <caps:sentence id="src73" class="srcSentence"> They can do things like:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src74" class="srcSentence">Reset your device back to manufacturer’s defaults.</caps:sentence>
                <caps:sentence id="src75" class="srcSentence"> This is helpful if the device is lost or stolen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src76" class="srcSentence">Remove all company related data.</caps:sentence>
                <caps:sentence id="src77" class="srcSentence"> Your personal data and settings aren’t removed.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src78" class="srcSentence">Force you to have a password or PIN on the device, which may lock you out of the device, or reset your device back to manufacturer’s default settings, which may include the deletion of data, if there are too many incorrect password attempts.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src79" class="srcSentence">Require you to accept terms and conditions.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src80" class="srcSentence">Enable or disable the camera on your device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src81" class="srcSentence">Force all the data, including corporate and personal data, on the device to be encrypted.</caps:sentence>
                <caps:sentence id="src82" class="srcSentence"> This helps protect the data if the device is lost or stolen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src83" class="srcSentence">After your device is added to the Company Portal, approximately every 8 hours it will:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">Download any policy or app updates that your IT administrator has made available.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">Send any hardware inventory updates (these updates do not contain personal information).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">Send any company app inventory updates (these updates do not contain personal information).</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_whatis_cp_website">
        <title>
          <caps:sentence id="src87" class="srcSentence">What is the Company Portal website and what can I do with it?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src88" class="srcSentence">The <externalLink><linkText>Company Portal website</linkText><linkUri>http://portal.manage.microsoft.com</linkUri></externalLink> is your company’s web interface that you use to manage your work computers and devices, and your personal computers and devices that you choose to use at work.</caps:sentence>
            <caps:sentence id="src89" class="srcSentence"> You can do most of the same tasks on this website that you can do by using the Company Portal app that you install on your device.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src90" class="srcSentence">You can do the following tasks from the Company Portal website:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src91" class="srcSentence">Browse for and download company apps</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src92" class="srcSentence">Rename your device</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src93" class="srcSentence">Remove your device from Intune</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src94" class="srcSentence">Reset your mobile device to its factory default settings</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src95" class="srcSentence">Find contact information for your IT administrator</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_andr_encrypt_your_device" expanded="true">
        <title>
          <caps:sentence id="src96" class="srcSentence">Encrypt your device</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src97" class="srcSentence">If your company or organization requires you to encrypt your device before you can access company files, email, or data, follow these steps to encrypt your device:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src98" class="srcSentence">Ensure that your device is connected to the charger.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src99" class="srcSentence">Tap <ui>Search</ui>.</caps:sentence>
                <caps:sentence id="src100" class="srcSentence"> In the Search box, type <ui>company portal</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src101" class="srcSentence">Ensure that a screen lock PIN or password has been set for your device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src102" class="srcSentence">In Settings, click <ui>Security</ui> &gt; <ui>Encrypt Phone</ui>.</caps:sentence>
                <caps:sentence id="src103" class="srcSentence"> (On some phones, you’ll need to click <ui>Storage</ui> &gt; <ui>Storage encryption</ui>).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src104" class="srcSentence">Follow the on-screen instructions.</caps:sentence>
                <caps:sentence id="src105" class="srcSentence"> During encryption, your device might restart several times.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src106" class="srcSentence">Ensure that your device is enrolled with Microsoft Intune by following the instructions in <link xlink:href="8373c587-b1ad-4c25-93f9-e0148834d495">Enroll your device in Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <maml:section expanded="true" address="BKMK_andr_set_pin" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src107" class="srcSentence">Set your PIN or password</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src108" class="srcSentence">Tap  <maml:ui>Settings</maml:ui> &gt; <maml:ui>Security</maml:ui> &gt; <maml:ui>Screen Lock</maml:ui> &gt; <maml:ui>Password</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src109" class="srcSentence">Choose and confirm your new password.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src110" class="srcSentence">Ensure that your device is enrolled with Microsoft Intune by following the instructions in <maml:link xlink:href="#BKMK_andr_enroll_devc"> Enroll your device in Intune</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src111" class="srcSentence">Tap <maml:ui>GET</maml:ui> &gt; <maml:ui>INSTALL</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_install_vpn" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src112" class="srcSentence">Install your company's Virtual Private Network (VPN)</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src113" class="srcSentence">If your IT administrator has configured a VPN application to enable you to  connect to your company's resources, you'll see a notification on your device indicating that you need to install a VPN app.</caps:sentence>
            <caps:sentence id="src114" class="srcSentence"> Follow these steps to install the VPN app:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src115" class="srcSentence">Open the notification, and tap <maml:ui>Tap to install this required app</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src116" class="srcSentence">In the <maml:ui>Play Store</maml:ui>, click <maml:ui>INSTALL</maml:ui> and follow the prompts to install the app.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src117" class="srcSentence">Tap <maml:ui>Install corporate VPN profile</maml:ui> and follow the prompts to accept and activate the app.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_unenroll_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src118" class="srcSentence">Unenroll your device from Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src119" class="srcSentence">When you unenroll your device from Intune, your device will not longer be able to access company resources and will no longer be managed by Intune.</caps:sentence>
          </maml:para>
          <maml:para>
            <caps:sentence id="src120" class="srcSentence">To unenroll your device from Intune:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src121" class="srcSentence">Press <maml:ui>MY DEVICES</maml:ui> and select the device to unenroll.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src122" class="srcSentence">Press <maml:ui>Remove</maml:ui> &gt; <maml:ui>OK</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
          <maml:para>
            <caps:sentence id="src123" class="srcSentence">When you unenroll your device from Intune, here's what happens:</caps:sentence>
          </maml:para>
          <maml:list class="bullet">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src124" class="srcSentence">Your device won’t appear in the Company Portal anymore.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src125" class="srcSentence">You can’t install apps from the Company Portal anymore.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src126" class="srcSentence">Any settings that were changed on your device when you added it, for example disabling the camera, or requiring a certain password length, will no longer apply.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src127" class="srcSentence">You might not have access to some company resources, such as file shares or internal web sites, on your device anymore.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src128" class="srcSentence">Devices that are configured for email only won't appear in the Company Portal app or website anymore.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_erase_lost_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src129" class="srcSentence">Reset (erase) your lost or stolen device</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src130" class="srcSentence">If your phone is lost or stolen, you can reset it to factory defaults.</caps:sentence>
          </maml:para>
          <maml:alert class="warning">
            <maml:para>
              <caps:sentence id="src131" class="srcSentence">Resetting a device to factor defaults removes both your personal and work information from it.</caps:sentence>
            </maml:para>
          </maml:alert>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src132" class="srcSentence">Open <maml:ui>portal.manage.microsoft.com</maml:ui> in your browser, and sign in to your work account.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src133" class="srcSentence">Tap <maml:ui>My Devices</maml:ui> and select the name of the lost of stolen  device.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src134" class="srcSentence">Click <maml:ui>Reset</maml:ui> &gt; <maml:ui>Reset</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:alert class="note">
                <maml:para>
                  <caps:sentence id="src135" class="srcSentence">If you are unable to reset your lost or stolen device, ask your IT administrator to reset it for you.</caps:sentence>
                </maml:para>
              </maml:alert>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section address="BKMK_andr_data_collect" expanded="true">
        <title>
          <caps:sentence id="src136" class="srcSentence">Turn off Microsoft usage data collection</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src137" class="srcSentence">In order to improve its products and services, Microsoft automatically collects anonymous data about the reliability and performance of the Company Portal app and how it is used.</caps:sentence>
            <caps:sentence id="src138" class="srcSentence"> You can turn off the collection of that data by using the Usage Data setting in the Company Portal app.</caps:sentence>
            <caps:sentence id="src139" class="srcSentence"> IT administrators have no control over the collection of the data, and they cannot change your selection for the setting.</caps:sentence>
          </para>
        </content>
      </section>
      <maml:section address="BKMK_andr_fix_issues" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src140" class="srcSentence">Fix issues when your device is enrolled in Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src141" class="srcSentence">Use this information to help your IT admin fix any issues that you have with your device when you've installed the Company Portal app and enrolled your device in Intune.</caps:sentence>
          </maml:para>
        </maml:content>
        <maml:sections>
          <maml:section address="BKMK_andr_verboselogging">
            <maml:title>
              <caps:sentence id="src142" class="srcSentence">Use Verbose Logging to help your IT admin fix issues</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence id="src143" class="srcSentence">When your device is enrolled in Intune, you can use the <maml:ui>Verbose Logging</maml:ui> setting to make the Company Portal app and Intune-managed apps record detailed logs about what's happening on your device.</caps:sentence>
                <caps:sentence id="src144" class="srcSentence"> These logs help your IT admin fix any issues that you might have when you're using the Company Portal or an app that's managed by Intune.</caps:sentence>
                <caps:sentence id="src145" class="srcSentence"> Verbose Logging is enabled on your device  by default, and the  logs that are sent to your IT admin  include your email address.</caps:sentence>
              </maml:para>
              <maml:para>
                <caps:sentence id="src146" class="srcSentence">To turn <maml:ui>Verbose Logging</maml:ui> on or off, sign in to the Company Portal app using your work or school credentials, tap <maml:ui>Settings</maml:ui>, and tap the on/off button next to the <maml:ui>Verbose Logging</maml:ui> setting.</caps:sentence>
              </maml:para>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_diag_logs">
            <maml:title>
              <caps:sentence id="src147" class="srcSentence">Send diagnostic data logs to your IT admin using email</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence id="src148" class="srcSentence">If you get an error while you're working with your school or company apps or while you're in the Company Portal app, you can send diagnostic data logs  to help your IT admin figure out and fix the error.</caps:sentence>
                <caps:sentence id="src149" class="srcSentence"> To include all of the details in the logs, which will make it easier for your IT admin to figure out the issue, turn on Verbose Logging.</caps:sentence>
              </maml:para>
              <maml:list class="ordered">
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src150" class="srcSentence">Open the Company Portal app.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src151" class="srcSentence">Tap <maml:ui>Menu</maml:ui> &gt;  <maml:ui>Settings</maml:ui>.</caps:sentence>
                  </maml:para>
                  <maml:alert class="note">
                    <maml:para>
                      <caps:sentence id="src152" class="srcSentence">
                        <maml:ui>Menu</maml:ui> could be a software button or a hardware button, depending on the type of Android device you have.</caps:sentence>
                    </maml:para>
                  </maml:alert>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src153" class="srcSentence">Under <maml:ui>Diagnostic Data</maml:ui>, tap <maml:ui>Send Data</maml:ui>.</caps:sentence>
                  </maml:para>
                  <maml:mediaLink>
                    <maml:image xlink:href="e689c712-0ce0-461a-bfb2-5dd59e218a7b"></maml:image>
                  </maml:mediaLink>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src154" class="srcSentence">Follow the prompts to choose an email app to use for sending the logs to your IT admin.</caps:sentence>
                    <caps:sentence id="src155" class="srcSentence"> The app will create a pre-addressed email with all the logs attached.</caps:sentence>
                  </maml:para>
                </maml:listItem>
              </maml:list>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_diag_usbcable">
            <maml:title>
              <caps:sentence id="src156" class="srcSentence">Send diagnostic data logs to your IT admin using a USB cable</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence id="src157" class="srcSentence">If you're using a computer rather than a mobile device, and you want to send data logs to have your IT admin figure out and fix your issue, use these steps:</caps:sentence>
              </maml:para>
              <maml:list class="ordered">
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src158" class="srcSentence">Before you start, make sure that you have your IT admin's email address.</caps:sentence>
                    <caps:sentence id="src159" class="srcSentence"> It is typically listed on your Company Portal website or in your Company Portal app.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src160" class="srcSentence">Use a USB cable to connect your device to a computer.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src161" class="srcSentence">On the computer, look for a directory that has the name of your phone.</caps:sentence>
                    <caps:sentence id="src162" class="srcSentence"> In that directory, find &lt;Android Device&gt;\Phone\Android\data\com.microsoft.windowsintune.companyportal\files\.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src163" class="srcSentence">Attach all of the files to an email and send them to your IT admin.</caps:sentence>
                  </maml:para>
                </maml:listItem>
              </maml:list>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_enroll_errors">
            <maml:title>
              <caps:sentence id="src164" class="srcSentence">Send enrollment errors to your IT admin</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence id="src165" class="srcSentence">If you get an error while trying to enroll your device in Intune, you can try enrolling again by tapping <maml:ui>Retry</maml:ui>, or send the error information to your IT admin in an email by tapping <maml:ui>Send info</maml:ui>.</caps:sentence>
                <caps:sentence id="src166" class="srcSentence"> An email, addressed to your IT administrator, is automatically created and contains the logs that your IT admin needs to help troubleshoot your device.</caps:sentence>
              </maml:para>
            </maml:content>
          </maml:section>
        </maml:sections>
      </maml:section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>