### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant 또는 Contract.Requires<TException> 를 순수 String.IsNullOrEmpty 고려 하지 않습니다

|   |   |
|---|---|
|설명|에 대 한 고정 계약 하는 경우.NET Framework 4.6.1을 대상으로 하는 앱에 대 한 <xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType> 또는 대 한 사전 조건 계약 <xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)> 호출은 <xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType> 메서드, 재작성 기에서 내보내는 컴파일러 CC1036 경고: &quot;메서드 호출을 감지 ' System.String.IsNullOrWhteSpace(System.String)' [순수형] 없이 메서드에서 합니다.&quot; 이 컴파일러 오류가 아닌 컴파일러 경고가 발생 합니다.|
|제안 해결 방법|이 동작에서는 [GitHub 문제 #339](https://github.com/Microsoft/CodeContracts/issues/339)가 해결되었습니다. 이 경고를 제거 하려면 다운로드 및 업데이트 된 버전에서 코드 계약 도구에 대 한 소스 코드의 컴파일 수 [GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md)합니다. 다운로드 정보는 페이지 하단에서 찾을 수 있습니다.|
|범위|부|
|버전|4.6.1|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

