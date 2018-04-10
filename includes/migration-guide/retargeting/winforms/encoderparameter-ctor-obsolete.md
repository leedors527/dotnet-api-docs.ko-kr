### <a name="encoderparameter-ctor-is-obsolete"></a>EncoderParameter ctor 사용 되지 않습니다.

|   |   |
|---|---|
|설명|<xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)> 생성자는 이제 사용되지 않으며 사용하는 경우 빌드 경고가 발생합니다.|
|제안 해결 방법|하지만 <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)>생성자는 계속 작동,.NET 4.5 도구를 사용 하 여 코드를 다시 컴파일할 때 사용 되지 않는 빌드 경고를 방지 하기 위해 다음 생성자를 대신 사용 해야: <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Drawing.Imaging.EncoderParameterValueType,System.IntPtr)>합니다.|
|범위|부|
|버전|4.5|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

