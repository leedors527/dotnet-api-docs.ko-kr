### <a name="xslt-forward-compat-now-works"></a>XSLT 정방향 compat 이제 작동합니다.

|   |   |
|---|---|
|설명|.NET Framework 4의 XSLT 1.0 다음 버전과 호환성에 다음과 같은 문제가 있었습니다.<ul><li>버전이 2.0으로 설정되고 인식할 수 없는 XSLT 1.0 구문에서 파서가 발생하면 스타일시트를 로드하지 못했습니다.</li><li>스타일시트 버전이 1.1로 설정된 경우 <code>xsl:sort</code> 구문이 데이터를 정렬하지 못했습니다.</li></ul>.NET Framework 4.5에서 이러한 문제를 해결 한 및 XSLT 1.0 다음 버전과 호환성 모드는 제대로 작동 합니다.|
|제안 해결 방법|하지만 데이터 정렬 다르게 일부 경우에 xsl: sort가 적용 했으므로 대부분의 응용 프로그램의 영향을 취소 해야 합니다. 경우 <code>xsl:sort</code> 은 앱 데이터의 정렬 되지 않은 순서에 따라 되지 않은 확인 1.1 스타일 시트를 사용 합니다. 앱에서 4.0 정렬 동작에 사용 해야 하는 경우 제거 <code>xsl:sort</code> 스타일 시트에서.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|

