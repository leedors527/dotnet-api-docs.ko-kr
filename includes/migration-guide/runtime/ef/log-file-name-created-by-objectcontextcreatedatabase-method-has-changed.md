### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a>SQL Server 사양에 맞게 변경 되었습니다 ObjectContext.CreateDatabase 메서드에서 만든 로그 파일 이름

|   |   |
|---|---|
|설명|경우는 <xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name> 메서드를 호출 하거나 직접 하거나 구성 요소를 (여기서 filename은의 이름 대신 filename.ldf filename_log.ldf 라는 로그 파일이 사용 하 여 코드 첫 번째 SqlClient 공급자와 연결 문자열의 AttachDBFilename 값으로 생성 지정 된 파일이 AttachDBFilename 값). 이 변경을 통해 SQL Server 사양에 따라 명명된 로그 파일을 제공하여 디버깅을 개선합니다.|
|제안 해결 방법|로그 파일 이름이 응용 프로그램에서 중요한 경우 응용 프로그램은 표준 _log.ldf 파일 이름 형식을 사용하도록 업데이트되어야 합니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|

