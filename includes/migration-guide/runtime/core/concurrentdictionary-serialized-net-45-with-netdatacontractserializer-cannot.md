### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>NetDataContractSerializer 사용.NET 4.5에서 직렬화 ConcurrentDictionary.NET 4.5.1 또는 4.5.2에서 역직렬화 할 수 없습니다.

|   |   |
|---|---|
|설명|이 형식에는 내부 변경 내용으로 인해 <xref:System.Collections.Concurrent.ConcurrentDictionary%602> serialize 되는.NET Framework 4.5가 설치 된 개체를 사용 하 여는 <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> .NET Framework 4.5.1 또는.NET Framework 4.5.2.Note 역직렬화 할 수 없습니다는 다른 방향 (에서 이동 .NET Framework와 함께 직렬화 4.5.x 및.NET Framework 4.5가 설치 된 역직렬화) 작동 합니다. 마찬가지로, 모든 4.x 버전 간 serialization으로.NET Framework 4.6.Serializing를.NET Framework의 단일 버전과 역직렬화 하는 동안 영향을 받지 않습니다.|
|제안 해결 방법|serialize 및 deserialize 해야 하는 경우는 <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> 대체 serializer와 같은.NET Framework 4.5와.NET Framework 4.5.1/4.5.2 간에 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> 또는 <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> 대신 serializer를 사용 해야는 <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>합니다. 또는.NET Framework 4.6에서이 문제가 해결 되 면 때문에.NET Framework의 해당 버전으로 업그레이드 하 여 해결할 수 있습니다.|
|범위|부|
|버전|4.5.1|
|형식|런타임|

