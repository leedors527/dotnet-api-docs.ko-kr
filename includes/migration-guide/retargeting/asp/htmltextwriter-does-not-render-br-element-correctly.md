### <a name="htmltextwriter-does-not-render-br-element-correctly"></a>HtmlTextWriter 렌더링 하지 않습니다 `<br/>` 요소 올바르게

|   |   |
|---|---|
|설명|.NET Framework 4.6부터 <code>&lt;BR /&gt;</code> 요소로 <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> 및 <xref:System.Web.UI.HtmlTextWriter.RenderEndTag>를 호출하면 (두 개가 아닌) 단 하나의 <code>&lt;BR /&gt;</code>만 올바르게 삽입합니다.|
|제안 해결 방법|응용 프로그램이 추가 <code>&lt;BR /&gt;</code> 태그에 종속된 경우 <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)>를 두 번째로 호출해야 합니다. 이 동작은 변경만.NET Framework 4.6 이상을 대상으로 또 다른 옵션은 이전 동작을 얻기 위해 이전 버전의.NET Framework를 대상으로 하므로 앱을 영향을 줍니다.|
|범위|Microsoft Edge|
|버전|4.6|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|

