### <a name="unicode-standard-version-80-categories-now-supported"></a>유니코드 표준 버전 8.0 범주 이제 지원

|   |   |
|---|---|
|설명|.NET Framework 4.6.2에서에서 버전 8.0으로 프레임 워크의 유니코드 데이터 유니코드 표준 버전 6.3에서에서 업그레이드 않았습니다.  .NET Framework 4.6.2에서에서 유니코드 문자 범주를 요청할 때는 일부 결과가 이전.NET Framework 버전에서 결과 다릅니다.  영향을 줌 체로키어 사용 음절 및 새 비상 Lue 모음 기호 및 톤 표식 주로 변경 합니다.|
|제안 해결 방법|코드 검토 하 고 하드 코드 된 유니코드 문자 범주에 따라 달라 지는 논리 제거/변경 합니다.|
|범위|부|
|버전|4.6.2|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

