### <a name="xslt-style-sheet-exception-message-changed"></a>변경 하는 XSLT 스타일 시트 예외 메시지

|   |   |
|---|---|
|설명|.NET Framework 4.5에서 XSLT 파일이 너무 복잡할 경우 오류 메시지의 텍스트는 &quot;스타일 시트가 너무 복잡 합니다.&quot; 오류 메시지는 이전 버전에서는 &quot;XSLT 컴파일 오류가 발생 합니다.&quot; 오류 메시지 텍스트에 종속되어 있는 응용 프로그램 코드는 더 이상 작동하지 않습니다. 그러나 예외 형식은 동일하게 유지되므로 이 변경은 실제 영향을 미쳐서는 안 됩니다.|
|제안 해결 방법|이 오류 조건에서 새 메시지를 기대 하는 예외 메시지에 따라 모든 응용 프로그램 코드 (더 좋은) 예외 형식에 따라서만 결정 하는 코드를 업데이트 하거나 (<xref:System.Xml.Xsl.XsltException?displayProperty=name>), 변경 되지 않았습니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Type)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Reflection.MethodInfo,System.Byte[],System.Type[])?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li></ul>|

