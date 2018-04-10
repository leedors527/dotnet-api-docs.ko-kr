### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>EntityDeploySplit 또는 EntityClean 작업을 사용 하는 경우 MSB4062 오류로 실패할 수 있습니다는 Entity Framework edmx Visual Studio 2013과 함께 작성

|   |   |
|---|---|
|설명|MSBuild 파일 위치, 유효 하지 않은 것 이전 Entity Framework 대상 파일을 일으키는 변경 하는 MSBuild 12.0 도구 (Visual Studio 2013에 포함 됨). 그 결과로 <code>EntityDeploySplit</code> 및 <code>EntityClean</code> 작업이 <code>Microsoft.Data.Entity.Build.Tasks.dll</code>을 찾을 수 없어 실패합니다. 이 줄 바꿈으로 아닌지 (MSBuild/VS) 도구 집합 변경으로 인해.NET Framework 변경으로 인해 note 합니다. 이것은 단순히 .NET Framework를 업그레이드할 때가 아니라 개발자 도구를 업그레이드할 때에만 발생합니다.|
|제안 해결 방법|Entity Framework 대상 파일은.NET Framework 4.6의 새로운 MSBuild 레이아웃 기능인 작업할 고정 됩니다. 해당 버전의 Framework로 업그레이드하면 이 문제가 해결됩니다. 또는 [이](http://stackoverflow.com/a/24249247/131944) 해결 방법을 대상 파일을 직접 패치하는데 사용할 수 있습니다.|
|범위|주요함|
|버전|4.5.1|
|형식|대상 변경|

