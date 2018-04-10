### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable.Empty&lt;TResult&gt; 캐시 된 인스턴스가 항상 반환

|   |   |
|---|---|
|설명|.NET 4.5부터 <xref:System.Linq.Enumerable.Empty%60%601> 항상 캐시 된 내부 인스턴스를 반환 <xref:System.Collections.Generic.IEnumerable%601>합니다. 이전에 <xref:System.Linq.Enumerable.Empty%60%601> 빈 캐시는 <xref:System.Collections.Generic.IEnumerable%601> API 호출 된 시간에는 일부 조건에 의미 <xref:System.Linq.Enumerable.Empty%60%601> 호출한 신속 하 고 동시에 다른 형식의 인스턴스를 서로 다른 호출에 대해 반환 될 수는 API입니다.|
|제안 해결 방법|이전 동작이 명확하지 않았으므로 코드가 종속될 가능성이 작습니다. 그러나 빈 열거형은 비교되고 때로는 같지 않은 것으로 예상되는 드문 경우에는, <xref:System.Linq.Enumerable.Empty%60%601>를 사용하는 대신 명시적인 빈 배열을 만들어야 합니다(<code>new T[0]</code>).|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

