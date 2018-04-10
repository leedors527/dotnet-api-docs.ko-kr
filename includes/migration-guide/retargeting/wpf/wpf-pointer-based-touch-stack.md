### <a name="wpf-pointer-based-touch-stack"></a>WPF 포인터 기반 터치 스택

|   |   |
|---|---|
|설명|이 변경은 선택적 WM_POINTER를 사용할 수 있는 기능에는 WPF 터치/스타일러스 스택 기반 추가 합니다.  이 명시적으로 사용 하지 않는 개발자 WPF 터치/스타일러스 동작은 변경 되지 않습니다 나타나야 합니다. 선택적 WM_POINTER 알려진 문제를 현재 따라 터치/스타일러스 스택:<ul><li>실시간 잉크 기능을 지원하지 않습니다.</li><li>잉크 입력 하는 동안 스타일러스 플러그 인은 계속 작동 하 고, 성능이 저하 될 수 있는 UI 스레드에서 처리 됩니다.</li><li>마우스 이벤트에 터치/스타일러스 이벤트에서 프로 모션의 변경으로 인해 변경 된 동작</li><li>조작 다르게 동작할 수 있습니다.</li><li>끌기/놓기 터치식 입력에 대 한 적절 한 피드백이 표시 되지 않습니다.</li><li>스타일러스 입력 내용은 적용 되지 않습니다.</li><li>끌기/놓기 터치/스타일러스 이벤트에서 더 이상 시작할 수 없습니다.</li><li>이로 인해 마우스 입력이 감지될 때까지 응용 프로그램이 중단될 수 있습니다.</li><li>대신, 개발자는 마우스 이벤트에서 끌어서 놓기를 시작하는 것이 좋습니다.</li></ul>|
|제안 해결 방법|이 스택 하려는 개발자가 수 추가/병합이 응용 프로그램의 App.config 파일에 다음:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Input.Stylus.EnablePointerSupport=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>이 제거 하거나 값을 false로 설정 꺼집니다이 선택적 스택. 이 스택은 Windows 10 작성자가 업데이트에 대해서만 이상 사용할 수 note 하십시오.|
|범위|Microsoft Edge|
|버전|4.7|
|형식|대상 변경|

