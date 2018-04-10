### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a>ASP.Net MVC4 응용 프로그램 프로 파일링 실행 엔진 오류가 발생할 수 있습니다.

|   |   |
|---|---|
|설명|NGEN /Profile 어셈블리를 사용 하는 프로파일러는 프로 파일링된 ASP.NET MVC4 응용 프로그램을 시작할 때 ' 심각한 실행 엔진 예외가 발생 하 여' 충돌이 발생할 수 있습니다.|
|제안 해결 방법|이 문제는.NET Framework 4.5.2에서에서 해결 됩니다. 프로파일러를 지정 하 여이 문제를 방지 될 수 있습니다 또는 <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> 해당 이벤트 마스크에 있습니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|

