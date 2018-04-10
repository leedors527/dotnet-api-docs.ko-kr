### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>TransportWithMessageCredential 보안 모드와 함께 WCF 바인딩

|   |   |
|---|---|
|설명|.NET Framework 4.6.1부터, TransportWithMessageCredential 보안 모드를 사용 하는 WCF 바인딩을 설정할 수 있습니다를 부호 없는 사용 하 여 메시지를 받을 &quot;를&quot; 비대칭 보안 키에 대 한 헤더입니다. 기본적으로 부호 없는 &quot;를&quot; 헤더는 계속.NET 4.6.1에서에서 거부 됩니다. 경우에 허용 Switch.System.ServiceModel.AllowUnsignedToHeader 구성 스위치를 사용 하 여 작업의이 새로운 모드에 opts 응용 프로그램입니다. 이 기능은 옵트인 기능이 때문에 기존 앱의 동작에는 영향을 주지 해야 합니다.|
|제안 해결 방법|이 기능은 옵트인 기능이기 때문에 기존 앱의 동작에는 영향을 주지 않습니다. 새 동작 사용 여부를 제어 하려면 다음 구성 설정을 사용 합니다.<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|투명|
|버전|4.6.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

