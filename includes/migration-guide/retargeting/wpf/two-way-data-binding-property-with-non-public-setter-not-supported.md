### <a name="two-way-data-binding-to-a-property-with-a-non-public-setter-is-not-supported"></a>Public이 아닌 setter 사용 하 여 속성에 양방향 데이터 바인딩은 지원 되지 않습니다.

|   |   |
|---|---|
|설명|public setter가 없는 속성에 데이터 바인딩을 시도하는 것은 지원된 적이 없는 시나리오였습니다. .NET Framework 4.5.1부터,이 시나리오는 throw 되는 <xref:System.InvalidOperationException?displayProperty=name>합니다. 이 새로운 예외는 구체적으로 .NET Framework 4.5.1을 대상으로 하는 응용 프로그램만 throw됩니다. 응용 프로그램이 .NET Framework 4.5를 대상으로 하는 경우 호출이 허용됩니다. 응용 프로그램이 특정 .NET Framework 버전을 대상으로 하지 않는 경우 바인딩은 단방향으로 처리됩니다.|
|제안 해결 방법|응용 프로그램은 단방향 바인딩을 사용하거나 속성의 setter를 공개적으로 노출하도록 업데이트되어야 합니다. 또는 .NET Framework 4.5를 대상으로 하면 응용 프로그램이 이전 동작을 실행하게 됩니다.|
|범위|부|
|버전|4.5.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType></li></ul>|

