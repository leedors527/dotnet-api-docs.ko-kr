### <a name="item-scrolling-a-flat-list-with-items-of-different-pixel-height"></a>다른 픽셀 높이의 항목과 단순 목록 항목 스크롤

|   |   |
|---|---|
|설명|경우는 <xref:System.Windows.Controls.ItemsControl?displayProperty=name> 가상화를 사용 하 여 컬렉션을 표시 (<code>IsVirtualizing=true</code>) 및 항목-스크롤 (<code>ScrollUnit=Item</code>), 해당 네트워크 환경에서 해당 높이 픽셀 단위로 다른 항목을 표시 하는 컨트롤을 스크롤할 때와 <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> 모두에 대해 반복 컬렉션의 항목입니다. 이 반복 하는 동안 UI가 응답 하지 않습니다. 컬렉션 클 경우이 시스템 중단으로 감지 될 수 있는 합니다. 반복 이전.Net 버전에도 다른 상황에서 발생합니다. 예를 들어 픽셀 스크롤할 때 발생 (<code>ScrollUnit=Pixel</code>) 항목 스크롤할 때 발생 하는 다른 픽셀 높이 및 항목에 대해 계층적 데이터 (같은 <xref:System.Windows.Controls.TreeView?displayProperty=name> 또는 <xref:System.Windows.Controls.ItemsControl?displayProperty=name> 그룹화를 사용 하도록 설정)를 가진 항목이 있을 때는 다른 인접 보다 하위 항목 수입니다. 항목 스크롤 및 다른 픽셀 높이의 사례에 대 한 반복 계층적 데이터의 레이아웃에 버그를 수정 하는.Net 4.6.1에서에서 도입 되었습니다.  (계층 없음)를 플랫 하며.Net 4.6.2 수행 하지 않습니다 것이 경우 데이터는 필요 하지 않습니다.|
|제안 해결 방법|발생 하는 경우 반복 이전 릴리스에서-있지만.Net 4.6.1에에서, 즉 경우는 <xref:System.Windows.Controls.ItemsControl?displayProperty=name> 는 스크롤 단순 목록 항목--다른 픽셀 높이의 항목으로는 두 해결 방법을 찾으려면:<ol><li>.NET 4.6.2를 설치 합니다.</li><li>.NET 4.6.1 용 HR 1605 핫픽스를 설치 합니다.</li></ol>|
|범위|부|
|버전|4.6.1|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=nameWithType></li></ul>|

