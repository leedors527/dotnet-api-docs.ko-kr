### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>Items.Clear는 SelectedItems에서 중복 항목을 제거 하지 않습니다.

|   |   |
|---|---|
|설명|(여러 선택 영역을 사용 하도록 설정) 된 선택기 중복 된 경우를 가정해 볼 해당 <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> 수집-같은 항목이 표시 두 번 이상.  제거할 수 없으며 (예: 호출 하 여 Items.Clear) 데이터 원본에서 해당 항목을 제거 <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>만 첫 번째 인스턴스를 제거 합니다. 또한 이후에 사용 하는 <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> (예: SelectedItems.Clear()) 문제가 발생할 수와 같은 <xref:System.ArgumentException?displayProperty=name>때문에, <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> 더 이상 데이터 원본에 있는 항목을 포함 합니다.|
|제안 해결 방법|.NET 4.6.2 가능 하면를 업그레이드 합니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

