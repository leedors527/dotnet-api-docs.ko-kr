### <a name="contentdisposition-datetimes-returns-slightly-different-string"></a>ContentDisposition Datetime 약간 다른 문자열을 반환합니다.

|   |   |
|---|---|
|설명|문자열의 표현을 <xref:System.Net.Mime.ContentDisposition?displayProperty=name>의 업데이트 되지 않은 경우 항상의 시간 구성 요소를 나타내기 위해 4.6부터는 <xref:System.DateTime?displayProperty=name> 두 자리입니다. 이것은 [RFC822](http://www.ietf.org/rfc/rfc0822.txt) 및 [RFC2822](http://www.ietf.org/rfc/rfc2822.txt)를 준수하기 위함입니다. 이로 인해 4.6에서 <xref:System.Net.Mime.ContentDisposition.ToString>은 처리 시간 요소 중 하나가 오전 10시 전인 시나리오에서 약간 다른 문자열을 반환합니다. ContentDispositions 요소를 문자열로 변환, 내용이 통해 경우에 따라 serialize 되 참고 <xref:System.Net.Mime.ContentDisposition.ToString> 작업, serialization 또는 GetHashCode 호출을 검토 해야 합니다.|
|제안 해결 방법|다른 .NET Framework 버전에서 ContentDispositions의 문자열 표현이 서로 올바르게 비교할 것으로 기대하지 마십시오. 가능하면 비교를 수행하기 전에 문자열을 다시 ContentDispositions로 변환합니다.|
|범위|부|
|버전|4.6|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Net.Mime.ContentDisposition.ToString?displayProperty=nameWithType></li><li><xref:System.Net.Mime.ContentDisposition.GetHashCode?displayProperty=nameWithType></li></ul>|

