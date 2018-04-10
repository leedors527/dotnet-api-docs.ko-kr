### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>UseRandomizedStringHashAlgorithm 여 AppDomainSetup.DynamicBase는 임의 더 이상

|   |   |
|---|---|
|설명|.NET Framework 4.6의 값 이전의 <xref:System.AppDomainSetup.DynamicBase> 것 될 임의 응용 프로그램 도메인 간 또는 프로세스 간 UseRandomizedStringHashAlgorithm 응용 프로그램의 구성 파일에서 사용 하도록 설정 된 경우. .NET Framework 4.6부터 <xref:System.AppDomainSetup.DynamicBase> 다른 응용 프로그램 도메인 간 및 응용 프로그램을 실행 하는 여러 인스턴스 간에 안정적인 결과 반환 합니다. 다른 앱;에 대 한 동적 자료 여전히 다릅니다. 이 변경만 동일한 앱의 다른 인스턴스에 대 한 명명 임의 요소를 제거합니다.|
|제안 해결 방법|주의 설정 해도 <code>UseRandomizedStringHashAlgorithm</code> 발생 하지 않을 <xref:System.AppDomainSetup.DynamicBase> 임의 되 고 있습니다. 임의 자료 필요한 경우 대신이 API를 통해 앱의 코드에서 생성 될 해야 합니다.|
|범위|Microsoft Edge|
|버전|4.6|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

