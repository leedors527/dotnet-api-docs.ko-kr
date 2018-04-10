### <a name="wpf-datatemplate-elements-are-now-visible-to-uia"></a>WPF DataTemplate 요소 UIA에 표시 됩니다.

|   |   |
|---|---|
|설명|이전에 <xref:System.Windows.DataTemplate?displayProperty=name> 요소 UI 자동화에 표시 되지 않았습니다. 4.5부터는 UI 자동화가 이러한 요소를 감지합니다. 이 대부분의 경우에 유용 하지만 UIA 트리를 포함 하지 않음에 의존 하는 테스트를 분석할 수 <xref:System.Windows.DataTemplate?displayProperty=name> 요소입니다.|
|제안 해결 방법|UI 자동화 테스트이 앱이 할 수에 대 한 업데이트 이전에 표시 되지 않는 포함 하 여 이제 UIA 트리에 대 한 설명 하기 위해 <xref:System.Windows.DataTemplate?displayProperty=name> 요소입니다. 예를 들어 일부 요소가 서로 옆에 있도록 예상하는 테스트는 이제 이전에 요소 간에 보이지 않던 UIA 요소를 예상해야 할 수 있습니다. 또는 UIA 요소에 대한 특정 개수 또는 인덱스를 사용하는 테스트는 새 값으로 업데이트해야 할 수 있습니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.DataTemplate.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.DataTemplate.%23ctor(System.Object)?displayProperty=nameWithType></li></ul>|

