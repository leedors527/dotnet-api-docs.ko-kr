### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>True로, allowcustompaging은 설정 된 Gridview PageIndexChanging 이벤트 보기의 마지막 페이지를 벗어날 때 실행 될 수 있습니다.

|   |   |
|---|---|
|설명|.NET Framework 4.5의 버그로 인해 <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> 때로는 대 한 발생 하지 않도록 <xref:System.Web.UI.WebControls.GridView?displayProperty=name>사용 하도록 설정한 s <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>합니다.|
|제안 해결 방법|이 문제는.NET Framework 4.6에서 수정 되었습니다 및.NET Framework의 해당 버전으로 업그레이드 하 여 해결 될 수도 있습니다. 해결 방법으로, 응용 프로그램에는 명시적 BindGrid 수행할 수 <code>Page_Load</code> 이러한 상황을 적중 하는 (의 <xref:System.Web.UI.WebControls.GridView?displayProperty=name> 은 마지막 페이지 및 마지막<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> 간에 차이가 있는 <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>). 또는 앱 처럼이 시나리오 문제를 보여 주지 않습니다 (대신 사용자 지정 페이징), 페이징을 허용 하도록 수정할 수 있습니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

