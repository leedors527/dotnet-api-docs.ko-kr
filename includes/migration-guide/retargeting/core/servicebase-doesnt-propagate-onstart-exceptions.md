### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase는 OnStart 예외를 전달 하지 않습니다.

|   |   |
|---|---|
|설명|.NET Framework 4.7 및 이전 버전에서는 서비스를 시작할 때 throw 되는 예외의 호출자에 게 전파 되지 않습니다 <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>합니다. 에 대 한 예외는 전파 런타임 4.7.1.NET Framework를 대상으로 하는 응용 프로그램을 시작 <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType> 를 시작 하지 못한 서비스에 대 한 합니다.|
|제안 해결 방법|서비스 시작에는 예외가 있는 경우 해당 예외 전파 됩니다. 서비스가 시작 되지 사례를 진단 하는 데 도움이 됩니다. 다음을 추가 하 여 옵트아웃 선택할 수이 동작이 필요 없는 경우 <AppContextSwitchOverrides> 요소는 <runtime> 응용 프로그램 구성 파일의 섹션:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>응용 프로그램이 대상 4.7.1 보다 이전 버전에는 이러한 동작이 하려는 경우 다음 추가 <AppContextSwitchOverrides> 요소는 <runtime> 응용 프로그램 구성 파일의 섹션:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

