### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>AddressHeader 요소가 null 인 경우 이제 WCF AddressHeaderCollection는 ArgumentException throw

|   |   |
|---|---|
|설명|.NET Framework 4.7.1부터 <xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})> 생성자 throw는 <xref:System.ArgumentException> 요소 중 하나 이면 <code>null</code>합니다. .NET Framework 4.7 및 이전 버전에서 예외가 throw 되지 않습니다.|
|제안 해결 방법|.NET Framework 4.7.1 또는 이후 버전에서 이러한 변경으로 인해 호환성 문제가 발생 하는 경우 있습니다 수 옵트아웃의 다음 줄을 추가 하 여는 <code>&lt;runtime&gt;</code> app.config 파일의 섹션::<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7.1|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|

