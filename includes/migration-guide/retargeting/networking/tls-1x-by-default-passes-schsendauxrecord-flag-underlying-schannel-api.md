### <a name="tls-1x-by-default-passes-the-schsendauxrecord-flag-to-the-underlying-schannel-api"></a>TLS 1.x 기본적으로 기본 SCHANNEL API를 SCH_SEND_AUX_RECORD 플래그를 전달

|   |   |
|---|---|
|설명|TLS를 사용 하는 경우 1.x,.NET Framework 기본 Windows SCHANNEL API에 의존 합니다. .NET Framework 4.6부터는 [SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx) 플래그는 기본적으로 SCHANNEL으로 전달 됩니다. 이 인해 데이터를 두 개의 별도 레코드로 싱글바이트 및 초 간격으로 첫 번째 암호화할 분할 SCHANNEL <em>n</em>-1 바이트입니다. 드문 경우 지만이 단일 레코드의 데이터가 있는 가정 하는 기존 서버와 클라이언트 간의 통신을 중단 합니다.|
|제안 해결 방법|이 변경은 기존 서버와 통신을 끊고, 보내는 비활성화할 수 있습니다는 [SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx) 플래그 지정 및 다음 스위치를 추가 하 여 별도 레코드를 데이터를 분할 하지 이전 동작을 복원할는 [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) 에 [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 응용 프로그램 구성 파일:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontEnableSchSendAuxRecord=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] 이 설정에 대 한 이전 버전과 호환성을 위해서만 제공 됩니다. 사용 하지 않으면 권장 되지 않습니다.</blockquote> |
|범위|Microsoft Edge|
|버전|4.6|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

