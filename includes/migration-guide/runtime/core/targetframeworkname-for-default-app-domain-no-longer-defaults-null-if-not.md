### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>기본 응용 프로그램 도메인에 대 한 TargetFrameworkName 더 이상 기본적으로 설정 하지 않으면 null

|   |   |
|---|---|
|설명|<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> 을 명시적으로 설정 하지 않으면 기본 응용 프로그램 도메인에서 이전에 null 되었습니다. 4.6부터는 <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> 기본 응용 프로그램 도메인에 대 한 속성 (있는 경우)는 TargetFrameworkAttribute에서 파생 된 기본값을 갖습니다. 기본이 아닌 응용 프로그램 도메인 상속 하도록 계속 해당 <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> (4.6에서 null로 기본은)는 기본 응용 프로그램 도메인에서 명시적으로 재정의 되지 않는 합니다.|
|제안 해결 방법|코드는 기본값을 null로 하는 <xref:System.AppDomainSetup.TargetFrameworkName>에 종속하지 않도록 업데이트되어야 합니다. 이 속성이 계속 null을 평가해야 하는 경우 명시적으로 해당 값을 설정할 수 있습니다.|
|범위|Microsoft Edge|
|버전|4.6|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

