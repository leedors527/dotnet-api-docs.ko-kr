### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>ImageSourceConverter.ConvertFrom의 예외 처리 코드에서 NullReferenceException이 발생

|   |   |
|---|---|
|설명|<xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)>에 대한 예외 처리 코드의 오류로 인해 의도된 예외(예: <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>) 대신 잘못된 <xref:System.NullReferenceException?displayProperty=name>이 throw되고, 이러한 변경으로 메서드에서 이제 올바른 예외를 throw하도록 오류를 수정합니다. 기본적으로 .NET Framework 4.6.2 이하를 대상으로 하는 모든 응용 프로그램은 호환성을 위해 <xref:System.NullReferenceException?displayProperty=name>을 계속 throw하므로 .NET Framework 4.7 이상을 대상으로 하는 개발자는 올바른 예외가 표시되도록 하여야 합니다.// 해당하는 경우 공백을 'x'로 바꿉니다.|
|제안 해결 방법|.NET Framework 4.7을 대상으로 할 때 <xref:System.NullReferenceException?displayProperty=name>을 가져오는 것으로 되돌리려는 개발자는 응용 프로그램의 App.config 파일에 다음을 추가/병합할 수 있습니다.<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.7|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

