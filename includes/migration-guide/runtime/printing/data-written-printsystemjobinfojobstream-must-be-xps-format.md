### <a name="data-written-to-printsystemjobinfojobstream-must-be-in-xps-format"></a>PrintSystemJobInfo.JobStream에 기록 된 데이터는 XPS 형식에서 이어야 합니다.

|   |   |
|---|---|
|설명|<xref:System.Printing.PrintSystemJobInfo.JobStream> 속성 인쇄 작업 스트림을 노출 합니다. 사용자는이 스트림에 작성 하 여 기본 운영 체제 인쇄 구성 요소에 원시 데이터를 보낼 수 있습니다. Windows 8 및 Windows 운영 체제의 이후 버전의.NET Framework 4.5부터이 스트림에 기록 된 데이터 형식 이어야 합니다 XPS는 패키지 스트림과 같은 합니다.|
|제안 해결 방법|인쇄 내용을 출력하려면 다음 중 하나를 수행할 수 있습니다.<ul><li><xref:System.Windows.Xps.XpsDocumentWriter> 클래스를 사용하여 인쇄 내용을 출력합니다. 이는 권장되는 대안입니다.</li><li>반환 된 스트림으로 전송 되는 데이터를 확인 하는 <xref:System.Printing.PrintSystemJobInfo.JobStream> 속성은 패키지 스트림과 같은 XPS 형식입니다.</li></ul>|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Printing.PrintSystemJobInfo.JobStream?displayProperty=nameWithType></li></ul>|

