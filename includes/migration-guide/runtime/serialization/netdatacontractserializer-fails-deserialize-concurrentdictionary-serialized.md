### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>NetDataContractSerializer 다른.NET 버전을 사용 하 여 serialize ConcurrentDictionary deserialize 하는 데 실패

|   |   |
|---|---|
|설명|기본적으로 <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> 는 직렬화 및 역직렬화 끝 모두는 동일한 CLR 형식을 공유 하는 경우에 사용할 수 있습니다. 따라서 보장할 수는 없습니다 버전의.NET Framework를 사용 하 여 serialize 하는 개체를 다른 버전으로 deserialize 할 수 있습니다.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> .NET Framework 4.5를 사용 하 여 serialize 되 고.NET Framework 4.5.1로 deserialize 하는 경우 제대로 deserialize 하지 알려진 이상이 되는 형식이입니다.|
|제안 해결 방법|이 문제에 대 한 가능한 해결 방법의 여러 가지:<ul><li>.NET Framework 4.5.1도 사용 하도록 직렬화 컴퓨터를 업그레이드 합니다.</li><li>사용 하 여 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> 대신 <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> 대로 직렬화 및 역직렬화 끝 모두에서 정확히 동일한 CLR 형식은이 필요 하지 않습니다.</li><li>사용 하 여 <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> 대신 <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> 발생 하지 않습니다이 특정 4.5-이후&gt;4.5.1을 중단 합니다.</li></ul>|
|범위|부|
|버전|4.5.1|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

