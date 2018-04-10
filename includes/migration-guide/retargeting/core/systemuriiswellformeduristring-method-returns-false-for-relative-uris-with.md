### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>첫 번째 세그먼트에 콜론 char가 포함 된 상대 Uri에 대 한 System.Uri.IsWellFormedUriString 메서드가 false 반환

|   |   |
|---|---|
|설명|.NET Framework 4.5 부터는 <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> 와 상대 Uri를 처리 합니다는 <code>:</code> 형식이 잘못 되었습니다. 대로 첫 번째 세그먼트에 있습니다. 이 변경 내용에서 <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> RFC3986에 맞게 작성 된.NET Framework 4.0의 동작입니다.|
|제안 해결 방법|이러한 변경 (예: 다른 여러 URI 변경).NET Framework 4.5 (또는 이후 버전)을 대상으로 응용 프로그램만 적용 됩니다. 계속 사용 이전 동작을.NET Framework 4.0에 대해 앱의 대상입니다. 또는 URI의 호출 하기 전에 검사 <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> 찾고 <code>:</code> 이전 동작이 문제가 있는 경우 유효성 검사를 위해 제거 해야 할 수 있는 문자입니다.|
|범위|부|
|버전|4.5|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

