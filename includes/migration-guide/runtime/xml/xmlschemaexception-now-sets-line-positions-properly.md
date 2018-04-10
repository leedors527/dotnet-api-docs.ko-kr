### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException 이제 줄 위치 설정 제대로

|   |   |
|---|---|
|설명|경우는 <xref:System.Xml.Linq.LoadOptions.SetLineInfo> 값은에 Load 메서드에서 전달 및 유효성 검사 오류가 발생 하는 <xref:System.Xml.Schema.XmlSchemaException.LineNumber> 및 <xref:System.Xml.Schema.XmlSchemaException.LinePosition> 속성은 이제 줄 정보를 포함 합니다.|
|제안 해결 방법|가정 하는 예외 처리 코드 <xref:System.Xml.Schema.XmlSchemaException.LineNumber> 및 <xref:System.Xml.Schema.XmlSchemaException.LinePosition> 됩니다 SetLineInfo XML을 로드 하는 동안 사용 되는 경우 이러한 속성이 제대로 설정 이제는 때문에 집합을 업데이트 해야 합니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

