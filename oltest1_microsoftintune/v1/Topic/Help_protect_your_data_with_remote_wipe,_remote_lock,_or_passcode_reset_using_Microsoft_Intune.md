---
description: na
keywords: na
title: Help protect your data with remote wipe, remote lock, or passcode reset using Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8519e411-3d48-44eb-9b41-3e4fd6a93112
---
# Sch&#252;tzen Ihrer Daten mit Remotezur&#252;cksetzen, Remotesperre und Kennungszur&#252;cksetzung in Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerHowToDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0fdf1dd07c8716c405006a8ffbe79cc8" id="tgt1" class="tgtSentence">In <token>wit_firstref</token> sind Funktionen zum selektiven und vollständigen Zurücksetzen, zum Remotesperren und zur Kennungsrückstellung verfügbar.</caps:sentence>
          <caps:sentence sentenceid="8aa0f9aa43918aa75163959b8689a869" id="tgt2" class="tgtSentence"> Da auf mobilen Geräten sensible Unternehmensdaten gespeichert sein können und die Geräte mitunter Zugriff auf zahlreiche Unternehmensressourcen bieten, haben Sie über die <token>wit_adminconsole</token> die Möglichkeit, bei Verlust oder Diebstahl eines Geräts einen Remotebefehl zum Zurücksetzen des Geräts zu erteilen.</caps:sentence>
          <caps:sentence sentenceid="6358c4f3c978ba55a20d30d161186924" id="tgt3" class="tgtSentence"> Für private Geräte, die in Intune registriert sind, können Benutzer auch über das <token>wit_iwportal_1</token> einen Remotebefehl zum Zurücksetzen des Geräts erteilen.</caps:sentence>
        </para>
      </introduction>
      <section address="bkmk_wipe">
        <title>
          <caps:sentence sentenceid="517980a5512703c7fafe7e46b016b352" id="tgt4" class="tgtSentence">Abkoppeln/Zurücksetzen</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="be87cddee46f2da39b1c5a90d139d2b4" id="tgt5" class="tgtSentence">Sie können einen Befehl zm <embeddedLabel>Abkoppeln/Zurücksetzen</embeddedLabel> senden, um ein verlorengegangenes Gerät zu sichern oder ein Gerät von der aktiven Verwendung abzukoppeln.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="04e77bb2f0f59c25bd82968b9a14071c" id="tgt6" class="tgtSentence">
              <ui>Vollständiges Zurücksetzen</ui> setzt ein Gerät auf die standardmäßigen Werkseinstellungen zurück, wobei alle Unternehmens- und Benutzerdaten und -einstellungen entfernt werden.</caps:sentence>
            <caps:sentence sentenceid="d13d61ac22b43e737647c2daf81cbc00" id="tgt7" class="tgtSentence">    Das Gerät wird aus Intune entfernt.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0b334164ddedd5420c2cb07c4ed67380" id="tgt8" class="tgtSentence">
              <ui>Selektives Zurücksetzen</ui> entfernt Unternehmensdaten von einem Gerät.</caps:sentence>
            <caps:sentence sentenceid="9e438635f99f9d9878eac5b751f39976" id="tgt9" class="tgtSentence">   Das Gerät wird aus Intune entfernt.</caps:sentence>
            <caps:sentence sentenceid="dc88b50382d39d734ea8b187bcee1142" id="tgt10" class="tgtSentence"> In der folgenden Tabelle wird nach Plattform sortiert beschrieben, welche Daten bei einem selektiven Zurücksetzen entfernt werden und mit welchen Auswirkungen auf verbleibende Daten zu rechnen ist.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7ba981cac505bfc21adfc15465f0dcd7" id="tgt11" class="tgtSentence">Inhaltstyp</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1199aa0fe830abab3654601a8a83f5ab" id="tgt12" class="tgtSentence">Windows 8.1 (registriert als mobiles Gerät) und Windows RT 8.1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="94c0739f54e8886ceea4fe3078c068e3" id="tgt13" class="tgtSentence">Windows RT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8df8bb88e54e9e991ed9987776f3a9d0" id="tgt14" class="tgtSentence">Windows Phone 8 und Windows Phone 8.1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt15" class="tgtSentence">iOS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c31b32364ce19ca8fcd150a417ecce58" id="tgt16" class="tgtSentence">Android</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="856d140b0d1a4ba4c61320eaf8142dda" id="tgt17" class="tgtSentence">Android Samsung KNOX</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="248adbc7972000022411aec2b46f432b" id="tgt18" class="tgtSentence">Unternehmensanwendungen und zugehörige Daten, die von <token>wit_firstref</token> installiert wurden.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="641bab2555bc9b0a4fc1b79d15f849f2" id="tgt19" class="tgtSentence">Bei Dateien, die durch ein EFS geschützt sind, wird der Schlüssel gesperrt, und der Benutzer kann die Dateien nicht mehr öffnen.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7a0eb6565f6d3ef0bc7d865fae381c36" id="tgt20" class="tgtSentence">Unternehmensanwendungen werden nicht entfernt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8a5fd0192c8c7337e1a765f5f923b6a1" id="tgt21" class="tgtSentence">Ursprünglich über das Unternehmensportal installierte Anwendungen werden deinstalliert.</caps:sentence>
                    <caps:sentence sentenceid="f4ba89f19df104a382e77619f788c090" id="tgt22" class="tgtSentence"> Daten von Unternehmens-Apps werden entfernt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="35b9ca0c3036bad69b90708f9edf415e" id="tgt23" class="tgtSentence">Apps werden deinstalliert.</caps:sentence>
                    <caps:sentence sentenceid="f4ba89f19df104a382e77619f788c090" id="tgt24" class="tgtSentence"> Daten von Unternehmens-Apps werden entfernt.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d92f748390d893c3fc0f163555371fec" id="tgt25" class="tgtSentence">App-Daten aus Microsoft-Anwendungen, die die Verwaltung von mobilen Anwendungen verwenden, werden entfernt.</caps:sentence>
                    <caps:sentence sentenceid="2e681ff2912b5ade2e6d3c81e4b02ecc" id="tgt26" class="tgtSentence"> Die App wird nicht entfernt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="19e787dc6c19522aa54ca375a63538ca" id="tgt27" class="tgtSentence">Für Intune optimierte Unternehmens-Apps wie Microsoft Office-Apps oder Apps, die mithilfe des App Wrapping Tools oder des Intune SDKs bereitgestellt wurden, werden zusammen mit ihren Daten entfernt.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f9ea170d5c2a5e928b217673e3d783eb" id="tgt28" class="tgtSentence">App-Daten aus Microsoft-Anwendungen, die die Verwaltung von mobilen Anwendungen verwenden, werden entfernt.</caps:sentence>
                    <caps:sentence sentenceid="2e681ff2912b5ade2e6d3c81e4b02ecc" id="tgt29" class="tgtSentence"> Die App wird nicht entfernt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0f59e20ee59f0ff596972e0dab0114c5" id="tgt30" class="tgtSentence">Für Intune optimierte Unternehmens-Apps wie Office-Apps oder Apps, die mithilfe des App Wrapping Tools oder des Intune SDKs bereitgestellt wurden, werden zusammen mit ihren Daten entfernt.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f9ea170d5c2a5e928b217673e3d783eb" id="tgt31" class="tgtSentence">App-Daten aus Microsoft-Anwendungen, die die Verwaltung von mobilen Anwendungen verwenden, werden entfernt.</caps:sentence>
                    <caps:sentence sentenceid="2e681ff2912b5ade2e6d3c81e4b02ecc" id="tgt32" class="tgtSentence"> Die App wird nicht entfernt.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2e5d8aa3dfa8ef34ca5131d20f9dad51" id="tgt33" class="tgtSentence">Einstellung</caps:sentence>
                  </para>
                </TD>
                <TD colspan="6">
                  <para>
                    <caps:sentence sentenceid="5515abf17871a5a41d24ac61f5a00e10" id="tgt34" class="tgtSentence">Konfigurationen, die von der <token>wit_nextref</token>-Richtlinie festgelegt wurden, werden nicht mehr erzwungen, und Benutzer können die Einstellungen ändern.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b3696463a19c9f7dd525cf212b97bd93" id="tgt35" class="tgtSentence">Einstellungen für WLAN- und VPN-Profil</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b07286ebbb5bc7aa91cc3eaa8bc19711" id="tgt36" class="tgtSentence">Entfernt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b07286ebbb5bc7aa91cc3eaa8bc19711" id="tgt37" class="tgtSentence">Entfernt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb3a4d67c4f997a68df8924b2b18d70d" id="tgt38" class="tgtSentence">Nicht unterstützt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b07286ebbb5bc7aa91cc3eaa8bc19711" id="tgt39" class="tgtSentence">Entfernt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b07286ebbb5bc7aa91cc3eaa8bc19711" id="tgt40" class="tgtSentence">Entfernt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b07286ebbb5bc7aa91cc3eaa8bc19711" id="tgt41" class="tgtSentence">Entfernt</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a1e290362e2e431324af3eef742af3ce" id="tgt42" class="tgtSentence">Zertifikatprofil-Einstellungen</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d45e44c6d24444e3ac79628540f418df" id="tgt43" class="tgtSentence">Zertifikate wurden entfernt und gesperrt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d45e44c6d24444e3ac79628540f418df" id="tgt44" class="tgtSentence">Zertifikate wurden entfernt und gesperrt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb3a4d67c4f997a68df8924b2b18d70d" id="tgt45" class="tgtSentence">Nicht unterstützt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d45e44c6d24444e3ac79628540f418df" id="tgt46" class="tgtSentence">Zertifikate wurden entfernt und gesperrt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c1f1616f49996f4e35ff1f127ad03b55" id="tgt47" class="tgtSentence">Zertifikate gesperrt, aber nicht entfernt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d45e44c6d24444e3ac79628540f418df" id="tgt48" class="tgtSentence">Zertifikate wurden entfernt und gesperrt.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bd9b65cb279ae2fb856ab9832fab5c64" id="tgt49" class="tgtSentence">Verwaltungs-Agent</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a2d8e98f65bdf9f5c22398df2acade0e" id="tgt50" class="tgtSentence">Nicht zutreffend.</caps:sentence>
                    <caps:sentence sentenceid="5a752e4ee6eddc6924d8b667c8466f87" id="tgt51" class="tgtSentence"> Der Verwaltungs-Agent ist integriert.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a2d8e98f65bdf9f5c22398df2acade0e" id="tgt52" class="tgtSentence">Nicht zutreffend.</caps:sentence>
                    <caps:sentence sentenceid="5a752e4ee6eddc6924d8b667c8466f87" id="tgt53" class="tgtSentence"> Der Verwaltungs-Agent ist integriert.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a2d8e98f65bdf9f5c22398df2acade0e" id="tgt54" class="tgtSentence">Nicht zutreffend.</caps:sentence>
                    <caps:sentence sentenceid="5a752e4ee6eddc6924d8b667c8466f87" id="tgt55" class="tgtSentence"> Der Verwaltungs-Agent ist integriert.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a424d59c2e5d4a9b4bdcea4e50134b68" id="tgt56" class="tgtSentence">Das Verwaltungsprofil wird entfernt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e93bda2da711ce09e859054c87645a02" id="tgt57" class="tgtSentence">Die Berechtigung „Geräteadministrator“ wird gesperrt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e93bda2da711ce09e859054c87645a02" id="tgt58" class="tgtSentence">Die Berechtigung „Geräteadministrator“ wird gesperrt.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0c83f57c786a0b4a39efab23731c7ebc" id="tgt59" class="tgtSentence">E-Mail</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34b9cc3d3f5fdd627fafe5ecf705ed39" id="tgt60" class="tgtSentence">Entfernt EFS-aktivierte E-Mails, darunter die E-Mail-App für Windows-E-Mails und -Anlagen.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cb3a4d67c4f997a68df8924b2b18d70d" id="tgt61" class="tgtSentence">Nicht unterstützt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3ba6fc700e02d74f8e72323bd2f704e3" id="tgt62" class="tgtSentence">E-Mail-Profile, die über <token>wit_nextref</token> bereitgestellt werden, werden entfernt und zwischengespeicherte E-Mails auf dem Gerät gelöscht.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3ba6fc700e02d74f8e72323bd2f704e3" id="tgt63" class="tgtSentence">E-Mail-Profile, die über <token>wit_nextref</token> bereitgestellt werden, werden entfernt und zwischengespeicherte E-Mails auf dem Gerät gelöscht.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d7ffe390c0fdddea5c2469abec685f43" id="tgt64" class="tgtSentence">E-Mails, die über die Microsoft Outlook-App für Android empfangen wurden, werden entfernt.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3ba6fc700e02d74f8e72323bd2f704e3" id="tgt65" class="tgtSentence">E-Mail-Profile, die über <token>wit_nextref</token> bereitgestellt werden, werden entfernt und zwischengespeicherte E-Mails auf dem Gerät gelöscht.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4deaf0758dfb35855809099264903491" id="tgt66" class="tgtSentence">Azure Active Directory (AAD)-Verbindung aufgehoben</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt67" class="tgtSentence">Nein</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt68" class="tgtSentence">Nein</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3dfa7e05f720cd0b504e106170dbbc69" id="tgt69" class="tgtSentence">AAD-Datensatz entfernt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3dfa7e05f720cd0b504e106170dbbc69" id="tgt70" class="tgtSentence">AAD-Datensatz entfernt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3dfa7e05f720cd0b504e106170dbbc69" id="tgt71" class="tgtSentence">AAD-Datensatz entfernt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3dfa7e05f720cd0b504e106170dbbc69" id="tgt72" class="tgtSentence">AAD-Datensatz entfernt</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <procedure>
            <title>
              <caps:sentence sentenceid="d7b4fbd2cf0e7ae3ea4defa03de16e69" id="tgt73" class="tgtSentence">So starten Sie eine Remotezurücksetzung aus der <token>wit_adminconsole</token></caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3c273d415b28a2ac22697b0eb19856e7" id="tgt74" class="tgtSentence">Wählen Sie die Geräte aus, die zurückgesetzt werden sollen:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="981fa6c30ee3ec35e8756b39fd843f84" id="tgt75" class="tgtSentence">Nach Benutzer:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt76" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Gruppen</ui> &gt; <ui>Alle Benutzer</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="2954ea3aa8132f31aa56da7f72bb2fb9" id="tgt77" class="tgtSentence">Klicken Sie auf den Namen des Benutzers, dessen mobiles Gerät Sie zurücksetzen möchten, und dann auf <ui>Eigenschaften anzeigen</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt78" class="tgtSentence">Klicken Sie auf der Seite <ui>Eigenschaften</ui> des Benutzers auf die Registerkarte <ui>Geräte</ui>, und klicken Sie dann auf den Namen des mobilen Geräts, das Sie zurücksetzen möchten.</caps:sentence>
                            <caps:sentence sentenceid="727a56da56bee5792b4945646d6f7672" id="tgt79" class="tgtSentence"> Halten Sie die STRG-Taste gedrückt, und klicken Sie, um mehrere Geräte auszuwählen.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="97d704a3459af48615e1cf81ab00f2b6" id="tgt80" class="tgtSentence">Nach Gerät:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt81" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Gruppen</ui> &gt; <ui>Alle mobilen Geräte</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="41ad10da17628099ea69f30e0bc238ba" id="tgt82" class="tgtSentence">Klicken Sie auf die Registerkarte <ui>Geräte</ui>, und klicken Sie dann auf den Namen des mobilen Geräts, das Sie zurücksetzen möchten.</caps:sentence>
                            <caps:sentence sentenceid="727a56da56bee5792b4945646d6f7672" id="tgt83" class="tgtSentence"> Halten Sie die STRG-Taste gedrückt, und klicken Sie, um mehrere Geräte auszuwählen.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt84" class="tgtSentence">Klicken Sie auf der Taskleiste auf <ui>Abkoppeln/Zurücksetzen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1bc1a1b9527f837f7619ed0387bcc1c9" id="tgt85" class="tgtSentence">Durch eine Meldung werden Sie aufgefordert, zu bestätigen, ob Sie das Gerät abkoppeln möchten.</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="eeb2815e2c9edf95a1482ca6d529b2c0" id="tgt86" class="tgtSentence">Klicken Sie zum Ausführen einer <embeddedLabel>selektiven Zurücksetzung</embeddedLabel>, bei der nur unternehmenseigene Apps und Daten entfernt werden, auf <ui>Ja</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="eeb2815e2c9edf95a1482ca6d529b2c0" id="tgt87" class="tgtSentence">Wählen Sie zum Ausführen einer <embeddedLabel>vollständigen Zurücksetzung</embeddedLabel>, bei der alle Apps und Daten gelöscht werden und das Gerät auf die werkseitigen Standardeinstellungen zurückgesetzt wird, auf <ui>Gerät vor dem Abkoppeln zurücksetzen</ui>.</caps:sentence>
                        <caps:sentence sentenceid="ff8685b8e4c2ea4438bef60ecd8d212f" id="tgt88" class="tgtSentence"> Diese Aktion gilt für alle Plattformen außer Windows 8.1.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="1a1db6d598541ad47478446ec7008755" id="tgt89" class="tgtSentence">Das Verteilen des Zurücksetzens über alle Gerätetypen dauert höchstens 15 Minuten.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="bdf292ed9e8274795ce4fcad1514bb2f" id="tgt90" class="tgtSentence">Zurücksetzen EFS-aktivierter Inhalte</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="92b3247491198dea139851cd8b6506a2" id="tgt91" class="tgtSentence">Das selektive Zurücksetzen von EFS-verschlüsselten Inhalten wird von Windows 8.1 und Windows RT 8.1 unterstützt.</caps:sentence>
                <caps:sentence sentenceid="437b76eea4aa9e767dec2d7785a5fcf8" id="tgt92" class="tgtSentence"> Folgendes gilt für das selektive Zurücksetzen von EFS-aktivierten Inhalten:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="95eddd6912804e29548c4be10200179a" id="tgt93" class="tgtSentence">Nur Apps und Daten, die mit derselben Internetdomäne wie das <token>wit_nextref</token>-Konto von EFS geschützt werden, werden selektiv zurückgesetzt.</caps:sentence>
                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt94" class="tgtSentence"> Weitere Informationen finden Sie unter <externalLink><linkText>Windows Selective Wipe for Device Data Management</linkText><linkUri>http://technet.microsoft.com/library/dn486874.aspx</linkUri></externalLink> (in englischer Sprache).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3bf56d3061cc1860fd939191f2143720" id="tgt95" class="tgtSentence">Wenn Änderungen an der EFS zugeordneten Domäne vorgenommen werden, können die Änderungen bis zu 48 Stunden dauern, bevor Apps und Daten selektiv zurückgesetzt werden können, die die neue Domäne verwenden.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="24766dd1e82928456fb2e813bfde59d5" id="tgt96" class="tgtSentence">Jede bei <token>wit_nextref</token> registrierte Domäne wird zurückgesetzt.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="5a5b63a5e4782152b6a52ca2fdbae408" id="tgt97" class="tgtSentence">Folgende Daten und Apps werden derzeit vom selektiven Zurücksetzen mit EFS unterstützt:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d036fead104e3385f807517e047afff7" id="tgt98" class="tgtSentence">E-Mail-App für Windows</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f3b8eb1798e64e6757ef9fa9d8944496" id="tgt99" class="tgtSentence">Arbeitsordner</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8f7e07520abeef68a5890d4802647909" id="tgt100" class="tgtSentence">Von EFS verschlüsselte Dateien und Ordner</caps:sentence>
                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt101" class="tgtSentence"> Weitere Informationen finden Sie unter <externalLink><linkText>Vorgehensweisen bei Verwendung des verschlüsselnden Dateisystems</linkText><linkUri>http://support.microsoft.com/kb/223316</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ccc713659b97dbbd9d5abb98f1d8dcb2" id="tgt102" class="tgtSentence">Wenn Ihr Unternehmen seine Identität in Active Directory verwaltet, muss das Tool Verzeichnissynchronisierung (DirSync) verwendet werden, um Informationen in AAD zu synchronisieren, damit das selektive EFS-Zurücksetzen ordnungsgemäß funktioniert.</caps:sentence>
                    <caps:sentence sentenceid="e952290feee5dd578dcd199c0ee78883" id="tgt103" class="tgtSentence">  Weitere Informationen zu DirSync finden Sie unter <externalLink><linkText>Verzeichnissynchronisierungsszenario</linkText><linkUri>http://technet.microsoft.com/library/dn441212.aspx</linkUri></externalLink> in der Azure Active Directory-Dokumentation.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="c68a03e60001a5a3a5ab3897740f0eb0" id="tgt104" class="tgtSentence">Aktionen zum Deaktivieren, Zurücksetzen und Löschen des Monitors</caps:sentence>
            </title>
            <content>
              <procedure>
                <title></title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt105" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Berichte</ui> &gt; <ui>Berichte zum Geräteverlauf</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ca82b6719d9778f6c36790debb0d6010" id="tgt106" class="tgtSentence">Geben Sie ein Start- und Enddatum für den Bericht ein, und klicken Sie dann auf <ui>Bericht anzeigen</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence sentenceid="035bb4e87dc1b2639437f93364af284f" id="tgt107" class="tgtSentence">Der Bericht enthält eine Liste der Abkoppel-, Zurücksetz- und Löschvorgänge, die für jedes Gerät ausgeführt wurden, sowie den Namen des jeweiligen Initiators.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
          <section address="BKMK_passcode">
            <title>
              <caps:sentence sentenceid="d003b5fa135070b607f30bd2047fb2f9" id="tgt108" class="tgtSentence">Zurücksetzen der Kennung</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="7156d3310b4f3e4eecb38e2f0e07a970" id="tgt109" class="tgtSentence">Wenn ein Benutzer seine Kennung vergisst, können Sie die Kennung von einem Gerät entfernen oder eine neue temporäre Kennung auf einem Gerät erzwingen.</caps:sentence>
                <caps:sentence sentenceid="473ff4760e1f79d2236f427350f2382d" id="tgt110" class="tgtSentence"> In der folgenden Tabelle ist die Funktionsweise der Kennungszurücksetzung auf verschiedenen mobilen Plattformen aufgeführt.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt111" class="tgtSentence">Plattform</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d003b5fa135070b607f30bd2047fb2f9" id="tgt112" class="tgtSentence">Zurücksetzen der Kennung</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt113" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ed851cc49d89f8860dddee29b0e09e64" id="tgt114" class="tgtSentence">Wird für das Löschen der Kennung von einem Gerät unterstützt.</caps:sentence>
                        <caps:sentence sentenceid="6c58177fc175f12389e9a81a17483004" id="tgt115" class="tgtSentence"> Es wird keine neue temporäre Kennung erstellt.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c31b32364ce19ca8fcd150a417ecce58" id="tgt116" class="tgtSentence">Android</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e8778a9be97546f5450de9e79f728a51" id="tgt117" class="tgtSentence">Wird unterstützt. Zudem wird eine temporäre Kennung erstellt.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt118" class="tgtSentence">Windows Phone 8 und Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="42bd4c0819c498d1c1ab622de74d6f82" id="tgt119" class="tgtSentence">Unterstützt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0060636b449d1da5a8581bfee180f0c2" id="tgt120" class="tgtSentence">
                          <token>winblue_winrt_2</token>und <token>win8RT_client_1</token> (möglicherweise in englischer Sprache)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cb3a4d67c4f997a68df8924b2b18d70d" id="tgt121" class="tgtSentence">Nicht unterstützt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ff096d14c13e95dfc9db9eb98f194114" id="tgt122" class="tgtSentence">Windows 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cb3a4d67c4f997a68df8924b2b18d70d" id="tgt123" class="tgtSentence">Nicht unterstützt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <procedure>
                <title>
                  <caps:sentence sentenceid="963c2f8d77aab37c6b9f96168a226abb" id="tgt124" class="tgtSentence">So setzen Sie die Kennung auf einem mobilen Gerät remote über die Microsoft Intune-Konsole zurück</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt125" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Gruppen</ui> &gt; <ui>Alle Geräte</ui> &gt; <ui>Alle mobilen Geräte</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt126" class="tgtSentence">Klicken Sie bei Geräten, die bei <token>wit_firstref</token> registriert sind, auf <ui>Alle direkt verwalteten Geräte</ui>, andernfalls klicken Sie auf <ui>Alle mit Exchange ActiveSync verwalteten Geräte</ui>.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="2fd557135cf53053330bb04689a384e9" id="tgt127" class="tgtSentence">Sie können auch nach Benutzer zu einem Gerät navigieren.</caps:sentence>
                          <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt128" class="tgtSentence"> Klicken Sie auf <ui>Alle Benutzer</ui> und dann auf der Eigenschaftenseite des Benutzers auf die Registerkarte <ui>Geräte</ui>. Klicken Sie auf den Namen des mobilen Geräts, das Sie zurücksetzen möchten.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="b2a4a834d3cbf2a1af63b6ec06c37db2" id="tgt129" class="tgtSentence">Klicken Sie in der Liste auf das oder die Geräte, die Sie sperren möchten. Klicken Sie dann in der Taskleiste auf <ui>Remotetasks</ui> und wählen Sie <ui>Kennung zurücksetzen</ui> aus.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="ebad506c3c37d17b9f5505ba14630ace" id="tgt130" class="tgtSentence">Remotesperre</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="c89c942f9b9de10589d07262c1be436e" id="tgt131" class="tgtSentence">Wenn ein Benutzer sein Gerät verliert, können Sie es remote sperren.</caps:sentence>
                <caps:sentence sentenceid="f2b75f6f7299e9f52d0a30d09a19fdaa" id="tgt132" class="tgtSentence"> In der folgenden Tabelle ist die Funktionsweise der Remotesperrung auf verschiedenen mobilen Plattformen aufgeführt.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt133" class="tgtSentence">Plattform</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ebad506c3c37d17b9f5505ba14630ace" id="tgt134" class="tgtSentence">Remotesperre</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt135" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="42bd4c0819c498d1c1ab622de74d6f82" id="tgt136" class="tgtSentence">Unterstützt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c31b32364ce19ca8fcd150a417ecce58" id="tgt137" class="tgtSentence">Android</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="42bd4c0819c498d1c1ab622de74d6f82" id="tgt138" class="tgtSentence">Unterstützt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt139" class="tgtSentence">Windows Phone 8 und Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="42bd4c0819c498d1c1ab622de74d6f82" id="tgt140" class="tgtSentence">Unterstützt</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0060636b449d1da5a8581bfee180f0c2" id="tgt141" class="tgtSentence">
                          <token>winblue_winrt_2</token>und <token>win8RT_client_1</token> (möglicherweise in englischer Sprache)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a1fdc8d8c4af2c04e08cbc0c3836d765" id="tgt142" class="tgtSentence">Unterstützt, wenn der aktuelle Benutzer des Geräts derjenige ist, der das Gerät registriert hat.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ff096d14c13e95dfc9db9eb98f194114" id="tgt143" class="tgtSentence">Windows 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a1fdc8d8c4af2c04e08cbc0c3836d765" id="tgt144" class="tgtSentence">Unterstützt, wenn der aktuelle Benutzer des Geräts derjenige ist, der das Gerät registriert hat.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <procedure>
                <title>
                  <caps:sentence sentenceid="f02c3b40e8a7f6b44719e18d9dc022bd" id="tgt145" class="tgtSentence">So sperren Sie ein mobiles Gerät remote über die Microsoft Intune-Konsole</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt146" class="tgtSentence">Klicken Sie in der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink> auf <ui>Gruppen</ui> &gt; <ui>Alle Geräte</ui> &gt; <ui>Alle mobilen Geräte</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt147" class="tgtSentence">Klicken Sie bei Geräten, die bei <token>wit_firstref</token> registriert sind, auf <ui>Alle direkt verwalteten Geräte</ui>, andernfalls klicken Sie auf <ui>Alle mit Exchange ActiveSync verwalteten Geräte</ui>.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="2fd557135cf53053330bb04689a384e9" id="tgt148" class="tgtSentence">Sie können auch nach Benutzer zu einem Gerät navigieren.</caps:sentence>
                          <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt149" class="tgtSentence"> Klicken Sie auf <ui>Alle Benutzer</ui> und dann auf der Eigenschaftenseite des Benutzers auf die Registerkarte <ui>Geräte</ui>. Klicken Sie auf den Namen des mobilen Geräts, das Sie zurücksetzen möchten.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="b2a4a834d3cbf2a1af63b6ec06c37db2" id="tgt150" class="tgtSentence">Klicken Sie in der Liste auf das oder die Geräte, die Sie sperren möchten. Klicken Sie dann in der Taskleiste auf <ui>Remotetasks</ui> und wählen Sie <ui>Remotesperre</ui> aus.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="3dbec400-5d8a-47be-b892-7745811d9de2">Retire data and devices from Microsoft Intune management</link>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="ce57cdd63557682338b263927b21908c" id="tgt151" class="tgtSentence">Windows Selective Wipe for Device Data Management (Selektives Zurücksetzen bei der Gerätedatenverwaltung in Windows)</caps:sentence>
          </linkText>
          <linkUri>http://technet.microsoft.com/library/dn486874.aspx</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="bd854e819a9550dafe0c9b715e019a4d" id="tgt152" class="tgtSentence">Intune-Bezugsquellen</caps:sentence>
          </linkText>
          <linkUri>http://technet.microsoft.com/library/dn646949.aspx</linkUri>
        </externalLink>
      </relatedTopics>
    </developerHowToDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerHowToDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <token>wit_firstref</token> provides selective wipe, full wipe, remote lock, and passcode reset capabilities.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Because mobile devices can store sensitive corporate data and provide access to many corporate resources, you can issue a remote device wipe command from the <token>wit_adminconsole</token> to wipe a lost or stolen device.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Also, users can issue a remote device wipe command from the <token>wit_iwportal_1</token> on privately owned devices enrolled in Intune.</caps:sentence>
        </para>
      </introduction>
      <section address="bkmk_wipe">
        <title>
          <caps:sentence id="src4" class="srcSentence">Retire/Wipe</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">You can issue a <embeddedLabel>Retire/Wipe</embeddedLabel> command to help secure a lost device or to retire a device from active use.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">
              <ui>Full wipe</ui> restores a device to its factory default settings, removing all company and user data and settings.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence">    The device is removed from Intune.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">
              <ui>Selective wipe</ui> removes company data from a device.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence">   The device is removed from Intune.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> The following table describes by platform what data is removed and the effect on data that remains on the device after a selective wipe.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Content Type</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Windows 8.1(enrolled as a mobile device) and Windows RT 8.1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Windows RT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">iOS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Android</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Android Samsung KNOX</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Company apps and associated data installed by <token>wit_firstref</token>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Files protected by EFS will have their key revoked and the user will not be able to open the files.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Will not remove company apps.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">Apps originally installed through the company portal are uninstalled.</caps:sentence>
                    <caps:sentence id="src22" class="srcSentence"> Company app data is removed.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Apps are uninstalled.</caps:sentence>
                    <caps:sentence id="src24" class="srcSentence"> Company app data is removed.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">App data from Microsoft apps that use mobile app management is removed.</caps:sentence>
                    <caps:sentence id="src26" class="srcSentence"> The app is not removed.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">Company apps optimized for Intune such as Microsoft Office apps or apps deployed using the  App Wrapping Tool or Intune SDK are removed along with their data.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">App data from apps that use mobile app management is removed.</caps:sentence>
                    <caps:sentence id="src29" class="srcSentence"> The app is not removed.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Company apps optimized for Intune such as Office apps or apps deployed using  the App Wrapping Tool or Intune SDK are removed along with their data.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">App data from apps that use mobile app management is removed.</caps:sentence>
                    <caps:sentence id="src32" class="srcSentence"> The app is not removed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Settings</caps:sentence>
                  </para>
                </TD>
                <TD colspan="6">
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Configurations that were set by <token>wit_nextref</token> policy are no longer enforced and users can change the settings.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Wi-Fi and VPN profile settings</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">Removed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">Removed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Not supported</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Removed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Removed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Removed</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Certificate profile settings</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Certificates removed and revoked.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Certificates removed and revoked.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Not supported</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Certificates removed and revoked.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Certificates revoked, but not removed.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Certificates removed and revoked.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">Management Agent</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">Not applicable.</caps:sentence>
                    <caps:sentence id="src51" class="srcSentence"> Management agent is built-in.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Not applicable.</caps:sentence>
                    <caps:sentence id="src53" class="srcSentence"> Management agent is built-in.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Not applicable.</caps:sentence>
                    <caps:sentence id="src55" class="srcSentence"> Management agent is built-in.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">Management profile is removed.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Device Administrator privilege is revoked.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">Device Administrator privilege is revoked.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Email</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">Removes email that is EFS enabled which includes the Mail app for Windows email and attachments.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">Not supported</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Email profiles that are provisioned through <token>wit_nextref</token> are removed and cached email on the device is deleted.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Email profiles that are provisioned through <token>wit_nextref</token> are removed and cached email on the device is deleted.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">Email  received by the Microsoft Outlook app for Android  app is removed.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">Email profiles that are provisioned through <token>wit_nextref</token> are removed and cached email on the device is deleted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">Azure Active Directory (AAD) Unjoin</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">AAD Record removed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">AAD Record removed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">AAD Record removed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">AAD Record removed</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <procedure>
            <title>
              <caps:sentence id="src73" class="srcSentence">To initiate a remote wipe from the <token>wit_adminconsole</token></caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">Select devices to be wiped:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src75" class="srcSentence">By user:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src76" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>All Users</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src77" class="srcSentence">Click the name of the user whose mobile device you want to wipe, and then click <ui>View Properties</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src78" class="srcSentence">On the <ui>Properties </ui> page for the user, click the <ui>Devices</ui> tab, and then click the name of the mobile device that you want to wipe.</caps:sentence>
                            <caps:sentence id="src79" class="srcSentence"> Use Ctrl+click to multi-select devices.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src80" class="srcSentence">By device:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src81" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>All Mobile Devices</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src82" class="srcSentence">Click the <ui>Devices</ui> tab, and then click the name of the mobile device that you want to wipe.</caps:sentence>
                            <caps:sentence id="src83" class="srcSentence"> Use Ctrl+click to multi-select devices.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">Click <ui>Retire/Wipe</ui> in the task bar.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">A message appears, prompting you to confirm whether you want to retire the device.</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">To perform a <embeddedLabel>Selective wipe</embeddedLabel> which only removes company apps and data, click <ui>Yes</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">To perform a <embeddedLabel>Full wipe</embeddedLabel> that erases all apps and data and returns the device to factory default settings, select <ui>Wipe the device before retiring</ui>.</caps:sentence>
                        <caps:sentence id="src88" class="srcSentence"> This action applies to all platforms except Windows 8.1.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src89" class="srcSentence">It takes less than 15 minutes for a wipe to propagate across all device types.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src90" class="srcSentence">Wiping EFS-enabled content</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src91" class="srcSentence">Selective wipe of EFS-encrypted content is supported by Windows 8.1 and Windows RT 8.1.</caps:sentence>
                <caps:sentence id="src92" class="srcSentence"> The following apply to a selective wipe of EFS-enabled content:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">Only apps and data that are protected by EFS using the same Internet domain as the <token>wit_nextref</token> account are selectively wiped.</caps:sentence>
                    <caps:sentence id="src94" class="srcSentence"> For more information, see <externalLink><linkText>Windows Selective Wipe for Device Data Management</linkText><linkUri>http://technet.microsoft.com/library/dn486874.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">If there are any changes are made to the domain associated with EFS, the changes can take up to 48 hours before apps and data using the new domain can be selectively wiped.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">Each domain that is registered with <token>wit_nextref</token> will be wiped.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src97" class="srcSentence">The data and apps that are currently supported by EFS selective wipe are:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">Mail app for Windows</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">Work Folders</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">Files and folders encrypted by EFS.</caps:sentence>
                    <caps:sentence id="src101" class="srcSentence"> For more information, see <externalLink><linkText>Best practices for the Encrypting File System</linkText><linkUri>http://support.microsoft.com/kb/223316</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src102" class="srcSentence">If your organization maintains its identity in Active Directory, it must use the Directory Sync (DirSync) tool to sync information into AAD for EFS selective wipe to work correctly.</caps:sentence>
                    <caps:sentence id="src103" class="srcSentence">  For more information on DirSync, see <externalLink><linkText>Directory Sync Scenario</linkText><linkUri>http://technet.microsoft.com/library/dn441212.aspx</linkUri></externalLink> in the Azure Active Directory documentation.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src104" class="srcSentence">Monitor retire, wipe and delete actions</caps:sentence>
            </title>
            <content>
              <procedure>
                <title></title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Reports</ui> &gt; <ui>Device History Reports</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">Provide a start and end date for the report, then click <ui>View Report</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence id="src107" class="srcSentence">The report provides a list of retire, wipe and delete actions taken on each device, and who initiated them.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
          <section address="BKMK_passcode">
            <title>
              <caps:sentence id="src108" class="srcSentence">Passcode Reset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src109" class="srcSentence">If a user forgets their passcode, you can help them by removing the passcode from a device or by forcing a new temporary passcode on a device.</caps:sentence>
                <caps:sentence id="src110" class="srcSentence"> The table below lists how passcode reset works on different mobile platforms.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src111" class="srcSentence">Platform</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src112" class="srcSentence">Passcode Reset</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src113" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src114" class="srcSentence">Supported for clearing the passcode from a device.</caps:sentence>
                        <caps:sentence id="src115" class="srcSentence"> Does not create a new temporary passcode.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src116" class="srcSentence">Android</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">Supported and a temporary passcode is created.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src118" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">Supported</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">
                          <token>winblue_winrt_2</token> and <token>win8RT_client_1</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src121" class="srcSentence">Not Supported</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src122" class="srcSentence">Windows 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src123" class="srcSentence">Not Supported</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <procedure>
                <title>
                  <caps:sentence id="src124" class="srcSentence">To reset the passcode on a mobile device remotely through the Microsoft Intune Console</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src125" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>All Devices</ui> &gt; <ui>All Mobile Devices</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">Click <ui>All Direct Managed Devices</ui> for devices enrolled to <token>wit_firstref</token> or <ui>All Exchange ActiveSync Managed Devices</ui>.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src127" class="srcSentence">You can also navigate to a device by user.</caps:sentence>
                          <caps:sentence id="src128" class="srcSentence"> Click <ui>All Users</ui> and on the properties page for the user, click the <ui>Devices</ui> tab, and then click the name of the mobile device that you want to wipe.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src129" class="srcSentence">In the list, click the device or devices that you want to lock, and then on the taskbar click <ui>Remote Tasks</ui> and select <ui>Passcode Reset</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src130" class="srcSentence">Remote Lock</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src131" class="srcSentence">If a user loses their device you can lock the device remotely.</caps:sentence>
                <caps:sentence id="src132" class="srcSentence"> The table below lists how remote lock works on different mobile platforms.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">Platform</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src134" class="srcSentence">Remote Lock</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src135" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src136" class="srcSentence">Supported</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src137" class="srcSentence">Android</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src138" class="srcSentence">Supported</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src139" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src140" class="srcSentence">Supported</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src141" class="srcSentence">
                          <token>winblue_winrt_2</token> and <token>win8RT_client_1</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src142" class="srcSentence">Supported if the current user of the device is the same user who enrolled the device.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src143" class="srcSentence">Windows 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src144" class="srcSentence">Supported if the current user of the device is the same user who enrolled the device.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <procedure>
                <title>
                  <caps:sentence id="src145" class="srcSentence">To lock a mobile device remotely through the Microsoft Intune Console</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src146" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>All Devices</ui> &gt; <ui>All Mobile Devices</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src147" class="srcSentence">Click <ui>All Direct Managed Devices</ui> for devices enrolled to <token>wit_firstref</token> or <ui>All Exchange ActiveSync Managed Devices</ui>.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src148" class="srcSentence">You can also navigate to a device by user.</caps:sentence>
                          <caps:sentence id="src149" class="srcSentence"> Click <ui>All Users</ui> and on the properties page for the user, click the <ui>Devices</ui> tab, and then click the name of the mobile device that you want to wipe.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src150" class="srcSentence">In the list, click the device or devices that you want to lock, and then on the taskbar click <ui>Remote Tasks</ui> and select <ui>Remote Lock</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="3dbec400-5d8a-47be-b892-7745811d9de2">Retire data and devices from Microsoft Intune management</link>
        <externalLink>
          <linkText>
            <caps:sentence id="src151" class="srcSentence">Windows Selective Wipe for Device Data Management</caps:sentence>
          </linkText>
          <linkUri>http://technet.microsoft.com/library/dn486874.aspx</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence id="src152" class="srcSentence">How to buy Intune</caps:sentence>
          </linkText>
          <linkUri>http://technet.microsoft.com/library/dn646949.aspx</linkUri>
        </externalLink>
      </relatedTopics>
    </developerHowToDocument>
  </caps:SxSSource>
</caps:SxS>