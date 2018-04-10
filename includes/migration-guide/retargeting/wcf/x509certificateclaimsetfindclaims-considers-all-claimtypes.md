### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>X509CertificateClaimSet.FindClaims 모든 claimTypes 고려

|   |   |
|---|---|
|설명|X509 클레임 집합이 해당 SAN 필드에 여러 DNS 항목이 있는 인증서 로부터 초기화 되는.NET Framework 4.6.1을 대상으로 하는 앱에서의 <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> 메서드 claimType 인수를 모든 DNS 항목과 일치 시 키 려 합니다. 이전 버전의.NET Framework를 대상으로 하는 앱에 대 한는 <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> 메서드 claimType 인수를 마지막 DNS 항목만 일치 시 키 려 합니다.|
|제안 해결 방법|이 변경은 .NET Framework 4.6.1을 대상으로 하는 응용 프로그램에만 영향을 줍니다. 이 변경 내용은 [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation) 호환성 스위치로 비활성화(또는 4.6.1 전 버전을 대상으로 하는 경우 활성화)될 수 있습니다.|
|범위|부|
|버전|4.6.1|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

