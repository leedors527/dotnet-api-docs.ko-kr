### <a name="systemuri-parsing-adheres-to-rfc-3987"></a>RFC 3987을 준수 System.Uri 구문 분석

|   |   |
|---|---|
|설명|.NET 4.5에서 URI 구문 분석은 여러 방법으로 변경되었습니다. 단, 이러한 변경 내용은 .NET 4.5를 대상으로 하는 코드에 영향을 줍니다. 이진 파일이 .NET 4.0을 대상으로 하는 경우, 이전 동작이 관찰됩니다. .NET 4.5의 URI 구문 분석 변경 내용은 다음을 포함합니다.<ul><li>URI 구문 분석 정규화 및 문자에서 RFC 3987 최신 IRI 규칙에 따라 검사를 수행 합니다.</li><li>유니코드 정규화 형식 C uri 호스트 부분 에서만 수행 됩니다.</li><li>잘못 된 mailto: Uri에서 예외가 발생 합니다.</li><li>경로 세그먼트의 끝에 후행 점은 이제 유지 됩니다.</li><li><code>file://</code> Uri 이스케이프 되지 않은 <code>?</code> 문자입니다.</li><li>유니코드 제어 문자 <code>U+0080</code> 통해 <code>U+009F</code> 지원 되지 않습니다.</li><li>쉼표 문자 <code>,</code> 또는 <code>%2c</code> 자동으로 해제 되지 않습니다.</li></ul>|
|제안 해결 방법|이전 .NET 4.0 URI 구문 분석 의미 체계가 필요한 경우(주로 필요하지 않음) .NET 4.0을 대상으로 하여 사용할 수 있습니다. 이 사용 하 여 수행할 수 있습니다는 <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> '프로젝트 속성' 페이지에서 Visual Studio의 프로젝트 시스템 UI 통해 또는 어셈블리에 있습니다.|
|범위|주요함|
|버전|4.5|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Uri.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.UriKind)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.Uri,System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.String,System.UriKind,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.String,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.Uri,System.Uri@)?displayProperty=nameWithType></li></ul>|

