### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>.NET Framework 4.6 레지스트리에 등록 되는 경우 4.5.x.x 버전을 사용 하지 않습니다.

|   |   |
|---|---|
|설명|예상할 수 버전 키 레지스트리에서 설정 (에 <code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) '4.6' 하지 '4.5'로 시작 하는.NET Framework 4.6에 대 한 합니다. 4.6은 새 가능한 버전 및 릴리스 이전 4.5.x와 호환 되는 것을 이해 하는 컴퓨터에 설치 된.NET Framework 버전에 알아야 이러한 레지스트리 키에 의존 하는 응용 프로그램 업데이트 되어야 합니다.|
|제안 해결 방법|.NET Framework 4.5에 대 한 검색 업데이트 앱도 4.6을 수락 하도록 4.5 레지스트리 키를 검색 하 여 설치 합니다.|
|범위|Microsoft Edge|
|버전|4.6|
|형식|런타임|

