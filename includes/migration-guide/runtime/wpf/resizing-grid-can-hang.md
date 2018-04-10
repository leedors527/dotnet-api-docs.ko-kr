### <a name="resizing-a-grid-can-hang"></a>눈금 크기 조정 중지 될 수 있다

|   |   |
|---|---|
|설명|레이아웃 하는 동안 무한 루프가 발생할 수 있습니다는 <code>T:System.Windows.Controls.Grid</code> 다음과 같은 경우:<ul><li>행 정의 포함 되어 두 *-행는 MinHeight 및는 최대 높이 모두 선언 합니다.</li><li>콘텐츠는 *-행 해당 최대 높이 초과 하지 않는지</li><li>표의 높이 초과 하 여 첫 번째 MinHeight 하 (및 다른 모든 고정 또는 자동으로 행)</li><li>응용 프로그램.Net 4.7, 대상 또는 옵트인 하 고 4.7 할당 알고리즘을 설정 하 여 <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>루프는 두 개 이상의 행 또는 열에 대 한 유사한 경우에 이루어집니다. 이 문제는.Net 4.7.1에서에서 해결 됩니다.|
|제안 해결 방법|4.7.1.Net으로 업그레이드 합니다.  또는 4.7 할당 알고리즘 필요 하지 않으면 다음 구성 설정을 사용할 수 있습니다.<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.7|
|형식|런타임|

