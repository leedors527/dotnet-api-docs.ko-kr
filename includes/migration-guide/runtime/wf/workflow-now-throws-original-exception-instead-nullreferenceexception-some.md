### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>워크플로 이제 경우에 따라 nullreferenceexception이 발생 하는 대신 원래 예외 throw

|   |   |
|---|---|
|설명|.NET Framework 4.6.2 및 이전 버전에서는 워크플로 활동의 Execute 메서드에서 사용 하 여 예외를 throw 하는 경우에 <code>null</code> 값에 대 한는 <xref:System.Exception.Message> 속성 System.Activities 워크플로 런타임에서 throw는 <xref:System.NullReferenceException?displayProperty=name>, 마스크는 원래 예외입니다. .NET Framework 4.7에서 이전에 마스크 된 예외가 throw 됩니다.|
|제안 해결 방법|코드에서 처리에 의존 하는 경우는 <xref:System.NullReferenceException?displayProperty=name>, 사용자 지정 작업에서 throw 될 수 있는 예외를 catch 하도록 변경 합니다.|
|범위|부|
|버전|4.7|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

