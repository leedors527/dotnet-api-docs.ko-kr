### <a name="serialport-background-thread-exceptions"></a>SerialPort 백그라운드 스레드 예외

|   |   |
|---|---|
|설명|백그라운드 스레드를 사용 하 여 만든 <xref:System.IO.Ports.SerialPort> OS 예외가 throw 되 면 스트림 프로세스를 더 이상 종료 합니다. .NET Framework 4.7 및 이전 버전을 대상으로 하는 응용 프로그램에서 프로세스를 사용 하 여 만든 백그라운드 스레드는 운영 체제 예외가 throw 되 면 종료할는 <xref:System.IO.Ports.SerialPort> 스트림 합니다. 응용 프로그램에는 대상.NET Framework 4.7.1 또는 이후 버전 백그라운드 스레드 OS 이벤트에 대 한 활성 직렬 포트와 관련 기다렸다가 작동이 중단 되는 직렬 포트의 급격 한 제거 같은 일부 경우에.|
|제안 해결 방법|4.7.1.NET Framework를 대상으로 하는 응용 프로그램의 경우이 필요 없는 경우 다음을 추가 하 여 예외 처리에서 선택할 수 있습니다는 <code>&lt;runtime&gt;</code> 섹션 프로그램 <code>app.config</code> 파일:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>대상으로 하는 앱에 대 한 이전 버전의.NET Framework는 하지만 4.7.1.NET Framework에서 실행 하거나 나중에 선택할 수 있습니다 다음을 추가 하 여 처리 하는 예외는 <code>&lt;runtime&gt;</code> 섹션 프로그램 <code>app.config</code> 파일:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

