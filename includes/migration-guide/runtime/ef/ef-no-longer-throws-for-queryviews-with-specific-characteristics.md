### <a name="ef-no-longer-throws-for-queryviews-with-specific-characteristics"></a>EF 더 이상 throw 있는 Queryview에 대 한 특정 특성을 가진

|   |   |
|---|---|
|설명|Entity Framework가 더 이상 throw 한 <xref:System.StackOverflowException?displayProperty=name> 예외는 응용 프로그램 0..1으로 QueryView가 포함 된 쿼리를 실행 하는 경우 관련된 엔터티를 쿼리의 일부로 포함 하려고 하는 탐색 속성입니다. 예를 들어 호출 하 여 <code>.Include(e =&gt; e.RelatedNavProp)</code>합니다.|
|제안 해결 방법|이 변경은 1 있는 Queryview를 사용 하는 코드에만 영향을 미칩니다-0..1 관계를 호출 하는 쿼리를 실행할 때. 포함 됩니다. 이 변경으로 인해 안정성이 향상되며 거의 모든 앱에는 영향을 주지 않습니다. 하지만 이 변경으로 예기치 않은 동작이 발생하면 다음 항목을 앱 구성 파일의 <code>&lt;appSettings&gt;</code> 섹션에 추가하여 이 기능을 비활성화할 수 있습니다.<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyUserSpecifiedViews&quot; value=&quot;false&quot; /&gt;&#13;&#10;</code></pre>|
|범위|Microsoft Edge|
|버전|4.5.2|
|형식|런타임|

