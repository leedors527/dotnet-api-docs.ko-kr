### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute는 WinMD 시나리오에서 ObsoleteAttribute 및 DeprecatedAttribute로 내보내는

|   |   |
|---|---|
|설명|Windows 메타 데이터 라이브러리 (.winmd 파일)을 만들 때의 <xref:System.ObsoleteAttribute?displayProperty=name> 특성 둘 다로 내보내집니다 <xref:System.ObsoleteAttribute?displayProperty=name> 및 [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute)합니다.|
|제안 해결 방법|사용 된 기존 소스 코드의 재컴파일을 <xref:System.ObsoleteAttribute?displayProperty=name> 특성 C + 해당 코드가 사용 될 때 경고가 발생할 수 있습니다 + /CX 또는 JavaScript.We 권장 하지는 않습니다 둘 다 적용 <xref:System.ObsoleteAttribute?displayProperty=name> 및 [ Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) ; 관리 되는 어셈블리에 코드를 빌드 경고가 발생할 수 있습니다.|
|범위|Microsoft Edge|
|버전|4.5.1|
|형식|대상 변경|

