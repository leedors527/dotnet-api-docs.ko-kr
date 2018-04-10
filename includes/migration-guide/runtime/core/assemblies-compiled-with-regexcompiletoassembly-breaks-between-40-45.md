### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>4.0 및 4.5 간의 Regex.CompileToAssembly 구분선이 있는 컴파일된 어셈블리

|   |   |
|---|---|
|설명|컴파일된 정규식의 어셈블리가.NET Framework 4를 대상으로 하지만.NET Framework 4.5를 빌드한.NET Framework 4 부터는 시스템에서 어셈블리를 설치 한다는 점에서 정규식 중 하나를 사용 하는 예외를 throw 합니다.|
|제안 해결 방법|이 문제를 해결하기 위해서는 다음 중 하나를 수행합니다.<ul><li>.NET Framework 4는 정규식이 포함 된 어셈블리를 빌드하십시오.</li><li>해석된 정규식을 사용합니다.</li></ul>|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|

