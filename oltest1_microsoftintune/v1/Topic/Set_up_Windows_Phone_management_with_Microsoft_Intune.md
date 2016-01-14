---
description: na
keywords: na
title: Set up Windows Phone management with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f
---
# Einrichten der Windows Phone-Verwaltung mit Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0a604f324c694ee705db618e2cc994e9" id="tgt1" class="tgtSentence">Bevor Sie mobile Windows Phone-Geräte mit <token>wit_nextref</token> verwalten können, müssen Sie die Verwaltungsanforderungen einrichten.</caps:sentence>
          <caps:sentence sentenceid="6f851c45e9fe79c5ab6de4130d2b9cbe" id="tgt2" class="tgtSentence"> Durch das Erstellen eines DNS CNAME können Benutzer sich leichter mit dem <token>wit_nextref</token>-Unternehmensportal verbinden.</caps:sentence>
          <caps:sentence sentenceid="5048746af5eac71abe898d904199556e" id="tgt3" class="tgtSentence"> Windows Phone 8.0 erfordert ein Symantec-Zertifikat zum Herstellen einer verschlüsselten IP-Verbindung zwischen Geräten und <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="7596d820b20382b1f595d4fa01fc958a" id="tgt4" class="tgtSentence"> Je nachdem, wie Benutzer auf das Unternehmensportal zugreifen, gilt dies möglicherweise auch für Windows Phone 8.1.</caps:sentence>
          <caps:sentence sentenceid="2d1734cd0fa2c65f906473cecceca448" id="tgt5" class="tgtSentence"> Ein Zertifikat ist auch zum Signieren von Branchen-Apps erforderlich.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="2a52668cbd9bfc247e2bf159f9d980ce" id="tgt6" class="tgtSentence">
                <embeddedLabel>Windows Phone 8.1</embeddedLabel>: Erfordert nur in den folgenden Fällen ein Zertifikat:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence sentenceid="e22b0f840d2e0467c16eb174f11e04f2" id="tgt7" class="tgtSentence">Benutzer laden das Unternehmensportal nicht aus dem Store herunter.</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="f0de3decc6ae84fd99714b0ad425c29d" id="tgt8" class="tgtSentence">Sie stellen Branchen-Apps ("quergeladene Apps") bereit.</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="323f02ea3fa5ad027c887ea625be0018" id="tgt9" class="tgtSentence">
                <embeddedLabel>Windows Phone 8</embeddedLabel>: Erforderlich </caps:sentence>
            </para>
          </listItem>
        </list>
        <mediaLink>
          <image xlink:href="b457bc08-2634-4137-86f6-5f7cc330fbd2"></image>
        </mediaLink>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="d4e96b071977754f0ffe26a9bede39c0" id="tgt10" class="tgtSentence">Vorbereiten der Verwaltung von Windows Phone-Mobilgeräten mit Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="37424f9fbd3c42659c22e62c71daf0f2" id="tgt11" class="tgtSentence">Die Setupanforderungen für die Verwaltung von Windows Phone-Mobilgeräten hängen davon ab, wie Sie die Geräte verwalten möchten.</caps:sentence>
            <caps:sentence sentenceid="42c1899193d3a45f4bb620920c6b9b20" id="tgt12" class="tgtSentence">  Das Festlegen von zwei CNAMEs in der DNS-Registrierung Ihres Unternehmens erleichtert die Registrierung für die Benutzer.</caps:sentence>
            <caps:sentence sentenceid="f5b7fd6292695d16931124513f401587" id="tgt13" class="tgtSentence"> Wenn Ihre Benutzer die Unternehmensportal-App aus dem Store herunterladen, müssen Sie nach dem Konfigurieren der DNS-Einstellungen nur noch das Unternehmensportal einrichten und den Benutzern erklären, wie sie sich registrieren können.</caps:sentence>
            <caps:sentence sentenceid="1ce89ba3e652aab3dc4cbc73697fd68e" id="tgt14" class="tgtSentence">  Für Windows Phone 8.0 oder für Windows Phone 8.1 mit Bereitstellung des Unternehmensportals benötigen Sie ein Symntec-Zertifikat zur Codesignatur der App.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="27a772f8b3aee6a88266de7b2f38dd01" id="tgt15" class="tgtSentence">Einrichten der Windows Phone-Registrierung mit Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt16" class="tgtSentence">
                      <embeddedLabel>Einrichten von <token>wit_nextref</token></embeddedLabel>
                      <br />Wenn nicht bereits geschehen,  bereiten Sie die Verwaltung mobiler Geräte vor, indem Sie die <externalLink><linkText>Autorität für die Verwaltung mobiler Geräte</linkText><linkUri>https://technet.microsoft.com/library/mt346013.aspx</linkUri></externalLink> auf <embeddedLabel>Microsoft Intune</embeddedLabel> festlegen.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9781b62d0e687e3d5e772f805a335d75" id="tgt17" class="tgtSentence">
                      <embeddedLabel>Festlegen eines DNS-Alias für die Adresse des Registrierungsservers</embeddedLabel> (optional)<br /> </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f560aa912f671a18f3703213593be7cb" id="tgt18" class="tgtSentence">Wenn ein DNS-Alias (CNAME-Datensatztyp) vorhanden ist, können Benutzer ihre Geräte einfacher registrieren, da der Servername bei der Registrierung bereits automatisch aufgefüllt wird.</caps:sentence>
                  </para>
                  <procedure>
                    <title>
                      <caps:sentence sentenceid="749993060a7e3a66e889394faf5c9e22" id="tgt19" class="tgtSentence">Überprüfen und Erstellen eines DNS CNAME</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt20" class="tgtSentence">Klicken Sie in der <externalLink target="_blank"><linkText>Intune-Verwaltungskonsole</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> auf <ui>Verwaltung</ui> &gt; <ui>Verwaltung mobiler Geräte</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="5471ca9a49d6463fbc7f3306fe385bd7" id="tgt21" class="tgtSentence">Geben Sie die URL der überprüften Domäne der Unternehmenswebsite in das Feld <ui>Verifizierten Domänennamen eingeben</ui>, und klicken Sie dann auf <ui>Test Auto-Detection</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="e7791f265c2e6ed258d1beb636e351c5" id="tgt22" class="tgtSentence">Erstellen Sie CNAME-Ressourceneinträge für die Domäne des Unternehmens.</caps:sentence>
                            <caps:sentence sentenceid="e38c4e5bb6340155dd5172a5b1971886" id="tgt23" class="tgtSentence"> Die CNAME-Ressourceneinträge müssen die folgenden Informationen enthalten:</caps:sentence>
                          </para>
                          <table border="1">
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt24" class="tgtSentence">TYP</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="7bac9dc63b9408f7043a63c902ca5bdf" id="tgt25" class="tgtSentence">Hostname</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="9a69c94d460695b849447f29c4698904" id="tgt26" class="tgtSentence">Verweist auf</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="c431a4425bc56080c868435c8d910f83" id="tgt27" class="tgtSentence">TTL</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="056301054c43f8bbea2090debfec16b1" id="tgt28" class="tgtSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence sentenceid="8e2237c00eca06c96d1d66c5a5b546c7" id="tgt29" class="tgtSentence">  <para>enterpriseenrollment.company_domain.com</para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="103f16169e6c5483d3c3522b5673024d" id="tgt30" class="tgtSentence">manage.microsoft.com
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="72ab9d0304d3e84c6aa2dd15eda282f2" id="tgt31" class="tgtSentence">1 Stunde</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="056301054c43f8bbea2090debfec16b1" id="tgt32" class="tgtSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt33" class="tgtSentence"> <para>enterpriseregistration.company_domain.com</para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="b8e596718f436b22e7d47c18522a0117" id="tgt34" class="tgtSentence">enterpriseregistration.windows.net
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="72ab9d0304d3e84c6aa2dd15eda282f2" id="tgt35" class="tgtSentence">1 Stunde</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                          <para>
                            <caps:sentence sentenceid="0ddb188e0c3d6f753fa556e387c3eedb" id="tgt36" class="tgtSentence">Wenn der Name Ihrer Unternehmens-Website beispielsweise contoso.com lautet, erstellen Sie einen CNAME in DNS, von dem EnterpriseEnrollment.contoso.com an manage.microsoft.com umgeleitet wird.</caps:sentence>
                            <caps:sentence sentenceid="74ebccfb9a34b27966e6e47a30e9a2ac" id="tgt37" class="tgtSentence"> Existieren mehrere überprüfte Domänen, erstellen Sie einen CNAME-Eintrag für jede Domäne.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="fc2c4794f88183cd526fc7be558726b6" id="tgt38" class="tgtSentence">
                                  <codeInline>manage.microsoft.com</codeInline> – Unterstützt eine Umleitung zum Intune-Dienst mit Domänenerkennung anhand des E-Mail-Domänennamens</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a2983dbe3d567d4058550acda540ca05" id="tgt39" class="tgtSentence">
                                  <codeInline>enterpriseregistration.windows.net</codeInline> – Unterstützt eine Arbeitsbereichverknüpfung für mobile Geräte.</caps:sentence>
                                <caps:sentence sentenceid="99fde62d77c6759ad6803da7822eab47" id="tgt40" class="tgtSentence"> Der bedingte Zugriff auf Windows 8.1 wird ebenfalls unterstützt.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                  <mediaLink>
                    <image xlink:href="33622fc8-d7ad-4f20-a4ec-c50de6a158bc"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a596843407babf6e4c25e584affedd4b" id="tgt41" class="tgtSentence">
                      <embeddedLabel>Zertifikatsverwaltung zur Unterstützung der App-Signierung</embeddedLabel>
                      <br />[Erforderlich für Windows Phone 8.0 und Windows Phone 8.1, da damit kein Zugriff auf den Windows Phone Store erfolgt und/oder keine Branchen-Apps benötigen werden]</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1ea59c51f5e88f231ce3342443a35380" id="tgt42" class="tgtSentence">Zur Unterstützung der Unternehmensportal-App für Windows Phone 8.0 und zur Bereitstellung von Unternehmens-Apps für Windows Phone 8.1 benötigen Sie ein <embeddedLabel>Symantec Enterprise Mobile Code Signing Certificate</embeddedLabel>.</caps:sentence>
                    <caps:sentence sentenceid="1973c953a5aedfde14cbef8d3a7448e3" id="tgt43" class="tgtSentence"> Sie können kein Zertifikat verwenden, das von Ihrer eigenen Zertifizierungsstelle ausgestellt wurde, da für Windows Phone-Geräte nur das Symantec-Zertifikat vertrauenswürdig ist.</caps:sentence>
                    <caps:sentence sentenceid="2ff6639b8ad24df47cc02757d66f1c8a" id="tgt44" class="tgtSentence"> Dieses Zertifikat ist für folgende Zwecke erforderlich:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="eed648e5bed91d657e01816fdb7be98c" id="tgt45" class="tgtSentence">Signieren einer Unternehmensportal-App zur Bereitstellung in <token>winphone8_client_1</token> für Registrierung und Telefonverwaltung</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a4104207177adb1ac885342c9c759d74" id="tgt46" class="tgtSentence">Signieren von Branchen-Apps eines Unternehmens, sodass <token>wit_nextref</token> sie für Windows Phones bereitstellen kann</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt47" class="tgtSentence">Weitere Informationen finden Sie unter <externalLink><linkText>Häufig gestellte Fragen zur Windows Phone-Mobilgeräteverwaltung</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_FAQ</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="37e3d99e42a049de76e0dfebd9dfb8f9" id="tgt48" class="tgtSentence">Mithilfe der folgenden Schritte können Sie die erforderlichen Zertifikate bereitstellen und die Unternehmensportal-App signieren.</caps:sentence>
                    <caps:sentence sentenceid="28646b41405959e87441d471b331ff11" id="tgt49" class="tgtSentence"> Sie benötigen ein Windows Phone Dev Center-Konto, und Sie müssen ein Symantec-Zertifikat erwerben.</caps:sentence>
                  </para>
                  <procedure expanded="false" address="BKMK_CodeSign">
                    <title>
                      <caps:sentence sentenceid="ff3c52f78f7a2aa39610b4221277e835" id="tgt50" class="tgtSentence">So rufen Sie ein Zertifikat ab und versehen das Unternehmensportal mit einer Codesignatur</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt51" class="tgtSentence">
                              <embeddedLabel>Anmelden beim Windows Phone Dev Center</embeddedLabel> <br />Registrieren Sie sich mithilfe von Unternehmenskontodaten beim <externalLink target="_blank"><linkText>Windows Phone Dev Center</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268442</linkUri></externalLink>, wenn Sie sich anmelden, um Ihr Unternehmenskonto zu erwerben.</caps:sentence>
                            <caps:sentence sentenceid="a261c9138f990d03116c76f848cafd13" id="tgt52" class="tgtSentence"> Diese Anforderung muss von einem Mitglied der Geschäftsleitung autorisiert werden, bevor Sie ein Codesignaturzertifikat erhalten.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt53" class="tgtSentence">
                              <embeddedLabel>Beziehen eines Symantec-Zertifikats für Unternehmen</embeddedLabel> <br />Erwerben Sie unter Verwendung Ihrer Symantec-ID ein Zertifikat von der <externalLink target="_blank"><linkText>Symantec-Website</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268441</linkUri></externalLink>.</caps:sentence>
                            <caps:sentence sentenceid="c139bb5145d959ef2cde38b0e3628817" id="tgt54" class="tgtSentence"> Nach dem Kauf des Zertifikats erhält die genehmigende Person in Ihrem Unternehmen, die Sie in Ihrem Windows Phone Dev Center-Konto bestimmt haben, eine E-Mail, in der die Genehmigung der Zertifikatanforderung angefordert wird.</caps:sentence>
                            <caps:sentence sentenceid="25dd18ac503217d095e40e9383a2e9c3" id="tgt55" class="tgtSentence"> Weitere Informationen zu den Anforderungen des Symantec-Zertifikats finden Sie unter <externalLink><linkText>Warum ist für Windows Phone ein Symantec-Zertifikat erforderlich?</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_Symantec</linkUri></externalLink> in den häufig gestellten Fragen zur Windows-Geräteregistrierung.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt56" class="tgtSentence">
                              <embeddedLabel>Importieren von Zertifikaten</embeddedLabel> <br />Nachdem die Anforderung genehmigt wurde, erhalten Sie eine E-Mail mit Anweisungen zum Importieren von Zertifikaten.</caps:sentence>
                            <caps:sentence sentenceid="203edf623515d6f2eae34af754786d57" id="tgt57" class="tgtSentence"> Führen Sie die Anweisungen in der E-Mail aus, um die Zertifikate zu importieren.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt58" class="tgtSentence">
                              <embeddedLabel>Überprüfen der importierten Zertifikate</embeddedLabel> <br />Um zu überprüfen, ob die Zertifikate einwandfrei importiert wurden, navigieren Sie zum Snap-In <ui>Zertifikate</ui>. Klicken Sie mit der rechten Maustaste auf <ui>Zertifikate</ui>, und wählen Sie anschließend <ui>Zertifikate suchen</ui>.</caps:sentence>
                            <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt59" class="tgtSentence"> Geben Sie „Symantec“ in das Feld <ui>Enthält</ui> ein, und klicken Sie auf <ui>Jetzt suchen</ui>.</caps:sentence>
                            <caps:sentence sentenceid="4f457d2e2b9d837831a16cf2dafd91fe" id="tgt60" class="tgtSentence"> Die importierten Zertifikate werden in den Ergebnissen angezeigt.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="52f7f33c-987f-48ad-b661-d826489044cd"></image>
                            </mediaLinkInline>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt61" class="tgtSentence">
                              <embeddedLabel>Exportieren eines Signaturzertifikats</embeddedLabel> <br />Wenn Sie überprüft haben, dass die Zertifikate vorhanden sind, können Sie die PFX-Datei exportieren, um das Unternehmensportal zu signieren.</caps:sentence>
                            <caps:sentence sentenceid="95b28e0eac464de8a1ea35219cdc8fd6" id="tgt62" class="tgtSentence"> Wählen Sie das Symantec-Zertifikat mit <ui>Beabsichtigter Zweck</ui> "Codesignatur" aus.</caps:sentence>
                            <caps:sentence sentenceid="9df574524024f4ac803c969217c4c6b1" id="tgt63" class="tgtSentence"> Klicken Sie mit der rechten Maustaste auf das Codesignaturzertifikat, und wählen Sie <ui>Exportieren</ui> aus.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="a5e198a5-7d2b-4797-bdfa-853a8e664b3c"></image>
                            </mediaLinkInline>
                          </para>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt64" class="tgtSentence">Wählen Sie im <ui>Assistenten zum Exportieren von Zertifikaten</ui> die Option <ui>Ja, privaten Schlüssel exportieren</ui> aus, und klicken Sie dann auf <ui>Weiter</ui>.</caps:sentence>
                            <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt65" class="tgtSentence"> Wählen Sie die Option <ui>Privater Informationsaustausch –PKCS #12 (.PFX)</ui> aus, und aktivieren Sie das Kontrollkästchen <ui>Möglichst alle Zertifikate im Zertifizierungspfad berücksichtigen</ui>.</caps:sentence>
                            <caps:sentence sentenceid="476c3dffb6ddcfdd6308dcf7ac393bb6" id="tgt66" class="tgtSentence"> Schließen Sie den Assistenten ab.</caps:sentence>
                            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt67" class="tgtSentence"> Weitere Informationen finden Sie unter <externalLink><linkText>Exportieren eines Zertifikats mit dem privaten Schlüssel</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=203031</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <embeddedLabel>
                              <caps:sentence sentenceid="09b777d4b84b7ca37eca8d47cb17a4f7" id="tgt68" class="tgtSentence">Herunterladen und Signieren der Unternehmensportal-App</caps:sentence>
                            </embeddedLabel>
                            <br />
                          </para>
                          <para>
                            <caps:sentence sentenceid="2fb11af53d6b4d40a30c696b128fe5fa" id="tgt69" class="tgtSentence">Damit die Windows Phone-Registrierung unterstützt wird, muss die Unternehmensportal-App für Windows Phone 8.0 signiert und in Intune hochgeladen werden.</caps:sentence>
                          </para>
                          <procedure expanded="true">
                            <title>
                              <caps:sentence sentenceid="5df8bc8d708ed06a1927b3b6dcff7f22" id="tgt70" class="tgtSentence">Windows Phone 8.0: Herunterladen und Signieren der Unternehmensportal-App </caps:sentence>
                            </title>
                            <steps class="ordered">
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt71" class="tgtSentence">
                                      <embeddedLabel>Herunterladen des Unternehmensportals</embeddedLabel> <br />Laden Sie das <externalLink target="_blank"><linkText>Intune-Unternehmensportal für Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink> aus dem Download Center herunter.</caps:sentence>
                                    <caps:sentence sentenceid="66a94af7ea41447f1131ef2d9f973fd4" id="tgt72" class="tgtSentence"> Der Standardinstallationspfad lautet <codeInline>C:\Program Files (x86)\Microsoft Corporation\Windows Intune Company Portal for Windows Phone</codeInline>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt73" class="tgtSentence">
                                      <embeddedLabel>Herunterladen des Windows Phone 8.0 SDK</embeddedLabel>
                                      <br />Laden Sie das <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink> herunter.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt74" class="tgtSentence">
                                      <embeddedLabel>Erstellen einer Codesignatur für die Unternehmensportal-App</embeddedLabel> <br />Verwenden Sie die App XAPSignTool, die Sie mit dem SDK heruntergeladen haben, um das Unternehmensportal mit der PFX-Datei zu signieren, die Sie anhand des Symantec-Zertifikats erstellt haben.</caps:sentence>
                                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt75" class="tgtSentence"> Weitere Informationen dazu finden Sie unter <externalLink target="_blank"><linkText>Signieren einer Unternehmens-App mit dem Tool XapSignTool</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=280195</linkUri></externalLink>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                            </steps>
                          </procedure>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt76" class="tgtSentence">
                              <embeddedLabel>Hochladen der App in <token>wit_nextref</token></embeddedLabel>
                              <br />Laden Sie die signierte Unternehmensportal-App-Datei und Ihr Codesignaturzertifikat hoch, um die App den Endbenutzern zur Verfügung zu stellen.</caps:sentence>
                          </para>
                          <list class="ordered">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt77" class="tgtSentence">Klicken Sie in der <externalLink target="_blank"><linkText>Intune-Verwaltungskonsole</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> auf <ui>Verwaltung</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="41ad10da17628099ea69f30e0bc238ba" id="tgt78" class="tgtSentence">Klicken Sie auf <ui>Signierte App-Datei signieren</ui>, und melden Sie sich mit Ihrer <token>wit_nextref</token>-Administrator-ID an.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt79" class="tgtSentence">Navigieren Sie auf der Seite <ui>Softwaresetup</ui> für <ui>Geben Sie den Speicherort der Softwaresetupdateien an</ui> zum Speicherort der codesignierten Unternehmensportal-App  (.xap für Windows Phone 8.0 oder .appx für Windows Phone 8.1).</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="a3dd3999c7c2f2311b445428e3279147" id="tgt80" class="tgtSentence">Wenn Sie <token>wit_nextref</token> auswerten und eine codesignierte App-Datei in ein <token>wit_nextref</token>-Testkonto hochladen, deaktivieren Sie das Kontrollkästchen <ui>Die vom codesignierten Beispiel-Symantec-Zertifikat signierte Unternehmensportal-App-Datei verwenden</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="699e0486160e2a34fb947dc0d669fb82" id="tgt81" class="tgtSentence">Fügen Sie die Zertifikatdatei (.pfx) hinzu, die Sie nach <ui>Codesignaturzertifikat</ui> exportiert haben, und erstellen Sie ein Kennwort für das Zertifikat.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt82" class="tgtSentence">Füllen Sie die Felder auf der Seite <ui>Softwarebeschreibung</ui> aus. Denken Sie daran, dass Benutzer diese Informationen auf ihren Geräten sehen, wenn sie Details zur App im Unternehmensportal aufrufen.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="2267545103c9e1387bf304a0df2c06f5" id="tgt83" class="tgtSentence">Schließen Sie den Assistenten ab.</caps:sentence>
                                <caps:sentence sentenceid="fa2ac8e896b35eb1e96d789e6f67fffc" id="tgt84" class="tgtSentence"> Benutzer, die ein Windows Phone 8.0-Gerät registrieren, erhalten nun die Unternehmensportal-App auf ihren Geräten bei der Registrierung.</caps:sentence>
                                <caps:sentence sentenceid="ba525c5963210483a84bfef0dd02203d" id="tgt85" class="tgtSentence"> Windows Phone 8.1-Benutzer können die Unternehmensportal-App mit der Speicherversion des Unternehmensportals installieren.</caps:sentence>
                                <caps:sentence sentenceid="d56409e2c2ed2fbf8715df89e747e428" id="tgt86" class="tgtSentence">  Wenn Windows Phone 8.1-Geräte im Windows Phone Store blockiert sind oder Sie mithilfe von Intune die Unternehmensportal-App bereitstellen möchten, laden Sie die Unternehmensportal-App für Windows Phone 8.1 (SSP.appx) herunter, und signieren sie.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt87" class="tgtSentence">
                      <embeddedLabel>Hinzufügen von Intune-Benutzern</embeddedLabel> <br />Der Eigentümer des mobilen Geräts muss dem Microsoft Intune-Kontoportal hinzugefügt werden, bevor Geräte registriert werden können.</caps:sentence>
                    <caps:sentence sentenceid="4ad3f37ced51ee31a6023786a31e0a36" id="tgt88" class="tgtSentence"> Melden Sie sich beim <externalLink><linkText>Microsoft Intune-Kontoportal</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=698854</linkUri></externalLink> an, klicken Sie auf <ui>Benutzer hinzufügen</ui>, und wählen Sie eine Option aus:</caps:sentence>
                  </para>
                  <para></para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="18c21fa550c6e43924af228a0679d742" id="tgt89" class="tgtSentence">
                          <embeddedLabel>Benutzer</embeddedLabel>: Zum Hinzufügen eines einzelnen Benutzers wählen Sie <ui>Neu</ui> &gt; <ui>Benutzer</ui> und geben in den Feldern <ui>Details</ui>, <ui>Rollen zuweisen</ui> und <ui>   Benutzerstandort einstellen</ui> Informationen an. Weisen Sie den Benutzer anschließend einer <ui>Gruppe</ui> zu.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a2f878d4f238f251d1ca75147c9c0fbf" id="tgt90" class="tgtSentence">
                          <embeddedLabel>Per Massenvorgang hinzufügen</embeddedLabel>: Erstellen Sie eine CSV-Datei (siehe bereitgestellte Beispieldateien), und importieren Sie diese ins Intune-Kontoportal.</caps:sentence>
                        <caps:sentence sentenceid="c1b650589e7e36a0c106e31a527a915b" id="tgt91" class="tgtSentence"> Geben Sie Rollen, den Speicherort und die Gruppe an, und erstellen Sie anschließend die Konten.</caps:sentence>
                        <caps:sentence sentenceid="310c151380683e4137bd81b5c16379fa" id="tgt92" class="tgtSentence"> Beispieldateien und leere CSV-Dateien können vom Microsoft Intune-Kontoportal heruntergeladen werden.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="665358b9ae967c6584e5f22475cbb77e" id="tgt93" class="tgtSentence">Sie können auch die Active Directory- oder Azure Active Directory-Synchronisierung aktivieren.</caps:sentence>
                    <caps:sentence sentenceid="ccabfe774f8edea6ef04ff48472298c4" id="tgt94" class="tgtSentence"> Weitere Informationen zur Integration anderer Azure Active Directory-Benutzer in Intune finden Sie unter <externalLink><linkText>Fahrplan zur Verzeichnissynchronisierung</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=511540</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9781b62d0e687e3d5e772f805a335d75" id="tgt95" class="tgtSentence">
                      <embeddedLabel>Erstellen von Gruppen </embeddedLabel> (optional)<br />Gruppen bieten Flexibilität für die Verwaltung von Geräten und Benutzern.</caps:sentence>
                    <caps:sentence sentenceid="507c76716449010dc59f1483e3964cd5" id="tgt96" class="tgtSentence"> Sie können die Gruppen so einrichten, wie es Ihren organisatorischen Anforderungen am besten entspricht, beispielsweise nach geografischem Standort, Abteilung oder Hardwareeigenschaften.</caps:sentence>
                    <caps:sentence sentenceid="e3d2410d4aed3acc53c4e7d50a0202e7" id="tgt97" class="tgtSentence">   Weitere Informationen finden Sie unter <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt98" class="tgtSentence">
                    <para>
                      <embeddedLabel>Hinzufügen von Richtlinien für Geräte</embeddedLabel> (optional)<br />Richtlinien sind Gruppen von Einstellungen zum Steuern der Features auf Geräten. Die meisten MDM-Richtlinien sind plattformspezifisch. Sie erstellen Richtlinien mithilfe von Vorlagen, in denen empfohlene oder angepasste Einstellungen enthalten sind, und stellen diese dann für Gruppen bereit. Weitere Informationen finden Sie unter <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para> </caps:sentence>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ebc4e07b040da274fbcd0bc615d552aa" id="tgt99" class="tgtSentence">
                      <embeddedLabel>Festlegen der Beschränkung für Registrierungen für das Gerät</embeddedLabel> (optional) <br />Um die Anzahl von mobilen Geräten zu beschränken, die ein Benutzer registrieren kann, melden Sie sich bei der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> an, klicken Sie auf <ui>Verwaltung</ui> &gt; <ui>Verwaltung mobiler Geräte</ui> &gt; <ui>Registrierungsregeln</ui>.</caps:sentence>
                    <caps:sentence sentenceid="81896f17af8e74876e83bdcbfb84232d" id="tgt100" class="tgtSentence"> Wählen Sie die maximale Anzahl der Geräte aus, die ein Benutzer registrieren kann, und klicken Sie dann auf <ui>Speichern</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="486bbd9b1c2d83f16fd091ae8a3e3110" id="tgt101" class="tgtSentence">
                      <embeddedLabel>Festlegen von Unternehmensportaleinstellungen </embeddedLabel>
                      <br /> Sie können das Intune-Unternehmensportal für Ihr Unternehmen anpassen.</caps:sentence>
                    <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt102" class="tgtSentence"> Klicken Sie in der <externalLink><linkText>Microsoft Intune-Verwaltungskonsole</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> auf <ui>Verwaltung</ui> &gt; <ui>Unternehmensportal</ui>.</caps:sentence>
                    <caps:sentence sentenceid="625a8686dac7b5297d90d5266d7fcd78" id="tgt103" class="tgtSentence"> Konfigurieren Sie Folgendes</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9bb4c85dfbafa8c61f627241bb21358c" id="tgt104" class="tgtSentence">Firmenname</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="16576d71cb733d359db3b6e40b97b228" id="tgt105" class="tgtSentence">Kontaktname für IT-Abteilung</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="965d8e507652fcc1b19d4b13823cf800" id="tgt106" class="tgtSentence">Telefonnummer der IT-Abteilung</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt107" class="tgtSentence">Weitere Informationen</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2ddf6ec5ba19603e0bbf4dd9dd16b1c5" id="tgt108" class="tgtSentence">URL der Datenschutzrichtlinie des Unternehmens</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="07c657dc49d79de1aa99cc410449492d" id="tgt109" class="tgtSentence">URL der Supportwebsite (nicht angezeigt)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ca75dc95767c2d020aba7b02bb2837c8" id="tgt110" class="tgtSentence">Websitename</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step address="BKMK_Terms">
                <content>
                  <tokenBlock>CPEnrollmentTermsAndConditions</tokenBlock>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt111" class="tgtSentence">
                      <embeddedLabel>Erläutern des Zugriffs auf Unternehmensressourcen über das Unternehmensportal</embeddedLabel>
                      <br />Ihre Benutzer müssen wissen, wie sie ihre Geräte registrieren können und was sie erwartet, wenn die Geräte in die Verwaltung eingebunden sind.</caps:sentence>
                    <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt112" class="tgtSentence">
                      <link xlink:href="48914533-f138-4dc0-8b93-4cea3ac61f7b">What to tell your end users about using Intune</link>
                    </caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="58f2e45a7f16fb7d9bb18f3e983eebf2" id="tgt113" class="tgtSentence">Bereitstellen der Unternehmensportal-App von Windows Phone 8.1</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a40f9fafcca406b45bc874831dbb4b58" id="tgt114" class="tgtSentence">Sie können die Unternehmensportal-App für Windows Phone 8.1-Geräte mit <token>wit_nextref</token> bereitstellen, statt sie über den Windows Phone Store zu installieren.</caps:sentence>
                <caps:sentence sentenceid="60e7e9dcd9deab69d4aefb99d1eb669f" id="tgt115" class="tgtSentence"> Dennoch müssen Sie die Windows Phone-Geräteregistrierung anhand der obigen Schritte mithilfe des Symantec-Zertifikats aktivieren.</caps:sentence>
                <caps:sentence sentenceid="f2855d100c99c8677c7ce473fb8bb0fe" id="tgt116" class="tgtSentence"> Anschließend müssen Sie die Windows Phone 8.1-Unternehmensportal-App herunterladen und sie mit Ihrem Symantec-Zertifikat signieren.</caps:sentence>
                <caps:sentence sentenceid="38239abcf1644ec61ea21beda72d8faa" id="tgt117" class="tgtSentence">  Dies ist nur erforderlich, wenn Ihre Benutzer nicht den Store des Unternehmens verwenden und Sie das Unternehmensportal für Windows Phone 8.1-Geräte bereitstellen möchten.</caps:sentence>
              </para>
              <procedure expanded="false" address="BKMK_WP81appx">
                <title>
                  <caps:sentence sentenceid="593063f388f896f2b7939233bc0b76d1" id="tgt118" class="tgtSentence">Schritte zum Herunterladen und Signieren der Windows Phone 8.1-Unternehmensportal-App für die Bereitstellung mit Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt119" class="tgtSentence">
                          <embeddedLabel>Herunterladen des Unternehmensportals</embeddedLabel> <br /></caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt120" class="tgtSentence">Laden Sie die <externalLink target="_blank"><linkText>Microsoft Intune-Unternehmensportal-App für Windows Phone 8.1</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink> aus dem Download Center herunter, und führen Sie die selbstextrahierende Datei (.exe) aus.</caps:sentence>
                        <caps:sentence sentenceid="915293ff28ecd13258a5c246d8ff93e6" id="tgt121" class="tgtSentence"> Diese Datei enthält zwei Dateien:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d3b17b87a0f03614ef445ef6e1871e7e" id="tgt122" class="tgtSentence">CompanyPortal.appx: Die Installations-App des Unternehmensportals für Windows Phone 8.1</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9b70becfcf3be271def18686c811a1d5" id="tgt123" class="tgtSentence">WinPhoneCompanyPortal.ps1: Ein PowerShell-Skript, das Sie verwenden können, um die Unternehmensportal-App-Datei zu signieren, sodass sie für Windows Phone 8.1-Geräte bereitgestellt werden kann</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt124" class="tgtSentence">
                          <embeddedLabel>Herunterladen des Windows Phone SDK</embeddedLabel>
                          <br />Laden Sie <externalLink target="_blank"><linkText>Windows Phone SDK 8.0</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink> herunter (http://go.microsoft.com/fwlink/?LinkId=268439), und installieren Sie das SDK auf Ihrem Computer.</caps:sentence>
                        <caps:sentence sentenceid="7c37c9028d2f59387e2b9f2db1452021" id="tgt125" class="tgtSentence"> Dieses SDK ist erforderlich, um ein Anwendungsregistrierungstoken zu generieren.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="def41a67e2ddf550a1efd2f9dcbec355" id="tgt126" class="tgtSentence">
                          <embeddedLabel>Generieren einer AETX-Datei</embeddedLabel>
                          <br />Generieren Sie aus der Symantec PFX-Datei eine Anwendungsregistrierungstoken-Datei (.aetx) mithilfe von AETGenerator.exe. AETGenerator.exe ist Teil von Windows Phone SDK 8.0.</caps:sentence>
                        <caps:sentence sentenceid="ad2cb60a6fa7c1facec37cfb7a9c337b" id="tgt127" class="tgtSentence"> Eine Anleitung zum Erstellen einer AETX-Datei finden Sie im Abschnitt über das <externalLink><linkText>Generieren eines Anwendungsregistrierungstokens für Windows Phone</linkText><linkUri>https://msdn.microsoft.com/library/windows/apps/jj735576.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="599f968755b3fd6fb4191c3386a799f0" id="tgt128" class="tgtSentence">
                          <embeddedLabel>Herunterladen des Windows SDK für Windows 8.1</embeddedLabel>
                          <br />Laden Sie das <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=613525</linkUri></externalLink> herunter (http://go.microsoft.com/fwlink/?LinkId=613525), und installieren Sie es.</caps:sentence>
                        <caps:sentence sentenceid="e052a473d1029072cf5b45d0ecd3934d" id="tgt129" class="tgtSentence"> Beachten Sie, dass das in der Unternehmensportal-App verwendete PowerShell-Skript den Standardinstallationsort <codeInline>${env:ProgramFiles(x86)}\Windows Kits\8.1</codeInline> nutzt.</caps:sentence>
                        <caps:sentence sentenceid="2b4b5bf4ef49b31264c4644aca27912f" id="tgt130" class="tgtSentence"> Wenn Sie die App an einem anderen Ort installieren möchten, beziehen Sie den Speicherort in einem Cmdlet-Parameter ein.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="c5aa190bef9dfa4cf52860037fb9a409" id="tgt131" class="tgtSentence">
                          <embeddedLabel>Codesignieren der App mithilfe von PowerShell</embeddedLabel>
                          <br />Öffnen Sie als Administrator <ui>Windows PowerShell</ui> auf dem Hostcomputer, auf dem Windows SDK mit dem Symantec Enterprise Mobile Code Signing Certificate installiert wurde. Navigieren Sie zur Datei "Sign-WinPhoneCompanyPortal.ps1", und führen Sie das Skript aus.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="e93b3fa481be3932aa08bd68c3deee70" id="tgt132" class="tgtSentence">Beispiel 1</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -AetxPath 'C:\signing\cert.aetx'</code>
                      <para>
                        <caps:sentence sentenceid="99b6b6e0e44a19e34c86098e5979a3f0" id="tgt133" class="tgtSentence">In diesem Beispiel wird die Datei "CompanyPortal.appx" unter "C:\temp\" signiert und die Datei "CompanyPortalEnterpriseSigned.appx" erstellt.</caps:sentence>
                        <caps:sentence sentenceid="e0571817898d04af0c95c719456cf5f3" id="tgt134" class="tgtSentence"> Das PFX-Kennwort "1234" wird verwendet und die Herausgeber-ID wird aus der PFX-Datei gelesen.</caps:sentence>
                        <caps:sentence sentenceid="0c83a38d77d189b78d21a6f71153363e" id="tgt135" class="tgtSentence"> Die Unternehmens-ID wird aus der Datei "cert.aetx" gelesen.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="a6b23ee7f9c084154997ea3bf5b4c1e3" id="tgt136" class="tgtSentence">Beispiel 2</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -PublisherId 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1' -EnterpriseId 1000000001</code>
                      <para>
                        <caps:sentence sentenceid="99b6b6e0e44a19e34c86098e5979a3f0" id="tgt137" class="tgtSentence">In diesem Beispiel wird die Datei "CompanyPortal.appx" unter "C:\temp\" signiert und die Datei "CompanyPortalEnterpriseSigned.appx" erstellt.</caps:sentence>
                        <caps:sentence sentenceid="b38e6ecb4a008c1d5ae7bcddb70adb6d" id="tgt138" class="tgtSentence"> Das PFX-Kennwort "1234" und die festgelegte Herausgeber-ID werden verwendet.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="bf987f0415d3fefd8fbfbb5a6ab3a60a" id="tgt139" class="tgtSentence">Parameter:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="2154f1323d71cabff7d84e69486cbb99" id="tgt140" class="tgtSentence">
                              <codeInline>-InputAppx</codeInline>: Der lokale Pfad zur Datei "CompanyPortal.appx" in einfachen Anführungszeichen.</caps:sentence>
                            <caps:sentence sentenceid="8e7c82dcb51ef0a29f4c91c6d48afda8" id="tgt141" class="tgtSentence"> Beispiel: 'C:\temp\CompanyPortal.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="db0f98a70046962795dda19d1353f7d7" id="tgt142" class="tgtSentence">
                              <codeInline>-OutputAppx</codeInline>: Der lokale Pfad und Dateiname für die signierte Unternehmensportal-App in einfachen Anführungszeichen.</caps:sentence>
                            <caps:sentence sentenceid="0403882cb14e21a75053b8fe46e4660f" id="tgt143" class="tgtSentence"> Beispiel: 'C:\temp\CompanyPortalEnterpriseSigned.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="37406b23da0c95feeadffe0ed2f2e2f2" id="tgt144" class="tgtSentence">
                              <codeInline>-PfxFilePath</codeInline>: Der lokale Pfad und Dateiname für die exportierte PFX-Datei mit dem Symantec-Zertifikat.</caps:sentence>
                            <caps:sentence sentenceid="cb7e1c17fd7fbccdfee34f6ec3517046" id="tgt145" class="tgtSentence"> Beispiel: 'C:\signing\cert.pfx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="608a28ced851bec9f91fd064f5951e1a" id="tgt146" class="tgtSentence">
                              <codeInline>-PfxPassword</codeInline>: Das Kennwort, das zum Signieren der PFX-Datei verwendet wird, in einfachen Anführungszeichen.</caps:sentence>
                            <caps:sentence sentenceid="a1c69f54fcc3343fbe05ee9e1b639a7b" id="tgt147" class="tgtSentence"> Beispiel: '1234'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="a2ae2bbf3241fcd3cbad4e21210007ae" id="tgt148" class="tgtSentence">
                              <codeInline>-AetxPath</codeInline>: Der lokale Pfad zur AETX-Datei, die zum Lesen der Unternehmens-ID verwendet wird, wenn das Argument "EnterpriseId" nicht definiert ist.</caps:sentence>
                            <caps:sentence sentenceid="8026272ac081154b279b2ec9d1f56295" id="tgt149" class="tgtSentence"> Dieses Argument oder EnterpriseId muss angegeben werden.</caps:sentence>
                            <caps:sentence sentenceid="92ed377af9bc50371ea5446337c47cdb" id="tgt150" class="tgtSentence"> Beispiel: 'C:\signing\cert.aetx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0054ce9e0acf26959d5f7755005669f8" id="tgt151" class="tgtSentence">
                              <codeInline>-PublisherId</codeInline>: Die Herausgeber-ID des Unternehmens.</caps:sentence>
                            <caps:sentence sentenceid="e57c41ca30767da4088e84d285ebea57" id="tgt152" class="tgtSentence"> Wenn sie nicht vorhanden ist, wird das Feld "Subject" von Symantec Enterprise Mobile Code Signing Certificate verwendet.</caps:sentence>
                            <caps:sentence sentenceid="447aa2f9d4781de497f6fe66f1dd35af" id="tgt153" class="tgtSentence"> Beispiel: 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0eaa511e60ba861b2b429991814e3b4e" id="tgt154" class="tgtSentence">
                              <codeInline>-SdkPath</codeInline>: Der Pfad zum Stammordner des Windows SDK für Windows 8.1.</caps:sentence>
                            <caps:sentence sentenceid="4e16b4deaf8c428580187b116de8d533" id="tgt155" class="tgtSentence"> Dieses Argument ist optional und wird standardmäßig auf "${env:ProgramFiles(x86)}\Windows Kits\8.1" gesetzt.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="72598cc79faa20a87ad1c8e33e9d7214" id="tgt156" class="tgtSentence">
                              <codeInline>-EnterpriseId</codeInline>: Die Unternehmens-ID.</caps:sentence>
                            <caps:sentence sentenceid="07968656625d1c14a856a4e62db43118" id="tgt157" class="tgtSentence"> Dieses Argument oder "AetxPath" muss angegeben werden.</caps:sentence>
                            <caps:sentence sentenceid="4180f108ac1f3ae2e8d9735c058f6773" id="tgt158" class="tgtSentence"> Wenn dieses Argument nicht angegeben ist, wird die Unternehmens-ID aus der AETX-Datei gelesen.</caps:sentence>
                            <caps:sentence sentenceid="1ff4112e83e346066d3e4ba0d4c33bc1" id="tgt159" class="tgtSentence"> Beispiel: 1000000001</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="78ed0e740ca082d18b5b55d5445d1cda" id="tgt160" class="tgtSentence">Stellen Sie die Unternehmensportal-App (SSP.appx) für Windows Phone 8.1 bereit.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence sentenceid="660dbabe465935d074e99c94422cbe4e" id="tgt161" class="tgtSentence">Die ssp.xap und das Unternehmensportal aus dem Speicher können beide gleichzeitig installiert werden. Dies kann für den Benutzer verwirrend sein.</caps:sentence>
                          <caps:sentence sentenceid="7b153146551f60db93bc0d7b4ee78bf9" id="tgt162" class="tgtSentence"> Damit alle Benutzer die ssp.xap verwenden, erstellen Sie eine blockierte App für die Speicherversion des Unternehmensportals.</caps:sentence>
                          <caps:sentence sentenceid="42234178a8dc0432f4f0234ce726c309" id="tgt163" class="tgtSentence"> Um zu erreichen, dass alle Windows Phone 8.1-Geräte nur die Speicherversion des Unternehmensportals verwenden, haben Sie drei Möglichkeiten:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="d21d43181a8ebfa6f82099e6abbea447" id="tgt164" class="tgtSentence">Wenn Sie keine Apps per Sideload übertragen und Windows Phone 8.0 nicht unterstützen müssen, laden Sie die signierte ssp.xap nicht herunter.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="11fc13be9f3cde7c629ce0337906461a" id="tgt165" class="tgtSentence">Wenn Sideload-Apps erforderlich sind und sich keine Windows Phone 8-Geräte registrieren, ändern Sie die automatisch erstellte ssp.xap-Bereitstellung von "Verfügbar" in "Deinstallieren".</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="14c0fdbc4a0ce4ce8ddfbda28f481f4e" id="tgt166" class="tgtSentence">Wenn Sideload-Apps installiert werden und Windows Phone 8.0-Geräte sich registrieren müssen und die ssp.xap benötigen, erstellen Sie eine neue Softwarebereitstellung der ssp.xap, und stellen Sie sie mit der Aktion <ui>Deinstallieren</ui> bereit.</caps:sentence>
                              <caps:sentence sentenceid="2ceab1c373f1181739ed568303dc2ba4" id="tgt167" class="tgtSentence"> Windows Phone 8.0-Geräte unterstützen nicht die erzwungene Installation oder Deinstallation von Anwendungen, d. h. sie ignorieren die Bereitstellung.</caps:sentence>
                              <caps:sentence sentenceid="3af88cba174c19fa141be3b55f0598c5" id="tgt168" class="tgtSentence"> Windows Phone 8.1-Geräte unterstützen den Deinstallationsvorgang und entfernen die ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0ae8e358ce25de11f47161cfaf786819" id="tgt169" class="tgtSentence">Ihr Codesignaturzertifikat von Symantec für Windows-Geräte erneuern</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="51bfdd2c469f2f32f7ee1784438cc90c" id="tgt170" class="tgtSentence">Das zur Verwaltung bestimmter mobiler Windows- und Windows Phone-Geräte verwendete Symantec-Zertifikat muss regelmäßig erneuert werden.</caps:sentence>
            <caps:sentence sentenceid="326cb7aa260d149bc539350181b33bac" id="tgt171" class="tgtSentence"> Für Windows Phone 8.0-Geräte sind für die Geräteregistrierung eine signierte Unternehmensportal-App und das Codesignaturzertifikat erforderlich.</caps:sentence>
            <caps:sentence sentenceid="80ae8b75cfe475eff3037cedfc65ee80" id="tgt172" class="tgtSentence"> Spätere Windows Phone-Geräte können die aus dem Store heruntergeladene Unternehmensportal-App verwenden.</caps:sentence>
            <caps:sentence sentenceid="0e1f6a8e9350b2b4e355406fb6b90232" id="tgt173" class="tgtSentence"> Zur Bereitstellung von Branchen-Apps ist auch ein codesigniertes Zertifikat erforderlich.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="779e8425c55023567c0632d6ab4473af" id="tgt174" class="tgtSentence">So wird das Symantec-Codesignaturzertifikat erneuert</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="02971f9aca16d5e2a7ce66fb3ca89d07" id="tgt175" class="tgtSentence">Suchen Sie nach einer Erneuerungs-E-Mail, die ungefähr 14 Tage vor Ablauf des Zertifikats von Symantec gesendet wurde.</caps:sentence>
                    <caps:sentence sentenceid="ea9c74b6105f1c78a125f30f5ae444a1" id="tgt176" class="tgtSentence"> Diese E-Mail enthält Anweisungen von Symantec zum Erneuern des Zertifikats für Ihr Unternehmen.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="bb5af1c3a6d60b4947f070de9780726c" id="tgt177" class="tgtSentence">Weitere Informationen zu Symantec-Zertifikaten finden Sie unter <externalLink><linkText>www.symantec.com</linkText><linkUri>http://www.symantec.com</linkUri></externalLink>, oder telefonisch unter 1-877-438-8776 oder + 1-650-426-3400.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8a20404fb2a9dceb5dc3641a00eb463b" id="tgt178" class="tgtSentence">Wechseln Sie zu der Website (z. B.: <externalLink><linkText>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkText><linkUri>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkUri></externalLink>), und melden Sie sich mit der Symantec-Herausgeber-ID und der mit dem Zertifikat verbundenen E-Mail-Adresse an.</caps:sentence>
                    <caps:sentence sentenceid="a9387d7047bd71af5ca17dc633e94791" id="tgt179" class="tgtSentence"> Denken Sie daran, den gleichen Computer für das Starten der Erneuerung zu verwenden, den Sie auch zum Herunterladen des Zertifikats verwenden werden.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d4099a7d6380929b7b5c6b5a6623ae09" id="tgt180" class="tgtSentence">Sobald die Erneuerung genehmigt und bezahlt wurde, können Sie das Zertifikat herunterladen.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="b922e0fb4a86449b6aff176e41af7e88" id="tgt181" class="tgtSentence">Installieren des aktualisierten Zertifikats für Windows Phone 8.0</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="444257c164a32b232b9ede0412edc362" id="tgt182" class="tgtSentence">Das neueste Windows Phone-Unternehmensportal können Sie hier herunterladen und signieren: <externalLink><linkText>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="84f8df8e69faaf38b6a258b5e17b3926" id="tgt183" class="tgtSentence">Öffnen Sie Ihre Intune-Verwaltungskonsole (<externalLink><linkText>https://admin.manage.microsoft.com</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink>), und wechseln Sie zu <ui>Admin</ui>, <ui>Verwaltung mobiler Geräte</ui> &gt; <ui>Windows Phone</ui>, und klicken Sie auf <ui>Signierte App hochladen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fd66cd717e159db47ce295d4bcd12623" id="tgt184" class="tgtSentence">Laden Sie das neu signierte Unternehmensportal hoch.</caps:sentence>
                    <caps:sentence sentenceid="6f3395584021182930fb87574e71da98" id="tgt185" class="tgtSentence"> Sie benötigen die neu signierte SSP.XAP-Datei und die neue PFX-Datei, die Sie von Symantec erhalten, oder das Anwendungsregistrierungstoken, das mit dieser neuen PFX-Datei erstellt wurde.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5101a1da5de5102b696fa683c6c7c620" id="tgt186" class="tgtSentence">Wenn das Hochladen abgeschlossen ist, entfernen Sie in der Intune-Verwaltungskonsole die alte Version des Unternehmensportals im Arbeitsbereich <ui>Software</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1d2af3b8610e8640021243c7527825f7" id="tgt187" class="tgtSentence">Signieren Sie alle Branchen-Apps erneut mit demselben Zertifikat, laden Sie sie hoch, und ersetzen Sie vorhandene Anwendungen.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="c1cf3e547f3444db486cda0bccd743ad" id="tgt188" class="tgtSentence">Das Bereitstellen einer signierten SSP.XAP-Datei ist derzeit die einzige Möglichkeit, das aktualisierte Codesignaturzertifikat bereitzustellen.</caps:sentence>
                  <caps:sentence sentenceid="615a79d1519ef0e08e059151c7c938f3" id="tgt189" class="tgtSentence"> Zur Unterstützung signierter Branchen-Apps müssen Sie eine Unternehmensportal-App signieren und hochladen, auch wenn die Benutzer die Unternehmensportal-App über den Store installieren.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="3761619c03e867047963ca0a54e469c8" id="tgt190" class="tgtSentence">Installieren des aktualisierten Zertifikats für Geräte mit Windows Phone 8.1 oder höher</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b524d5abe0e85f658b0662dc161112b8" id="tgt191" class="tgtSentence">Das neueste Windows Phone-Unternehmensportal können Sie im Download Center herunterladen und signieren: <externalLink><linkText>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="41ab81aedec29d904a088b53214e2e6b" id="tgt192" class="tgtSentence">Öffnen Sie Ihre <externalLink><linkText>Intune-Verwaltungskonsole</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink> (https://admin.manage.microsoft.com), und wechseln Sie zu <ui>Admin</ui> &gt; <ui>Verwaltung mobiler Geräte</ui> &gt; <ui>Windows Phone</ui>, und klicken Sie auf <ui>Signierte App hochladen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fd66cd717e159db47ce295d4bcd12623" id="tgt193" class="tgtSentence">Laden Sie das neu signierte Unternehmensportal hoch.</caps:sentence>
                    <caps:sentence sentenceid="6f3395584021182930fb87574e71da98" id="tgt194" class="tgtSentence"> Sie benötigen die neu signierte SSP.XAP-Datei und die neue PFX-Datei, die Sie von Symantec erhalten, oder das Anwendungsregistrierungstoken, das mit dieser neuen PFX-Datei erstellt wurde.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5101a1da5de5102b696fa683c6c7c620" id="tgt195" class="tgtSentence">Wenn das Hochladen abgeschlossen ist, entfernen Sie die alte Version des Unternehmensportals im Arbeitsbereich <ui>Software</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1ab4bf40c46f0ac064fb574c89e0f60e" id="tgt196" class="tgtSentence">Signieren Sie alle neuen und aktualisierten Unternehmens-Apps unter Verwendung des neuen Zertifikats.</caps:sentence>
                    <caps:sentence sentenceid="135e5abbaa26e9cd47fdb5b9fbaf2c5e" id="tgt197" class="tgtSentence"> Vorhandene Anwendungen müssen nicht erneut signiert und erneut bereitgestellt werden.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_FAQ">
        <title>
          <caps:sentence sentenceid="a8473d2d445d6121c874811a283e6f1e" id="tgt198" class="tgtSentence">Häufig gestellte Fragen zur Verwaltung mobiler Geräte für Microsoft Intune einschließlich der Verwaltung mit Configuration Manager 2012</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false" address="BKMK_Symantec">
            <title>
              <caps:sentence sentenceid="0acc04a99923ff487f1e62cc62ac9283" id="tgt199" class="tgtSentence">Warum erfordert Windows Phone ein Symantec-Zertifikat für die Verwaltung?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="bca5bdf78a9a87711a6a2f3191e339a6" id="tgt200" class="tgtSentence">Windows Phone steuert, wie Sie Apps installieren können.</caps:sentence>
                <caps:sentence sentenceid="aeca71661d91b31dd20f037d310b34d6" id="tgt201" class="tgtSentence"> Jeder Benutzer mit einem Microsoft-Konto kann Apps aus dem Windows Phone Store installieren. Unternehmen können ihre intern entwickelten Branchen-Apps über einen besonderen Prozess installieren oder per Sideload-Verfahren übertragen, das in der Windows Phone-Dokumentation beschrieben wird.</caps:sentence>
                <caps:sentence sentenceid="63c52d556e83a21fa24b077fe618d2ba" id="tgt202" class="tgtSentence"> Bei der Installation von Branchenanwendungen unterstützen Windows Phones nur eine spezielle Art von Symantec-Zertifikat.</caps:sentence>
                <caps:sentence sentenceid="f967bb0d3d96cb9455c59003bf2f1a63" id="tgt203" class="tgtSentence"> Sie können keine anderen gewerblich oder privat generiertes Zertifikat verwenden.</caps:sentence>
                <caps:sentence sentenceid="09cd94f170cf68ec7afe6f8b3f228614" id="tgt204" class="tgtSentence"> Diese Anforderung gilt für alle Mobilgeräteverwaltungslösungen, nicht nur Intune.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4486bedaf2aad8fbd8ce6308c36365dc" id="tgt205" class="tgtSentence">Das Symantec-Zertifikat erstellt ein Anwendungsregistrierungs-Token (AET).</caps:sentence>
                <caps:sentence sentenceid="cd7946b0d209a2874b077a3e4b85958c" id="tgt206" class="tgtSentence"> Das AET kann auf einem Gerät installiert werden, wenn das Gerät sich für die Verwaltung mobiler Geräte registriert, oder es kann Out-of-Band von einer sicheren Website oder aus einen E-Mail-Anhang installiert werden.</caps:sentence>
                <caps:sentence sentenceid="e23ee43b117aa2f05f7ce0678c65031b" id="tgt207" class="tgtSentence"> Administratoren müssen alle Branchen-Apps mit dem Symantec-Zertifikat signieren, mit den Tools aus dem <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268439</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="d9f30d299b5c3971eac4739d37396740" id="tgt208" class="tgtSentence"> Wenn Benutzer versuchen, Branchen-Apps zu installieren, vergleicht das Windows Phone-Betriebssystem die Signatur im AET mit der Signatur der App.</caps:sentence>
                <caps:sentence sentenceid="8a269fe729dc7c14c459805ff817eef8" id="tgt209" class="tgtSentence"> Wenn die Signaturen übereinstimmen, kann die Installation fortgesetzt werden.</caps:sentence>
                <caps:sentence sentenceid="e72acee76aeaa6415d939c088ceb8f84" id="tgt210" class="tgtSentence"> Wenn das AET nicht überprüft werden kann, schlägt die Installation fehl.</caps:sentence>
                <caps:sentence sentenceid="a4d47b612e312de7101ea5ec01510e5b" id="tgt211" class="tgtSentence"> Es gibt verschiedene Gründe dafür, dass das AET nicht überprüft werden kann:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fd645953ed631257d19883615b793f22" id="tgt212" class="tgtSentence">Das AET wurde nie auf dem Gerät installiert.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="16368cf359f2911f56f6321b92beef47" id="tgt213" class="tgtSentence">Das AET ist abgelaufen.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="71a1e04f27919212d81bb91fbcc26f01" id="tgt214" class="tgtSentence">Das AET wurde nicht mit demselben Symantec-Zertifikat erstellt, das zum Signieren der App verwendet wurde.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="a6aef39c4d509b2213305476b24cd130" id="tgt215" class="tgtSentence">Windows Phone erfordert nicht, dass das AET während der MDM-Registrierung vorhanden ist. Vor der November 2014-Version erforderte Intune jedoch das AET und eine signierte ssp.xap, da es keine andere Möglichkeit zum Installieren des AET und der ssp.xap außer während der Registrierung gab.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="c5579fc500647b65bf98f37f19979c94" id="tgt216" class="tgtSentence">Wie wird das AET für Intune Benutzer erstellt?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="5ae84604a7e2d71341406f67047c6ca3" id="tgt217" class="tgtSentence">Wenn Administratoren die .pfx-Datei für ihr Symantec-Zertifikat hochladen, erstellt Intune das AET automatisch und stellt es auf registrierten Windows Phones bereit.</caps:sentence>
                <caps:sentence sentenceid="3673950fa30fb4a5b214efc6c1ece8c8" id="tgt218" class="tgtSentence"> Es ist nicht erforderlich, dass Intune-Administratoren das AET Generator-Tool aus dem Windows Phone SDK verwenden.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="77fefb917a7ab6999763d45d4eab2972" id="tgt219" class="tgtSentence">Intune unterstützt nicht die manuelle Erstellung des AET und seine Out-of-Band-Bereitstellung.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="06f29a6979696756b4ca89ca6e4655c3" id="tgt220" class="tgtSentence">Welche Änderungen haben dazu geführt, dass nicht unbedingt ein Symantec-Zertifikat erforderlich ist?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="16a954d50815f14c2eaae99c548348e0" id="tgt221" class="tgtSentence">Für die November 2014-Version wurden Änderungen an Intune vorgenommen, um Szenarios zuzulassen, in denen Unternehmen nicht über ein Symantec-Zertifikat verfügen.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8e5785e0f2a407289b2b448597ee4ed2" id="tgt222" class="tgtSentence">Das Unternehmensportal für Windows Phone 8.1 kann aus dem Store installiert werden. D. h. es muss nicht mit einem Symantec-Zertifikat signiert sein und mit einem AET validiert werden.</caps:sentence>
                    <caps:sentence sentenceid="870b721c9c385fe3b369476a0ccb4c5e" id="tgt223" class="tgtSentence"> Stattdessen wird die App als Teil des Store-Veröffentlichungsprozesses validiert.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3fd9c84ead013cd036b409c5f6b4e687" id="tgt224" class="tgtSentence">Windows Phone 8.1-Geräte können sich mit oder ohne einen AET auf dem Telefon registrieren.</caps:sentence>
                    <caps:sentence sentenceid="17e8f2f82c4f4daa47f60466d31857ab" id="tgt225" class="tgtSentence"> Wenn ein AET verfügbar ist, wird er zum ersten Mal installiert, wenn das Gerät mit Intune synchronisiert wird.</caps:sentence>
                    <caps:sentence sentenceid="ab1784c5d6cb3c52abf66f14a2a0352a" id="tgt226" class="tgtSentence"> Wenn kein AET vorhanden ist, kann das Gerät weiterhin von Intune verwaltet werden. Benutzer können das Unternehmensportal aus dem Store installieren und die meisten Funktionen des Unternehmensportals ohne ein Symantec-Zertifikat zum Signieren von Apps verwenden.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="f9bff7cb4f98158765d890ba47c27592" id="tgt227" class="tgtSentence">Die Symantec-Anforderung für Windows Phone 8-Geräte besteht weiterhin.</caps:sentence>
                <caps:sentence sentenceid="968858e5bbf674e1176a63319dd99275" id="tgt228" class="tgtSentence"> Für Windows Phone 8-Geräte müssen die signierte ssp.xap und das AET während der Registrierung vorhanden sein. Andernfalls werden sie für die Registrierung blockiert.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="27f38a368b320d3bbda10e828f5db6a2" id="tgt229" class="tgtSentence">Welche Funktionen werden unterstützt, wenn ein Windows Phone 8.1-Gerät registriert wird, aber kein Symantec-Zertifikat vorhanden ist?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d37d81db57a8768a88d00a5b32137827" id="tgt230" class="tgtSentence">Wenn ein Windows Phone 8.1-Gerät registriert wird, aber kein Symantec-Zertifikat vorhanden ist, können Sie:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a6eff3471ecee6ba66f3a757e9dc7857" id="tgt231" class="tgtSentence">Richtlinien erstellen und sie an das Gerät weiterleiten</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="617b7bebf9b5e89394b404b407e3d5e9" id="tgt232" class="tgtSentence">Kontaktinformationen für die IT-Abteilung konfigurieren, die im Unternehmensportal anzeigt werden</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="878fb2365222c016787648a0d3ef3001" id="tgt233" class="tgtSentence">Deep Links im Speicher erstellen und für das Unternehmensportal bereitstellen</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ed637eb5906e5ebdc91f81d3053198a7" id="tgt234" class="tgtSentence">Links zu Webseiten erstellen und für das Unternehmensportal bereitstellen</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e95d654aba16b07959b72d850e5f12b7" id="tgt235" class="tgtSentence">Bedingungen erstellen, die von Benutzern akzeptiert werden müssen, bevor das Unternehmensportal verwendet werden kann</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="80ada9528124e15df4dd26935aa605ae" id="tgt236" class="tgtSentence">Das Einzige, was ohne ein Symantec-Zertifikat nicht möglich ist, ist Branchen-Apps bereitzustellen.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="a81bff7622c8e73171ad3e2b93dc1ca4" id="tgt237" class="tgtSentence">Der Intune Software Publisher überprüft nicht, ob Apps signiert sind, wenn Sie sie hochladen.</caps:sentence>
                  <caps:sentence sentenceid="46660005128f53bc64e6c7bceceb2bcd" id="tgt238" class="tgtSentence"> Wenn Sie nicht signierte Apps bereitstellen, schlagen sie fehl, wenn Benutzer versuchen, diese zu installieren.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="d959623c7541516bd9a781d53b0c4d3e" id="tgt239" class="tgtSentence">Was können Benutzer tun, wenn sie ein Unternehmensportal haben, jedoch kein Symantec-Zertifikat?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="552f4dae42c6b84b79e6bebb5d79ec29" id="tgt240" class="tgtSentence">Windows Phone 8.1-Geräte müssen nicht registriert werden, bevor Benutzer das Unternehmensportal aus dem Store installieren.</caps:sentence>
                <caps:sentence sentenceid="275b38084299a98feb7e0a323b5dd812" id="tgt241" class="tgtSentence"> Wenn das Gerät nicht registriert ist, werden Benutzer aufgefordert, es zu registrieren.</caps:sentence>
                <caps:sentence sentenceid="a65d8c8ad714514177dfcd664bc69b9c" id="tgt242" class="tgtSentence"> Durch Berühren der Eingabeaufforderung im Unternehmensportal gelangen Benutzer direkt zu <ui>Einstellungen / Arbeitsplatz</ui>, wo sie ihre Geräte registrieren können.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a47ea5cf9d9625766c7477800cd6d202" id="tgt243" class="tgtSentence">Benutzer können selbst ohne Registrierung des Geräts die folgenden Aktionen im Unternehmensportal durchführen, das aus dem Store installiert wurde:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="86a130c9193962978650feab26546162" id="tgt244" class="tgtSentence">Akzeptieren Sie die Bedingungen, die vom Administrator konfiguriert wurden, oder lehnen Sie sie ab.</caps:sentence>
                    <caps:sentence sentenceid="aedd567dbc376df8e6e4b11fb43e7996" id="tgt245" class="tgtSentence"> Wenn Benutzer die Bedingungen ablehnen, wird das Unternehmensportal geschlossen.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5b8adf835d42ecf17a11dcab8a95fa7d" id="tgt246" class="tgtSentence">Kontaktinformationen für die IT-Abteilung anzeigen</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="425b6b3da98781c5b55f481080080d5d" id="tgt247" class="tgtSentence">Alle registrierten Geräte anzeigen, einschließlich iOS-, Android- und Windows-Geräte</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="bf4492432aa4d31374f36fe6cb0db216" id="tgt248" class="tgtSentence">Deep Links zu Apps im Store verwenden</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5245e8a94087a5a2082528f421784aae" id="tgt249" class="tgtSentence">Weblinks verwenden, um Webseiten zu öffnen</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="681cef1de549baba59faf4f773c29f5e" id="tgt250" class="tgtSentence">Wenn das Gerät registriert ist, können Benutzer das Gerät in der Liste <ui>Meine Geräte</ui> anzeigen.</caps:sentence>
                <caps:sentence sentenceid="453ba15b346c9557a686cb0db7a346e4" id="tgt251" class="tgtSentence"> Nach der Registrierung unterliegt das Gerät allen bereitgestellten Intune-Richtlinien.</caps:sentence>
                <caps:sentence sentenceid="2b3bf3125ff7527a76fc76a2a4982d6f" id="tgt252" class="tgtSentence"> Geräte müssen registriert werden, um das AET zu erhalten und Branchen-Apps zu installieren.</caps:sentence>
                <caps:sentence sentenceid="274077dccf96d6b4d7e6e2ff6be0b8a9" id="tgt253" class="tgtSentence"> Ein nicht registriertes Gerät, das versucht, eine Branchen-App zu installieren, wird zur Registrierung weitergeleitet.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="44fc05b4e45d60fc7658f2f7bb9f722e" id="tgt254" class="tgtSentence">Das Einzige, was Benutzer nicht tun können, wenn das Unternehmen nicht über ein Symantec-Zertifikat verfügt, ist, vom Administrator bereitgestellt Branchen-Apps zu installieren.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="8908a0afb06ed65c1edef45b122baa65" id="tgt255" class="tgtSentence">Unser Unternehmen verfügt bereits über ein Zertifikat und hat Windows Phone 8.1-Geräte registriert.</caps:sentence>
              <caps:sentence sentenceid="cdd7ef49ee7488b490b74a567305aa8f" id="tgt256" class="tgtSentence"> Muss ich zusätzlich etwas tun, da das Unternehmensportal jetzt im Store verfügbar ist?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cdb72a02b423f4db13f9914d497fedf6" id="tgt257" class="tgtSentence">Die aktuelle ssp.xap aus dem Download Center funktioniert weiterhin auf Windows Phone 8.1-Geräten.</caps:sentence>
                <caps:sentence sentenceid="635f418afd05eff3c5a8c22f835f6426" id="tgt258" class="tgtSentence"> Sie können weiterhin Benutzer weiterleiten, um sich zu registrieren und das Unternehmensportal während der Installation abzurufen.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="5c9f54b558a579c725d95fa79d038f6c" id="tgt259" class="tgtSentence">Was sind die Vor- und Nachteile, wenn Benutzer das Unternehmensportal aus dem Store abrufen?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="b028aaa3d7589d6f1a8f4dcc51bc5886" id="tgt260" class="tgtSentence">Vorteile:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="44b59bd5003a52759f5badd8abe57c0c" id="tgt261" class="tgtSentence">Benutzer erhalten Deep Links und Weblinks, selbst wenn das Windows Phone 8.1-Gerät nicht registriert ist.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="930a4f8505ad69bd7f0d04a1e85b6a8f" id="tgt262" class="tgtSentence">Wenn Microsoft das Unternehmensportal aktualisiert, wird die Store-App automatisch ohne Herunterladen, Signieren und erneutes Bereitstellen der ssp.xap aktualisiert.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f59020828d42d1f89021c34991e5fb27" id="tgt263" class="tgtSentence">Die Dokumentation für Windows Phone 8.1-, iOS-, Android- und Windows-Benutzer ist konsistent: „Wechseln Sie zum Store, und installieren Sie das Unternehmensportal.“</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a8b1fc65f186cd804791e0063b4822e6" id="tgt264" class="tgtSentence">Benutzer sehen die App während sie Installiert wird und erhalten Registrierungsanweisungen, wenn sie geöffnet wird.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="c5e9cbdfd23494eade05650d2e315736" id="tgt265" class="tgtSentence">Nachteile:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="67b0cdf5eb7cc1353e29dc9091eeda50" id="tgt266" class="tgtSentence">Benutzer sehen ein Kontrollkästchen zum Installieren eines <ui>Unternehmens-Hub</ui>. Sie werden jedoch nicht zum Unternehmensportal in der App-Liste des Geräts weitergeleitet.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="527369e8b7bcd296bf39deeb7102bccf" id="tgt267" class="tgtSentence">Benutzer müssen keine benutzerdefinierten Bedingungen akzeptieren, bis sie das Unternehmensportal öffnen.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="e0670c64da4d7a389e3edc4f98074a3d" id="tgt268" class="tgtSentence">In den folgenden Situationen können Sie weiterhin Benutzer zur Registrierung und Installation der ssp.xap bei der Registrierung weiterleiten:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2e775f1961bb6cf07c5a85ae329a4f14" id="tgt269" class="tgtSentence">Wenn die Unternehmensblöcke auf den Store von Windows Phones zugreifen, müssen Benutzer die ssp.xap abrufen, die bei der Registrierung installiert wird.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c549b0bfebbc3da38fcb01ac665be91c" id="tgt270" class="tgtSentence">Wenn Benutzer keine Microsoft-Konten auf ihren Windows Phones konfiguriert haben, können sie nicht das Unternehmensportal aus dem Store installieren.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="21b30a7e587b3dbe09fdec247f457275" id="tgt271" class="tgtSentence">Wenn in der vorhandenen Dokumentation für die Windows Phone-Registrierung steht, dass der Benutzer zunächst zu "Einstellungen" &gt; "Arbeitsplatz" gehen soll, kann es dauern, bis die Dokumentation aktualisiert wird und die Benutzer zum Store weitergeleitet werden.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="fe8f3c69642c11e2b9ea6d84f0371765" id="tgt272" class="tgtSentence">Was ist der Unterschied zwischen de ssp.xap im Download Center und der App im Store?</caps:sentence>
            </title>
            <content>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9158d571d0ffe116fdd82a094e7beab5" id="tgt273" class="tgtSentence">Das Unternehmensportal im Store muss nicht durch ein zu installierendes Symantec-Zertifikat signiert werden.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ff8c41c93a55cc70906a725b57770f47" id="tgt274" class="tgtSentence">Das Unternehmensportal im Store stellt dem Benutzer die Bedingungen bereit, die ssp.xap im Download Center nicht.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="47295996a58c02577f305efe2c34562e" id="tgt275" class="tgtSentence">Das Unternehmensportal im Speicher ist eine .appx und keine .xap.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="b2e4b482c2464ea642f30472708b0fd4" id="tgt276" class="tgtSentence">Kann ich die Unternehmensportaldatei abrufen und sie an meine Benutzer weiterleiten, statt sie auf den Store zu verweisen?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt277" class="tgtSentence">Ja.</caps:sentence>
                <caps:sentence sentenceid="863d73f5079173aed48a39a775f609f7" id="tgt278" class="tgtSentence"> Die Unternehmensportal-App kann für die folgenden Betriebssysteme aus dem Download Center heruntergeladen werden:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="80ca961f21952f878b8688c0b28b72d1" id="tgt279" class="tgtSentence">Windows Phone 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615799</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="132a42035119c4b6819173ebaefee335" id="tgt280" class="tgtSentence">Windows Phone 8.0: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=268440</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4e458d4908dd91d3612a8e39fd1b9903" id="tgt281" class="tgtSentence">Windows 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615800</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615800</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="07a844f479ec1aa2a83c1de9c238a276" id="tgt282" class="tgtSentence">Können Unternehmen weiterhin das Support Tool for Windows Intune Trial Management of Windows Phone verwenden, wenn sie nicht über ein Symantec-Zertifikat verfügen, und müssen Benutzer weiterhin das Unternehmensportal aus dem Store installieren?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt283" class="tgtSentence">Ja.</caps:sentence>
                <caps:sentence sentenceid="8c24975691fabd85fb3ead253d3c9451" id="tgt284" class="tgtSentence"> Wenn Sie eine Machbarkeitsstudie durchführen müssen, die die Installation von Branchen-Apps beinhaltet, nutzt das Trial Management Tool die Store-Version des Unternehmensportals.</caps:sentence>
                <caps:sentence sentenceid="6b9cdd25078fdd8f3f3544de94cb24e6" id="tgt285" class="tgtSentence"> Da das AET aus dem Symantec-Zertifikat nicht mehr erforderlich ist, um Windows Phone 8.1-Geräte zu registrieren, können Unternehmen jedoch die App-Installation mit Deep Links zu Apps im Store testen.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e0b94b3beb8578f9a74f62aa274e8de8" id="tgt286" class="tgtSentence">Das Support Tool for Windows Intune Trial Management of Windows Phone ist nur für Testabonnements von Intune verfügbar.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="b423f1f2cd0cd14a02d5a88c115ce89e" id="tgt287" class="tgtSentence">Verwenden Sie nur die Trial Management Tool-Tests.</caps:sentence>
                  <caps:sentence sentenceid="a10570b481f6494ad67cbda562791b19" id="tgt288" class="tgtSentence"> Für mit dem AET aus dem Trial Management Tool registrierte Geräte müssen Sie die Registrierung aufheben und sie erneut registrieren, wenn das Symantec-Zertifikat für das Trial Management Tool nicht mehr verfügbar ist oder wenn das Unternehmen ein eigenes Symantec-Zertifikat für das Signieren von Apps erhält.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="9b2d8eef1c442aab1669ce98878685c9" id="tgt289" class="tgtSentence">Können Unternehmen ohne ein Symantec-Zertifikat beginnen und es später hinzufügen, selbst nachdem Windows Phone 8.1-Geräte registriert wurden?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt290" class="tgtSentence">Ja.</caps:sentence>
                <caps:sentence sentenceid="c542071594b3362f2e3a769ea372178b" id="tgt291" class="tgtSentence"> Selbst wenn Windows Phone 8.1-Geräte bereits registriert wurden, können Sie ein Symantec-Zertifikat erhalten, die ssp.xap signieren, sie und die pfx-Datei hochladen.</caps:sentence>
                <caps:sentence sentenceid="8e37b1ff45265fcef519fe877434c54e" id="tgt292" class="tgtSentence"> Intune generiert dann das AET.</caps:sentence>
                <caps:sentence sentenceid="0366852c1413d4a083ea32d99992e9dc" id="tgt293" class="tgtSentence"> Windows Phone 8.1-Geräte erhalten das AET bei der nächsten Synchronisierung, bis zu acht Stunden.</caps:sentence>
                <caps:sentence sentenceid="fee18265465e2efd8f40eba170049879" id="tgt294" class="tgtSentence"> Stellen Sie Branchen-Apps erst acht Stunden nach dem Hochladen der xap und pfx bereit.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Before you can manage Windows Phone mobile devices with <token>wit_nextref</token>, you have to set up management requirements.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Creating a DNS CNAME helps users connect to the <token>wit_nextref</token> company portal.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Windows Phone 8.0 requires a Symantec certificate to establish an encrypted IP connection between devices and <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Depending upon how users access the company portal, Windows Phone 8.1 might also.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> A certificate is also required to sign line-of-business apps.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">
                <embeddedLabel>Windows Phone 8.1</embeddedLabel> - Requires a certificate only if:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Users won't download the company portal from the Store</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src8" class="srcSentence">You'll deploy  line-of-business (AKA "sideloaded") apps</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">
                <embeddedLabel>Windows Phone 8</embeddedLabel> - Required </caps:sentence>
            </para>
          </listItem>
        </list>
        <mediaLink>
          <image xlink:href="b457bc08-2634-4137-86f6-5f7cc330fbd2"></image>
        </mediaLink>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Prepare to manage Windows Phone mobile devices with Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">Setup requirements for Window Phone mobile device management depend upon how you'll manage devices.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence">  Setting two CNAMEs in your company's DNS registration makes enrollment easier for uses.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> If your users will download the Company Portal app from the Store, then once you've configured DNS settings you just need to set up the Company Portal and inform users how to enroll.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence">  For Windows Phone 8.0, or Windows Phone 8.1 where you'll deploy the Company Portal, you'll need a Symntec certificate to code-sign the app.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src15" class="srcSentence">Set up Windows Phone enrollment with Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">
                      <embeddedLabel>Set up <token>wit_nextref</token></embeddedLabel> <br />If you haven’t already, prepare for mobile device management by  <externalLink><linkText>setting the mobile device management authority</linkText><linkUri>https://technet.microsoft.com/library/mt346013.aspx</linkUri></externalLink> as <embeddedLabel>Microsoft Intune</embeddedLabel>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">
                      <embeddedLabel>Set a DNS alias for the enrollment server address</embeddedLabel> (optional)<br /> </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">A DNS alias (CNAME record type) makes it easier users to enroll their devices by automatically populating the server name during enrollment.</caps:sentence>
                  </para>
                  <procedure>
                    <title>
                      <caps:sentence id="src19" class="srcSentence">Verify and create DNS CNAME</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src20" class="srcSentence">In the <externalLink target="_blank"><linkText>Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, click <ui>Administration</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src21" class="srcSentence">Type the URL of the verified domain of the company website in the <ui>Specify a verified domain name</ui> box and then click <ui>Test Auto-Detection</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src22" class="srcSentence">Create CNAME resource records for your company’s domain.</caps:sentence>
                            <caps:sentence id="src23" class="srcSentence"> The CNAME resource records must contain the following information:</caps:sentence>
                          </para>
                          <table border="1">
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src24" class="srcSentence">TYPE</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src25" class="srcSentence">Host Hame</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src26" class="srcSentence">Points to</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src27" class="srcSentence">TTL</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src28" class="srcSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence id="src29" class="srcSentence">  <para>enterpriseenrollment.company_domain.com </para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src30" class="srcSentence">manage.microsoft.com
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src31" class="srcSentence">1 Hour</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src32" class="srcSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence id="src33" class="srcSentence"> <para>enterpriseregistration.company_domain.com </para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src34" class="srcSentence">enterpriseregistration.windows.net
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src35" class="srcSentence">1 Hour</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                          <para>
                            <caps:sentence id="src36" class="srcSentence">For example, if your company’s website is contoso.com, you would create a CNAME in DNS that redirects EnterpriseEnrollment.contoso.com to manage.microsoft.com.</caps:sentence>
                            <caps:sentence id="src37" class="srcSentence"> If there is more than one verified domain, create a CNAME record for each domain.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src38" class="srcSentence">
                                  <codeInline>manage.microsoft.com</codeInline> – Supports a redirect to the Intune service with domain recognition from the email’s domain name</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src39" class="srcSentence">
                                  <codeInline>enterpriseregistration.windows.net</codeInline> – Supports workplace join for mobile devices.</caps:sentence>
                                <caps:sentence id="src40" class="srcSentence"> It also supports conditional access for Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                  <mediaLink>
                    <image xlink:href="33622fc8-d7ad-4f20-a4ec-c50de6a158bc"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">
                      <embeddedLabel>Certificate management to support app signing</embeddedLabel>
                      <br />[Required for Windows Phone 8.0 and Windows Phone 8.1 that won’t access the Windows Phone Store and/or need line-of-business apps.]</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">To support the Company Portal app for Windows Phone 8.0 and to deploy company apps to Windows Phone 8.1 you must get a <embeddedLabel>Symantec Enterprise Mobile Code Signing Certificate</embeddedLabel>.</caps:sentence>
                    <caps:sentence id="src43" class="srcSentence"> You cannot use a certificate issued by your own certification authority because only the Symantec certificate is trusted by Windows Phone devices.</caps:sentence>
                    <caps:sentence id="src44" class="srcSentence"> This certificate is required in order to:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Sign the Company Portal app for deployment to <token>winphone8_client_1</token> for enrollment and phone management</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Sign company line-of-business apps so <token>wit_nextref</token> can deploy them to Windows Phones</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">For more information, see <externalLink><linkText>Frequently Asked Questions about Windows Phone Mobile Device Management</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_FAQ</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">The steps below will help you get the required certificates and sign the company portal app.</caps:sentence>
                    <caps:sentence id="src49" class="srcSentence"> You will need a Windows Phone Dev Center account and then you will need to purchase a Symantec certificate.</caps:sentence>
                  </para>
                  <procedure expanded="false" address="BKMK_CodeSign">
                    <title>
                      <caps:sentence id="src50" class="srcSentence">To get a certificate and code-sign the Company Portal</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src51" class="srcSentence">
                              <embeddedLabel>Join the Windows Phone Dev Center</embeddedLabel> <br />Join the <externalLink target="_blank"><linkText>Windows Phone Dev Center</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268442</linkUri></externalLink> using corporate account information when logging in to purchase your company account.</caps:sentence>
                            <caps:sentence id="src52" class="srcSentence"> This request will need to be authorized by a company officer before you receive a code-signing certificate.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src53" class="srcSentence">
                              <embeddedLabel>Get a company Symantec certificate</embeddedLabel> <br />Purchase a certificate from the <externalLink target="_blank"><linkText>Symantec website</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268441</linkUri></externalLink> using your Symantec ID.</caps:sentence>
                            <caps:sentence id="src54" class="srcSentence"> After you purchase the certificate, the corporate approver whom you designated in your Windows Phone Dev Center account will receive an email asking for approval of the certificate request.</caps:sentence>
                            <caps:sentence id="src55" class="srcSentence"> For more information about the Symantec certificate requirement, see the <externalLink><linkText>Why Windows Phone requires a Symantec certificate?</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_Symantec</linkUri></externalLink> Windows device enrollment FAQ.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src56" class="srcSentence">
                              <embeddedLabel>Import certificates</embeddedLabel> <br />Once the request has been approved, you will receive an email containing instructions for importing certificates.</caps:sentence>
                            <caps:sentence id="src57" class="srcSentence"> Follow the instructions in the email to import the certificates.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src58" class="srcSentence">
                              <embeddedLabel>Verify certificates imported</embeddedLabel> <br />To verify that the certificates have been imported correctly, go to the <ui>Certificates</ui> snap-in, right-click <ui>Certificates</ui>, and select <ui>Find Certificates</ui>.</caps:sentence>
                            <caps:sentence id="src59" class="srcSentence"> In the <ui>Contains</ui> field, enter “Symantec”, and click <ui>Find Now</ui>.</caps:sentence>
                            <caps:sentence id="src60" class="srcSentence"> The certificates you imported should appear in the results.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="52f7f33c-987f-48ad-b661-d826489044cd"></image>
                            </mediaLinkInline>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">
                              <embeddedLabel>Export a signing certificate</embeddedLabel> <br />Having verified that the certificates are present, you can export the .pfx file to sign the company portal.</caps:sentence>
                            <caps:sentence id="src62" class="srcSentence"> Select the Symantec certificate with <ui>Intended purpose</ui> “code-signing.”</caps:sentence>
                            <caps:sentence id="src63" class="srcSentence"> Right-click the code-signing certificate and select <ui>Export</ui>.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="a5e198a5-7d2b-4797-bdfa-853a8e664b3c"></image>
                            </mediaLinkInline>
                          </para>
                          <para>
                            <caps:sentence id="src64" class="srcSentence">In the <ui>Certificate Export Wizard</ui>, select <ui>Yes, export the private key</ui> and then click <ui>Next</ui>.</caps:sentence>
                            <caps:sentence id="src65" class="srcSentence">
                              <ui>Select Personal Information Exchange –PKCS #12 (.PFX)</ui> and check <ui>Include all the certificates in the certification path if possible</ui>.</caps:sentence>
                            <caps:sentence id="src66" class="srcSentence"> Complete the wizard.</caps:sentence>
                            <caps:sentence id="src67" class="srcSentence"> For more information, see <externalLink><linkText>How to Export a Certificate with the Private Key</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=203031</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <embeddedLabel>
                              <caps:sentence id="src68" class="srcSentence">Download and sign the Company Portal app</caps:sentence>
                            </embeddedLabel>
                            <br />
                          </para>
                          <para>
                            <caps:sentence id="src69" class="srcSentence">Support for Windows Phone enrollment requires the Windows Phone 8.0 Company Portal app be signed and uploaded to Intune.</caps:sentence>
                          </para>
                          <procedure expanded="true">
                            <title>
                              <caps:sentence id="src70" class="srcSentence">Windows Phone 8.0: Download and sign the Company Portal app </caps:sentence>
                            </title>
                            <steps class="ordered">
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence id="src71" class="srcSentence">
                                      <embeddedLabel>Download the Company Portal</embeddedLabel> <br />Download the <externalLink target="_blank"><linkText>Intune Company Portal for Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink> from the Download Center.</caps:sentence>
                                    <caps:sentence id="src72" class="srcSentence"> The default installation location is <codeInline>C:\Program Files (x86)\Microsoft Corporation\Windows Intune Company Portal for Windows Phone</codeInline>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence id="src73" class="srcSentence">
                                      <embeddedLabel>Download the Windows Phone 8.0 SDK</embeddedLabel>
                                      <br />Download the <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence id="src74" class="srcSentence">
                                      <embeddedLabel>Code-sign the Company Portal app</embeddedLabel> <br />Use the XAPSignTool app downloaded with the SDK to sign the company portal with the .pfx file you created from the Symantec certificate.</caps:sentence>
                                    <caps:sentence id="src75" class="srcSentence"> For more information, see <externalLink target="_blank"><linkText>How to sign a company app by using XapSignTool</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=280195</linkUri></externalLink>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                            </steps>
                          </procedure>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src76" class="srcSentence">
                              <embeddedLabel>Upload the Company Portal app to <token>wit_nextref</token></embeddedLabel> <br />Upload the signed Company Portal app file and your code-signing certificate to make the app available to your end users.</caps:sentence>
                          </para>
                          <list class="ordered">
                            <listItem>
                              <para>
                                <caps:sentence id="src77" class="srcSentence">In the <externalLink target="_blank"><linkText>Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Administration</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src78" class="srcSentence">Click the <ui>Upload Signed App File</ui> and sign in with your <token>wit_nextref</token> Administrator ID.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src79" class="srcSentence">On the <ui>Software setup</ui> page for <ui>Specify the location of the software setup files</ui>, browse to the code-signed Company Portal app location (.xap for Windows Phone 8.0 or .appx for Windows Phone 8.1).</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src80" class="srcSentence">If you are evaluating <token>wit_nextref</token> and uploading a code-signed app file in a trial <token>wit_nextref</token> account, uncheck the <ui>Use the Company Portal App file signed by the sample Symantec code-signed certificate</ui> checkbox.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src81" class="srcSentence">Add the certificate (.pfx) file that you exported to <ui>Code-signing certificate</ui> and create a password for the certificate.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src82" class="srcSentence">On the <ui>Software description</ui> page, complete the fields remembering that users see this information on their devices when viewing details about the app in the Company Portal.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src83" class="srcSentence">Complete the wizard.</caps:sentence>
                                <caps:sentence id="src84" class="srcSentence"> Users who enroll a Windows Phone 8.0 device will now get the Company Portal app on their devices during enrollment.</caps:sentence>
                                <caps:sentence id="src85" class="srcSentence"> Windows Phone 8.1 users can install the Company Portal app from the store version of the Company Portal.</caps:sentence>
                                <caps:sentence id="src86" class="srcSentence">  If Windows Phone 8.1 devices are blocked from the Windows Phone Store or you want to deploy the Company Portal app using Intune, you must download and sign the Windows Phone 8.1 Company Portal (SSP.appx) app.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">
                      <embeddedLabel>Add Intune users</embeddedLabel> <br />The mobile device owner must be added to the Microsoft Intune Account Portal before devices can be enrolled.</caps:sentence>
                    <caps:sentence id="src88" class="srcSentence"> Log in to the <externalLink><linkText>Microsoft Intune Account Portal</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=698854</linkUri></externalLink>, click <ui>Add users</ui>, and select an option:</caps:sentence>
                  </para>
                  <para></para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">
                          <embeddedLabel>User</embeddedLabel>: To add a single user select <ui>New</ui> &gt; <ui>User</ui> and enter <ui>Details</ui>, <ui>Assign roles</ui>, <ui>Set user location</ui>, and then assign the user to a <ui>Group</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">
                          <embeddedLabel>Bulk add</embeddedLabel>: Create a .csv file (see samples files provided) and import it into the Intune Account Portal.</caps:sentence>
                        <caps:sentence id="src91" class="srcSentence"> Specify roles, location, and group, and then create the accounts.</caps:sentence>
                        <caps:sentence id="src92" class="srcSentence"> Sample and blank .csv files can be downloaded from the Microsoft Intune Account Portal.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">You can also enable Active Directory or Azure Active Directory synchronization.</caps:sentence>
                    <caps:sentence id="src94" class="srcSentence"> For more information about integrating other Azure Active Directory users with Intune, see <externalLink><linkText>Directory synchronization roadmap</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=511540</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">
                      <embeddedLabel>Create groups </embeddedLabel> (Optional)<br />Groups give flexibility for managing devices and users.</caps:sentence>
                    <caps:sentence id="src96" class="srcSentence"> You can set up groups to suit your organizational needs by geographic location, department, or hardware characteristics, for example.</caps:sentence>
                    <caps:sentence id="src97" class="srcSentence">   See <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <caps:sentence id="src98" class="srcSentence">
                    <para>
                      <embeddedLabel>Add policies for devices</embeddedLabel> (Optional)<br />Policies are groups of settings that control features on devices. Most MDM policies are platform specific. You create policies using templates  containing recommended or customized settings, and then deploy them to groups. See <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para> </caps:sentence>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">
                      <embeddedLabel>Set device enrollment limit</embeddedLabel> (Optional) <br />To limit the number of mobile devices a user can enroll, log in to the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Enrollment rules</ui>.</caps:sentence>
                    <caps:sentence id="src100" class="srcSentence"> Select the maximum number of devices a user can enroll and then click <ui>Save</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">
                      <embeddedLabel>Set Company Portal settings </embeddedLabel>
                      <br /> You can customize the Intune Company Portal for your company.</caps:sentence>
                    <caps:sentence id="src102" class="srcSentence"> In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Admin</ui> &gt; <ui>Company Portal</ui>.</caps:sentence>
                    <caps:sentence id="src103" class="srcSentence"> Configure the following</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src104" class="srcSentence">Company Name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src105" class="srcSentence">IT department contact name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src106" class="srcSentence">IT department phone number</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src107" class="srcSentence">Additional information</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src108" class="srcSentence">Company privacy statement URL</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src109" class="srcSentence">Support website URL (not displayed)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src110" class="srcSentence">Website name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step address="BKMK_Terms">
                <content>
                  <tokenBlock>CPEnrollmentTermsAndConditions</tokenBlock>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">
                      <embeddedLabel>Tell users how to get access to company resources with the company portal</embeddedLabel> <br />Your users will need to know how to enroll their devices and what to expect once they're brought into management.</caps:sentence>
                    <caps:sentence id="src112" class="srcSentence">
                      <link xlink:href="48914533-f138-4dc0-8b93-4cea3ac61f7b">What to tell your end users about using Intune</link>
                    </caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src113" class="srcSentence">Deploy the Windows Phone 8.1 Company Portal app</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src114" class="srcSentence">You can deploy the Company Portal app to Windows Phone 8.1 devices with <token>wit_nextref</token> instead of installing from the Windows Phone Store.</caps:sentence>
                <caps:sentence id="src115" class="srcSentence"> You must still enable Windows Phone device enrollment with the steps above using the Symantec certificate.</caps:sentence>
                <caps:sentence id="src116" class="srcSentence"> You must then download the Windows Phone 8.1 Company Portal app and sign it with your Symantec certificate.</caps:sentence>
                <caps:sentence id="src117" class="srcSentence">  This is only necessary if your users won't use the Company Store and you want to deploy the Company Portal to Windows Phone 8.1 devices.</caps:sentence>
              </para>
              <procedure expanded="false" address="BKMK_WP81appx">
                <title>
                  <caps:sentence id="src118" class="srcSentence">Steps to download and sign the Windows Phone 8.1 Company Portal app for deployment with Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">
                          <embeddedLabel>Download the Company Portal</embeddedLabel> <br /></caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">Download the <externalLink target="_blank"><linkText>Microsoft Intune Company Portal App for Windows Phone 8.1</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink> from the Download Center and run the self-extracting (.exe) file.</caps:sentence>
                        <caps:sentence id="src121" class="srcSentence"> This file contains two files:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src122" class="srcSentence">CompanyPortal.appx– The Company Portal installation app for Windows Phone 8.1</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src123" class="srcSentence">WinPhoneCompanyPortal.ps1 – A PowerShell script you can use to sign the Company Portal app file so it can be deployed to Windows Phone 8.1 devices</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src124" class="srcSentence">
                          <embeddedLabel>Download the Windows Phone SDK</embeddedLabel>
                          <br />Download the <externalLink target="_blank"><linkText>Windows Phone SDK 8.0</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=268439) and install the SDK to your computer.</caps:sentence>
                        <caps:sentence id="src125" class="srcSentence"> This SDK is needed to generate an application enrollment token.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">
                          <embeddedLabel>Generate an AETX file</embeddedLabel>
                          <br />Generate an application enrollment token (.aetx) file from the Symantec PFX file using AETGenerator.exe, part of Windows Phone SDK 8.0.</caps:sentence>
                        <caps:sentence id="src127" class="srcSentence"> For instructions on how to create an AETX file, see <externalLink><linkText>How to generate an application enrollment token for Windows Phone</linkText><linkUri>https://msdn.microsoft.com/library/windows/apps/jj735576.aspx</linkUri></externalLink></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src128" class="srcSentence">
                          <embeddedLabel>Download the Windows SDK for Windows 8.1</embeddedLabel>
                          <br />Download and install the <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=613525</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=613525).</caps:sentence>
                        <caps:sentence id="src129" class="srcSentence"> Note that the PowerShell script included with the Company Portal app uses the default install location, <codeInline>${env:ProgramFiles(x86)}\Windows Kits\8.1</codeInline>.</caps:sentence>
                        <caps:sentence id="src130" class="srcSentence"> If you install elsewhere, you must include the location in a cmdlet parameter.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src131" class="srcSentence">
                          <embeddedLabel>Code-sign the app using PowerShell</embeddedLabel>
                          <br />As an administrator, open <ui>Windows PowerShell</ui> on the host computer installed with the Windows SDK, the Symantec Enterprise Mobile Code Signing Certificate, navigate to the Sign-WinPhoneCompanyPortal.ps1 file and run the script.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src132" class="srcSentence">Example 1</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -AetxPath 'C:\signing\cert.aetx'</code>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">This example signs the CompanyPortal.appx at C:\temp\ and produces the CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence id="src134" class="srcSentence"> It would use PFX password 1234 and read the publisher ID from the PFX file.</caps:sentence>
                        <caps:sentence id="src135" class="srcSentence"> It reads the enterprise ID from the cert.aetx file as well.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src136" class="srcSentence">Example 2</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -PublisherId 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1' -EnterpriseId 1000000001</code>
                      <para>
                        <caps:sentence id="src137" class="srcSentence">This example signs the CompanyPortal.appx at C:\temp\ and produces the CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence id="src138" class="srcSentence"> It would use PFX password 1234 and use the publisher ID specified.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src139" class="srcSentence">Parameters:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src140" class="srcSentence">
                              <codeInline>-InputAppx</codeInline> – The local path to the CompanyPortal.appx file in single quotes.</caps:sentence>
                            <caps:sentence id="src141" class="srcSentence"> For example 'C:\temp\CompanyPortal.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src142" class="srcSentence">
                              <codeInline>-OutputAppx</codeInline> – The local path and file name for the signed Company Portal app in single quotes.</caps:sentence>
                            <caps:sentence id="src143" class="srcSentence"> For example, 'C:\temp\CompanyPortalEnterpriseSigned.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src144" class="srcSentence">
                              <codeInline>-PfxFilePath</codeInline> – The local path and file name for the exported PFX file of the Symantec certificate.</caps:sentence>
                            <caps:sentence id="src145" class="srcSentence"> For example, 'C:\signing\cert.pfx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src146" class="srcSentence">
                              <codeInline>-PfxPassword</codeInline> – The password used to sign the PFX file in single quotes.</caps:sentence>
                            <caps:sentence id="src147" class="srcSentence"> For example '1234'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src148" class="srcSentence">
                              <codeInline>-AetxPath</codeInline> – The local path to the .aetx file which is used for reading the enterprise ID if the 'EnterpriseId' argument is not defined.</caps:sentence>
                            <caps:sentence id="src149" class="srcSentence"> Either this argument or EnterpriseId must be provided.</caps:sentence>
                            <caps:sentence id="src150" class="srcSentence"> For example 'C:\signing\cert.aetx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src151" class="srcSentence">
                              <codeInline>-PublisherId</codeInline> - The Publisher ID of the enterprise.</caps:sentence>
                            <caps:sentence id="src152" class="srcSentence"> If absent, the 'Subject' field of the Symantec Enterprise Mobile Code Signing Certificate is used.</caps:sentence>
                            <caps:sentence id="src153" class="srcSentence"> For example, 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src154" class="srcSentence">
                              <codeInline>-SdkPath</codeInline> - The path to the root folder of the Windows SDK for Windows 8.1.</caps:sentence>
                            <caps:sentence id="src155" class="srcSentence"> This argument is optional and defaults to ${env:ProgramFiles(x86)}\Windows Kits\8.1.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src156" class="srcSentence">
                              <codeInline>-EnterpriseId</codeInline> - The enterprise ID.</caps:sentence>
                            <caps:sentence id="src157" class="srcSentence"> Either this argument or 'AetxPath' must be provided.</caps:sentence>
                            <caps:sentence id="src158" class="srcSentence"> If this argument is not provided, the enterprise ID is read from the AETX file.</caps:sentence>
                            <caps:sentence id="src159" class="srcSentence"> For example, 1000000001</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src160" class="srcSentence">Deploy the Windows Phone 8.1 Company Portal (SSP.appx) app.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence id="src161" class="srcSentence">The ssp.xap and the Company Portal from the store can both be installed at the same time, which can be confusing for users.</caps:sentence>
                          <caps:sentence id="src162" class="srcSentence"> To have all users using the ssp.xap, create a blocked app for the store version of the Company Portal.</caps:sentence>
                          <caps:sentence id="src163" class="srcSentence"> To have all Windows Phone 8.1 devices to use only the store version of the Company Portal, you have three choices:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence id="src164" class="srcSentence">If you won’t sideload apps and don’t need to support Windows Phone 8.0, don’t upload the signed ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src165" class="srcSentence">If sideloaded apps are needed, and if there are no Windows Phone 8 devices enrolling, change the automatically created ssp.xap deployment from “available” to “uninstall.”</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src166" class="srcSentence">If sideloaded apps need to be installed and Windows Phone 8.0 devices need to enroll and receive the ssp.xap, create a new software deployment of the ssp.xap and deploy it with the <ui>uninstall</ui> action.</caps:sentence>
                              <caps:sentence id="src167" class="srcSentence"> Windows Phone 8.0 devices don’t support forced install or uninstall of apps, so they will ignore the deployment.</caps:sentence>
                              <caps:sentence id="src168" class="srcSentence"> Windows Phone 8.1 devices support the uninstall action and will remove the ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src169" class="srcSentence">Renew your Symantec enterprise code-signing certificate for Windows devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src170" class="srcSentence">The Symantec certificate used to manage certain Windows and Windows Phone mobile devices must be renewed periodically.</caps:sentence>
            <caps:sentence id="src171" class="srcSentence"> For Windows Phone 8.0 devices, a signed Company Portal app and the code-signing certificate are needed for device enrollment.</caps:sentence>
            <caps:sentence id="src172" class="srcSentence"> Later Windows Phone devices can use the company portal app downloaded from the store.</caps:sentence>
            <caps:sentence id="src173" class="srcSentence"> A code-signing certificate is also be required for deploying line-of-business apps.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src174" class="srcSentence">How to renew the Symantec enterprise code-signing certificate</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">Look for a renewal email sent from Symantec approximately 14 days prior to certificate expiration.</caps:sentence>
                    <caps:sentence id="src176" class="srcSentence"> This email contains directions from Symantec about renewing your enterprise certificate.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">For additional information about Symantec certificates, visit <externalLink><linkText>www.symantec.com</linkText><linkUri>http://www.symantec.com</linkUri></externalLink> or call 1-877-438-8776 or 1-650-426-3400.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">Go to the website (example: <externalLink><linkText>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkText><linkUri>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkUri></externalLink>) and login with the Symantec Publisher ID and email addressed associated with the certificate.</caps:sentence>
                    <caps:sentence id="src179" class="srcSentence"> Remember to use the same machine for starting the renewal that you’ll use to download the certificate.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">Once the renewal is approved and paid for, download the certificate.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src181" class="srcSentence">How to install the updated certificate for Windows Phone 8.0</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">Download and sign the latest Windows Phone Company Portal located here: <externalLink><linkText>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">Open your Intune Administration Console (<externalLink><linkText>https://admin.manage.microsoft.com</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink>) and go to <ui>Admin</ui>, <ui>Mobile Device Management</ui> &gt; <ui>Windows Phone</ui> and click <ui>Upload Signed App</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">Upload the newly signed Company Portal.</caps:sentence>
                    <caps:sentence id="src185" class="srcSentence"> You’ll need the newly signed SSP.xap and the new .PFX file you received from Symantec or the application enrollment token that was created with this new .PFX file.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">When the upload is complete, remove the old Company Portal version in the <ui>Software</ui> workspace in the Intune Management Console.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">Sign all enterprise line-of-business apps again using the same certificate and upload and replace existing applications.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src188" class="srcSentence">Providing a signed SSP.xap file is currently the only way to provide the updated code signing certificate.</caps:sentence>
                  <caps:sentence id="src189" class="srcSentence"> To support signed line-of-business apps, you must sign and upload a Company Portal app even though your users will install the Company Portal app from the store.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src190" class="srcSentence">How to install the updated certificate for Windows Phone 8.1 and later devices</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">Download and sign the latest Windows Phone Company Portal from the Download Center located here: <externalLink><linkText>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">Open your <externalLink><linkText>Intune Administration Console</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink> (https://admin.manage.microsoft.com) and go to <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Windows Phone</ui> and click <ui>Upload Signed App</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src193" class="srcSentence">Upload the newly signed Company Portal.</caps:sentence>
                    <caps:sentence id="src194" class="srcSentence"> You’ll need the newly signed SSP.xap and the new .PFX file you received from Symantec or the Application enrollment token that was created with this new .PFX file.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">When the upload is complete, remove the old Company Portal version in the <ui>Software </ui> workspace.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">Sign all new and any updated enterprise line-of-business apps using the new certificate.</caps:sentence>
                    <caps:sentence id="src197" class="srcSentence"> Existing applications do not need to be resigned and redeployed.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_FAQ">
        <title>
          <caps:sentence id="src198" class="srcSentence">Frequently asked questions about mobile device management for Microsoft Intune including management with Configuration Manager 2012</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false" address="BKMK_Symantec">
            <title>
              <caps:sentence id="src199" class="srcSentence">Why does Windows Phone require a Symantec certificate for management?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src200" class="srcSentence">Windows Phone controls how you can install apps.</caps:sentence>
                <caps:sentence id="src201" class="srcSentence"> Any user with a Microsoft account can install apps from the Windows Phone store, or companies can install or sideload their internally developed line of business (LOB) apps using a special process described in the Windows Phone documentation.</caps:sentence>
                <caps:sentence id="src202" class="srcSentence"> When installing LOB apps, Windows Phones trust only one special type of certificate issued by Symantec.</caps:sentence>
                <caps:sentence id="src203" class="srcSentence"> You cannot use any other commercially or privately generated certificate.</caps:sentence>
                <caps:sentence id="src204" class="srcSentence"> This requirement is true for all mobile device management solutions, not just Intune.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src205" class="srcSentence">The Symantec certificate creates an application enrollment token (AET).</caps:sentence>
                <caps:sentence id="src206" class="srcSentence"> The AET can be installed on a device when the device enrolls for mobile device management, or it can be installed out-of-band from a secure website or from an email attachment.</caps:sentence>
                <caps:sentence id="src207" class="srcSentence"> Administrators must sign every LOB app with the Symantec certificate, using the tools provided in the <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268439</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src208" class="srcSentence"> When users attempt to install LOB apps, the Windows Phone operating system checks the signature in the AET against the signature on the app.</caps:sentence>
                <caps:sentence id="src209" class="srcSentence"> If the signatures match, the installation is allowed to proceed.</caps:sentence>
                <caps:sentence id="src210" class="srcSentence"> If the AET cannot be verified, installation fails.</caps:sentence>
                <caps:sentence id="src211" class="srcSentence"> There are several reasons the AET might not be verified:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">The AET was never installed on the device</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">The AET has expired</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">The AET was not created using the same Symantec certificate used to sign the app</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src215" class="srcSentence">Windows Phone does not require that the AET be present during MDM enrollment, but prior to the November 2014 release, Intune required the AET and a signed ssp.xap because there was no other way to install the AET and ssp.xap except during enrollment.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src216" class="srcSentence">How is the AET created for Intune users?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src217" class="srcSentence">When administrators upload the .pfx file for their Symantec certificate, Intune automatically creates the AET and deploys it to enrolled Windows Phones.</caps:sentence>
                <caps:sentence id="src218" class="srcSentence"> It is not necessary for Intune admins to use the AET Generator tool in the Windows Phone SDK.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src219" class="srcSentence">Intune does not support manually creating the AET and deploying it out-of-band.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src220" class="srcSentence">What changes happened to reduce the requirement for a Symantec certificate?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src221" class="srcSentence">For the November 2014 release, Intune made changes to allow for scenarios where companies do not have a Symantec certificate.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src222" class="srcSentence">The Company Portal for Windows Phone 8.1 is available to install from the store, so it needn’t be signed with a Symantec certificate and validated against an AET.</caps:sentence>
                    <caps:sentence id="src223" class="srcSentence"> Instead, the app is validated as part of the store publishing process.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">Windows Phone 8.1 devices can enroll with or without an AET on the phone.</caps:sentence>
                    <caps:sentence id="src225" class="srcSentence"> If an AET is available, it will be installed the first time the device synchronizes with Intune.</caps:sentence>
                    <caps:sentence id="src226" class="srcSentence"> If there is no AET, the device can still be managed by Intune, and users can install the Company Portal from the store and use most features of the Company Portal without a Symantec certificate to sign apps.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src227" class="srcSentence">There are no changes to the Symantec requirement for Windows Phone 8 devices.</caps:sentence>
                <caps:sentence id="src228" class="srcSentence"> Windows Phone 8 devices must have the signed ssp.xap and the AET present during enrollment or they will be blocked from enrolling.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src229" class="srcSentence">What functionality is supported if a Windows Phone 8.1 device is enrolled but there is no Symantec certificate?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src230" class="srcSentence">If a Windows Phone 8.1 device is enrolled but there’s no Symantec certificate, you can:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src231" class="srcSentence">Create policies and push them to the device</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">Configure contact information for the IT department that will shows in the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src233" class="srcSentence">Create deep links to the store and deploy them to the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src234" class="srcSentence">Create links to web pages and deploy them to the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src235" class="srcSentence">Create terms and conditions that must be accepted by users before they can use the Company Portal</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src236" class="srcSentence">The one thing you cannot do without a Symantec certificate is deploy LOB apps.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src237" class="srcSentence">The Intune Software Publisher does not verify that apps are signed when you upload them.</caps:sentence>
                  <caps:sentence id="src238" class="srcSentence"> If you deploy unsigned apps, they will fail when users try to install them.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src239" class="srcSentence">What can users do if they have the Company Portal but there is no Symantec certificate?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src240" class="srcSentence">Windows Phone 8.1 devices don’t have to be enrolled before users install the Company Portal from the store.</caps:sentence>
                <caps:sentence id="src241" class="srcSentence"> If the device is not enrolled, users are prompted to enroll.</caps:sentence>
                <caps:sentence id="src242" class="srcSentence"> Touching the prompt in the Company Portal takes users directly to <ui>Settings / Workplace</ui> where they can enroll their devices.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src243" class="srcSentence">Even without enrolling the device, uses can perform the following actions with the Company Portal installed from the store:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">Accept or decline any terms and conditions configured by the admin.</caps:sentence>
                    <caps:sentence id="src245" class="srcSentence"> If users decline the terms and conditions, the Company Portal closes.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src246" class="srcSentence">View the contact information for the IT department</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src247" class="srcSentence">View any enrolled devices including iOS, Android, and Windows devices</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src248" class="srcSentence">Use deep links to apps in the store</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src249" class="srcSentence">Use web links to open web pages</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src250" class="srcSentence">With the device enrolled, users can view the device in the <ui>My Devices</ui> list.</caps:sentence>
                <caps:sentence id="src251" class="srcSentence"> Once enrolled, the device is subject to any deployed Intune policies.</caps:sentence>
                <caps:sentence id="src252" class="srcSentence"> Devices must be enrolled to get the AET and install LOB apps.</caps:sentence>
                <caps:sentence id="src253" class="srcSentence"> An unenrolled device trying to install an LOB app will be directed to enroll.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src254" class="srcSentence">The only thing users cannot do if the company does not have a Symantec certificate is install LOB apps deployed by the admin.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src255" class="srcSentence">Our company already has a certificate and has been enrolling Windows Phone 8.1 devices.</caps:sentence>
              <caps:sentence id="src256" class="srcSentence"> Do I have to do anything different now that the Company Portal is available in the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src257" class="srcSentence">The current ssp.xap from the Download Center still works on Windows Phone 8.1 devices.</caps:sentence>
                <caps:sentence id="src258" class="srcSentence"> You can continue to direct users to enroll and get the company portal during installation.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src259" class="srcSentence">What are the advantages and disadvantages of users getting the Company Portal from the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src260" class="srcSentence">Advantages:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src261" class="srcSentence">Users get deep links and web links, even if the Windows Phone 8.1 device isn’t enrolled</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src262" class="srcSentence">When Microsoft updates the Company Portal, the store app updates automatically without your downloading, signing, and redeploying the ssp.xap</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src263" class="srcSentence">Documentation for Windows Phone 8.1, iOS, Android, and Windows users is consistent: “Go to the store and install the Company Portal.”</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src264" class="srcSentence">Users see the app as it installs and get enrollment instructions when it opens</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src265" class="srcSentence">Disadvantages:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src266" class="srcSentence">Users see a checkbox to install a “<ui>company hub</ui>” but nothing directs them to the Company Portal in the device’s app list</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src267" class="srcSentence">Users aren’t required to accept custom terms and conditions until they open the Company Portal</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src268" class="srcSentence">In the following circumstances, you can continue directing users to enroll and have the ssp.xap installed during enrollment:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src269" class="srcSentence">If the company blocks access to the store from Windows Phones, users must get the ssp.xap installed during enrollment.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src270" class="srcSentence">If users do not have Microsoft accounts configured on their Windows Phones, they will not be able to install the Company Portal from the store.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src271" class="srcSentence">If the existing documentation for Windows Phone enrollment tells them to go to Settings, Workplace first, it may take a while to update the docs and direct users to the store.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src272" class="srcSentence">What’s the difference between the ssp.xap on the Download Center and the app in the store?</caps:sentence>
            </title>
            <content>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src273" class="srcSentence">The Company Portal in the store does not have to be signed by a Symantec certificate to be installed</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src274" class="srcSentence">The Company Portal in the store presents the terms and conditions to the user but the ssp.xap on the Download Center doesn’t</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src275" class="srcSentence">The Company Portal in the store is an .appx instead of a .xap</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src276" class="srcSentence">Can I get the Company Portal file and push it to my users instead of sending them to the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src277" class="srcSentence">Yes.</caps:sentence>
                <caps:sentence id="src278" class="srcSentence"> The Company Portal app can be downloaded for the following operating systems from the Download Center:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">Windows Phone 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615799</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src280" class="srcSentence">Windows Phone 8.0 : <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=268440</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src281" class="srcSentence">Windows 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615800</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615800</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src282" class="srcSentence">Can companies still use the Support Tool for Windows Intune Trial Management of Windows Phone if they don’t have a Symantec certificate, and still have users install the Company Portal from the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src283" class="srcSentence">Yes.</caps:sentence>
                <caps:sentence id="src284" class="srcSentence"> If you need to do a proof of concept that includes installation of LOB apps, the trial management tool works with the store version of the company portal.</caps:sentence>
                <caps:sentence id="src285" class="srcSentence"> Because the AET from the Symantec certificate is no longer required to enroll Windows Phone 8.1 devices, however, companies can test app installation using deep links to apps in the store.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src286" class="srcSentence">The Support Tool for Windows Intune Trial Management of Windows Phone is only for trial subscriptions of Intune.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src287" class="srcSentence">Only use the trial management tool testing.</caps:sentence>
                  <caps:sentence id="src288" class="srcSentence"> Devices enrolled with the AET from the trial management tool must unenroll and reenroll if the Symantec certificate for the trial management tool is no longer available, or if the company obtains its own Symantec certificate for signing apps.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src289" class="srcSentence">Can companies start without any Symantec certificate and then add one later, even after Windows Phone 8.1 devices have enrolled?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src290" class="srcSentence">Yes.</caps:sentence>
                <caps:sentence id="src291" class="srcSentence"> Even if Windows Phone 8.1 devices have already enrolled, you can get a Symantec certificate, sign the ssp.xap, and upload it and the pfx file.</caps:sentence>
                <caps:sentence id="src292" class="srcSentence"> Intune will then generate the AET.</caps:sentence>
                <caps:sentence id="src293" class="srcSentence"> Windows Phone 8.1 devices will get the AET the next time they sync, up to eight hours.</caps:sentence>
                <caps:sentence id="src294" class="srcSentence"> Allow at least eight hours before deploying line of business apps after uploading the xap and pfx.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>