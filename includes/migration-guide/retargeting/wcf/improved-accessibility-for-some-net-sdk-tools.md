### <a name="improved-accessibility-for-some-net-sdk-tools"></a>일부.NET SDK 도구에 대 한 향상 된 접근성

|   |   |
|---|---|
|설명|.NET Framework SDK 4.7.1 svcconfigedit.exe 및 svctraceviewer.exe 도구는 다양 한 액세스 가능성 문제를 수정 하 여 개선 되었습니다. 이들 중 대부분 올바르게 구현 되지 않은 특정 UI 자동화 패턴 또는 정의 되지 이름과 같은 작은 문제 했습니다. 많은 사용자가 이러한 잘못 된 값을 알지 수, 하는 동안 화면 판독기와 같은 보조 기술을 사용 하 여 고객 알 이러한 SDK 도구 보다 쉽게 사용할 수 있습니다. 물론, 이러한 수정 사항은 키보드 포커스 주문 등의 일부 이전 동작을 변경합니다. 이러한 도구에는 내게 필요한 옵션 수정 모두를 사용 하려면 app.config 파일에 다음 수행할 수 있습니다.<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.7.1|
|형식|대상 변경|

