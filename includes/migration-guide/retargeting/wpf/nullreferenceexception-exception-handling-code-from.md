### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>예외 처리 ImageSourceConverter.ConvertFrom에서 코드에서에서 nullreferenceexception이 발생

|   |   |
|---|---|
|설명|예외 처리에 대 한 코드에에서 오류가 <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> 잘못 된 발생 <xref:System.NullReferenceException?displayProperty=name> 의도 한 예외가 아닌 throw 됩니다 (예: <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>), 이러한 변경 메서드에서 이제 올바른 예외가 throw 되도록 오류를 수정 합니다. 기본.NET Framework 4.6.2를 대상으로 하는 모든 응용 프로그램 계속 사용 되며 다음 throw <xref:System.NullReferenceException?displayProperty=name> 호환성,.NET Framework 4.7 목표로 하는 개발자 이상 나타나야 오른쪽 exceptions.// Replace는 'x'를 사용 하 여 공간 해당 하는 경우|
|제안 해결 방법|가져오기로 되돌리려면 하려는 개발자는 <xref:System.NullReferenceException?displayProperty=name> 때.NET Framework 4.7를 대상으로 수 추가/병합이 응용 프로그램의 App.config 파일에 다음:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.7|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

