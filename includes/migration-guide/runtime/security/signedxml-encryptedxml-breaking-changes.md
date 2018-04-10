### <a name="signedxml-and-encryptedxml-breaking-changes"></a>SignedXml 및 EncryptedXml 주요 변경 내용

|   |   |
|---|---|
|설명|.NET Framework 4.6.2에서에서 보안에 고정 <xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name> 및 <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name> 다른 런타임 동작을 선행 합니다. 예를 들어 개체에 적용된<ul><li>문서에 동일한 여러 요소가 <code>id</code> 특성 및 서명을 서명의 루트로 이러한 요소 중 하나를 대상, 문서 이제으로 간주 됩니다 잘못 되었습니다.</li><li>참조에 비정식 XPath 변환 알고리즘을 사용 하 여 문서 잘못 간주 됩니다.</li><li>이제 참조에서 정식이 아닌 XSLT 변환 알고리즘을 사용 하 여 문서는 잘못 된 살펴보겠습니다.</li><li>모든 프로그램을 사용 하 여 외부 리소스 분리 서명 할 수 없습니다.</li></ul>|
|제안 해결 방법|개발자의 사용을 검토 하려는 <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform> 및 <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>형식에서 파생 하는 것은 물론, <xref:System.Security.Cryptography.Xml.Transform> 수신자가 문서를 처리할 수 있습니다.|
|범위|부|
|버전|4.6.2|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

