### <a name="marshalsizeof-and-marshalptrtostructure-overloads-break-dynamic-code"></a>동적 코드를 손상 Marshal.SizeOf 및 Marshal.PtrToStructure 오버 로드

|   |   |
|---|---|
|설명|메서드를 동적으로 바인딩.NET Framework 4.5.1부터 <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>, <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>, 또는 <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>, (Windows PowerShell, IronPython, 예를 들어 C# 동적 키워드를 통해) 발생할 수 있습니다 <code>MethodInvocationExceptions</code> 이러한 메서드의 새 오버 로드 추가 되어 있는 스크립팅 엔진에 모호할 수 있습니다.|
|제안 해결 방법|업데이트를 명확 하 게 사용 해야 하는 오버 로드를 나타내는 스크립트입니다. 이것은 일반적으로 메서드의 형식 매개 변수를 <xref:System.Type>로 명시적 캐스팅하여 수행할 수 있습니다. 문제를 해결하는 예제와 자세한 정보는 [이 링크](https://support.microsoft.com/kb/2909958/)를 참조하십시오.|
|범위|부|
|버전|4.5.1|
|형식|런타임|

