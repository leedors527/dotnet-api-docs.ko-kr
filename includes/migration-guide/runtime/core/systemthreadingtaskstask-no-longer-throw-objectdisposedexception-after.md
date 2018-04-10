### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>개체가 삭제 된 후 더 이상에서 System.Threading.Tasks.Task ObjectDisposedException throw

|   |   |
|---|---|
|설명|제외 하 고 <xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>, <xref:System.Threading.Tasks.Task?displayProperty=name> 메서드는 더 이상 throw는 <xref:System.ObjectDisposedException?displayProperty=name> 는 개체가 삭제 된 후에 예외입니다. 이 변경은 캐시 된 작업의 사용을 지원 합니다. 예를 들어, 메서드는 새로운 작업을 할당하는 대신에 이미 완료된 작업을 나타내기 위해 캐시된 작업을 반환할 수 있습니다. 작업의 모든 소비자는 다시 사용할 수 없게 렌더링된 작업을 삭제할 수 있었기 때문에 이전 .NET Framework 버전에서는 이것이 불가능했습니다.|
|제안 해결 방법|작업 메서드가 더 이상 throw 될 수 없습니다 유의 <xref:System.ObjectDisposedException?displayProperty=name> 는 개체가 삭제 된 경우에서. 앱이이 예외는 작업이 삭제 되었습니다 알아야에 따라 되었습니다, 하는 경우 명시적으로 작업의 상태를 확인 하도록 업데이트 되어야 합니다를 사용 하 여 <xref:System.Threading.Tasks.Task.Status>합니다.|
|범위|부|
|버전|4.5|
|형식|런타임|

