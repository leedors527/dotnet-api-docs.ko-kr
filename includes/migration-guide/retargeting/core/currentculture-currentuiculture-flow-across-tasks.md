### <a name="currentculture-and-currentuiculture-flow-across-tasks"></a>태스크에 걸쳐 CurrentCulture 및 CurrentUICulture 흐름

|   |   |
|---|---|
|설명|.NET Framework 4.6부터 <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> 및 <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> 스레드의에 저장 된 <xref:System.Threading.ExecutionContext?displayProperty=name>는 비동기 작업 전체를 이동 합니다. 이 변경을 의미 <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> 또는 <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> 나중에 비동기적으로 실행 되는 작업에 반영 됩니다. 이 이전.NET Framework 버전의 동작은 다릅니다 (약 사용할 수 있는 <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> 및 <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> 모든 비동기 작업에서).|
|제안 해결 방법|앱이이 변경의 영향을 명시적으로 원하는 설정 하 여 주위 못할 <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> 또는 <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> 는 비동기 작업의에서 첫 번째 작업으로 합니다. 이전 동작 또는 (흐르지의 <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) 다음 호환성 스위치를 설정 하 여 옵트인 수 있습니다.<pre><code class="language-C#">AppContext.SetSwitch(&quot;Switch.System.Globalization.NoAsyncCurrentCulture&quot;, true);&#13;&#10;</code></pre>이 문제는.NET Framework 4.6.2에서에서 WPF에 의해 해결 되었습니다. 또한.NET 프레임 워크 4.6을 통해 4.6.1에서 수정 되었습니다 [KB 3139549](https://support.microsoft.com/kb/3139549)합니다. .NET 4.6 이상을 대상으로 응용 프로그램 WPF 응용 프로그램-에 올바른 동작을 자동으로 가져오게 됩니다 <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) 디스패처 작업 전체에서 유지 되어야 합니다.|
|범위|부|
|버전|4.6|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentUICulture?displayProperty=nameWithType></li></ul>|

