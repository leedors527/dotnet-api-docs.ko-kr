### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>.NET Framework 4.5에서 serialize MailMessage 개체의 deserialization 실패할 수 있습니다.

|   |   |
|---|---|
|설명|.NET Framework 4.5부터 <xref:System.Web.Mail.MailMessage> 개체에서 비 ASCII 문자를 포함할 수 있습니다. .NET Framework 4에서는 ASCII 문자만 지원됩니다. <xref:System.Web.Mail.MailMessage> .NET Framework 4에서 비 ASCII 문자를 포함 하 고.NET Framework 4.5 이상 serialize 되는 개체를 역직렬화 할 수 없습니다.|
|제안 해결 방법|역직렬화 하는 동안 코드 예외 처리를 제공 하는지 확인 한 <xref:System.Web.Mail.MailMessage> 개체입니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

