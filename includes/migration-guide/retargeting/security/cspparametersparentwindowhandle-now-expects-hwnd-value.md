### <a name="cspparametersparentwindowhandle-now-expects-hwnd-value"></a>CspParameters.ParentWindowHandle 이제 HWND 값이 필요 하며

|   |   |
|---|---|
|설명|<xref:System.Security.Cryptography.CspParameters.ParentWindowHandle> 값,.NET Framework 2.0에 도입 된 키에 액세스 하는 데 필요한 모든 UI를 부모 창 핸들 값을 등록 하는 응용 프로그램을 사용 하면 (PIN 같은 메시지를 표시 또는 동의 대화 상자)에 지정된 된 창의 모달 하위로 열립니다. .NET Framework 4.7를 대상으로 하는 앱 부터는 Windows Forms 응용 프로그램을 설정할 수는 <xref:System.Security.Cryptography.CspParameters.ParentWindowHandle> 다음과 같은 코드를 사용 하 여 속성:<pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre>.NET Framework의 이전 버전에서는 값 있을 것으로 예상는 <xref:System.IntPtr?displayProperty=name> 메모리 내의 위치를 나타내는 위치는 [HWND](https://msdn.microsoft.com/library/windows/desktop/aa383751.aspx#HWND) 내 상주 하는 값입니다. 이 속성 폼을 설정 합니다. Windows 7에서 처리 하 고 이전 버전 아무런 영향이 있지만 Windows 8 이상 버전에서 발생 한 &quot; <xref:System.Security.Cryptography.CryptographicException?displayProperty=name>: 매개 변수가 올바르지 않습니다.&quot;|
|제안 해결 방법|응용 프로그램이.NET 4.7 대상 또는 부모 창 관계를 등록 하려는 높을수록 간소화 된 형식을 사용 하도록:<pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre>사용자에 게 전달 하려면 올바른 값이 값을 보유 하는 메모리 위치 주소 되었음을 확인 된 <code>form.Handle</code> AppContext 스위치를 설정 하 여 동작 변경 하지 않을 수 <code>Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle</code> 를 <code>true</code>합니다.<ol><li>프로그래밍 방식으로 설정 하 여 compat에서 전환 하는 AppContext 설명 된 대로 [여기](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</li><li>다음 줄을 app.config 파일의 <code>&lt;runtime&gt;</code> 섹션에 추가</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>이전.NET Framework 버전에서의 응용 프로그램 작업 부하는 AppContext를 설정할 수 있습니다 때 새.NET Framework 4.7 런타임 동작에 참여 하도록 하려는 사용자에 게로 전환 하는 반면 <code>false</code>합니다.|
|범위|부|
|버전|4.7|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Security.Cryptography.CspParameters.ParentWindowHandle?displayProperty=nameWithType></li></ul>|

