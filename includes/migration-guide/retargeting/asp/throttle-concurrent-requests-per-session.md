### <a name="throttle-concurrent-requests-per-session"></a>세션당 동시 요청 수 조절

|   |   |
|---|---|
|설명|.NET Framework 4.6.2에서에서 및 이전 버전에서 ASP.NET 동일한 세션 Id 사용 하 여 요청을 순차적으로, 실행 및 ASP.NET 기본적으로 항상 쿠키를 통해 세션 Id를 발급 합니다. 페이지 변수를 사용할 경우 응답 하는 데 시간이 오래이 크게 성능이 저하 됩니다 서버 브라우저에서 f5 키를 여 합니다. 수정 프로그램을 큐에 대기 중인된 요청을 추적 하 고 지정된 된 한도 초과 하는 경우 요청을 종료 하는 카운터를 추가 했습니다. 기본값은 50입니다. 제한에 도달 하면 이벤트 로그 및 HTTP 500 응답 IIS 로그에 기록 될 수 있습니다에 경고가 기록 됩니다.|
|제안 해결 방법|이전 동작을 복원하려면 web.config 파일에 다음 설정을 추가하여 새 동작을 옵트아웃(opt out)할 수 있습니다.<pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.7|
|형식|대상 변경|

