### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF serialize Expressions.Literal&lt;T&gt; Datetime 이제 다르게 (사용자 지정 XAML 파서가 중단)

|   |   |
|---|---|
|설명|연결 된 <xref:System.Windows.Markup.ValueSerializer> 개체는 변환는 <xref:System.DateTime?displayProperty=name> 또는 <xref:System.DateTimeOffset?displayProperty=name> 두 번째 개체 및 <xref:System.DateTime.Millisecond?displayProperty=name> 구성 요소는 0이 아닌 및 (에 대 한는 <xref:System.DateTime?displayProperty=name> 값) 인 <xref:System.DateTime.Kind> 속성 요소에 지정 되지 않은 속성이 아닙니다. 문자열 대신 구문입니다. 이 변경은 <xref:System.DateTime?displayProperty=name> 및 <xref:System.DateTimeOffset?displayProperty=name> 값이 라운드트립되는 것을 허용합니다. 입력 XAML이 특성 구문에 있다고 가정하는 사용자 지정 XAML 파서가 올바르게 작동하지 않습니다.|
|제안 해결 방법|이 변경은 <xref:System.DateTime?displayProperty=name> 및 <xref:System.DateTimeOffset?displayProperty=name> 값이 라운드트립되는 것을 허용합니다. 입력 XAML이 특성 구문에 있다고 가정하는 사용자 지정 XAML 파서가 올바르게 작동하지 않습니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|

