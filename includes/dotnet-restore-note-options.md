> [!NOTE]
> .NET Core 2.0 부터는 필요가 없습니다 실행 [ `dotnet restore` ](~/docs/core/tools/dotnet-restore.md) 와 같은 모든 명령을 사용 하 여 암시적으로 실행이 때문에 `dotnet build` 및 `dotnet run`, 발생 하 여 복원 해야 하는 합니다. 이것이 여전히 있는 경우 명시적 복원을 수행 하는 것이 좋습니다, 특정 시나리오에서 유효한 명령와 같은 [Visual Studio Team Services에서 연속 통합 빌드](/vsts/build-release/apps/aspnet/build-aspnet-core) 또는 명시적으로 제어 하는 시간을 해야 하는 빌드 시스템에는 복원이 발생 합니다.
>
> 이 명령은 지원 합니다.는 `dotnet restore` 긴 형식으로 전달 될 때 옵션 (예를 들어 `--source`). 와 같은 양식 옵션 짧은 `-s`, 지원 되지 않습니다.