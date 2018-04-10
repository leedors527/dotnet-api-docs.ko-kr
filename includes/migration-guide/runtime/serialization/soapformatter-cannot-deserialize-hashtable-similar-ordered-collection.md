### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter 해시 테이블을 역직렬화 할 수 없습니다 및 순서가 지정 된 유사한 컬렉션 개체

|   |   |
|---|---|
|설명|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> 않습니다 개체 serialize 한.NET Framework 버전을 보장 하지는 다른 버전에서 성공적으로 deserialize 됩니다. 컬렉션 정렬 일부는 특히 (같은 <xref:System.Collections.Hashtable?displayProperty=name>)는.NET 4.5가 설치 된 serialize 된 경우.NET 4.0이 있는 이러한 유형의 개체를 역직렬화 할 수 없습니다 4.0 및 4.5 사이의 멤버를 추가 합니다. 직렬화된 데이터가 같은 .NET Framework 버전으로 직렬화 및 역직렬화되면 문제가 발생하지 않습니다.|
|제안 해결 방법|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> 직렬화로 대체 해야 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serialization 또는 <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> .NET Framework 변경 시 복원이 가능 합니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

