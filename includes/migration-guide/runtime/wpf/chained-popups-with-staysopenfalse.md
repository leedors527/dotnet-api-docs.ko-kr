### <a name="chained-popups-with-staysopenfalse"></a>연결로 StaysOpen 팝업 = False

|   |   |
|---|---|
|설명|StaysOpen 인 팝업 = False 닫히도록 팝업 외부를 클릭 해야 합니다. 이러한 팝업의 두 개 이상의 연결 된 경우 (즉, 하나에 있으면 다른) 등 많은 문제가 발생 했습니다.<ul><li>두 수준 열려 P2 외부 이지만 p 1의 내부를 클릭 합니다.  아무 반응이 없습니다.</li><li>두 수준 열려 외부 P1를 클릭 합니다.  두 팝업을 닫습니다.</li><li>시가 및 종가 두 수준입니다.  다음을 p 2를 다시 열어 봅니다.  아무 반응이 없습니다.</li><li>세 가지 수준 열어 보십시오.  당신은 할 수 없어요.  (아무 일도 발생 또는 클릭 한 위치에 따라 첫 두를 닫습니다.) 이러한 경우 (및 다른 변형) 정상적으로 작동 합니다.</li></ul>|
|범위|Microsoft Edge|
|버전|4.7.1|
|형식|런타임|
|영향을 받는 API|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|

