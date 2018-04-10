### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a>옵트인 나누기에서 다른 4.5 SQL 생성으로 되돌리려면 간단 4.0 SQL 생성

|   |   |
|---|---|
|설명|조인 문을 생성할지 및 호출을 포함 하는 쿼리에 단순한 SQL을 생성 이제 OrderBy를 사용 하 여 첫 번째 하지 않고 제한 작업을 합니다. .NET Framework 4.5로 업그레이드 한 후 이러한 쿼리는 이전 버전 보다 더욱 복잡 한 SQL을 생성 합니다.|
|제안 해결 방법|이 기능은 기본적으로 비활성화되어 있습니다. Entity Framework 성능 저하가 발생 하는 추가 조인 문을 생성 하는 경우 다음의 항목을 추가 하 여이 기능을 활성화할 수 있습니다는 <code>&lt;appSettings&gt;</code> 응용 프로그램 구성 (app.config) 파일의 섹션:<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|범위|투명|
|버전|4.5.2|
|형식|런타임|

