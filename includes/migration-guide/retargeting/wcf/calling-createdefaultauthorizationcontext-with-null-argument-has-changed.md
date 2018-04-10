### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>변경 된 CreateDefaultAuthorizationContext null 인수와 함께 호출

|   |   |
|---|---|
|설명|구현에서 <xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name> 에 대 한 호출에서 반환 되는 <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name> null authorizationPolicies와 인수에는.NET Framework 4.6에서 해당 구현을 변경 했습니다.|
|제안 해결 방법|드문 경우이지만 사용자 지정 인증을 사용하는 WCF 앱은 다르게 동작할 수 있습니다. 이러한 경우 두 가지 방법 중 하나로 이전 동작을 복원할 수 있습니다.<ol><li>4.6 이전 버전의 .NET Framework를 대상으로 사용하도록 앱을 다시 컴파일합니다. IIS 호스트 서비스에 대 한 사용는 &lt;httpRuntime targetFramework =&quot;x.x&quot;  / &gt; 요소는 이전 버전의.NET Framework를 대상으로 합니다.</li><li>다음 줄을 app.config 파일의 <code>&lt;appSettings&gt;</code> 섹션에 추가합니다. <code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code></li></ol>|
|범위|부|
|버전|4.6|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|

