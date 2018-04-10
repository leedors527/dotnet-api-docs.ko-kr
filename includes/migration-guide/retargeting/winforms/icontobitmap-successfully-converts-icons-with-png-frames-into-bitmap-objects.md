### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap은 비트맵 개체에 PNG 프레임이 있는 아이콘을 성공적으로 변환

|   |   |
|---|---|
|설명|.NET Framework 4.6을 대상으로 하는 앱부터는 <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> 메서드 비트맵 개체에 PNG 프레임이 있는 아이콘을 성공적으로 변환 합니다. .NET Framework 4.5.2 및 이전 버전을 대상으로 하는 앱에서의 <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> 메서드가 throw는 <xref:System.ArgumentOutOfRangeException> 아이콘 개체에 PNG 프레임이 있는 경우는 예외입니다. 이 변경 사항은.NET Framework 4.6을 대상으로 다시 컴파일되는 및에 대 한 특수 처리를 구현 하는 앱에 적용 된 <xref:System.ArgumentOutOfRangeException> Icon 개체에 PNG 프레임이 있을 때 throw 되는 합니다. .NET Framework 4.6에서 실행되는 경우 변환이 성공하고 <xref:System.ArgumentOutOfRangeException> 이 더 이상 throw되지 않습니다. 따라서 예외 처리기가 더 이상 호출되지 않습니다.|
|제안 해결 방법|이 동작이 필요 없는 경우 다음 요소를 추가 하 여 이전 동작을 유지할 수 있습니다는 <code>&lt;runtime&gt;</code> app.config 파일의 섹션:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>App.config 파일에 이미 있는 경우는 <code>AppContextSwitchOverrides</code> 요소를 다음과 같이 값 특성을 가진 새 값을 병합 해야 합니다.<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.6|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

