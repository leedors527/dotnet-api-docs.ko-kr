### <a name="certificate-eku-oid-validation"></a>인증서 또는 EKU OID 유효성 검사

|   |   |
|---|---|
|설명|.NET Framework 4.6부터는 <xref:System.Net.Security.SslStream> 또는 <xref:System.Net.ServicePointManager> 클래스는 향상 된 키 사용 (EKU) 개체 식별자 (OID) 유효성 검사를 수행 합니다. (Eku 확장) 확장 된 키 사용 확장은 키를 사용 하는 응용 프로그램을 나타내는 개체 식별자 (Oid)의 컬렉션입니다. EKU OID 유효성 검사 원격 인증서 콜백을 사용 하 여 원격 인증서가 의도 한 목적에 대 한 올바른 Oid를 확인할 수 있습니다.|
|제안 해결 방법|이 변경은 필요 없는 경우에 다음 스위치를 추가 하 여 인증서 EKU OID 유효성 검사를 해제할 수 있습니다는 [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) 에 [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 의 사용자 응용 프로그램 구성 파일:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] 이 설정에 대 한 이전 버전과 호환성을 위해서만 제공 됩니다. 사용 하지 않으면 권장 되지 않습니다.</blockquote> |
|범위|부|
|버전|4.6|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

