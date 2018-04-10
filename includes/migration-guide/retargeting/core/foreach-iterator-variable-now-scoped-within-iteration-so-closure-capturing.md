### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a>Foreach 반복기 변수가 현재 범위는 반복 내에서 하므로 클로저 캡처링 의미 체계는 다르게 (C# 5)

|   |   |
|---|---|
|설명|C# 5 (Visual Studio 2012)부터 <code>foreach</code> 반복기 변수 반복 내로 범위가 지정 됩니다. 코드에 포함 되어 있으면 변수에 따라 이전에 나누기 발생할 수 있습니다는 <code>foreach</code>클로저에 합니다. 이 변경의 증상은 대리자가 호출 시에 값이 아닌 대리자 당시에 값을 만들 때 대리자에 전달 된 반복기 변수 처리 됩니다.|
|제안 해결 방법|이상적으로 코드는 새 컴파일러 동작을 예상하도록 업데이트되어야 합니다. 이전의 의미 체계가 필요한 경우 반복기 변수는 루프 외부에 명시적으로 배치된 별도의 변수로 대체할 수 있습니다.|
|범위|주요함|
|버전|4.5|
|형식|대상 변경|

