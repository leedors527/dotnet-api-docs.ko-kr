### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView ArgumentOutOfRangeException를 발생 시킵니다.

|   |   |
|---|---|
|설명|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> 열 가상화를 사용할 수 있지만 열 너비 아직 확인 되지 않아 비동기적으로 작동 합니다.  비동기 작업이 발생 하기 전에 열 제거는 <xref:System.ArgumentOutOfRangeException?displayProperty=name> 발생할 수 있습니다.|
|제안 해결 방법|다음 중 하나:<ol><li>4.7.NET으로 업그레이드 합니다.</li><li>.NET 4.6.2 용 최신 서비스 패치를 설치 합니다.</li><li>열에 대 한 비동기 응답 될 때까지 제거 되지 않도록 <xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> 완료 되었습니다.</li></ol>|
|범위|Microsoft Edge|
|버전|4.6.2|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

