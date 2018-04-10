### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>HttpRuntime.AppDomainAppPath NullReferenceException을 Throw

|   |   |
|---|---|
|설명|.NET Framework 4.6.2에서에서 런타임에서 throw 한 <code>T:System.NullReferenceException</code> 를 검색할 때는 <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> null 문자를 포함 하는 값입니다. .NET Framework 4.6.1에서 이전 버전 런타임에서 throw 된 <code>T:System.ArgumentNullException</code>합니다.|
|제안 해결 방법|이러한 변경에 응답 하려면 다음 중 하나를 수행할 수 있습니다.<ul><li>처리는 <code>T:System.NullReferenceException</code> .NET Framework 4.6.2에서 실행 중인 응용 프로그램 경우.</li><li>이전 동작을 복원 하 고 throw 하는.NET Framework 4.7 업그레이드는 <code>T:System.ArgumentNullException</code>합니다.</li></ul>|
|범위|Microsoft Edge|
|버전|4.6.2|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

