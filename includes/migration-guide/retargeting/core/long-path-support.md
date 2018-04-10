### <a name="long-path-support"></a>긴 경로 지원

|   |   |
|---|---|
|설명|(최대 32 K 문자)의.NET Framework 4.6.2, 긴 경로 지원 대상으로 하 고 260 자는 앱 부터는 (또는 <code>MAX_PATH</code>) 경로 길이 제한이 제거 되었습니다. .NET Framework 4.6.2를 대상으로 다시 컴파일되는 앱에 대 한 코드 경로 이전에 시킨는 <xref:System.IO.PathTooLongException?displayProperty=name> 260 자 throw 합니다 초과 하는 경로 <xref:System.IO.PathTooLongException?displayProperty=name> 다음과 같은 경우에만:<ul><li>경로 길이 보다 크면 <xref:System.Int16.MaxValue> (32767) 문자.</li><li>운영 체제가 <code>COR_E_PATHTOOLONG</code> 또는 동급을 반환하는 경우</li></ul>.NET Framework 4.6.1 및 이전 버전을 대상으로 하는 응용 프로그램의 경우 런타임에서 자동으로 throw 한 <xref:System.IO.PathTooLongException?displayProperty=name> 경로 260 자를 초과할 때마다 합니다.|
|제안 해결 방법|.NET Framework 4.6.2를 대상으로 하는 응용 프로그램의 경우 선택할 수 있습니다 긴 경로 지원 되지 것 필요 없는 경우 다음을 추가 하 여는 <code>&lt;runtime&gt;</code> 섹션 프로그램 <code>app.config</code> 파일:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>대상으로 하는 앱에 대 한 이전 버전의.NET Framework는 하지만.NET Framework 4.6.2에서 실행 하거나 나중에 선택할 수 있습니다 긴 경로 지원에 다음을 추가 하 여는 <code>&lt;runtime&gt;</code> 섹션 프로그램 <code>app.config</code> 파일:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.6.2|
|형식|대상 변경|

