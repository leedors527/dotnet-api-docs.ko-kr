### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>ADO.NET은 이제 끊어진된 SQL 연결을 자동으로 다시 연결 시도

|   |   |
|---|---|
|설명|.NET Framework 4.5.1부터,.NET Framework 끊어진된 SQL 연결을 자동으로 다시 연결 하려고 시도 합니다. 하지만 이렇게 하면 일반적으로 더욱 앱 더 안정적으로 앱이 다시 연결 시에 특정 작업을 수행할 수 있도록 연결이 손실 된 알아야 할 수 있는 가장자리 경우가 있습니다.|
|제안 해결 방법|이 기능은 호환성 문제로 인해 필요 없는 경우 설정 하 여 해제할 수 있습니다는 <xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name> 연결 문자열의 속성 (또는 <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>)을 0으로 합니다.|
|범위|Microsoft Edge|
|버전|4.5.1|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|

