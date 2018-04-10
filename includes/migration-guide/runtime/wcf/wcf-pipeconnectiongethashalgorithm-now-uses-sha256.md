### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>WCF PipeConnection.GetHashAlgorithm now uses SHA256

|   |   |
|---|---|
|설명|.NET Framework 4.7.1 부터는 Windows Communication Foundation를 사용 하 여 SHA256 해시 명명 된 파이프에 대 한 임의의 이름을 생성 합니다. .NET Framework 4.7 및 이전 버전에서이 SHA1 해시를 사용 했습니다.|
|제안 해결 방법|이러한 변경으로 인해 호환성 문제가 4.7.1.NET Framework에서 실행 하면 또는 이상 버전에서는 있습니다 수 옵트아웃 것에 다음 줄을 추가 하 여 하는 경우는 <code>&lt;runtime&gt;</code> app.config 파일의 섹션:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7.1|
|형식|런타임|

