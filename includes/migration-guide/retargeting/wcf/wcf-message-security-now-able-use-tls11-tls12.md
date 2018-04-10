### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>WCF 메시지 보안 이제 TLS1.1 및 TLS1.2를 사용 하는

|   |   |
|---|---|
|설명|고객은.NET Framework 4.7 년부터 응용 프로그램 구성 설정을 통해 SSL3.0 및 TLS1.0 외에도 WCF 메시지 보안에 TLS1.1 또는 TLS1.2 구성할 수 있습니다.|
|제안 해결 방법|.NET Framework 4.7 WCF 메시지 보안의 TLS1.1 및 TLS1.2 지원 기본적으로 비활성화 됩니다. 다음 줄을 추가 하 여 사용할 수 있습니다는 <code>&lt;runtime&gt;</code> app.config 또는 web.config 파일의 섹션:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.7|
|형식|대상 변경|

