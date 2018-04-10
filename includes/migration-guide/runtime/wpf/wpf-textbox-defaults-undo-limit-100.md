### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>WPF TextBox 기본값 제한인 100 개를 실행 취소 하려면

|   |   |
|---|---|
|설명|.NET 4.5에서는 WPF TextBox에 대한 실행 취소 제한 기본값은 100(.NET 4.0에서 무제한이던 것과 반대)|
|제안 해결 방법|사용 제한은 실행 취소 제한 100 너무 낮으면 명시적으로 설정할 수 있습니다. <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

