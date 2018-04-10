### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>MaxRequestLength 또는 maxReceivedMessageSize에 대 한 오류 코드는 서로 다른

|   |   |
|---|---|
|설명|WCF 웹의 메시지 maxRequestLength (ASP.NET에서)를 초과 하는 인터넷 정보 서비스 (IIS) 또는 ASP.NET Development Server에서 호스트 되는 서비스 또는 maxReceivedMessageSize (WCF)에서 다른 오류 코드 HTTP 상태 코드 400 (잘못 된 요청에서 변경 되었습니다 ) 413 (요청 엔터티 너무 큼), 및는 maxRequestLength 또는 maxReceivedMessageSize 설정을 초과 하는 메시지를 throw 한 <xref:System.ServiceModel.ProtocolException?displayProperty=name> 예외입니다. 이 경우 전송 모드는 스트리밍됩니다 포함 됩니다.|
|제안 해결 방법|이러한 변경 메시지 길이가 ASP.NET 또는 WCF에서 허용한 한계를 초과 하는 경우에 디버깅을 용이 하 게 합니다. 400 HTTP 상태 코드에 따라 처리를 수행 하는 코드를 수정 해야 합니다.|
|범위|Microsoft Edge|
|버전|4.5|
|형식|런타임|

