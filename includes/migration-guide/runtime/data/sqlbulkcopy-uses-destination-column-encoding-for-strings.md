### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>SqlBulkCopy는 문자열에 대 한 대상 열의 인코딩을 사용 하 여

|   |   |
|---|---|
|설명|열에 데이터를 삽입할 때 <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name>에서는 <code>VARCHAR</code> 및 <code>CHAR</code> 형식에 대한 기본 인코딩 대신 대상 열의 인코딩을 사용합니다. 이러한 변경을 통해 대상 열에서 기본 인코딩을 사용하지 않는 경우 기본 인코딩을 사용하여 발생하는 데이터 손상의 가능성을 제거합니다. 드문 경우 지만 인코딩 데이터를 대상 열에 맞게 너무 커서를 생성 하는 경우 기존 응용 프로그램 SqlException 예외를 throw 될 수 있습니다.|
|제안 해결 방법|에 <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> 인코딩 차이 때문에 데이터를 더 이상 손상 됩니다. 대상 열의 크기 제한 근처 문자열을 복사 하는 경우 하거나 (복사할 데이터를 대상 열에 맞게 데이터를 확인 하려면) 미리 인코딩할 할 수 있습니다 또는 catch <xref:System.Data.SqlClient.SqlException?displayProperty=name>s입니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

