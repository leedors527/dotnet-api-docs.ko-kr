### <a name="path-colon-checks-are-stricter"></a>경로가 콜론 검사는 더욱 엄격 하 게

|   |   |
|---|---|
|설명|.NET Framework 4.6.2에서에서 변경 내용 수 (둘 다에서 길이 형식) 이전에 지원 되지 않는 경로를 지원 했습니다. 적절 한 드라이브 (콜론) 구분 기호 구문에 대 한 검사 수행로 어떤 모델이 영향을 주는 몇 가지 URI 경로를 허용 하는 데 있는 몇 가지 선택 경로 Api에서 차단 됩니다.|
|제안 해결 방법|URI, 영향을 받는 Api에 전달 하는 경우 올바른 경로 먼저 되도록 문자열을 수정 합니다.<ul><li>Url의 체계를 수동으로 제거 (예: 제거 <code>file://</code> Url에서)</li><li>URI를 전달한는 <xref:System.Uri> 클래스 및 사용 <xref:System.Uri.LocalPath></li></ul>또는 선택할 수 있습니다 새 경로 정규화 외부로 설정 하 여는 <code>Switch.System.IO.UseLegacyPathHandling</code> true로 AppContext 스위치입니다.|
|범위|Microsoft Edge|
|버전|4.6.2|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|

