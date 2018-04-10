### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a>예기치 않게에서 실패 WPF 맞춤법 검사

|   |   |
|---|---|
|설명|다양 한 WPF 맞춤법 검사기 문제가 포함 됩니다.<ul><li>WPF 맞춤법 검사기 경우가 발생합니다. <xref:System.Runtime.InteropServices.COMException?displayProperty=name></li><li>WPF 맞춤법 검사기와 함께 실패 <xref:System.UnauthorizedAccessException> '다른 사용자로 실행'을 사용 하 여 응용 프로그램이 시작 되는 경우</li><li>WPF 맞춤법 검사기에서 독일어에서 'Hausnummer'와 같은 복합 단어의 맞춤법 오류 올바르게 식별합니다.</li></ul>|
|제안 해결 방법|문제-# 1이.NET Framework 4.6.2에서에서 해결 되었습니다 문제 #2-WPF 맞춤법 검사기는 더 이상 '다른 사용자로 실행'을 사용 하 여 응용 프로그램이 시작 되는 경우 지원 됩니다. .NET Framework 4.6.2부터 이런이 방식으로 시작 된 응용 프로그램의 작동이 예기치 않게 중단 더 이상 됩니다-대신 맞춤법 검사기 기능이 자동으로 비활성화 됩니다. 문제 #3-.NET Framework 4.6.2에서에서 수정 되었습니다.|
|범위|Microsoft Edge|
|버전|4.6.1|
|형식|런타임|

