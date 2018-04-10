### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>동일한.NET Framework 버전을 사용 하려면 웹 팜의 모든 서버에에서 필요한 Asp.Net StateServer와 세션 상태를 공유 합니다.

|   |   |
|---|---|
|설명|사용 하도록 설정할 때 <xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name> 세션 상태를 제대로 공유 상태에 대 한 순서 대로 같은 버전의.NET Framework를 사용 해야 모든 지정 된 웹 팜에 있는 서버.|
|제안 해결 방법|동시에 상태를 공유 하는 웹 서버에.NET Framework 버전을 업그레이드 해야 합니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

