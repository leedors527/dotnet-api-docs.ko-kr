### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a>WPF 창이 단일 모니터 외부로 확장 하는 경우 클리핑 없이 렌더링 됩니다.

|   |   |
|---|---|
|설명|.NET Framework 4.6 실행 중일 때 Windows 8 이상을 다중 모니터 시나리오에서 단일 디스플레이 벗어나 확장 될 때에 전체 창은 클리핑 없이 렌더링 됩니다. 이 이전 버전의 WPF 창이 단일 디스플레이 벗어나 확장을 자르는 것는.NET Framework와 다릅니다.|
|제안 해결 방법|이 동작은 (잘라 여부 여부) 명시적으로 설정할를 사용 하 여는 <code>&lt;EnableMultiMonitorDisplayClipping&gt;</code> 요소에 <code>&lt;appSettings&gt;</code> 하거나 설정 하는 응용 프로그램의 구성 파일에는 <code>EnableMultiMonitorDisplayClipping</code> 앱을 시작할 때 속성.|
|범위|부|
|버전|4.6|
|형식|런타임|

