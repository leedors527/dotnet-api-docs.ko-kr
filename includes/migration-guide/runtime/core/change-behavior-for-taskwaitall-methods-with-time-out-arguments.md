### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>제한 시간 인수가 있는 Task.WaitAll 메서드에 대 한 동작 변경 사항

|   |   |
|---|---|
|설명|Task.WaitAll 수행 보다 일관 된.NET 4.5.In에.NET Framework 4에서는 이러한 메서드 되지 않게 동작 했었습니다. 제한 시간이 만료되고 메서드 호출 전에 하나 이상의 작업이 완료되거나 취소되면 이 메서드는 <xref:System.AggregateException?displayProperty=name> 예외를 throw합니다. 제한 시간이 만료되고 메서드 호출 전에 완료되거나 취소된 작업은 없지만 메서드 호출 후에 하나 이상의 작업이 완료되거나 취소되면 이 메서드는 false를 반환합니다.<br/><br/>.NET Framework 4.5에서 이러한 메서드 오버 로드 이제 false를 반환 하는 경우 시간 제한 간격이 만료 되 고 throw 하는 경우 모든 작업이 실행 되는 <xref:System.AggregateException?displayProperty=name> (에 관계 없이 앞 이나 뒤의 메서드는 여부 입력된 한 작업이 취소 되는 경우에 예외 호출) 다른 작업이 실행 되 고 있습니다.|
|제안 해결 방법|경우는 <xref:System.AggregateException?displayProperty=name> 코드 IsCanceled 속성을 통해 동일한 검색을 수행 해야 대신 호출 되는 WaitAll 호출 하기 전에 취소 된 작업을 검색 하는 방법으로 발견 되 고 되었습니다 (예:. Any(t =&gt; t.IsCanceled)) 이후 시간 제한 전에 대기 중이 던된 모든 작업을 완료 하는.NET 4.6이 경우 throw만 합니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

