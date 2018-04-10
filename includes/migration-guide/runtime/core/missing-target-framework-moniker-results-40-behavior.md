### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>누락 된 대상 프레임 워크 모니커 4.0 동작이 발생

|   |   |
|---|---|
|설명|응용 프로그램을 <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> 어셈블리 수준도 자동으로.NET Framework 4.0의 (quirks) 의미 체계를 사용 하 여를 실행에 적용 합니다. 높은 품질을 보장 하려면 것이 좋습니다 모든 이진 파일에 명시적으로 추측할는 <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> 으로 빌드된.NET Framework의 버전을 나타내는입니다. 프로젝트 파일의 대상 프레임 워크 모니커를 사용 하 여 자동으로 적용 하기 위해 MSBuild 발생할 됩니다는 <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>합니다.|
|제안 해결 방법|A <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> 제공 해야 합니다는 어셈블리를 직접 또는에 대상 프레임 워크를 지정 하 여 특성을 추가 하는 과정 중 하나는 [프로젝트 파일 또는 Visual Studio를 통해 프로젝트 속성 GUI](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx)합니다.|
|범위|주요함|
|버전|4.5|
|형식|런타임|

