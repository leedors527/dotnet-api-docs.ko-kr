### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>잘못 된 코드 생성 UInt16 값을 비교 하 고 전달 하는 경우

|   |   |
|---|---|
|설명|.NET Framework 4.7에 도입 된 차이로 인해 일부 경우에 응용 프로그램 실행에.NET Framework 4.7 올바르게에서 JIT 컴파일러에서 생성 된 코드 비교 하 여 두 개의 <code>T:System.UInt16</code> 값입니다. 자세한 내용은 참조 [문제 #11508: ushort args 비교 하 고 전달 하는 경우 자동 불량 codegen](https://github.com/dotnet/coreclr/issues/11508) GitHub.com에 있습니다.|
|제안 해결 방법|.NET Framework 4.7에 16 비트 부호 없는 값 비교에 문제가 발생 하면 경우에.NET Framework 4.7.1 업그레이드 합니다.|
|범위|Microsoft Edge|
|버전|4.7|
|형식|런타임|

