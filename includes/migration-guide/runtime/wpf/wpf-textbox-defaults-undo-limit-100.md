### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a><span data-ttu-id="56ced-101">WPF TextBox 기본값 제한인 100 개를 실행 취소 하려면</span><span class="sxs-lookup"><span data-stu-id="56ced-101">WPF TextBox defaults to undo limit of 100</span></span>

|   |   |
|---|---|
|<span data-ttu-id="56ced-102">설명</span><span class="sxs-lookup"><span data-stu-id="56ced-102">Details</span></span>|<span data-ttu-id="56ced-103">.NET 4.5에서는 WPF TextBox에 대한 실행 취소 제한 기본값은 100(.NET 4.0에서 무제한이던 것과 반대)</span><span class="sxs-lookup"><span data-stu-id="56ced-103">In .NET 4.5, the default undo limit for a WPF textbox is 100 (as opposed to being unlimited in .NET 4.0)</span></span>|
|<span data-ttu-id="56ced-104">제안 해결 방법</span><span class="sxs-lookup"><span data-stu-id="56ced-104">Suggestion</span></span>|<span data-ttu-id="56ced-105">사용 제한은 실행 취소 제한 100 너무 낮으면 명시적으로 설정할 수 있습니다. <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit></span><span class="sxs-lookup"><span data-stu-id="56ced-105">If an undo limit of 100 is too low, the limit can be set explicitly with <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit></span></span>|
|<span data-ttu-id="56ced-106">범위</span><span class="sxs-lookup"><span data-stu-id="56ced-106">Scope</span></span>|<span data-ttu-id="56ced-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="56ced-107">Edge</span></span>|
|<span data-ttu-id="56ced-108">버전</span><span class="sxs-lookup"><span data-stu-id="56ced-108">Version</span></span>|<span data-ttu-id="56ced-109">4.5</span><span class="sxs-lookup"><span data-stu-id="56ced-109">4.5</span></span>|
|<span data-ttu-id="56ced-110">형식</span><span class="sxs-lookup"><span data-stu-id="56ced-110">Type</span></span>|<span data-ttu-id="56ced-111">런타임</span><span class="sxs-lookup"><span data-stu-id="56ced-111">Runtime</span></span>|
|<span data-ttu-id="56ced-112">영향을 받는 API</span><span class="sxs-lookup"><span data-stu-id="56ced-112">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

