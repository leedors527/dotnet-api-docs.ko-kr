### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>터치 사용 시스템에서 System.Windows.Input.PenContext.Disable에 대 한 호출에는 ArgumentException throw 될 수 있습니다.

|   |   |
|---|---|
|설명|상황에 따라 내부 호출 <strong>System.Windows.Intput.PenContext.Disable</strong> 메서드 터치 기반의 시스템에서 처리 되지 않은 throw 될 수 있습니다 <code>T:System.ArgumentException</code> 재입력으로 인해 합니다.|
|제안 해결 방법|.NET Framework 4.7에서이 문제가 해결 되었습니다. 예외를 방지 하려면.NET Framework 4.7 부터는.NET Framework의 버전으로 업그레이드 합니다.|
|범위|Microsoft Edge|
|버전|4.6.1|
|형식|대상 변경|

