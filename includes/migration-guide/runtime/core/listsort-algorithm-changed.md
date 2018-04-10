### <a name="listsort-algorithm-changed"></a>List.Sort 알고리즘 변경

|   |   |
|---|---|
|설명|.NET Framework 4.5부터 <xref:System.Collections.Generic.List%601?displayProperty=name>의 정렬 알고리즘 (대신 빠른 정렬은 맞추어 내면적인 정렬 되도록) 변경 되었습니다. <xref:System.Collections.Generic.List%601?displayProperty=name>정렬에 안정 된 적이 없지만이 변경은 불안정 한 방법으로 정렬 하려면 다양 한 시나리오를 시작할 수 있습니다. 단순히 즉, 해당 항목은 API에 대 한 후속 호출에서 다른 순서로 정렬할 수 있습니다.|
|제안 해결 방법|때문에 이전 정렬 알고리즘 된 에서도 (하지만 약간 다른 방식) 안정적인, 항상 특정 순서로 정렬 하는 해당 항목에 종속 된 코드가 있어야 합니다. 이전 동작으로 운이 되 고 있는에 따라 코드의 인스턴스가 없는 경우 해당 코드는 명확 하 게 항목을 원하는 순서로 정렬 되는 비교자를 사용 하도록 업데이트 되어야 합니다.|
|범위|투명|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

