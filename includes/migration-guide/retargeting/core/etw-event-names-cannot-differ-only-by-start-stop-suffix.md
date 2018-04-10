### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>ETW 이벤트 이름은 소문자만 달라 서 "Start" 또는 "Stop" 접미사

|   |   |
|---|---|
|설명|.NET Framework 4.6 및 4.6.1의 런타임 throw는 <xref:System.ArgumentException> 때 두 개의 이벤트에 대 한 ETW (Windows 추적) 이벤트 이름만 다르기는 &quot;시작&quot; 또는 &quot;중지&quot; 접미사 (때 하나의 이벤트 이름은 로<code>LogUser</code>즉 다른 <code>LogUserStart</code>). 이 경우 런타임에서 로깅을 발생할 수 없는 이벤트 소스를 구성할 수 없습니다.|
|제안 해결 방법|예외를 방지 하려면 두 개의 이벤트 이름이 없으면 해야만 다른 지를 확인 한 &quot;시작&quot; 또는 &quot;중지&quot; 접미사입니다. 이 요구 사항은.NET Framework 4.6.2;부터 제거 런타임에서 수만 다른 이벤트 이름을 명확 하 게는 &quot;시작&quot; 및 &quot;중지&quot; 접미사입니다.|
|범위|Microsoft Edge|
|버전|4.6|
|형식|대상 변경|

