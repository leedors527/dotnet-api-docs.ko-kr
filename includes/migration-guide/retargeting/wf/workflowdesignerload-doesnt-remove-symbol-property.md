### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load 기호 속성을 제거 하지 않음

|   |   |
|---|---|
|설명|워크플로 디자이너 및 사용 하 여 3.5 재 호스트 된 워크플로 로드 합니다..NET Framework 4.5를 대상으로 할 때는 <xref:System.Activities.Presentation.WorkflowDesigner.Load> 메서드를 한 <xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name> 워크플로 저장 하는 동안 throw 됩니다.|
|제안 해결 방법|설정 하 여 해결할 수 수 있도록 워크플로 디자이너에서.NET Framework 4.5를 대상으로 하는 경우에이 버그 매니페스트는 <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> 4.0.NET Framework.Alternatively에 문제를 피할 수 있습니다를 사용 하 여는 <xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)> 는 워크플로 로드 하는 메서드 대신 <xref:System.Activities.Presentation.WorkflowDesigner.Load>합니다.|
|범위|주요함|
|버전|4.5|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

