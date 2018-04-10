### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>페르시아력을 이제는 회교식 양력 알고리즘을 사용

|   |   |
|---|---|
|설명|.NET Framework 4.6부터는 <xref:System.Globalization.PersianCalendar?displayProperty=name> 클래스는 회교식 양력 알고리즘을 사용 합니다. 변환 사이의 날짜는 <xref:System.Globalization.PersianCalendar?displayProperty=name> 및 다른 달력 (그레고리오 력) 2023 보다 이후 이거나 1800 보다 이전 날짜에 대 한.NET Framework 4.6과 함께 시작 하는 약간 다른 결과 생성할 수 있습니다. 또한 <xref:System.Globalization.PersianCalendar.MinSupportedDateTime> 이제 <code>March 22, 0622 instead of March 21, 0622</code>합니다.|
|제안 해결 방법|.NET 4.6에서 PersianCalendar를 사용할 때 일부 이전 또는 늦은 날짜는 약간 다를 수 있습니다. 또한 다른 .NET Framework 버전에서 실행될 수 있는 프로세스 사이의 날짜를 직렬화할 때 PersianCalendar 날짜 문자열로 저장하지 마십시오(해당 값이 다를 수 있음).|
|범위|부|
|버전|4.6|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|

