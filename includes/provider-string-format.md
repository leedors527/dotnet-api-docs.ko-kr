 
그러나 **String.Format** 메서드를 호출할 때 호출할 특정 오버로드에 집중할 필요가 없습니다. 대신 문화권 구분 또는 사용자 지정 서식을 제공하는 개체와 하나 이상의 서식 항목이 포함된 [복합 형식 문자열](~/docs/standard/base-types/composite-formatting.md)을 사용하여 메서드를 호출할 수 있습니다. 첫 번째 인덱스는 0으로 시작하는 숫자 인덱스를 각 서식 항목에 할당합니다. 초기 문자열 이외에도 메서드 호출에는 인덱스 값만큼 많은 추가 인수가 있어야 합니다. 예를 들어 서식 항목에 0과 1의 인덱스가 있는 문자열에는 2개의 인수가 있어야 하며, 0에서 5의 인덱스가 있는 문자열에는 6개의 인수가 있어야 합니다. 그러면 언어 컴파일러가 메서드 호출을 **String.Format** 메서드의 특정 오버로드로 확인합니다.   

**String.Format** 메서드 사용에 대한 자세한 설명서는 [String.Format 메서드 시작](#Starting) 및 [어느 메서드를 호출해야 합니까?](#FTaskList)를 참조하세요.   
