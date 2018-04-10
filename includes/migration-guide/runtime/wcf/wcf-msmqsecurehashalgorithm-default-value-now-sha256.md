### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>WCF MsmqSecureHashAlgorithm 기본값은 SHA256 이제

|   |   |
|---|---|
|설명|.NET Framework 4.7.1 부터는 서명 알고리즘 WCF에서 Msmq 메시지에 대 한 기본 메시지는 s h a 256입니다. .NET Framework 4.7 및 이전 버전에서 서명 알고리즘의 기본 메시지는 s h a 1입니다.|
|제안 해결 방법|이러한 변경으로 인해 호환성 문제가 발생 4.7.1.NET Framework에서 실행 하면 또는 이상 버전에서는 있습니다 수 옵트아웃 변경에 다음 줄을 추가 하 여 하는 경우는 <code>&lt;runtime&gt;</code>app.config 파일의 섹션:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7.1|
|형식|런타임|

