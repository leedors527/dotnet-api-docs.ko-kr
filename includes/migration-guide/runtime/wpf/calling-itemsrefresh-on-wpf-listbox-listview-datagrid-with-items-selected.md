### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>WPF ListBox, ListView 항목 선택 된 상태로 DataGrid에서 호출 Items.Refresh 요소에 중복 항목이 발생할 수 있습니다.

|   |   |
|---|---|
|설명|항목을 선택 하는 동안 ListBox.Items.Refresh 코드에서 호출 하는.NET Framework 4.5에서는 <xref:System.Windows.Controls.ListBox?displayProperty=name> 선택한 항목 목록에서 중복을 발생할 수 있습니다. 유사한 문제가 발생 된 <xref:System.Windows.Controls.ListView?displayProperty=name> 및 <xref:System.Windows.Controls.DataGrid?displayProperty=name>합니다. 이것은 .NET Framework 4.6에서 수정되었습니다.|
|제안 해결 방법|프로그래밍 하기 전에 항목 선택을 취소 하 여이 문제를 해결할 수 있습니다 <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> 다음 호출이 완료 된 후에 다시 선택 하 고 호출 됩니다. 또는 .NET Framework 4.6에서 이 문제가 수정되어 해당 버전의 .NET Framework로 업그레이드하여 해결할 수 있습니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

