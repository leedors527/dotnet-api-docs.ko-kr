### <a name="default-value-of-servicepointmanagersecurityprotocol-is-securityprotocoltypesystemdefault"></a>ServicePointManager.SecurityProtocol의 기본값은 SecurityProtocolType.System.Default

|   |   |
|---|---|
|설명|.NET Framework 4.7의 기본값을 대상으로 하는 앱부터는 <xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType> 속성은 <xref:System.Net.SecurityProtocolType.SystemDefault?displayProperty=nameWithType>합니다. 이 변경 사항은.NET Framework는.NET Framework에 정의 된 하드 코드 된 값을 사용 하는 대신 운영 체제에서 기본 보안 프로토콜을 상속 하도록 네트워킹 Api (예: FTP, HTTPS 및 SMTP) SslStream 기반 허용 합니다. 기본 운영 체제와 시스템 관리자가 수행 하는 모든 사용자 지정 구성에 따라 다릅니다. 각 버전의 Windows 운영 체제에 기본 SChannel 프로토콜에 대 한 자세한 내용은 참조 [TLS/SSL (Schannel SSP)의 프로토콜](https://msdn.microsoft.com/library/windows/desktop/mt808159.aspx)합니다. 이전 버전의.NET Framework의 기본값을 대상으로 하는 응용 프로그램에 대 한는 <xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType> 속성의 대상.NET Framework 버전에 따라 달라 집니다. 참조는 [.NET Framework 4.5.2을 4.6에서에서의 마이그레이션에 대 한 변경 내용 대상 변경의 네트워킹 섹션](~/docs/framework/migration-guide/retargeting/4.5.2-4.6.md#networking) 자세한 정보에 대 한 합니다.|
|제안 해결 방법|이 변경 사항은.NET Framework 4.7 또는 이후 버전을 대상으로 하는 응용 프로그램에 적용 합니다. 시스템 기본값에 의존 하는 값을 명시적으로 설정할 수 있습니다 하는 대신 정의 된 프로토콜을 사용 하려는 경우는 <xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType> 속성입니다. 에 구성 설정을 추가 하 여 옵트아웃 선택할 수 있습니다이 변경은 필요 없는 경우는 [ \<런타임 >](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 응용 프로그램 구성 파일의 섹션입니다. 다음 예제에서는 모두는 <code>&lt;runtime&gt;</code> 섹션 및 <code>Switch.System.Net.DontEnableSystemDefaultTlsVersions</code> 옵트아웃 스위치:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSystemDefaultTlsVersions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType></li></ul>|

