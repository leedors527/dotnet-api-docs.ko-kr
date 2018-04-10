### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>WPF TreeView 또는 그룹화 된 목록 상자는 VirtualizingStackPanel에 스크롤 시스템 중지가 발생할 수 있습니다.

|   |   |
|---|---|
|설명|.NET Framework v 4.5의 WPF 스크롤 <xref:System.Windows.Controls.TreeView?displayProperty=name> 가상화 스택에서 뷰포트에 여백 경우 패널 중지 발생할 수 있습니다 (의 항목은 <xref:System.Windows.Controls.TreeView?displayProperty=name>, 예를 들어 또는 ItemsPresenter 요소에). 또한 일부 경우에는 보기에서 다양한 크기의 항목은 여백이 없더라도 불안정해 보일 수 있습니다.|
|제안 해결 방법|.NET Framework 4.5.1로 업그레이드하여 이 버그를 방지할 수 있습니다. 또는 컬렉션 보기에서에서 여백을 제거할 수 있습니다 (같은 <xref:System.Windows.Controls.TreeView?displayProperty=name>s) 가상화 스택 내에서 모든 항목을 포함 하는 경우 패널은 동일한 크기입니다.|
|범위|주요함|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

