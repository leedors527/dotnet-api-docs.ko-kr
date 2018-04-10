### <a name="wpf-treeviewitem-must-be-used-within-a-treeview"></a>WPF TreeViewItem TreeView 내에서 사용 해야 합니다.

|   |   |
|---|---|
|설명|변경의 사용량을 제한 하는 4.5에서 도입 된 <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> 의 외부 요소는 <xref:System.Windows.Controls.TreeView?displayProperty=name>합니다. 이것은 다음과 같은 경우에 매니페스트할 수 있습니다.<ul><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=name>시각적 부모가 패널 아닙니다. (A <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> 에 대해 생성 된 <xref:System.Windows.Controls.TreeView?displayProperty=name> 부모로 패널 갖습니다)</li><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=name> 노드의 하위는 <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> 역할을 하는 &quot;항목 호스트&quot; (ListBox, DataGrid, ListView 등) 목록 컨트롤에 대 한 합니다. 가상화를 사용할 필요가 없습니다.</li><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> 항목 스크롤 됩니다 (<code>ScrollUnit=&quot;Item&quot;</code>).</li><li>누군가 <code>VirtualizingStackPanel.MakeVisible(v)</code>을 호출하여 요소 <code>v</code>를 보기로 스크롤합니다. 이것은 명시적으로 또는 암시적인 몇 가지 방법으로 실행될 수 있습니다. 아마도 가장 일반적인 방법은 간단히 <code>v</code>를 클릭하여 키보드 포커스를 부여하는 것입니다.</li><li>시각적 부모가 체인 <code>v</code> 에 <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> 통과 <xref:System.Windows.Controls.TreeViewItem?displayProperty=name>합니다.</li></ul>즉,이 표시 됩니다 때는 <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> 외부에서 사용 되는 <xref:System.Windows.Controls.TreeView?displayProperty=name>, 되 고 사용자가의 하위 항목에는 <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> 를 뷰로 가져옵니다. 경우는 <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> 포커스 하위 항목이 없는,이 문제가 표시 되지 않습니다. 이 적중 될 경우의 예는 경우는 <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> DataTemplate의 루트입니다. 이 문제가 적중하면 WPF 프레임워크 내에 InvalidCastException가 발생합니다.|
|제안 해결 방법|이것을 위해 사용 가능한 핫픽스가 생성됩니다.|
|범위|부|
|버전|4.5|
|형식|런타임|

