### <a name="exceptions-during-unobserved-processing-in-systemthreadingtaskstask-no-longer-propagate-on-finalizer-thread"></a>더 이상에서 System.Threading.Tasks.Task에서 관찰 되지 않은 처리 하는 동안 예외가 종료자 스레드에서 전파

|   |   |
|---|---|
|설명|<xref:System.Threading.Tasks.Task?displayProperty=name> 클래스는 비동기 작업을 나타내기 때문에 비동기 처리를 하는 동안 발생하는 심각하지 않은 예외를 모두 catch합니다. .NET Framework 4.5에서는 예외가 관찰되지 않고 코드가 작업에서 대기하지 않으면 예외는 더 이상 종료자 스레드에서 전파되지 않고 가비지 수집 도중 프로세스와 충돌합니다. 이러한 변경으로 인해 관찰되지 않은 비동기 처리를 수행하기 위해 Task 클래스를 사용하는 응용 프로그램의 안정성이 향상됩니다.|
|제안 해결 방법|종료자 스레드에 완전히 전파 관찰 되지 않은 비동기 예외에 종속 되는 응용 프로그램, 이전 동작에 대 한 적절 한 처리기를 제공 하 여 복원할 수 있습니다는 <xref:System.Threading.Tasks.TaskScheduler.UnobservedTaskException> 이벤트를 설정 하거나는 [런타임 구성 요소 ](~/docs/framework/configure-apps/file-schema/runtime/throwunobservedtaskexceptions-element.md).|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Threading.Tasks.Task.Run(System.Action)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.Run(System.Action,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.Run(System.Func{System.Threading.Tasks.Task})?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.Run(System.Func{System.Threading.Tasks.Task},System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.Run%60%601(System.Func{%60%600})?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.Run%60%601(System.Func{%60%600},System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.Run%60%601(System.Func{System.Threading.Tasks.Task{%60%600}})?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.Run%60%601(System.Func{System.Threading.Tasks.Task{%60%600}},System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.Start?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.Start(System.Threading.Tasks.TaskScheduler)?displayProperty=nameWithType></li></ul>|

