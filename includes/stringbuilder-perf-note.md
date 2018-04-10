문자 기반 사용 하는 인덱싱을 사용 하는 <xref:System.Text.StringBuilder.Chars%2A> 속성은 다음과 같은 매우 느려질 수 있습니다.

- <xref:System.Text.StringBuilder> 인스턴스 큽니다 (예를 들어 이루어져 여러 수만 개의 문자)입니다.
- <xref:System.Text.StringBuilder> 은 "규모가 큰"입니다. 즉, 메서드 호출을와 같은 반복 <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> 자동으로 개체의 확장 <xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType> 속성 및 해당 메모리의 할당 된 새 청크 합니다.

각 문자 액세스에서는 연결 된 전체 목록은 청크 인덱싱할 올바른 버퍼를 찾을 수 때문에 성능이 저하 심각 하 게 됩니다.

> [!NOTE]
>  큰 경우에 "규모가 큰" <xref:System.Text.StringBuilder> 개체를 사용 하는 <xref:System.Text.StringBuilder.Chars%2A> 속성 하나 또는 적은 수의 문자에 대 한 인덱스 기반 액세스에 대 한 영향은 미미 성능에 미치는 영향이; 일반적으로 **0(n)** 작업 합니다. 상당한 성능 저하의 문자를 반복할 때 발생는 <xref:System.Text.StringBuilder> 인 개체는 **O(n^2)** 작업 합니다. 

문자 기반 사용 하는 인덱싱을 사용 하는 경우 성능 문제가 발생 한 경우 <xref:System.Text.StringBuilder> 개체의 경우 다음 방법 중 하나를 사용할 수 있습니다.

- 변환의 <xref:System.Text.StringBuilder> 인스턴스는 <xref:System.String> 호출 하 여는 <xref:System.Text.StringBuilder.ToString%2A> 메서드를 다음 문자열의 문자에 액세스 합니다.

- 기존 내용을 복사 <xref:System.Text.StringBuilder> 새 개체 크기가 미리 지정 <xref:System.Text.StringBuilder> 개체입니다. 때문에 성능이 향상 됩니다 새 <xref:System.Text.StringBuilder> 대규모 개체가 아닙니다. 예:

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- 초기 용량 설정는 <xref:System.Text.StringBuilder> 은 약 최대 예상된 크기를 호출 하 여 값으로 개체는 <xref:System.Text.StringBuilder.%23ctor(System.Int32)> 생성자입니다. 전체 블록의 경우에도 메모리를 할당이 참고는 <xref:System.Text.StringBuilder> 거의 최대 용량에 도달 합니다.
