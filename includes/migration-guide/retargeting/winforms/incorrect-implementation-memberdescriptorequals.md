### <a name="incorrect-implementation-of-memberdescriptorequals"></a>MemberDescriptor.Equals 잘못 구현

|   |   |
|---|---|
|설명|기본 구현을 &quot;Equals&quot; 메서드 비교에서 개체에서 두 개의 서로 다른 문자열 속성을 비교 했습니다: 설명 문자열에 범주 이름입니다. 비교 하는 것의 수정이 반영 &quot;범주&quot; 첫 번째 개체의 &quot;범주&quot; 의 차이 및 &quot;설명&quot; 를 &quot;설명&quot;합니다. 4.6.2를 대상으로 하는 경우 새로운 동작을 취소 하기 위해 true로 또는 대상 framework 버전 4.6.2 미달 하는 경우이 해결 방법을 사용 하도록 설정 하려면 false로 MemberDescriptorEqualsReturnsFalseIfEquivalent 구성 값을 설정할 수 있습니다.|
|제안 해결 방법|경우에 따라 false를 반환 하는 MemberDescriptor.Equals에 종속 되는 응용 프로그램 경우 설명자 동일 하며 4.6.2 대상으로 하는 버전의.NET Framework에 몇 가지 옵션이 있습니다.<ol><li>비교할 코드 변경 &quot;범주&quot; 및 &quot;설명&quot; Equals 메서드 실행 외에도 수동으로 필드입니다.</li><li>App.config 파일에 다음 값을 추가 하 여 이러한 변경으로 인해 옵트아웃:</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>응용 프로그램이 대상 4.6.1 나.NET Framework의 낮은 버전에이 변경 내용을 사용 하도록 설정 하려면, app.config 파일에 다음 값을 추가 하 여 호환성 스위치를 false로 설정할 수 있습니다.<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.6.2|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

