### <a name="aescryptoserviceprovider-decryptor-provides-a-reusable-transform"></a>AesCryptoServiceProvider 암호 해독기는 다시 사용할 수 있는 변환을 제공합니다

|   |   |
|---|---|
|설명|.NET Framework 4.6.2, 대상으로 하는 앱부터는 <xref:System.Security.Cryptography.AesCryptoServiceProvider> 암호 해독기는 다시 사용할 수 있는 변환을 제공 합니다. <xref:System.Security.Cryptography.CryptoAPITransform.TransformFinalBlock(System.Byte[],System.Int32,System.Int32)?displayProperty=name>을 호출하고 나면 변환이 다시 초기화되므로 재사용할 수 있습니다. 암호 해독기를 호출 하 여 다시 사용 하는 응용 프로그램의 이전 버전의.NET Framework를 대상으로 하는 경우 <xref:System.Security.Cryptography.CryptoAPITransform.TransformBlock(System.Byte[],System.Int32,System.Int32,System.Byte[],System.Int32)?displayProperty=name> 를 호출한 후 <xref:System.Security.Cryptography.CryptoAPITransform.TransformFinalBlock(System.Byte[],System.Int32,System.Int32)?displayProperty=name> throw 한 <xref:System.Security.Cryptography.CryptographicException> 되었거나 손상 된 데이터를 생성 합니다.|
|제안 해결 방법|이 정상적인된 동작 이므로이 변경의 영향을 최소화, 해야 합니다. 이전 동작에 종속 된 응용 프로그램에 다음 구성 설정을 추가 하 여 사용 하 여 않을 수 있습니다는 <code>&lt;runtime&gt;</code> 응용 프로그램의 구성 파일의 섹션:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.AesCryptoServiceProvider.DontCorrectlyResetDecryptor=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>또한 이전 버전의.NET Framework를 대상으로 하지만.NET Framework 4.6.2부터.NET Framework의 버전에서 실행 되는 응용 프로그램에 선택할 수에 다음 구성 설정을 추가 하 여는 <code>&lt;runtime&gt;</code> 의 섹션은 응용 프로그램의 구성 파일:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.AesCryptoServiceProvider.DontCorrectlyResetDecryptor=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.6.2|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Security.Cryptography.AesCryptoServiceProvider.CreateDecryptor?displayProperty=nameWithType></li></ul>|

