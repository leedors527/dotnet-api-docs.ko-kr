### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>WPF PackageDigitalSignatureManager에 대 한 기본 해시 알고리즘은 s h a 256 이제

|   |   |
|---|---|
|설명|<code>System.IO.Packaging.PackageDigitalSignatureManager</code> WPF 패키지와 관련 하 여 디지털 서명을 위한 기능을 제공 합니다.  .NET Framework 4.7 및 이전 버전에서는 기본 알고리즘 (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) SHA1가 패키지의 일부 서명에 사용 합니다.  SHA1와 최근 보안 문제로 인해이 기본값으로 변경 되었습니다 SHA256 4.7.1.NET Framework로 시작 합니다.  이 변경 내용은 패키지 서명, XPS 문서를 비롯 한 모든 결정 합니다.|
|제안 해결 방법|.NET 4.7.1 또는 큰 수를 대상으로 하는 동안 이전 기능을 필요로 하는 개발자 또는 아래 4.7.1.NET framework 버전을 대상으로 하는 동안이 변경 내용을 활용 하 여 원하는 개발자에 게 다음 AppContext 플래그를 적절 하 게 설정 합니다.  값이 true 이면 SHA1 발생 합니다; 기본 알고리즘으로 사용 되 고 s h a 256에 false 결과입니다.<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.7.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

