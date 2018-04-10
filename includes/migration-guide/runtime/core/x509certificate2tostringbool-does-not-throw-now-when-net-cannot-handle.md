### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) 이제 때.NET 처리할 수 없는 인증서를 throw 하지 않습니다.

|   |   |
|---|---|
|설명|경우이 메서드는 이전에 throw <code>true</code> verbose 매개 변수에 대해 전달 된 했 고.NET Framework에서 지원 되지 않는 설치 된 인증서입니다. 이제 메서드는 성공 하 고 인증서의 액세스할 수 없는 부분을 생략 하는 유효한 문자열을 반환 합니다.|
|제안 해결 방법|모든 코드에 따라 <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)> 예상 되는 반환 된 문자열 일부 인증서 데이터 (예: 공개 키, 개인 키 및 확장)를 제외 시킬 수도 있는 API 이전에 throw 할 경우에 따라 업데이트 해야 합니다.|
|범위|Microsoft Edge|
|버전|4.6|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

