### <a name="aspnet-accessibility-improvements-in-net-471"></a>4.7.1.NET의 향상 된 ASP.NET 내게 필요한 옵션 기능

|   |   |
|---|---|
|설명|.NET Framework 4.7.1 부터는 ASP.NET ASP.NET 웹 컨트롤 더 나은 지원 ASP.NET 고객에 게 Visual Studio의 내게 필요한 옵션 기술을 사용 하는 방법을 향상 되었습니다.  다음과 같이 변경은 다음과 같습니다.<ul><li>컨트롤에서 누락 된 UI 액세스 가능성 패턴을 구현 하는 변경 등의 세부 정보 보기 마법사에서 필드 추가 대화 상자 또는 ListView 마법사의 ListView 구성 대화 상자</li><li>고대비 모드에 표시 되는 개선 하기 위해 변경 내용을 같은 데이터 호출기 필드 편집기입니다.</li><li>DataPager 컨트롤, ObjectContext 구성 대화 상자에서 데이터 소스 구성 마법사의 구성 데이터 선택 영역 대화의 페이저 필드 편집 마법사에 필드 대화 상자와 같은 컨트롤에 대 한 키보드 탐색을 개선 하기 위해 변경 내용이 발생 합니다.</li></ul>|
|제안 해결 방법|<strong>내부 / 외부로 이러한 변경 내용을 취소 하는 방법</strong>4.7.1.NET Framework에서 실행 해야 이러한 변경 내용에서 사용 하기 위해 Visual Studio 디자이너에 대 한 순서로 이상. 이러한 변경에는 다음 방법 중 하나에서 웹 응용 프로그램을 활용할 수 있습니다.<ul><li>Visual Studio 2017 15.3 설치 또는 이상 버전에서는 기본적으로 다음 AppContext 스위치와 함께 새 내게 필요한 옵션 기능을 지원입니다.</li><li>추가 하 여 레거시 내게 필요한 옵션 동작 하지 않을 <code>Switch.UseLegacyAccessibilityFeatures</code> AppContext 스위치에는 <code>&lt;runtime&gt;</code> devenv.exe.config 파일에 섹션 및로 설정 <code>false</code>다음 예제와 같이 합니다.</li></ul><pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;...&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false&#39;  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;...;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;...&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>4.7.1.NET Framework를 대상으로 하는 응용 프로그램 이상 레거시를 보존 하려면 및 내게 필요한 옵션 동작을이 AppContext 스위치를 명시적으로 설정 하 여 사용 하는 레거시 내게 필요한 옵션 기능에 선택할 수 <code>true</code>합니다.|
|범위|부|
|버전|4.7.1|
|형식|대상 변경|

