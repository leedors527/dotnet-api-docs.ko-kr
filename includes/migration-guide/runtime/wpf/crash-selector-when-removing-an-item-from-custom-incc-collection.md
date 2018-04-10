### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>선택기는 사용자 지정 INCC 컬렉션에서 항목을 제거할 때 크래시

|   |   |
|---|---|
|설명|<code>T:System.InvalidOperationException</code> 다음과 같은 시나리오에서 발생할 수 있습니다.<ul><li>에 대 한 ItemsSource는 <code>T:System.Windows.Controls.Primitives.Selector</code> 는 컬렉션의 사용자 지정 구현 <code>T:System.Collections.Specialized.INotifyCollectionChanged</code>합니다.</li><li>선택한 항목 컬렉션에서 제거 됩니다.</li><li><code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code> 가 <code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code> =-1 (알 수 없는 위치를 나타냄).</li></ul>예외의 호출 스택을 System.Windows.Threading.Dispatcher.VerifyAccess() System.Windows.Controls.Primitives.Selector.GetIsSelected (DependencyObject에서 System.Windows.DependencyObject.GetValue DependencyProperty dp ()에서 시작 요소)이이 예외는 응용 프로그램에서 둘 이상의 디스패처 스레드가.Net 4.5에서에서 발생할 수 있습니다. 4.7.net에서 예외 단일 발송자 스레드와 응용 프로그램에서 발생할 수도 있습니다. 이 문제는.Net 4.7.1에서에서 해결 됩니다.|
|제안 해결 방법|4.7.1.Net으로 업그레이드 합니다.|
|범위|부|
|버전|4.7|
|형식|런타임|

