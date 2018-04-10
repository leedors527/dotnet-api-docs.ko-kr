### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>포커스 삭제 DataGrid.CommitEdit CellEditEnding 처리기에서 호출

|   |   |
|---|---|
|설명|호출 <xref:System.Windows.Controls.DataGrid.CommitEdit> 중 하나에서 <xref:System.Windows.Controls.DataGrid?displayProperty=name>의 <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> 하면 이벤트 처리기는 <xref:System.Windows.Controls.DataGrid?displayProperty=name> 포커스를 잃고 합니다.|
|제안 해결 방법|이 버그는 .NET Framework 4.5.2에서 수정되었으므로 .NET Framework를 업그레이드하여 방지할 수 있습니다. 또는 명시적으로 다시 선택 하 여 방지할 수 있습니다는 <xref:System.Windows.Controls.DataGrid?displayProperty=name> 호출한 후 <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>합니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

