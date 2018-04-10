### <a name="workflow-checksums-changed-from-md5-to-sha1"></a>MD5에서 s h a 1로 변경 하는 워크플로 체크섬

|   |   |
|---|---|
|설명|Visual Studio를 사용 하 여 디버깅을 지원 하려면 워크플로 런타임에서 해시 알고리즘을 사용 하 여 워크플로 인스턴스에 대 한 체크섬을 생성 합니다. .NET Framework 4.6.2 및 이전 버전에서 워크플로 체크섬 해시 사용 하는 FIPS 활성화 시스템에서 문제를 일으킨 MD5 알고리즘입니다. .NET Framework 4.7 부터는 알고리즘은 s h a 1입니다. 이러한 체크섬을 유지 하는 코드 경우은 호환 되지 않을 수 있습니다.|
|제안 해결 방법|코드 체크섬 오류로 인해 워크플로 인스턴스를 로드할 수 없는 경우 설정 해 보십시오.는 <code>AppContext</code> 전환 &quot;Switch.System.Activities.UseMD5ForWFDebugger&quot; true로 합니다. 코드:<pre><code class="language-csharp">System.AppContext.SetSwitch(&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;, true);&#13;&#10;</code></pre>또는 구성:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Activities.UseMD5ForWFDebugger=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7|
|형식|대상 변경|

