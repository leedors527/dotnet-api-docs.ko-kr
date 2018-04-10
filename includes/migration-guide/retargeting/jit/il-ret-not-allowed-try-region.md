### <a name="il-ret-not-allowed-in-a-try-region"></a>IL ret try 지역에서 사용할 수 없습니다.

|   |   |
|---|---|
|설명|JIT64-just-in-time 컴파일러와 달리 RyuJIT (.NET 4.6에서 사용)에서는 IL ret try 영역에 있는 명령으로 수 없습니다. Try 영역에서 반환은 ecma-335 사양에서 허용 되지 않으며 이러한 IL을 생성 하는 알려진된 관리 컴파일러는 없습니다. 그러나 이러한 IL이 리플렉션 내보내기를 사용하여 생성된 경우에는 JIT64 컴파일러에서 실행됩니다.|
|제안 해결 방법|응용 프로그램 ret opcode try 지역에 포함 된 IL을 생성 하는 경우 응용 프로그램.NET 4.5 이전 JIT를 사용 하 고이 줄 바꿈으로 방지를 대상으로 할 수 있습니다. 또는 생성된 된 IL try 영역 뒤 반환할 업데이트 될 수 있습니다.|
|범위|Microsoft Edge|
|버전|4.6|
|형식|대상 변경|

