### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>이제 RSACng.VerifyHash 확인 오류가 발생 한 False를 반환

|   |   |
|---|---|
|설명|.NET Framework 4.6.2부터,이 메서드가 반환 <strong>False</strong> 경우 자체 서명 형식이 잘못 되었습니다. 이제 모든 확인 실패에 대해 false를 반환합니다. .NET Framework 4.6 및 4.6.1에서 메서드에서 throw 한 <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> 경우 자체 서명 형식이 잘못 되었습니다.|
|제안 해결 방법|처리 해야만 해당 실행 되는 모든 코드는 <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> 유효성 검사가 실패 하면 대신 실행 해야 할 메서드가 반환 하 고 <strong>False</strong>합니다.|
|범위|부|
|버전|4.6.2|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

