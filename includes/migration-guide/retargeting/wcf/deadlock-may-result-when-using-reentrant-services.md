### <a name="deadlock-may-result-when-using-reentrant-services"></a>재진입 서비스를 사용 하는 경우 교착 상태가 발생할 수 있습니다.

|   |   |
|---|---|
|설명|실행 한 번에 하나의 스레드를 서비스의 인스턴스를 제한 하는 재진입 서비스에서 교착 상태가 발생할 수 있습니다. 이 문제가 발생 하기 쉬운 서비스에는 다음 항목이 됩니다 <xref:System.ServiceModel.ServiceBehaviorAttribute> 가 코드에서:<pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Reentrant)]&#13;&#10;</code></pre>|
|제안 해결 방법|이 문제를 해결 하려면 다음을 수행할 수 있습니다.<ul><li>서비스의 동시성 모드를 설정 <xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType> 또는 &lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;합니다. 예:</li></ul><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single)]&#13;&#10;</code></pre><ul><li>.NET Framework 4.6.2에 대 한 최신 업데이트를 설치 하거나.NET Framework의 이후 버전으로 업그레이드 하십시오. 흐름을 사용할 수 없게 된 <xref:System.Threading.ExecutionContext> 에서 <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>합니다. 이 동작은 구성할 수 없습니다. 다음 응용 프로그램 설정을 구성 파일에 추가 하는 것이 같습니다.</li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;&#13;&#10;The value of &#39;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&#39; should never be set to &#39;false&#39; for Rentrant services.&#13;&#10;</code></pre>|
|범위|부|
|버전|4.6.2|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.ServiceModel.ServiceBehaviorAttribute?displayProperty=nameWithType></li><li><xref:System.ServiceModel.ConcurrencyMode.Reentrant?displayProperty=nameWithType></li></ul>|

