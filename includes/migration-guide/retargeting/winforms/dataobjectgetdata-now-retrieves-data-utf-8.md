### <a name="dataobjectgetdata-now-retrieves-data-as-utf-8"></a>이제 DataObject.GetData u t F-8로 데이터를 검색

|   |   |
|---|---|
|설명|대상.NET Framework 4 또는.NET Framework 4.5.1 또는 이전 버전에서 실행 되는 앱에 대 한 <code>DataObject.GetData</code> HTML 형식의 데이터를 ASCII 문자열로 검색 합니다. 결과적으로 비-ASCII 문자 (ASCII 코드가 0x7F 보다 큰는 문자)는 임의의 두 문자로 표시 됩니다. 대상.NET Framework 4.5 또는 이상 및.NET Framework 4.5.2에서 실행 하는 앱에 대 한 <code>DataObject.GetData</code> 0x7F 보다 큰 문자를 올바르게 나타낼는 u t F-8로 HTML 형식의 데이터를 검색 합니다.|
|제안 해결 방법|인코딩 문제 HTML 형식 문자열에 대 한 해결 방법을 구현한 상태 (예를 들어 HTML 문자열을 명시적으로 인코딩 함으로써 클립보드에서 검색할 전달 하 여 <xref:System.Text.UTF8Encoding.GetString(System.Byte[],System.Int32,System.Int32)?displayProperty=name>) 버전 4에서 4.5로에서 응용 프로그램 대상을입니다 해결 방법을 제거 해야 합니다. 어떤 이유로 이전 동작이 필요한 경우 응용 프로그램 이렇게 되도록 하려면.NET Framework 4.0 대상으로 지정할 수 있습니다.|
|범위|Microsoft Edge|
|버전|4.5.2|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Windows.DataObject.GetData(System.String)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.Type)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

