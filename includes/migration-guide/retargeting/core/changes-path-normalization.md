### <a name="changes-in-path-normalization"></a>경로 정규화의 변경 내용

|   |   |
|---|---|
|설명|앱 부터는.NET Framework 4.6.2 대상, 런타임에서는 경로 정규화 하는 방식 변경 되었습니다. 정규화 된 경로 대상 운영 체제에서 올바른 경로를 따르도록 경로 또는 파일을 식별 하는 문자열을 수정 해야 합니다. 정규화에는 일반적으로 다음이 수행됩니다.<ul><li>구성 요소 및 디렉터리 구분 기호 정규화</li><li>상대 경로에 현재 디렉터리 적용</li><li>경로에서 부모 디렉터리 (.) 또는 상대 디렉터리 (.)을 평가 합니다.</li><li>지정된 문자 자르기</li></ul>부터는 앱 대상으로 하는.NET Framework 4.6.2 경로 정규화의 다음 변경 내용은 기본적으로 활성화 됩니다.<ul><li>런타임은 운영 체제의 [GetFullPathName](https://msdn.microsoft.com/library/windows/desktop/aa364963(v=vs.85).aspx) 함수를 지연시켜 경로를 정규화합니다.</li><li>정규화 중에 더 이상 디렉터리 세그먼트의 끝(예: 디렉터리 이름 끝의 공백)이 잘리지 않습니다.</li><li>완전 신뢰에서 장치 경로 구문에 대 한 지원을 포함 하 여 <code>\\.\</code> and, for file I/O APIs in mscorlib.dll, '\?'.</li><li>The runtime does not validate device syntax paths.</li><li>The use of device syntax to access alternate data streams is supported.</li></ul>These changes improve performance while allowing methods to access previously inaccessible paths. Apps that target the .NET Framework 4.6.1 and earlier versions but are running under the .NET Framework 4.6.2 or later are unaffected by this change.|
|제안 해결 방법|.NET Framework 4.6.2 대상으로 하거나 나중에 않을 수 있습니다이 앱을 변경 하 고 다음을 추가 하 여 레거시 정규화를 사용는 <code>&lt;runtime&gt;</code> 응용 프로그램 구성 파일의 섹션:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>.NET Framework 4.6.1 또는 이전 이지만 대상으로 하는 응용 프로그램은.NET Framework 4.6.2에서 실행 중인 또는 나중에 다음 줄을 추가 하 여 경로 정규화에 변경 내용을 활성화할 수는 <code>&lt;runtime&gt;</code> .configuration 응용 프로그램 파일의 섹션:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.6.2|
|형식|대상 변경|

