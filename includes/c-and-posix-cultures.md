---
ms.openlocfilehash: 92b3aa8ebf6a4c0d6968287fd09d84d4415d47f5
ms.sourcegitcommit: c58096d6814a25766abaf19020c7831e5c59ffc9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57665859"
---
> [!NOTE]
> <span data-ttu-id="6bde9-101">**Linux 및 macOS 시스템에서 실행되는 .NET Core만 해당:** C 및 Posix 문화권은 예상 유니코드 데이터 정렬 순서를 사용하지 않으므로 해당 문화권의 데이터 정렬 동작은 항상 대/소문자를 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="6bde9-101">**.NET Core running on Linux and macOS systems only:** The collation behavior for the C and Posix cultures is always case-sensitive because these cultures do not use the expected Unicode collation order.</span></span> <span data-ttu-id="6bde9-102">C 또는 Posix 이외의 문화권을 사용하여 문화권 구분, 대/소문자 비구분 정렬 작업을 수행하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6bde9-102">We recommend that you use a culture other than C or Posix for performing culture-sensitive, case-insensitive sorting operations.</span></span>  
