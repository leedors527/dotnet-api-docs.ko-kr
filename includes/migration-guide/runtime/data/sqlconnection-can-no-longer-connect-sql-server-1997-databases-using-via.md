### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection은 SQL Server 1997 또는 VIA 어댑터를 사용 하 여 데이터베이스에 더 이상 연결할 수 없습니다.

|   |   |
|---|---|
|설명|사용 하 여 SQL Server 데이터베이스에 대 한 연결의 [어댑터 VIA (Virtual Interface) 프로토콜](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx) 이상 지원 되지 않습니다. SQL Server 데이터베이스에 연결 하는 데 사용 되는 프로토콜 연결 문자열에 표시 됩니다. 통해 VIA 연결이 포함 됩니다:&lt;servername&gt;합니다. VIA 이외의 프로토콜을 통해이 앱에 연결 하는 경우 (tcp: 또는 np: 예를 들어), 다음 주요 변경 내용 없음 발생 합니다. 또한 SQL Server 7 (1997)에 대 한 연결 더 이상 사용할 수 없습니다.|
|제안 해결 방법|SQL 데이터베이스에 연결 하는 다른 프로토콜을 사용 해야 하므로 VIA 프로토콜에 사용 되지 않습니다. 사용 되는 가장 일반적인 프로토콜은 TCP/IP입니다. TCP/IP 프로토콜을 사용 하는 것에 대 한 지침은 [여기](https://msdn.microsoft.com/library/bb909712.aspx)합니다. 데이터베이스만 액세스 하는 경우에서 인트라넷 내에서 공유 파이프 프로토콜 네트워크 속도가 느린 경우 더 나은 성능을 제공할 수 있습니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

