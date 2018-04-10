### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument은 텍스트의 줄에 표시 될 수 있습니다.

|   |   |
|---|---|
|설명|일부 경우에는 <xref:System.Windows.Documents.FlowDocument> 에서.NET Framework 4.0에서 실행 될 때를 표시 방법에 비해.NET Framework 4.5에서 실행 중인 요소 텍스트의 줄에 표시 됩니다. 제대로 되지 않았거나, 읽을 수 없을 정도로 표시할 텍스트를 일으키는 변경의 알려진 경우가 있지만 나타날 텍스트를에서 누락 된 이전에 발생할 수 있습니다는 <xref:System.Windows.Documents.FlowDocument>의 보기입니다.|
|제안 해결 방법|경우에 따라 디스플레이 요소의 PageHeight 속성 씩 감소 이전 표시 된 줄 수를 복원할 수 있습니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

