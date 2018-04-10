### <a name="wpf-printing-stack-update"></a>WPF 인쇄 스택 업데이트

|   |   |
|---|---|
|설명|WPF의 인쇄 Api를 사용 하 여 <xref:System.Printing.PrintQueue?displayProperty=name> 이제는 이제 사용 되지 않는 XPS 인쇄 API 대신 창 인쇄 문서 패키지 API를 호출 합니다. 서비스 가능성에 주의;으로 변경 사용자가 아니고 개발자 동작이 나 API 사용의 모든 변경 내용을 표시 됩니다. Windows 10 작성자 업데이트에서 실행 될 때 새 인쇄 스택 기본적으로 사용 됩니다. 이전 Windows 버전에서 이전과 동일 하 게 작동 하도록 이전 인쇄 스택 계속 계속 됩니다.|
|제안 해결 방법|Windows 10 작성자가 업데이트를 이전 스택을 사용 하려면 설정는 <code>UseXpsOMPrinting</code> REG_DWORD 값은 <code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code> 레지스트리 키를 <code>1</code>합니다.|
|범위|Microsoft Edge|
|버전|4.7|
|형식|런타임|

