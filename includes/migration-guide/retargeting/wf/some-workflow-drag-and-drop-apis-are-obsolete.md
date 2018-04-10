### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a>일부 워크플로 끌어서 놓기 Api 사용 되지 않습니다.

|   |   |
|---|---|
|설명|이 워크플로 끌어서 놓기 API 사용 되지 않으며 4.5에 대해 응용 프로그램은 다시 작성 하는 경우 컴파일러 경고가 발생 합니다.|
|제안 해결 방법|새 <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> 여러 개체에 대 한 작업을 지 원하는 Api를 대신 사용 해야 합니다. 또는 빌드 경고를 표시하지 않거나 이전 컴파일러를 사용하여 방지할 수 있습니다. API는 계속 지원됩니다.|
|범위|부|
|버전|4.5|
|형식|대상 변경|
|영향을 받는 API|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|

