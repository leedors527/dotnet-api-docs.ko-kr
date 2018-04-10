### <a name="wpf-layout-rounding-of-margins-has-changed"></a>변경 된 여백이 WPF 레이아웃 반올림

|   |   |
|---|---|
|설명|여백이 반올림되는 방식과 그 안의 테두리 및 배경이 변경되었습니다. 레이아웃을 변경한 결과는 다음과 같습니다.<ul><li>요소의 너비나 높이가 최대 1픽셀씩 늘어나거나 줄어들 수 있습니다.</li><li>개체의 배치가 최대 1픽셀씩 이동할 수 있습니다.</li><li>가운데 맞춤 요소가 가로 또는 세로로 최대 1픽셀씩 가운데에서 벗어날 수 있습니다.</li></ul>기본적으로 이 새 레이아웃은 .NET Framework 4.6을 대상으로 하는 앱에 대해서만 사용할 수 있습니다.|
|제안 해결 방법|이전 버전의.NET Framework를 대상으로 하지만.NET Framework 4.6에서 실행 되는 앱이이 수정 오른쪽 또는 높은 Dpi에서 WPF 컨트롤의 아래쪽의 클리핑을 제거 하는 경향이, 때문에 다음 줄을 추가 하 여이 새로운 동작으로 선택할 수는 <code>&lt;runtime&gt;</code> app.config 파일의 섹션: <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=false&quot; /&gt;</code>를.NET Framework 4.6을 대상으로 하지만 이전 레이아웃 알고리즘을 사용 하 여 렌더링에 WPF 컨트롤을 원하는 앱에 다음 줄을 추가 하 여 수행할 수는 <code>&lt;runtime&gt;</code> app.config 파일의 섹션: <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=true&quot; /&gt;</code>.|
|범위|부|
|버전|4.6|
|형식|대상 변경|

