### <a name="sqlconnectionopen-fails-on-windows-7-with-non-ifs-winsock-bsp-or-lsp-present"></a>SqlConnection.Open 비 IFS Winsock BSP 또는 LSP 현재 Windows 7에서 실패합니다.

|   |   |
|---|---|
|설명|<xref:System.Data.SqlClient.SqlConnection.Open> 및 <xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)> 비 IFS Winsock BSP 또는 LSP와 Windows 7 컴퓨터에서 실행 중인 컴퓨터에 있는 경우.NET Framework 4.5에서 실패 합니다. 비 IFS BSP 또는 LSP가 설치 되어 있는지 여부를 확인 하려면는 <code>netsh WinSock Show Catalog</code> 명령을 실행 하 고 검사 모든 <code>Winsock Catalog Provider Entry</code> 반환 되는 항목입니다. 서비스 플래그 값이 <code>0x20000</code> 비트 집합을 가진 경우, 공급자는 IFS 핸들을 사용하고 올바르게 작동합니다. <code>0x20000</code> 비트가 지우기인 경우(집합 아님) 비 IFS BSP 또는 LSP입니다.|
|제안 해결 방법|이 버그는 .NET Framework 4.5.2에서 수정되었으므로 .NET Framework를 업그레이드하여 방지할 수 있습니다. 또는 설치된 모든 비 IFS Winsock LSP를 제거하여 방지할 수 있습니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

