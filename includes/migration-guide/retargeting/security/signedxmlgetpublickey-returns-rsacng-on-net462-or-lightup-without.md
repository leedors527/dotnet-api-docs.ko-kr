### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey RSACng net462 (또는 lightup)에서 변경 내용 대상 변경 하지 않고 반환

|   |   |
|---|---|
|설명|.NET Framework 4.6.2, 반환 되는 개체의 구체적인 형식 부터는 <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> 메서드 (하지 않고 변경 스트리밍되) CryptoServiceProvider 구현에서 Cng 구현을 합니다. 사용 하 여 구현이 변경 때문에 이것이 <code>certificate.PublicKey.Key</code> 내부에서 사용 하 여 <code>certificate.GetAnyPublicKey</code> 을 전달 하 <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>합니다.|
|제안 해결 방법|4.7.1.NET Framework에서 실행 되는 앱 부터는.NET Framework 4.6.1에서에서 기본적으로 사용 되는 CryptoServiceProvider 구현을 사용할 수 있으며 다음 구성을 추가 하 여 이전 버전으로 전환 된 [런타임](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)응용 프로그램 구성 파일의 섹션:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.6.2|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

