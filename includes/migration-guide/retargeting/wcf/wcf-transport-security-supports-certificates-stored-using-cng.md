### <a name="wcf-transport-security-supports-certificates-stored-using-cng"></a>WCF 전송 보안 CNG를 사용 하 여 저장 된 인증서를 지원 합니다.

|   |   |
|---|---|
|설명|앱 부터는.NET Framework 4.6.2 대상, WCF 전송 보안 Windows 라이브러리 CNG (Cryptography)를 사용 하 여 저장 된 인증서를 지원 합니다. 이 지원은 지수 길이가 32비트 이하인 공개 키로 인증서로 제한됩니다. 응용 프로그램에서.NET Framework 4.6.2를 대상으로 하는 경우이 기능은 기본적으로 켜져 있습니다. .NET Framework의 이전 버전에서는 X509를 사용 하려고 한 CSG와 함께 인증서 키 저장소 공급자는 예외를 throw 합니다.|
|제안 해결 방법|대상.NET Framework 4.6.1 및 이전 하지만.NET Framework 4.6.2에서 실행 되는 앱에 다음 줄을 추가 하 여 CNG 인증서에 대 한 지원을 사용 하도록 설정할 수는 <code>&lt;runtime&gt;</code> app.config 또는 web.config 파일의 섹션:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableCngCertificates=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>다음 코드를 사용하여 프로그래밍 방식으로 이 작업을 수행할 수도 있습니다.<pre><code class="language-cs">private const string DisableCngCertificates = @&quot;Switch.System.ServiceModel.DisableCngCertificate&quot;;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, false);&#13;&#10;</code></pre><pre><code class="language-vb">Const DisableCngCertificates As String = &quot;Switch.System.ServiceModel.DisableCngCertificates&quot;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, False)&#13;&#10;</code></pre>이러한 변경으로 인해 CNG 인증서와의 보안 통신을 시작하려는 시도에 종속되는 예외 처리 코드를 더 이상 실행할 수 없습니다.|
|범위|부|
|버전|4.6.2|
|형식|대상 변경|

