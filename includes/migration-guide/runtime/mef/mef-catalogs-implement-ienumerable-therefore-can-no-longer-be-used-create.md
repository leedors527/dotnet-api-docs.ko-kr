### <a name="mef-catalogs-implement-ienumerable-and-therefore-can-no-longer-be-used-to-create-a-serializer"></a>MEF 카탈로그는 IEnumerable을 구현 하 고 따라서 더 이상 사용할 수는 serializer를 만들려면

|   |   |
|---|---|
|설명|.NET Framework 4.5부터 MEF 카탈로그 IEnumerable을 구현 하 고 따라서 더 이상 사용할 수는 serializer를 만들려면 (<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name> 개체). MEF 카탈로그를 serialize하려고 하면 예외가 throw됩니다.|
|제안 해결 방법|직렬 변환기를 만드는데 MEF를 더 이상 사용할 수 없음|
|범위|주요함|
|버전|4.5|
|형식|런타임|

