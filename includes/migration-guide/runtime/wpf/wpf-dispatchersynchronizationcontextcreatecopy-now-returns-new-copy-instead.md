### <a name="wpf-dispatchersynchronizationcontextcreatecopy-now-returns-a-new-copy-instead-of-the-current-instance"></a>WPF DispatcherSynchronizationContext.CreateCopy 이제 대신 현재 인스턴스의 새 복사본을 반환

|   |   |
|---|---|
|설명|.NET Framework 4의 <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> 주로 성능 최적화로 현재 인스턴스에 대 한 참조를 반환 합니다. .NET Framework 4.5에서는 처음으로 동일한 참조가 실행 스레드를 올바른 동기화 컨텍스트에 나타내도록 마무리하는 것을 가능하게 하는 새 인스턴스를 반환합니다.  이러한 참조의 id를 확인 하는 코드 영향을 않는지 그럴 가능성은 있지만,이 변경으로 인해 호출 하는 코드가 <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> .NET Framework 4.5 이상이 마이그레이션의 일환으로 테스트 해야 합니다.|
|제안 해결 방법|주의 <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> 새 반환 <xref:System.Threading.SynchronizationContext?displayProperty=name> 개체입니다. 이전에는 이러한 방식으로 생성된 참조의 동등성을 사용한 코드는 적절한 컨텍스트에 있는지 실제로 확인되지 않았지만 .NET 4.5 이상에 대해 빌드할 때는 확인됩니다.  문제가 발생할 가능성은 작지만 발생하는 경우 영향을 받은 코드 경로를 실행하는 것으로 확인하기에 충분할 것입니다.|
|범위|부|
|버전|4.5|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy?displayProperty=nameWithType></li></ul>|

