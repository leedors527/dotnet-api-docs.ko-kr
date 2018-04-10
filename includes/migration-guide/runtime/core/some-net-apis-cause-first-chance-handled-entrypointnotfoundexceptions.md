### <a name="some-net-apis-cause-first-chance-handled-entrypointnotfoundexceptions"></a>일부.NET Api 원인 첫 번째 기회 EntryPointNotFoundExceptions (처리)

|   |   |
|---|---|
|설명|.NET Framework 4.5에서 적은 수의.NET 메서드 시작 된 첫 번째 기회를 throw <xref:System.EntryPointNotFoundException?displayProperty=name>s입니다. 이러한 예외는 .Net Framework 내에서 처리되지만 첫 번째 예외를 예상하지 않은 테스트 자동화를 중단시킬 수 있습니다. 이러한 동일 API는 HighVersionLie를 사용하는 경우 일부 ApiVerifier 시나리오를 중단시킵니다.|
|제안 해결 방법|.NET Framework 4.5.1로 업그레이드하여 이 버그를 방지할 수 있습니다. 테스트 자동화 되지 첫째에서 중단 하도록 업데이트할 수 있습니다 또는 <xref:System.EntryPointNotFoundException?displayProperty=name>s입니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Diagnostics.Debug.Assert(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Xml.Serialization.XmlSerializer.%23ctor(System.Type)?displayProperty=nameWithType></li></ul>|

