### <a name="connection-pool-blocking-period-for-azure-sql-databases-is-removed"></a>Azure SQL 데이터베이스에 대 한 기간을 차단 하는 연결 풀 제거

|   |   |
|---|---|
|설명|열 연결에 대 한.NET Framework 4.6.2부터 알려진된 Azure SQL 데이터베이스에 대 한 요청 (*. database.windows.net, *. database.chinacloudapi.cn, *. database.usgovcloudapi.net, *. database.cloudapi.de), 차단 기간은 연결 풀 제거 하 고 연결 열기 오류는 캐시 되지 않습니다. 연결 열기 요청 다시 시도는 일시적인 연결 오류 발생 직후에 수행됩니다. 이 변경을 통해 Azure SQL 데이터베이스, 클라우드 기능 사용 앱의 성능 향상에 대 한 즉시 다시 시도 하도록 연결 열기 시도 합니다. 다른 모든 연결 시도 대 한 연결 풀 차단 기간 계속 적용 합니다. .NET Framework 4.6.1에서 이전 버전은 데이터베이스에 연결할 때 응용 프로그램에서 일시적인 연결 오류를 발견 한 경우 연결을 시도할 경우 다시 시도할 수 없는 신속 하 게 연결 풀 오류를 캐시 하 고 1로 5 초 동안 다시 throw 하므로 분입니다. 자세한 내용은 참조 [SQL Server 연결 풀링 (ADO.NET)](~/docs/framework/data/adonet/sql-server-connection-pooling.md)합니다. 이 동작은 일반적으로 몇 초 내에 복구되는 일시적인 오류가 자주 발생하는 Azure SQL 데이터베이스에 대한 연결 문제가 있습니다. 연결 풀 차단 기능이 응용 프로그램에 연결할 수 없음을 데이터베이스는 광범위 한 기간에 대 한 데이터베이스를 사용할 응용 프로그램 몇 초 안에 렌더링 해야 하는 경우에 의미 합니다.|
|제안 해결 방법|이 동작이 필요 없는 경우 연결 풀 차단 기간을 설정 하 여 구성할 수 있습니다는 <xref:System.Data.SqlClient.SqlConnectionStringBuilder.PoolBlockingPeriod?displayProperty=name> .NET Framework 4.6.2에서에서 새로 추가 된 속성입니다. 속성의 값은 다음의 세 값 중 하나를 사용할 수 있는 <xref:System.Data.SqlClient.PoolBlockingPeriod?displayProperty=name> 열거형의 멤버입니다.<ul><li><xref:System.Data.SqlClient.PoolBlockingPeriod.AlwaysBlock></li><li><xref:System.Data.SqlClient.PoolBlockingPeriod.Auto></li><li><xref:System.Data.SqlClient.PoolBlockingPeriod.NeverBlock></li></ul><xref:System.Data.SqlClient.SqlConnectionStringBuilder.PoolBlockingPeriod?displayProperty=name> 속성을 <xref:System.Data.SqlClient.PoolBlockingPeriod.AlwaysBlock>으로 설정하여 이전 동작을 복원할 수 있습니다.|
|범위|부|
|버전|4.6.2|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Data.Common.DbConnection.OpenAsync?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

