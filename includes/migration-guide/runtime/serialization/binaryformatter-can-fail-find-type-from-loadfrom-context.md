### <a name="binaryformatter-can-fail-to-find-type-from-loadfrom-context"></a>LoadFrom 컨텍스트에서 형식을 찾기 위해 BinaryFormatter 실패할 수 있습니다.

|   |   |
|---|---|
|설명|.NET Framework 4.5, 다양 한 기준으로 <xref:System.Xml.Serialization.XmlSerializer?displayProperty=name> 사용 하는 경우 변경 deserialization의 차이 발생할 수 있습니다 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> 를 LoadFrom 컨텍스트에서 로드 된 형식을 역직렬화 합니다. 이러한 변경 사항은 새로운 방법으로 인해 <xref:System.Xml.Serialization.XmlSerializer?displayProperty=name> 이제 다른 동작이 발생 하는 형식 로드 때는 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> 나중에 해당 형식으로 deserialize 하려고 시도 합니다. XmlSerializer의 이전 동작에 따라 일부 환경에서 작업 하는 수는 있지만 기본 serialization 바인더 LoadFrom 컨텍스트의 자동으로 검색 하지 않습니다. 형식이 각기 다른 컨텍스트에서 로드 된 어셈블리에서 로드 되는 경우 변경 내용으로 인해 한 <xref:System.IO.FileNotFoundException?displayProperty=name> throw 될 수 있습니다.|
|제안 해결 방법|이 예외가 표시 되는 <code>Binder</code> 의 속성은 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> 올바른 형식을 찾을 수는 사용자 지정 바인더로 설정할 수 있습니다.<pre><code class="language-C#">var formatter = new BinaryFormatter { Binder = new TypeFinderBinder() }&#13;&#10;</code></pre>및 사용자 지정 된 바인더 다음:<pre><code class="language-C#">public class TypeFinderBinder : SerializationBinder&#13;&#10;{&#13;&#10;private static readonly string s_assemblyName = Assembly.GetExecutingAssembly().FullName;&#13;&#10;&#13;&#10;public override Type BindToType(string assemblyName, string typeName)&#13;&#10;{&#13;&#10;return Type.GetType(String.Format(CultureInfo.InvariantCulture, &quot;{0}, {1}&quot;, typeName, s_assemblyName));&#13;&#10;}&#13;&#10;}&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

