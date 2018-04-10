### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>간헐적으로 하지 않습니다. (예: 목록 상자 및 DataGrid) ItemsControls 항목 아래쪽으로 스크롤하여 DataTemplates 사용자 지정을 사용 하는 경우

|   |   |
|---|---|
|설명|어떤 경우에는.NET Framework 4.5의 버그를 일으키는지 ItemsControls (같은 <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>등) DataTemplates 사용자 지정을 사용 하는 경우 해당 항목의 아래쪽 하지 스크롤합니다. 스크롤이 두 번째 시도되는 경우(스크롤 백업 후) 그때에는 작동합니다.|
|제안 해결 방법|.NET Framework 4.5.2에서 이 문제가 수정되어 해당 버전(또는 이후 버전)의 .NET Framework로 업그레이드하여 해결할 수 있습니다. 또는 사용자가 이러한 컬렉션의 마지막 항목까지 스크롤 막대를 끌 수 있지만 성공하려면 두 번 시도해야 할 수 있습니다.|
|범위|부|
|버전|4.5|
|형식|런타임|

