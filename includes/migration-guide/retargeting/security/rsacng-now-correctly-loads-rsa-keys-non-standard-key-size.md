### <a name="rsacng-now-correctly-loads-rsa-keys-of-non-standard-key-size"></a>RSACng 이제 올바르게 로드 비표준 키 크기의 RSA 키

|   |   |
|---|---|
|설명|4.6.2 하기 전에.NET Framework 버전에서는 RSA 인증서에 대 한 비표준 키 크기와 고객은 해당 키를 통해 액세스할 수는 <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name> 및 <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name> 확장 메서드입니다.  A <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> 메시지와 함께 &quot;요청 된 키 크기가 지원 되지 않음을&quot; throw 됩니다. .NET Framework 4.6.2에서에서이 문제가 해결 되었습니다. 마찬가지로, <xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)> 및 <xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)> 이제 사용할 수 없는 키 크기를 throw 하지 않고 작업할 <xref:System.Security.Cryptography.CryptographicException?displayProperty=name>s입니다.|
|제안 해결 방법|이전 동작에 사용 하는 논리를 처리 하는 모든 예외가 있는 경우 여기서는 <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> 비표준 키 크기를 사용 하는 경우 throw 되는 논리를 제거 하십시오.|
|범위|Microsoft Edge|
|버전|4.6.2|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li></ul>|

