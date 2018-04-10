### <a name="attempting-a-tcpip-connection-to-a-sql-server-database-that-resolves-to-localhost-fails"></a>확인 되는 SQL Server 데이터베이스에 TCP/IP 연결을 시도 `localhost` 실패

|   |   |
|---|---|
|설명|.NET Framework 4.6 및 4.6.1에서 확인 되는 SQL Server 데이터베이스에 TCP/IP 연결을 시도 <code>localhost</code> 의 오류와 함께 실패 &quot;SQL Server에 연결을 설정 하는 동안 네트워크 관련 또는 인스턴스 관련 오류가 발생 했습니다. 서버를 찾을 수 없거나 액세스할 수 없습니다. 인스턴스 이름이 올바르고 SQL Server가 원격 연결을 허용하도록 구성되어 있는지 확인합니다. (공급자: SQL 네트워크 인터페이스, 오류: 26-서버/인스턴스 지정 된 찾기 오류)&quot;|
|제안 해결 방법|이 문제가 해결 되었음을 이전 동작은.NET Framework 4.6.2에서에서 복원 합니다. 확인 되는 SQL Server 목록에 연결할 <code>localhost</code>.NET Framework 4.6.2로 업그레이드 합니다.|
|범위|부|
|버전|4.6|
|형식|런타임|

