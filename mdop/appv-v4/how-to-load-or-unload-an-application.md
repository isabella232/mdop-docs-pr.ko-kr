---
title: 응용 프로그램을 로드 또는 언로드하는 방법
description: 응용 프로그램을 로드 또는 언로드하는 방법
author: dansimp
ms.assetid: 8c149761-c591-433f-972b-91793a69c654
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb99b1f38034ccb7bc16b2c8ebdcfa1cc8b36a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817233"
---
# <span data-ttu-id="71890-103">응용 프로그램을 로드 또는 언로드하는 방법</span><span class="sxs-lookup"><span data-stu-id="71890-103">How to Load or Unload an Application</span></span>


<span data-ttu-id="71890-104">다음 절차를 사용 하 여 응용 프로그램 가상화 클라이언트 관리 콘솔에서 **응용** 프로그램 노드의 **결과** 창에 있는 응용 프로그램을 캐시에서 직접 로드 하거나 언로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71890-104">You can use the following procedures to load or unload an application from the cache, directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="71890-105">이 노드를 선택 하면 **결과** 창에 응용 프로그램 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71890-105">When you select this node, the **Results** pane displays a list of applications.</span></span>

<span data-ttu-id="71890-106">**참고**  패키지를 로드 하거나 언로드하면 패키지의 모든 응용 프로그램이 캐시에서 로드 되거나 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71890-106">**Note** When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span> <span data-ttu-id="71890-107">패키지를 로드할 때 캐시에 응용 프로그램을 로드 하는 데 적절 한 공간이 없는 경우 캐시 크기를 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="71890-107">When loading a package, if you do not have adequate space in cache to load the applications, increase your cache size.</span></span> <span data-ttu-id="71890-108">캐시 크기에 대 한 자세한 내용은 [캐시 크기 및 드라이브 문자 지정을 변경 하는 방법을](how-to-change-the-cache-size-and-the-drive-letter-designation.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="71890-108">For more information about cache size, see [How to Change the Cache Size and the Drive Letter Designation](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span></span>

 

**<span data-ttu-id="71890-109">응용 프로그램을 로드 하려면</span><span class="sxs-lookup"><span data-stu-id="71890-109">To load an application</span></span>**

1.  <span data-ttu-id="71890-110">커서를 **결과** 창으로 이동 하 고 원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 한 다음 팝업 메뉴에서 **로드** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="71890-110">Move the cursor to the **Results** pane, right-click the desired application, and select **Load** from the pop-up menu.</span></span>

2.  <span data-ttu-id="71890-111">응용 프로그램이 자동으로 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71890-111">The application is automatically loaded.</span></span> <span data-ttu-id="71890-112">진행률은 **패키지 상태**레이블이 붙은 열에서 추적 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71890-112">The progress is tracked in the column labeled **Package Status**.</span></span> <span data-ttu-id="71890-113">로드가 완료 되었는지 확인 하거나 진행률을 확인 하려면 보기를 새로 고쳐야 합니다.</span><span class="sxs-lookup"><span data-stu-id="71890-113">You must refresh the view to see that the load is complete or to see the progress.</span></span>

**<span data-ttu-id="71890-114">응용 프로그램을 언로드하려면</span><span class="sxs-lookup"><span data-stu-id="71890-114">To unload an application</span></span>**

1.  <span data-ttu-id="71890-115">커서를 **결과** 창으로 이동 하 고 원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 한 다음 팝업 메뉴에서 **언로드** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="71890-115">Move the cursor to the **Results** pane, right-click the desired application, and select **Unload** from the pop-up menu.</span></span>

2.  <span data-ttu-id="71890-116">응용 프로그램이 자동으로 언로드되고, **패키지 상태** 열이 업데이트 되어 변경 내용이 반영 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71890-116">The application is automatically unloaded, and the **Package Status** column is updated to reflect the change.</span></span>

## <span data-ttu-id="71890-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="71890-117">Related topics</span></span>


[<span data-ttu-id="71890-118">캐시 크기 및 드라이브 문자 지정을 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="71890-118">How to Change the Cache Size and the Drive Letter Designation</span></span>](how-to-change-the-cache-size-and-the-drive-letter-designation.md)

 

 





