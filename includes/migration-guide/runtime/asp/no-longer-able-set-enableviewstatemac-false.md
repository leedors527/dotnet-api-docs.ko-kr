### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>더 이상 수 EnableViewStateMac false로 설정

|   |   |
|---|---|
|설명|ASP.NET에서 개발자는 더 이상 <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> 또는 <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>를 지정할 수 없습니다. 포함된 뷰 상태가 사용된 모든 요청에 뷰 상태 MAC(메시지 인증 코드)가 적용됩니다. 명시적으로 EnableViewStateMac 속성을 설정 하는 응용 프로그램만 <code>false</code> 영향을 받습니다.|
|제안 해결 방법|EnableViewStateMac true 인 것으로 간주 해야 하 고 모든 결과 MAC 오류를 해결 해야 합니다. (에 설명 된 대로 [이 지침은](https://support.microsoft.com/kb/2915218), MAC 오류 원인을의 세부 사항에 따라 여러 해상도 포함 된).|
|범위|주요함|
|버전|4.5.2|
|형식|런타임|

