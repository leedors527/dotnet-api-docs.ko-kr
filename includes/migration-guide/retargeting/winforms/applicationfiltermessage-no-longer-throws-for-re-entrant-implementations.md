### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>Application.FilterMessage 재진입용 IMessageFilter.PreFilterMessage 구현에 대해 더 이상 throw

|   |   |
|---|---|
|설명|.NET Framework 4.6.1 하기 전에, 호출 <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> 와 <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> 호출한 <xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> 또는 <xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> (호출 또한 하는 동안 <xref:System.Windows.Forms.Application.DoEvents>)로 인해는 <xref:System.IndexOutOfRangeException?displayProperty=name>합니다. .NET Framework 4.6.1을 대상으로 응용 프로그램부터,이 더 이상 예외가 하며 재진입용 필터 위에서 설명한 것 처럼 사용할 수 없습니다.|
|제안 해결 방법|주의 <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> 는 재진입용에 대 한 더 이상 throw 됩니다 <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> 위에서 설명한 동작 합니다. 만 사용 하 여는.NET Framework 4.6.1.Apps 대상.NET Framework 4.6.1이이 변경 하지 않을 수 있습니다 (또는 응용 프로그램의 이전 프레임 워크를 대상으로 선택할 수 있습니다)을 대상으로 응용 프로그램을 미치면는 [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation) 호환성 스위치입니다.|
|범위|Microsoft Edge|
|버전|4.6.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

