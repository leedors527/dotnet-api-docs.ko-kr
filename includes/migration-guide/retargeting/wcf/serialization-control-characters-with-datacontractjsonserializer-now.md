### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>제어 문자 DataContractJsonSerializer로의 serialization V8 및 V6 ECMAScript와 호환 됩니다.

|   |   |
|---|---|
|설명|.NET framework 4.6.2 이전 버전에서의 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name> \b, \f, \t ECMAScript V6 및 V8 표준와 호환 되는 방식에서 등 몇 가지 특수 제어 문자를 serialize 하지 못했습니다. .NET Framework 4.7 이상에서는 이러한 제어 문자 serialization은 V8 및 V6 ECMAScript와 호환 됩니다.|
|제안 해결 방법|.NET Framework 4.7를 대상으로 하는 응용 프로그램의 경우이 기능은 기본적으로 사용 됩니다. 이 동작을 원치 않는 경우 app.config 또는 web.config 파일의 <code>&lt;runtime&gt;</code> 섹션에 다음 줄을 추가하여 이 기능을 옵트아웃(opt out)할 수 있습니다.<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.7|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

