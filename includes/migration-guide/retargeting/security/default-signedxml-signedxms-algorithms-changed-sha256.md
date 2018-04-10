### <a name="default-signedxml-and-signedxms-algorithms-changed-to-sha256"></a>S h a 256으로 변경 하는 기본 SignedXML 및 SignedXMS 알고리즘

|   |   |
|---|---|
|설명|.NET Framework 4.7 및 이전 버전에서는 SignedXML 및 SignedCMS 기본적으로 SHA1 일부 작업에 대 한. .NET Framework 4.7.1 부터는 s h a 256이이 작업에 대해 기본적으로 사용 됩니다. 이 변경은 s h a 1은 안전한 것으로 간주 더 이상 필요 합니다.|
|제안 해결 방법|SHA1 (안전 하지 않음) 또는 s h a 256이 기본적으로 사용 되는지 여부를 제어 하기 위해 두 새 컨텍스트 스위치 값을 있습니다.<ul><li>Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms</li><li>Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms</li></ul>.NET Framework 4.7.1 대상 및 이후 버전에서는 s h a 256 사용 하는 것은 바람직하지 하는 경우를 복원할 수 있습니다 기본값 SHA1 다음 구성을 추가 하 여 응용 프로그램에 대 한 전환 하는 [런타임](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 응용 프로그램 구성의 섹션 파일:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=true;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=true&quot; /&gt;&#13;&#10;</code></pre>.NET Framework 4.7 및 이전 버전을 대상으로 하는 응용 프로그램의 경우 선택할 수 있습니다 이러한 변경에는 다음 구성 스위치를 추가 하 여는 [런타임](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 응용 프로그램 구성 파일의 섹션:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=false;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=false&quot; /&gt;&#13;&#10;</code></pre>|
|범위|부|
|버전|4.7.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Security.Cryptography.Pkcs.CmsSigner?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.Reference?displayProperty=nameWithType></li></ul>|

