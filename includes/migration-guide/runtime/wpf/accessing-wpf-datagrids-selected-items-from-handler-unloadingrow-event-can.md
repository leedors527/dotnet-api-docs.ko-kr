### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>DataGrid의 UnloadingRow 이벤트의 처리기에서 WPF DataGrid의 선택한 항목에 액세스 하면 nullreferenceexception이 발생 될 수 있습니다.

|   |   |
|---|---|
|설명|.NET Framework 4.5에 대 한 이벤트 처리기의 버그 때문 <xref:System.Windows.Controls.DataGrid> 행을 제거 하 고 관련 된 이벤트로 인해 발생할 수 있습니다는 <xref:System.NullReferenceException?displayProperty=name> 액세스 하는 경우 throw 되는 <xref:System.Windows.Controls.DataGrid>의 <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> 또는 <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> 속성입니다.|
|제안 해결 방법|이 문제는.NET Framework 4.6에서 수정 되었습니다 및.NET Framework의 해당 버전으로 업그레이드 하 여 해결 될 수도 있습니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

