### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>클러스터 및 일부 열에 null 값을 허용 하지 않는 기본 키를 추가 하는 SQL 지 속성 워크플로

|   |   |
|---|---|
|설명|.NET Framework 4.7 이상에서는 SQL 워크플로 인스턴스 저장소 (SWIS)에 대 한 SqlWorkflowInstanceStoreSchema.sql 스크립트에서 만든 테이블 클러스터형된 기본 키를 사용 합니다. 이 인해 identities 지원 하지 않는 <code>null</code> 값입니다. SWIS 작업이이 변경의 영향을 받지 않습니다. SQL Server 트랜잭션 복제를 지원 하도록 업데이트 되었습니다.|
|제안 해결 방법|SQL 파일 위해 SqlWorkflowInstanceStoreSchemaUpgrade.sql이이 변경을 발생 하기 위해 기존 설치에 적용 되어야 합니다. 데이터베이스에 새 설치에는 변경 내용을 자동으로 포함 됩니다.|
|범위|Microsoft Edge|
|버전|4.7|
|형식|런타임|

